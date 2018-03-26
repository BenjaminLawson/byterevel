---
id: 4119
title: 'PHP Tutorial 5 &#8211; if/else Conditional Statements and Comparison Operators'
date: 2012-08-22T18:51:25+00:00
author: Ipodnerd
layout: single
guid: /?p=4119
permalink: /2012/08/22/php-tutorial-5-ifelse-conditional-statements-and-comparison-operators/
image: /wp-content/uploads/2011/07/PHP-icon.jpeg
categories:
  - PHP
tags:
  - conditional
  - if else
  - operators
  - php
  - tutorial
---
[<img class="aligncenter size-full wp-image-2185" title="PHP icon" src="/wp-content/uploads/2011/07/PHP-icon.jpeg" alt="" width="238" height="283" srcset="/wp-content/uploads/2011/07/PHP-icon.jpeg 238w, /wp-content/uploads/2011/07/PHP-icon-180x214.jpeg 180w" sizes="(max-width: 238px) 100vw, 238px" />](/wp-content/uploads/2011/07/PHP-icon.jpeg)

In programming, conditional statements are used to evaluate and compare sets of data. The &#8220;if&#8221; statement executes a block of code only if a certain condition is true. A comparison to this statement used in everyday life might be &#8220;If it is cloudy, then bring an umbrella&#8221; (cloudy being the condition, bringing an umbrella being the action or code). It is often used in conjunction with an &#8220;else&#8221; statement, which executes a block of code if the condition expressed in the if statement is not true.

<pre class="prettyprint linenumstrigger linenums lang-HTML">&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Conditional Statements&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
 
&lt; ?php

$number = 5;

if ($number == 5) {
	echo "The number is 5";
}

?&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

The above code will output &#8220;The value is 5&#8221;. This is because the condition in line 11 is true; the value of the variable $number is equal to 5. The &#8220;==&#8221; is the comparison operator in this case, and translates to &#8220;is equal to&#8221;.

<pre class="prettyprint linenumstrigger linenums lang-HTML">&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Conditional Statements&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
 
&lt; ?php

$number = 2;

if ($number == 5) {
	echo "The number is 5";
} else {
	echo "The number is not 5";
}

?&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

The above code will output &#8220;The number is not 5&#8221; because the condition expressed in line 11, &#8220;$number == 5&#8221; (the value of $number is equal to 5), is false. Because it is false, the code in the else statement is executed.

You may find that you want to test multiple conditions, and that making multiple if/else statements is inefficient. Thankfully, you can utilize &#8220;else if&#8221; statements to append additional blocks of code that you want to execute if other conditions are true.

<pre class="prettyprint linenumstrigger linenums lang-HTML">&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Conditional Statements&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
 
&lt; ?php

$number = 7;

if ($number == 5) {
	echo "The number is 5";
} else if ($number == 7) {
	echo "The number is 7";
} else {
	echo "The number is neither 5 nor 7";
}

?&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

The above code will output &#8220;The number is 7&#8221; because the condition of the &#8220;else if&#8221; statement on line 13 is true. Note that if previous &#8220;if&#8221; or &#8220;else if&#8221; statements are true, further &#8220;else if&#8221; statements that are true will not be executed.

Comparison operators are the symbols in the &#8220;if&#8221; statement condition parentheses. So far, we&#8217;ve only used the &#8220;==&#8221; operator. However, there are several more operators that you can use.

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
      $X < 5
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
      $X > 5
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
      $X == 5
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
      $X != 5
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
      $X <= 5
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
      $X >= 5
    </td>
  </tr>
</table>

Here is an example of the greater than operator in use:

<pre class="prettyprint linenumstrigger linenums lang-HTML">&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Comparison Operator&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
 
&lt; ?php

$number = 6;

if ($number &gt; 3) {
	echo "The number is greater than 3";
}

?&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>

The above code will output &#8220;The number is greater than 3&#8221; because the value of the variable $number is greater than 3, and that is the condition that is being tested. If you set $number equal to a value less than or equal to 3, nothing will be output.
