---
id: 2697
title: 'Cocos2D For iPhone Tutorial 3 &#8211; Moving Sprites'
date: 2011-09-10T11:15:16+00:00
author: Ipodnerd
layout: single
guid: /?p=2697
permalink: /2011/09/10/cocos2d-for-iphone-tutorial-3-moving-sprites/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/06/cocos2d.png
categories:
  - Cocos2D
tags:
  - cocos2d
  - ios
  - iphone
  - moving sprites
  - sprite
---
[<img class="aligncenter size-full wp-image-769" title="cocos2d" src="/wp-content/uploads/2011/06/cocos2d.png" alt="" width="160" height="237" />](/wp-content/uploads/2011/06/cocos2d.png)

In our last tutorial, we covered [making a sprite](/2011/07/15/cocos2d-for-iphone-tutorial-2-make-a-sprite-not-the-drink/ "Cocos2D For iPhone Tutorial 2 –  Make A Sprite (Not The Drink!)") appear on the screen. In this tutorial, we will be moving a sprite across the screen by using a technique called &#8220;animation&#8221;. In animation, a succession of new positions are combined to give the illusion of movement. Think &#8220;Steamboat Willie&#8221;, the famous Walt Disney cartoon. It was created with thousands of drawings all strung together and played in quick succession. Similarly, we will set a new position for our sprite in every frame. This new position will be right next to the last, and when the app is opened, these frames containing the new positions will be played in quick succession. Unlike cartoons, however, this animation will only consist of the movement of a single static object.

<p style="text-align: center;">
  <span class="vvqbox vvqyoutube" style="width:585px;height:330px;"><span id="vvq-2697-youtube-1"><a href="http://www.youtube.com/watch?v=BBgghnQF6E4"><img src="http://img.youtube.com/vi/BBgghnQF6E4/0.jpg" alt="YouTube Preview Image" /></a></span></span>
</p>

To begin the coding process for animating our sprite, we must first have a sprite. We already did that in the last tutorial, so let&#8217;s simply work with that code. If you don&#8217;t already have it, go to the last tutorial and copy and paste the code into Xcode.

