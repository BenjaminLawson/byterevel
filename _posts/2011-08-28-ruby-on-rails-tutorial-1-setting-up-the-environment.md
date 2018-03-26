---
id: 2566
title: 'Ruby On Rails Tutorial 1 &#8211; Setting Up The Environment'
date: 2011-08-28T20:07:57+00:00
author: Ipodnerd
layout: single
guid: /?p=2566
permalink: /2011/08/28/ruby-on-rails-tutorial-1-setting-up-the-environment/
Hide SexyBookmarks:
  - "0"
Hide OgTags:
  - "0"
image: /wp-content/uploads/2011/08/RoR.png
categories:
  - Ruby On Rails
tags:
  - install
  - mysql
  - rails
  - ruby
  - ruby on rails
  - set-up
  - tutorial
---
[<img class="aligncenter size-full wp-image-2568" title="RoR" src="/wp-content/uploads/2011/08/RoR.png" alt="" width="150" height="194" />](/wp-content/uploads/2011/08/RoR.png)

&nbsp;

Ruby on Rails is a web-app framework that is written in the Ruby programming language. Since its release in 2004, it has quickly gained popularity in the developer community. It aims to make developing web applications easier, efficient, and fun. In order to maximize developer efficiency, it is designed so that the best ways to do things are encouraged, and other ways discouraged. Plus, it takes less code to accomplish things than in alternative frameworks.

Similar to [PHP](/2011/07/28/php-tutorial-i-about-php-installing-mamp-and-xampp/ "PHP Tutorial 1 – About PHP & Installing MAMP And XAMPP"), Rails code is run server side and can communicate with SQL databases.

Rails is open-source, and, as a result, is more stable, secure, and available. In addition, it&#8217;s completely free.

Some famous websites that run on Rails include Twitter, Hulu, Github, Groupon, Jango, and <a title="http://rubyonrails.org/applications" href="http://rubyonrails.org/applications" target="_blank">more</a>. Some of these websites, like Twitter, have found that Rails doesn&#8217;t scale very well (when you are running a web-app with millons of visitors, Rails is either too slow or too limited). Because of this, they are considering moving to alternatives.

<h1 style="text-align: center;">
  Installing On Windows
</h1>

### Install Ruby

Go to <a title="http://rubyforge.org/frs/?group_id=167" href="http://rubyforge.org/frs/?group_id=167" target="_blank">http://rubyforge.org/frs/?group_id=167</a> and download the .exe file for the latest version of Ruby. Run the installation wizard, and, on the second page of the installer, the page asking you what components you want to install, uncheck &#8220;SciTE&#8221; and check &#8220;Enable RubyGems&#8221;. Continue clicking through the defaults of the installer, and install anywhere you want.

### Install Rails

