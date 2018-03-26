---
id: 2497
title: 'Objective-C Tutorial 6 &#8211; Returning The Values Of Instance Variables'
date: 2011-08-24T18:59:29+00:00
author: Ipodnerd
layout: single
guid: /?p=2497
permalink: /2011/08/24/objective-c-tutorial-6-returning-the-values-of-instance-variables/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/06/objc.png
categories:
  - Objective-C
tags:
  - accessing
  - getter
  - instance variable
  - method
  - objective-c
---
[<img class="aligncenter size-full wp-image-1340" title="objective-c" src="/wp-content/uploads/2011/06/objc.png" alt="" width="303" height="297" srcset="/wp-content/uploads/2011/06/objc.png 303w, /wp-content/uploads/2011/06/objc-300x294.png 300w, /wp-content/uploads/2011/06/objc-30x30.png 30w, /wp-content/uploads/2011/06/objc-45x45.png 45w, /wp-content/uploads/2011/06/objc-180x176.png 180w" sizes="(max-width: 303px) 100vw, 303px" />](/wp-content/uploads/2011/06/objc.png)

Hip hip, hooray! It&#8217;s time for another Objective-C tutorial. I&#8217;m going to try to keep this one short but sweet, as it is intended to add some additional information to our [last tutorial](/2011/08/20/objective-c-tutorial-5-objects/ "Objective-C Tutorial 5 – Objects"). I&#8217;ll be talking about using instance variables in our main function.

An instance variable is a variable that is defined within a class. For example, we had the class Alien in our last tutorial. The variable &#8220;NumberOfEyes&#8221; that was inside of our Alien class is an instance variable.

We can&#8217;t access instance variables directly from our main function. Instead, we need to create another method that returns the value of our instance variables (only methods can access instance variables directly). These kinds of methods are referred to as &#8220;getter&#8221; methods because they &#8220;get&#8221; the values of the instance variables.

