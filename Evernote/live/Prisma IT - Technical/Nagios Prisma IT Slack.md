---
id: "1f165abf-1c2a-4053-b323-766bb24f3bca"
title: "Nagios | Prisma IT Slack"
notebook: "Prisma IT - Technical"
created: "2015-05-21T08:07:20+00:00"
updated: "2015-05-21T08:07:20+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# Nagios | Prisma IT Slack

Prisma IT Slack

   

    

   

  
 
  
 Use of the Nagios integration requires installing and configuring our Nagios plugin. To do so, follow these steps:
  
Install the necessary perl modules with: 
sudo apt-get install libwww-perl libcrypt-ssleay-perl
 (or similar)
Download the plugin and move it into place: 
wget https://raw.github.com/tinyspeck/services-examples/master
agios.pl
cp nagios.pl /usr/local/bin/slack_nagios.pl
chmod 755 /usr/local/bin/slack_nagios.pl
Edit the 
slack_nagios.pl
, find the 
$opt_domain
 and 
$opt_token
 variables, and set them to:
my $opt_domain = "prismait.slack.com"; # Your team's domain
my $opt_token = "6wvqlXzVdwnaAWsi9d2bM41f"; # The token from your Nagios services page
 
Configure Nagios to use the plugin by creating a 
slack_nagios.cfg
 file alongside the rest of your Nagios configs. Ours happens to be in 
/etc/icinga/
. Start with the following content:
define contact {
      contact_name                             slack
      alias                                    Slack
      service_notification_period              24x7
      host_notification_period                 24x7
      service_notification_options             w,u,c,r
      host_notification_options                d,r
      service_notification_commands            notify-service-by-slack
      host_notification_commands               notify-host-by-slack
}

define command {
      command_name     notify-service-by-slack
      command_line     /usr/local/bin/slack_nagios.pl -field slack_channel=#alerts
}

define command {
      command_name     notify-host-by-slack
      command_line     /usr/local/bin/slack_nagios.pl -field slack_channel=#ops
}
 Customize the 
slack_channel
 command options to specify the channel(s) where you would like alerts to be sent.
Tell Nagios to use your new Slack contact group by editing your Nagios 
contacts.cfg
 file (ours was in 
/etc/icinga/conf.d/
). Look for the "admins" contactgroup and add 
slack
 as a member. Like so:
define contactgroup {
  contactgroup_name admins
  alias             Nagios Administrators
  members           root,slack
			}
 
For Nagios XI, ensure that 
enable_environment_macros=1
 is set in your main 
nagios.cfg
 file (it may already be enabled).
For older versions and Nagios Core, you'll need to pass the variables as so:
define command {
	command_name notify-service-by-slack
	command_line /usr/local/bin/slack_nagios.pl -field slack_channel=#alerts -field HOSTALIAS="$HOSTNAME$" -field SERVICEDESC="$SERVICEDESC$" -field SERVICESTATE="$SERVICESTATE$" -field SERVICEOUTPUT="$SERVICEOUTPUT$" -field NOTIFICATIONTYPE="$NOTIFICATIONTYPE$"
}

define command {
	command_name notify-host-by-slack
	command_line /usr/local/bin/slack_nagios.pl -field slack_channel=#ops -field HOSTALIAS="$HOSTNAME$" -field HOSTSTATE="$HOSTSTATE$" -field HOSTOUTPUT="$HOSTOUTPUT$" -field NOTIFICATIONTYPE="$NOTIFICATIONTYPE$"
}

 
Restart Nagios and wait for some alerts! (Or intentionally cause some alerts -- we're not picky.)
