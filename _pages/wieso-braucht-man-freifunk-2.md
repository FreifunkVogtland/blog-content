---
ID: 419
post_title: Häufig gestellte Fragen (FAQ)
author: Maximilian Hahn
post_excerpt: ""
layout: page
permalink: >
  https://vogtland.freifunk.net/wieso-braucht-man-freifunk-2/
published: true
post_date: 2016-10-13 09:59:12
---
<h2><strong>Ist</strong> WLAN-Strahlung<strong> gefährlich?</strong></h2>
Anders, als z.B. Sendemasten für Mobilfunk (Handynetze), die mit Leistungen von 1 bis 2 Watt senden dürfen, beträgt die maximale Sendeleistung für WLAN nicht mehr als 0,1 Watt. Dies entspricht etwa der Lichtleistung einer normalen Fahrradglühbirne.
WLAN darf daher auch völlig lizenzfrei, von jedem, überall verwendet werden und ist mittlerweile auch in fast allen Haushalten und quasi jedem Computer und Smartphone anzutreffen.
Die von Freifunk verwendete Technik sind handelsübliche WLAN-Geräte mit angepasster Software. Nicht nur Hochfrequenzexperten, sondern auch das Bundesamt für Strahlenschutz (BfS) hält diese Technik für <a href="http://www.bfs.de/DE/themen/emf/hff/anwendung/kabellos/kabellos.html">unbedenklich</a>.

&nbsp;
<h2><strong>Ist das</strong> wirklich<strong> Rechtssicher?</strong></h2>
Hier gibt es eine gute Stellungnahme der <a href="http://www.anwaltskanzlei-feuerhake.de/freifunk">Anwaltskanzlei Feuerhake</a> mit einigen Details. Die Situation von Freifunk Goettingen ist auf unsere Situation uebetragbar. Hier wurden im allgemeinen <a href="https://wiki.freifunk.net/FAQ_Rechtliches">Freifunk Wiki</a> diverse rechtliche Infos (auch über Stoererhaftung hinaus) zusammengetragen. Wie bereits erwaehnt ist unser Internet-Gateway (Foerderverein freie Netzwerke e.V.), deren IP-Adressen auch im Internet fuer Verbindungen aus unserem Netz sichtbar werden, selbst <a href="https://www.bundesnetzagentur.de/SharedDocs/Downloads/DE/Sachgebiete/Telekommunikation/Unternehmen_Institutionen/Anbieterpflichten/Meldepflicht/TKDiensteanbieterPDF.pdf?__blob=publicationFile&amp;v=54">Provider</a>: Freifunk Rheinland e.V. Eickener Straße 83 41061 Mönchengladbach Reg-Nr. 15/130 Desweiteren ist der <a href="https://foerderverein.freie-netzwerke.de/">Förderverein Freie Netzwerke e.V.</a> politisch auch gegen die Stoererhaftung sehr aktiv. Weitere Informationen unter: <a href="http://freifunkstattangst.de/">http://freifunkstattangst.de/</a>

&nbsp;
<h2><strong>Was ist</strong> ein<strong> Knoten?</strong></h2>
Knoten ist gleichbedeutend mit Router, Accesspoint oder Zugangspunkt. Sie werden von Privatpersonen oder Firmen betrieben und bieten Dir und Anderen Zugang zu unserem Freifunknetzwerk.

&nbsp;
<h2><strong>Darf ich</strong> Freifunk<strong> einfach so benutzen?</strong></h2>
Ja, Du darfst Freifunk ohne zu bezahlen und schlechtes Gewissen nutzen! Und wenn Du doch eins bekommst, mach mit, indem Du selbst einen Knoten aufstellst. ;)

