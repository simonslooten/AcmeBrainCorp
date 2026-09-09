---
id: "699a05c2-acb0-4c41-9f1b-ce5abc5a05e9"
title: "General input from mailinglist"
notebook: "Railo Roadmap"
created: "2013-11-11T15:21:32+00:00"
updated: "2014-01-09T21:40:38+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# General input from mailinglist

Check vertex.io (http://vertx.io)

If you don't want the whole platform, Vert.x can be
embedded
 as a library in your existing Java applications. 

From: 
Kai Koenig 
<
kai@getrailo.com
]]
>

Date: 
Thursday 9 January 2014 21:37

To: 
Simon Slooten 
<
slooten@prisma-it.com
]]
>

Subject: 
Fwd: [railo-team] Railo as a service

Hi Simon,

Happy New Year... just thought you might be interested in this discussion. Not sure if you're on that list and actively following it.

Cheers

Kai

Begin forwarded message:

From: 
Kai Koenig 
<
kai@getrailo.com
]]
>

Date: 
10 January 2014 9:35:43 AM NZDT

To: 
railo-team@googlegroups.com

Subject: 
Re: [railo-team] Railo as a service

Sorry for the briefness, I was just quickly responding on my phone last night.

As Mark said, Adobe did something similar for Flex and AIR. From a conceptual point of view that did seem to make sense back then because it looked like as if could be a cool way to hook into backed services really, really easily for Flex developers. There was a .swc file that you could compile/link into your Flex app and then you had access to MXML tags such as 
<
cf:mail.../> in your Flex and AIR apps. 

Did it ever take off? No. The main reason however was Adobe missing the point when it comes to market both Flex and CF and in reality the majority of Flex developers couldn't care less about CF and used something else anyway.

Why I'm against this particular idea of Railo as a service is different though. There are two thoughts:

1. As a Railo "product feature": People could use it for their own client apps to connect to some Railo "services" on their own server. Nice idea, but that's already easy. Wrap a SOAP/REST-web service call around one of the suggested tags and off you go. I don't think it's a feature that Railo should invest development time/money into to bake it into the product.

2. As a commercial Railo service (maybe on 
Railo.io
): I'm less inclined to say "No!" here, but it'd really come down to a realistic market evaluation and how/if Railo could provide a competitive service. There's a general movement towards PaaS and things like 
Backendless.com
, Windows Azure Mobile Services etc. but could a Railo offering really break into a particular or multiple of those markets and provide a better solution? Honestly, I don't know.

CFIMAGE - maybe --- competing to 
http://cloudinary.com/
 

CFDOCUMENT - an option, too, also CFPDF?

CFCHART --- now that everyone seems to be using D3.js?

CFQUERY --- that'd be the traditional 
Backendless.com
 competitor

CFSEARCH and friends --- a hosted SOLR service? Not sure if that exists.

Those are all interesting ideas, but I guess my main point is: If you're not sure you can do it really well and be a serious competitor, then don't do it.

Cheers

Kai

A bit more elaborate than Kai, but still:

should we implement Railo as a service? Where you can call Railo like a remote API? The potential candidates IMHO are:

Since I don’t see a real use case but a lot of security implications I’d say „No!“ as well.

-Stefan

-- 

You received this message because you are subscribed to the Google Groups "Railo Team" group.

To unsubscribe from this group and stop receiving emails from it, send an email to 
railo-team+unsubscribe@googlegroups.com
.

For more options, visit 
https://groups.google.com/groups/opt_out
.

From: 
Bruce Kirkpatrick 
<
skyflare@gmail.com
]]
>

Reply-To: 
"
railo@googlegroups.com
" 
<
railo@googlegroups.com
]]
>

Date: 
Thursday 20 September 2012 14:15

To: 
"
railo@googlegroups.com
" 
<
railo@googlegroups.com
]]
>

Subject: 
[railo] Re: What do you want Railo Server to be?

