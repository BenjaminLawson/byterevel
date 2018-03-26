---
id: 4683
title: 'Perl Tutorial &#8211; Building a Local Network'
date: 2014-07-07T15:33:48+00:00
author: Nikhil Palanki
layout: single
guid: /?p=4683
permalink: /2014/07/07/perl-tutorial-building-a-local-network/
image: /wp-content/uploads/2014/07/PERL.gif
categories:
  - Perl
tags:
  - introduction to perl networking
  - perl networking
  - sockets in perl
  - What do sockets do?
---
Perl is slowly growing out of fashion, despite it&#8217;s ubiquitous influence on developing modern languages. Much of Perl&#8217;s syntax and structure has been cleaned up and made more accessible via Python, thus many developers would favor Python instead of Perl. Yet, Larry Wall&#8217;s creation is still relevant to understanding modern programming. In this tutorial, we&#8217;ll build a local network in Perl to showcase it&#8217;s ease of networking via socketry.

**Sockets**

If you&#8217;re unfamiliar with networking, here is a brief overview of a socket. A socket is basically opening a connection on a computer via a port (computers have a certain amount of ports that they can communicate on with other computers). In order to use a socket, you first must &#8220;create&#8221; one or open it. Then, you must script something that tells the socket to accept incoming socket requests. Finally, you must tell the socket to do something otherwise it&#8217;s not very useful.

**Receiver End**

We&#8217;ll first build the receiver end of the Perl script. This end must be run first in order to create an open socket to receive incoming networks.

[<img class="aligncenter size-full wp-image-4684" src="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.51.35-PM.png" alt="Screen Shot 2014-07-07 at 3.51.35 PM" width="680" height="240" srcset="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.51.35-PM.png 680w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.51.35-PM-300x105.png 300w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.51.35-PM-180x63.png 180w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.51.35-PM-360x127.png 360w" sizes="(max-width: 680px) 100vw, 680px" />](/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.51.35-PM.png)

Enter the above code into your editor. There is a slight problem though. What if the port is being used? What if you have multiple networks going on or your running a server in port 8000. In that case, we need someway to stop the script if it cannot make a connection.

[<img class="aligncenter size-full wp-image-4685" src="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.55.46-PM.png" alt="Screen Shot 2014-07-07 at 3.55.46 PM" width="680" height="23" srcset="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.55.46-PM.png 680w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.55.46-PM-300x10.png 300w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.55.46-PM-180x6.png 180w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.55.46-PM-360x12.png 360w" sizes="(max-width: 680px) 100vw, 680px" />](/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.55.46-PM.png)

This script takes care of busy ports. Next, we  need to script the socket to do something when another machine/user tries to make a connection.

[<img class="aligncenter size-full wp-image-4686" src="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.59.44-PM.png" alt="Screen Shot 2014-07-07 at 3.59.44 PM" width="680" height="89" srcset="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.59.44-PM.png 680w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.59.44-PM-300x39.png 300w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.59.44-PM-180x23.png 180w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.59.44-PM-360x47.png 360w" sizes="(max-width: 680px) 100vw, 680px" />](/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-3.59.44-PM.png)

What this code will do is whenever something is being received, it will print what is being received into Terminal/Command Line. Now, let&#8217;s code the sending end of the network.

**Sending End**

Now we want to be able to send stuff over the port for the other user (which in this case would be yourself) to see.

[<img class="aligncenter size-full wp-image-4687" src="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.14.23-PM.png" alt="Screen Shot 2014-07-07 at 4.14.23 PM" width="680" height="374" srcset="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.14.23-PM.png 680w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.14.23-PM-300x165.png 300w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.14.23-PM-180x99.png 180w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.14.23-PM-360x198.png 360w" sizes="(max-width: 680px) 100vw, 680px" />](/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.14.23-PM.png)

**Running the Test**

For this network to work, open up two Terminal Windows and cd to the directory containing both the receiver.pl file and the sending.pl file. In one Terminal window, execute the following commands:

<div id="attachment_4689" style="max-width: 310px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.16.40-PM.png"><img class="wp-image-4689 size-full" src="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.16.40-PM.png" alt="Screen Shot 2014-07-07 at 4.16.40 PM" width="300" height="17" srcset="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.16.40-PM.png 300w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.16.40-PM-180x10.png 180w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Execute this in 1 Terminal
  </p>
</div>

<div id="attachment_4688" style="max-width: 310px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.17.13-PM.png"><img class="size-full wp-image-4688" src="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.17.13-PM.png" alt="Execute this in the other Terminal" width="300" height="15" srcset="/wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.17.13-PM.png 300w, /wp-content/uploads/2014/07/Screen-Shot-2014-07-07-at-4.17.13-PM-180x9.png 180w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Execute this in the other Terminal
  </p>
</div>

What you should see is nothing on one end and a prompt on the other Terminal asking to &#8220;Send Messages: &#8221;

Enter a message on one Terminal and hit enter. You should see it on the other Terminal.

**Experimentation**

Now that you&#8217;ve successfully created a mini-network using Perl, feel free to incorporate other features like sending files (which Perl handles nicely) or sending/intercepting messages (and possibly test some encryption methods). If you have any questions, feel free to ask!

&nbsp;

&nbsp;
