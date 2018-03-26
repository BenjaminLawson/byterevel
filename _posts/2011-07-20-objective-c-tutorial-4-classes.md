---
id: 1981
title: 'Objective-C Tutorial 4 &#8211; Classes'
date: 2011-07-20T18:58:15+00:00
author: Ipodnerd
layout: single
guid: /?p=1981
permalink: /2011/07/20/objective-c-tutorial-4-classes/
image: /wp-content/uploads/2011/06/objc.png
categories:
  - Objective-C
tags:
  - class
  - interface
  - method
  - objective-c
  - programming
  - tutorial
  - variable
---
[<img class="aligncenter size-full wp-image-1340" title="objective-c" src="/wp-content/uploads/2011/06/objc.png" alt="" width="303" height="297" srcset="/wp-content/uploads/2011/06/objc.png 303w, /wp-content/uploads/2011/06/objc-300x294.png 300w, /wp-content/uploads/2011/06/objc-30x30.png 30w, /wp-content/uploads/2011/06/objc-45x45.png 45w, /wp-content/uploads/2011/06/objc-180x176.png 180w" sizes="(max-width: 303px) 100vw, 303px" />](/wp-content/uploads/2011/06/objc.png)

As you probably heard on the news this morning, there is a new Objective-C tutorial out. And it&#8217;s right here. How cool is that? Last time, we [discussed if else statements and basic loops](/2011/07/13/objective-c-tutorial-3-if-else-statements-and-basic-looping/ "Objective-C Tutorial 3 – If Else Statements And Basic Looping"). This time, we&#8217;re going to master the art of the class. So what is a class? A class is basically a classification and framework for an object. Objects that are members of a class inherit variables and methods that are declared in the class. To put this into a real life example, you would be an object of the class &#8220;Human&#8221;. You might inherit variables such as height, gender, age, and weight. Some methods that you might inherit include tying your shoe and walking. Get it yet? Don&#8217;t worry if you don&#8217;t. That&#8217;s what this tutorial is for. Let&#8217;s make a class &#8220;aliens&#8221; (and, in the next tutorial, an object &#8220;Bill&#8221;).

<h1 style="text-align: center;">
  Interface
</h1>

The first part of a class is the interface. In the interface, we name the variables and  methods of the class. When making a program that adheres to proper Objective-C practices, the interface goes in the header file ( .h ) and is imported into the main ( .m ) file. For the purpose of this tutorial, however, we are going to ignorantly put it in the main ( .m ) file. That&#8217;s pretty important to know.

Our class is going to be &#8220;Alien&#8221;. The variables that we want members of the alien class to have include: number of eyes, age, and number of ears. Methods that members of the alien class are going to inherit will include: setNumberOfEyes, setAge, setNumberOfEars, and output. All of the &#8220;set&#8221; methods will be used in our program to set the value of the variables. Enough explaining for now, lets look over the code of an interface. Since we are coding only in the main file for now, the interface section will go right under the &#8220;#import&#8221; line(s).

<table border="0" align="center">
  <tr>
    <td>
      <pre>#import &lt;Foundation/Foundation.h&gt;</pre>
      
      <pre><span style="color: #ff0000;">@interface Alien : NSObject {</span></pre>
      
      <pre><span style="color: #ff0000;">int NumberOfEyes;</span></pre>
      
      <pre><span style="color: #ff0000;">int Age;</span></pre>
      
      <pre><span style="color: #ff0000;">int NumberOfEars;</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) output;</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) setNumberOfEyes: (int) i;</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) setAge: (int) a;</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) setNumberOfEars: (int) e;</span></pre>
      
      <pre><span style="color: #ff0000;">@end</span></pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

