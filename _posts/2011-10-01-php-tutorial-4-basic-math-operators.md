---
id: 2972
title: 'PHP Tutorial 4 &#8211; Basic Math Operators'
date: 2011-10-01T19:07:52+00:00
author: Ipodnerd
layout: single
guid: /?p=2972
permalink: /2011/10/01/php-tutorial-4-basic-math-operators/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
onswipe_thumb:
  - /wp-content/uploads/2011/07/PHP-icon.jpeg
image: /wp-content/uploads/2011/07/PHP-icon.jpeg
categories:
  - PHP
tags:
  - php
  - tutorial
  - tutorials
---
[<img class="aligncenter size-full wp-image-2185" title="PHP icon" src="/wp-content/uploads/2011/07/PHP-icon.jpeg" alt="" width="238" height="283" srcset="/wp-content/uploads/2011/07/PHP-icon.jpeg 238w, /wp-content/uploads/2011/07/PHP-icon-180x214.jpeg 180w" sizes="(max-width: 238px) 100vw, 238px" />](/wp-content/uploads/2011/07/PHP-icon.jpeg)

In our last tutorial, we discussed variables and comments in PHP. Today, we are going to go over basic math operators. By math operators, I mean symbols that represent math operations. Adding, subtracting, dividing, and multiplying are all examples of math operators. There are seven main operators in PHP, and they can be seen in the following table:

<table border="0" align="center">
  <tr>
    <td style="text-align: center;">
      <strong>Operation</strong>
    </td>
    
    <td style="text-align: center;">
      <strong>Operator (Symbol Used To Perform The Operation)</strong>
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      Addition
    </td>
    
    <td style="text-align: center;">
      +
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      Subtraction
    </td>
    
    <td style="text-align: center;">
      &#8211;
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      Multiplication
    </td>
    
    <td style="text-align: center;">
      *
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      Division
    </td>
    
    <td style="text-align: center;">
      /
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      Remainder / Modulus
    </td>
    
    <td style="text-align: center;">
      %
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      Increase By 1 / Increment
    </td>
    
    <td style="text-align: center;">
      ++
    </td>
  </tr>
  
  <tr>
    <td style="text-align: center;">
      Decrease By 1 / Decrement
    </td>
    
    <td style="text-align: center;">
      &#8212;
    </td>
  </tr>
</table>

Let&#8217;s put the first five basic math operations to use in a short program:

<table border="0" align="center">
  <tr>
    <td>
      <pre>



< ?php

<span style="color: #ff0000;">echo (6 + 4)."";
<span style="color: #ff0000;">echo (6 - 4)."";</span>
<span style="color: #ff0000;">echo (6 * 4)."";</span>
<span style="color: #ff0000;">echo (6 / 4)."";</span>
<span style="color: #ff0000;">echo (6 % 4)."";</span>

?>

</body>
</html></pre>
</td>
</tr>
</tbody>
</table>


<p>
  When compiled, the above code will output the following to the screen:
</p>


<table border="0" align="center">
  
  
  
  <tr>
    <td>
      10<br />
      2<br />
      24<br />
      1.5<br />
      2
    </td>
    
  </tr>
  
  
</table>


<p>
  <span style="font-size: large;"><strong>echo (6 + 4).&#8221;&#8221;;</strong></span>
</p>


<p>
  Every line of PHP code in this program was almost the same, so let&#8217;s take a look at this one. We outputted the sum of six and four to the screen. Notice the lack of quotation marks, this isn&#8217;t a string. We also concatenated an HTML line break tag onto the end of our echo function. Without a line break, all of the numbers would be squished together on one line. If we were working with a strictly PHP page, then we could simply output &#8220;\n&#8221; to get the same effect. However, since our PHP code is within an HTML page, we must adhere to HTML syntax when outputting anything to the page.
</p>


<p>
  We can also use mathematical operators in variable definitions.
</p>


<table border="0" align="center">
  
  
  
  <tr>
    <td>
      <pre>



< ?php

<span style="color: #ff0000;">$adding = 6 + 4;
<span style="color: #ff0000;">$subtracting = 6 - 4;</span>
<span style="color: #ff0000;">$multiplying = 6 * 4;</span>
<span style="color: #ff0000;">$dividing = 6 / 4;</span>
<span style="color: #ff0000;">$modulus = 6 % 4;</span>

<span style="color: #ff0000;">echo $adding."";</span>
<span style="color: #ff0000;">echo $subtracting."";</span>
<span style="color: #ff0000;">echo $multiplying."";</span>
<span style="color: #ff0000;">echo $dividing."";</span>
<span style="color: #ff0000;">echo $modulus."";</span>

