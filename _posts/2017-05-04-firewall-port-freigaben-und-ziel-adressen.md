---
ID: 859
post_title: >
  Firewall Port-Freigaben und
  Ziel-Adressen
author: andre
post_excerpt: ""
layout: post
permalink: >
  https://vogtland.freifunk.net/firewall-port-freigaben-und-ziel-adressen/
published: true
post_date: 2017-05-04 23:43:05
---
In manchen Fällen müssen für die Funktion des Freifunk Router in einer vorhanden Firewall noch Ports freigegeben werden. Nachfolgend findet ihr eine Liste der benötigten Ports und Adressen: <!--more-->   

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
    
    <tr>
      <td width="261">
        firmware.freifunk-vogtland.net
      </td>
      
      <td width="261">
        tcp/80, tcp/443
      </td>
      
      <td width="261">
      </td>
    </tr>
    
    <tr>
      <td width="261">
        2003:49:a051:9000::42
      </td>
      
      <td width="261">
      </td>
      
      <td width="261">
      </td>
    </tr>
  </tbody>
</table>