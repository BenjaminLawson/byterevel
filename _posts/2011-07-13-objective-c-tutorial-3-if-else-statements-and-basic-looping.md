---
id: 1904
title: 'Objective-C Tutorial 3 &#8211; If Else Statements And Basic Looping'
date: 2011-07-13T21:24:27+00:00
author: Ipodnerd
layout: single
guid: /?p=1904
permalink: /2011/07/13/objective-c-tutorial-3-if-else-statements-and-basic-looping/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/06/objc.png
categories:
  - Objective-C
tags:
  - "3"
  - do
  - else
  - for
  - if
  - looping
  - loops
  - objective-c
  - operator
  - tutorial
  - while
---
[<img class="aligncenter size-full wp-image-1340" title="objective-c" src="/wp-content/uploads/2011/06/objc.png" alt="" width="303" height="297" srcset="/wp-content/uploads/2011/06/objc.png 303w, /wp-content/uploads/2011/06/objc-300x294.png 300w, /wp-content/uploads/2011/06/objc-30x30.png 30w, /wp-content/uploads/2011/06/objc-45x45.png 45w, /wp-content/uploads/2011/06/objc-180x176.png 180w" sizes="(max-width: 303px) 100vw, 303px" />](/wp-content/uploads/2011/06/objc.png)

And it&#8217;s time for a shiny, new Objective-C tutorial! In our last tutorial, [we covered variables and data types](/2011/07/10/objective-c-tutorial-2-variables-and-data-types/ "Objective-C Tutorial 2 – Variables And Data Types"). In this tutorial, we will be covering the famous if else statements as well as loops. Enjoy!

<h1 style="text-align: center;">
  The if-else Statement
</h1>

So what exactly is an if else statement? It is a statement that allows the computer to test a condition and execute a chunk of code if it is true, or execute a different chunk of code if it is false. Here&#8217;s a picture that might help you grasp the concept:

