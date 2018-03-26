---
id: 2751
title: 'JAVA Tutorial II &#8211; Data Types (Part V &#8211; Char)'
date: 2011-09-16T18:04:15+00:00
author: Nikhil Palanki
layout: single
guid: /?p=2751
permalink: /2011/09/16/java-tutorial-ii-data-types-part-v-char/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/06/ipad-java2.jpg
categories:
  - JAVA
  - Tutorials
tags:
  - java
  - java coffee
  - java is awesome
  - java lang
  - java math
  - scan
---
**What is a Char?**

Char is short for character, and they are interesting data types.They can only hold single values, which isn&#8217;t very useful if you are trying to hold a lot of data. But they do have their uses. If you want to create a multiple choice test, you can use chars as the values, but you are going to have to convert them from Strings. That is a complicated process which I am not inclined to explain in this tutorial. What I will explain is how to declare the value of a char.

**Here is the Code:**

So we&#8217;ll declare a simple char, and output it.

<table border="0" align="center">
  <tr>
    <td>
      import java.util.Scanner;public class Char {public static void main(String[] args) {</p> 
      
      <p>
        Scanner charscanner = new Scanner(System.in);
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        char x = &#8216;a&#8217;;
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        System.out.print(&#8220;The character is &#8221; + x);
      </p>
      
      <p>
        &nbsp;
      </p>
      
      <p>
        &nbsp;
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
          This is pretty self-explanatory. But the only difference, is in order to declare a char, you need to use only a single character like a period or the letter &#8220;a.&#8221;
        </p>
        
        <p style="text-align: center;">
          So this is how you use a Char in Java
        </p>
        
        <p style="text-align: center;">
          <a href="/2011/09/16/java-tutorial-ii-data-types-part-iv-double/"><< Return to Double</a>
        </p>
