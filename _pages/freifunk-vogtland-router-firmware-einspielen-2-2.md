---
ID: 337
post_title: >
  Freifunk Vogtland Router Firmware
  installieren – PicoStation
author: andre
post_excerpt: ""
layout: page
permalink: >
  https://vogtland.freifunk.net/freifunk-vogtland-router-firmware-einspielen-2-2/
published: true
post_date: 2016-08-09 20:29:03
---
Schritt für Schritt Anleitung für die Neuinstallation der Freifunk Vogtland Firmware auf einer Ubiquiti PicoStation<span class="itemreviewed fn"> mit originaler Firmware. Bitte lade dazu das "<a href="http://firmware.freifunk-vogtland.net/firmware/stable/factory/" target="_blank">factory</a>" Firmware Image herunter.
Falls du auf deinem Router bereits eine andere Freifunk Firmware, oder eine offene Router Firmware wie OpenWRT installiert hast, benutze bitte ein "<a href="http://firmware.freifunk-vogtland.net/firmware/stable/sysupgrade/" target="_blank">sysupgrade</a>" anstelle des "factory" Firmware Image.
</span>

<span style="color: #dc0067;"><strong>Achtung: Diese Anleitung nur nutzen, wenn du den Router im Vogtland betreiben möchtest!</strong></span>

<span style="color: #dc0067;">Außerhalb des Vogtlandes wird das Mesh nicht funktionieren und wir haben viel Arbeit damit, Leute anzuschreiben und zu erklären, dass Freifunk dezentral ist. Die dir nächstgelegene Gemeinde findest du unter <a style="color: #dc0067;" href="https://freifunk.net/community-finden/">https://freifunk.net/community-finden/</a>, bitte erkundige dich dort nach der passenden Firmware für deinen Router.</span>
<h2>Einleitung</h2>
Um einen Router als Freifunk Router zu nutzen, ist es erforderlich dort das Freifunk Betriebssystem – die Freifunk Firmware – zu installieren.

Die Installation ist ganz einfach und Du benötigst keine technischen Kenntnisse. Wenn du dieser Anleitung folgst kann eigentlich nichts schiefgehen. Los geht's!
<h2>1. Freifunk-Router mit dem Computer verbinden</h2>
&nbsp;

<img class="so-widget-image" title="picostation-pc-change-static-ip" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-change-static-ip.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-change-static-ip.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-change-static-ip-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-change-static-ip-768x678.png 768w" width="832" height="735" />

Um mit deinem Router kommunizieren zu können, musst du deinem PC eine statische IP-Adresse vergeben. Da der Router selbst die 192.168.1.20 belegt, vergibst du am besten die <span style="color: #dc0067;"><strong>192.168.1.21</strong></span>.

<img class="so-widget-image" title="picostation-and-stuff" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-and-stuff.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-and-stuff.png 2612w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-and-stuff-300x194.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-and-stuff-768x497.png 768w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-and-stuff-1024x663.png 1024w" width="2612" height="1692" />

Schraube bitte die beiliegende Antenne <span style="color: #dc0067;"><strong>(2) </strong></span>auf deinen Router <span style="color: #dc0067;"><strong>(1)</strong></span>. Mit den Schrauben <span style="color: #dc0067;"><strong>(7)</strong></span> und der Adapterplatte <span style="color: #dc0067;"><strong>(6)</strong></span> kannst du deinen Router irgendwo anschrauben. Ansonsten kannst du den Kabelbinder <span style="color: #dc0067;"><strong>(5)</strong></span> ohne Adapterplatte benutzen.

&nbsp;

<img class="so-widget-image" title="picostation-connect-antenna" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-connect-antenna.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-connect-antenna.png 3072w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-connect-antenna-300x169.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-connect-antenna-768x432.png 768w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-connect-antenna-1024x576.png 1024w" width="3072" height="1728" />

Dein Router wird über ein Lan-Kabel mit Strom versorgt, dies nennt man "Power over Ethernet", kurz POE. Das Lan-Kabel wird dazu durch ein Netzteil <span style="color: #dc0067;"><strong>(3)</strong></span> geschleift. Mit dem beiliegenden Netzkabel <span style="color: #dc0067;"><strong>(4)</strong></span> schließt du das Netzteil jetzt an eine Steckdose an.

Verbinde dann den Router mit dem POE Port des Netzteils. Den LAN Port des Netzteiles verbindest du mit deinem Rechner.

&nbsp;

<img class="so-widget-image" title="picostation-poe-lan" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan.png 3072w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan-300x169.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan-768x432.png 768w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan-1024x576.png 1024w" width="3072" height="1728" />
<h2>2. Firmware herunterladen</h2>
Während dein Router nun startet, kannst du die Freifunk Firmware herunter laden. Für die PicoStation gibt es nur eine Firmware-Version, lade bitte die Firmware mit dem Name "gluon-ffv-b20xxxxxx-v-ubiquiti-picostation-m.bin" herunter.

