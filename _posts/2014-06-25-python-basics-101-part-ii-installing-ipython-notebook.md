---
id: 4553
title: 'Python Basics 101 &#8211; Part II: Installing iPython Notebook'
date: 2014-06-25T09:11:50+00:00
author: Nikhil Palanki
layout: single
guid: /?p=4553
permalink: /2014/06/25/python-basics-101-part-ii-installing-ipython-notebook/
image: /wp-content/uploads/2014/06/693947_python-logo_png26f0333ad80ad765dabb1115dde48966.png
categories:
  - Programming
  - Python
  - Tutorials
tags:
  - a good python ide
  - ipython notebook
  - pycharm
  - python
---
As you get into Python, you may be looking for new Python IDE&#8217;s or looking for a text editor that satisfies your initial concerns; simplicity, effectiveness, and cost are some examples. When you are scouring for the right editor, be sure to consider the following: what will I do without this editor/IDE? Will you be more stressed when you can&#8217;t effectively debug your code? Will you be lost without an in-text editor navigation system? All of these are aspects you should consider before dropping $50+ on an IDE. While $50 is a small piece of change in the short-term, if the software you pick up is one that you don&#8217;t use, you&#8217;ll be setting a precedent in your development career: keep buying technology until something works.

For the new Python developer, [PyCharm](http://www.jetbrains.com/pycharm/) seems like the best option. IDE&#8217;s are always a good option, and for budding developers, IDE&#8217;s help when trying to figure out bugs or coding errors. Additionally, PyCharm is a beautifully styled IDE with lots of cross-language support. Plus, the layout and functionality of the IDE is pretty sophisticated, making it both visually and technically appealing. But, PyCharm carries a price tag to complement its excessive features for a new Python developer. While the new Python developer might be able to justify the use of such an IDE, he or she may be thinking that such an IDE is not suitable to his or her respective development needs.

So where does this developer go? There are free alternatives such as Eclipse + PyDev. There is even a PyCharm community edition. These are all acceptable free solutions. But, there is a simple IDE that can easily be installed and implemented using pip ([which you hopefully installed](/2014/06/24/python-basics-101-part-i-installing-pip/)). It is called iPython Notebook.

**Installing iPython Notebook**

Installing the notebook is much easier done than said. Open up Terminal/Command Prompt. If you have pip installed, you should be good to go with installing the notebook. Type the following command into Terminal/Command Prompt.

<div id="attachment_4554" style="max-width: 238px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.54.04-AM.png"><img class="size-full wp-image-4554" src="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.54.04-AM.png" alt="This command installs all ipython dependencies as well." width="228" height="20" srcset="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.54.04-AM.png 228w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.54.04-AM-180x15.png 180w" sizes="(max-width: 228px) 100vw, 228px" /></a>
  
  <p class="wp-caption-text">
    This command installs all ipython dependencies as well.
  </p>
</div>

Done! pip should install all of the iPython notebook dependencies.

**Running iPython Notebook**

To run iPython Notebook, enter the following into Terminal/Command Prompt.

<div id="attachment_4555" style="max-width: 145px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.56.49-AM.png"><img class="wp-image-4555 size-full" src="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.56.49-AM.png" alt="Screen Shot 2014-06-25 at 9.56.49 AM" width="135" height="16" /></a>
  
  <p class="wp-caption-text">
    This script will start the iPython Server
  </p>
</div>

This will begin the iPython server. If the server is successfully running, a new browser window should open up at the following address: http://localhost:8888/tree

<div id="attachment_4556" style="max-width: 575px" class="wp-caption aligncenter">
  <a href="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.58.15-AM.png"><img class="size-full wp-image-4556" src="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.58.15-AM.png" alt="This tells you where the server is running. " width="565" height="30" srcset="/wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.58.15-AM.png 565w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.58.15-AM-300x15.png 300w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.58.15-AM-180x9.png 180w, /wp-content/uploads/2014/06/Screen-Shot-2014-06-25-at-9.58.15-AM-360x19.png 360w" sizes="(max-width: 565px) 100vw, 565px" /></a>
  
  <p class="wp-caption-text">
    This tells you where the server is running. If your browser doesn&#8217;t open up http:/localhost:8888/, then you can manually enter this address in your browser
  </p>
</div>

Congratulations, you have successfully installed iPython Notebook! If you have comments or concerns, please leave them below and I&#8217;ll get back to you as soon as possible.

&nbsp;
