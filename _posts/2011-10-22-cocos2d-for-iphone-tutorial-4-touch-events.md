---
id: 3097
title: 'Cocos2D For iPhone Tutorial 4 &#8211; Touch Events'
date: 2011-10-22T11:47:44+00:00
author: Ipodnerd
layout: single
guid: /?p=3097
permalink: /2011/10/22/cocos2d-for-iphone-tutorial-4-touch-events/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
onswipe_thumb:
  - /wp-content/uploads/2011/07/cocos2d-logo.png
image: /wp-content/uploads/2011/07/cocos2d-logo.png
categories:
  - Cocos2D
tags:
  - cocos2d
  - touch events
---
[<img class="aligncenter size-full wp-image-1965" title="cocos2d logo" src="/wp-content/uploads/2011/07/cocos2d-logo.png" alt="" width="160" height="237" />](/wp-content/uploads/2011/07/cocos2d-logo.png)

&nbsp;

Welcome back to our Cocos2D tutorial series! Last time we went over the code that is used to move sprites on the screen. In this tutorial, I will be covering touch events.

There are four touch events that can occur in the process of touching the screen of any touch-enabled device. These are:

  * Touch Start (When you first touch the screen)
  * Touch Move (When you slide your finger across the screen)
  * Touch Cancel (When something disrupts the touch)
  * Touch End (When you lift your finger off of the screen)

<div>
  You can assign different code to be executed based upon touch events and the location of a touch. To demonstrate this, we will be creating a simple app in which the Cocos2D icon (or other image of your choice) moves to where you touch the screen. The code below is the final product, and I have removed the code for moving it across the screen (from the last tutorial).
</div>

<pre class="prettyprint linenumstrigger linenums lang-C">#import "HelloWorldScene.h"
#import "CCTouchDispatcher.h"

CCSprite *icon;
@implementation HelloWorld
+(id) scene
{
	CCScene *scene = [CCScene node];
	HelloWorld *layer = [HelloWorld node];
	[scene addChild: layer];
	return scene;
}
-(id) init
{
	if( (self=[super init] )) {
		icon = [CCSprite spriteWithFile:@"Icon.png"];
		icon.position = ccp(300,200);
		[self addChild:icon];

		[[CCTouchDispatcher sharedDispatcher]addTargetedDelegate:self priority:0 swallowsTouches:YES];
	}
	return self;
}
- (void) dealloc
{
	[super dealloc];
}
-(BOOL)ccTouchBegan:(UITouch *)touch withEvent:(UIEvent *)event{
	return YES;
}

-(void)ccTouchEnded:(UITouch *)touch withEvent:(UIEvent *)event{
	CGPoint location = [self convertTouchToNodeSpace: touch];

	[icon stopAllActions];
	[icon runAction:[CCMoveTo actionWithDuration:1 position:location]];
}
@end</pre>

If you run this program, you will find that it does exactly as I described above. A Cocos2D icon will appear on the screen and it will move to wherever you touch.

<pre class="prettyprint linenumstrigger linenums:2 lang-C">#import "CCTouchDispatcher.h"</pre>

Before we start working with touches, we have to import the CCTouchDispatcher header file. The code in this header file will allow us to work with touches.

<pre class="prettyprint linenumstrigger linenums:20 lang-C">[[CCTouchDispatcher sharedDispatcher]addTargetedDelegate:self priority:0 swallowsTouches:YES];</pre>

This line of code will tell CCLayer that our touch methods are going to be &#8220;Targeted&#8221; and in &#8220;self&#8221;, that our priority is 0 (high), and that we want to respond to touches.

<pre class="prettyprint linenumstrigger linenums:28 lang-C">-(BOOL)ccTouchBegan:(UITouch *)touch withEvent:(UIEvent *)event{
	return YES;
}</pre>

When working with touch events, the &#8220;touch start&#8221; method is mandatory, while the other touch events are optional. In Cocos2D, the name of the &#8220;touch start&#8221; method is &#8220;ccTouchBegan&#8221; and it returns a boolean value.

<pre class="prettyprint linenumstrigger linenums:32 lang-C">-(void)ccTouchEnded:(UITouch *)touch withEvent:(UIEvent *)event{
	CGPoint location = [self convertTouchToNodeSpace: touch];

	[icon stopAllActions];
	[icon runAction:[CCMoveTo actionWithDuration:1 position:location]];
}</pre>

The code within the &#8220;Touch End&#8221; event is run when the user releases their finger from the screen. The method itself is &#8220;ccTouchEnded&#8221;, and it doesn&#8217;t return any values (hence the &#8220;void&#8221;). Line one of our method sets the GCPoint (coordinate) &#8220;location&#8221; equal to the location of the touch. However, since the location of the touch isn&#8217;t a GCPoint, we must use the method &#8220;convertTouchToNodeSpace&#8221; to convert the touch location to GL coordinates, and then from GL coordinates to node-space. Next, we use the method &#8220;stopAllActions&#8221; to stop any actions that are currently in progress. With the code above, this line won&#8217;t actually make any difference (there are no other actions going on), but it is important to get in the habit of stopping all actions before initiating a new action. After we have stopped all actions, we use the method &#8220;runAction&#8221; to run the action specified in brackets. In this case, we move the icon to the location touched. &#8220;actionWithDuration&#8221; is used to specify how long we want the action to take place. In our program, we have set the duration to 1 second.

Now that you understand what the code is doing, it should make sense that, when running your app in the iPhone Simulator, nothing happens when you first click it, nor when you slid your finger across the screen. The action only happens when you remove your finger from the screen because that is the touch event at which our code starts running.

I hope that you have found this tutorial useful, and I encourage you to play around with these touch events. If you have any questions, or if you run into any problems, please leave a comment!
