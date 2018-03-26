---
id: 367
title: 'C++ Tutorial I &#8211; Hello World!'
date: 2011-05-15T15:13:11+00:00
author: Nikhil Palanki
layout: single
guid: /?p=367
permalink: /2011/05/15/c-tutorial-i-hello-world/
image: /wp-content/uploads/2011/05/C++.jpg
categories:
  - C++
  - Tutorials
tags:
  - c++
  - cplusplus
  - hello
  - programming
  - world
  - xcode
---
Many consider C++ to be cliche and a bit ancient. But nonetheless, it is great for beginners who want to start programming, but don&#8217;t know where to start. If you learn C or C++, Objective-C becomes much easier to learn. And believe us, Objective-C is not for beginner programmers.

Before you get started programming in C++, you should have a IDE. For Windows, I suggest Bloodshed <a title="http://www.bloodshed.net/devcpp.html" href="http://www.bloodshed.net/devcpp.html" target="_blank">Dev-C++</a>. For Macintosh, <a title="http://itunes.apple.com/us/app/xcode/id422352214?mt=12&ls=1" href="http://itunes.apple.com/us/app/xcode/id422352214?mt=12&ls=1" target="_blank">Xcode</a> is ideal, with <a title="http://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/heliossr2" href="http://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/heliossr2" target="_blank">Eclipse for C++</a> being another choice (Eclipse is also available for Windows and Linux).

Anyhow, take a look at the C++ code: (Bold is C++, text after &#8220;//&#8221; is a comment. That is, it isn&#8217;t run when the program is compiled.)

&nbsp;

 ****

<table border="0" align="center">
  <tr>
    <td>
      <strong>#include <iostream></strong> //imports the basic output/input library<strong>using namespace std;</strong> //without this, you woud need to type &#8220;std::&#8221; before most lines of code in your program</p> 
      
      <p>
        <strong>int main()</strong> //the main function of the program; starting point of all C++ programs
      </p>
      
      <p>
        <strong>{ </strong>//left curly bracket; it begins/opens the main function
      </p>
      
      <p>
        <strong>cout <<&#8220;Hello World!&#8221;;</strong> //cout is what you tell the program to say to the user; this outputs &#8220;Hello World!&#8221; in the console window
      </p>
      
      <p>
        <strong>system(&#8220;pause&#8221; );</strong> //This tells the program to pause the program so that the user can actually see what is output on the screen; use this if you are running the program on Windows, don&#8217;t use this on Macintosh or Linux
      </p>
      
      <p>
        <strong>cout << endl; </strong>//outputs a line break, all further output is done on the next line
      </p>
      
      <p>
        <strong>return 0;</strong> //Tells the computer that the program ran successfully
      </p>
      
      <p>
        <strong>} </strong>//right curly bracket; this ends/closes the main function</td> </tr> </tbody> </table> 
        
        <p>
          &nbsp;
        </p>
        
        <p>
          And now you know how the program works! Enjoy!
        </p>
        
        <div id="attachment_462" style="max-width: 350px" class="wp-caption aligncenter">
          <a rel="attachment wp-att-462" href="/2011/05/15/c-tutorial-i-hello-world/c/"><img class="size-full wp-image-462" src="/wp-content/uploads/2011/05/C++.jpg" alt="" width="340" height="255" srcset="/wp-content/uploads/2011/05/C++.jpg 340w, /wp-content/uploads/2011/05/C++-300x225.jpg 300w" sizes="(max-width: 340px) 100vw, 340px" /></a>
          
          <p class="wp-caption-text">
            As you can see, it says Hello World! on the paper!!!!!!!
          </p>
        </div>
