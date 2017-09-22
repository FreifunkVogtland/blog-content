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
<div id="pl-691"  class="panel-layout" ><div id="pg-691-0"  class="panel-grid panel-no-style" ><div id="pgc-691-0-0"  class="panel-grid-cell"  data-weight="1" ><div id="panel-691-0-0-0" class="so-panel widget widget_sow-editor panel-first-child" data-index="0" data-style="{&quot;background_display&quot;:&quot;tile&quot;}" ><div class="so-widget-sow-editor so-widget-sow-editor-base">
<div class="siteorigin-widget-tinymce textwidget">
	<p>Wenn man Besitzer einer aktuellen FritzBox und der Option ein Gästenetzwerk an dem LAN-Port 4 schalten kann, ist es damit möglich die Bandbreite eines Freifunk-Routers einfach automatisch drosseln zulassen. Somit haben alle Verbindungen im eigenen Netzwerk Vorrang und sollte der Download oder das Streaming beendet werden, wird wieder mehr Bandbreite für den Freifunk-Router freigegeben.</p><p>So geht's:</p><ul><li>FritzBox per http://fritz.box öffnen</li><li>evtl. Anmeldedaten eingeben</li><li>Über das Menü "Internet" -&gt; "Filter" die "Listen" öffnen</li><li>Filterliste "alles außer Surfen und Mailen öffnen"</li><li>Die Einstellungen des Bildes übernehmen</li></ul></div>
</div></div><div id="panel-691-0-0-1" class="so-panel widget widget_sow-image" data-index="1" data-style="{&quot;background_image_attachment&quot;:false,&quot;background_display&quot;:&quot;tile&quot;}" ><div class="so-widget-sow-image so-widget-sow-image-default-46f30e3d504b">

<div class="sow-image-container">
	<img src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-01-1024x660.png" width="720" height="464" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-01-1024x660.png 1024w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-01-300x193.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-01-768x495.png 768w" sizes="(max-width: 720px) 100vw, 720px" title="Fritz 01" 		class="so-widget-image"/>
</div>

</div></div><div id="panel-691-0-0-2" class="so-panel widget widget_sow-editor" data-index="2" data-style="{&quot;background_display&quot;:&quot;tile&quot;}" ><div class="so-widget-sow-editor so-widget-sow-editor-base">
<div class="siteorigin-widget-tinymce textwidget">
	<p><span class="s2">Achtung: Ich habe in meiner Einstellung das Häkchen bei „E-Mail-Filter über Port 25 aktiv“ aktiviert, d.H. es können Mails nur mittels SSL Versand werden. Somit sind in dem Bild die Ports 25 und 110 nicht ausgeschlossen.</span></p><ul class="ol1"><li class="li1"><span class="s2">Änderungen an der Liste speichern</span></li><li class="li1"><span class="s2">evtl. den Namen der Liste noch ändern in „alles außer Surfen und Mailen und Freifunk“</span></li><li class="li1"><span class="s2">Danach über das Menü „Internet“ -&gt; „Filter“ die „Zugangsprofile“ öffnen und im Profil „Gast“ die Netzwerkanwendung „alles außer Surfen und Mailen und Freifunk“ wählen und den Filter für Internetseiten deaktivieren</span></li></ul></div>
</div></div><div id="panel-691-0-0-3" class="so-panel widget widget_sow-image" data-index="3" data-style="{&quot;background_display&quot;:&quot;tile&quot;}" ><div class="so-widget-sow-image so-widget-sow-image-default-46f30e3d504b">

<div class="sow-image-container">
	<img src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-02-1024x660.png" width="720" height="464" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-02-1024x660.png 1024w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-02-300x193.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-02-768x495.png 768w" sizes="(max-width: 720px) 100vw, 720px" title="Fritz 02" 		class="so-widget-image"/>
</div>

</div></div><div id="panel-691-0-0-4" class="so-panel widget widget_sow-editor" data-index="4" data-style="{&quot;background_display&quot;:&quot;tile&quot;}" ><div class="so-widget-sow-editor so-widget-sow-editor-base">
<div class="siteorigin-widget-tinymce textwidget">
	<ul class="ol1"><li class="li1"><span class="s2">Nun geht es zum „Heimnetzwerk“ -&gt; „Heimnetzübersicht“ zu dem Reiter „Netzwerkeinstellungen“</span></li><li class="li1"><span class="s2">In den „Netzwerkeinstellungen“ das Häkchen bei „Gastzugang für LAN 4 aktiv“</span></li></ul></div>
</div></div><div id="panel-691-0-0-5" class="so-panel widget widget_sow-image" data-index="5" data-style="{&quot;background_display&quot;:&quot;tile&quot;}" ><div class="so-widget-sow-image so-widget-sow-image-default-46f30e3d504b">

<div class="sow-image-container">
	<img src="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-04-1024x660.png" width="720" height="464" srcset="https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-04-1024x660.png 1024w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-04-300x193.png 300w, https://vogtland.freifunk.net/wordpress/wp-content/uploads/2017/09/Fritz-04-768x495.png 768w" sizes="(max-width: 720px) 100vw, 720px" title="Fritz 03" 		class="so-widget-image"/>
</div>

</div></div><div id="panel-691-0-0-6" class="so-panel widget widget_sow-editor panel-last-child" data-index="6" data-style="{&quot;background_display&quot;:&quot;tile&quot;}" ><div class="so-widget-sow-editor so-widget-sow-editor-base">
<div class="siteorigin-widget-tinymce textwidget">
	<ul class="ol1"><li class="li1"><span class="s2">evtl. das Häkchen bei „Anmeldung am Gastzugang nur nach Zustimmung zu den Nutzungsbedingungen gestatten“ entfernen</span></li><li class="li1"><span class="s2">Freifunk-Router an den LAN 4 anschließen und einschalten</span></li><li class="li1"><span class="s2">der Freifunk-Router sollte sich nun automatisch mit dem Freifunk-Netz verbinden und fertig ist es</span></li></ul><p class="p1"><span class="s2">Nun hat man eine automatische Anpassung der Bandbreite für Freifunk.</span></p></div>
</div></div></div></div></div>