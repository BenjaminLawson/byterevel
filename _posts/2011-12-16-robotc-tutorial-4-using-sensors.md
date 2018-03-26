---
id: 3236
title: 'RobotC Tutorial 4 &#8211; Using Sensors'
date: 2011-12-16T22:21:14+00:00
author: Murf
layout: single
guid: /?p=3236
permalink: /2011/12/16/robotc-tutorial-4-using-sensors/
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
  - sensors
---
<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/09/RobotC.jpeg"><img class="aligncenter size-full wp-image-2736" title="RobotC" src="/wp-content/uploads/2011/09/RobotC.jpeg" alt="" width="290" height="137" srcset="/wp-content/uploads/2011/09/RobotC.jpeg 290w, /wp-content/uploads/2011/09/RobotC-180x85.jpeg 180w" sizes="(max-width: 290px) 100vw, 290px" /></a>
</p>

Sensors are the main part of the NXT, and are the items that the NXT is most useful for. The NXT has four types sensors that come with it: the ultrasonic sensor, the light sensor, the touch sensor, and the sound sensor. Later models come with a color sensor that replaces light, but I prefer the light over color. Let&#8217;s get straight to programming.

<pre class="prettyprint lang-C">#pragma config(Sensor, S1, touch, sensorTouch)</pre>

What&#8217;s this, you say? It is saying that the sensor is in sensor port 1, named &#8220;touch&#8221;, and it is a touch sensor. Now we dont want to type that every time, so to automatically insert it, go to Robot>Motors and Sensors Setup, and go to the sensor tab to fill in the sensor info. Click OK and the text should be at the top of your code. You need these lines to have the sensors work.

In order to program sensors, we need to learn two simple but very helpful statements. These are the &#8220;While&#8221; and &#8220;If&#8221; statements. In this tutorial, though, I will just be going over the while statement. Let&#8217;s look at another program.

<pre class="prettyprint lang-C">while(SensorValue(touch) == 0)
{
motor[motorC] = 50;
motor[motorB] = 50;
}

motor[motorB] = -50;
motor[motorC] = -50;
wait1Msec(500);</pre>

This tells the robot to go forward while the touch sensor is not pressed, the go back a little when it is pressed. For the first line here, you put the name of the sensor, in this case &#8220;touch&#8221; in the parenthesis, use an equality (==) or inequality (!=) sign, and a set a value. For the touch sensor, there are only two values, 0 (not pressed) or 1 (pressed). For the ultrasonic sensor, the value is distance, and for color, the value is the reflected light. I don&#8217;t use the sound sensor very often because I think it does not have much value in programs. Now here is a more complex program using ultrasonic and touch sensors.

<pre class="prettyprint lang-C">#pragma config(Sensor, S1, touch, sensorTouch)
#pragma config(Sensor, S4, sonar, sensorSONAR)

task main()
{
while(true)
{
while(SensorValue(touch) == 1)
{
motor[motorD] = -25;
motor[motorE] = -25;
wait1Msec(200);

motor[motorD] = 25;
motor[motorE] = -25;
wait1Msec(250);
}
while(SensorValue(sonar) &lt; 25)
{
motor[motorD] = 0;
motor[motorE] = 0;
wait1Msec(250);
PlaySound(soundBeepBeep);
}

motor[motorD] = 25;
motor[motorE] = 25;
}
}</pre>

What you might notice here is the &#8220;while(true)&#8221;. This is an infinite loop so the program will run forever (or until you stop it.) I use that to loop the program. This program codes the robot to, while the touch sensor is pressed, back up and turn. Also, while there is an object in the way, it will stop and play an annoying beeping sound until you move the object. When everything is clear, the robot will simply go forward.

Now, how can we incorporate functions into this? Let&#8217;s take a look.

<pre class="prettyprint lang-C">task main()

while(true)
{
while(SensorValue(touch) == 1)
{
one();
}
while(SensorValue(sonar) &lt; 25)
{
two();
}
}</pre>

So, while the touch sensor is pressed, it will run the function &#8220;one&#8221;, and when there is an object in the robot&#8217;s way, it will run the function &#8220;two&#8221;.

That is all for now. Next time, we will look at the light sensor more and I will show you how to follow lines. If you have any questions, be brave and leave a comment!
