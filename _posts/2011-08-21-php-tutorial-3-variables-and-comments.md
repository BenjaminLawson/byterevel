---
id: 2474
title: 'PHP Tutorial 3 &#8211; Variables And Comments'
date: 2011-08-21T21:01:13+00:00
author: Ipodnerd
layout: single
guid: /?p=2474
permalink: /2011/08/21/php-tutorial-3-variables-and-comments/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/07/PHP-icon.jpeg
categories:
  - PHP
tags:
  - comments
  - php
  - variables
---
[<img class="aligncenter size-full wp-image-2185" title="PHP icon" src="/wp-content/uploads/2011/07/PHP-icon.jpeg" alt="" width="238" height="283" srcset="/wp-content/uploads/2011/07/PHP-icon.jpeg 238w, /wp-content/uploads/2011/07/PHP-icon-180x214.jpeg 180w" sizes="(max-width: 238px) 100vw, 238px" />](/wp-content/uploads/2011/07/PHP-icon.jpeg)

Let&#8217;s see if we can squeeze in another tutorial before a <a title="http://www.youtube.com/watch?v=bU1QPtOZQZU" href="http://www.youtube.com/watch?v=bU1QPtOZQZU" target="_blank">massive asteroid smashes into the Earth</a>. In our last mind-boggling  PHP tutorial, we made our first web page using PHP. This time around, we are going to cover variables and comments.

<h1 style="text-align: center;">
  Variables
</h1>

If you&#8217;ve worked with other programming languages, or have taken a basic Algebra class, then you probably already know what a variable is. In programming, a variable is a name that can represent an assigned value. For example, we could have a variable called &#8220;X&#8221;. It doesn&#8217;t represent a value on its own, so we&#8217;ll need to assign it a value. Let&#8217;s assign the value &#8220;1&#8221; to X. Now, we have a variable &#8220;X&#8221; with an assigned value of &#8220;1&#8221;. Variables in programming aren&#8217;t limited to numbers; We could assign the phrase &#8220;Row Row Row Your Boat&#8221; to X.

In PHP, we declare a variable by simply giving a name for the variable, and setting it equal to a value. A dollar sign is placed immediately before the name of the variable as to tell the computer that the name is in fact a name for a variable, and not a function or other statement.

<table border="0" align="center">
  <tr>
    <td>
      <pre>&lt;html&gt;
&lt;head&gt;
&lt;title&gt;My Cool PHP Page&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;?php

<span style="color: #ff0000;">$number = 5;</span>

<span style="color: #ff0000;">$words = 'Byte Revel Rocks';</span>

<span style="color: #ff0000;">$boolean = true;</span>

?&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>
    </td>
  </tr>
</table>

&nbsp;

In the code above, we declared three variables and set them equal to three different kinds of values. The first is an integer, the second is a string of text, and the third is boolean. If you are coming from another programming language, you are probably both shocked and relieved that you don&#8217;t have to declare a data type.

If you didn&#8217;t quite understand what I was saying earlier about declaring variables, you can probably follow the above variable declarations. They&#8217;re as easy as a dollar sign followed by the name of your variable, and an equal sign followed by the value you want to assign the variable. Think &#8220;$variablename = value;&#8221;.

Variables can be named with any combination of alphanumeric characters, with one exception. You can&#8217;t have a variable name that is just a number.

Depending on what kind of value you want to assign a variable, you may or may not use quotation marks around your value. Both numbers and boolean values will not have quotes around them, while strings (words) will.

What&#8217;s that? You&#8217;re not familiar with the boolean data type? It&#8217;s quite simple really. It can either be &#8220;true&#8221; or &#8220;false&#8221;.

Now that we&#8217;ve created some variables and assigned them some values, let&#8217;s go over outputting the value of a variable to the screen. You may recall that we used a function called &#8220;echo&#8221; in our last tutorial. Well, we are going to use that again to display the values of our variables.

<table border="0" align="center">
  <tr>
    <td>
      <pre>&lt;html&gt;</pre>
      
      <pre>&lt;head&gt;</pre>
      
      <pre>&lt;title&gt;My Cool PHP Page&lt;/title&gt;</pre>
      
      <pre>&lt;/head&gt;</pre>
      
      <pre>&lt;body&gt;</pre>
      
      <pre>&lt;?php</pre>
      
      <pre>$number = 5;</pre>
      
      <pre>$words = 'Byte Revel Rocks';</pre>
      
      <pre>$boolean = false;</pre>
      
      <pre><span style="color: #ff0000;">echo $number;</span></pre>
      
      <pre><span style="color: #ff0000;">echo $words;</span></pre>
      
      <pre>?&gt;</pre>
      
      <pre>&lt;/body&gt;</pre>
      
      <pre>&lt;/html&gt;</pre>
    </td>
  </tr>