I don't know if I'm unique, but I prefer to write most application type features from scratch even if plugins or open source projects exist for them.   I just want a language to be fast and reliable and be able to handle the complexities of I/O in the best way for me.  However, after building a single CFML framework/application for the last 9 years, I think I've got a lot of great features in my applications that may benefit others if they were part of the railo server or extensions.  Plus there are areas where other languages are still better suited, which Railo could choose to include to be more of a swiss army knife for any server based app.

1: Add strict typing if it would improve performance. This would include adding new data type keywords/functions that are closer to the underlying data types that have to be manually cast if type must be changed.  For example, look at how javascript is starting to include new data types to enable higher performance in webgl with typed arrays, 
http://www.khronos.org/registry/typedarray/specs/latest/
    I know we can use java objects within CFML.  What I don't know is if that is faster or if array operations on a java objects are no different from a CFML array operation.   Isn't there wasted memory when you have a more generic struct/array object that can accept strings, numbers, boolean, objects, etc.  I'm asking to eliminate all that memory overhead somehow and have simple data and be able to enforce it when it is passed into CFML functions, but only if it is proven to be faster or can somehow be made into parallel code better.

2: Enable creation of socket servers via application or server scope cacheable CFML components that can outperform node.js or others - I haven't actually tested any of the early extensions compared to node.js, but it seems like there is work on websockets and maybe other extensions are in an alpha state right now which may not be done in the 4.0 release schedule.  I'd like to see those get finished to a high level of performance very soon so I can consider using railo for a low latency multiplayer game server or other real-time apps.  Ideally, make it easy to replace them while the server is running and yet still bind them to different ports.

3. enable compiling CFML into other languages.  I noticed the Haxe language lets you use strict typing to generate php or javascript, which seems like a novel idea if it is performant.  A lot of us have concerns about php vs CFML vs javascript occasionally and if you could easily switch between all of those, it would be irrelevant at that point.  It also makes debugging a little easier if a lot of the syntax is validated and enforced by another language, especially if the other language has stricter syntax.  node.js likes to claim how great it is to use one language for client side and server side.   What if you could write CFML that generates javascript for you? Or what if railo was able to compile its java classes from javascript source?  It doesn't have to use V8 like node.js, but perhaps V8 has some benefits if it was integrated.  The long-lived java server with dynamic class loading, threading and fast shared memory abilities of railo make it superior to V8 for certain things, but perhaps it is far more heavy and less suited for applications in need of asynchronous I/O currently compared to node.js.   Perhaps the new javascript version would abandon the tag concepts in favor of just a single method of writing for railo.  It is a bit annoying to have 2 types of syntax in CFML even though both are easy to understand for an experienced developer.

4. Make it possible to execute low level commands on mysql like their C api or via a new native driver perhaps which would allow asynchronous queries.  We can currently fake this using 
<
cfthread>, but perhaps a built-in option would be more memory efficient and faster.  For example in PHP, an unbufferred query with mysqlnd uses about half the memory and completes in about half the time.  I'd like to be able to set callback methods for processing all I/O.   CF/Railo has to return a complete result, turn it into an object and then you loop over that object.   I'd like to have an additional set of functions that let you setup a much more fine grained database connection for some added performance.   I often use code generation techniques to automate verbose high performance techniques.  If I had this low level api, then I would generate each query as a cfc that sits in shared memory, so that it would just have the overhead of a function call and the full performance of the low level api.

