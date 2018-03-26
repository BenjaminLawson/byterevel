---
id: 2436
title: 'Objective-C Tutorial 5 &#8211; Objects'
date: 2011-08-20T19:47:17+00:00
author: Ipodnerd
layout: single
guid: /?p=2436
permalink: /2011/08/20/objective-c-tutorial-5-objects/
image: /wp-content/uploads/2011/06/objc.png
categories:
  - Objective-C
tags:
  - alien
  - bill
  - classes
  - objective-c
  - objects
  - tutorial
---
[<img class="aligncenter size-full wp-image-1340" title="objective-c" src="/wp-content/uploads/2011/06/objc.png" alt="" width="303" height="297" srcset="/wp-content/uploads/2011/06/objc.png 303w, /wp-content/uploads/2011/06/objc-300x294.png 300w, /wp-content/uploads/2011/06/objc-30x30.png 30w, /wp-content/uploads/2011/06/objc-45x45.png 45w, /wp-content/uploads/2011/06/objc-180x176.png 180w" sizes="(max-width: 303px) 100vw, 303px" />](/wp-content/uploads/2011/06/objc.png)

Hit the play button on <a title="http://www.youtube.com/watch?v=dQw4w9WgXcQ" href="http://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">your favorite music video</a>, because it&#8217;s time for yet another tutorial on the awesome programming language that is Objective-C! In our <a title="Objective-C Tutorial 4 – Classes" href="/2011/07/20/objective-c-tutorial-4-classes/" target="_blank">last tutorial</a>, we studied classes. In our code, we made the &#8220;Alien&#8221; class. This time &#8217;round, we&#8217;re going to make an object. This object is going to be &#8220;Bill&#8221;. Bill is going to be a member of the Alien class.

We briefly discussed what objects were in our last tutorial, but let&#8217;s go over them again anyways. Objects are basically things that inherit all the characteristics of the class that it is a member of. To put this into a  real life example, &#8220;Humans&#8221; could be a class of objects. Your best friend Tom would be an object that is a member of the class &#8220;Humans&#8221;. Tom would inherit (from the Human class) variables like height, gender, age, and weight. Some methods that he might inherit include tying his shoe and walking. Still don&#8217;t get it? Let&#8217;s go over creating objects that are members of a class.

<h1 style="text-align: center;">
  Making An Object
</h1>

We are going to continue working with the code from our last tutorial. That code currently consists of the &#8220;Alien&#8221; class. Just like I promised, we are going to make the Alien &#8220;Bill&#8221;. Bill is going to be an object that is a member of the Alien class.

When we declared the Alien class, we were working entirely outside of the main function. We are now going to start working in the main function, as that is where objects are declared.

