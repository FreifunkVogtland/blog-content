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
In manchen Fällen müssen für die Funktion des Freifunk Router in einer vorhanden Firewall noch Ports freigegeben werden. Nachfolgend findet ihr eine Liste der benötigten Ports und Adressen:
<!--more-->


<table>
<tbody>
<tr>
<th width="261">Host</th>
<th width="261">Port</th>
</tr><tr>
<td width="261">vpn0[1-9].freifunk-vogtland.net</td>
<td width="261">(udp) 10000 – 10003</td>
</tr><tr>
<td width="261">vpn10.freifunk-vogtland.net</td>
<td width="261">(udp) 10000 – 10003</td>
</tr><tr>
<td width="261">*</td><td width="261">udp/53</td>
</tr><tr>
<td width="261">Firmware.freifunk-vogtland.net</td>
<td width="261">tcp/80, tcp/443</td>
</tr><tr>
<td width="261">2003:49:a051:9000:42</td>
<td width="261">&nbsp;</td>
</tr>
</tbody>
</table>