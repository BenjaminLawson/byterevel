---
id: 1860
title: 'Objective-C Tutorial 2 &#8211; Variables And Data Types'
date: 2011-07-10T21:14:13+00:00
author: Ipodnerd
layout: single
guid: /?p=1860
permalink: /2011/07/10/objective-c-tutorial-2-variables-and-data-types/
image: /wp-content/uploads/2011/06/objc.png
categories:
  - Objective-C
tags:
  - "2"
  - data types
  - objective-c
  - tutorial
  - variables
---
&nbsp;

&nbsp;

[<img class="aligncenter size-full wp-image-1340" title="objective-c" src="/wp-content/uploads/2011/06/objc.png" alt="" width="303" height="297" srcset="/wp-content/uploads/2011/06/objc.png 303w, /wp-content/uploads/2011/06/objc-300x294.png 300w, /wp-content/uploads/2011/06/objc-30x30.png 30w, /wp-content/uploads/2011/06/objc-45x45.png 45w, /wp-content/uploads/2011/06/objc-180x176.png 180w" sizes="(max-width: 303px) 100vw, 303px" />](/wp-content/uploads/2011/06/objc.png)

In our [last Objective-C tutorial](/2011/06/20/objective-c-tutorial-1-set-up-xcode-hello-world-and-comments/ "Objective-C Tutorial 1 – Set Up Xcode, Output Hello World!, And Make Comments"), we covered setting up Xcode, running the Hello World program, and making comments. In this tutorial, we are going to go over variables.

If you went through any basic algebra course, then you probably know what a mathematical variable is. As a quick reminder, a variable is a letter or symbol that represents a  value (or values). The value of a variable can change given different equations. In programming, variables are names that are placeholders for a data value. For example, a variable named &#8220;x&#8221; could represent 5.

There are many different types of variables for different kinds of data values. For example, integer variables can only represent numbers that are integers (integers are pretty much whole numbers like -1, 0, and 1). Floats, or floating point numbers, are variables that represent numbers that can have decimal places (up to 7 digits total). A double is a variable type like a float, but it  can hold a much larger amount of digits. When displaying a double in the console window, scientific notation is used for numbers with more than 6 decimal places. Now I know that this paragraph is somewhat confusing and difficult to reference, so here is a comprehensive chart of data values that you can look over now, and back at in the future.

<table border="0" align="center">
  <tr>
    <td>
      <strong>Date Type</strong>
    </td>
    
    <td>
      <strong>Description</strong>
    </td>
    
    <td>
      <strong>Example(s)</strong>
    </td>
  </tr>
  
  <tr>
    <td>
      int
    </td>
    
    <td>
      variables that are integers can store whole numbers
    </td>
    
    <td>
      -1, 0, 1
    </td>
  </tr>
  
  <tr>
    <td>
      float
    </td>
    
    <td>
      variables that are floats can store numbers with (a limited) number of decimals
    </td>
    
    <td>
       3.14, 5.68, 2.333
    </td>
  </tr>
  
  <tr>
    <td>
      double
    </td>
    
    <td>
      variables that are doubles can store a very large amount of decimals and are displayed in scientific notation
    </td>
    
    <td>
       <span class="Apple-style-span" style="font-family: Consolas, Monaco, monospace; line-height: 18px; white-space: pre;">3.141592653589793238462643383279502884197169399375105820974944</span>
    </td>
  </tr>
  
  <tr>
    <td>
       char
    </td>
    
    <td>
       variables that are characters can store a letter
    </td>
    
    <td>
       a, b, c
    </td>
  </tr>
  
  <tr>
    <td>
      bool
    </td>
    
    <td>
      a variable that is either true or false; boolean values are integers; any number that is not 0 is true, 0 is false
    </td>
    
    <td>
      true, false, 0, 1, 2
    </td>
  </tr>
  
  <tr>
    <td>
      id
    </td>
    
    <td>
      id variables can store any type of data as well as entire objects
    </td>
    
    <td>
       &#8220;hello&#8221;, 1, pool
    </td>
  </tr>
</table>

&nbsp;

Don&#8217;t worry if you don&#8217;t understand some of these data types, we will be going over the use of integers right now, and the others we will cover in the future.

It&#8217;s time do dive right in to the code. In this program, we will declare a variable &#8220;x&#8221; and set it equal to 3. Then, we will output the value of x using NSLog.

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int x = 3;</pre>
      
      <pre>NSLog(@"The value of x is %i", x);</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

If you run the program (see [tutorial 1](/2011/06/20/objective-c-tutorial-1-set-up-xcode-hello-world-and-comments/ "Objective-C Tutorial 1 – Set Up Xcode, Output Hello World!, And Make Comments")), you will find that it outputs &#8220;The value of x is 3&#8221;. Pretty darn amazing, eh? Now lets break it down and go through the lines of code that you haven&#8217;t sen before.

<span style="font-size: large;"><strong>int x = 3;</strong></span>

This sets the integer variable x to equal the value 3. It can also be typed as follows:

<table border="0" align="center">
  <tr>
    <td>
      <pre>int x;</pre>
      
      <pre>x = 3;</pre>
    </td>
  </tr>
</table>

&nbsp;

<span style="font-size: large;"><strong>NSLog(@&#8221;The value of x is %i&#8221;, x);</strong></span>

This NSLog statement outputs &#8220;The value of x is 3&#8221;. In order to output the value of an integer variable (in this case, x) in the NSLog statement, you must place %i in the part of the output (text in parenthesis) where you want the variable to be output. Then, you must follow the output statement in quotes by a comma and the name of the variable that you want the %i to represent (in this case, it was x).

Now, let&#8217;s look at some situations that you might run into while using variables. Say you want to output the values of two variables in the same NSLog statement. The code would be as follows:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int x = 3;</pre>
      
      <pre>int y = 12;</pre>
      
      <pre>NSLog(@"The value of x is %i, and the value of y is %i", x, y);</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

This will output &#8220;The value of x is 3, and the value of y is 12&#8221;.

<span style="font-size: large;"><strong>NSLog(@&#8221;The value of x is %i, and the value of y is %i&#8221;, x, y);</strong></span>

The two %i&#8217;s correspond to the variables that are in the same place in order in the list of variables after the quotation.

Another interesting thing you can do with variables is set a variable to equal an equation that can include other variables. The following code demonstrates this:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int x = 3;</pre>
      
      <pre>int y = 12;</pre>
      
      <pre>int z = x + y;</pre>
      
      <pre>NSLog(@"The sum of x and y is %i", z);</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

This outputs &#8220;The sum of x and y is 15&#8221;. The line &#8220;int z = x + y;&#8221; sets integer variable z to equal the sum of the values of x and y.

The last thing I want to demonstrate is the use of a different data type. Let&#8217;s use a float.

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>float x = 3.1415;</pre>
      
      <pre>NSLog(@"The value of x is %f", x);</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

<span class="Apple-style-span" style="line-height: normal; font-size: small;">This outputs &#8220;The value of x is 3.141500&#8221;. Note how all 6 decimals are displayed, even if you didn&#8217;t have that many. Also note that we used %f in our NSLog statement to output a float. For doubles, we use %e. We will discuss the use of other variables in NSLog in future tutorials.</span>

<span style="font-size: small;">I hope that you found this tutorial helpful! Please feel free to leave comments asking questions regarding this tutorial.</span>

&nbsp;
