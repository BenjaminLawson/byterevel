---
id: 4924
title: BeardedSpice for Mac Lets You Control Any Music Website with Your Media Keys
date: 2016-08-21T20:49:24+00:00
author: Ben Lawson
layout: single
guid: /?p=4924
permalink: /2016/08/21/beardedspice-for-mac-lets-you-control-any-music-website-with-your-media-keys/
image: /wp-content/uploads/2016/08/icon1024.png
header:
  teaser: /wp-content/uploads/2016/08/icon1024.png
categories:
  - Music
  - Software
tags:
  - itunes
  - mac
  - music
  - Software
  - soundcloud
  - spotify
  - vlc
---

![BeardedSpice]({{ site.url }}/wp-content/uploads/2016/08/icon1024.png)

Have you ever tried to pause your music with your native media keys only to accidentally start up iTunes and have multiple songs playing at once? Have you ever had the absurd notion that pressing the &#8220;skip&#8221; button should play the next video in a YouTube playlist? You aren&#8217;t alone. Providing this intuitive functionality has been the goal of open source project [BeardedSpice](http://beardedspice.github.io/) since late 2013, and the [list of services it supports](https://github.com/beardedspice/beardedspice#supported-sites) is huge! It even supports now defunct websites like GrooveShark (yikes, if a contributor is reading this, please removing this!).

BeardedSpice lives in your menu bar. It will attempt to control the currently focused tab or application, but you can also select the service you want to control from its dropdown menu.

It would seem that the ability to pause any media playing should be native functionality for all Macs, but implementing specific javascript hooks for controlling web applications is delicate and messy at the best of times. BeardedSpice works by applying scripts developed by the community to supported websites that interact with their javascript controls, so support can indeed break at any time, and adding support for websites is time consuming.

To maintain consistency, the utility also supports popular native media players like [Spotify](/2011/07/14/music-streaming-service-spotify-is-now-available-in-the-u-s/) and [VLC](/2011/06/24/vlc-the-media-playback-gurus-one-tool/).

<img class="size-full wp-image-4930 aligncenter" src="/wp-content/uploads/2016/08/beardedspice-screenshot.jpg" alt="BeardedSpice Menu" width="319" height="187" srcset="/wp-content/uploads/2016/08/beardedspice-screenshot.jpg 319w, /wp-content/uploads/2016/08/beardedspice-screenshot-300x176.jpg 300w, /wp-content/uploads/2016/08/beardedspice-screenshot-180x106.jpg 180w" sizes="(max-width: 319px) 100vw, 319px" />

If you don&#8217;t use a keyboard with media keys, fear not. BeardedSpice is highly configurable and allows you to bind any keys to &#8216;previous&#8217;, &#8216;pause/play&#8217;, and &#8216;next&#8217; actions. Be sure to set it to launch on login!

This is a great opportunity to make contributions to an open source project that will be noticed and appreciated. If a website you use isn&#8217;t yet supported, consider [having a go at it](https://github.com/beardedspice/beardedspice) and submitting your plugin to the project. There are also a few open issues with websites that people already want support for.