<img class="so-widget-image" title="picostation-accept-ssl-certificate" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-accept-ssl-certificate.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-accept-ssl-certificate.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-accept-ssl-certificate-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-accept-ssl-certificate-768x678.png 768w" width="832" height="735" />

Gib nun in deinem Browser die IP-Adresse des Routers ein, es ist die https://192.168.1.20. Wenn du eine Meldung bekommst, dass das SSL-Zertifikat ungültig ist, bestätige bitte die Ausnahme dafür.
<h2>3. Firmware einspielen</h2>
Jetzt kannst du den Router einfach über den Browser konfigurieren.

Bevor du weitermachst, musst du dich erst anmelden. Die wenig inspirierte Username / Passwort Kombination ist: ubnt / ubnt

<img class="so-widget-image" title="picostation-first-login" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-login.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-login.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-login-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-login-768x678.png 768w" width="832" height="735" />

Dein Browserfenster müsste nun so aussehen – Öffne hier dem Tab "System".

<img class="so-widget-image" title="picostation-choose-file" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-choose-file.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-choose-file.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-choose-file-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-choose-file-768x678.png 768w" width="832" height="735" />

Als nächstes wählst du die vorhin (in Schritt 2) geladene Datei zum Hochladen aus.

<img class="so-widget-image" title="picostation-upload-file" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-upload-file.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-upload-file.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-upload-file-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-upload-file-768x678.png 768w" width="832" height="735" />

Danach klickst du auf "Hochladen".

<img class="so-widget-image" title="picostation-perform-update" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-perform-update.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-perform-update.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-perform-update-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-perform-update-768x678.png 768w" width="832" height="735" />

Mit einem Klick auf "Aktualisieren" beginnt der Installationsprozess.

<img class="so-widget-image" title="picostation-wait-for-update-to-finish" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-wait-for-update-to-finish.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-wait-for-update-to-finish.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-wait-for-update-to-finish-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-wait-for-update-to-finish-768x678.png 768w" width="832" height="735" />

Warte nun bis der Balken zum Ende gelaufen ist. Der Router wird in dieser Zeit mehrmals neu starten. Während die Installation läuft, zieh bitte auf keinen Fall einen der Stecker – denn dann ist dein Router hinüber!

<img class="so-widget-image" title="picostation-update-finished" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-update-finished.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-update-finished.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-update-finished-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-update-finished-768x678.png 768w" width="832" height="735" />

Wenn du dieses Bild siehst ist der Installationsprozess abgeschlossen.
<h2>4. Abschluss</h2>
Nachdem die Firmware fertig eingespielt ist, startet der Router neu. Wenn danach die Lämpchen wie in folgendem Bild blinken, ist der Router einsatzbereit.

<img class="so-widget-image" title="picostation-first-start" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-start.jpg" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-start.jpg 3072w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-start-300x169.jpg 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-start-768x432.jpg 768w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-first-start-1024x576.jpg 1024w" width="3072" height="1728" />

Jetzt ist der Router nicht mehr unter der (oben) angegeben Adresse erreichbar. Das ist gut so. Denn nun läuft nicht mehr die alte Firmware, sondern die neue Freifunk Firmware auf deinem Router.

<img class="so-widget-image" title="picostation-pc-dhcp" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-dhcp.png" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-dhcp.png 832w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-dhcp-300x265.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2016/08/picostation-pc-dhcp-768x678.png 768w" width="832" height="735" />

Vergiss nicht deinen PC wieder auf DHCP umzustellen!

Nun kannst du deinen Router noch konfigurieren, sodass er auf der Freifunk-Karte angezeigt wird, oder direkt an das Internet anschließen und nutzen.

Wenn du deinen Router noch richtig konfigurierst, hilfst du uns dabei das Netz zu planen und zu optimieren, zeigst anderen wo sich dein Router befindet und siehst selbst, wie und wann dein Router genutzt wird. Das Konfigurieren deines Routers ist ganz einfach, eine Anleitung dazu findest du <a href="http://freifunk-vogtland.net/?page_id=166">auf dieser Seite</a>.

Wenn Du deinen Router ohne Konfiguration nutzen möchtest, dann schließe bitte jetzt den Router an das Internet an. Dazu verbindest du die blaue Buchse deines neuen Freifunk-Routers mithilfe eines Netzwerkkabels mit Deinem Internet-Router.
<h2>Fragen?</h2>
Solltest Du Fragen oder Probleme haben oder Einträge deines Knoten ändern wollen, schreibe uns bitte eine Nachricht. Unsere Kontaktmöglichkeiten findest du <a href="http://vogtland.freifunk.net/?page_id=251">hier</a>.