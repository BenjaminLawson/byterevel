---
id: 4611
title: 'Python Basics 101 &#8211; Part IV: Defining Functions'
date: 2014-06-26T16:54:44+00:00
author: Nikhil Palanki
layout: single
guid: /?p=4611
permalink: /2014/06/26/python-basics-101-part-iv-defining-functions/
image: /wp-content/uploads/2014/06/693947_python-logo_png26f0333ad80ad765dabb1115dde48966.png
categories:
  - Programming
  - Python
  - Tutorials
tags:
  - defining functions in python
  - functions in python
  - ipython notebook
  - python
  - python basics
---
Functions in Python can be easily defined and called upon throughout a directory of files as well as a single file itself. This tutorial will briefly demonstrate how Python functions work as well as defining a Python function.

The advantage of defining functions is that a script or application could be dealing with several instances of pretty much the same purpose. When you define a function, you can call it multiple times, thus eliminating the need for coding what the function does every time. Python has some pretty cool functions within its various imports which we will also look at.

**Setting Up the Application**

Go ahead and launch iPython Notebook. If you need a review of how the notebook works, feel free to check out [here](/2014/06/25/python-basics-101-part-iii-how-to-create-a-python-script-in-ipython-notebook/). Next, rename the program &#8220;Functions.&#8221;

<div id="attachment_4612" style="max-width: 830px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM.png"><img class="size-large wp-image-4612" src="/wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-1024x159.png" alt="Ready to Go" width="820" height="127" srcset="/wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-1024x159.png 1024w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-300x46.png 300w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-180x27.png 180w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-360x55.png 360w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-790x122.png 790w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-1095x170.png 1095w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM-900x139.png 900w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-9.38.31-AM.png 1204w" sizes="(max-width: 820px) 100vw, 820px" /></a>
  
  <p class="wp-caption-text">
    Ready to Go
  </p>
</div>

**Writing the Code**

Next, we&#8217;re going to type in some code. I&#8217;ll explain what each element is responsible for later.

<div id="attachment_4617" style="max-width: 830px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM.png"><img class="size-large wp-image-4617" src="/wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-1024x220.png" alt="A simple function" width="820" height="176" srcset="/wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-1024x220.png 1024w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-300x64.png 300w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-180x38.png 180w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-360x77.png 360w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-790x170.png 790w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-1095x235.png 1095w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM-900x193.png 900w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-26-at-5.35.38-PM.png 1171w" sizes="(max-width: 820px) 100vw, 820px" /></a>
  
  <p class="wp-caption-text">
    A simple function
  </p>
</div>

Now there are several other functions at play that we should address first. The function that we defined is called **function1**. The general organization of a function is:

<table>
  <tr>
    <td>
      def function(variable):</p> 
      
      <p>
        #what variable does</td> </tr> </tbody> </table> 
        
        <p>
          In our above example, the user inputs two types of information: a number and a word. The <strong>raw_input()</strong> function is one way of getting the user to input information. Because our function is a function of 2 data types, we include a comma in between each component of the argument (the argument, for definition&#8217;s sake, is what is in between the parentheses next to a function).
        </p>
        
        <p>
          Next, we want our function to do something. Our above function uses some external functions in part of its defintion. First we take use <strong>len()</strong>. What <strong>len()</strong> does is it takes the length of a string inputted and outputs its integer length. The next function is <strong>int().</strong> The <strong>raw_input()</strong> function stores data as <em>strings</em> which cannot be added together (as they are not numbers &#8211; while they could be numbers, the computer doesn&#8217;t recognize them as numbers but rather as words or strings of letters). The function <strong>int() </strong>converts the variable within the argument to integer form (only if the argument is a number &#8211; you can&#8217;t convert a word to an integer).
        </p>
        
        <p>
          The final part of our function adds the two numbers together. Then, it invokes <strong>print</strong> and returns the sum of x and y. But, this isn&#8217;t the end. We need to call our function. Defining the function only defines it; it doesn&#8217;t implement it. Thus, we use function1(word, number) to call the function on the various pieces of data inputted by the user.
        </p>
        
        <p>
          And there we go! Functions in Python!
        </p>
