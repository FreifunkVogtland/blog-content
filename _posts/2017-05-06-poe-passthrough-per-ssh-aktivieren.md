---
ID: 867
post_title: PoE Passthrough per SSH aktivieren
author: andre
post_excerpt: ""
layout: post
permalink: >
  https://vogtland.freifunk.net/poe-passthrough-per-ssh-aktivieren/
published: true
post_date: 2017-05-06 00:31:07
---
Falls ihr eine zweite Ubiquiti (Nano|Pico)station oder CPE (oder auch Kamera) an eine bereits vorhandene anstecken möchtet, aber nicht die Möglichkeit habt das PoE Passthrough per Konfigurations-Menu zu aktivieren<!--more-->, findet ihr hier die Kommandozeilen-Befehle dafür:

<code>uci set system.gpio_switch_poe_passthrough.value=1
uci commit system
/etc/init.d/gpio_switch restart
</code>