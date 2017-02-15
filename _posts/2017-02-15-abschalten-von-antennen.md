---
ID: 654
post_title: Abschalten von Antennen
author: andre
post_date: 2017-02-15 12:26:20
post_excerpt: ""
layout: post
permalink: http://vogtland.freifunk.net/?p=654
published: true
vantage_panels_no_legacy:
  - 'true'
siteorigin_page_settings:
  - 'a:6:{s:6:"layout";s:7:"default";s:15:"masthead_margin";b:1;s:13:"footer_margin";b:1;s:10:"page_title";b:0;s:13:"hide_masthead";b:0;s:19:"hide_footer_widgets";b:0;}'
---
Hier eine kurze Anleitung zum Abschalten von Antennen beim TP-Link TL-WR842ND. Dies kann notwendig sein, wenn Du zum Beispiel eine Antenne außen nutzen möchtest. Der TP-Link TL-WR842ND nutzt in seiner normalen Konfiguration das MIMO Verfahren. Wenn man Änderungen an den Antennen vornimmt, sollte man dies deaktivieren, indem man eine der beiden Antennen deaktiviert. Ansonsten kann es zur Verschlechterung der Sende-/Empfangsstärke des Routers kommen.

Erst einmal zum Auslesen der Signalstaerke:

<code>root@PL-See68-DG:~# iw dev ibss0 station dump
Station f6:f5:6e:c1:fa:ea (on ibss0)
	inactive time:  5160 ms
	rx bytes:       244
	rx packets:     2
	tx bytes:       0
	tx packets:     0
	tx retries:     0
	tx failed:      0
	signal:         -88 [-88, -96] dBm
	signal avg:     -87 [-88, -96] dBm
	tx bitrate:     1.0 MBit/s
	rx bitrate:     1.0 MBit/s
	authorized:     yes
	authenticated:  yes
	preamble:       long
	WMM/WME:        yes
	MFP:            no
	TDLS peer:      no
	connected time: 5 seconds</code>

Hier wurde das Mesh-Interface (<code>ibss0</code>) getestet. Du kannst auch einen Test-Client mit dem AccessPoint verbinden, nutze dann bitte <code>client0</code> anstelle von <code>ibss0</code>.

Interessant sind folgende zwei Zeilen (also das in den <code>[...]</code>-Klammern):

<code>	signal:         -88 [-88, -96] dBm
	signal avg:     -87 [-88, -96] dBm</code>

Nehmen wir an, dass dein Router den anderen Router via Mesh-Interface (<code>ibss0</code>), oder deinen Test-Client (<code>client0</code>) mit der Antenne ausserhalb des Fensters besser "sehen" müsste. Also wissen wir nun, dass -88 der höhere Wert ist und das dies die 1. Antenne ist. Jetzt müssen wir eine Bitmaske erstellen bei der nur das <code>0.</code> Bit (1. Antenne) aktiviert ist und damit alle anderen Antennen deaktiviert sind: 

<code>b00000001</code> -> in Dezimalform: <code>1</code>

Die Dezimalform müssen wir nun für das WiFi Device (<code>radio0</code>) eintragen:

<code>uci set wireless.radio0.rxantenna='1'
uci set wireless.radio0.txantenna='1'
uci commit
wifi</code>

Beim Ueberpruefen, sieht man nun, dass nur eine Antenne aktiviert ist und das es ungefaehr die selben Werte wie die "beste" Antenne im letzten Test liefert.

<code>root@PL-See68-DG:~# iw dev ibss0 station dump
Station f6:f5:6e:c1:fa:ea (on ibss0)
	inactive time:  0 ms
	rx bytes:       5656263
	rx packets:     51340
	tx bytes:       64247
	tx packets:     553
	tx retries:     747
	tx failed:      0
	signal:         -86 [-86] dBm
	signal avg:     -85 [-85] dBm
	tx bitrate:     21.7 MBit/s MCS 2 short GI
	rx bitrate:     11.0 MBit/s
	expected throughput:    7.48Mbps
	authorized:     yes
	authenticated:  yes
	preamble:       long
	WMM/WME:        yes
	MFP:            no
	TDLS peer:      no
	connected time: 1007 seconds</code>