Here is the code we will use to create the object Bill:

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>@interface Alien : NSObject {</pre>
      
      <pre>int NumberOfEyes;</pre>
      
      <pre>int Age;</pre>
      
      <pre>int NumberOfEars;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) output;</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i;</pre>
      
      <pre>-(void) setAge: (int) a;</pre>
      
      <pre>-(void) setNumberOfEars: (int) e;</pre>
      
      <pre>@end</pre>
      
      <pre>@implementation Alien</pre>
      
      <pre>-(void) output {</pre>
      
      <pre>NSLog(@"The alien is %i years old and has %i eyes and %i ears.", Age, NumberOfEyes, NumberOfEars);</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i {</pre>
      
      <pre>NumberOfEyes = i;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setAge: (int) a {</pre>
      
      <pre>Age = a;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEars: (int) e {</pre>
      
      <pre>NumberOfEars = e;</pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre><span style="color: #ff0000;">Alien *Bill;</span></pre>
      
      <pre><span style="color: #ff0000;">Bill = [Alien alloc];</span></pre>
      
      <pre><span style="color: #ff0000;">Bill = [Bill init];</span></pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

<span style="font-size: large;"><strong>Alien *Bill;</strong></span>

We declare an object by giving the name of a class followed by an asterisk and the name of the object you want to create (this is called a pointer, we&#8217;ll be going over them in a future tutorial). In this line, we created the object &#8220;Bill&#8221; that is a member of the class &#8220;Alien&#8221;.

**<span style="font-size: large;">Bill = [Alien alloc];</span>**

In this line, we allocate some memory for the object Bill. That is, we borrow some memory from the computer for our object to use. This is done by giving a declared object&#8217;s name, and setting it equal to &#8220;[Class alloc]&#8221; (replacing &#8220;Class&#8221; with the name of the class that the object is a member of).

**<span style="font-size: large;">Bill = [Bill init];</span>**

Before we can use our object, we have to initialize it. This is done by giving a declared object&#8217;s name, and setting it equal to &#8220;[Object init]&#8221; (replacing &#8220;Object&#8221; with the name of the object).

That&#8217;s all there is to creating an object!

<h1 style="text-align: center;">
  Using Methods
</h1>

Now that we&#8217;ve created our object, we want to use the methods that our object inherited from the Alien class.

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>@interface Alien : NSObject {</pre>
      
      <pre>int NumberOfEyes;</pre>
      
      <pre>int Age;</pre>
      
      <pre>int NumberOfEars;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) output;</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i;</pre>
      
      <pre>-(void) setAge: (int) a;</pre>
      
      <pre>-(void) setNumberOfEars: (int) e;</pre>
      
      <pre>@end</pre>
      
      <pre>@implementation Alien</pre>
      
      <pre>-(void) output {</pre>
      
      <pre>NSLog(@"The alien is %i years old and has %i eyes and %i ears.", Age, NumberOfEyes, NumberOfEars);</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i {</pre>
      
      <pre>NumberOfEyes = i;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setAge: (int) a {</pre>
      
      <pre>Age = a;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEars: (int) e {</pre>
      
      <pre>NumberOfEars = e;</pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>Alien *Bill;</pre>
      
      <pre>Bill = [Alien alloc];</pre>
      
      <pre>Bill = [Bill init];</pre>
      
      <pre><span style="color: #ff0000;">[Bill setNumberOfEyes: 8];</span></pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

**<span style="font-size: large;">[Bill setNumberOfEyes: 8];</span>**

To call upon one of the methods that we declared in the Alien class, we put, inside of square brackets, the name of the object followed by the name of the method. If the method needs some kind of value passed into it, then we follow the function name with a colon and the value. In this case, we are using the setNumberOfEyes method and providing it with a value of 8. In our @Implementation section, we made the setNumberOfEyes method take whatever value was passed into it and set the variable NumberOfEyes equal to it. And, just like that, we used the setNumberOFEyes method to give Bill 8 eyes.

Now that we&#8217;ve gone over how to use one method, let&#8217;s use all of the methods that we declared.

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre>@interface Alien : NSObject {</pre>
      
      <pre>int NumberOfEyes;</pre>
      
      <pre>int Age;</pre>
      
      <pre>int NumberOfEars;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) output;</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i;</pre>
      
      <pre>-(void) setAge: (int) a;</pre>
      
      <pre>-(void) setNumberOfEars: (int) e;</pre>
      
      <pre>@end</pre>
      
      <pre>@implementation Alien</pre>
      
      <pre>-(void) output {</pre>
      
      <pre>NSLog(@"The alien is %i years old and has %i eyes and %i ears.", Age, NumberOfEyes, NumberOfEars);</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEyes: (int) i {</pre>
      
      <pre>NumberOfEyes = i;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setAge: (int) a {</pre>
      
      <pre>Age = a;</pre>
      
      <pre>}</pre>
      
      <pre>-(void) setNumberOfEars: (int) e {</pre>
      
      <pre>NumberOfEars = e;</pre>
      
      <pre>}</pre>
      
      <pre>@end</pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>Alien *Bill;</pre>
      
      <pre>Bill = [Alien alloc];</pre>
      
      <pre>Bill = [Bill init];</pre>
      
      <pre><span style="color: #ff0000;">[Bill setNumberOfEyes: 8];</span></pre>
      
      <pre><span style="color: #ff0000;">[Bill setAge: 344];</span></pre>
      
      <pre><span style="color: #ff0000;">[Bill setNumberOfEars: 3];</span></pre>
      
      <pre><span style="color: #ff0000;">[Bill output];</span></pre>
      
      <pre><span style="color: #ff0000;">[Bill release];</span></pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

<span style="font-size: large;"><strong>[Bill output];</strong></span>

The setAge and setNumberOfEars methods are pretty straightforward, but the output method could use a little narration. Unlike the other methods, it doesn&#8217;t need any arguments (values passed into it). What it does is take the variables that we set values for (with the other methods) and plugs them into the sentence we declared in the output method in the@implementation section. It then NSLog&#8217;s (outputs) the sentence to the console.

<span style="font-size: large;"><strong>[Bill release];</strong></span>

Remember how we allocated, or borrowed, some memory from the computer for our Bill object? Well, now we need to release, or give back, that memory. That is done with the line &#8220;[Object release];&#8221; (replacing &#8220;Object&#8221; with the name of the object).

That&#8217;s it. We&#8217;re done. We created the object Bill. Bill was a member of the Alien class. We ran some methods that set the values of some of Bill&#8217;s variables (that he inherited from the Alien class) and then plugged those variables into a sentence and outputted that sentence to the screen. What? You haven&#8217;t done that last thing yet? Whoops. Let&#8217;s do that now.

If you haven&#8217;t opened your console window already, do so now by going to Run -> Console. Next, hit that shiny &#8220;Build and Run&#8221; button. The sentence  &#8220;The alien is 344 years old and has 8 eyes and 3 ears.&#8221; should be outputted to the console window.

Feeling brave? try creating your own alien with different numbers of eyes and ears!

<span class="vvqbox vvqyoutube" style="width:585px;height:330px;"><span id="vvq-2436-youtube-1"><a href="http://www.youtube.com/watch?v=gBzJGckMYO4"><img src="http://img.youtube.com/vi/gBzJGckMYO4/0.jpg" alt="YouTube Preview Image" /></a></span></span> 

_So ya. That&#8217;s all folks. See you next time! I&#8217;m not yet sure what the next tutorial is going to be about._
