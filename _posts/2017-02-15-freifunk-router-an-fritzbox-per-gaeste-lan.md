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
Wenn man eine aktuellen FritzBox mit 4 LAN-Ports besitzt, ist es möglich, die Bandbreite eines Freifunk-Routers automatisch anpassen zulassen.<!--more--> Somit haben alle Verbindungen im eigenen Netzwerk Vorrang und sollte der Download oder das Streaming beendet werden, wird mehr Bandbreite dem Freifunk-Router zugewiesen. 

### So geht's:

*   FritzBox per `http://fritz.box` öffnen
*   evtl. Anmeldedaten eingeben
*   Über das Menü oben rechts (drei Punkte <img class="wp-image-1015 alignnone" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-17-um-00.00.57.png" alt="" width="23" height="31" />) die "Erweiterte Ansicht" aktivieren <img class="alignnone size-full wp-image-1014" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-16-um-23.59.52.png" alt="" width="285" height="213" />
*   Über das Menü "Internet" -> "Filter" die "Listen" öffnen [<img class="alignnone wp-image-1016 size-medium" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-17-um-00.04.24-300x115.png" alt="" width="300" height="115" />][1]
*   Filterliste "alles außer Surfen und Mailen" bearbeiten (Stift-Symbol) <img class="alignnone size-medium wp-image-1017" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-17-um-00.05.13-300x26.png" alt="" width="300" height="26" />
*   Folgende Einstellungen wie in dem Bild unten übernehmen 
    <table>
      <tbody>
        <tr>
          <th width="261">
            Host
          </th>
          
          <th width="261">
            Port
          </th>
          
          <th width="261">
            Grund
          </th>
        </tr>
        
        <tr>
          <td width="261">
            vpnXX.freifunk-vogtland.net
          </td>
          
          <td width="261">
            <span style="font-family: inherit; font-size: inherit;">udp/10000–10099</span>
          </td>
          
          <td width="261">
            Für fastd
          </td>
        </tr>
        
        <tr>
          <td width="261">
            vpnXX.freifunk-vogtland.net
          </td>
          
          <td width="261">
            <span style="font-family: inherit; font-size: inherit;"><span style="font-family: inherit; font-size: inherit;">udp/11000</span></span><span style="font-family: inherit; font-size: inherit;">–11099</span>
          </td>
          
          <td width="261">
            Für<span style="font-family: inherit; font-size: inherit;"> tunneldigger/L2TPv3</span>
          </td>
        </tr>
        
        <tr>
          <td width="261">
            *
          </td>
          
          <td width="261">
            udp/53
          </td>
          
          <td width="261">
          </td>
        </tr>
      </tbody>
    </table>
    
    <img class="alignnone wp-image-1018 size-medium" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-17-um-00.08.50-300x172.png" alt="" width="300" height="172" />

*   Änderungen an der Liste speichern
*   evtl. den Namen der Liste noch ändern in "alles außer Surfen und Mailen und Freifunk"
*   Danach über das Menü "Internet" -> "Filter" die "Zugangsprofile" öffnen und im Profil "Gast" die Netzwerkanwendung "alles außer Surfen und Mailen und Freifunk" wählen und den Filter für Internetseiten deaktivieren<img class="alignnone wp-image-1019 size-medium" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-17-um-00.13.37-300x183.png" alt="" width="300" height="183" />

*   Nun geht es zum "Heimnetz" -> "Netzwerk" zu dem Reiter "Netzwerkeinstellungen"
*   In den "Netzwerkeinstellungen" das Häkchen bei "Gastzugang für LAN 4 aktiv" <img class="alignnone wp-image-1020 size-medium" src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-17-um-00.15.50-300x192.png" alt="" width="300" height="192" />

*   evtl. das Häkchen bei "Anmeldung am Gastzugang nur nach Zustimmung zu den Nutzungsbedingungen gestatten" entfernen
*   Freifunk-Router an den LAN 4 anschließen und einschalten
*   <span class="s2">der Freifunk-Router sollte sich nun automatisch mit dem Freifunk-Netz verbinden und fertig ist es</span> Nun hat man eine automatische Anpassung der Bandbreite für Freifunk.

 [1]: https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/02/Bildschirmfoto-2018-06-17-um-00.04.24.png