</table>

&nbsp;

The above code will output &#8220;5Byte Revel Rocks&#8221;. Similarly to how we outputted text in our last tutorial using the statement &#8221; echo &#8220;Hello World&#8221;; &#8220;, we use the echo function followed by the name of the variable to output the value of the variable.

Take note that I didn&#8217;t echo the boolean variable. This is because the computer reads boolean values as &#8220;1&#8221; if it is true, and &#8220;0&#8221; if it is false. Using the echo function, boolean variables either result in an outputted &#8220;1&#8221; or nothing. Echo&#8217;ing boolean variables isn&#8217;t very useful.

You&#8217;re probably thinking that &#8220;5Byte Revel Rocks&#8221; is pretty ugly. Let&#8217;s stick the variables inside of a string of text to pretty them up (and make them more useful).

<table border="0" align="center">
  <tr>
    <td>
      <pre>&lt;html&gt;
&lt;head&gt;
&lt;title&gt;My Cool PHP Page&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;?php

$number = 5;

$words = 'Byte Revel Rocks';

$boolean = false;

<span style="color: #ff0000;">echo "My favorite number is $number, and $words";</span>

?&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>
    </td>
  </tr>
</table>

&nbsp;

The above code will output &#8220;My favorite number is 5, and Byte Revel Rocks&#8221;. Pretty cool, eh? Including variables in strings of text is as easy as inserting the name of the variable into the string of text.

Alternatively, you can include the values of variables inside echo statements through an operation called concatenation. To do this, simply put a &#8220;.&#8221; between each string of text and and each variable. Make sure that all strings of text are enclosed by quotation marks. Like so:

<table border="0" align="center">
  <tr>
    <td>
      <pre>&lt;html&gt;</pre>
      
      <pre>&lt;head&gt;</pre>
      
      <pre>&lt;title&gt;My Cool PHP Page&lt;/title&gt;</pre>
      
      <pre>&lt;/head&gt;</pre>
      
      <pre>&lt;body&gt;</pre>
      
      <pre>&lt;?php</pre>
      
      <pre>$number = 5;</pre>
      
      <pre>$words = 'Byte Revel Rocks';</pre>
      
      <pre>$boolean = false;</pre>
      
      <pre><span style="color: #ff0000;">echo "My favorite number is ".$number.", and ".$words;</span></pre>
      
      <pre>?&gt;</pre>
      
      <pre>&lt;/body&gt;</pre>
      
      <pre>&lt;/html&gt;</pre>
    </td>
  </tr>
</table>

&nbsp;

<h1 style="text-align: center;">
  Comments
</h1>

<div style="max-width: 564px" class="wp-caption aligncenter">
  <img class="   " title="Commented" src="http://imgs.xkcd.com/comics/commented.png" alt="" width="554" height="150" />
  
  <p class="wp-caption-text">
    "Commented" by XKCD
  </p>
</div>

In programming, comments are sections of text inside the program that aren&#8217;t run. They are marked with certain characters so that the computer knows to skip over them. They are most commonly used to add annotations, or notes, to the code. They can also be used to temporarily &#8220;mute&#8221; parts of a program.

The syntax for comments in PHP is the same as C, C++, and Perl (or rather, it allows you to use the syntax from any of those languages).

<table border="0" align="center">
  <tr>
    <td>
      <pre>&lt;html&gt;
&lt;head&gt;
&lt;title&gt;My Cool PHP Page&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;?php

<span style="color: #ff0000;">// this is a single-line comment</span>

<span style="color: #ff0000;"># this is a single-line comment</span>

<span style="color: #ff0000;">/* this is</span>
<span style="color: #ff0000;"> a</span>
<span style="color: #ff0000;"> multi-line</span>
<span style="color: #ff0000;"> comment */</span>

?&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>
    </td>
  </tr>
</table>

&nbsp;

The above code will output absolutely nothing, and I believe it is pretty self explanatory.

&nbsp;

<span class="vvqbox vvqyoutube" style="width:585px;height:330px;"><span id="vvq-2474-youtube-1"><a href="http://www.youtube.com/watch?v=l-ceg763Voc"><img src="http://img.youtube.com/vi/l-ceg763Voc/0.jpg" alt="YouTube Preview Image" /></a></span></span>
