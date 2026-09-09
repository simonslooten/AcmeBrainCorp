---
id: "7162861d-b39f-48ae-9e31-410fe8754c4f"
title: "Easy Mac Hacks: Run OS X applications without their Dock icon"
notebook: "Simon's notebook"
created: "2015-05-18T08:19:25+00:00"
updated: "2015-05-18T08:19:25+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# Easy Mac Hacks: Run OS X applications without their Dock icon

Easy Mac Hacks: Run OS X applications without their Dock icon

	  	  
	  	  

		  
Posted 07/14/2014 at 2:54pm 

		  
| by Cory Bohon

	  

	  
	  	  

		
1
Comment

		
 
17
 
3
 
	  

  

  

  
Every Monday we show you how to do something quick and cool using built-in OS X utilities such as Terminal, Apple’s command line application. These easy hacks can make life better and simpler, and don’t require any knowledge of coding — all you need is a keyboard to type 'em out!
You may have come accross applications that run in the menu bar without cluttering your Dock with an icon, but did you know that 
any
 OS X app can be made to work this way? Continue reading and we'll show you how.
Hide the Dock Icon
Start the process by quitting any open apps that you want to perform the trick on. Next, you must locate the app's associated .app package. Find the app itself (it's usually located in your /Applications folder), then right-click the application icon and select "Show Package Contents" from the menu.
Locate the 
Info.plist
 file in the Contents folder that appears. (To be on the safe side, you may wish to make a backup copy of the file, since altering it incorrectly could make the app inoperable.) Open the 
Info.plist
 file with the TextEdit application, then add the following two lines of XML into it:
<
key>LSUIElement
<
/key>
<
true/>
These two lines of code need to go inside the ending "
<
/dict>" that's just before the line ending with "
<
/plist>" for this trick to work. In other words, place these new statements above the last two lines; if you place them anywhere else in the file, then the hack won't work.
Save and quit the file, then open the application that you applied this hack to and you'll notice that the Dock doesn't display the app icon, saving a bit of space.
Codesigned Applications
There's one more step to the process if the developer has signed the application with an Apple Developer Certificate — and that includes all Mac App Store applications. Without this step, you'll likely get a crash when opening the app. To prevent this, you'll need to re-sign the application using the following command in the Terminal:
sudo codesign -f -s - /path_to_app/
appname.app
Replace "/path_to_app/
appname.app
" with the path and the application name that you just tweaked the 
Info.plist
 for. After doing this, press enter, and enter your password. The application will be re-codesigned and you should be able to launch the app without any issues.
Re-show the Dock Icon
To undo this change, simply re-open the "
Info.plist
" file you made the changes to and remove the two lines of XML you added. Restart the application, and the Dock icon will begin appearing again when the app is running.
Some Caveats
As with all hacks, there are a few caveats you should know when using this method to run applications:
Hiding the dock icon also disables the top menu-bar controls for the app, so unless you know the keyboard shortcuts or the app runs in single-window mode or resides in the system tray, you may want to think twice about performing this trick. Additionally, this hack may be overwritten whenever you update the application, and you will be required to perform the steps above again. Also, even though it doesn't look like it, the application is still running, and still taking up system resources. If you do this to enough apps you may notice your computer slow down a bit, and you will need to quit apps to bring the Mac back up to speed.
Cory Bohon is a freelance technology writer, indie Mac and iOS developer, and amateur photographer. 
Follow this article's author on Twitter
.
    
Tags: 
Columns
dock
Easy Mac Hack
Easy Mac Hacks
hidden
Hide
How to
icons
OS X
Terminal
Terminal 101
Mac
How-Tos
