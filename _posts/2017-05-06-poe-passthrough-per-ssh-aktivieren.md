---
ID: 867
post_title: PoE Passthrough per SSH aktivieren
author: andre
post_date: 2017-05-06 00:31:07
post_excerpt: ""
layout: post
permalink: >
  https://vogtland.freifunk.net/poe-passthrough-per-ssh-aktivieren/
published: true
vantage_panels_no_legacy:
  - 'true'
siteorigin_page_settings:
  - 'a:6:{s:6:"layout";s:7:"default";s:10:"page_title";b:1;s:15:"masthead_margin";b:1;s:13:"footer_margin";b:1;s:13:"hide_masthead";b:0;s:19:"hide_footer_widgets";b:0;}'
---
Falls ihr eine zweite NanoStation oder CPE  (oder Kamera) an eine bereits vorhandene anstecken möchtet, aber nicht die Möglichkeit habt das PoE Passthrough per Konfigurations-Menu zu aktivieren, findet ihr hier die Kommandozeilen-Befehle dafür:
<pre>uci set system.gpio_switch_poe_passthrough.value=1
uci commit system
/etc/init.d/gpio_switch restart

</pre>