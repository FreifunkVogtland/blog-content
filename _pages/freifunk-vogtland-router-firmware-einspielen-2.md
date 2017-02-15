---
ID: 441
post_title: >
  Freifunk Vogtland Router Firmware
  installieren – UniFi AP AC
author: andre
post_date: 2016-11-30 18:04:47
post_excerpt: ""
layout: page
permalink: >
  http://vogtland.freifunk.net/?page_id=441
published: true
panels_data:
  - |
    a:3:{s:7:"widgets";a:3:{i:0;a:6:{s:5:"title";s:0:"";s:4:"text";s:956:"<p>Schritt für Schritt Anleitung für die Neuinstallation der Freifunk Vogtland Firmware auf einem Ubiquiti <span class="itemreviewed fn">UniFi AP AC (Lite &amp; Pro) mit originaler Firmware. Bitte lade dazu das "<a href="http://firmware.freifunk-vogtland.net/firmware/stable/sysupgrade/" target="_blank">sysupgrade</a>" Firmware Image herunter.<br /></span></p><p><span style="color: #dc0067;"><strong>Achtung: Diese Anleitung nur nutzen, wenn du den Router im Vogtland betreiben möchtest!</strong></span></p><p><span style="color: #dc0067;">Außerhalb des Vogtlandes wird das Mesh nicht funktionieren und wir haben viel Arbeit damit, Leute anzuschreiben und zu erklären, dass Freifunk dezentral ist. Die dir nächstgelegene Gemeinde findest du unter <a style="color: #dc0067;" href="https://freifunk.net/community-finden/">https://freifunk.net/community-finden/</a>, bitte erkundige dich dort nach der passenden Firmware für deinen Router.</span></p>";s:20:"text_selected_editor";s:7:"tinymce";s:5:"autop";b:1;s:12:"_sow_form_id";s:13:"573c11fa51b35";s:11:"panels_info";a:7:{s:5:"class";s:31:"SiteOrigin_Widget_Editor_Widget";s:3:"raw";b:0;s:4:"grid";i:0;s:4:"cell";i:0;s:2:"id";i:0;s:9:"widget_id";s:36:"1f95dce2-215e-4b87-8eaa-05c2ccb21087";s:5:"style";a:1:{s:18:"background_display";s:4:"tile";}}}i:1;a:13:{s:5:"image";i:457;s:14:"image_fallback";s:0:"";s:4:"size";s:4:"full";s:5:"align";s:6:"center";s:5:"title";s:0:"";s:14:"title_position";s:6:"hidden";s:3:"alt";s:0:"";s:3:"url";s:0:"";s:5:"bound";b:1;s:10:"full_width";b:1;s:12:"_sow_form_id";s:13:"584532c586501";s:10:"new_window";b:0;s:11:"panels_info";a:7:{s:5:"class";s:30:"SiteOrigin_Widget_Image_Widget";s:3:"raw";b:0;s:4:"grid";i:0;s:4:"cell";i:0;s:2:"id";i:1;s:9:"widget_id";s:36:"265a419a-3025-4fed-a51c-bb00ffd06900";s:5:"style";a:1:{s:18:"background_display";s:4:"tile";}}}i:2;a:6:{s:5:"title";s:0:"";s:4:"text";s:4641:"<h2>Einleitung</h2><p>Um einen Router als Freifunk Router zu nutzen, ist es erforderlich dort das Freifunk Betriebssystem – die Freifunk Firmware – zu installieren.</p><p>Die Installation ist ganz einfach und Du benötigst keine technischen Kenntnisse. Wenn du dieser Anleitung folgst kann eigentlich nichts schiefgehen. Los geht's!</p><h2>1. Freifunk-Router mit dem Computer verbinden</h2><p>Um mit deinem Router kommunizieren zu können, musst du deinem PC eine statische IP-Adresse vergeben. Da der Router selbst die 192.168.1.20 belegt, vergibst du am besten die <strong>192.168.1.21</strong>.</p><p>Dein Router wird über ein Lan-Kabel mit Strom versorgt, dies nennt man "Power over Ethernet", kurz POE. Das Lan-Kabel wird dazu durch ein Netzteil geschleift. Mit dem beiliegenden Netzkabel schließt du das Netzteil jetzt an eine Steckdose an.</p><p>Verbinde dann den Router mit dem POE Port des Netzteils. Den LAN Port des Netzteiles verbindest du mit deinem Rechner.</p><div id="panel-337-0-0-8" class="so-panel widget widget_sow-editor" data-index="8"><div class="so-widget-sow-editor so-widget-sow-editor-base"><div class="siteorigin-widget-tinymce textwidget"><h2>2. Firmware herunterladen</h2><p>Während dein Router nun startet, kannst du die Freifunk Firmware herunter laden. Lade bitte die Firmware mit dem Name "gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin" herunter.</p><h2>3. Firmware einspielen</h2><p><span id="result_box" class="" lang="de"><span class="">Öffne nun eine SSH-Sitzung zur orginalen Firmware (Benutzer: ubnt, Pswd: ubnt).</span> D<span class="">er AP hat die IP 192.168.1.20</span></span></p><p>Kopiere nun das heruntergeladene sysupgrade image mittels scp in das temporäre Verzeichnis des Router:</p><div class="level4"><blockquote><p class="code">scp gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin ubnt@192.168.1.20:/tmp/</p></blockquote></div><h3 id="unifi_ap_ac_lite_devices">UniFi AP AC Lite und Pro Geräte</h3><p><span id="result_box" class="" lang="de"><span class="">Führen in der SSH-Sitzung den folgenden Befehl aus, um die primäre Firmware-Partition durch die Freifunk Vogtland Firmware zu ersetzen:</span></span></p><div class="level5"><blockquote><p class="code"># mtd -r write /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin kernel0<br /><br />Unlocking kernel0 ... <br />Writing from /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin to kernel0 ... <br />Rebooting ...</p></blockquote><div id="panel-337-0-0-23" class="so-panel widget widget_sow-editor" data-index="23"><div class="so-widget-sow-editor so-widget-sow-editor-base"><div class="siteorigin-widget-tinymce textwidget"><h2>4. Abschluss</h2><p>Nachdem die Firmware fertig eingespielt ist, startet der Router neu. Wenn danach der runde Kreis dauerhaft leuchtet, ist der Router einsatzbereit.</p><p>Jetzt ist der Router nicht mehr unter der (oben) angegeben Adresse erreichbar. Das ist gut so. Denn nun läuft nicht mehr die alte Firmware, sondern die neue Freifunk Firmware auf deinem Router.</p><div id="panel-337-0-0-27" class="so-panel widget widget_sow-editor" data-index="27"><div class="so-widget-sow-editor so-widget-sow-editor-base"><div class="siteorigin-widget-tinymce textwidget"><p>Vergiss nicht deinen PC wieder auf DHCP umzustellen!</p><p>Nun kannst du deinen Router noch konfigurieren, sodass er auf der Freifunk-Karte angezeigt wird, oder direkt an das Internet anschließen und nutzen.</p><p>Wenn du deinen Router noch richtig konfigurierst, hilfst du uns dabei das Netz zu planen und zu optimieren, zeigst anderen wo sich dein Router befindet und siehst selbst, wie und wann dein Router genutzt wird. Das Konfigurieren deines Routers ist ganz einfach, eine Anleitung dazu findest du <a href="http://freifunk-vogtland.net/?page_id=166">auf dieser Seite</a>.</p><p>Wenn Du deinen Router ohne Konfiguration nutzen möchtest, dann schließe bitte jetzt den Router an das Internet an. Dazu verbindest du die blaue Buchse deines neuen Freifunk-Routers mithilfe eines Netzwerkkabels mit Deinem Internet-Router.</p></div></div></div><div id="panel-337-0-0-28" class="so-panel widget widget_sow-editor panel-last-child" data-index="28"><div class="so-widget-sow-editor so-widget-sow-editor-base"><div class="siteorigin-widget-tinymce textwidget"><h2>Fragen?</h2><p>Solltest Du Fragen oder Probleme haben oder Einträge deines Knoten ändern wollen, schreibe uns bitte eine Nachricht. Unsere Kontaktmöglichkeiten findest du <a href="http://vogtland.freifunk.net/?page_id=251">hier</a>.</p></div></div></div></div></div></div></div></div></div></div>";s:20:"text_selected_editor";s:7:"tinymce";s:5:"autop";b:1;s:12:"_sow_form_id";s:13:"584532a02c39b";s:11:"panels_info";a:6:{s:5:"class";s:31:"SiteOrigin_Widget_Editor_Widget";s:4:"grid";i:0;s:4:"cell";i:0;s:2:"id";i:2;s:9:"widget_id";s:36:"1f95dce2-215e-4b87-8eaa-05c2ccb21087";s:5:"style";a:2:{s:27:"background_image_attachment";b:0;s:18:"background_display";s:4:"tile";}}}}s:5:"grids";a:1:{i:0;a:2:{s:5:"cells";i:1;s:5:"style";a:0:{}}}s:10:"grid_cells";a:1:{i:0;a:2:{s:4:"grid";i:0;s:6:"weight";i:1;}}}
---
Schritt für Schritt Anleitung für die Neuinstallation der Freifunk Vogtland Firmware auf einem Ubiquiti <span class="itemreviewed fn">UniFi AP AC (Lite &amp; Pro) mit originaler Firmware. Bitte lade dazu das "<a href="http://firmware.freifunk-vogtland.net/firmware/stable/sysupgrade/" target="_blank">sysupgrade</a>" Firmware Image herunter.
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
<p class="code"># mtd -r write /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin
kernel0 Unlocking kernel0 ... Writing from /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin to kernel0 ... Rebooting ...</p>
</blockquote>
<h3 class="code">UniFi AP AC LR und UniFi AP AC Pro Geräte</h3>
<p class="code"><span id="result_box" class="" lang="de">Das Ausführen des oben genannten mtd Befehls funktioniert nicht für das UniFi AP AC <strong>LR</strong>-Modell. Es wird kein Schaden angerichtet, nach dem Neustart wird die originale Firmware wieder ausgeführt. <span class="">Allerdings funktioniert es mit kernel<strong>1</strong> anstelle von kernel<strong>0</strong>:
</span></span></p>

<blockquote>
<p class="code"># mtd -r -e kernel1 write /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin
kernel1 Unlocking kernel1 ... Erasing kernel1 ... Writing from /tmp/gluon-ffv-xxxxxxxxx-v-ubiquiti-unifi-xx-xxxx-sysupgrade.bin to kernel1 ...</p>
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