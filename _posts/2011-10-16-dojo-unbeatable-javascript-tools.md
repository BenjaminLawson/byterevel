---
id: 3079
title: 'Dojo &#8211; Unbeatable JavaScript Tools'
date: 2011-10-16T15:09:13+00:00
author: Nikhil Palanki
layout: single
guid: /?p=3079
permalink: /2011/10/16/dojo-unbeatable-javascript-tools/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
onswipe_thumb:
  - /wp-content/uploads/2011/10/dijit1.jpg
image: /wp-content/uploads/2011/10/dijit1.jpg
categories:
  - Javascript
  - Programming
  - Software
tags:
  - ajax
  - ajax development
  - dojo
  - javascript
  - javascript development
---
JavaScript has become essential amongst Web Developers (probably developers in general). Whether it be AJAX, jQuery, JSON, or CoffeeScript it has become very prevalent and used in everyday application building, on both sides of the production spectrum. But JavaScript can become a hassle when you don&#8217;t have the right tools, or your tools have become too complicated for basic usage. Luckily, we have Dojo, a toolkit that provides code for completing various tasks such as presenting a pretty grid or a much nicer user interface.

<div id="attachment_3080" style="max-width: 593px" class="wp-caption aligncenter">
  <a href="/2011/10/16/dojo-unbeatable-javascript-tools/screen-shot-2011-10-16-at-3-45-38-pm/" rel="attachment wp-att-3080"><img class="size-full wp-image-3080 " title="Screen Shot 2011-10-16 at 3.45.38 PM" src="/wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-3.45.38-PM.png" alt="" width="583" height="368" srcset="/wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-3.45.38-PM.png 971w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-3.45.38-PM-300x189.png 300w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-3.45.38-PM-180x113.png 180w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-3.45.38-PM-360x227.png 360w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-3.45.38-PM-790x498.png 790w" sizes="(max-width: 583px) 100vw, 583px" /></a>
  
  <p class="wp-caption-text">
    This Interactive Calendar can be found on the Dojo Website
  </p>
</div>

Dojo is an open-source technology created by the Dojo Foundation (primarily Alex Russell, Dylan Schiemann, and David Schlontzer) to ease the development of the complex AJAX language as well as JavaScript in general. And they did a bang-up job of it. Dojo&#8217;s APIs are bountiful, ranging from iOS compatibility to its Rich UI features. Here is an example of the Dojo &#8220;Hello, World.&#8221;

<table border="0" cellspacing="0" cellpadding="0">
  <tr>
    <td>
      <div>
        1
      </div>
      
      <div>
        2
      </div>
      
      <div>
        3
      </div>
      
      <div>
        4
      </div>
      
      <div>
        5
      </div>
      
      <div>
        6
      </div>
      
      <div>
        7
      </div>
      
      <div>
        8
      </div>
      
      <div>
        9
      </div>
      
      <div>
        10
      </div>
      
      <div>
        11
      </div>
      
      <div>
        12
      </div>
    </td>
    
    <td>
      <div>
        <div>
          <code>&lt;!DOCTYPE html&gt;</code>
        </div>
        
        <div>
          <code>&lt;</code><code>html</code><code>&gt;</code>
        </div>
        
        <div>
          <code>&lt;</code><code>head</code><code>&gt;</code>
        </div>
        
        <div>
          <code>    </code><code>&lt;</code><code>meta</code> <code>charset</code><code>=</code><code>"utf-8"</code><code>&gt;</code>
        </div>
        
        <div>
          <code>    </code><code>&lt;</code><code>title</code><code>&gt;Tutorial: Hello Dojo!&lt;/</code><code>title</code><code>&gt;</code>
        </div>
        
        <div>
          <code>    </code><code>&lt;!-- load Dojo --&gt;</code>
        </div>
        
        <div>
          <code>    </code><code>&lt;script src="&lt;a href="http://ajax.googleapis.com/ajax/libs/dojo/1.6.0/dojo/dojo.xd.js">http://ajax.googleapis.com/ajax/libs/dojo/1.6.0/dojo/dojo.xd.js&lt;/a>"&gt;</code><code>&lt;/script&gt;</code>
        </div>
        
        <div>
          <code>&lt;/</code><code>head</code><code>&gt;</code>
        </div>
        
        <div>
          <code>&lt;</code><code>body</code><code>&gt;</code>
        </div>
        
        <div>
          <code>    </code><code>&lt;</code><code>h1</code> <code>id</code><code>=</code><code>"greeting"</code><code>&gt;Hello&lt;/</code><code>h1</code><code>&gt;</code>
        </div>
        
        <div>
          <code>&lt;/</code><code>body</code><code>&gt;</code>
        </div>
        
        <div>
          <code>&lt;/</code><code>html</code><code>&gt;</code>
        </div>
      </div>
    </td>
  </tr>
</table>

This was directly from the Dojo Documentation. As you can see, it works similarly to regular JavaScript but this is, quote-on-quote, vanilla. It is basic Dojo, but it kind of gives a basic feel for how it works. Here is a second example of Dojo  that displays a nice and neat graph (directly from the Dojo Documentation).

