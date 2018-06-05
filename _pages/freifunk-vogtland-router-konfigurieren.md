---
ID: 166
post_title: Freifunk Vogtland Router konfigurieren
author: andre
post_excerpt: ""
layout: page
permalink: >
  https://vogtland.freifunk.net/freifunk-vogtland-router-konfigurieren/
published: true
post_date: 2016-05-26 19:24:49
---
Um den Router in den Config-Mode zu versetzen, drücke bitte die Reset-Taste so lange (ca. 10 Sekunden), bis alle LED's kurz an, dann aus und wieder an gehen. <img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-reset.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-reset.png 3072w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-reset-300x169.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-reset-768x432.png 768w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-reset-1024x576.png 1024w" width="3072" height="1728" /> <img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-reset.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-reset.png 2427w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-reset-300x188.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-reset-768x480.png 768w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-reset-1024x640.png 1024w" width="2427" height="1517" /> Dass kannst du übrigens auch machen, wenn du deinen Router einmal neu konfigurieren möchtest. falls noch nicht geschehen, verbinde Deinen Freifunk-Router mit dem beiliegenden grauen LAN-Kabel mit Deinem Computer. Stecke dafür das Kabel in eine der gelben Buchsen (die blaue brauchst du später). <img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable.png 3072w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-300x169.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-768x432.png 768w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-1024x576.png 1024w" width="3072" height="1728" /> <img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan.png 3072w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan-300x169.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan-768x432.png 768w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/08/picostation-poe-lan-1024x576.png 1024w" width="3072" height="1728" /> Versuche also nun den Router auf seiner neuen Konfigurationsadresse zu erreichen: <span style="color: #dc0067;"><strong>192.168.1.1</strong></span>. Solltest Du ihn nicht erreichen, dann ziehe das Netzwerkkabel am Router oder PC ab, warte kurz und stecke es wieder ein. Wenn alles funktioniert hat, dann solltest du nun in deinem Browser folgende Oberfläche sehen: <img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.06.52.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.06.52.png 818w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.06.52-300x266.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.06.52-768x682.png 768w" width="818" height="726" /> <h3 class="widget-title">
  Name dieses Knotens
</h3> Als erstes musst du deinem Router einen Namen geben. Im Freifunk Vogtland bennenen wir die Router immer nach einem speziellen Schema: abgekürzter Name der Stadt + Bindestrich + Straßenname + Hausnummer 

### Beispiel

