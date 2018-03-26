---
id: 2456
title: 'JAVA Tutorial II &#8211; Data Types (Part III &#8211; Floats)'
date: 2011-09-16T18:00:23+00:00
author: Nikhil Palanki
layout: single
guid: /?p=2456
permalink: /2011/09/16/java-tutorial-ii-data-types-part-iii-floats/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/06/ipad-java4.jpg
categories:
  - JAVA
  - Tutorials
tags:
  - float
  - java
  - java math
  - joe blabbah
  - scanners
---
Floats can do what Ints cannot because Ints are stupid&#8230;Just kidding. People prefer Ints because &#8220;they use less memory.&#8221; Most computers nowadays can handle all of the floats so it wouldn&#8217;t be much of a problem to outsource the Ints&#8217; job to the floats.

**What&#8217;s a Float?**

A Float is a number than can hold a limited amount of decimal places. They are commonly declared as a **Float** x; or **Float** potatoes;. Since Java is heavily inspired by C++, Floats are declared the same way in both.

**What&#8217;s in Store?**

For this section, we are going to rebuild the Division problem. We are also going to cover the other 2 types of simple mathematics logic (subtraction and multiplication). Many of the terms learned in the Ints section will spill over into this section, such as the Scanner. We&#8217;ll learn how to implement floats and what happens when you replace ints with a float on a division problem.

**Part I of Part III of Java Tutorial II**

Create a new program and new class. You should have this down by now. After creating the new class, (we&#8217;ll name it Float), create the code as if you were making the Division Program but replace all of the Ints with Floats. Here is the code you will need for the actual program.

<table border="0">
  <tr>
    <td>
      import java.util.Scanner;public class Float {&nbsp;</p> 
      
      <p>
        public static void main(String[] args) {
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        System.out.print(&#8220;Enter Your Dividend&#8221;);
      </p>
      
      <p>
        Scanner scan = new Scanner(System.in);
      </p>
      
      <p>
        float x = scan.nextFloat();
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        System.out.print(&#8220;Enter Your Divisor&#8221;);
      </p>
      
      <p>
        Scanner scan2 = new Scanner(System.in);
      </p>
      
      <p>
        float y = scan.nextFloat();
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        float total=x/y;
      </p>
      
      <p>
        System.out.print(&#8220;Your Quotient is &#8221; + total);
      </p>
      
      <p>
        }
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        }</td> </tr> </tbody> </table> 
        
        <p>
          And here is the color coded copy:
        </p>
        
        <div id="attachment_2464" style="max-width: 546px" class="wp-caption aligncenter">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-iii-floats/screen-shot-2011-08-21-at-5-12-15-pm/" rel="attachment wp-att-2464"><img class="size-full wp-image-2464" title="Screen shot 2011-08-21 at 5.12.15 PM" src="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.12.15-PM.png" alt="" width="536" height="508" srcset="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.12.15-PM.png 536w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.12.15-PM-300x284.png 300w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.12.15-PM-180x170.png 180w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.12.15-PM-360x341.png 360w" sizes="(max-width: 536px) 100vw, 536px" /></a>
          
          <p class="wp-caption-text">
            Here is the code
          </p>
        </div>
        
        <p>
          <strong>Float Result</strong>
        </p>
        
        <p>
          Once you compile the program, enter numbers. If you place non-Integral numbers, notice that it gives a response including a decimal. But this decimal is limited to a certain amount of digits. If we wanted to increase the amount of digits, you&#8217;d need a data type that has a larger memory capacity.
        </p>
        
        <p>
          <strong>Division Logic</strong>
        </p>
        
        <p>
          To divide numbers, you just use the &#8220;/&#8221; forward slash symbol.
        </p>
        
        <p>
          <strong>Part II of Part III of Java Tutorial II</strong>
        </p>
        
        <p>
          We aren&#8217;t going to change the code so the result would have multiplied numbers. But when using Multiplication logic, you have to just change the forward slash (&#8220;/&#8221;) symbol into an asterisk. When creating a program that subtracts numbers, you&#8217;d change the forward slash, asterisk, or addition sign into a dash. Pretty simple huh?
        </p>
        
        <p style="text-align: center;">
          We covered Floats and Ints, but we also covered simple mathematics and Input/Output!
        </p>
        
        <p style="text-align: center;">
          You ready for Double? <a href="/2011/09/16/java-tutorial-ii-data-types-part-iv-double/">Next Page >></a>
        </p>
        
        <p style="text-align: center;">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-ii-integers/"><<Previous Page</a> Return to Integers?
        </p>
