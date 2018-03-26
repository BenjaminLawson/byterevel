---
id: 2209
title: 'PHP Tutorial 2 &#8211; Creating Your First Web Page Using PHP (Hello World)'
date: 2011-07-30T10:55:15+00:00
author: Ipodnerd
layout: single
guid: /?p=2209
permalink: /2011/07/30/php-tutorial-2-creating-your-first-web-page-using-php-hello-world/
image: /wp-content/uploads/2011/07/PHP-icon.jpeg
categories:
  - PHP
tags:
  - hello world
  - html
  - php
  - tutorial
---
<img class="aligncenter size-full wp-image-2185" title="PHP icon" src="/wp-content/uploads/2011/07/PHP-icon.jpeg" alt="" width="238" height="283" srcset="/wp-content/uploads/2011/07/PHP-icon.jpeg 238w, /wp-content/uploads/2011/07/PHP-icon-180x214.jpeg 180w" sizes="(max-width: 238px) 100vw, 238px" />

Ladies and gentlemen, welcome to PHP tutorial 2! In our [last tutorial](/2011/07/28/php-tutorial-i-about-php-installing-mamp-and-xampp/ "PHP Tutorial 1 – About PHP & Installing MAMP And XAMPP"), we covered setting up your server environment. In this tutorial, we are going to go over creating your first web page using PHP.

With all standard server environments, there is a folder called &#8220;htdocs&#8221; where you put the actual files that make up your website. This is where you put your PHP files. For MAMP, this folder will be in the MAMP folder that you put in your Applications folder earlier. For Mac users of XAMPP, this folder will be in the XAMPP folder that is in your Applications folder. For Windows users of MAMP, this will be in the XAMPP folder on your hard drive. For Linux users of XAMPP, this folder will be in your XAMPP folder. Found the htdocs folder? Good.

If you open the htdocs folder, you should see an &#8220;index.php&#8221; file (among others).  This is the default file that is run when a user goes to your URL (think of it as the home page). The server runs the PHP code in it, and the browser renders the HTML that the server sends it (as output of the PHP code).

Before we start editing it, we will need a PHP editor. We&#8217;re not going to be working on a ny major projects any time soon, so a simple, free one will suite the purpose just fine. For If you are on a Mac, I suggest you download a neat application called Komodo Edit (<a title="http://www.activestate.com/komodo-edit" href="http://www.activestate.com/komodo-edit" target="_blank">http://www.activestate.com/komodo-edit</a>). This program is also available for Windows, but Notepad++ (<a title="http://notepad-plus-plus.org/" href="http://notepad-plus-plus.org/" target="_blank">http://notepad-plus-plus.org/</a>)is also a great option.

Now that you have an editor, let&#8217;s start coding. First, open the index.php file that is in the htdocs folder (on Macintosh, you can right click index.php, choose &#8220;open with&#8221;, and  navigate to your editor; on Windows, you can go to File -> Open in your editor and choose index.php). Next, replace all the code that you see with the following:

<table border="0" align="center">
  <tr>
    <td>
      <pre>&lt;html&gt;</pre>
      
      <pre>&lt;head&gt;</pre>
      
      <pre>&lt;title&gt;My Cool PHP Page&lt;/title&gt;</pre>
      
      <pre>&lt;/head&gt;</pre>
      
      <pre>&lt;body&gt;</pre>
      
      <pre>&lt;?php</pre>
      
      <pre>echo "Hello World!";</pre>
      
      <pre>?&gt;</pre>
      
      <pre>&lt;/body&gt;</pre>
      
      <pre>&lt;/html&gt;</pre>
    </td>
  </tr>
</table>

To view the result, save the PHP document, start your Apache server, and go to <a title="http://localhost" href="http://localhost" target="_blank">http://localhost</a> .

You should already understand the HTML, and we won&#8217;t be going over that. You should, however, take note that a PHP document is really a HTML document with special code. What you probably aren&#8217;t familiar with is the chunk of code that starts with &#8220;<?php&#8221; and ends with &#8220;?>&#8221;. This is the PHP code. When working with PHP, you have to enclose the code with the tags &#8220;<?php&#8221; (for opening the section) and &#8220;?>&#8221; (for closing the section). As for the &#8221; echo &#8216;Hello World!&#8217;; &#8220;, this will output &#8220;Hello World!&#8221; to the HTML document. &#8220;Echo&#8221; is a language construct that behaves like a function. It is used to output strings of text to the HTML document. The text that you want outputted must be in parenthesis, although it will work with both single and double parenthesis. You may want to use one or the other based on what you are outputting. For example, if I wanted to output double quotations, I would want to use single quotations (otherwise the computer would get confused and think I were ending my string of text in the middle of it). And that is your standard &#8220;Hello World!&#8221; in PHP!
