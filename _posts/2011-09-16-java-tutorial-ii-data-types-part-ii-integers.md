---
id: 2403
title: 'JAVA Tutorial II &#8211; Data Types (Part II &#8211; Integers)'
date: 2011-09-16T18:05:58+00:00
author: Nikhil Palanki
layout: single
guid: /?p=2403
permalink: /2011/09/16/java-tutorial-ii-data-types-part-ii-integers/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/06/ipad-java2.jpg
categories:
  - JAVA
  - Tutorials
tags:
  - ints
  - java
  - math
  - pre-algebra essentails
  - stuffs
  - tutorials
---
In this tutorial, we&#8217;ll create simple programs using Eclipse that compute solid numbers. We&#8217;ll create a program the divides 2 numbers and a program that adds 2 numbers.

**What&#8217;s an Integer?**

An integer is a number that can be expressed as either a negative or a positive value, but can never be a decimal value. For instance, **3.4** is not an integer, but **-122** is an integer.

Ex) 4/2 = 2. The program will respond with a 2.

Ex) 4/3 = 1.33333&#8230; The program will respond with a 1 instead of the expected/correct answer of 1.33333 .

Why? Because you specified the number to be an Integer, not a Float or Double.

**Setting Up the Project**

I&#8217;m assuming you are familiar with setting up a standard Java Program in Eclipse. But in case it slipped your memory here are the steps:

1. Go to **File > New > Java Project**

2. Label the project &#8220;Integer&#8221;

3. Go to **File > New > Class**

4. Click Browse adjacent to source and select &#8220;Integer&#8221; as the Source folder

5. Label the class &#8220;Integer&#8221;

Congratulations!

**Part I of Part II of Java Tutorial II**

So we&#8217;ll start with observing the adding of integers in a Java program. Here is the code you&#8217;ll need:

