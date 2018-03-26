---
id: 1997
title: 'PHP Tutorial 1 &#8211; About PHP &#038; Installing MAMP And XAMPP'
date: 2011-07-28T22:53:30+00:00
author: Nikhil Palanki
layout: single
guid: /?p=1997
permalink: /2011/07/28/php-tutorial-i-about-php-installing-mamp-and-xampp/
image: /wp-content/uploads/2011/07/PHP-icon.jpeg
categories:
  - PHP
tags:
  - lamp
  - mamp
  - php
  - tutorial
  - wamp
  - xampp
---
[<img class="aligncenter size-full wp-image-2185" title="PHP icon" src="/wp-content/uploads/2011/07/PHP-icon.jpeg" alt="" width="238" height="283" srcset="/wp-content/uploads/2011/07/PHP-icon.jpeg 238w, /wp-content/uploads/2011/07/PHP-icon-180x214.jpeg 180w" sizes="(max-width: 238px) 100vw, 238px" />](/wp-content/uploads/2011/07/PHP-icon.jpeg)

PHP is one of the most useful and powerful scripting languages in web development. Facebook was mostly coded using PHP (along with the help of database management system Mysql). You can create an entire search engine for a website using PHP. The possibilities are endless. But the main reasons that PHP is so great is that it is easy to use and it allows for rapidly changing web pages. One can even just incorporate a little bit of PHP into their HTML document and voila! PHP all done!

<p style="text-align: center;">
  <span style="font-size: large;"><strong>What is PHP?</strong></span>
</p>

PHP stands for &#8220;PHP: Hypertext Preprocessor&#8221;. It was first designed by Rasmus Lerdorf back in 1994 with the goal of recording website traffic and displaying his résumé. Since then, a number of developers have stepped in and further developed the language.

PHP is used for server-side scripting. That is, PHP code is interpreted, run, and compiled by the server it is on. Scripting and markup languages such as Javascript and HTML, on the other hand, are executed by a browser. Understand the difference? Good.

When PHP code is compiled and run, it results in HTML. This HTML is then sent to the browser that is requesting a web page. PHP is extremely useful for creating dynamic web pages. The content of these pages can constantly change depending on what information the PHP code is given. This is done by means of variables and functions (which you should be familiar with if you have worked with almost any programming language). Enough of my blabbering, let&#8217;s set up our PHP environments and start coding!

<p style="text-align: center;">
  <span style="font-size: large;"><strong>Installing A Server Environment</strong></span>
</p>

<p style="text-align: left;">
  Most computers don&#8217;t come with PHP installed. An exception is Macintosh, but you&#8217;ll still want to install a complete server environment even if you are on a Mac.
</p>

<p style="text-align: left;">
  Server environment installers and managers install all the necessary libraries and programs necessary to run PHP, Mysql, Apache, and more (depending on which server environment you go with). There are a large number of these environment packages available, and it can seem a little overwhelming. Allow me to break it down for you and instruct you on how to choose and install them.
</p>

<table border="0" align="center">
  <tr>
    <td>
      <strong>Environment & What It Stands For/What It Offers</strong>
    </td>
    
    <td>
      <strong>Operating System(s) It Can Run On</strong>
    </td>
    
    <td>
      <strong>How To Install</strong>
    </td>
  </tr>
  
  <tr>
    <td>
      MAMP &#8211; Mac Apache Mysql PHP
    </td>
    
    <td>
      Mac
    </td>
    
    <td>
       Head on over to <a title="http://www.mamp.info/en/downloads/index.html" href="http://www.mamp.info/en/downloads/index.html" target="_blank">http://www.mamp.info/en/downloads/index.html</a> and hit the big download link at the top of the page. This will download a zip file containing the software installer packages for the MAMP software. Run the package to install MAMP. Done.
    </td>
  </tr>
  
  <tr>
    <td>
      WAMP &#8211; Windows, Apache, Mysql, PHP
    </td>
    
    <td>
      Windows
    </td>
    
    <td>
       Go to <a title="http://www.wampserver.com/en/download.php" href="http://www.wampserver.com/en/download.php" target="_blank">http://www.wampserver.com/en/download.php</a> and click the corresponding download link. Simply run the executable to install.
    </td>
  </tr>
  
  <tr>
    <td>
      LAMP &#8211; Linux, Apache, Mysql, PHP
    </td>
    
    <td>
      Linux
    </td>
    
    <td>
      LAMP doesn&#8217;t come in a nice bundle of software, you have to install each element separately. Due to this, I&#8217;m just going to refer you to this helpful tutorial: <a title="http://www.howtoforge.com/ubuntu_lamp_for_newbies" href="http://www.howtoforge.com/ubuntu_lamp_for_newbies" target="_blank">http://www.howtoforge.com/ubuntu_lamp_for_newbies</a>
    </td>
  </tr>
  
  <tr>
    <td>
      XAMPP
    </td>
    
    <td>
      Mac, Windows, Linux, Solaris
    </td>
    
    <td>
       Click on over to <a title="http://www.apachefriends.org/en/xampp.html" href="http://www.apachefriends.org/en/xampp.html" target="_blank">http://www.apachefriends.org/en/xampp.html</a> and select your operating system from the list. After you download the file from the page that you are sent to, follow the detailed instructions on the download page to install.
    </td>
  </tr>
