---
ID: 877
post_title: >
  Plauen – Freifunk im Heinrichs und in
  der Matsch
author: andre
post_excerpt: ""
layout: post
permalink: >
  https://vogtland.freifunk.net/plauen-freifunk-im-heinrichs-und-in-der-matsch/
published: true
post_date: 2017-05-29 22:05:40
---
<h3>Freier Datenverkehr für die Gäste</h3>

Das <a href="http://www.heinrichs-plauen.de/" target="_blank">Heinrichs</a> und die <a href="https://matsch-plauen.jimdo.com/" target="_blank">Matsch</a> in der Plauener Innenstadt bieten seit ein paar Tagen Freifunk für ihre Gäste<!--more--> und sind in das <a href="https://vogtland.freifunk.net/map/" target="_blank">Vogtland Freifunk Mesh</a> eingebunden. Die Gäste können damit frei ihren Online-Aktivitäten nachgehen, ohne sich in die Home-WLAN-Netzwerke der Gastronomie einloggen zu müssen - eine für beide Seiten vorteilhafte, sichere Lösung.


<h3>Situation vor der Installation</h3>

In beiden Gaststätten werden die Bestellungen über eine Cloud-basierte <a href="https://www.gastronovi.de/" target="_blank">POS Anwendung</a> mittels mobiler Clients (iOS, Android) aufgenommen. Aufgrund der massiven Steinmauern von bis zu einem Meter Dicke kommt es in den historischen Gebäuden bei der Bestands-Installation immer wieder zu Verbindungsabbrüchen zwischen den Clients und Access Points. Der Drucker für die Belege ist am lokalen Netz angeschlossen. Tischreservierungen werden Cloud-basiert mittels <a href="https://www.opentable.de/start/home" target="_blank">OpenTable</a> vorgenommen. Ein Gäste-WLAN ist nicht vorhanden.

Ziel der Neuausrichtung der WLAN-Installation ist  ein zuverlässiges Roaming der Clients zwischen den Access Points des Home-WLAN für die POS Anwendungen und das Angebot eines Gäste-WLAN. Von der Nutzung von Freifunk für das Gäste-WLAN und dessen Wert für das <a href="http://www.vogtland-tourismus.de/" target="_blank">Vogtland</a> ist der Betreiber der Gaststätten von Anfang an überzeugt. Freifunk bietet ihm zur Realisierung zwei Möglichkeiten an:


<h3>Variante 1 - Nutzung der bestehenden Router (verworfen)</h3>

Die erste Variante beinhaltet die Nutzung und den Ausbau der bestehenden Infrastruktur durch Aufspielen der Freifunk Firmware. Die Router würden dann als Freifunk-Knoten miteinander meshen und ein zweites Home-WLAN für POS bereitstellen. Diese Variante erfordert, dass alle Access Points per LAN mit dem DSL Router verbunden sind. Dies war jedoch nicht immer der Fall und eine nachträgliche LAN Installation ist in den gegebenen Räumlichkeiten sehr aufwändig. Bei einem Ausfall des WLAN wäre nicht nur Freifunk, sondern auch das Home-WLAN für die POS-Anwendung betroffen. Auch wenn die Verantwortung für den Betrieb laut <a href="http://www.picopeer.net/PPA-de.shtml" target="_blank">Pico Peering Agreement</a> beim Eigentümer und nicht bei Freifunk Vogtland liegt, sollte Freifunk Vogtland bei möglichen Ausfällen des Freifunk Backbones nicht in der Verantwortung für die Funktionsfähigkeit der POS-Anwendung stehen. 

<h3>Variante 2 - Freifunk als offenes (gekapseltes) Gäste-WLAN</h3>

Die zweite und gewählte Variante beinhaltet eine Neuinstallation mittels <a href="http://dl-origin.ubnt.com/datasheets/unifi/UniFi_AC_Mesh_DS.pdf" target="_blank">Ubiquiti Unifi Mesh Routern</a>. Die Unifi APs unterstützen Client-Roaming und erzeugen untereinander ein Mesh für das Home-WLAN. Dadurch wird ein stabiles und von Freifunk unabhängiges Home-WLAN für die POS-Anwendungen erzeugt. Freifunk wird als offenes (gekapseltes) Gäste-WLAN mittels VLAN bereitgestellt. Der Aufbau und die Installation folgt dabei der <a href="https://psi.cx/2017/unifi-ff-setup/" target="_blank">Anleitung von Christoph Weichert</a>. Der Uplink wird mittels Offloader am <a href="https://vogtland.freifunk.net/freifunk-router-an-fritzbox-per-gaeste-lan/" target="_blank">Gäste LAN Port des DSL Router</a> realisiert. Da die Ubiquiti Original-Firmware zum Einsatz kam, erweitern die APs leider nicht das Freifunk Mesh. Das Mesh zu anderen Knoten im <a href="https://vogtland.freifunk.net/map/" target="_blank">Mesh des Vogtland Freifunks</a> wird durch einen zusätzlichen Outdoor-Router und aufgespielte Vogtland Freifunk Firmware realisiert. 

<h3>Hardware pro Installation</h3>

Basisinstallation für Home-WLAN 
<ul>
 	<li style="font-weight: 400;">Ubiquiti UniFi AC Mesh Routern (4-6 je nach Situation vor Ort) (ca. 95€ pro Router)</li>
 	<li style="font-weight: 400;">Ubiquiti ToughSwitch 8 Port (ca. 175€)</li>
 	<li style="font-weight: 400;">Ubiquiti UniFi Cloud Key am Ubiquiti ToughSwitch (ca. 90€)</li>
 	<li style="font-weight: 400;">TP-Link TL-SG108E 8 Port Easy Smart Managed Switch (ca. 30€)</li>
</ul>

Freifunk
<ul>
 	<li style="font-weight: 400;">Futro S550 als Offloader (ca. 30€)</li>
 	<li style="font-weight: 400;">TP-Link CPE210 als Outdoor Freifunk Mesh Router im Heinrichs (ca. 55€)</li>
 	<li style="font-weight: 400;">Ubiquiti NSM2 als Outdoor Freifunk Mesh Router im Matsch/Café Heimweh (ca. 90€)</li>
</ul>

<h3>Ziel erreicht: zuverlässiges Roaming und freies Gäste-WLAN</h3>

Als Freifunk Vogtland haben wir bei der Auswahl der Geräte unterstützt und die Einrichtung des Freifunks am Switch, dem Offloader und dem Outdoor-Router vorgenommen. Das freie Gäste-WLAN über unser Freifunk-Netzwerk funktioniert nun sowohl im Heinrichs als auch in der Matsch bei zuverlässigem Roaming der Clients. Wir bedanken uns für das in Freifunk gesetzte Vertrauen, für die Bewirtung vor Ort und die Spende der Router aus der Bestands-Installation, auf denen wir Freifunk Vogtland installieren und die wir bei einem gemeinnützigen Verein aufstellen werden.