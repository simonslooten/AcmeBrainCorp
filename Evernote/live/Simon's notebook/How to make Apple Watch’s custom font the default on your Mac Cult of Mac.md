---
id: "87599033-ecb1-49d0-a12b-a3c300d1e459"
title: "How to make Apple Watch’s custom font the default on your Mac | Cult of Mac"
notebook: "Simon's notebook"
created: "2014-11-20T08:54:07+00:00"
updated: "2014-11-20T08:54:07+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# How to make Apple Watch’s custom font the default on your Mac | Cult of Mac

How to make Apple Watch’s custom font the default on your Mac
Buster Hein
 (12:02 pm PDT, Nov 19th)
Apple took the wraps of WatchKit yesterday and revealed an entirely new font created just for Apple Watch called San Francisco. Designers are heaping praise on the sexy new typeface that condenses at larger sizes to take up less space, and becomes easier to read at smaller sizes, but we can’t help but wish it was coming to OS X soon.
For those that can’t wait to interact with San Francisco on the Apple Watch there’s good news though: A
 developer named Wells Riley
 has released a bundle on GitHub that swaps Yosemite Helvetica Neue system font for Apple’s new Sans Serif creation.
To make San Francisco your Mac’s system font, follow these steps:
Download the zipped font files 
here
.
Copy the 6 font files to /Library/Fonts on your Mac.
Open Terminal and enter the command “sudo chown root:wheel /Library/Fonts/System\ San\ Francisco*”
Repair Disk Permissions by entering ‘diskutil repairPermissions /’
Log out and log back in to apply the changes.
If you want to go back to Yosemite’s default font, go to /Library/Fonts and delete the 6 files, starting with System San Francisco. Log out and log back in to see the changes applied.
7 comments
Related
More from Cult of Mac
Powered by