<table border="0">
  <tr>
    <td>
      import java.util.Scanner;public class Integer {public static void main(String [] args) { </p> 
      
      <p>
        System.out.print(&#8220;Enter Your First Number&#8221;);
      </p>
      
      <p>
        Scanner scan = new Scanner(System.in);
      </p>
      
      <p>
        int x = scan.nextInt();
      </p>
      
      <p>
        System.out.print(&#8220;Enter Your Second Number&#8221;);
      </p>
      
      <p>
        Scanner scan2 = new Scanner(System.in);
      </p>
      
      <p>
        int y = scan2.nextInt();
      </p>
      
      <p>
        int total = x+y;
      </p>
      
      <p>
        System.out.print(&#8220;The Sum of the Two Numbers is &#8221; + total);
      </p>
      
      <p>
        }
      </p>
      
      <p>
        }</td> </tr> </tbody> </table> 
        
        <p>
          If you want to look at a colored example as the text may help you see the code better, here is a screenshot of the code.
        </p>
        
        <div id="attachment_2452" style="max-width: 549px" class="wp-caption aligncenter">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-ii-integers/screen-shot-2011-08-21-at-10-53-09-am-2/" rel="attachment wp-att-2452"><img class="size-full wp-image-2452" title="Screen shot 2011-08-21 at 10.53.09 AM" src="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-10.53.09-AM1.png" alt="" width="539" height="510" srcset="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-10.53.09-AM1.png 539w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-10.53.09-AM1-300x283.png 300w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-10.53.09-AM1-180x170.png 180w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-10.53.09-AM1-360x340.png 360w" sizes="(max-width: 539px) 100vw, 539px" /></a>
          
          <p class="wp-caption-text">
            Here is the Code
          </p>
        </div>
        
        <p>
          <strong>import java.util.Scanner;</strong>
        </p>
        
        <p>
          There are 2 major ways of allowing the user to input data. You can use BufferedReader (which we will eventually cover) or Scanner. Scanner is much easier to use and for our learning sake, we&#8217;ll use it. But in order to use the Scanner, you have to import it first. <em>import java.util.Scanner;</em> is the piece of code you use.
        </p>
        
        <p>
          So when you use the scanner, you do the following:
        </p>
        
        <p>
          1. Scanner scan = new Scanner(System.in); //System.in means you are going to input data. &#8220;scan&#8221; after Scanner is like a new instance of it. That&#8217;s why during the second block of code, you use &#8220;scan2&#8221; because scan is already in use.
        </p>
        
        <p>
          2. int x = scan.nextInt(); //You declare the integer you are using here and you MUST put the &#8220;scan&#8221; that you are going to scan with. This is very vague isn&#8217;t it? Well, you can figure this part out if my explanation was too obscure (chances are it was)
        </p>
        
        <p>
          <strong>Declaring Ints</strong>
        </p>
        
        <p>
          You can declare an integer anywhere by placing the <strong>int </strong>next to a name followed by a semi-colon. But in this case, it has to be declared at a certain point. And that certain point is directly after you declare the Scanner.
        </p>
        
        <p>
          <strong>Addition Logic</strong>
        </p>
        
        <p>
          When adding 2 numbers, you have to come up with the resulting integer. &#8220;Int total = x+y;&#8221; was the code to use.
        </p>
        
        <div id="attachment_2453" style="max-width: 694px" class="wp-caption aligncenter">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-ii-integers/screen-shot-2011-08-21-at-11-08-19-am/" rel="attachment wp-att-2453"><img class="size-full wp-image-2453 " title="Screen shot 2011-08-21 at 11.08.19 AM" src="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.08.19-AM.png" alt="" width="684" height="156" srcset="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.08.19-AM.png 760w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.08.19-AM-300x68.png 300w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.08.19-AM-180x40.png 180w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.08.19-AM-360x81.png 360w" sizes="(max-width: 684px) 100vw, 684px" /></a>
          
          <p class="wp-caption-text">
            Example of the Console's Building of the Application
          </p>
        </div>
        
        <p>
          <strong>Part II of Part II of Java Tutorial II</strong>
        </p>
        
        <p>
          Now we are going to look at division. Not because division is cool or difficult or starts with a &#8220;d.&#8221; Division requires a float to be as the quotient of the problem because most division problems result with a non-integral number. But since this is an Integer tutorial, we are going to not use float just because we are rebels.
        </p>
        
        <p>
          <strong>Creating the Program</strong>
        </p>
        
        <p>
          You do not need to create a new class or anything. Just stick with what you already have. All you have to do is change the section where it says &#8220;int total = x+y&#8221; to &#8220;int total = x/y.&#8221; Then you can change all of the System.out.print to (&#8220;Enter the Dividend&#8221;) and to (&#8220;Enter the Divisor&#8221;). Then you can change the System.out.print that says (&#8220;The Sum of the Two Numbers is&#8221; + total); to (&#8220;The Quotient of the Two Numbers is&#8221; + total);
        </p>
        
        <p>
          Here is what the code should look like in the program:
        </p>
        
        <div id="attachment_2454" style="max-width: 547px" class="wp-caption aligncenter">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-ii-integers/screen-shot-2011-08-21-at-11-15-28-am/" rel="attachment wp-att-2454"><img class="size-full wp-image-2454" title="Screen shot 2011-08-21 at 11.15.28 AM" src="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.15.28-AM.png" alt="" width="537" height="507" srcset="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.15.28-AM.png 537w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.15.28-AM-300x283.png 300w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.15.28-AM-180x169.png 180w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.15.28-AM-360x339.png 360w" sizes="(max-width: 537px) 100vw, 537px" /></a>
          
          <p class="wp-caption-text">
            Notice the changes in the System.out.print and the Math Logic
          </p>
        </div>
        
        <p>
          So let&#8217;s compile this program and launch it. If you enter numbers that would normally result in a decimal, it&#8217;ll round down. Always. So you should replace the &#8220;Int&#8221; before &#8220;total&#8221; with a &#8220;Float.&#8221;
        </p>
        
        <div id="attachment_2455" style="max-width: 691px" class="wp-caption aligncenter">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-ii-integers/screen-shot-2011-08-21-at-11-19-37-am/" rel="attachment wp-att-2455"><img class="size-full wp-image-2455 " title="Screen shot 2011-08-21 at 11.19.37 AM" src="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.19.37-AM.png" alt="" width="681" height="131" srcset="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.19.37-AM.png 757w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.19.37-AM-300x57.png 300w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.19.37-AM-180x34.png 180w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-11.19.37-AM-360x69.png 360w" sizes="(max-width: 681px) 100vw, 681px" /></a>
          
          <p class="wp-caption-text">
            Just What I thought. 4 divided by 3 equals 0. I'll ace AP Division for sure.
          </p>
        </div>
        
        <p style="text-align: center;">
          So, you are now a master of inputting floats and such. Congratulations.
        </p>
        
        <p style="text-align: center;">
          Are you ready for Part III, floats? &#8211; <a href="/2011/09/16/java-tutorial-ii-data-types-part-iii-floats/">Next Page>></a>
        </p>
        
        <p style="text-align: center;">
          <a href="/2011/09/16/java-tutorial-ii-data-types-scanners-and-java-math-part-i/">< <Previous Page</a> &#8211; Need to Go Back to Part I?</a>
        </p>
