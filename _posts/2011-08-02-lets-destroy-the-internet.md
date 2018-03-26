---
id: 2221
title: 'P versus NP &#8211; Destruction of the Internet'
date: 2011-08-02T05:08:26+00:00
author: Nikhil Palanki
layout: single
guid: /?p=2221
permalink: /2011/08/02/lets-destroy-the-internet/
image: /wp-content/uploads/2011/08/pnp.png
categories:
  - How To
tags:
  - algorithms
  - destroy the internet
  - how to become rich
  - how to hack
  - non-deterministic time
  - p versus np
  - richard elwes
---
You are going to look at me like I&#8217;m crazy, but hypothetically one could destroy the internet. All one would have to do was solve the P versus NP problem (which is borderline paradoxical) a certain way and you could bypass any single security on the internet.

**How does one solve P versus NP?**

First we need to understand exactly what an algorithm is. If you know, then you can skip my next stupid question. If you don&#8217;t, then check it out.

**Algorithms**

An algorithm is a confined process of completing a mathematical or non-mathematical problem. Some conditions of the algorithm is that it cannot have any errors or be too arbitrary when completed properly.

Ex)

The Euclidean Algorithm is used to find the Greatest Common Factor of 2 numbers.

  1. The numbers are 455 and 900
  2. Subtract the smaller integer from the larger one
  3. 900-455 = 445
  4. You now have the two numbers of 455 and 445
  5. Then subtract 445 from 455
  6. The answer is 10.
  7. Take 445 and subtract 10 from it
  8. Your answer is 435
  9. Take 435 and continuously subtract 10 from it until you get a number lower than 10.
 10. That number will be 5.
 11. Subtract 5 from 10. You&#8217;ll get 5.
 12. If you subtract 5 from 5, you&#8217;ll get 0.
 13. This means 5 is the greatest common factor of 455 and 900.
 14. Check it out yourself.

That is how an algorithm would work.

**Time Complexity**

Programming&#8217;s most jumbled aspect is the Time Complexity. How fast can a program go in its worst case scenario? How about its best case scenario? How about average? This is all very convoluted.

What you need to know is that Time isn&#8217;t counted 1 second, 2 second&#8230; It is counted just using numbers. No units.

So what are the 2 times used in P versus NP? Polynomial and Non-Deterministic.

**Polynomial Time &#8211; Fast and Easy
  
** 

Let&#8217;s say I write a program that adds 2 numbers together. We know that the maximum amount of numbers that can be added in this situation is. So this makes the time at which the program travels at, x^2. 2 is the constant of the equation and x is the number of pieces of data being used. If we want to add 3 numbers together, the equation becomes 3^2 = 9. Small amount of time, huh? Even if we want to add 100 numbers together, we&#8217;ll still only get 10,000, which is less than a second&#8217;s work for a computer. Needless to say, Polynomial Time is the fastest type of time the computer could use.

**
  
Non-Deterministic Polynomial Time &#8211; Slow to Do, Fast to check
  
** 

This is what NP stands for. An example of this time is the Subset Problem. Let&#8217;s take a subset of 5 numbers {5, -1, 1, 4, -4}. In this problem, we wish to know whether or not the sum of some of the integers equals 0. The obvious answer is yes. (-4) + (4) = 0 would be the stupidly simple answer. But for a computer, the computer has to check each answer by taking the 5, adding it to -1&#8230;So on and so forth. The factorial of this subset is 120, so the computer has to check the subset 120 times. But how does the computer check? It just adds the numbers up, to see whether or not it equals 0. If the numbers equal 0, then the process to determine if it is equal to 0 is called a witness.

WAIT! The process of adding the numbers to create the witness! It is in Polynomial Time! This makes another theorem proven correct. All problems in NP (that answer to be yes)  has to have  been checked using P. If a problem in NP answers to be no, then it doesn&#8217;t have to be checked using P.

**P versus NP**

So what is P versus NP? It is a question theorized by Stephen Cook in 1971. P versus NP asks &#8220;can problems that are checked easily, be solved easily too?&#8221; Well we know problems in NP cannot be solved easily but can be checked easily. And we know that questions in P can be both solved and checked easily. This makes the simple answer &#8220;no.&#8221; No, P is always faster than NP, and NP is never equal to P.

The problem is how do you prove your answer equals no? How do you prove that P will never be slower than NP? How do you prove computers cannot ever solve problems that are in NP faster than they can solve problems in P? If you can prove it, though, the Clay Mathematics Institute offers a prize of $1,000,000 to who ever proved it.

**Significance**

Now you are wondering how to destroy the internet. This is very hypothetical as most people believe P to be faster than NP. But what if P _is_ slower than NP? This would be catastrophic:

If I could write a program that uses NP to be faster than P, that is supposed to hack past firewalls, I could get into any account. See, accounts are nothing but number/letter combinations. But these combinations has a maximum different type of letters, and a maximum length of password. For example; The code for a billionaire&#8217;s bank account is a 11-digit code. Since there are 10 different possible numbers, this makes the permutation for the number of combinations is 11! or 11 x 10 x 9 x 8 x 7 x 6&#8230; This would take the computer quite some time to figure out. But since NP is faster than P, one could compute this in the time it takes one to compute 2 +2 =4. This could be very disastrous to the world.

And since the internet is just interconnected, this&#8217;ll be happening if NP is faster than P. But thankfully, most people accept P to be much faster than NP, and computers that can check their problems quickly, can not necessarily solve them quickly.

&nbsp;

Sources:

_Mathematics_ by Richard Elwes

www.wikipedia.org

&nbsp;
