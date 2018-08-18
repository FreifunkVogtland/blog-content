---
ID: 654
post_title: Abschalten von Antennen
author: andre
post_excerpt: ""
layout: post
permalink: >
  https://vogtland.freifunk.net/abschalten-von-antennen/
published: true
post_date: 2017-02-15 12:26:20
---
Hier eine kurze Anleitung zum Abschalten von Antennen beim TP-Link TL-WR842ND. Dies kann notwendig sein, wenn Du zum Beispiel eine Antenne außen nutzen möchtest.<!--more--> Der TP-Link TL-WR842ND nutzt in seiner normalen Konfiguration das MIMO Verfahren. Wenn man Änderungen an den Antennen vornimmt, sollte man dies deaktivieren, indem man eine der beiden Antennen deaktiviert. Ansonsten kann es zur Verschlechterung der Sende-/Empfangsstärke des Routers kommen. Erst einmal zum Auslesen der Signalstaerke: 

`root@PL-See68-DG:~# iw dev ibss0 station dump
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
	connected time: 5 seconds` Hier wurde das Mesh-Interface (`ibss0`) getestet. Du kannst auch einen Test-Client mit dem AccessPoint verbinden, nutze dann bitte `client0` anstelle von `ibss0`. Interessant sind folgende zwei Zeilen (also das in den `[...]`-Klammern): `	signal:         -88 [-88, -96] dBm
	signal avg:     -87 [-88, -96] dBm` Nehmen wir an, dass dein Router den anderen Router via Mesh-Interface (`ibss0`), oder deinen Test-Client (`client0`) mit der Antenne ausserhalb des Fensters besser "sehen" müsste. Also wissen wir nun, dass -88 der höhere Wert ist und das dies die 1. Antenne ist. Jetzt müssen wir eine Bitmaske erstellen bei der nur das `0.` Bit (1. Antenne) aktiviert ist und damit alle anderen Antennen deaktiviert sind: `b00000001` -> in Dezimalform: `1` Die Dezimalform müssen wir nun für das WiFi Device (`radio0`) eintragen: `uci set wireless.radio0.rxantenna='1'
uci set wireless.radio0.txantenna='1'
uci commit
wifi` Beim Ueberpruefen, sieht man nun, dass nur eine Antenne aktiviert ist und das es ungefaehr die selben Werte wie die "beste" Antenne im letzten Test liefert. `root@PL-See68-DG:~# iw dev ibss0 station dump
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
	connected time: 1007 seconds`