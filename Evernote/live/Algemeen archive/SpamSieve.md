---
id: "0b77a3c4-db06-472e-8f10-8ab907f7950d"
title: "SpamSieve"
notebook: "Algemeen archive"
created: "2017-09-12T09:38:51+00:00"
updated: "2022-12-25T13:33:11+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# SpamSieve

https://c-command.com/spamsieve/help/how-can-i-hide-spamsiev
To hide SpamSieve’s Dock icon, enter this command in Terminal:
/usr/libexec/PlistBuddy /Applications/SpamSieve.app/Contents/Info.plist -c "Set LSUIElement 1"
To show the Dock icon again, enter this command in Terminal:
/usr/libexec/PlistBuddy /Applications/SpamSieve.app/Contents/Info.plist -c "Set LSUIElement 0"