&nbsp;
<h2><strong>Was kostet</strong> Freifunk?</h2>
Wenn Du Freifunk nur auf einem WLAN-fähigen Gerät nutzen möchtest, dann fallen keine Kosten für Dich an. Falls Du selbst einen Freifunk-Zugang anbieten möchtest benötigst Du neben Deinem eigenen Internetanschluss einen passenden Router, der je nach Modell für ab 35 Euro bei uns erhältlich ist. Die jährlichen Stromkosten für das Betreiben des Routers belaufen sich auf etwa 5-10 Euro, weitere Kosten fallen nicht an.

&nbsp;
<h2><strong>Ich</strong> habe<strong> keine Ahnung von Technik. Kann ich dennoch einen Zugangspunkt betreiben?</strong></h2>
Die kurze Antwort ist: Ja, Du kannst! Auch wenn Du absolut keine Ahnung von Technik hast, aber dennoch einen Router betreiben möchtest, kannst Du über uns einen vorbereiteten Router bekommen, den Du nur noch am Stromnetz (und gegebenenfalls an deinem Router) anschließen musst. Ein derart vorbereiteter Router sollte „einfach so“ (out of the box) funktionieren. Weiter Informationen findest du unter: <a href="http://vogtland.freifunk.net/?page_id=32">Wie kann ich mitmachen?</a>

&nbsp;
<h2><strong>Verliere ich</strong> nicht<strong> die Garantie, wenn ich die Software des Gerätes ändere?</strong></h2>
Nein. TP-Link, die Firma, mit deren WLAN-Routern wir unser Netz aufspannen, unterstützt explizit das Aufspielen und Betreiben alternativer Firmware, ohne dass dadurch ein Verlust der Garantie eintritt.

&nbsp;
<h2><strong>Lässt sich die</strong> original<strong> Firmware wieder einspielen?</strong></h2>
Ja! Ein bereits in einen Freifunk-Knoten umgewandeltes Gerät kann jederzeit wieder mit der original Hersteller-Firmware geflasht (bespielt) werden und entspricht damit wieder dem Original.

&nbsp;
<h2><strong>Wie schnell ist</strong> mein<strong> Zugang im Freifunk?</strong></h2>
Innerhalb des Funknetzes hängt die Geschwindigkeit stark von der Qualität der Verbindung ab und über wie viele Knoten sie geht. Die Geschwindigkeit der Knoten ins kabelgebundene Netz (z.B. Internet) wird jedoch maßgeblich durch die Prozessor-Leistung der Router begrenzt. Denn die müssen den VPN-Tunnel ver- &amp; entschlüsseln, was viel Rechenleistung benötigt. Gemessene Richtwerte pro Modell findest Du unter <a href="https://wiki.tecff.de/router-vpn-speed">Freifunk Altdorf</a>.

&nbsp;
<h2>Zugriff auf den aktuellen Knoten über die Next-Node Adresse</h2>
In unserem Freifunk-Netz existiert eine spezielle IP-Adresse, über die man jederzeit auf den Knoten zugreifen kann, mit dem man derzeit per WLAN oder LAN verbunden ist. Es handelt sich dabei um die folgenden IP-Adresse:
<pre>IPv4 <a href="http://10.204.0.1/" target="_blank" rel="noopener">10.204.0.1</a></pre>
Zur Vereinfachung kann auch der Domainname <em>nextnode.fffd</em> verwendet werden, der auf die zuvor genannten IP-Adressen verweist. Um also die Statusseite des aktuellen Knoten anzuzeigen, kann im Browser auf eine der folgenden Adressen zugegriffen werden:
<pre><a href="http://nextnode.ffv/" target="_blank" rel="noopener">http://nextnode.ffv</a></pre>
<em>Hinweis: Der Zugriff erfolgt auf den Knoten, mit dem der zugreifende Rechner zum Zeitpunkt des Zugriffs verbunden ist. Falls mehrere Knoten in der Nähe sind, muss dies nicht zwangsläufig der Knoten sein, den ihr eigentlich erreichen wolltet.</em>

&nbsp;
<h2><a href="http://vogtland.freifunk.net/?page_id=29"><strong>Wer ist Freifunk</strong> Vogtland?</a></h2>