In the program that we&#8217;ll be creating, we will replace the &#8220;output&#8221; method that we used in our last tutorial with  an NSLog statement in our main function. In order to accomplish this, we&#8217;ll need to use some getter methods that return the values of our instance variables.

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>@interface Alien : NSObject {</pre>
      
      <pre>int NumberOfEyes;</pre>
      
      <pre>int Age;</pre>
      
      <pre>int NumberOfEars;<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i;</pre>
      
      <pre>-(void) setAge: (int) a;</pre>
      
      <pre>-(void) setNumberOfEars: (int) e;</pre>
      
      <pre><span style="color: #ff0000;">-(int) NumberOfEyes;</span></pre>
      
      <pre><span style="color: #ff0000;">-(int) Age;</span></pre>
      
      <pre><span style="color: #ff0000;">-(int) NumberOfEars;</span></pre>
      
      <pre>@end<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>@implementation Alien<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>-(void) setNumberOfEyes: (int) i {</pre>
      
      <pre>NumberOfEyes = i;</pre>
      
      <pre>}<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>-(void) setAge: (int) a {</pre>
      
      <pre>Age = a;</pre>
      
      <pre>}<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>-(void) setNumberOfEars: (int) e {</pre>
      
      <pre>NumberOfEars = e;</pre>
      
      <pre>}<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre><span style="color: #ff0000;">-(int) NumberOfEyes {</span></pre>
      
      <pre><span style="color: #ff0000;">return NumberOfEyes;</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre><span style="color: #ff0000;">-(int) Age {</span></pre>
      
      <pre><span style="color: #ff0000;">return Age;</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre><span style="color: #ff0000;">-(int) NumberOfEars {</span></pre>
      
      <pre><span style="color: #ff0000;">return NumberOfEars;</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre>@end</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>Alien *Bill;</pre>
      
      <pre>Bill = [Alien alloc];</pre>
      
      <pre>Bill = [Bill init];<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>[Bill setNumberOfEyes: 8];</pre>
      
      <p>
        <span class="Apple-style-span" style="font-family: Consolas, Monaco, monospace; font-size: 12px; line-height: 18px; white-space: pre;">[Bill setAge: 344];</span>
      </p>
      
      <p>
        <span class="Apple-style-span" style="font-family: Consolas, Monaco, monospace; font-size: 12px; line-height: 18px; white-space: pre;">[Bill setNumberOfEars: 3];</span>
      </p>
      
      <pre><span style="color: #ff0000;">int NumberOfEyes = [Bill NumberOfEyes];</span></pre>
      
      <pre><span style="color: #ff0000;">int Age = [Bill Age];</span></pre>
      
      <pre><span style="color: #ff0000;">int NumberOfEars = [Bill NumberOfEars];</span></pre>
      
      <pre><span style="color: #ff0000;">NSLog(@"The alien is %i years old and has %i eyes and %i ears.", Age, NumberOfEyes, NumberOfEars);</span></pre>
      
      <pre>[Bill release];<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>[pool drain];</pre>
      
      <pre>return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

The above code will output &#8220;The alien is 344 years old and has 8 eyes and 3 ears.&#8221;

<span style="font-size: large;"><strong>-(int) NumberOfEyes;</strong></span>

<span style="font-size: large;"><strong>-(int) Age;</strong></span>

<span style="font-size: large;"><strong>-(int) NumberOfEars;</strong></span>

As you might recall from our [tutorial about classes](/2011/07/20/objective-c-tutorial-4-classes/ "Objective-C Tutorial 4 – Classes"), we need to declare our methods in the @interface section of the class. All of the methods that we have created prior to this tutorial didn&#8217;t need to return anything. Because of this, we put &#8220;void&#8221; in the parentheses. Now, we want our methods to return the values of our instance variables. All of our instance variables are integers, so we will want to return integers. Similar to how we use &#8220;int&#8221; to declare an integer variable, we will use &#8220;int&#8221; to tell the computer that we are going to be returning an integer.

<span style="font-size: large;"><strong>-(int) NumberOfEyes {</strong></span>

<span style="font-size: large;"><strong>return NumberOfEyes;</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

<span style="font-size: large;"><strong>-(int) Age {</strong></span>

<span style="font-size: large;"><strong>return Age;</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

<span style="font-size: large;"><strong>-(int) NumberOfEars {</strong></span>

<span style="font-size: large;"><strong>return NumberOfEars;</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

Now that we&#8217;ve declared our methods in the @interface, we need to give our methods some code to run. First, copy the method declaration (minus the semicolon) and paste it in the implementation. Then, open the body of the method with an opening curly bracket. The code that we want inside of our methods is &#8220;return instancevariable&#8221; (replacing &#8220;instancevariable&#8221; with the corresponding name of the instance variable that we want the value of). This &#8220;return&#8221; statement is how we return values in our methods. In our NumberOfEyes method, the value of the instance variable &#8220;NumberOfEyes&#8221; is returned. When writing code in the main function, we will be able to call this method and, once the &#8220;return&#8221; statement is run, we will receive the value of &#8220;NumberOfEyes&#8221;.

<span style="font-size: large;"><strong>int NumberOfEyes = [Bill NumberOfEyes];</strong></span>

<span style="font-size: large;"><strong>int Age = [Bill Age];</strong></span>

<span style="font-size: large;"><strong>int NumberOfEars = [Bill NumberOfEars];</strong></span>

You&#8217;ve declared variables before. Nothing new there. But wait, what&#8217;s this crazy looking [Bill NumberOfEyes] ? We&#8217;re just [calling the method](/2011/08/20/objective-c-tutorial-5-objects/ "Objective-C Tutorial 5 – Objects") &#8220;NumberOfEyes&#8221;. That&#8217;s right, we can set a variable equal to the returned value of a method.

<span style="font-size: large;"><strong>NSLog(@&#8221;The alien is %i years old and has %i eyes and %i ears.&#8221;, Age, NumberOfEyes, NumberOfEars);</strong></span>

Nothing new here either, we&#8217;re just [plugging some variables into an NSLog statement](/2011/07/10/objective-c-tutorial-2-variables-and-data-types/ "Objective-C Tutorial 2 – Variables And Data Types").

<h1 style="text-align: center;">
  A Shortcut
</h1>

Instead of setting variables equal to the returned value of a method, we can just call the methods from inside the NSLog statement.

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>@interface Alien : NSObject {</pre>
      
      <pre>int NumberOfEyes;</pre>
      
      <pre>int Age;</pre>
      
      <pre>int NumberOfEars;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i;</pre>
      
      <pre>-(void) setAge: (int) a;</pre>
      
      <pre>-(void) setNumberOfEars: (int) e;</pre>
      
      <pre>-(int) NumberOfEyes;</pre>
      
      <pre>-(int) Age;</pre>
      
      <pre>-(int) NumberOfEars;</pre>
      
      <pre>@end<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>@implementation Alien</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i {</pre>
      
      <pre>NumberOfEyes = i;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setAge: (int) a {</pre>
      
      <pre>Age = a;</pre>
      
      <pre>}<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>-(void) setNumberOfEars: (int) e {</pre>
      
      <pre>NumberOfEars = e;</pre>
      
      <pre>}<span class="Apple-style-span" style="font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 11px; line-height: normal; white-space: normal;"> </span></pre>
      
      <pre>-(int) NumberOfEyes {</pre>
      
      <pre>return NumberOfEyes;</pre>
      
      <pre>}</pre>
      
      <pre>-(int) Age {</pre>
      
      <pre>return Age;</pre>
      
      <pre>}</pre>
      
      <pre>-(int) NumberOfEars {</pre>
      
      <pre>return NumberOfEars;</pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>Alien *Bill;</pre>
      
      <pre>Bill = [Alien alloc];</pre>
      
      <pre>Bill = [Bill init];</pre>
      
      <pre>[Bill setNumberOfEyes: 8];</pre>
      
      <pre>[Bill setAge: 344];</pre>
      
      <pre>[Bill setNumberOfEars: 3];</pre>
      
      <pre><span style="color: #ff0000;">NSLog(@"The alien is %i years old and has %i eyes and %i ears.", [Bill Age], [Bill NumberOfEyes], [Bill NumberOfEars]);</span></pre>
      
      <pre>[Bill release];</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

The above code will output &#8220;The alien is 344 years old and has 8 eyes and 3 ears.&#8221;

<span style="font-size: large;"><strong>NSLog(@&#8221;The alien is %i years old and has %i eyes and %i ears.&#8221;, [Bill Age], [Bill NumberOfEyes], [Bill NumberOfEars]);</strong></span>

And there you have it, a much simpler and compact way to get the values of the instance variables and output them to the screen.
