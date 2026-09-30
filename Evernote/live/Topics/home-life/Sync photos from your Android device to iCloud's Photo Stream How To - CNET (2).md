---
id: "41c3a791-7f9e-401a-9761-7cf158b07636"
title: "Sync photos from your Android device to iCloud's Photo Stream | How To - CNET"
notebook: "Default Notebook"
created: "2012-10-28T00:00:45+00:00"
updated: "2012-10-28T00:00:45+00:00"
deleted: true
body_source: "offline_search"
source: evernote-local-live
---

# Sync photos from your Android device to iCloud's Photo Stream | How To - CNET

Sync photos from your Android device to iCloud's Photo Stream
 
Have you recently switched from iPhone to Android and want to continue syncing photos with Photo Stream? It's possible.
 
 
 
 
 
 by 
Jason Cipriani
 
   
|
 July 11, 2012 1:29 PM PDT 
   
 
   

Over the last two weeks I have been thinking about switching to

Android
 for a few months in order to gain a better perspective of the differences between Android 4.1 and

iOS 6
. I can tinker and mess around with Android all I want, but unless I force myself to use it all the time, I won't truly learn the operating system. At least, that's my theory. 

So, I made a list of all the things I use on iOS/OS X and started looking for a way to replicate it on Android. One of the items on my list was Photo Stream. I use Photo Stream every day. It's a quick and easy way to access all of my photos from any device at any time. 

The 
Dropbox Camera Upload feature on Android
 seemed to be part of the solution for me, but I'd have to manually import screenshots and photos into iPhoto, or save them to my camera roll on my

iPad
 in order to get them into Photo Stream. Sure, I could just browse photos through the Dropbox app, but I'd still end up saving them to my Camera Roll if I wanted to edit or do anything with them. It was an unnecessary step. 
 
So I began looking for ways to automatically monitor the Camera Uploads folder on my Mac, and any time a new photo was added have it imported into iPhoto. I found Automator to be the answer. Now, with a simple Automator action, any time a new photo is placed in my Camera Uploads folder, iPhoto automatically imports it and uploads it to Photo Stream. Seamless.
 
Here's how you can set up the same action for yourself. (This guide assumes you already have the 
Dropbox app
 installed and set up on your Android device with the Camera Uploads feature enabled.)

Open Automator. It's located in your Applications folder. 

(Click to enlarge)

(Credit:
Screenshot by Jason Cipriani/CNET)

 
Select Folder Action from the list of options.

(Click to enlarge)

(Credit:
Screenshot by Jason Cipriani/CNET)

 
At the top, you'll be asked to designate a folder for the action to monitor. Click on Choose Folder and navigate to your Dropbox Camera Uploads folder. 

(Click to enlarge)

(Credit:
Screenshot by Jason Cipriani/CNET)

 
Once that's done, click on the Show Library option in the top-left corner of the screen. Instead of scrolling through all of the options to find the import to iPhoto option, just type iPhoto into the search bar. Then drag the action "Import Files into iPhoto" from the list to the blank area on the right. 

(Click to enlarge)

(Credit:
Screenshot by Jason Cipriani/CNET)

 
Your action should now look like the one above. We will be monitoring the Camera Uploads folder and importing files into iPhoto. If there is a specific event you'd like the photos imported into, change the setting in the import action. 
 
Next, you'll need to save the action we just created. Go to File > Save and give it a name you'll remember. After saving the action, quit Automator. 
Now, we need to test it. Take a photo on your Android device and then watch as Dropbox updates on your Mac, then as iPhoto opens and imports the photo. Pretty sweet, right? Of course, this means your Mac will have to be on and connected to the Internet for this to work. If you forget to leave iPhoto open, Automator will launch it automatically when action is triggered. 
 
If you have automatic upload to Photo Stream turned on in iPhoto, your photos will then be uploaded to Photo Stream after import. All in all, I can take a photo on my Galaxy Nexus and within 30 seconds or so, that same photo is on my iPad and the rest of my iCloud connected devices -- all without me doing a thing. 
 
If you change your mind and want to delete the action, you can find it in the 
~/Library/Workflows/Applications/ 
folder under user account. 
 
While this may not be an action that a lot of users will use, it's bound to help someone as much as it's going to help me.
