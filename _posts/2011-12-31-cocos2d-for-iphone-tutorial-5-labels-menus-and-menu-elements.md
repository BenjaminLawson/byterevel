---
id: 3259
title: 'Cocos2D For iPhone Tutorial 5 &#8211; Labels, Menus, And Menu Elements'
date: 2011-12-31T12:16:25+00:00
author: Ipodnerd
layout: single
guid: /?p=3259
permalink: /2011/12/31/cocos2d-for-iphone-tutorial-5-labels-menus-and-menu-elements/
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
  - label
  - menu
  - menu element
---
[<img class="aligncenter size-full wp-image-1965" title="cocos2d logo" src="/wp-content/uploads/2011/07/cocos2d-logo.png" alt="" width="160" height="237" />](/wp-content/uploads/2011/07/cocos2d-logo.png)

We really wore our fingers raw in our last tutorial by running dozens of [touch events](/2011/10/22/cocos2d-for-iphone-tutorial-4-touch-events/ "Cocos2D For iPhone Tutorial 4 – Touch Events")! In this tutorial I will be showing you how to make a gorgeous button-filled menu for your iOS app. By menu, I mean an array of buttons that can either be made from an image label or a text label, and can have a function executed when they are pressed. These menus can either be placed in their own scene, like a game start menu, or as a control menu overlaid on a scene.

Before we can make a text label in a menu, we need to know how to make a text label. As you may have noticed, this is exactly what the default Cocos2D program does. However, the way it positions it on the screen is a little advanced, so here is my slightly modified version:

<pre class="prettyprint linenumstrigger linenums lang-C">#import "HelloWorldScene.h"

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

		CCLabelTTF *label = [CCLabelTTF labelWithString:@"Hello World" fontName:@"Times New Roman" fontSize:64];

		label.position = ccp(240,160);

		label.color = ccc3(255, 255, 255);

		[self addChild: label];
	}
	return self;
}

- (void) dealloc
{

	[super dealloc];
}
@end</pre>

The above code in _HelloWorldScene.m_ will output &#8220;Hello World&#8221; to the screen with the font &#8220;Marker Felt&#8221; and with the font size &#8220;64&#8221;.

<pre class="prettyprint linenumstrigger linenums:21 lang-C">CCLabelTTF *label = [CCLabelTTF labelWithString:@"Hello World" fontName:@"Marker Felt" fontSize:64];</pre>

This line creates a label called &#8220;label&#8221; that is the member of the CCLabelTTF class. In order to give it some basic properties, we have to set it equal to, or initialize it, with a CCLabelTTF object with a label, font, and font size. The label and the size are self-explanatory, but for more fonts check out <a title="http://chrissheldrick.com/blog/2011/04/10/cocos2d-cclabelttf-font-list/" href="http://iosfonts.com/" target="_blank">this list</a>.

<pre class="prettyprint linenumstrigger linenums:23 lang-C">label.position = ccp(240,160);</pre>

Like many objects in Cocos2D, labels have the property &#8220;position&#8221;. This line simply sets the position of the center of the label equal to the coordinate (240,160). Take note that this is a ccp, or CGPoint, coordinate. This is the kind of coordinate that you use in Cocos2D.

<pre class="prettyprint linenumstrigger linenums:25 lang-C">label.color = ccc3(255, 255, 255);</pre>

Another property that labels have is color. Here, we set the label&#8217;s color to white. It is unnecessary to set a color, and the default is white. The color is an RGB code, and I suggest you use a color picker like <a title="http://www.rapidtables.com/web/color/RGB_Color.htm" href="http://www.rapidtables.com/web/color/RGB_Color.htm" target="_blank">this one</a> to choose a color.

There you have it, we placed a simple label on the screen. There are other kinds of labels, but we will save them for later tutorials.

Next, let&#8217;s create our menu.

<pre class="prettyprint linenumstrigger linenums lang-C">#import "HelloWorldScene.h"

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

		CCLabelTTF *start = [CCLabelTTF labelWithString:@"Start!" fontName:@"Georgia-Bold" fontSize:25];
		CCLabelTTF *options = [CCLabelTTF labelWithString:@"Options" fontName:@"Georgia-Bold" fontSize:25];

		CCMenuItemLabel *item1 = [CCMenuItemLabel itemWithLabel:start target:self selector:@selector(startGame:)];
		CCMenuItemLabel *item2 = [CCMenuItemLabel itemWithLabel:options target:self selector:@selector(optionsPage:)];

		CCMenu *menu = [CCMenu menuWithItems:item1, item2, nil];
		[menu alignItemsVertically];

		[self addChild:menu];
	}
	return self;
}

-(void)startGame:(id)sender{
//code goes here
}

-(void)optionsPage:(id)sender{
//code goes here
}

- (void) dealloc
{

	[super dealloc];
}
@end</pre>

The above code will produce this:

