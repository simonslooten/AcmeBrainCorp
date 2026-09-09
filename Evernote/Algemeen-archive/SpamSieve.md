---
title: SpamSieve
created: 2017-09-12T09:38:51Z
updated: 2022-12-25T13:33:11Z
tags: []
source_enex: /Users/marvin/Documents/ObsidianVault/Hermes_Team/processed/evernote/Algemeen archive.enex
notebook: Algemeen archive
author: "simon@simonslooten.com"
evernote_source: desktop.mac
---

# SpamSieve

<https://c-command.com/spamsieve/help/how-can-i-hide-spamsiev>  

  

  * To hide SpamSieve’s Dock icon, enter this command in Terminal:  
/usr/libexec/PlistBuddy /Applications/SpamSieve.app/Contents/Info.plist -c "Set LSUIElement 1"  
  

  * To show the Dock icon again, enter this command in Terminal:  
/usr/libexec/PlistBuddy /Applications/SpamSieve.app/Contents/Info.plist -c "Set LSUIElement 0"
