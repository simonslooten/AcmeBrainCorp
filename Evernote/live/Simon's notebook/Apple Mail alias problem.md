---
id: "6675c2d6-2206-4756-ab2c-149b3f12c162"
title: "Apple Mail alias problem"
notebook: "Simon's notebook"
created: "2014-11-27T16:57:48+00:00"
updated: "2014-11-27T16:58:09+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# Apple Mail alias problem

Close Mail.

 

Go to:

 

/Users/USERNAME/Library/Mail/V2/MailData/accounts.plist

 

Under this:

            
<
key>EmailAddresses
<
/key>

            
<
array>

                
<
string>
mail@mac.com
<
/string>

            
<
/array>

 

Type:

            
<
key>EmailAliases
<
/key>

            
<
array>

                
<
dict>

                    
<
key>alias
<
/key>

                    
<
string>
aliasmail@aliasblahblah.com
<
/string>

                    
<
key>name
<
/key>

                    
<
string>Name 1
<
/string>

                
<
/dict>

            
<
/array>

 

Save version of file.

 

Open Mail.

 

I hope this helps - it seemed to work for me.
