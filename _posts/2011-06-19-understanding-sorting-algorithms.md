---
id: 991
title: Understanding Sorting Algorithms
date: 2011-06-19T10:52:53+00:00
author: Nikhil Palanki
layout: single
guid: /?p=991
permalink: /2011/06/19/understanding-sorting-algorithms/
categories:
  - How To
  - Tutorials
  - Uncategorized
tags:
  - algorithms
  - bogus sort
  - bubble sort
  - great sorting algorithms
  - how can i use an algorithm
  - how to use a sorting algorithm
  - monkey sort bogosort
  - selection sort
  - what is a sorting algorithm
---
Question: What the !#$% is a Sorting Algorithm?

Answer: Don&#8217;t !@$#-ing swear on Byte Revel. A Sorting Algorithm is a process of putting a group of objects in a certain list or order.

Question: Why the heck would I need a Sorting Algorithm?

Answer: Programs don&#8217;t just sort stuff when you tell them to. They need to have a method for sorting things and putting them in a certain order. If you have four numbers; 4,5,6, and 7; and you want to put them in order of largest odd number to smallest even number, you use a sorting algorithm. Now this seems pretty obvious; 7,5,6,4 is the answer. But how can you get a program to do this? You know the answer.

There are several algorithms for programming usage. Some are just downright complicated. I&#8217;ll show you 3 algorithms that are simple to use so you get the gist of it.

  * **Bubble Sorting Algorithm**

The Bubble Sorting Algorithm, or Bubble Sort, is one of the most simple ways to sort items. It compares 2 adjacent items together and swaps their position depending on the value of the item. The higher the value, it goes higher up. Here is an example of the Bubble Sort Algorithm:

{7, 3, 1, 9, 5, 8} is a set of numbers that needs to be ordered

{**7, 3**, 1, 9, 5, 8} Since 7 and 3 are the first two numbers in the set, they are swapped because {**3, 7**, 1, 9, 5, 8}

{3, **7, 1**, 9, 5, 8} Since 7 and 1 are the next two numbers in the set, they are swapped because 1<7 {3, **1, 7**, 9, 5, 8}

{3, 1, **7, 9,** 5, 8} Since 7 and 9 are the next two numbers in the set, they aren&#8217;t swapped because 7<9

{3, 1, 7, **9, 5,** 8} Since 9 and 5 are the next two numbers in the set, they are swapped because 9>5 {3, 1, 7, **5, 9**, 8}

{3, 1, 7, 5, **9, 8**} Since 9 and 8 are the next two numbers in the set, they are swapped because 9>8 {3, 1, 7, 5, **8, 9**}

This isn&#8217;t finished because 7 is before 5 and 3 is before 1. So the process repeats itself:

{**3, 1**, 7, 5, 8, 9} Since 3 and 1 are the next two numbers in the set, they are swapped because 3>1 {**1, 3**, 7, 5, 8, 9}

{1, 3, **7, 5,** 8, 9} Since 7 and 5 are the next two numbers in the set, they are swapped because 7>5 {1, 3, **5, 7**, 8, 9}

The rest is unnecessary but you have to program it. Look at this picture I got off of wikipedia to explain all of the stuff I just wrote.

<div id="attachment_1308" style="max-width: 310px" class="wp-caption aligncenter">
  <a rel="attachment wp-att-1308" href="/2011/06/19/understanding-sorting-algorithms/bubble-sort-example-300px/"><img class="size-full wp-image-1308" title="Bubble-sort-example-300px" src="/wp-content/uploads/2011/06/Bubble-sort-example-300px.gif" alt="" width="300" height="180" /></a>
  
  <p class="wp-caption-text">
    Observe
  </p>
</div>

  * **Selection Sort**

Selection Sort is a very simple algorithm. But very inefficient. What it does is it searches through the entire list of items, finds the smallest value, and swaps it with the first item. It the finds the second smallest value and swamps it with the second item. And that is all that happens. Look at the following picture (from Wikipedia) and see how it works.

<div id="attachment_1309" style="max-width: 110px" class="wp-caption aligncenter">
  <a rel="attachment wp-att-1309" href="/2011/06/19/understanding-sorting-algorithms/selection-sort-animation/"><img class="size-full wp-image-1309" title="Selection Sort" src="/wp-content/uploads/2011/06/Selection-Sort-Animation.gif" alt="" width="100" height="371" /></a>
  
  <p class="wp-caption-text">
    It is Slower than Most Other Algorithms
  </p>
</div>

  * **Bogus Sort**

This is a very amusing sorting algorithm. It almost impossible to use. An example of using the Bogus Sort is checking a deck of cards or list of numbers. If they are in order from smallest to largest or however they are supposed to be, nothing happens. If they are not in order, and even if there are just 2 items misplaced, you throw the entire stack of numbers or deck of cards all over the place. That&#8217;s right. You throw them all over the place. You collect the cards or numbers, and see if they are in order. If they aren&#8217;t, you repeat the process. Eventually they will be in order, but after a maximum of (n-1)n! (if using a stack of numbers) or 52! if using the deck of cards. As you can see, Bogus Sort deserves its name.

I hope you now have a better grasp of Sorting Algorithms. Enjoy!
