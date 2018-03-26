---
id: 2465
title: 'JAVA Tutorial II &#8211; Data Types (Part IV &#8211; Double)'
date: 2011-09-16T17:58:47+00:00
author: Nikhil Palanki
layout: single
guid: /?p=2465
permalink: /2011/09/16/java-tutorial-ii-data-types-part-iv-double/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/06/ipad-java4.jpg
categories:
  - JAVA
tags:
  - byterevel
  - data types
  - double
  - hoopla
  - java
  - java math
  - joe blabbah
  - scanner
---
**What&#8217;s A Double?**

Doubles are variables that have an increased storage capacity. They use up twice as much memory as a float, but our computer being the way they are, it really doesn&#8217;t make much of a difference. When performing functions such as Logarithms and Square Roots, you have to use a Double because Floats and Ints generally aren&#8217;t capable to hold that amount of data.

**What&#8217;s In Store?**

We&#8217;ll take a good look at what would be &#8220;cmath&#8221; in C++. We&#8217;ll construct the program for Square Roots, but I&#8217;ll give you the functions for changing it to compute Logarithms, Cube Roots, Powers&#8230;

**Code for Square Roots**

Here is the code you&#8217;d need for the square roots.

<table border="0">
  <tr>
    <td>
      import java.util.Scanner;public class Double {</p> 
      
      <p>
        &nbsp;
      </p>
      
      <p>
        public static void main(String[] args) {
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        //Collecting the Data Here
      </p>
      
      <p>
        System.out.println(&#8220;Enter a number you&#8217;d like the square root of &#8220;);
      </p>
      
      <p>
        Scanner scan = new Scanner(System.in);
      </p>
      
      <p>
        double x = scan.nextDouble();
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        //Actual Square Root
      </p>
      
      <p>
        double answer = java.lang.Math.sqrt(x);
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        //Displaying the Answer
      </p>
      
      <p>
        System.out.print(&#8220;The Square Root of &#8221; + x + &#8221; is &#8221; + answer);
      </p>
      
      <p>
        }
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        }</td> </tr> </tbody> </table> 
        
        <p>
          And here is the color code:
        </p>
        
        <div id="attachment_2466" style="max-width: 496px" class="wp-caption aligncenter">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-iv-double/screen-shot-2011-08-21-at-5-50-18-pm/" rel="attachment wp-att-2466"><img class="size-full wp-image-2466  " title="Screen shot 2011-08-21 at 5.50.18 PM" src="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.50.18-PM.png" alt="" width="486" height="370" srcset="/wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.50.18-PM.png 759w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.50.18-PM-300x228.png 300w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.50.18-PM-180x136.png 180w, /wp-content/uploads/2011/08/Screen-shot-2011-08-21-at-5.50.18-PM-360x273.png 360w" sizes="(max-width: 486px) 100vw, 486px" /></a>
          
          <p class="wp-caption-text">
            Doubles
          </p>
        </div>
        
        <p>
          <strong>scan.nextDouble();</strong>
        </p>
        
        <p>
          If you have noticed, you change this function slightly depending on the data type you are using. We have seen Ints and Floats in place of the Double.
        </p>
        
        <p>
          <strong>java.lang.Math.sqrt();</strong>
        </p>
        
        <p>
          This function completes the mathematics function. You place the variable you want to use in the parenthesis. In the code, we used the variable from the Scanner input. Here is a table containing different and widely used java.lang.Math.insertfunctionhere();
        </p>
        
        <table class="alignleft" border="0">
          <tr>
            <td style="text-align: left;">
              <strong>Function Name</strong>
            </td>
            
            <td style="text-align: left;">
              <strong>Code of the Function</strong>
            </td>
          </tr>
          
          <tr>
            <td>
              Exponentiation
            </td>
            
            <td>
              double x = java.lang.Math.pow(insertbasehere, insertpowerhere);
            </td>
          </tr>
          
          <tr>
            <td>
              Cube Root
            </td>
            
            <td>
              double x = java.lang.Math.cbrt(cubednumber);
            </td>
          </tr>
          
          <tr>
            <td>
              Logarithm
            </td>
            
            <td>
              double x = java.lang.Math.log(insertdesirednumberhere)/Math.log(insertlognumberhere);
            </td>
          </tr>
          
          <tr>
            <td>
              Absolute Value
            </td>
            
            <td>
              int x = java.lang.Math.abs(insertnumberhere);
            </td>
          </tr>
          
          <tr>
            <td>
              Square Root
            </td>
            
            <td>
              double x = java.lang.Math.sqrt(insertnumberhere);
            </td>
          </tr>
          
          <tr>
            <td>
              Show the Minimum of 2 Numbers
            </td>
            
            <td>
              double answer = java.lang.Math.min(number1, number2);
            </td>
          </tr>
          
          <tr>
            <td>
              Show the Maximum of 2 Numbers
            </td>
            
            <td>
              double answer = java.lang.Math.max(number1, number2);
            </td>
          </tr>
          
          <tr>
            <td>
              Convert Radians to Degrees
            </td>
            
            <td>
              double answer = java.lang.Math.toDegrees(insertradianshere);
            </td>
          </tr>
          
          <tr>
            <td>
              Convert Degrees to Radians
            </td>
            
            <td>
              double answer = java.lang.Math.toRadians(insertradianshere);
            </td>
          </tr>
          
          <tr>
            <td>
            </td>
            
            <td>
            </td>
          </tr>
        </table>
        
        <p style="text-align: left;">
          So now you have a taste of Double. Since most computers can utilize large amounts of doubles, most programmers like to use doubles instead of float because of the accuracy and the large numbers that can be held on them.
        </p>
        
        <p style="text-align: center;">
          Now that you&#8217;ve &#8220;doubled&#8221; your knowledge (I know, I&#8217;m hilarious), let&#8217;s go onto char
        </p>
        
        <p style="text-align: center;">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-v-char/">Ready for char >></a>
        </p>
        
        <p style="text-align: center;">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-iii-floats/"><< Back to Float</a>
        </p>
