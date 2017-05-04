---
ID: 853
post_title: >
  Gluon Konfiguration exportieren und
  importieren (per SSH)
author: andre
post_date: 2017-05-04 23:24:56
post_excerpt: ""
layout: post
permalink: >
  https://vogtland.freifunk.net/gluon-konfiguration-exportieren-und-importieren-per-ssh/
published: true
vantage_panels_no_legacy:
  - 'true'
siteorigin_page_settings:
  - 'a:6:{s:6:"layout";s:7:"default";s:10:"page_title";b:1;s:15:"masthead_margin";b:1;s:13:"footer_margin";b:1;s:13:"hide_masthead";b:0;s:19:"hide_footer_widgets";b:0;}'
---
Manchmal möchte man etwas an seinem Router konfigurieren, ist sich allerdings nicht sicher, ob es funktioniert. Oder man möchte einfach mal schauen, welche Möglichkeiten es denn gibt. ;)

Ich beschreibe euch hier kurz, wie ihr die Konfiguration eures Routers exportieren und auf euren lokalen PC laden könnt. Und auch, wie ihr die Konfiguration wieder auf den Router übertragt und importiert.

Diese Anleitung, setzt den Kommandozeilen-Befehl "scp" voraus. Der Befehl ist auf Linux und Apple Macs in der Konsole vorhanden. Auf Windows nutzt ihr bitte die alternative Kommandozeile "cmder" oder das Programm WinSCP.

Bitte verbindet euch per SSH mit eurem Freifunk Router. Die IPv6-Adresse und die lokalen Pfade ersetzt ihr bitte durch eure eigenen. ;)

Nun exportiert ihr die Konfiguration auf eurem Router in eine Datei:
<code>uci export > /config.uci</code>

Danach öffnet ihr eine Konsole auf eurem PC (oder Mac) und ladet euch die exportierte Konfiguration mittels SCP wie folgt herunter:
<code>scp root@[2001:bc8:3f13:ffc2:6670:2ff:febe:85be]:/config.uci /Users/sunbox/Desktop</code>

Nun könnt ihr euch die Konfiguration anschauen, oder auch ändern. Nachfolgend die Befehle, um diese wieder zu importieren.

Auf eurem lokalen PC den folgenden Befehl ausführen, um die Konfigurationsdatei wieder auf den Router zu laden:
<code>scp /Users/sunbox/Desktop/config.uci root@[2001:bc8:3f13:ffc2:6670:2ff:febe:85be]:/</code>

Nun führt ihr folgenden Befehl auf dem Router aus, um die Konfiguration aus der Datei wieder zu importieren:
<code>cat /config.uci | uci import</code>

Zum Schluß noch die temporäre Konfigurationsdatei auf dem Router löschen:
<code>rm /config.uci</code>