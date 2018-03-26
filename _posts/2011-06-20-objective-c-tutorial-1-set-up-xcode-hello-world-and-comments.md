---
id: 1314
title: 'Objective-C Tutorial 1 &#8211; Set Up Xcode, Output Hello World!, And Make Comments'
date: 2011-06-20T13:16:15+00:00
author: Ipodnerd
layout: single
guid: /?p=1314
permalink: /2011/06/20/objective-c-tutorial-1-set-up-xcode-hello-world-and-comments/
onswipe_thumb:
  - /wp-content/uploads/2011/06/objc.png
image: /wp-content/uploads/2011/06/objc.png
categories:
  - Objective-C
tags:
  - comments
  - hello world
  - ios
  - language
  - mac
  - macintosh
  - obj-c
  - object-oriented
  - objective-c
  - programming
  - tutorial 1
  - xcode
---
<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/06/objc.png"><img class="aligncenter size-full wp-image-1340" title="objc" src="/wp-content/uploads/2011/06/objc.png" alt="" width="303" height="297" srcset="/wp-content/uploads/2011/06/objc.png 303w, /wp-content/uploads/2011/06/objc-300x294.png 300w, /wp-content/uploads/2011/06/objc-30x30.png 30w, /wp-content/uploads/2011/06/objc-45x45.png 45w, /wp-content/uploads/2011/06/objc-180x176.png 180w" sizes="(max-width: 303px) 100vw, 303px" /></a>
</p>

Objective-C is an object-oriented programming language that builds upon the C programming language. The language is most commonly used on Apple&#8217;s Macintosh operating system and Apple&#8217;s mobile operating system, iOS.

Before we start programming in Objective-C, we will want to set up our IDE. Xcode is the best IDE for Objective-C out there, so we&#8217;re going to go with that. In general, it&#8217;s best to always use the latest version of a piece of software. The latest version of Xcode (Xcode 4 as of the writing of this post) can be found in the Mac App Store ( <a title="http://itunes.apple.com/app/xcode/id422352214" href="http://itunes.apple.com/app/xcode/id422352214" target="_blank">link</a>), and Apple charges USD $4.99 for it. If you aren&#8217;t able to shell out the cash, or if you are running a version of Mac OS younger than 10.6, you can sign up for a developer account at <a title="http://developer.apple.com/programs/register/" href="http://developer.apple.com/programs/register/" target="_blank">http://developer.apple.com/programs/register/</a> and then find an earlier version of Xcode at [http://connect.apple.com](http://connect.apple.com/) (in the &#8220;Developer Tools&#8221; section).

Once you have downloaded Xcode, open it (if you downloaded it to the default location, it can be found in the root folder -> Developer -> Applications -> Xcode). Hit the &#8220;Create a new Xcode project&#8221; button. In the Mac OS X section of the sidebar, select &#8220;Application&#8221;. After that, choose &#8220;Command Line Tool&#8221; and, in the &#8220;Type&#8221; drop-down menu, choose &#8220;Foundation&#8221; (yes, Foundation as in the _Foundation_ Series by Isaac Asimov =P ). Next, click the &#8220;Choose&#8230;&#8221; button and give your project a name. Save it, and your project window will open.

The Hello World program is the default code of a new project. It can be found in the main file (_projectname_.m). The code is as follows:

<table style="width: 90%;" border="0" align="center">
  <tr>
    <td>
      <pre> <span style="font-size: small;">#import </span></pre>
      
      <pre><span style="font-size: small;">int main (int argc, const char * argv[]) {</span></pre>
      
      <pre><span style="font-size: small;">NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</span></pre>
      
      <pre><span style="font-size: small;">NSLog(@"Hello, World!");</span></pre>
      
      <pre><span style="font-size: small;">[pool drain];</span></pre>
      
      <pre><span style="font-size: small;">return 0;</span></pre>
      
      <pre><span style="font-size: small;">}</span></pre>
    </td>
  </tr>
</table>

It would seem obvious that to run the program, you should click the &#8220;Build and Run&#8221; button. While this WILL run the program, you won&#8217;t actually be able to see any output! What you are going to want to do is go to (in the menu bar) Run -> Console. This will bring up the console window that will show you program output and will allow for input as well. Hit &#8220;Build and Run&#8221; and watch &#8220;Hello World!&#8221; be outputted to the console!

