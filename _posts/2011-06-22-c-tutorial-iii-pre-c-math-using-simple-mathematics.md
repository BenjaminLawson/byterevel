---
id: 1270
title: 'C++ Tutorial III &#8211; Using Simple Mathematics'
date: 2011-06-22T11:23:43+00:00
author: Nikhil Palanki
layout: single
guid: /?p=1270
permalink: /2011/06/22/c-tutorial-iii-pre-c-math-using-simple-mathematics/
image: /wp-content/uploads/2011/06/C++.jpg
categories:
  - C++
  - Tutorials
tags:
  - byterevel
  - c math
  - c++
  - c++ tutorial III
  - i wanna learn c++
  - pre-c math
  - simple mathematics functions
---
To understand it better, you should first be familiar with everyday C++ Math Functions. In the following tutorial, look over the following 5 examples and look at how the code changes. We&#8217;ll look at Addition, Subtraction, Multiplication, and Division.

**ADDITION**

*The Math is bolded while the rest is in regular font

<table border="0">
  <tr>
    <td>
      <table border="0" align="left">
        <tr>
          <td>
            #include <iostream></p> 
            
            <p>
              using namespace std;
            </p>
            
            <p>
              &nbsp;
            </p>
            
            <p>
              int main()
            </p>
            
            <p>
              {
            </p>
            
            <p>
              int x;
            </p>
            
            <p>
              int y;
            </p>
            
            <p>
              cout<<&#8220;Have You Ever Wanted to Add 2 Numbers? Of course! You can do that right here! Enter your first number!&#8221;;
            </p>
            
            <p>
              cin>> x;
            </p>
            
            <p>
              cout<<&#8220;Enter your second number!&#8221;;
            </p>
            
            <p>
              cin>> y;
            </p>
            
            <p>
              cout<<&#8220;The sum of the two numbers is &#8221; <strong><< x+y;</strong>
            </p>
            
            <p>
              system(&#8220;pause&#8221;);
            </p>
            
            <p>
              return 0;
            </p>
            
            <p>
              }
            </p>
            
            <p>
              &nbsp;</td> </tr> </tbody> </table> </td> </tr> </tbody> </table> 
              
              <p>
                &nbsp;
              </p>
              
              <p>
                Pretty easy, huh? All you really need to know is how to place a variable within the quotations. But that isn&#8217;t too hard is it?
              </p>
              
              <p>
                <strong>SUBTRACTION</strong>
              </p>
              
              <p>
                Our next function is subtraction and it is not any more difficult. If you must see what the code looks like, look below. Notice that you show the variables the same way you do with addition but you take out the addition sign and place a subtraction sign.
              </p>
              
              <table border="0">
                <tr>
                  <td>
                    #include <iostream>using namespace std;&nbsp;</p> 
                    
                    <p>
                      int main()
                    </p>
                    
                    <p>
                      {
                    </p>
                    
                    <p>
                      int x;
                    </p>
                    
                    <p>
                      int y;
                    </p>
                    
                    <p>
                      cout<<&#8220;Have You Ever Wanted to subtract 2 Numbers? Of course! You can do that right here! Enter your first number!&#8221;;
                    </p>
                    
                    <p>
                      cin>> x;
                    </p>
                    
                    <p>
                      cout<<&#8220;Enter your second number!&#8221;;
                    </p>
                    
                    <p>
                      cin>> y;
                    </p>
                    
                    <p>
                      cout<<&#8220;The difference of the two numbers is &#8221; <strong><< x-y;</strong>
                    </p>
                    
                    <p>
                      system(&#8220;pause&#8221;);
                    </p>
                    
                    <p>
                      return 0;
                    </p>
                    
                    <p>
                      }</td> </tr> </tbody> </table> 
                      
                      <p>
                        Not hard at all. In fact, multiplication and division are practically the EXACT SAME. Just change the sign. Look below for an example of each.
                      </p>
                      
                      <p>
                        <strong>MULTIPLICATION</strong>
                      </p>
                      
                      <table border="0">
                        <tr>
                          <td>
                            #include <iostream>using namespace std;&nbsp;</p> 
                            
                            <p>
                              int main()
                            </p>
                            
                            <p>
                              {
                            </p>
                            
                            <p>
                              int x;
                            </p>
                            
                            <p>
                              int y;
                            </p>
                            
                            <p>
                              cout<<&#8220;Have You Ever Wanted to Multiply 2 Numbers? Of course! You can do that right here! Enter your first number!&#8221;;
                            </p>
                            
                            <p>
                              cin>> x;
                            </p>
                            
                            <p>
                              cout<<&#8220;Enter your second number!&#8221;;
                            </p>
                            
                            <p>
                              cin>> y;
                            </p>
                            
                            <p>
                              cout<<&#8220;The product of the two numbers is &#8221; <strong><< x*y;</strong>
                            </p>
                            
                            <p>
                              system(&#8220;pause&#8221;);
                            </p>
                            
                            <p>
                              return 0;
                            </p>
                            
                            <p>
                              }</td> </tr> </tbody> </table> 
                              
                              <p>
                                <strong>DIVISION</strong>
                              </p>
                              
                              <table border="0">
                                <tr>
                                  <td>
                                    #include <iostream>using namespace std;&nbsp;</p> 
                                    
                                    <p>
                                      int main()
                                    </p>
                                    
                                    <p>
                                      {
                                    </p>
                                    
                                    <p>
                                      int x;
                                    </p>
                                    
                                    <p>
                                      int y;
                                    </p>
                                    
                                    <p>
                                      cout<<&#8220;Have You Ever Wanted to Divide 2 Numbers? Of course! You can do that right here! Enter your dividend number!&#8221;;
                                    </p>
                                    
                                    <p>
                                      cin>> x;
                                    </p>
                                    
                                    <p>
                                      cout<<&#8220;Enter your divisor number!&#8221;;
                                    </p>
                                    
                                    <p>
                                      cin>> y;
                                    </p>
                                    
                                    <p>
                                      cout<<&#8220;The quotient of the two numbers is &#8221; <strong><< x/y;</strong>
                                    </p>
                                    
                                    <p>
                                      system(&#8220;pause&#8221;);
                                    </p>
                                    
                                    <p>
                                      return 0;
                                    </p>
                                    
                                    <p>
                                      }</td> </tr> </tbody> </table> 
                                      
                                      <p>
                                        <strong>THE CALCULATOR</strong>
                                      </p>
                                      
                                      <p>
                                        Now I think you&#8217;re ready to see what happens when everything is laced together. Our good friend iPodnerd wrote the following program for a class he taught and was gracious enough to let us use the code. Here is the following code for a simple calculator.
                                      </p>
                                      
                                      <table border="0">
                                        <tr>
                                          <td>
                                            #include <iostream>using namespace std;&nbsp;</p> 
                                            
                                            <p>
                                              int main()<br /> {<br /> int choice;<br /> float first;<br /> float second;<br /> char quit = &#8216;n&#8217;;<br /> cout << &#8220;Welcome to The Calculator&#8221; << endl;<br /> while(quit == &#8216;n&#8217;)<br /> {<br /> cout << endl << &#8220;Type:\n&#8221;<br /> &#8220;&#8216;1&#8217; If you would like to add two numbers together\n&#8221;<br /> &#8220;&#8216;2&#8217; If you would like to subtract one number from another\n&#8221;<br /> &#8220;&#8216;3&#8217; If you would like to multiply two numbers together\n&#8221;<br /> &#8220;&#8216;4&#8217; If you would like to divide one number by another&#8221; << endl;<br /> cin >> choice;
                                            </p>
                                            
                                            <p>
                                              if(choice == 1)<br /> {<br /> cout << &#8220;\nType the first number in the equation: &#8220;;<br /> cin >> first;<br /> cout << endl << &#8220;Type the second number in the equation: &#8220;;<br /> cin >> second;<br /> cout << &#8220;The sum of &#8221; << first << &#8221; and &#8221; << second << &#8221; is &#8221; << <strong>first+second;</strong><br /> cout << &#8220;, do you want to quit? (y/n): &#8220;;<br /> cin >> quit;<br /> }<br /> if(choice == 2)<br /> {<br /> cout << &#8220;\nType the first number in the equation (the one to be subtracted from): &#8220;;<br /> cin >> first;<br /> cout << endl << &#8220;Type the second number in the equation (the one to subtract): &#8220;;<br /> cin >> second;<br /> cout << &#8220;The difference of &#8221; << first << &#8221; and &#8221; << second << &#8221; is &#8221; << <strong>first-second;</strong><br /> cout << &#8220;, do you want to quit? (y/n): &#8220;;<br /> cin >> quit;<br /> }<br /> if(choice == 3)<br /> {<br /> cout << &#8220;\nType the first number in the equation: &#8220;;<br /> cin >> first;<br /> cout << endl << &#8220;Type the second number in the equation : &#8220;;<br /> cin >> second;<br /> cout << &#8220;The product of &#8221; << first << &#8221; and &#8221; << second << &#8221; is &#8221; << <strong>first*second;</strong><br /> cout << &#8220;, do you want to quit? (y/n): &#8220;;<br /> cin >> quit;<br /> }<br /> if(choice == 4)<br /> {<br /> cout << &#8220;\nType the first number in the equation (the dividend): &#8220;;<br /> cin >> first;<br /> cout << endl << &#8220;Type the second number in the equation (the divisor): &#8220;;<br /> cin >> second;<br /> cout << &#8220;The quotient of &#8221; << first << &#8221; and &#8221; << second << &#8221; is &#8221; <<<strong> first/second</strong>;<br /> cout << &#8220;, do you want to quit? (y/n): &#8220;;<br /> cin >> quit;<br /> }<br /> }
                                            </p>
                                            
                                            <p>
                                              system(&#8220;pause&#8221;)<br /> return 0;<br /> }</td> </tr> </tbody> </table> 
                                              
                                              <p>
                                                This may have come across as intimidating but it uses simple functions. Look at it carefully and notice the following two points as you scan the code:
                                              </p>
                                              
                                              <ul>
                                                <li>
                                                  At the beginning of the entire program, everything look standard, right?  iPodnerd defined all of the variables and all that happiness. But he used floats instead of integers! What the !@#$ is a float, you ask. Well, a float is another way of looking at integers. If you have trouble understanding floats, refer to <a href="/2011/06/22/c-tutorial-ii-float-vs-int/">this</a> tutorial.
                                                </li>
                                                <li>
                                                  The rest of the code is just like the addition, subtraction, multiplication, and division segments, but all in one. He reuses the same variable to make the code more concise and easier to follow.
                                                </li>
                                              </ul>
                                              
                                              <p>
                                                That wasn&#8217;t so hard was it? Of course not! Next time, we&#8217;ll show you other C++ Math functions. And remember the following:
                                              </p>
                                              
                                              <ul>
                                                <li>
                                                  Addition uses &#8220;+&#8221; when adding numbers
                                                </li>
                                                <li>
                                                  Subtraction uses &#8220;-&#8221; when subtracting numbers
                                                </li>
                                                <li>
                                                  Multiplication uses &#8220;*&#8221; when multiplying numbers
                                                </li>
                                                <li>
                                                  Division uses &#8220;/&#8221; when dividing numbers
                                                </li>
                                              </ul>
                                              
                                              <p>
                                                Happy trails!
                                              </p>
