---
id: 253
title: 'Javascript Tutorial I &#8211; Hello World!'
date: 2011-05-09T15:54:28+00:00
author: Nikhil Palanki
layout: single
guid: /?p=253
permalink: /2011/05/09/javascript-tutorial-i-hello-world/
categories:
  - Javascript
  - Tutorials
tags:
  - javascript
  - noobs
  - programming
---
I see you are back at ByteRevel, and for a good reason. You are interested in the art of Javascripting your HTML page! Well, we cannot progress any further till you have mastered the _Hello World!_ program. You will be punished if progressing without consulting Hello World.

Let&#8217;s take a look at the coding for Hello World! Note that the HTML is in the strange font and the Javascript is bolded.

<HTML>

<HEAD>

<TITLE></TITLE>

</HEAD>

<BODY>

**<script type=&#8221;text/javascript&#8221;>**
  
**document.write(&#8220;Hello World!&#8221; )**
  
**</script>**

</BODY>

</HTML**>**

&nbsp;

You HTML programmers would understand the basic template for creating a Body and Heading and all that happiness. But once you look at the Javascript, you&#8217;ll realize that using the function provided is just wasting your time. And that is true. **document.write** makes no difference, even if you were using just HTML to write &#8220;Hello World.&#8221; You should realize **document.write** will only make your life easier if you plan to use more Javascript.

&nbsp;

Another way of displaying &#8220;Hello World&#8221; on your Hello World! document is by creating a box so that when one types in &#8220;Hello World!&#8221; it will display, Hello World!

<HTML>

<HEAD>

<TITLE></TITLE>

</HEAD>

<BODY>

**<SCRIPT Language =&#8221;JavaScript&#8221; >**

**function MsgBox (textstring) {**

**alert (textstring) }**

**</SCRIPT>**

 ****

<FORM>

**<INPUT Name =&#8221;text1&#8243; TYPE=text>**

**<INPUT Name=&#8221;submit&#8221;TYPE=Button VALUE=&#8221;Show Me&#8221; onclick=&#8221;MsgBox(&#8220;hello World!&#8221; )&#8221; >**

</FORM>

</BODY>

</HTML**>**

&nbsp;

This allows the user to just type in his what-not and display it. We are hoping this person will type &#8220;Hello World&#8221; and not something obscene.

You may notice the other part of the Javascript has some strange inputs and names and other pieces of information that seem convoluted at the moment (if it doesn&#8217;t, you are either lying, know Javascript already, or just are very observant; I am guessing the third one). But I will re-post another Javascript tutorial later on, explaining how this works.

&nbsp;

<div id="attachment_255" style="max-width: 447px" class="wp-caption aligncenter">
  <a rel="attachment wp-att-255" href="/2011/05/09/javascript-tutorial-i-hello-world/best-javascript-resources1/"><img class="size-full wp-image-255" src="/wp-content/uploads/2011/05/best-javascript-resources1.jpg" alt="" width="437" height="352" srcset="/wp-content/uploads/2011/05/best-javascript-resources1.jpg 437w, /wp-content/uploads/2011/05/best-javascript-resources1-300x241.jpg 300w" sizes="(max-width: 437px) 100vw, 437px" /></a>
  
  <p class="wp-caption-text">
    One of the many Javascript Logos
  </p>
</div>