[<img class="aligncenter size-full wp-image-1905" title="ifelse" src="/wp-content/uploads/2011/07/ifelse.png" alt="" width="300" height="358" srcset="/wp-content/uploads/2011/07/ifelse.png 300w, /wp-content/uploads/2011/07/ifelse-251x300.png 251w, /wp-content/uploads/2011/07/ifelse-180x214.png 180w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/2011/07/ifelse.png)

Now if we translate that diagram into objective-c, we get:

<table border="0" align="center">
  <tr>
    <td>
      <pre>if (condition) {</pre>
      
      <pre>//true commands</pre>
      
      <pre>}</pre>
      
      <pre>else {</pre>
      
      <pre>//false commands</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

Now that code won&#8217;t run on it&#8217;s own, so let&#8217;s add some structure and content:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int x = 2;</pre>
      
      <pre>if (x &lt; 5) {</pre>
      
      <pre>NSLog(@"X is less than 5");</pre>
      
      <pre>}</pre>
      
      <pre>    else {</pre>
      
      <pre>NSLog(@"X is equal to or greater than 5");</pre>
      
      <pre>}</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

This program will output &#8220;X is less than 5&#8221; because, well, X is less than 5.

Let&#8217;s now go through the if else statement in our program.

<span style="font-size: large;"><strong>if (x < 5) {</strong></span>

The &#8220;if&#8221; statement begins the if else statement. In it, declare it an if statement and give a condition. The condition is given in the parenthesis and is, in this case, &#8220;x<5&#8221;. If x is less than 5, then the code inside the curly brackets of the if statement will be run.

<span style="font-size: large;"><strong>NSLog(@&#8221;X is less than 5&#8243;);</strong></span>

This is the code that will be run if the condition that is declared in the if statement is true.

<span style="font-size: large;"><strong>else {</strong></span>

The &#8220;else&#8221; statement ends the if else statement. We simply declare it by typing &#8220;else&#8221; and start the body of it with a curly bracket. The code that is in the curly brackets of the else statement is what will be run if the condition declared in the parenthesis of the if statement is false.

**<span style="font-size: large;">NSLog(@&#8221;X is equal to or greater than 5&#8243;);</span>**

This is the code that will be run if the condition that is declared in the if statement is false.

If we change the value of x from 2 to 7, then the code inside the else statement will be run because the condition x < 5 will be false. That is:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int x = 7;</pre>
      
      <pre>if (x&lt;5) {</pre>
      
      <pre>NSLog(@"X is less than 5");</pre>
      
      <pre>}</pre>
      
      <pre>    else {</pre>
      
      <pre>NSLog(@"X is equal to or greater than 5");</pre>
      
      <pre>}</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

This program will output &#8220;X is equal to or greater than 5&#8243; because the value of x, 7, is greater than 5. That makes the condition &#8221; x < 5&#8243; false.

<h1 style="text-align: center;">
  The While Loop
</h1>

Okay, now that we have gone over the basic if else statement, let&#8217;s get to some loops! A loop is a block of code that is repeated until or while a particular condition is satisfied. First, let&#8217;s go over the while loop.

A while loop is a loop that runs a block of code over and over until a specified condition is true. Here&#8217;s another image that may help you grasp the concept:

[<img class="aligncenter size-full wp-image-1917" title="while loop" src="/wp-content/uploads/2011/07/while-loop.png" alt="" width="300" height="287" srcset="/wp-content/uploads/2011/07/while-loop.png 300w, /wp-content/uploads/2011/07/while-loop-30x30.png 30w, /wp-content/uploads/2011/07/while-loop-180x172.png 180w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/2011/07/while-loop.png)

The computer checks to see if a condition is true. If it is, then a block of code in the while loop is run. If it isn&#8217;t, then the code isn&#8217;t run. Every time the block of code runs, the same process occurs.

Any questions should clear up after we go over this next bit of code:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int x = 20;</pre>
      
      <pre>while (x &gt;= 10) {</pre>
      
      <pre>NSLog(@"%i", x);</pre>
      
      <pre>x = x - 1;</pre>
      
      <pre>}</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

This program will output &#8220;20 19 18 17 16 15 14 13 12 11 10&#8221; (each number on a new line). As usual, we&#8217;re going to go through the new code that you haven&#8217;t seen before (if you don&#8217;t understand a line that I leave unmentioned, look at previous tutorials).

<span style="font-size: large;"><strong>while (x >= 10) {</strong></span>

This line starts the while loop by declaring the loop &#8220;while&#8221; and giving a condition. In this case, the condition is &#8220;x is less than or equal to 10&#8221; . As long as the value of x is less than or equal to the value of 10, the code inside the curly brackets will be run. It is important to make sure that the code inside the curly brackets changes the value of a variable in the condition so that the code doesn&#8217;t run infinitely.

<span style="font-size: large;"><strong>x = x &#8211; 1;</strong></span>

All we&#8217;re doing here is setting x equal to be one less than the current value. This can also be written as:

<table border="0" align="center">
  <tr>
    <td>
      <pre>x--;</pre>
    </td>
  </tr>
</table>

The reason we are setting the value of x to be one less is so that the while loop doesn&#8217;t run infinitely. Eventually, x is no longer greater than or equal to 10.

<h1 style="text-align: center;">
  The For Loop
</h1>

The next loop we are going to go over is the &#8220;for&#8221; loop. This is the most complicated, so pay close attention! A for loop is useful if you want to run some lines of code a certain number of times.

[<img class="aligncenter size-full wp-image-1928" title="for loop" src="/wp-content/uploads/2011/07/for-loop.png" alt="" width="300" height="431" srcset="/wp-content/uploads/2011/07/for-loop.png 300w, /wp-content/uploads/2011/07/for-loop-208x300.png 208w, /wp-content/uploads/2011/07/for-loop-180x258.png 180w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/2011/07/for-loop.png)

As usual, here&#8217;s some code with a for loop that we will go over:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int y;</pre>
      
      <pre>for (y = 0; y &lt;= 20; y = y + 1) {</pre>
      
      <pre>NSLog(@"%i", y);</pre>
      
      <pre>}</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

This program will output the numbers 1 through 20 to the console window.

<span class="Apple-style-span" style="font-size: large;"><strong>for (y = 0; y <= 20; y = y + 1) {</strong></span>

The for loop is declared with &#8220;for&#8221; (I bet you didn&#8217;t see that coming!) and  is followed by three expressions in parenthesis. The first expression (in this case &#8220;y=0;&#8221;)  sets a variable equal to something as a starting point. Notice how we declared the variable &#8220;y&#8221; before the for loop. Instead of doing that we can declare the variable and set its value right inside this expression. (like this: &#8221; for (int y = 0; y<=20; y = y + 1&#8243;)&#8221; ). Now, as I mentioned previously, this is only a starting point. The second expression sets a limit on the value of the variable. In the case of this program, out limit is &#8221; y <= 20&#8243;. That is, as long as y is less than or equal to 20, the code inside the loop will run. It would seem that the code inside the loop would then run forever, but this is where the third expression kicks in. The third expression manipulates the value of the variable in some way so that the limit set in expression 2 is eventually reached. The most common things to do with the value is either increase it by one (which is what the third expression in this program does) or decrease it by one. Similarly to how &#8220;x = x &#8211; 1&#8221; is the same thing as &#8220;x&#8211;;&#8221; (as mentioned in the explanation of the while loop), &#8220;y = y + 1&#8221; can be re-written as &#8220;y++&#8221;.

To summarize, the first expression sets the value of the variable, the second sets a limit on the value of the variable, and the third changes the value of the variable so that it eventually reaches the limit.

<span style="font-size: large;"><strong>NSLog(@&#8221;%i&#8221;, y);</strong></span>

You&#8217;ve seen this before, but I want to point a couple of things out. The first being that this is the code in our for loop that is run a certain number of times (in this case, 20). The second is that this is a useful way of increasing the value of a variable by a certain amount each time a chunk of code is run. You can use the same variable in your loop as the one used in the expressions.

<p style="text-align: center;">
  <span style="font-size: large;"><strong>The Do While Loop</strong></span>
</p>

<p style="text-align: left;">
  The last loop that I want to go over in this tutorial is the do while loop. The do while loop is very similar to the while loop but with one major difference. That difference is that the code inside the loop is run once before the condition is tested. If you don&#8217;t understand what I&#8217;m saying look at the following image:
</p>

<p style="text-align: left;">
  <a href="/wp-content/uploads/2011/07/do-while.jpeg"><img class="aligncenter size-full wp-image-1932" title="do while" src="/wp-content/uploads/2011/07/do-while.jpeg" alt="" width="201" height="282" srcset="/wp-content/uploads/2011/07/do-while.jpeg 201w, /wp-content/uploads/2011/07/do-while-180x252.jpeg 180w" sizes="(max-width: 201px) 100vw, 201px" /></a>Now compare that to the diagram of the while loop, and you should see the difference. Now, let&#8217;s study some more code:
</p>

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int z = 10;</pre>
      
      <pre>do {</pre>
      
      <pre>NSLog(@"%i", z);</pre>
      
      <pre>z = z - 1;</pre>
      
      <pre>} while (z &gt;= 0);</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

<span style="font-size: large;"><strong>do {</strong></span>

That&#8217;s all there is to declaring a do while loop. The &#8220;do&#8221; declares the do part of the do while loop and the opening curly bracket opens/starts the loop.

<span style="font-size: large;"><strong>z = z &#8211; 1;</strong></span>

I know that this is probably getting annoying, but I want to mention this one last time. This line can also be written &#8220;z- -;&#8221;

<span style="font-size: large;"><strong>} while (z >= 0);</strong></span>

The closing curly bracket closes/ends the loop body. Now this is where the while part of the do while loop comes in. After the &#8220;do&#8221; code is run, the while condition is checked and, if it is true, the &#8220;do&#8221; code will be run again. If it is false, than the program will continue and the &#8220;do&#8221; code won&#8217;t be run again. Take note that there is a semicolon after the condition (expression in parenthesis).

<h1 style="text-align: center;">
  Some more information regarding operators&#8230;
</h1>

Now that we&#8217;ve covered most of the loops, I would like to provide a little more information regarding conditions. You probably gathered most of the information you need to know from the above code, but I&#8217;m going to clarify anyway. There are 6 different comparison operators that you can use to compare two values/ variables, and here they are:

<table border="0" align="center">
  <tr>
    <td style="text-align: center;">
      <strong>Operator</strong>
    </td>
    
    <td style="text-align: center;">
      <strong>In words</strong>
    </td>
    
    <td style="text-align: center;">
      <strong>Example</strong>
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      <
    </td>
    
    <td style="text-align: center;">
      Is less than
    </td>
    
    <td style="text-align: center;">
      X < 5
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      >
    </td>
    
    <td style="text-align: center;">
      Is greater than
    </td>
    
    <td style="text-align: center;">
      X > 5
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      ==
    </td>
    
    <td style="text-align: center;">
      Is equal to
    </td>
    
    <td style="text-align: center;">
      X == 5
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      !=
    </td>
    
    <td style="text-align: center;">
      Is not equal to
    </td>
    
    <td style="text-align: center;">
      X != 5
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      <=
    </td>
    
    <td style="text-align: center;">
      Is less than or equal to
    </td>
    
    <td style="text-align: center;">
      X <= 5
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      >=
    </td>
    
    <td style="text-align: center;">
      Is greater than or equal to
    </td>
    
    <td style="text-align: center;">
      X >= 5
    </td>
  </tr>
</table>

Now say you want to have multiple conditions that have to be met in order for a chunk of code in a loop or an if else statement to be run. Well, you can insert &#8220;&&&#8221;  between the conditions in the parenthesis and all of them will be checked. This is referred to as the AND operator. Here&#8217;s an example:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int n = 10;</pre>
      
      <pre>if (n &gt; 0 && n &lt; 20) {</pre>
      
      <pre>NSLog(@"n is between 0 and 20!");</pre>
      
      <pre>}</pre>
      
      <pre>else {</pre>
      
      <pre>NSLog(@"n is not betwen 0 and 20");</pre>
      
      <pre>}</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

See if you can figure out what will be output by looking at the code.

Okay, now say that you have multiple conditions and you want at least one of them to be true. You would want to use the OR operator. It is typed like this: &#8220;||&#8221;. Like the AND operator, the OR operator is is placed between the expressions like so:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>int n = 15;</pre>
      
      <pre>if (n == 10 || n == 20) {</pre>
      
      <pre>NSLog(@"n is equal to either 10 or 20");</pre>
      
      <pre>}</pre>
      
      <pre>else {</pre>
      
      <pre>NSLog(@"n is not equal to 10 or 20");</pre>
      
      <pre>}</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

Like the previous code, I suggest you test yourself and se if you can figure out what the output will be.

Well, that&#8217;s all for now. See you next tutorial!

&nbsp;