</table>

&nbsp;

For the purposes of this series of tutorials, I suggest you use MAMP if you are on a Mac, and XAMPP if you are on Windows or Linux. If MAMP doesn&#8217;t work for you for some reason, try XAMPP. If XAMPP on Windows doesn&#8217;t work for you, try WAMP.

Now let&#8217;s make sure we&#8217;ve got our environment set up correctly (and go over starting all the necessary servers). Each has a slightly different start procedure, so I&#8217;m going to go through them separately.

<p style="text-align: center;">
  <span style="font-size: large;"><strong>MAMP</strong></span>
</p>

<p style="text-align: left;">
  There are two ways to start up the MAMP server. The first is using the MAMP app that comes bundled with the MAMP software. Navigate to the MAMP folder that you installed to your Applications folder. The MAMP application is in this folder. Upon opening it, a small control window will pop up. If the server statuses don&#8217;t switch to the on position automatically, click the &#8220;start servers&#8221; button. Next, click the &#8220;preferences&#8230;&#8221; button, and, in the &#8220;ports&#8221; tab, click &#8220;set to default Apache and MySQL ports&#8221; button.
</p>

<p style="text-align: left;">
  <a href="/wp-content/uploads/2011/07/mamp-screenshot.jpeg"><img class="aligncenter size-full wp-image-2200" title="mamp screenshot" src="/wp-content/uploads/2011/07/mamp-screenshot.jpeg" alt="" width="430" height="350" srcset="/wp-content/uploads/2011/07/mamp-screenshot.jpeg 430w, /wp-content/uploads/2011/07/mamp-screenshot-300x244.jpeg 300w, /wp-content/uploads/2011/07/mamp-screenshot-350x285.jpeg 350w, /wp-content/uploads/2011/07/mamp-screenshot-180x146.jpeg 180w, /wp-content/uploads/2011/07/mamp-screenshot-360x293.jpeg 360w" sizes="(max-width: 430px) 100vw, 430px" /></a>
</p>

<p style="text-align: left;">
  An alternative way (that I prefer) is using the dashboard widget. Unfortunately, the only way to get it is to download the old version of MAMP (the link can be found at the bottom of the MAMP download page). It&#8217;s in the MAMP folder that is in the disk image (MAmp Control.wdgt). Once the widget is installed (double-click it), all you have to do is click the start button on the widget when viewing your dashboard.
</p>

<p style="text-align: left;">
  Once all of the lights are green and everything is running, go to <a title="http://localhost/MAMP/" href="http://localhost/MAMP/" target="_blank">http://localhost/MAMP/</a> . You should see the &#8220;Welcome to MAMP&#8221; screen.
</p>

<p style="text-align: center;">
  <span style="font-size: large;"><strong>XAMPP</strong></span>
</p>

 On Macintosh, starting your server is as easy as opening the &#8220;XAMPP Control&#8221; application that is in the XAMPP folder. If you installed it as described in the instructions, the XAMPP folder is in your Applications folder. Upon opening it, a small control window will open. Start Apache. If all is well, you should see the XAMPP splash screen when you go to <a title="http://localhost" href="http://localhost" target="_blank">http://localhost</a> .

On Windows, you can access the XAMPP control panel by clicking on the &#8220;XAMPP Control Panel&#8221; shortcut that was made on your desktop during the installation. Start &#8220;Apache&#8221;, and navigate to <a title="http://localhost" href="http://localhost" target="_blank">http://localhost</a> . You should see the XAMPP splash screen.

[<img class="aligncenter size-full wp-image-2201" title="xampp windows splash" src="/wp-content/uploads/2011/07/xampp-windows-splash.png" alt="" width="449" height="309" srcset="/wp-content/uploads/2011/07/xampp-windows-splash.png 449w, /wp-content/uploads/2011/07/xampp-windows-splash-300x206.png 300w, /wp-content/uploads/2011/07/xampp-windows-splash-168x117.png 168w, /wp-content/uploads/2011/07/xampp-windows-splash-263x180.png 263w, /wp-content/uploads/2011/07/xampp-windows-splash-180x123.png 180w, /wp-content/uploads/2011/07/xampp-windows-splash-360x247.png 360w" sizes="(max-width: 449px) 100vw, 449px" />](/wp-content/uploads/2011/07/xampp-windows-splash.png)

On Linux, starting XAMPP is as easy as running the command &#8220;/opt/lampp/lampp start&#8221;. Point your browser to <a title="http://localhost" href="http://localhost" target="_blank">http://localhost</a> and you should see the XAMPP splash screen.

I hope you found this tutorial helpful! In our next tutorial, we are going to go over where to put our PHP files, what we should use to edit them, and a how to write basic program in PHP.