To make sure you installed RubyGems correctly, open command prompt (Start Menu -> Run, and type &#8220;CMD&#8221;) and type in &#8220;gem&#8221;. You should see a fairly long message regarding Gems. If not, try running the installer again and make sure &#8220;RubyGems&#8221; is checked. If all went well, type in &#8220;gem install rails &#8211;include-dependencies&#8221;.

### Install MySQL

Go to  <a title="http://www.mysql.com/downloads/mysql/" href="http://www.mysql.com/downloads/mysql/" target="_blank">http://www.mysql.com/downloads/mysql/</a> and choose &#8220;Microsoft Windows&#8221; in the &#8220;Select Platform&#8221; drop-down menu. Click the &#8220;.msi&#8221; download link for the version that corresponds with your version of Windows. Click the &#8220;No thanks, just take me to the downloads!&#8221; link near the bottom of the page, and click the download server nearest you. Run the installer, leaving everything default except for the &#8220;Modify Security Settings&#8221; page. Uncheck it. Next, download <a title="http://www.heidisql.com/" href="http://www.heidisql.com/" target="_blank">HeidiSQL</a>. This will provide you with a GUI for your MySQL databases.

### Download An IDE/Editor

When editing your project, you will want a text editor that is capable of understanding Ruby syntax. Having a file drawer within the app is very helpful.

There are a number of good Ruby IDE&#8217;s out there, some of the best being <a title="http://intype.info/home/index.php" href="http://intype.info/home/index.php" target="_blank">Intype</a>, <a title="http://www.jetbrains.com/ruby/" href="http://www.jetbrains.com/ruby/" target="_blank">RubyMine</a> (30-day free trial), <a title="http://www.sapphiresteel.com/spip?page=download" href="http://www.sapphiresteel.com/spip?page=download" target="_blank">Ruby in Steel</a> (60-day trial), <a title="http://www.zeusedit.com/" href="http://www.zeusedit.com/" target="_blank">ZeusEdit</a>,and <a title="E-Texteditor" href="E-Texteditor" target="_blank">E-Texteditor</a> (30-day free trial). Try &#8217;em all out and use the one you like the best. Intype and ZeusEdit are free, so use those if you don&#8217;t want to buy anything.

<h1 style="text-align: center;">
  Installing On Macintosh
</h1>

### Install Ruby & Rails

Guess what? You&#8217;re already done! Ruby and Ruby on Rails come pre-installed on the Mac OS. Apple wants to make their computers more appealing to developers, and one way they do this is by pre-installing several programming languages onto them. Your current version may be slightly outdated by now, but it should do. Updating it can pose as a major and unnecessary hassle. Plus, Linux should be used if you are serious about running Rails on a server.

### Install MySQL

Go to <a title="http://www.mysql.com/downloads/mysql/" href="http://www.mysql.com/downloads/mysql/" target="_blank">http://www.mysql.com/downloads/mysql/</a> and select &#8220;Mac OS X&#8221; in the &#8220;Select Platform&#8221; drop-down menu. Download a DMG archive that corresponds with your system.Once downloaded, open the DMG and run the .pkg that looks roughly like &#8220;mysql-5.1.58-osx10.60x86_64.pkg&#8221;. Next, double click the &#8220;MySQL.prefPane&#8221; in the DMG to install the System Preference window for MySQL that will allow you to start and stop your MySQL server. After you&#8217;ve done that, download <a title="http://www.sequelpro.com/download/" href="http://www.sequelpro.com/download/" target="_blank">Sequel Pro</a>, which will provide you with a GUI for managing your databases.

### Download An IDE/Editor

When editing your project, you will want a text editor that is capable of understanding Ruby syntax. Having a file drawer within the app is very helpful.

The best Ruby on Rails IDE out there is <a title="http://macromates.com/" href="http://macromates.com/" target="_blank">TextMate</a>. It&#8217;s not free, but they offer a 30-day trial that you should definitely take advantage of. Once your trial runs out, you can try some hopelessly inferior alternatives like <a title="http://code.google.com/p/macvim/" href="http://code.google.com/p/macvim/" target="_blank">MacVim</a>, Xcode, or <a title="http://www.activestate.com/komodo-edit" href="http://www.activestate.com/komodo-edit" target="_blank">Komodo Edit</a>.

<h1 style="text-align: center;">
  Running The Server
</h1>

Now that we&#8217;ve downloaded and installed all of the applications and libraries we need, we can create a default Rails app and view it in the browser.

### On Windows

First, we need to create our app. To do this, open up command prompt (Start Menu -> Run, and type &#8220;CMD&#8221;) and navigate to the directory on your computer where you want your projects to install. Use the commands &#8220;dir&#8221; to see the contents of the directory you are currently in and &#8220;cd&#8221; followed by the name of a folder in your current directory to navigate to that folder. I suggest simply making a folder named &#8220;rails&#8221; on the first level of your local drive and typing &#8220;cd rails&#8221;. When you are in your desired folder, type &#8220;rails helloworld&#8221;. This will create the helloworld project folder in your current directory.

While in the helloworld directory, type &#8220;ruby script/server&#8221; to start the Rails server. Go to <a title="http://localhost:3000" href="http://localhost:3000" target="_blank">http://localhost:3000</a> in your web browser, and you should see the Rails &#8220;Welcome Aboard&#8221; page. Congratulations! You&#8217;re all done setting up your Rails environment and are ready to start coding!

### On Macintosh

First, we need to create our app. To do this, open Terminal and navigate to a desired location on your system using &#8220;ls&#8221; to list all of the folders and files in your current directory, and &#8220;cd&#8221; followed by a folder name to navigate into a folder. I suggest simply typing &#8220;mkdir rails&#8221; as soon as you open terminal to make a folder called &#8220;rails&#8221; in your home directory (and then type &#8220;cd rails&#8221; to navigate into it). When you are in the folder where you want to create your project folder, type &#8220;rails helloworld&#8221; to make a folder with all of the default project files in it. When creating a project, you use the &#8220;rails projectname&#8221; command (replacing &#8220;projectname&#8221; with your project name).

Next, navigate to that folder in terminal. If you haven&#8217;t closed your Terminal window, then you should be able to get to your project folder by typing &#8220;cd helloworld&#8221;.

Now we can actually start the server. Type &#8220;script/server&#8221;.

If all went well, you should now see a &#8220;Welcome Aboard&#8221; page at <a title="http://localhost:3000" href="http://localhost:3000" target="_blank">http://localhost:3000</a> . Congratulations! You&#8217;re all done setting up your Rails environment and are ready to start coding!