5. Make it possible for most of the I/O tags to be non-blocking via using techniques similar to how node.js handles I/O. CFHTTP, CFFTP, CFFILE, CFQUERY, etc. For example, what if 
<
cfquery> had async="yes" callback="processQuery" attributes.  We'd have to reorganize the application so that it doesn't complete a request until the last callback is done processing, but this may improve throughput under high load because I believe it is possible to put threads in a deeper sleep state after they complete their work and while they are waiting for I/O callback events.  If this was done in pure java, it might be faster when the server is under high load compared to 
<
cfthread>?   Web server developers claim they beat the C10k problem using these kinds of techniques.  The node.js guy says it better then I can on his youtube presentations about node.js architecture.  I think it is important not only for high load web servers, but also to combat DDOS attacks and abusive behavior since the more load you can handle, the less likely an attacker will be able to fully saturate the server with too many requests.  I'm always scared that the big heavy java process is going to get clobbered the first time I have a big attack.  I have a configuration that has been tested on apachebench up to 1000 simultaneous and it is stable afterwards, but it is fairly easy to crash railo with apachebench under a certain amount of load 
&
 certain memory/connection configurations.  I don't know what a real DDOS attack would do.  If there are any ways to mitigate DDOS attacks within railo, that would be a nice feature.  Railo is able to track state better since it has all those shared scopes, etc.  I already have detection for excessively fast connections and I clear out the session memory automatically when that happens and block them for a while.  For example 50 CFML HTTP requests in a minute is obviously abusive.  I also have limits set on iptables connections, tomcat and apache to help. 

6. It seems like 64 bit numbers coming from JDBC / mysql bigint columns need extra manual conversion to retain precision and this is intentional to maintain ACF compatibility.  Perhaps we could have an option on how to treat bigint columns in railo admin so that we can preserve 64-bit precision with less code.  I wanted to use 64-bit numbers via the uuid_short() function in mysql to have unique ids that are server id specific so you could have do master/master replication without worrying about unique key errors.  It is easier to handle this in other languages that are more low-level with the database access.

My applications are getting close to the point where my entire html based web site functions like a desktop app with micro ajax updates and transitions.  My company site is built on my custom CFML framework and is using a lot of the most modern techniques including html 5, pushstate,  responsive web design for the front-end.  On the server side, I have an extremely efficient custom application where nearly everything is cached in railo shared memory scopes so that there is very little disk activity.  I want my ajax requests to have the least overhead possible so it feels like a seamless / instant desktop experience, so hopefully railo will keep its request startup and execution minimal and fast as it adds more features.   You can see this in action on my company web site:  
https://www.farbeyondcode.com/

7. I don't know if 
<
cfthread> is a heavyweight method of threading, but I'm guessing it is.   What if there was a way for you to perform parallel code operations by specifying an extra option or using new parallel functions.  For example, parallel sorting,  parallel math operations to arrays/structs,  parallel function callbacks and these new functions would use more efficient lightweight/threading commands which automatically handle thread management issue and complete with a single result.  Like if we had strict typing with new data types, perhaps it would be possible to have some of the vector operations become parallelized using cpu specific optimizations for multiple data operations like SSE, SIMD, and all that intel threading / parallel stuff that is available in the C++ world.  I don't know if java can utilize these optimizations.  In languages like C#, C++, you can use special compiler keywords or libraries to take advantage of more cpu cores for data processing.  I think all of us are using 4 to 16 core servers now and the cpu is sitting close to idle all the time.  I just need requests to finish faster, not to increase scale typically.   These improvements are much more useful if you are dealing with low-latency real-time socket connections.  I realize most people don't care about 10ms for a web page, but games only have 16ms to draw a frame and achieve 60 FPS, and you user input and AI / player reactions to be as close to a single frame as possible.   I currently plan on using node.js for my game server because it is easy and fast for websocket connections, but if Railo was further along with sockets, it would be better since I have 100k lines of code in CFML already.  Maybe when I'm more successful someday, I'd have time to build a C version, but initially I'd focus on what I know.  I want to start making simple free/cheap indie web games with a multiplayer component using web technologies like flash, html 5, etc.  I like writing fast code, because I want to have skills that are useful for writing efficient game code.