?>

</body>
</html></pre>
</td>
</tr>
</tbody>
</table>


<p>
  This code will output the same thing as the previous chunk of code, but it uses a different method. First, it sets four variables equal to one of 5 basic math operations. Then, it outputs the values of the variables (along with a line break tag). Notice how there aren&#8217;t any quotation marks around the operations in the variable declarations; only strings need quotation marks.
</p>


<p>
  When declaring variables, we aren&#8217;t limited to only using numbers in operations. We can also perform math operations with variables.
</p>


<table border="0" align="center">
  
  
  
  <tr>
    <td>
      <pre>



< ?php

<span style="color: #ff0000;">$six = 6;
<span style="color: #ff0000;">$four = 4;</span>

<span style="color: #ff0000;">$subtracting = $six - $four;</span>

<span style="color: #ff0000;">echo $adding;</span>

?>

</body>
</html></pre>
</td>
</tr>
</tbody>
</table>


<p>
  The above code will output &#8220;2&#8221;.
</p>


<p>
  <span style="font-size: large;"><strong>$subtracting = $six &#8211; $four;</strong></span>
</p>


<p>
  In this line, we set the variable &#8220;subtracting&#8221; equal to the value that results from subtracting the value of the variable &#8220;four&#8221; from the value of the variable &#8220;six&#8221;. Once the values of $six and $four have been retrieved, the line looks like &#8220;$subtracting = 6 &#8211; 4;&#8221;. In the line &#8220;echo $subtracting;&#8221;, we go on to output the value of $subtracting.
</p>


<p>
  PHP doesn&#8217;t limit you to simple operations; you can perform many operations at once.
</p>


<table border="0" align="center">
  
  
  
  <tr>
    <td>
      <pre>



< ?php

<span style="color: #ff0000;">$operations = 6 * 2 + 4 /2 - 7;

<span style="color: #ff0000;">echo $operations;</span>

?>

</body>
</html></pre>
</td>
</tr>
</tbody>
</table>


<p>
  The above code will output &#8220;7&#8221;.
</p>


<p>
  As you can see, we set a variable equal to a complex expression. Way back in your first years of school, you were  taught a process called &#8220;PEMDAS&#8221;. That is, different operations occur before others when simplifying an expression, equality, or even an inequality. PHP follows these basic math rules as well, so make sure you know the order of operations.
</p>


<p>
  <a href="/wp-content/uploads/2011/10/pemdas1.gif"><img class="aligncenter size-full wp-image-3004" title="pemdas1" src="/wp-content/uploads/2011/10/pemdas1.gif" alt="" width="246" height="130" /></a>
</p>


<p>
  As you can see, the first thing that happens when simplifying operations is that operations in parenthesis are simplified first. Therefore, if you want an operation to occur first, put it in parenthesis.
</p>


<p>
  It&#8217;s annoying to type &#8220;$variable = $variable + 1&#8221; so most programming languages have things called increment and decrement operators. PHP is no exception, so you can easily increase and decrease the values of variables by 1.
</p>


<table border="0" align="center">
  
  
  
  <tr>
    <td>
      <pre>


 
< ?php

<span style="color: #ff0000;">$increment = 5;
<span style="color: #ff0000;">$decrement = 8;</span>

<span style="color: #ff0000;">$increment++;</span>
<span style="color: #ff0000;">$decrement--;</span>

<span style="color: #ff0000;">echo $increment."";</span>
<span style="color: #ff0000;">echo $decrement."";</span>

?>

</body>
</html></pre>
</td>
</tr>
</tbody>
</table>


<p>
  The above code will output:
</p>


<table border="0" align="center">
  
  
  
  <tr>
    <td>
      6</p>
      
      
      <p>
        7</td>
        </tr>
        </tbody>
        </table>
        
        
        <p>
          <span style="font-size: large;"><strong>$increment++;</strong></span>
        </p>
        
        
        <p>
          This is simply equivalent to  the operation &#8220;$increment = $increment + 1;&#8221;.
        </p>
        
        
        <p>
          <span style="font-size: large;"><strong> $decrement++;</strong></span>
        </p>
        
        
        <p>
          This is simply equivalent to the operation &#8220;$decrement = $decrement &#8211; 1;&#8221;
        </p>
        
        
        <p>
          Sadly, our tutorial is coming to an end. I hope that you found it helpful and informative! If you are left with any questions, please leave a comment.
        </p>