<pre>Plauen, Rädelstraße 7 → <strong>PL-Raedel7</strong>
Auerbach, Str. des Friedens 42 → <strong>AE-StrDesFriedens42</strong></pre> Bitte achte darauf, dass keine Sonder- und Leerzeichen im Namen erlaubt sind. Wenn du noch zusätzliche Informationen anfügen möchtest (z.B. "

**OG**" oder "**FamMueller**"), trenne diese bitte ebenfalls mit einem Bindestrich. <h3 class="widget-title">
  Internetverbindung nutzen
</h3> Hiermit erlaubst du deinem Freifunk-Router über deinen Internetanschluss eine (sichere) Verbindung ins Internet herzustellen. Wir empfehlen diese Option in jedem Fall aktiviert zu lassen. Es kann auf keinen Fall schaden! Wenn kein Netzwerkkabel an ihm angeschlossen wird, dann hat er einfach keinen eigenen Internetzugang. Der Zugang zum Internet ist dann aber nur möglich, wenn mindestens bei einem der erreichbaren Freifunk-Router in deiner Nähe die Option aktiviert ist und dieser eine Verbindung mit dem Internet hat. 

<h3 class="widget-title">
  Bandbreite begrenzen (optional)
</h3> Aus unserer Erfahrung heraus ist es nicht notwendig die Begrenzung zu aktivieren. Dein Router wird im alltäglichen Betrieb nicht all-zuviel von deiner Bandbreite in Anspruch nehmen. Solltest du aber trotzdem eine Begrenzung eintragen wollen, setze den Haken “Bandbreite begrenzen” und trage einen Wert in kB ein. Wenn du z.B. eine 16.000er Leitung hast, kannst du ja auf 10.000 begrenzen. Somit hast Du dann 6.000 für dich reserviert. Aber ehrlich: es ist nicht notwendig. Wir haben bei noch keinem die Begrenzung nachträglich einschalten müssen! 

<h3 class="widget-title">
  Knoten auf der Karte anzeigen
</h3> Diese Option sollte ausgewählt werden, um anderen Freifunkern und Interessierten (Gästen!) die Position deines Routers anzuzeigen. Es geht hierbei, wie beim Namen des Knoten, nur um eine Darstellung in der Karte. Danach ist der Router auf der 

[Karte][1]<ins></ins> <ins>zu</ins> <ins>sehen</ins>. Bedenken um die Privatsphäre sollten hier ausnahmsweise keine Rolle spielen, denn du möchtest doch mit vielen ein großes Netzwerk aufbauen. Nach dem Aktivieren erscheinen drei neue Felder. Eines für den Breitengrad, den Längengrad und die Höhe. Die Ziel-Koordinaten an dem der Router stehen soll, findest du z.B. unter <a href="http://de.mygeoposition.com/" target="_blank">myGeoPosition</a> . In der Suche einfach die Adresse des Standortes eingeben und die Daten in die Konfiguration übertragen. Bitte achte bei den Werten auf die richtige Schreibweise. Es wird für die „Nachkommastelle“ ein Punkt und kein Komma verwendet. (Beispiel: Falsch = <span class="rad">50,1234; Richtig = 50.1234)</span> Bitte gib auch die Höhe in Meter über NN + die Höhe der Befestigung deines Routers an. Die Höhenangabe hilft uns dabei, das Netz kontinuierlich zu verbessern. Durch die Angabe der Höhe können wir Rückschlüsse ziehen, wo es sinnvoll ist weitere Router aufzustellen. 
### Beispiel für die Höhenangabe

<pre>337.123m NN + Router in der 2. Etage (ca. 5m) ≈ <strong>342</strong></pre>

<img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.07.49.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.07.49.png 818w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.07.49-300x259.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.07.49-768x662.png 768w" width="818" height="705" /> <h3 class="widget-title">
  Kontakt
</h3> Um dich im Zweifelsfall erreichen zu können, kannst du hier beispielsweise deine E-Mail-Adresse angeben, natürlich nur wenn du möchtest. 

<h3 class="widget-title">
  Speichern & Neustart
</h3> Bitte kontrolliere noch einmal alle Einstellungen. Man kann sie zwar später wieder ändern, aber das ist viel aufwendiger, als sie eben noch einmal zu kontrollieren. Alles richtig? Gut! Dann klicke auf „Save & Restart“! 

<img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.08.01.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.08.01.png 817w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.08.01-300x260.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/05/Bildschirmfoto-2016-05-26-um-19.08.01-768x666.png 768w" width="817" height="709" /> <h3 class="widget-title">
  Expert Mode
</h3> Wenn du nun noch Experteneinstellungen vornehmen möchest, bitte den Router nochmal wie oben beschrieben in den Config-Mode versetzen. Danach können Einstellung, wie Mesh per LAN oder Privates WLAN boosten einstellt werden. Mehr dazu findest du in der 

[Gluon-Dokumentation][2]. Ansonsten einfach mit dem nächsten Punkt fortfahren. <h3 class="widget-title">
  An’s Internet anschließen
</h3> Wenn du am Standort eine Internetverbindung hast, wird der Freifunk-Router nun an deinen Telekom-, Unitymedia- oder „Was_auch_immer“-Anschluss angeschlossen. Dazu verbindest du die blaue Buchse deines Freifunk-Routers mithilfe eines Netzwerkkabels mit deinem Internet-Router. 

<img class="so-widget-image" src="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-internet.png" srcset="http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-internet.png 3072w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-internet-300x169.png 300w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-internet-768x432.png 768w, http://freifunk-vogtland.net/wordpress/wp-content/uploads/2016/07/tp-link-connect-cable-internet-1024x576.png 1024w" width="3072" height="1728" />

 [1]: http://vogtland.freifunk.net/?page_id=201
 [2]: https://gluon.readthedocs.io/en/v2016.1.5/user/getting_started.html