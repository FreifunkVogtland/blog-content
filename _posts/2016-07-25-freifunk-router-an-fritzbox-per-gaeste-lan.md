---
post_title: Freifunk-Router an Fritzbox per Gäste-LAN
author: Enno
post_date: 2016-07-25 23:58:29
post_excerpt: ""
layout: post
published: true
---
Wenn man Beseitzer einer aktuellen FritzBox und der Option ein Gästenetzwerk an dem LAN-Port 4 schalten kann, ist es damit möglich die Bandbreite eines Ferifunk-Routers einfach automatisch drosseln zulassen. Somit haben alle Verbindungen im eigenen Netzwerk Vorrang und sollte der Download oder das Streaming beendet werden, wird wieder mehr Bandbreite für den Freifunk-Router freigegeben.

<!--more-->

Einrichtung:
<ol>
 	<li>FritzBox per http://fritz.box öffnen</li>
 	<li>evtl. Anmeldedaten eingeben</li>
 	<li>Über das Menü "Internet" -&gt; "Filter"  die "Listen" öffnen</li>
 	<li>Filterliste "alles außer Surfen und Mailen öffnen"</li>
 	<li>Die Einstellungen des Bildes übernehmen
<img class="aligncenter wp-image-10 size-large" src="http://blog.soapbubbles.de/wp-content/uploads/2016/07/wp_ss_20160725_0001-e1469483298200-622x1024.png" alt="wp_ss_20160725_0001" width="622" height="1024" />
Achtung: Ich habe in meiner Einstellung das Häkchen bei "E-Mail-Filter über Port 25 aktiv" aktiviert, d.H. es können Mails nur mittels SSL Versand werden. Somit sind in dem Bild die Ports 25 und 110 nicht ausgeschlossen.</li>
 	<li>Änderungen an der Liste speichern</li>
 	<li>evtl. den Namen der Liste noch ändern in "alles außer Surfen und Mailen und Freifunk"</li>
 	<li>Danach über das Menü "Internet" -&gt; "Filter" die "Zugangsprofile" öffnen und im Profil "Gast" die Netzwerkanwendung "alles außer Surfen und Mailen und Freifunk" wählen und den Filter für Internetseiten deaktivieren
<img class="aligncenter wp-image-11 size-large" src="http://blog.soapbubbles.de/wp-content/uploads/2016/07/wp_ss_20160725_0002-e1469483277520-626x1024.png" alt="wp_ss_20160725_0002" width="626" height="1024" /></li>
 	<li>Nun geht es zum "Heimnetzwerk" -&gt; "Heimnetzübersicht" zu dem Reiter "Netzwerkeinstellungen"</li>
 	<li>In den "Netzwerkeinstellungen" das Häkchen bei "Gastzugang für LAN 4 aktiv"
<img class="wp-image-12 size-large aligncenter" src="http://blog.soapbubbles.de/wp-content/uploads/2016/07/wp_ss_20160725_0003-e1469483331447-623x1024.png" alt="wp_ss_20160725_0003" width="623" height="1024" /></li>
 	<li>evtl. das Häkchen bei "Anmeldung am Gastzugang nur nach Zustimmung zu den Nutzungsbedingungen gestatten" entfernen</li>
 	<li>Freifunk-Router an den LAN 4 anschließen und einschalten</li>
 	<li>der Freifunk-Router sollte sich nun automatisch mit dem Freifunk-Netz verbinden und fertig ist es :)</li>
</ol>
&nbsp;

Nun hat man eine automatische Anpassung der Bandbreite für Freifunk.
