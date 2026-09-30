---
id: "acc67f2d-f451-c632-7b6c-ff98c014e1a2"
title: "Untitled"
notebook: "_INBOX"
created: "2024-11-06T19:15:16+00:00"
updated: "2024-11-08T19:34:59+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# Untitled

IF(SEARCH("9 - Amsterdam";J3);"9 - Amsterdam";IF(SEARCH("10 - Haarlem";J3);"10 - Haarlem";IF(SEARCH("11 - Den Helder";J3);"11 - Den Helder";" "))) 
=IF(ISERROR(FIND("9 - Amsterdam",J3)), IF(ISERROR(FIND("10 - Haarlem",J3)), "9 - Amsterdam", "10 - Haarlem"),"11 - Den Helder")
werkend:
=IF(ISERROR(FIND("Amsterdam";J814)); IF(ISERROR(FIND("Haarlem";J814)); "Den Helder"; "Haarlem");"Amsterdam")
=IF(ISERROR(FIND("Tilburg";T2)); "s-Hertogenbosch"; "Tilburg")
