---
id: 2627
title: How To Reformat Your USB Flash Drive
date: 2011-09-05T09:40:43+00:00
author: Ipodnerd
layout: single
guid: /?p=2627
permalink: /2011/09/05/how-to-reformat-your-usb-flash-drive/
image: /wp-content/uploads/2011/09/sandisk-4gb-flash-drive.jpeg
categories:
  - How To
tags:
  - .trashes
  - blueharvest
  - fat32
  - flash drive
  - format
  - reformat
  - thumb drive
  - usb
---
<p style="text-align: center;">
  <a href="/wp-content/uploads/2011/09/sandisk-4gb-flash-drive.jpeg"><img class="aligncenter size-full wp-image-2638" title="sandisk 4gb flash drive" src="/wp-content/uploads/2011/09/sandisk-4gb-flash-drive.jpeg" alt="" width="450" height="450" srcset="/wp-content/uploads/2011/09/sandisk-4gb-flash-drive.jpeg 500w, /wp-content/uploads/2011/09/sandisk-4gb-flash-drive-150x150.jpeg 150w, /wp-content/uploads/2011/09/sandisk-4gb-flash-drive-300x300.jpeg 300w, /wp-content/uploads/2011/09/sandisk-4gb-flash-drive-30x30.jpeg 30w, /wp-content/uploads/2011/09/sandisk-4gb-flash-drive-45x45.jpeg 45w, /wp-content/uploads/2011/09/sandisk-4gb-flash-drive-115x115.jpeg 115w, /wp-content/uploads/2011/09/sandisk-4gb-flash-drive-180x180.jpeg 180w, /wp-content/uploads/2011/09/sandisk-4gb-flash-drive-360x360.jpeg 360w" sizes="(max-width: 450px) 100vw, 450px" /></a>
</p>

I recently found the need to dig out and dust off my old USB flash drive in order to be able to transfer files between computers. Upon plugging in my flash drive, I found that there were about 300 megabytes available. That is, 300 MB of available space on my completely empty 4 GB flash drive. What the heck? How is that possible?

It turns out that there is a hidden trash folder that Mac OS X creates on the flash drive. When files are deleted on the flash drive through Finder, the files are actually moved to a hidden &#8220;.Trashes&#8221; folder on the flash drive. If you don&#8217;t empty the trash before removing your flash drive, these files will remain in this hidden folder and will take up precious storage space. Disgusting.

This problem can usually be remedied by plugging in the flash drive to a computer and emptying the Trash. If you find yourself having this trouble often, or if you work with many external storage units like flash drives and SD cards, you may want to check out a $10 application (with 30-day free trial) called <a title="http://www.zeroonetwenty.com/blueharvest4/" href="http://www.zeroonetwenty.com/blueharvest4/" target="_blank">BlueHarvest</a>. It automatically removes these hidden folders and files from your flash drives, SD cards, file servers, and more. I haven&#8217;t tried it out myself, but it has good reviews and it looks like a viable solution.

While reformatting my flash drive probably wasn&#8217;t necessary, I had a bunch of odd system files on it and I thought it would be a good idea to just delete everything and start with a brand new file system.

If you want to completely wipe your flash drive and start fresh, then you will want to reformat it. Some other reasons for doing this are

  * If you are going to sell your flash drive, then you will want to get rid of all the data on it
  * If you need to change the format of your flash drive for reasons like file size limit or usability on certain operating systems
  * The file system on your flash drive is a hopeless mess and you want to quickly and easily clean it up
  * You are having storage issues with your flash drive
  * You are having file corruption issues on your flash drive
  * To check for damaged sectors of your flash drive

<h2 style="text-align: center;">
  Reformatting A USB Flash Drive On A Mac
</h2>

  1. Plug in the flash drive to your computer
  2. Open Disk Utility (Applications -> Utilities -> Disk Utility, or search for &#8220;Disk Utility&#8221; in Spotlight)
  3. In the list of drives that are connected to your computer, select your flash drive. This should be the one that is labeled with a description of the drive rather than the name of your drive. Mine is &#8220;4.02 GB SanDisk Cruzer Media&#8221;. There should be a mounted volume that looks like a sub-drive of your flash drive.
  4. Go to the &#8220;Erase&#8221; tab
  5. Select the desired format (you probably want &#8220;Mac OS Extended (Journaled)&#8221;)
  6. Give a name for your flash drive
  7. Click the &#8220;Erase&#8230;&#8221; button
  8. Follow any on-screen instructions
  9. Give yourself a pat on the back- you&#8217;re done!

<h2 style="text-align: center;">
  Reformatting A USB Flash Drive On Windows
</h2>

  1. Plug in the flash drive to your computer
  2. Go to My Computer
  3. Right-click your flash drive and select &#8220;Format&#8230;&#8221;
  4. Select which format (&#8220;File System&#8221;) you want your flash drive to be reformatted to. You can do some research on this if you want, but you probably want to go with FAT32.
  5. Choose an allocation unit size. You probably want to leave this to the default, but if you have a large flash drive or you intend to store large files on it then you might want to increase the allocation size. Otherwise, a smaller allocation unit size might suit you better; try 512 bytes.
  6. Give your flash drive a name by typing it in the &#8220;Volume Label&#8221; box
  7. Click &#8220;Start&#8221;
  8. Click &#8220;OK&#8221; in the window that pops up
  9. Give yourself a pat on the back- you&#8217;re done!