<span style="font-size: large;"><strong>@interface Alien : NSObject {</strong></span>

We declare the interface of a class with &#8220;@interface&#8221; followed by the class name (in this case &#8220;Alien&#8221;), a colon, and the super class (you really don&#8217;t need to know about them yet, don&#8217;t worry about it; just use NSObject for your programs until a later date on which I will explain them). The opening curly bracket opens the section of the interface where we will give the variables of the class.

<span style="font-size: large;"><strong>int NumberOfEyes;</strong></span>

<span style="font-size: large;"><strong>int Age;</strong></span>

<span style="font-size: large;"><strong>int NumberOfEars;</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

This is where we declare the variables that members of our class will inherit. If we create an object that is a member of the class &#8220;Alien&#8221;, then it will have the variables NumberOfEyes, Age, and NumberOfEars. The closing curly bracket closes the part of the interface where we declare the variables.

<span style="font-size: large;"><strong>-(void) output;</strong></span>

<span style="font-size: large;"><strong>-(void) setNumberOfEyes: (int) i;</strong></span>

<span style="font-size: large;"><strong>-(void) setAge: (int) a;</strong></span>

<span style="font-size: large;"><strong>-(void) setNumberOfEars: (int) e;</strong></span>

These are the declarations of the methods for our class. The actual methods will be in the implementation section (which we will go over next). Let&#8217;s go over how we declare a method. First, we have a dash followed by what the method will be returning (the &#8220;return value&#8221;). By returning, I mean that when we call a method in our program, do we want to get  any information back from the method to use in our program, or do we just want the code in our method to run. If we don&#8217;t want to return anything, we put &#8220;void&#8221;. If we wanted to return an integer value, we would put &#8220;-(int)&#8221;. Next, we name out method. In the method &#8220;-(void) setNumberOfEyes: (int) i;&#8221;, setNumberOfEyes is the name of the method. This will be what we use to call on the method in our program. For methods that don&#8217;t need any information (they just run a bit of code when called upon), we would be done now (as is the case of the output method). For other methods, like setNumberOfEyes, we need to declare what type of information we are passing into it as well as the name of the variable that will be equal to the value that we pass into it. In the code of our methods, we can use that variable. If you don&#8217;t quite understand what I&#8217;m saying, just keep following along and you will get it at some point.

<span class="Apple-style-span" style="font-size: large;"><strong>@end</strong></span>

We use @end to end our interface section. Bam. We&#8217;re done with the interface. That wasn&#8217;t so bad, was it?

<h1 style="text-align: center;">
  Implementation
</h1>

The second part of a class is the implementation section. In it, we give the methods that we declared in the interface some body. That is, each of the methods that we declared in the interface has to have some code to run when they are called upon, and we write that code in the implementation section. You savvy? Here&#8217;s what the implementation section of our program is going to look like:

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
      
      <pre><span style="color: #ff0000;">@implementation Alien</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) output {</span></pre>
      
      <pre><span style="color: #ff0000;">NSLog(@"The alien is %i years old and has %i eyes and %i ears.", Age, NumberOfEyes, NumberOfEars);</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) setNumberOfEyes: (int) i {</span></pre>
      
      <pre><span style="color: #ff0000;">NumberOfEyes = i;</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) setAge: (int) a {</span></pre>
      
      <pre><span style="color: #ff0000;">Age = a;</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre><span style="color: #ff0000;">-(void) setNumberOfEars: (int) e {</span></pre>
      
      <pre><span style="color: #ff0000;">NumberOfEars = e;</span></pre>
      
      <pre><span style="color: #ff0000;">}</span></pre>
      
      <pre><span style="color: #ff0000;">@end</span></pre>
      
      <pre>int main (int argc, const char * argv[]) {</pre>
      
      <pre>    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];</pre>
      
      <pre>[pool drain];</pre>
      
      <pre>    return 0;</pre>
      
      <pre>}</pre>
    </td>
  </tr>
</table>

&nbsp;

<span style="font-size: large;"><strong>@implementation Alien</strong></span>

We declare the implementation section with a simple @implementation followed by the name of the class that the implementation corresponds to.

<span style="font-size: large;"><strong>-(void) output {</strong></span>

<span style="font-size: large;"><strong>NSLog(@&#8221;The alien is %i years old and has %i eyes and %i ears.&#8221;, Age, NumberOfEyes, NumberOfEars);</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

<span style="font-size: large;"><strong>-(void) setNumberOfEyes: (int) i {</strong></span>

<span style="font-size: large;"><strong>NumberOfEyes = i;</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

<span style="font-size: large;"><strong>-(void) setAge: (int) a {</strong></span>

<span style="font-size: large;"><strong>Age = a;</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

<span style="font-size: large;"><strong>-(void) setNumberOfEars: (int) e {</strong></span>

<span style="font-size: large;"><strong>NumberOfEars = e;</strong></span>

<span style="font-size: large;"><strong>}</strong></span>

These are the bodies of our methods. In order to tell the computer which lines of code correspond to which methods in the interface, we copy the interface method declaration (minus the semicolon) from the interface and paste it in the implementation section. Then, we surround the code of each method with curly brackets (as shown the code above). As I mentioned in the explanation of the interface, methods that require information to be passed into them have a colon after the method name followed by the data type and the name of the variable that will be equal to the information we are passing into the method. We can then use that variable in the code of each method. For example, the &#8220;setNumberOfEyes&#8221; method requires that an integer value be passed into it. The variable &#8220;i&#8221; will be set equal to the value that is passed into the method. In the code of our method, we set the variable &#8220;NumberOfEyes&#8221; (as declared in our @interface) equal to the variable &#8220;i&#8221;, thus setting &#8220;NumberOfEyes&#8221; equal to the integer value that is passed into the method.

You might ask why we are taking the long way around setting the alue of the variables that were declared in the interface section. Well, those variables are &#8220;protected&#8221; as it were, and can only be accessed by the methods of the same class.

<span style="font-size: large;"><strong>@end</strong></span>

Just like the interface, we end our implementation section with a &#8220;@end&#8221;.

_In our next tutorial, we will go over making objects that are members of our class._