Now, let&#8217;s go through the program line by line and I will explain what you should know about this program.

**<span style="font-size: medium;">#import </span>**

<span style="font-size: small;">This imports a header file that allows the computer to access the functionality of the Foundation framework. To simplify what I just said&#8230;. er&#8230; typed, there is a file with a bunch of code in it that you don&#8217;t want to have to type and this imports all of that code into the program. However, this functionality isn&#8217;t used in this program (and will run fine without it).</span>

**<span style="font-size: medium;">int main (int argc, const char * argv[]) {</span>**

<span style="font-size: small;">This declares the main function, and is known as a &#8220;function header&#8221;. The main function is the starting point for all programs in Objective-C. It is what is run by the computer when the entire program itself is run. Functions in general are chunks of code that contain instructions for the computer. They can be called upon at any time from any other function. For now, don&#8217;t worry about the code in the parentheses. Lastly, the &#8220;{&#8221; (left curly brace) begins the body of the main function.</span>

**<span style="font-size: medium;">NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</span>**

<span style="font-size: small;">This line borrows some memory from your computer so that your program can run.</span>

**<span style="font-size: medium;">NSLog(@&#8221;Hello, World!&#8221;);</span>**

<span style="font-size: small;">NSLog is used to display/output text on the screen. Anything in the quotation marks is the text that gets outputted.</span>

**<span style="font-size: medium;">[pool drain];</span>**

<span style="font-size: small;">This line releases, or &#8220;drains&#8221;, the memory that we borrowed earlier in the <em>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</em> line.</span>

**<span style="font-size: medium;">return 0;</span>**

<span style="font-size: small;">This line returns the value &#8220;0&#8221; to the computer. Every function, except for the void function, returns a value. This value is described by the data type declared in the function header. In this case, the data type is an int, or integer. Returning the value of &#8220;0&#8221; indicates that the program ran successfully.</span>

<span style="font-size: medium;"><strong>}</strong></span>

<span style="font-size: small;">The right curly brace is simply the end of the body function.</span>

<p style="text-align: center;">
  <span style="font-size: x-large;"><strong>Comments</strong></span>
</p>

<span style="font-size: small;">A comment is a section of text that isn&#8217;t run in a program. A single line comment is indicated by two forward slashes (//). All text after that on the same line won&#8217;t be run by the computer when it comes to it. Comments can be used to describe parts of your program, or to turn parts of your program off.</span>

<span style="font-size: small;">In addition to a single line comment, there are multi-line comments. Multi-line comments are comments that cover more than when line. They are started with a &#8220;/*&#8221; and ended with a &#8220;*/&#8221;.</span>

<span style="font-size: small;">Here&#8217;s an example of comments in use:</span>

<table style="width: 90%;" border="0" align="center">
  <tr>
    <td>
      <pre><span style="font-size: small;"> #import </span></pre>
      
      <pre><span style="font-size: small;">int main (int argc, const char * argv[]) {</span></pre>
      
      <pre><span style="font-size: small;">NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</span></pre>
      
      <pre><span style="font-size: small;">// this is a single line commment!</span></pre>
      
      <pre><span style="font-size: small;">/*</span></pre>
      
      <pre><span style="font-size: small;">this is a</span></pre>
      
      <pre><span style="font-size: small;">multi-line</span></pre>
      
      <pre><span style="font-size: small;">comment!</span></pre>
      
      <pre><span style="font-size: small;">*/</span></pre>
      
      <pre><span style="font-size: small;">[pool drain];</span></pre>
      
      <pre><span style="font-size: small;">return 0;</span></pre>
      
      <pre><span style="font-size: small;">}</span></pre>
    </td>
  </tr>
</table>

<span style="font-size: small;">That&#8217;s all for now folks, I hope that you found this tutorial helpful! I encourage you to play around with the code by changing the text outputted with NSLog and by testing out comments.</span>

EDIT: Objective-C tutorial 2 is now up at:[ /2011/07/10/objective-c-tutorial-2-variables-and-data-types/](/2011/07/10/objective-c-tutorial-2-variables-and-data-types/ "/2011/07/10/objective-c-tutorial-2-variables-and-data-types/") .