8. Perhaps add tags/functions that can parse CSS, javascript and html into CFML objects or a high performance non-blocking event stream with higher performance.  This would allow server-side processing of these without the tedious character by character approach I currently use.   I have already built my own css parser and html parser using cfml and php.  I did this to create my own template language and to convert html / css into strict valid syntax.   I want to enable developers with less skill to be able to upload their code and the system will insert the dynamic sections in place of the tag language.  It will also validate their input so that it is secure and prevents them from accessing the system in ways I haven't designed.  I also generate a sprite map from the CSS data and automatically insert the background-image, background-position code back into the css file.  Here is the spritemap for my company site, which is auto-generated with my own script when the css file changes:  
https://www.farbeyondcode.com/images/zspritemap.jpg
     -  Perhaps railo could have its own template language like I'm building.  I've built mine in a way that is similar to php's smarty.   However, railo is far superior in its ability to cache a CFC in shared memory.  My templates are "compiled" to a CFC that is cached in server or application scope.  This minimizes file i/o, and eliminates the overhead of parsing my templates.  I'd want a railo version of this functionality to be able to do all that and more.  Maybe the railo team should have a separate project that is actually the most complete and powerful CFML framework ever made, rather then try to build every feature into the server in a generic way.  Maybe you could create a set of conventions and standardize CFML development for the most modern techniques.   That would allow for a lean and mean version of railo, and a more heavy-weight version for that lets you have a full framework and tools.

9. If railo understood css, javascript and html syntax, then it could add other optimizations automatically in the future.  For example, css files could be served with data-uri,  sprite maps, valid syntax/alerts automatically.   HTML could be converted from xhtml to html 5 or a future standard by changing a server side option.  This would also make it easier to write javascript with CFML, since you could build the CFML javascript object and then there would be a built-in way to write it out to javascript.   The compilation process could be integrated with google's closure or yahoo YUI and support automatic minification and concatenation of all the external js files.  I have recently built this entire system of automating minify / concat and tracking file changes automatically on my company site.  It you look at the network tab in firebug/chrome inspector, you'll see the site has very few requests.   I'm just suggesting that railo have the ability to do more of this as a built-in feature so people don't need to be expert developers to build applications that follow all of the google pagespeed recommendations.  My site is currently scoring 96 of 100 on google pagespeed insights.  I've put hundreds of hours into correcting / automating all of those pagespeed changes across my sites.   Railo could choose to not only consider the server performance, but also how to make the front-end more efficient since I've found that as I have fully optimized my railo application, the front-end has become the bottleneck - i.e. deferred execution of javascript, fewer, smaller requests,  deferred loading of elements.   Perhaps these front-end ideas can be abstracted so that there is a consistent library available for railo developers which automates these tasks if you consistently use them.  I already make CFML function to generate a lot of the HTML / javascript syntax.  I automate the load-order and placement of this code by integrating it with my template system.  You need a lot of feature to achieve all that, but it works.   For example, instead of writing 
<
script type="text/javascript" src="/myfile.js">
<
/script>,  I have a skin component that I call request.zos.skin.includeJS("/myfile.js") in railo.  I also add version ids to the filename so that the browser is forced to download the file again.    This handles all the magic of minify/concat and the position that the file appears within the html code.  It also loads the file asynchronously via appending the script tag to the dom just before 
<
/body>.  I know someone was working on 
<
cfstylesheet> and 
<
cfjavascript> tags for railo in 2010, but I don't know if they are actively developed still.  I choose to write my own so that I had the ability to implement all the features I described in the most efficient way.  I handle the concatenation by using a separate function that groups files into "packages" so that I can still include individual files and benefit from the versioning and async loading.

Railo is really great how it is right now, but I think looking at node.js and c for ideas on sockets and non-blocking i/o is going to have the biggest impact on improving  what is possible with railo.   Adding framework type features to railo is less important to me, and just makes it a more complete solution.  Also anything that can be done to make server management and achieving continuous uptime would be great.  Perhaps an easy way to manage failover / high availability / shared configuration / synchronization.  I don't fully know what is available when attempting to cluster railo, since I currently use 1 instance, but I'd hope its really good whenever I get to the point of needing it.
