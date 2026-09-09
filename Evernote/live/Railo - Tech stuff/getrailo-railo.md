---
id: "11f59453-e3ce-4738-839a-c77a32d70f6c"
title: "getrailo/railo"
notebook: "Railo - Tech stuff"
created: "2017-03-06T07:41:43+00:00"
updated: "2017-03-06T07:41:43+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# getrailo/railo

Railo-Tests

Unit Tests for Railo Server.

This Test Suite needs 
MXUnit
 to be installed (copy of the folder MXUnit in webroot) and they need at least Railo 4.1.1.000.
To write your own testcases, check out the folder "/testcase-templates", there you can find various testcase templates with readme to all of them.

Mapped Folders

To run the tests from a mapped folder, create the following two mappings in the server or web admin:

virtual:    /railo-tests
resource:   {path-of-folder}/railo-tests
primary:    Resource
inspect:    Always

virtual:    /testcases
resource:   {path-of-folder}/railo-tests/testcases
primary:    Resource
inspect:    Always

Then you can run the tests by calling Railo at /railo-tests/index.cfm, for example

http://localhost:8888/railo-tests/index.cfm
