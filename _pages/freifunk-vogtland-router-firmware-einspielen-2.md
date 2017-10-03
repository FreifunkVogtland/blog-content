---
ID: 441
post_title: >
  Freifunk Vogtland Router Firmware
  installieren – UniFi AP AC
author: andre
post_excerpt: ""
layout: page
permalink: >
  https://vogtland.freifunk.net/freifunk-vogtland-router-firmware-einspielen-2/
published: true
post_date: 2016-11-30 18:04:47
---
Schritt für Schritt Anleitung für die Neuinstallation der Freifunk Vogtland Firmware auf einem Ubiquiti <span class="itemreviewed fn">UniFi AP AC (Lite &amp; Pro) mit originaler Firmware. Bitte lade dazu das "<a href="http://firmware.freifunk-vogtland.net/firmware/stable/sysupgrade/" target="_blank" rel="noopener">sysupgrade</a>" Firmware Image herunter.
</span>

<span style="color: #dc0067;"><strong>Achtung: Diese Anleitung nur nutzen, wenn du den Router im Vogtland betreiben möchtest!</strong></span>

<span style="color: #dc0067;">Außerhalb des Vogtlandes wird das Mesh nicht funktionieren und wir haben viel Arbeit damit, Leute anzuschreiben und zu erklären, dass Freifunk dezentral ist. Die dir nächstgelegene Gemeinde findest du unter <a style="color: #dc0067;" href="https://freifunk.net/community-finden/">https://freifunk.net/community-finden/</a>, bitte erkundige dich dort nach der passenden Firmware für deinen Router.</span>

<img class="so-widget-image" title="unifi_900" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/12/UniFi_900.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/12/UniFi_900.png 900w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/12/UniFi_900-300x261.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/12/UniFi_900-768x668.png 768w" width="900" height="783" />
<h2>Einleitung</h2>
Um einen Router als Freifunk Router zu nutzen, ist es erforderlich dort das Freifunk Betriebssystem – die Freifunk Firmware – zu installieren.

Die Installation ist ganz einfach und Du benötigst keine technischen Kenntnisse. Wenn du dieser Anleitung folgst kann eigentlich nichts schiefgehen. Los geht's!
<h2>1. Freifunk-Router mit dem Computer verbinden</h2>
Um mit deinem Router kommunizieren zu können, musst du deinem PC eine statische IP-Adresse vergeben. Da der Router selbst die 192.168.1.20 belegt, vergibst du am besten die <strong>192.168.1.21</strong>.

Dein Router wird über ein Lan-Kabel mit Strom versorgt, dies nennt man "Power over Ethernet", kurz POE. Das Lan-Kabel wird dazu durch ein Netzteil geschleift. Mit dem beiliegenden Netzkabel schließt du das Netzteil jetzt an eine Steckdose an.

Verbinde dann den Router mit dem POE Port des Netzteils. Den LAN Port des Netzteiles verbindest du mit deinem Rechner.
<h2>2. Firmware herunterladen</h2>
Während dein Router nun startet, kannst du die Freifunk Firmware herunter laden. Lade bitte die Firmware mit dem Name "gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin" herunter.
<h2>3. Firmware einspielen</h2>
<span id="result_box" class="" lang="de"><span class="">Öffne nun eine SSH-Sitzung zur orginalen Firmware (Benutzer: ubnt, Pswd: ubnt).</span> D<span class="">er AP hat die IP 192.168.1.20</span></span>

Kopiere nun das heruntergeladene sysupgrade image mittels scp in das temporäre Verzeichnis des Router:
<blockquote>
<p class="code">scp gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin ubnt@192.168.1.20:/tmp/</p>
</blockquote>
<h3 id="unifi_ap_ac_lite_devices">UniFi AP AC Lite Geräte</h3>
<span id="result_box" class="" lang="de"><span class="">Führen in der SSH-Sitzung den folgenden Befehl aus, um die primäre Firmware-Partition durch die Freifunk Vogtland Firmware zu ersetzen:</span></span>
<blockquote>
<p class="code"># mtd -r kernel0<strong> </strong>write /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin kernel0
kernel0 Unlocking kernel0 ... Writing from /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin to kernel0 ... Rebooting ...</p>
</blockquote>
<h3 class="code">UniFi AP AC LR und UniFi AP AC Pro Geräte</h3>
<p class="code"><span id="result_box" class="" lang="de">Das Ausführen des oben genannten mtd Befehls funktioniert nicht für das UniFi AP AC <strong>LR</strong>-Modell. Es wird kein Schaden angerichtet, nach dem Neustart wird die originale Firmware wieder ausgeführt. <span class="">Allerdings funktioniert es mit kernel<strong>1</strong> anstelle von kernel<strong>0</strong>:
</span></span></p>

<blockquote>
<p class="code"># mtd -r -e kernel1 write /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin kernel1
Unlocking kernel1 ... Erasing kernel1 ... Writing from /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin to kernel1 ...</p>
</blockquote>
<h2>4. Abschluss</h2>
Nachdem die Firmware fertig eingespielt ist, startet der Router neu. Wenn danach der runde Kreis dauerhaft leuchtet, ist der Router einsatzbereit.

Jetzt ist der Router nicht mehr unter der (oben) angegeben Adresse erreichbar. Das ist gut so. Denn nun läuft nicht mehr die alte Firmware, sondern die neue Freifunk Firmware auf deinem Router.

Vergiss nicht deinen PC wieder auf DHCP umzustellen!

&nbsp;

Nun kannst du deinen Router noch konfigurieren, sodass er auf der Freifunk-Karte angezeigt wird, oder direkt an das Internet anschließen und nutzen.

Wenn du deinen Router noch richtig konfigurierst, hilfst du uns dabei das Netz zu planen und zu optimieren, zeigst anderen wo sich dein Router befindet und siehst selbst, wie und wann dein Router genutzt wird. Das Konfigurieren deines Routers ist ganz einfach, eine Anleitung dazu findest du <a href="http://freifunk-vogtland.net/?page_id=166">auf dieser Seite</a>.

Wenn Du deinen Router ohne Konfiguration nutzen möchtest, dann schließe bitte jetzt den Router an das Internet an. Dazu verbindest du die blaue Buchse deines neuen Freifunk-Routers mithilfe eines Netzwerkkabels mit Deinem Internet-Router.
<h2>Fragen?</h2>
Solltest Du Fragen oder Probleme haben oder Einträge deines Knoten ändern wollen, schreibe uns bitte eine Nachricht. Unsere Kontaktmöglichkeiten findest du <a href="http://vogtland.freifunk.net/?page_id=251">hier</a>.