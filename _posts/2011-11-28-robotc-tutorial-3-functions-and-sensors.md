---
id: 3203
title: 'RobotC Tutorial 3 &#8211; Functions'
date: 2011-11-28T14:39:38+00:00
author: Murf
layout: single
guid: /?p=3203
permalink: /2011/11/28/robotc-tutorial-3-functions-and-sensors/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
onswipe_thumb:
  - /wp-content/uploads/2011/09/RobotC.jpeg
image: /wp-content/uploads/2011/09/RobotC.jpeg
categories:
  - RobotC
tags:
  - function
  - robotc
---
<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/09/RobotC.jpeg"><img class="aligncenter size-full wp-image-2736" title="RobotC" src="/wp-content/uploads/2011/09/RobotC.jpeg" alt="" width="290" height="137" srcset="/wp-content/uploads/2011/09/RobotC.jpeg 290w, /wp-content/uploads/2011/09/RobotC-180x85.jpeg 180w" sizes="(max-width: 290px) 100vw, 290px" /></a>
</p>

<p style="text-align: center;">
  <strong>To make life easier when programming, sometimes people may use things called functions. Functions are blocks of code that perform a specific task. Fuctions can be used to reduce the complexity of a code, and to make it more clear. In RobotC, I use functions a lot because they help other people understand what the code does.</strong>
</p>

<p style="text-align: left;">
  Let&#8217;s start out basic. Functions in RobotC are made by typing <strong>void name()</strong>. Replace name with the name of your function, and you&#8217;re set. Let&#8217;s take a look at a sample program I made.
</p>

<pre class="prettyprint lang-YOURLANG">void one()
{
motor[motorB] = 50;
motor[motorC] = 50;
}
void two()
{
motor[motorB] = -50;
motor[motorC] = -50;
}
task main() {
one();
wait1Msec(1000);
two();
wait1Msec(2000);
}</pre>

<p style="text-align: left;">
  This is a simple example of functions. In the task main, it runs the function &#8220;one&#8221;, which codes for going forward, for one second. I then runs &#8220;two&#8221;, which codes for going backward, for two seconds. In order to include a function defined outside of the main function, you use the format &#8220;name();&#8221;. Functions can be used for much more than this, but this is a simple example. We will be using them more in the next tutorial, using sensors.
</p>