<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/12/SimulatorMenu.png"><img class="aligncenter size-full wp-image-3287" title="SimulatorMenu" src="/wp-content/uploads/2011/12/SimulatorMenu.png" alt="" width="573" height="294" srcset="/wp-content/uploads/2011/12/SimulatorMenu.png 716w, /wp-content/uploads/2011/12/SimulatorMenu-300x154.png 300w, /wp-content/uploads/2011/12/SimulatorMenu-180x92.png 180w, /wp-content/uploads/2011/12/SimulatorMenu-360x185.png 360w" sizes="(max-width: 573px) 100vw, 573px" /></a>
</p>

<pre class="prettyprint linenumstrigger linenums:21,22 lang-C">CCLabelTTF *start = [CCLabelTTF labelWithString:@"Start!" fontName:@"Georgia-Bold" fontSize:25];
CCLabelTTF *options = [CCLabelTTF labelWithString:@"Options" fontName:@"Georgia-Bold" fontSize:25];</pre>

The first thing we have to do to create a menu item with a label is actually create the labels. These two lines of code create two labels with the font Georgia-Bold.

<pre class="prettyprint linenumstrigger linenums:24,25 lang-C">CCMenuItemLabel *item1 = [CCMenuItemLabel itemWithLabel:start target:self selector:@selector(startGame:)];
CCMenuItemLabel *item2 = [CCMenuItemLabel itemWithLabel:options target:self selector:@selector(optionsPage:)];</pre>

Next, we create two menu items, item1 and item2. They are of the class CCMenuItemLabel. We then have to initialize them with a label (the name of a CCLabelTTF object that has been created), a target, and a function to run when they are touched.

<pre class="prettyprint linenumstrigger linenums:35 lang-C">-(void)startGame:(id)sender{
//code goes here
}

-(void)optionsPage:(id)sender{
//code goes here
}</pre>

Skipping down a little bit, these are simply the two void functions that our menu items will call when they are touched. We will add some content to them in a later tutorial.

<pre class="prettyprint linenumstrigger linenums:27 lang-C">CCMenu *menu = [CCMenu menuWithItems:item1, item2, nil];</pre>

This line creates a menu called &#8220;menu&#8221; and it initializes the menu with the items &#8220;item1&#8221; and &#8220;item2&#8221;. We set the last item to &#8220;nil&#8221; to end our menu.

<pre class="prettyprint linenumstrigger linenums:28 lang-C">[menu alignItemsVertically];</pre>

Without this line, all of the elements on our menu would be stacked on top of each other. This line aligns our menu items vertically. You could also align the items horizontally, or specify the position of each menu item. By default, the menu is placed in the center of the screen, but we could also specify the exact position (menu.position) of the menu.

Our program now displays a nice text menu on the screen. However, if we were to make a game, we would want graphical menu items. No problem, we can do that in Cocos2D quickly and easily.

<pre class="prettyprint linenumstrigger linenums lang-C">#import "HelloWorldScene.h"

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
		CCMenuItem *item1 = [CCMenuItemImage itemFromNormalImage:@"start.png" selectedImage:@"startPressed.png" target:self selector:@selector(startGame:)];
		CCMenu *menu = [CCMenu menuWithItems:item1, nil];
		[menu alignItemsVertically];

		[self addChild:menu];
	}
	return self;
}

-(void)startGame:(id)sender{
//code goes here
}

- (void) dealloc
{

	[super dealloc];
}
@end</pre>

The above program will display the following when run:

<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/12/SimulatorMenuGraphic.png"><img class="aligncenter size-full wp-image-3291" title="SimulatorMenuGraphic" src="/wp-content/uploads/2011/12/SimulatorMenuGraphic.png" alt="" width="573" height="294" srcset="/wp-content/uploads/2011/12/SimulatorMenuGraphic.png 716w, /wp-content/uploads/2011/12/SimulatorMenuGraphic-300x154.png 300w, /wp-content/uploads/2011/12/SimulatorMenuGraphic-180x92.png 180w, /wp-content/uploads/2011/12/SimulatorMenuGraphic-360x185.png 360w" sizes="(max-width: 573px) 100vw, 573px" /></a>
</p>

<pre class="prettyprint linenumstrigger linenums:20 lang-C">CCMenuItem *item1 = [CCMenuItemImage itemFromNormalImage:@"start.png" selectedImage:@"startPressed.png" target:self selector:@selector(startGame:)];</pre>

This line creates a menu item called &#8220;item1&#8221; that is initialized with the images [start.png](/wp-content/uploads/2011/12/start.png) and [startPressed.png](/wp-content/uploads/2011/12/startPressed.png), the target &#8220;self&#8221;, and the function &#8220;startGame&#8221;. The image file specified after the method &#8220;itemFromNormalImage&#8221; is the initial image of the menu item, and the image file specified after the method &#8220;selectedImage&#8221; is the image of the menu item while it is being touched.

That&#8217;s all for now, folks! I hope you found my tutorial helpful.
