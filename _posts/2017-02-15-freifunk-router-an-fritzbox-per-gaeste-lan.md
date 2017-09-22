---
ID: 691
post_title: >
  Freifunk-Router an Fritzbox per
  Gäste-LAN
author: Enno
post_excerpt: ""
layout: post
permalink: >
  https://vogtland.freifunk.net/freifunk-router-an-fritzbox-per-gaeste-lan/
published: true
post_date: 2017-02-15 18:47:42
---
Wenn man eine aktuellen FritzBox mit 4 LAN-Ports besitzt, ist es möglich, die Bandbreite eines Freifunk-Routers automatisch anpassen zulassen. Somit haben alle Verbindungen im eigenen Netzwerk Vorrang und sollte der Download oder das Streaming beendet werden, wird mehr Bandbreite dem Freifunk-Router zugewiesen.
<!--more-->

<h3>So geht's:</h3>

<ul>
<li>FritzBox per <code>http://fritz.box</code> öffnen</li>
<li>evtl. Anmeldedaten eingeben</li>
<li>Über das Menü "Internet" -&gt; "Filter" die "Listen" öffnen</li>
<li>Filterliste "alles außer Surfen und Mailen öffnen"</li>
<li>Die Einstellungen des Bildes übernehmen</li>
</ul>

<a href="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-01.png"><img src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-01-300x193.png" alt="" width="300" height="193" class="aligncenter size-medium wp-image-912" /></a>

<ul>
<li>Änderungen an der Liste speichern</li>
<li>evtl. den Namen der Liste noch ändern in „alles außer Surfen und Mailen und Freifunk“</li>
<li>Danach über das Menü „Internet“ -&gt; „Filter“ die „Zugangsprofile“ öffnen und im Profil „Gast“ die Netzwerkanwendung „alles außer Surfen und Mailen und Freifunk“ wählen und den Filter für Internetseiten deaktivieren</li>
</ul>

<a href="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-02.png"><img src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-02-300x193.png" alt="" width="300" height="193" class="aligncenter size-medium wp-image-913" /></a>

<ul>
<li>Nun geht es zum „Heimnetzwerk“ -&gt; „Heimnetzübersicht“ zu dem Reiter „Netzwerkeinstellungen“</li>
<li>In den „Netzwerkeinstellungen“ das Häkchen bei „Gastzugang für LAN 4 aktiv“</li>
</ul>

<a href="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-04.png"><img src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-04-300x193.png" alt="" width="300" height="193" class="aligncenter size-medium wp-image-916" /></a>

<ul>
<li>evtl. das Häkchen bei „Anmeldung am Gastzugang nur nach Zustimmung zu den Nutzungsbedingungen gestatten“ entfernen</li>
<li>Freifunk-Router an den LAN 4 anschließen und einschalten</li>
<li><span class="s2">der Freifunk-Router sollte sich nun automatisch mit dem Freifunk-Netz verbinden und fertig ist es</li>
</ul>

Nun hat man eine automatische Anpassung der Bandbreite für Freifunk.