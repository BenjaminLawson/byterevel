---
id: 2854
title: 'RobotC Tutorial 2 &#8211; Hello World And Programming'
date: 2011-09-28T19:48:35+00:00
author: Murf
layout: single
guid: /?p=2854
permalink: /2011/09/28/robotc-tutorial-2-hello-world-and-programming/
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
  - robotc
  - tutorial
---
<p style="text-align: center;">
  <strong><span style="text-decoration: underline;"><a href="/wp-content/uploads/2011/09/RobotC.jpeg"><img class="aligncenter size-full wp-image-2736" title="RobotC" src="/wp-content/uploads/2011/09/RobotC.jpeg" alt="" width="290" height="137" srcset="/wp-content/uploads/2011/09/RobotC.jpeg 290w, /wp-content/uploads/2011/09/RobotC-180x85.jpeg 180w" sizes="(max-width: 290px) 100vw, 290px" /></a></span></strong>
</p>

<p style="text-align: center;">
  <strong>Now that you&#8217;ve got the basics for the Lego Mindstorms, we can start programming. To start, open up RobotC and open a new file. Outputting text is the first thing you will do with almost any programming language, so let&#8217;s start with a program that displays &#8220;Hello World&#8221; on the screen. Note that this program will not be very useful in actual programming, but I&#8217;m doing this to demonstrate that RobotC can display &#8220;Hello World&#8221;.</strong>
</p>

<table border="0" align="center">
  <tr>
    <td>
      <pre>task main() //the start of all RobotC programs</pre>
      
      <pre>{  // the start of the function</pre>
      
      <pre>eraseDisplay();      //clear the NXT display</pre>
      
      <pre>// now to display "Hello World"</pre>
      
      <pre>nxtDisplayCenteredBigTextLine(2, "Hello");</pre>
      
      <pre>nxtDisplayCenteredBigTextLine(4, "World!");</pre>
      
      <pre>while (true);</pre>
      
      <pre>//loop until program is terminated (so we can read the display)</pre>
      
      <pre>}  //the end of the function</pre>
    </td>
  </tr>
</table>

&nbsp;

This is what it will look like. Don&#8217;t worry about the commands, for they are not used much in RobotC.

**<span style="text-decoration: underline;"><a href="/wp-content/uploads/2011/09/hello-world-robotc.jpg"><img class="aligncenter size-full wp-image-2986" title="hello-world-robotc" src="/wp-content/uploads/2011/09/hello-world-robotc.jpg" alt="" width="251" height="353" srcset="/wp-content/uploads/2011/09/hello-world-robotc.jpg 251w, /wp-content/uploads/2011/09/hello-world-robotc-213x300.jpg 213w, /wp-content/uploads/2011/09/hello-world-robotc-180x253.jpg 180w" sizes="(max-width: 251px) 100vw, 251px" /></a><br /> </span>**

<p style="text-align: center;">
  <strong>Now that we have that out of the way, we can start with the actual programming. Let&#8217;s start with a basic program that tells you robot to move forward and backward.</strong>
</p>

<table border="0" align="center">
  <tr>
    <td>
      <pre>task main()  //this is the starting for all RobotC program</pre>
      
      <pre>{  //the start of the function</pre>
      
      <pre>motor[motorB] = 50;  //tells the robot's B motor to go forward at 50 power</pre>
      
      <pre>motor[motorC] = 50;  //tells the robot's C motor to go forward at 50 power</pre>
      
      <pre>wait1Msec(1000);  //runs previous tasks for 1000 milliseconds, or 1 second</pre>
      
      <pre>motor[motorB] = -40;  //tells the robot's B motor to go backward at 40 power</pre>
      
      <pre>motor[motorC] = -40;  //tells the robot's C motor to go backward at 40 power</pre>
      
      <pre>wait1Msec(2000);  //runs previous tasks for 2000 milliseconds, or 2 second</pre>
      
      <pre>}  //the end of the function</pre>
    </td>
  </tr>
</table>

<p style="text-align: left;">
  <p style="text-align: left;">
    This program makes the robot move forward at 50% power for 1 second,and then move backwards at 40% power for 2 seconds. For the power, I would advise that you dont run the power at 100 because the robot has a PID control that speeds up or slows down to get the desired speed. having the motor at 100 power will not allow the PID control to speed up the motor to get the desired speed. No need to understand that now, I will explain it more in a different tutorial.
  </p>
  
  <p style="text-align: left;">
    So, positive values make the robot go forward, and negative values make the robot go backwards. How do I make it turn?
  </p>
  
  <p style="text-align: left;">
    There are two simple ways to turn your robot. There are other ways, but that&#8217;ll come later. This is another simple program demonstrating them.
  </p>
  
  <table border="0" align="center">
    <tr>
      <td>
        <pre>task Main
{</pre>
        
        <pre>motor[motorB] = 50;</pre>
        
        <pre>motor[motorC] = -50;</pre>
        
        <pre>wait1Msec(400);</pre>
        
        <pre>motor[motorB] = 0;</pre>
        
        <pre>motor[motorC] = 50;</pre>
        
        <pre>wait1Msec(800);</pre>
        
        <pre>}</pre>
      </td>
    </tr>
  </table>
  
  <p style="text-align: left;">
    <p style="text-align: left;">
      First, this program tells the robot to turn on a dime to the left (assuming the B motor is the right one) for .4 seconds. It then tells the robot to turn in an arc for .8 seconds. That&#8217;s all for now, I&#8217;ll see you next time when I&#8217;m explaining functions!
    </p>