The things that we will need to add to our program in order to accomplish animation include a line that will call a method every frame, and the method that is called every frame.

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import "HelloWorldScene.h"</pre>
      
      <pre>CCSprite *icon;</pre>
      
      <pre>@implementation HelloWorld</pre>
      
      <pre>+(id) scene</pre>
      
      <pre>{</pre>
      
      <pre>CCScene *scene = [CCScene node];</pre>
      
      <pre>HelloWorld *layer = [HelloWorld node];</pre>
      
      <pre>[scene addChild: layer];</pre>
      
      <pre>return scene;</pre>
      
      <pre>}</pre>
      
      <pre>-(id) init</pre>
      
      <pre>{</pre>
      
      <pre>if( (self=[super init] )) {</pre>
      
      <pre>icon = [CCSprite spriteWithFile:@"Icon.png"];</pre>
      
      <pre>icon.position = ccp(300,200);</pre>
      
      <pre>[self addChild:icon];</pre>
      
      <pre><span style="color: #ff0000;">[self schedule:@selector(DoEveryFrame:)];</span></pre>
      
      <pre>}</pre>
      
      <pre>return self;</pre>
      
      <pre>}</pre>
      
      <pre>- (void) dealloc</pre>
      
      <pre>{</pre>
      
      <pre>[super dealloc];</pre>
      
      <pre>}</pre>
      
      <pre><span style="color: #ff0000;">-(void) DoEveryFrame: (ccTime)dt{</span></pre>
      
      <pre><span style="color: #ff0000;">icon.position = ccp(icon.position.x + 150*dt, icon.position.y);</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre>@end</pre>
    </td>
  </tr>
</table>

&nbsp;

**<span style="font-size: large;">[self schedule:@selector(DoEveryFrame:)];</span>**

This line will run the &#8220;schedule&#8221; method of the &#8220;self&#8221; object. When calling a method that is in the same class as the method you are working on, you use &#8220;self&#8221; instead of the name of your object to refer to the class. In this case, our class is CCLayer. The &#8220;schedule&#8221; method runs the method that is passed into it every frame. The method that we are passing into it is &#8220;DoEveryFrame.&#8221;

&nbsp;

**<span style="font-size: large;">-(void) DoEveryFrame: (ccTime)dt{</span>**

**<span style="font-size: large;">icon.position = ccp(icon.position.x + 150*dt, icon.position.y);</span>**

**<span style="font-size: large;">}</span>**

This is the method &#8220;DoEveryFrame.&#8221; It requires that that the paramater &#8220;ccTime&#8221; be passed into it. The variable &#8220;dt&#8221; will be set equal to &#8220;ccTime&#8221; so that we can use it in our method code. ccTime will give us the difference in time from when the DoEveryFrame method was last called. The only line of code in our method is going to be the one that sets a new position for our sprite. It basically sets the position equal to the point with an x-coordinate that is the current x-coordinate _plus_ 150 pixels times the difference in time since the last frame (usually fractions of a second), and a y-coordinate  that is the same as the current y-coordinate. The net effect is that our sprite will appear to slide right on our screen. The reason we use the difference in time is to make sure that the sprite moves 150 pixels a second no matter what the frame rate is.

If we run the program now, the cocos2d icon will appear on the screen and then slide to the right. It keeps on going even after it goes off the screen. The next thing we&#8217;re going to to is prevent it from going off screen by resetting its position to the left side of the screen once it&#8217;s reached the right side of the screen. We can do this with a simple <a title="Objective-C Tutorial 3 – If Else Statements And Basic Looping" href="/2011/07/13/objective-c-tutorial-3-if-else-statements-and-basic-looping/" target="_blank">if-else statement</a> that essentially says &#8220;if the x-coordinate is greater than this value, then change the x-coordinate to this.&#8221;

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import "HelloWorldScene.h"</pre>
      
      <pre>CCSprite *icon;</pre>
      
      <pre>@implementation HelloWorld</pre>
      
      <pre>+(id) scene</pre>
      
      <pre>{</pre>
      
      <pre>CCScene *scene = [CCScene node];</pre>
      
      <pre>HelloWorld *layer = [HelloWorld node];</pre>
      
      <pre>[scene addChild: layer];</pre>
      
      <pre>return scene;</pre>
      
      <pre>}</pre>
      
      <pre>-(id) init</pre>
      
      <pre>{</pre>
      
      <pre>if( (self=[super init] )) {</pre>
      
      <pre>icon = [CCSprite spriteWithFile:@"Icon.png"];</pre>
      
      <pre>icon.position = ccp(300,200);</pre>
      
      <pre>[self addChild:icon];</pre>
      
      <pre>[self schedule:@selector(DoEveryFrame:)];</pre>
      
      <pre>}</pre>
      
      <pre>return self;</pre>
      
      <pre>}</pre>
      
      <pre>- (void) dealloc</pre>
      
      <pre>{</pre>
      
      <pre>[super dealloc];</pre>
      
      <pre>}</pre>
      
      <pre>-(void) DoEveryFrame: (ccTime)dt{</pre>
      
      <pre>icon.position = ccp(icon.position.x + 150*dt, icon.position.y);</pre>
      
      <pre><span style="color: #ff0000;">if (icon.position.x &gt; 480+30) {</span></pre>
      
      <pre><span style="color: #ff0000;">icon.position = ccp(-30, icon.position.y);</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
    </td>
  </tr>
</table>

&nbsp;

**<span style="font-size: large;">if (icon.position.x > 480+30) {</span>**

**<span style="font-size: large;">icon.position = ccp(-30, icon.position.y);</span>**

**<span style="font-size: large;">}</span>**

This is the if-else statement. In plain English, it says &#8220;If the x-coordinate of the icon sprite is greater than 480 + 30, then set its  x-coordinate to -30 and leave the y-coordinate the same as it currently is.&#8221; The reason we chose 480 + 30 as the x-coordinate at which the position is reset is because the width of the screen is 480 pixels, and half the width of our sprite is 30 pixels. That way, the icon re-appears on the left side of the screen at the same time it disappears off the right side of the screen.

Upon running the above code, your sprite will move across the screen, re-appearing on the left side of the screen as it goes off the right side. I encourage you to mess around with the positions in the DoEveryFrame method. See if you can get the sprite to scroll vertically or even diagonally!
