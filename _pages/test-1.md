---
ID: 579
post_title: Termine
author: andre
post_date: 2017-02-14 11:43:29
post_excerpt: ""
layout: page
permalink: >
  http://vogtland.freifunk.net/?page_id=579
published: true
vantage_panels_no_legacy:
  - 'true'
vantage_metaslider_slider:
  - ""
vantage_metaslider_slider_stretch:
  - "1"
vantage_menu_icon:
  - ""
siteorigin_page_settings:
  - 'a:7:{s:6:"layout";s:7:"default";s:10:"page_title";b:1;s:15:"masthead_margin";b:1;s:13:"footer_margin";b:1;s:14:"featured_image";b:0;s:13:"hide_masthead";b:0;s:19:"hide_footer_widgets";b:0;}'
---
[vereinonline_kalender]

[vereinonline_termine(100,495)]
<a name="[vereinonline:id]"></a>
<a name="[vereinonline:anker]"></a>
<div style="height:80px;">&nbsp;</div>
[vc_row_inner]
[vc_column_inner width="1/3"]
[vc_column_text]
<a href="http://www.vereinonline.org/tresorvinum/attachments/[vereinonline:foto]"><img class="alignnone wp-image-361 size-medium" src="http://www.vereinonline.org/tresorvinum/?download=[vereinonline:foto]&width=300" alt="[vereinonline:key_foto_copyright]" width="300" height="200" /></a>
<h5>[vereinonline:key_foto_copyright]</h5>
[/vc_column_text]
[/vc_column_inner]
[vc_column_inner width="2/3"]
[vc_column_text]
<h4></h4>
<b>
[vereinonline:datum]
[vereinonline:zeit]
<a href="http://tresorvinum.de/anfahrt/">TRESOR VINUM</a></b>[/vc_column_text]

[vc_accordion style="accordion" collapsible="yes" active_tab="[vereinonline:activetab]"]
[vereinonline_if(kategorie)]
[vc_accordion_tab title="[vereinonline:key_titel_kategorie:name]" title_tag="h4"]
[vc_column_text]
[vereinonline:key_titel_kategorie:beschreibung]
[/vc_column_text]
[/vc_accordion_tab]
[vereinonline_endif]
[/vc_accordion]
[/vc_column_inner]
[/vc_row_inner]

[vc_column_text]
<h4>[vereinonline:titel]</h4>
[vereinonline:beschreibung]&nbsp;

[vereinonline_if(key_datei_einladung)]
<a href="http://www.vereinonline.org/tresorvinum/?download=[vereinonline:key_datei_einladung]&path=list">PDF Einladung</a>&nbsp;
[vereinonline_endif]
[/vc_column_text]

[vc_column_text el_class="linkorange"]
[vereinonline_if(anmeldungmoeglich)]
<h3><a href="#" onclick="javascript:window.open('http://www.vereinonline.org/tresorvinum/?veranstaltunganmelden=[vereinonline:id]','','toolbar=no,location=no,directories=no,status=yes,scrollbars=yes,resizable=yes,copyhistory=no,width=600,height=600');return false;">>> ANMELDEN</a></h3>
[vereinonline_endif]&nbsp;
[/vc_column_text]
<hr noshade>
[/vereinonline_termine]