<table border="0">
  <tr>
    <td>
      <div id=&#8221;grid1&#8243; dojoType=&#8221;dojox.grid.EnhancedGrid&#8221; query=&#8221;{ Track: &#8216;*&#8217; }&#8221; rowsPerPage=&#8221;30&#8243;<br /> plugins='{nestedSorting: true, dnd: true, indirectSelection: true, menus:{headerMenu:&#8221;headerMenu&#8221;, rowMenu:&#8221;rowMenu&#8221;, cellMenu:&#8221;cellMenu&#8221;, selectedRegionMenu:&#8221;selectedRegionMenu&#8221;}}&#8217;<br /> store=&#8221;csvStore1&#8243; structure=&#8221;layout&#8221; rowSelector=&#8221;20px&#8221;><br /> <div dojoType=&#8221;dijit.Menu&#8221; id=&#8221;headerMenu&#8221; style=&#8221;display: none;&#8221;><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Header Menu Item 1</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Header Menu Item 2</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Header Menu Item 3</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Header Menu Item 4</div><br /> </div><br /> <div dojoType=&#8221;dijit.Menu&#8221; id=&#8221;rowMenu&#8221; style=&#8221;display: none;&#8221;><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Row Menu Item 1</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Row Menu Item 2</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Row Menu Item 3</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Row Menu Item 4</div><br /> </div><br /> <div dojoType=&#8221;dijit.Menu&#8221; id=&#8221;cellMenu&#8221; style=&#8221;display: none;&#8221;><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Cell Menu Item 1</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Cell Menu Item 2</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Cell Menu Item 3</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Cell Menu Item 4</div><br /> </div><br /> <div dojoType=&#8221;dijit.Menu&#8221; id=&#8221;selectedRegionMenu&#8221; style=&#8221;display: none;&#8221;><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Action 1 for Selected Region</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Action 2 for Selected Region</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Action 3 for Selected Region</div><br /> <div dojoType=&#8221;dijit.MenuItem&#8221;>Action 4 for Selected Region</div><br /> </div><br /> </div><br /> <script><br /> //requires<br /> dojo.require(&#8216;dojox.grid.EnhancedGrid&#8217;);<br /> dojo.require(&#8216;dojox.grid.enhanced.plugins.DnD&#8217;);<br /> dojo.require(&#8216;dojox.grid.enhanced.plugins.Menu&#8217;);<br /> dojo.require(&#8216;dojox.grid.enhanced.plugins.NestedSorting&#8217;);<br /> dojo.require(&#8216;dojox.grid.enhanced.plugins.IndirectSelection&#8217;);<br /> dojo.require(&#8216;dojox.data.CsvStore&#8217;);<br /> dojo.require(&#8216;dijit.form.Button&#8217;);<br /> dojo.require(&#8216;dojo.parser&#8217;);//when resources are loaded<br /> dojo.ready(function() {<br /> //layout<br /> layout = [{<br /> defaultCell: { width: 8, editable: false, type: dojox.grid.cells._Widget },<br /> rows:<br /> [<br /> { field: &#8216;Genre&#8217;, width: &#8217;10&#8217; },<br /> { field: &#8216;Artist&#8217;, width: &#8217;15&#8217; },<br /> { field: &#8216;Year&#8217;, width: &#8216;6&#8217; },<br /> { field: &#8216;Album&#8217;, width: &#8217;28&#8217; },<br /> { field: &#8216;Name&#8217;, width: &#8217;22&#8217; }<br /> ]}<br /> ];<br /> //get data store<br /> csvStore1 = new dojox.data.CsvStore({ id:&#8217;csvStore1&#8242;, url:&#8217;includes/grid-demo-data.csv&#8217;});<br /> //parse!<br /> dojo.parser.parse();<br /> });<br /> </script>
    </td>
  </tr>
</table>

And here is what the finished product looks like:

<div id="attachment_3086" style="max-width: 600px" class="wp-caption aligncenter">
  <a href="/2011/10/16/dojo-unbeatable-javascript-tools/screen-shot-2011-10-16-at-4-06-33-pm/" rel="attachment wp-att-3086"><img class="size-full wp-image-3086 " title="Screen Shot 2011-10-16 at 4.06.33 PM" src="/wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-4.06.33-PM.png" alt="" width="590" height="187" srcset="/wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-4.06.33-PM.png 984w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-4.06.33-PM-300x95.png 300w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-4.06.33-PM-180x57.png 180w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-4.06.33-PM-360x114.png 360w, /wp-content/uploads/2011/10/Screen-Shot-2011-10-16-at-4.06.33-PM-790x250.png 790w" sizes="(max-width: 590px) 100vw, 590px" /></a>
  
  <p class="wp-caption-text">
    This is on the Website: It is interactive and stuff
  </p>
</div>

It is loaded with APIs that generally would be too difficult to program with out. It can work on Mobile Apps as well as just Web applications. Dojo is a fantastic tool kit that is essential for all web developers. You can visit it [here](http://dojotoolkit.org/).
