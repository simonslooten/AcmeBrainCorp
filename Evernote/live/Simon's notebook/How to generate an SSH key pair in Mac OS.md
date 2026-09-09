---
id: "bd9e955d-4b71-4b9a-bda0-010394d15fba"
title: "How to generate an SSH key pair in Mac OS?"
notebook: "Simon's notebook"
created: "2018-06-26T08:41:49+00:00"
updated: "2018-06-26T08:42:34+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# How to generate an SSH key pair in Mac OS?

https://www.siteground.com/kb/how_to_generate_an_ssh_key_pair_in_mac_os/
How to generate an SSH key pair in Mac OS? 
SiteGround uses key pairs for SSH authentication purposes, as opposed to plain username and password. More information on SSH keys is available 
here
.
You can generate an SSH key pair in Mac OS following these steps:
Open up the Terminal by going to Applications -> Utilities -> Terminal
In the terminal, use the following command to start the key generation
Next you will be prompted to provide the location where you want to create the private key file:

Leave this empty to create the key in the default location, which is /home/youruser/.ssh/
id_rsa. 
The public key file will be created in the very same location, and with the same name, but with the .PUB extension.
Afterwards you will be prompted to choose a password. This is the password required to use the private key.
That completes the key generation. Below is an example of the entire process:
Mac_user: 
ssh-keygen -t rsa

Generating public/private rsa key pair.

Enter file in which to save the key (/home/user/.ssh/id_rsa):

Enter passphrase (empty for no passphrase):

Enter same passphrase again:

Your identification has been saved in id_rsa.

Your public key has been saved in id_rsa.pub.

The key fingerprint is:

16:8e:e8:f2:1d:c9:b9:cf:43:9a:b3:3c:c1:1f:95:93 Mac_user
This will create a private key written to 
/home/user/.ssh/
id_rsa
 and a public key written to 
/home/user/.ssh/
id_rsa.pub
.
After that you will have to upload public key in cPanel, under 
SSH/Shell access
 and load the private key in your Terminal using the 
ssh-add 
command:
You will be asked for the passphrase of your key when loading it in the Terminal.
With the generated keys, you should now be able to connect via SSH. More information on how to connect via SSH to your SiteGround hosting account can be found below:
How to log in to my SiteGround shared account via SSH in Mac OS
How to Enable SSH for Cloud on Mac OS 
How to log in to my dedicated server via SSH in Mac OS
You find this article useful? Click here to learn more about SiteGround 
web hosting
 experts and what else we can do for you!
Measure
Measure
