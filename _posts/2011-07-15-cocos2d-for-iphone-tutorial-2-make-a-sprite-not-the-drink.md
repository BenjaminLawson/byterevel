---
id: 1964
title: 'Cocos2D For iPhone Tutorial 2 &#8211;  Make A Sprite (Not The Drink!)'
date: 2011-07-15T22:34:35+00:00
author: Ipodnerd
layout: single
guid: /?p=1964
permalink: /2011/07/15/cocos2d-for-iphone-tutorial-2-make-a-sprite-not-the-drink/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/07/cocos2d-icon-on-screen.png
categories:
  - Cocos2D
tags:
  - cocos2d
  - icon
  - ios
  - iphone
  - ipod touch
  - sorite
  - sprites
  - tutorial
---
<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/07/cocos2d-logo.png"><img class="aligncenter size-full wp-image-1965" title="cocos2d logo" src="/wp-content/uploads/2011/07/cocos2d-logo.png" alt="" width="160" height="237" /></a>
</p>

Okay, now that you&#8217;ve <a title="Cocos2D for iPhone Tutorial I – How To Install Cocos2D for iPhone in Xcode" href="/2011/06/02/cocos2d-tutorial-i-how-to-install-cocos2d-in-xcode/" target="_blank">successfully installed Cocos2D for iPhone</a>, let&#8217;s go over making a project and displaying a sprite.

First off, we need to create a new project. This is done by opening Xcode and going to File -> New Project. Alternatively, Hit the &#8220;Create a new Xcode project&#8221; button in the welcome window. In the new project window, select &#8220;Cocos2d&#8221; from the user templates section of the sidebar. The type of application that you want to make right now is a &#8220;cocos2d Application&#8221;. Double click the corresponding icon.

In your project sidebar, expand the &#8220;Classes&#8221; folder. The file that we are going to work with in this tutorial is &#8220;HelloWorldScene.m&#8221;. Click it.

Be default, the code should be as follows:

<table border="0" align="center">
  <tr>
    <td>
      <span class="Apple-style-span" style="font-family: Consolas, Monaco, monospace; font-size: 12px; line-height: 18px; white-space: pre;">//  HelloWorldLayer.m</span></p> 
      
      <pre>// Import the interfaces</pre>
      
      <pre>#import "HelloWorldScene.h"</pre>
      
      <pre>// HelloWorld implementation</pre>
      
      <pre>@implementation HelloWorld</pre>
      
      <pre>+(id) scene</pre>
      
      <pre>{</pre>
      
      <pre>// 'scene' is an autorelease object.</pre>
      
      <pre>CCScene *scene = [CCScene node];</pre>
      
      <pre>// 'layer' is an autorelease object.</pre>
      
      <pre>HelloWorld *layer = [HelloWorld node];</pre>
      
      <pre>// add layer as a child to scene</pre>
      
      <pre>[scene addChild: layer];</pre>
      
      <pre>// return the scene</pre>
      
      <pre>return scene;</pre>
      
      <pre>}</pre>
      
      <pre>// on "init" you need to initialize your instance</pre>
      
      <pre>-(id) init</pre>
      
      <pre>{</pre>
      
      <pre>// always call "super" init</pre>
      
      <pre>// Apple recommends to re-assign "self" with the "super" return value</pre>
      
      <pre>if( (self=[super init] )) {</pre>
      
      <pre>// create and initialize a Label</pre>
      
      <pre>CCLabelTTF *label = [CCLabelTTF labelWithString:@"Hello World" fontName:@"Marker Felt" fontSize:64];</pre>
      
      <pre>// ask director the the window size</pre>
      
      <pre>CGSize size = [[CCDirector sharedDirector] winSize];</pre>
      
      <pre>// position the label on the center of the screen</pre>
      
      <pre>label.position =  ccp( size.width /2 , size.height/2 );</pre>
      
      <pre>// add the label as a child to this Layer</pre>
      
      <pre>[self addChild: label];</pre>
      
      <pre>}</pre>
      
      <pre>return self;</pre>
      
      <pre>}</pre>
      
      <pre>// on "dealloc" you need to release all your retained objects</pre>
      
      <pre>- (void) dealloc</pre>
      
      <pre>{</pre>
      
      <pre>// in case you have something to dealloc, do it in this method</pre>
      
      <pre>// in this particular example nothing needs to be released.</pre>
      
      <pre>// cocos2d will automatically release all the children (Label)</pre>
      
      <pre>// don't forget to call "super dealloc"</pre>
      
      <pre>[super dealloc];</pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
    </td>
  </tr>
</table>

To make sure Cocos2D is configured correctly, click &#8220;Build and Debug&#8221; (at the top of the window). The iOs simulator application should open, and the Cocos2D application should run. The default code will cause &#8220;Hello World&#8221; to be displayed on the screen. All is well? Good.

After getting rid of all the unnecessary parts of code in our HelloWorldScene.m file, such as comments, we can trim it down to:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import "HelloWorldScene.h"</pre>
      
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
      
      <pre>}</pre>
      
      <pre>return self;</pre>
      
      <pre>}</pre>
      
      <pre>- (void) dealloc</pre>
      
      <pre>{</pre>
      
      <pre>[super dealloc];</pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
    </td>
  </tr>
</table>

&nbsp;

Before we get to writing the code that will display a sprite, let&#8217;s make sure we know what a sprite is. The definition of a sprite is &#8220;A computer graphic that may be moved on-screen and otherwise manipulated as a single entity&#8221;. For example, in <a title="Top 10 iPhone Games – Physics Games" href="/2011/05/11/top-10-iphone-games-physics-games/" target="_blank">Angry Birds</a>, the birds that you launch with a slingshot are sprites.

Now that we&#8217;ve got that over with, let&#8217;s get back to the project. Obviously, we are going to need a sprite that we can manipulate. Luckily, there is a default Cocos2D icon in the &#8220;Resources&#8221; folder in the sidebar that we can use. If you&#8217;re really against using that, then you can import your own small png image to the Resources folder and adjust the code that we go through accordingly. For the purpose of this tutorial, though, we are going to use the default image &#8220;Icon.png&#8221;.

Let&#8217;s cut to the code (I love saying that). We&#8217;re going to start off by making an object for our sprite. We do this by making an object in the class &#8220;CCSprite&#8221;. Let&#8217;s call our object &#8220;icon&#8221; because that&#8217;s the name of the image we are using. The code for this is &#8220;CCSprite *icon;&#8221;.  &#8220;Where do I put this?&#8221; you ask. Glad you asked. We are going to put this right under the #import code. Like so:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import "HelloWorldScene.h"</pre>
      
      <pre><span style="color: #ff0000;">CCSprite *icon;</span></pre>
      
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
      
      <pre>}</pre>
      
      <pre>return self;</pre>
      
      <pre>}</pre>
      
      <pre>- (void) dealloc</pre>
      
      <pre>{</pre>
      
      <pre>[super dealloc];</pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
    </td>
  </tr>
</table>

Because we declared our object outside of the methods, all of the methods will be able to access it. While this isn&#8217;t of real importance right now, it will become necessary when our code becomes more complicated.

The next thing we need to do is connect our icon.png file to our object &#8220;icon&#8221; and tell the iOS simulator where to place the image on the screen. The section of code that we are going to work in is the &#8220;init&#8221; method (look at the above code for &#8220;-(id) init&#8221;). The init method is what is run/initialized when a scene is loaded (we&#8217;ll go over scenes in a future tutorial, but you can probably figure out what they are by their name). It&#8217;s unnecessary for me to show the code in the rest of the program, so the next bit of code will only be the init method (you will want to add this to the init method in the code above).

<table border="0" align="center">
  <tr>
    <td>
      <pre>-(id) init</pre>
      
      <pre>{</pre>
      
      <pre>if( (self=[super init] )) {</pre>
      
      <pre>icon = [CCSprite spriteWithFile:@"Icon.png"];</pre>
      
      <pre>icon.position = ccp(300,200);</pre>
      
      <pre>[self addChild:icon];</pre>
      
      <pre>}</pre>
      
      <pre>return self;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

<span style="font-size: large;"><strong>icon = [CCSprite spriteWithFile:@&#8221;Icon.png&#8221;];</strong></span>

This line of code sets the image file of the sprite. You would change the object name (in this case, &#8220;icon&#8221;) depending on the name of your object. Also, the name of the image file would change depending on what the name of the image in your Resources folder is called.

<span style="font-size: large;"><strong>icon.position = ccp(300,200);</strong></span>

You can&#8217;t just tell a computer to stick an image on the screen and expect it to go where you want it to. This code specifies the coordinates of the image. In the case of Cocos2D, the origin of the coordinate plane is the bottom left corner of the iPhone or iPod Touch screen. The coordinate itself refers to the location of the exact center of the sprite/image.

<span style="font-size: large;"><strong>[self addChild:icon];</strong></span>

This simply adds the icon sprite to the current layer. We&#8217;ll go over layers and their many uses in a future tutorial.

<h1 style="text-align: center;">
  That&#8217;s it.
</h1>

Click &#8220;Run and Debug&#8221; and watch the Cocos2D icon sit at the coordinates (300,200) on your virtual iPhone screen!

<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/07/cocos2d-icon-on-screen.png"><img class="aligncenter size-full wp-image-1973" title="cocos2d icon on screen" src="/wp-content/uploads/2011/07/cocos2d-icon-on-screen.png" alt="" width="515" height="265" srcset="/wp-content/uploads/2011/07/cocos2d-icon-on-screen.png 716w, /wp-content/uploads/2011/07/cocos2d-icon-on-screen-300x154.png 300w, /wp-content/uploads/2011/07/cocos2d-icon-on-screen-180x92.png 180w, /wp-content/uploads/2011/07/cocos2d-icon-on-screen-360x185.png 360w" sizes="(max-width: 515px) 100vw, 515px" /></a>
</p>

<p style="text-align: left;">
  For practice (and to test your understanding), I suggest you try adding multiple sprites with different images to the screen.
</p>
