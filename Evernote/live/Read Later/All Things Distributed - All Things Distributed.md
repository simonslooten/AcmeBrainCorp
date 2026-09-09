---
id: "0a84b517-4786-421a-bc45-3fd94f6030a2"
title: "All Things Distributed - All Things Distributed"
notebook: "Read Later"
created: "2014-11-14T06:34:10+00:00"
updated: "2014-11-25T03:35:55+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# All Things Distributed - All Things Distributed

All Things Distributed

                        
Werner Vogels' weblog on building scalable and robust distributed systems.

                    
                
            
            
                
                    
                        
		  				

	
	

    	

			
				
When AWS launched, it changed how developers thought about IT services: What used to take weeks or months of purchasing and provisioning turned into minutes with Amazon EC2. Capital-intensive storage solutions became as simple as PUTting and GETting objects in Amazon S3. At AWS we innovate by listening to and learning from our customers, and one of the things we hear from them is that they want it to be even simpler to run code in the cloud and to connect services together easily. Customers want to focus on their unique application logic and business needs – not on the undifferentiated heavy lifting of provisioning and scaling servers, keeping software stacks patched and up to date, handling fleet-wide deployments, or dealing with routine monitoring, logging, and web service front ends. So we challenged ourselves to come up with an easy way to run applications without having to manage the underlying infrastructure and without giving up on the flexibility to run the code that developers wanted. Our answer is a new compute service called 
AWS Lambda
.

AWS Lambda
 makes building and delivering applications much easier by giving you a simple interface to upload your Node.js code directly to Lambda, set triggers to run the code (which can come from other AWS services like Amazon S3 or Amazon DynamoDB, to name a couple), and that’s it: you’re ready to go.  AWS handles all the administration of the underlying compute resources, including server and operating system maintenance, capacity provisioning and automatic scaling, code and security patch deployment, and code monitoring and logging. You can go from code to service in three clicks and then let AWS Lambda take care of the rest.

One of the most exciting aspects of Lambda is that it helps you create dynamic, event-driven applications in the cloud. Lambda is launching in conjunction with a new Amazon S3 feature called event notifications the generates events whenever objects are added or changed in a bucket, and our recently announced Amazon DynamoDB Streams feature that generates events when a table is updated.  Now developers can attach code to Amazon S3 buckets and Amazon DynamoDB tables, and it will automatically run whenever changes occur to those buckets or tables. Developers don’t have to poll, proxy, or worry about being over or under capacity – Lambda functions scale to match the event rate and execute only when needed, keeping your costs low.

Event-driven cloud computing makes it easy to create responsive applications, often without needing to write new APIs. For example, a mobile, tablet, or web application that uploads images to Amazon S3 can automatically trigger the generation of thumbnails with a few lines of code – no servers, queues, or new APIs are needed. Logs are equally easy to process – if you already use AWS CloudTrail to track API calls made to AWS services, you now can easily audit the result just by turning on S3 event notifications for the appropriate bucket and writing a few lines of JavaScript code. Data stored in Amazon DynamoDB can be automatically verified, audited, copied, or transformed with an AWS Lambda function through the new Streams feature we announced earlier this week. AWS Lambda is also launching with support for Amazon Kinesis that makes it easy to process data in a Kinesis stream...and we’re not stopping there – keep watching for more integration points between AWS Lambda and other AWS services that make it easy to respond to events of all types.

We’re excited about event-driven computing – using AWS Lambda to extend other AWS services helps developers create applications that are simple, powerful, and inherently scalable. Lambda also excels at another challenge we hear a lot from customers: Turning some library code into a scalable, secure, and reliable cloud-based backend. With Lambda, developers can upload any library, even native (“binary”) libraries, making it easy to use a few lines of JavaScript to turn a library into an AWS-operated cloud service accessible as a Lambda function. AWS Lambda’s “stateless” programming model lets you quickly deploy and seamlessly scale to the incoming request rate, so the same code that works for one request a day also works for a thousand requests a second.

As with other AWS services, AWS Lambda can be accessed programmatically using the AWS SDK, through a RESTful web service API, from the command line interface, or through the AWS Lambda console. The console lets you edit and run code directly from a browser – you can author, debug, and experiment in real time without even needing an IDE. The AWS Lambda console can also create simulated events for Amazon S3 event notifications, Amazon DynamoDB Streams, and other event sources to help you verify how your code handles events from those sources. Once you’ve created and tested your Lambda function, you can monitor its performance and activity in the AWS Lambda console dashboard or through AWS CloudWatch, including setting alarms on latency or error rates. Logs for your Lambda functions are automatically captured as AWS CloudWatch Logs.

AWS Lambda is launching as a [Preview(http://aws.amazon.com/lambda) with support for functions written in JavaScript (more languages to come) and event integration with Amazon S3, Amazon DynamoDB , and Amazon Kinesis. Preview mode lets you try all of AWS Lambda’s features with a limit on concurrent function requests. We look forward to seeing what our customers will do with AWS Lambda and the new Amazon S3 and DynamoDB event features. We’d like to hear your thoughts on our new event-driven compute service and features, so please connect directly with the product team on the AWS Lambda forum.

			
		

	

	

	
	

    	

			
				
Today, I am excited to announce the Preview of the 
Amazon EC2 Container Service
, a highly scalable, high performance container management service. We created EC2 Container Service to help customers run and manage Dockerized distributed applications.

Benefits of Containers

Customers have been using Linux containers for quite some time on AWS and have increasingly adopted microservice architectures. The microservices approach to developing a single application is to divide the application into a set of small services, each running its own processes, which communicate with each other. Each small service can be scaled independently of the application and can be managed by different teams. This approach can increase agility and speed of feature releases. The compact, resource efficient footprint of containers was attractive to sysadmins looking to pack lots of different applications and tasks, such as a microservice, onto an instance. Over the past 20 months, the development of Docker has opened up the power of containers to the masses by giving developers a simple way to package applications into containers that are portable from environment to environment. We saw a lot of customers start adopting containers in their production environments because Docker containers provided a consistent and resource efficient platform to run distributed applications. They experienced reduced operational complexity and increased developer velocity and pace of releases.

Cluster Management Difficulties

Getting started with Docker containers is relatively easy, but deploying and managing containers, in the thousands, at scale is difficult without proper cluster management. Maintaining your own cluster management platform involves installing and managing your own configuration management, service discovery, scheduling, and monitoring systems. Designing the right architecture to scale these systems is no trivial task. We saw customers struggle with this over and over.

Leveraging AWS

When we started AWS, the thinking was we could use Amazon’s expertise in ultra-scalable system software and offer a set of services that could act as infrastructure building blocks to customers. Through AWS, we believed that developers would no longer need to focus on buying, building, and maintaining infrastructure but rather focus on creating new things. Today with EC2 Container Service, we believe developers no longer need to worry about managing containers and clusters. Rather, we think they can go back to creating great applications, containerize them, and leave the rest to AWS. EC2 Container Service helps you capitalize on Docker’s array of benefits by taking care of the undifferentiated heavy lifting of container and cluster management:  we are providing you containers as a service. Furthermore, through EC2 Container Service, we are treating Docker containers as core building blocks of computing infrastructure and providing them many of the same capabilities that you are used to with EC2 instances (e.g., VPCs, security groups, etc) at the container level.

Sign up here for the Preview and tell us what you think. We are just getting started and have a lot planned on our roadmap. We are interested in listening to what features you all would like to use. Head over to 
Jeff Barr’s blog
 to learn more about how to use 
EC2 Container Service
.

			
		

	

	

	
	

    	

			
				
Automated deployments are the backbone of a strong DevOps environment. Without efficient, reliable, and repeatable software updates, engineers need to redirect their focus from developing new features to managing and debugging their deployments. Amazon first faced this challenge many years ago.

When making the move to a service-oriented architecture, Amazon refactored its software into small independent services and restructured its organization into small autonomous teams. Each team took on full ownership of the development and operation of a single service, and they worked directly with their customers to improve it. With this clear focus and control, the teams were able to quickly produce new features, but their deployment process soon became a bottleneck. Manual deployment steps slowed down releases and introduced bugs caused by human error. Many teams started to fully automate their deployments to fix this, but that was not as simple as it first appeared.

Deploying software to a single host is easy. You can SSH into a machine, run a script, get the result, and you’re done. The Amazon production environment, however, is more complex than that. Amazon web applications and web services run across large fleets of hosts spanning multiple data centers. The applications cannot afford any downtime, planned or otherwise. An automated deployment system needs to carefully sequence a software update across a fleet while it is actively receiving traffic. The system also requires the built-in logic to correctly respond to the many potential failure cases.

It didn’t make sense for each of the small service teams to duplicate this work, so Amazon created a shared internal deployment service called Apollo. Apollo’s job was to reliably deploy a specified set of software across a target fleet of hosts. Developers could define their software setup process for a single host, and Apollo would coordinate that update across an entire fleet of hosts. This made it easy for developers to “push-button” deploy their application to a development host for debugging, to a staging environment for tests, and finally to production to release an update to customers. The added efficiency and reliability of automated deployments removed the bottleneck and enabled the teams to rapidly deliver new features for their services.

Over time, Amazon has relied on and dramatically improved Apollo to fuel the constant stream of improvements to our web sites and web services. Thousands of Amazon developers use Apollo each day to deploy a wide variety of software, from Java, Python, and Ruby apps, to HTML web sites, to native code services. In the past 12 months alone, Apollo was used for 50M deployments to development, testing, and production hosts. That’s an average of more than one deployment each second.

The extensive use of Apollo inside Amazon has driven the addition of many valuable features. It can perform a rolling update across a fleet where only a fraction of the hosts are taken offline at a time to be upgraded, allowing an application to remain available during a deployment. If a fleet is distributed across separate data centers, Apollo will stripe the rolling update to simultaneously deploy to an equivalent number of hosts in each location. This keeps the fleet balanced and maximizes redundancy in the case of any unexpected events. When the fleet scales up to handle higher load, Apollo automatically installs the latest version of the software on the newly added hosts.

Apollo also tracks the detailed deployment status on individual hosts, and that information is leveraged in many scenarios. If the number of failed host updates crosses a configurable threshold, Apollo will automatically halt a deployment before it affects the application availability. On the next deployment, such as a quick rollback to the prior version, Apollo will start updating these failed hosts first, thus bringing the whole fleet to a healthy state as quickly as possible. Developers can monitor ongoing deployments and view their history to answer important questions like “When was this code deployed into production, and which hosts are currently running it?” or “What version of the application was running in production last week?”

Many of our customers are facing similar issues as they increase the rate of their application updates. They’ve asked us how we do it, because they want to optimize their processes to achieve the same rapid delivery. Since automated deployments are a fundamental requirement for agile software delivery, we created a new service called 
AWS CodeDeploy
.

CodeDeploy allows you to plug in your existing application setup logic, and then configure the desired deployment strategy across your fleets of EC2 instances. CodeDeploy will take care of orchestrating the fleet rollout, monitoring the status, and giving you a clear dashboard to control and track all of your deployments. It simplifies and standardizes your software release process so that developers can focus on what they do best –building new features for their customers. Jeff Barr’s blog post includes a great walkthrough of using CodeDeploy, and is a good place to start to gain a deeper understanding of the service.

AWS CodeDeploy is the first in a set of ALM services designed to help customers build a productive cloud development process. We look forward to sharing more about the internal processes and tools that Amazon uses for agile software delivery. Apollo is just one piece of a larger set of solutions. We’d like to hear about the ways that you think we can help improve your delivery process, so please connect directly with the product team on the CodeDeploy forum.

			
		

	

	

	
	

    	

			
				

I’m excited to be heading to Las Vegas in less than two weeks for our annual 
re:Invent conference
. One of the highlights for me is being able to host an extensive lineup of startup-focused events which take place at re:Invent on Thursday, November 13.

Here’s a quick peak at the startup experience this year:

Third Annual Startup Launches

I’m excited to host this event where five AWS-powered startups will make a significant, never-before-shared launch announcement on stage. Included in the announcements are special discounts on the newly-launched products—discounts only available to session attendees. And to top it all off, we’ll have a happy hour immediately following the final launch announcement!

Founders Fireside Chat

In this session I’ll sit down with leaders who have taken their startups from an idea on a cocktail napkin to known names in a matter of a few years by harnessing the possibilities of technology and AWS. Their insights and learnings apply not only to fledgling startups and future entrepreneurs, but to enterprises seeking out ways to become more agile, responsive, and dynamic in the rapid technology race. Dan Wagner, CEO of Civis Analytics, Adam Jacob, Chief Dev Officer of Chef, and Alan Schaaf, founder of Imgur will join me in this fireside chat.

CTO-to-CTO Fireside Chat

I’ll get into the mindsets of the technical leaders behind some of the most progressive and innovative startups in the world. This is your opportunity to learn what happens behind the scenes, how pivotal technology and AWS infrastructure decisions are made, and the thinking that leads to products and services that disrupt and reshape how businesses and people use technologies day to day. I’ll chat with Chris Wanstrath, CEO of Github, Andrew Miklas, CTO of Pagerduty, and Seth Proctor, CTO of NuoDB.

VC Panel Discussion

In this session you can hear what our high-powered panel of top venture capitalists have to say about trends, pleasant and unpleasant surprises, the next big things on the horizon, and emerging startup hotspots for cloud apps and infrastructure. Greylock Partners, Draper Associates, Scale Venture Partners, Madrona Venture Group, and General Catalyst Partners will join the panel.

Startup Pub Crawl

Don’t forget about Wednesday night! In preparation for the Thursday startup track, be sure to join the AWS Startup Team for a stop along the re:Invent Pub Crawl. It will be an opportunity to network with the hottest startups, enterprises, and AWS team members. Join the team at Buddy V’s on Wednesday, November 12 from 5:30-7:30 at the Grand Canal Shoppes at the Venetian.

For venue information, and detailed session schedules, please check out the 
re:Invent website
.

See you in Vegas!

			
		

	

	

	
	

    	

			
				

Today, Amazon Web Services is expanding its worldwide coverage with the launch of a new AWS region in Frankfurt, Germany. This is our 11th infrastructure region and was built to support the strong demand we are seeing in Europe and to give our customers the option to run infrastructure located in Germany. The new Frankfurt region provides low millisecond latencies to major cities in continental Europe and is also run with carbon neutral power. With the launch of the new Frankfurt region customers now also have the ability to architect across multiple regions within the European Union.

Many prominent German, and European, customers have been using AWS for quite some time already, including start-ups such as 6Wunderkinder, EyeEm, mytaxi, Onefootball, Soundcloud and Wooga, mid-market companies such as Airport Nuremburg, Euroforum, and Kärcher, and Enterprise companies such as Axel Springer, Hubert Burda Media, Kempinski Hotels, RTL, SAP, Software AG, and Talanx. These are just a small sample of the wide variety of companies that have been using AWS extensively and I know they will put the new region to good use.

In addition to a broad base of customers, AWS has a vibrant partner ecosystem in Germany that has built innovative solutions and services on AWS. Among the many local Independent Software Vendors are: SAP, Infopark, Suse, and Software AG.
With the new Frankfurt region, companies that are required to meet certain compliance, control, and data locality requirements may now be able to achieve these certifications: as with all AWS regions, customers can choose to keep their data entirely within the Frankfurt region.

You can learn more about our growing global infrastructure footprint at 
http://aws.amazon.com/about-aws/globalinfrastructure
. Please also visit the 
AWS developer blog
 for more great stories from our European customers and partners.

			
		

	

	

	
	

    	

			
				
Today, I’m thrilled to announce several major features that significantly enhance the development experience on DynamoDB. We are introducing native support for document model like JSON into DynamoDB, the ability to add / remove global secondary indexes, adding more flexible scaling options, and increasing the item size limit to 400KB. These improvements have been sought by many applications developers, and we are happy to be bringing them to you. The best part is that we are also significantly expanding the free tier many of you already enjoy by increasing the storage to 25 GB and throughput to 200 million requests per month. We designed DynamoDB to operate with at least 99.999% availability. Now that we have added support for document object model while delivering consistent fast performance, I think DynamoDB is the logical first choice for any application. Let’s now look at the history behind the service and the context for new innovations that make me think that.

NoSQL and Scale

More than a decade ago, Amazon embarked on a mission to build a distributed system that challenged conventional methods of data storage and querying. We started with Amazon Dynamo, a simple key-value store that was built to be highly available and scalable to power various mission-critical applications in Amazon’s e-commerce platform. The original Dynamo paper inspired many database solutions, which are now popularly referred to as NoSQL databases. These databases trade off complex querying capabilities and consistency for scale and availability.

In 2012, we launched Amazon DynamoDB, the successor to Amazon Dynamo. For DynamoDB, our primary focus was to build a fully-managed highly available database service with seamless scalability and predictable performance. We built DynamoDB as a fully-managed service because we wanted to enable our customers, both internal and external, to focus on their application rather than being distracted by undifferentiated heavy lifting like dealing with hardware and software maintenance. The goal of DynamoDB is simple: to provide the same level of scalability and availability as the original Dynamo, while freeing developers from the burden of operating distributed datastores (such as cluster setup, software upgrades, hardware lifecycle management, performance tuning, security upgrades, operations, etc.) Since launch, DynamoDB has been the core infrastructure powering various AWS and Amazon services and has provided more than 5 9s of availability worldwide. Developers within and outside of Amazon have embraced DynamoDB because it enables them to quickly write their app and it shields them from scaling concerns as their app changes or grows in popularity. This is why DynamoDB has been getting widespread adoption from exciting customers like AdRoll, Scopely, Electronic Arts, Amazon.com, Shazam, Devicescape, and Dropcam.

NoSQL and Flexibility: Document Model

A trend in NoSQL and relational databases is the mainstream adoption of the document model. JSON has become the accepted medium for interchange between numerous Internet services. JSON-style document model enables customers to build services that are schema-less. Typically, in a document model based datastore, each record and its associated data is modeled as a single document. Since each document can have a unique structure, schema migration becomes a non-issue for applications.

While you could store JSON documents in DynamoDB from the day we launched, it was hard to do anything beyond storing and retrieving these documents. Developers did not have direct access to the nested attributes embedded deep within a JSON document, and losing sight of these deeply nested attributes deprived developers of some of the incredible native capabilities of DynamoDB. They couldn’t leverage capabilities like conditional updates (the ability to make an insert into a DynamoDB table if a condition is met based on the latest state of the data across the distributed store) or Global Secondary Indexes (the ability to project one or more of the attributes of your items into a separate table for richer indexing capability). Until now, developers who wanted to store and query JSON had two choices: a) develop quickly and insert opaque JSON blobs in DynamoDB while losing access to key DynamoDB capabilities, or b) decompose the JSON objects themselves into attributes, which requires additional programming effort and a fair bit of forethought.

Enter Native Support for JSON in DynamoDB: Scalability and Flexibility Together at Last

The DynamoDB team is launching document model support. With today's announcement, DynamoDB developers can now use the AWS SDKs to inject a JSON map into DynamoDB. For example, imagine a map of student id that maps to detailed information about the student: their names, a list of their addresses (also represented as a map), etc.

{
      “id”: 1234,
      “firstname”: “John”,
      “lastname”: “Doe”,
      “addresses”: [
       {
            “street”: “main st”,
            “city”: “seattle”,
            “zipcode”: 98005,
            “type”: “current”,
       },
       {
           “street”: “9th st”,
           “city”: seattle,
           “zipcode”: 98005,
           “type”: “past”,
       }
       ]
}
 

With JSON support in DynamoDB, you can access the city of a student's current address by simply asking for students.1234.address[0].city. Moreover, developers can now impose conditions on these nested attributes, and perform operations like delete student 1234 if his primary residence is in Seattle.

With native support for JSON, we have unleashed the scalability and consistent fast performance capabilities of DynamoDB to provide deeper support for JSON. Now, developers do not have to choose between datastores that are optimized for scalability and those that are optimized for flexibility. Instead they can pick one NoSQL database, Amazon DynamoDB, that provides both.

Online Indexing: Improved Global Secondary Indexes

Global Secondary Index (GSI) is one of the most popular features for DynamoDB. GSIs enable developers to create scalable secondary indexes on attributes within their JSON document. However, when we initially launched GSI support, developers had to identify all of their secondary indexes up front: at the time of the table creation. As an application evolves and a developer learns more about her use cases, the indexing needs evolve as well. To minimize the up front planning, we will be adding the ability to add or remove indexes for your tables. This means that you can add, modify, and delete indexes on your table on demand. As always, you maintain the ability to independently scale your GSI indexes as the load on each index evolves. We will add the Online Indexing capability soon.

Support for Larger Items

With the document model, since you store the primary record and all its related attributes in a single document, the need for bigger items is more critical. We have increased the size of items you are able to store in DynamoDB. Starting today, you can store 400KB objects in DynamoDB, enabling you to use DynamoDB for a wider variety of applications.

Even Faster Scaling

We have made it even easier to scale your applications up and down with a single click. Previously, DynamoDB customers were only able to double the provisioned throughput on a table with each API call. This forced customers to interact with DynamoDB multiple times to, for example, scale their table from 10 writes per second to 100,000 writes per second. Starting today, you can go directly from 10 writes per second to 100,000 writes per second (or any other number) with a single click in the DynamoDB console or a single API call. This makes it easier and faster to reduce costs by optimizing your DynamoDB table’s capacity, or to react quickly as your database requirements evolve.

Mars rover image indexing using DynamoDB

We put together a demo app that indexes the metadata of NASA/JPL’s Curiosity Mars rover images. In this app, the images are stored in S3 with metadata represented as JSON documents and stored/indexed in DynamoDB.

Take a look at the application here: 
http://dynamodb-msl-image-explorer.s3-website-us-east-1.amazonaws.com/

Tom Soderstrom, IT Chief Technology Officer of NASA JPL, has made the point that leveraging the power of managed services like DynamoDB and S3 for these workloads allows NASA/JPL to scale applications seamlessly without having to deal with undifferentiated heavy lifting or manual effort. Having native JSON support in a database helps NASA developers write apps faster and makes it easier to share more data with global citizen scientists.

Look for a more detailed blog on the architecture of this application and its sample source code in the next few days!

Expanding the freedom to invent

Not only did we add these new capabilities, we have also expanded the free tier. Amazon DynamoDB has always provided a perpetual free tier for developers to build their new applications. Today we are announcing a significant expansion to the free tier. We are increasing the free storage tier to 25GB and giving you enough free throughput capacity to perform over 200 Million requests per month.  What does this mean for you as an application developer? You could build a web application with DynamoDB as a back-end and handle over 200 million requests per month, and not have to pay anything for the database. You could build a new gaming application that can support 15,000 monthly active users. You could build an ad-tech platform that serves over 500,000 ad impression requests per month. We are giving you the freedom and flexibility to invent on DynamoDB.

What does this all mean?

To sum it all up, we have added support for JSON to streamline document oriented development, enhanced the size of items you can store in tables to 400KB, and provided a faster and even easier way to scale up DynamoDB. These features are now available in four of our AWS Regions, and will be available in the remaining regions shortly. Today they are available in: US East (N. Virginia), US West (Oregon), Asia Pacific (Tokyo) region, and EU (Ireland). We also announced the ability to add or remove Global Secondary Indexes dynamically on existing tables, which will be available soon.

DynamoDB is the logical first choice for developers building new applications. It was designed to give developers flexibility and minimal operational overhead without compromising on scale, availability, durability, or performance. I am delighted to share today’s announcements and I look forward to hearing how you use our new features!

			
		

	

	

	
	

    	

			
				

    It’s an exciting time in San Francisco as the return of the
    

        AWS Loft
    

    is fast approaching. We’ve been working round-the-clock, making updates to ensure the experience is more fulfilling and educational than in June. Today
    we’re excited to announce that…

    
On Wednesday, October 1
st
, we’ll be returning to 925 Market Street! 

    The AWS Loft is all about helping you scale and grow your business by offering free AWS technical resources. You’ll have access to training including
    hands-on bootcamps and labs, and 1:1 sessions with AWS Solutions Architects. Or you can plugin, hang out, get some work done, and stick around for evening
    presentations by innovative startups and community experts.

    

        Take a look at the AWS Loft homepage
    

to see full weekly schedules, and if you see something you like,    
go here
 and start filling your calendar.

    
Hours and Location

    We’re at 925 Market Street and our doors will be open 10AM to 6PM on weekdays, with select events running until 8PM on weeknights. Be sure to check the
    calendar regularly as new evening events will be added regularly.

    
What’s Happening at the AWS Loft

    In October there will be an abundance of sessions, events, and coding activities focused on game and mobile app development. In addition, below is an
    overview of the activities taking place at the AWS Loft each week: 

    
Ask an Architect:

    You can schedule a 1:1, 60 minute session with a member of the AWS technical team. Be sure to bring your questions about AWS architecture, cost
    optimization, services and features, and anything else AWS-related. And don’t be shy—walk-ins are welcome too.

    
Technical Presentations:

    AWS Solution Architects, Product Managers, and Evangelists will deliver technical presentations covering some of the highest-rated and best-attended
    sessions from recent AWS events. Topics include Introduction to AWS, Big Data, Compute 
&
 Networking, Architecture, Mobile 
&
 Gaming, Databases,
    Operations, Security, and more.

    
AWS Technical Bootcamps

    : Limited to twenty participants, these full-day bootcamps include hands-on lab exercises using a live environment with the AWS console. Usually these cost
    $600, but at the AWS Loft we are offering them for free. Bootcamps you can register for include: “Getting Started with AWS,” “AWS Essentials,” “Highly
    Available Apps,” and “Taking AWS Operations to the Next Level.”

    
Self-paced, Hands-on Labs:

    These online technical labs are ready and waiting for walk-ins throughout the day. We’ll offer labs for beginners through advanced users on topics that
    range from creating Amazon EC2 instances to launching and managing a web application with CloudFormation. Usually $30 each, we are offering these labs for
    free in the AWS Loft.

    
Customer Speaking Events and Evening Happy Hours:

    Innovative Bay Area startups share the technical and business journeys they undertook as their ideas came to life. CircleCI, NPM, Lyft, Librato, Cotap,
    Runscope and others will be featured speakers during our evening happy hours.

    For example, join us next week in the Loft for this special event:

    
The Future of IT: Startups at the NASA Jet Propulsion Laboratory

    When: October 1, 2014 at 6:30 -8:00 PM

    Where: The AWS Pop-up Loft

    What do startups and NASA JPL have in common? You may be surprised at just how similar the Jet Propulsion Laboratory is to a startup. In this exciting talk
    from Tom Soderstrom, the Chief Innovation Officer of NASA JPL, will share the way he delivers projects in a startup environment: from seating to planning
    to delivering. You will learn the secrets of failing fast and trying lots of techniques in the quest to extend the reach of humanity. Tom will also share
    the role that Cloud Computing has played in the exploration of space in the last decade and where we are heading next. Don't be surprised to hear about the
    bold vision that NASA has set for exploration of space AND earth and how JPL plans to go about it.

    Check out the AWS Loft homepage to learn the details and
    

        see full weekly schedules
    

    .

			
		

	

	

	
	

    	

			
				

This is an extended version of an 
article that appeared in the Guardian
 today

We are rapidly entering into an era where massive computing power, digital storage and global network connections can be deployed by anyone as quickly and easily as turning on the lights.  This is the promise – and the reality – of cloud computing which is driving tremendous change in the technology industry and transforming how we do business in Europe and around the world.

Cloud computing unlocks innovation within organisations of all types and sizes. No longer do they need to spend valuable human and capital resources on maintaining and procuring expensive technology infrastructure and datacenters, they can focus their most valuable resources on what they do best, building better products and services for their customers. Europe’s fastest growing start-ups, like 
Spotify
, 
Soundcloud
, 
Hailo
, 
JustEat
, 
WeTransfer
 and 
Shazam
, through to some of the region’s largest, and oldest, enterprises, like 
Royal Dutch Shell
, 
Schneider Electric
, 
SAP
, 
BP
 and 
Unilever
, through to governments, education and research institutes, all are using cloud computing technologies to innovate faster and better serve their customers and the citizens of Europe.

According to 
a study
 from the center for economics and business research, the expected cumulative economic effects of cloud computing between 2010 and 2015 in the five largest European economies alone is around € 763 billion . Analyst firm 
IDC notes
 the cloud economy is growing by more than 20%  and could generate nearly € 1 trillion in GDP and 4 million jobs by 2020 . The change being driven by cloud computing has become so significant that many of Europe’s policy-makers are debating the best policy approaches to enable broad success with cloud computing across the continent.

The European Commission has taken a lead in this discussion and is recognising the benefit cloud has for the European economy and the role it can play in building a global competitive advantage, ongoing prosperity, and world-leading innovation for Europe’s commercial and public sectors. In 2012, the European Commission set up the 
European Cloud Partnership
 (ECP), an initiative that brings together technology leaders, cloud users, both private and public sector, and policy-makers to recommend how to establish a Digital Single Market with no walls for cloud computing in Europe. As a member of the steering board of the ECP, and someone who has been working with the European Commission on their cloud strategy for many years, I am privileged to help contribute to the collaboration on how to promote and shape cloud computing in the region.

With the recent publication of the ECP’s 
Trusted Cloud Europe
 vision, which encourages cloud adoption in the region, I wanted to give the AWS view of the ECP’s vision and define a high level approach of the elements needed to continue to drive adoption of cloud computing across Europe. I believe that many of the elements needed for cloud computing to be successful in the region focus on values that are core to all of us as Europeans. As a Dutchman, I hold European values in close regard - values such as the right to a fair and democratic society, and a strong protection of privacy and freedom. Cloud computing – done right –enables broad expression and realization of these European values, especially when combined with a business model that puts customers first. One of the key themes of the ECP’s vision document is the call for a cloud computing framework that focuses on customers and empowers Europeans. As a senior member of the Amazon team, focusing on customers is something I know well.

When Amazon launched, nearly 20 years ago, it was established with the mission to be Earth's most customer-centric company. This means giving customers’ choice - where they can find and discover anything they might want to buy online and offering the lowest possible prices - bringing products to everyone at an affordable price point. This customer focus permeates every part of the Amazon business where we will not do anything unless the customer is going to benefit directly. We also know that if we do not live up to this customer-first promise, and constantly strive to give the best service, they are free to walk away. This puts the power in their hands and constantly keeps us focused on delighting our customers.

For cloud computing to be successful in Europe, providers must hold exceeding customer needs as a core value. The easiest way to accomplish this is to put the power in the hands of the customer with no minimum or long term commitments. This means they have the freedom to walk away at any time if they don’t get the service that they expect. They also have the freedom to use as much or as little of the cloud services they want and only pay for the resources used. For too long customers have been locked in to long term service contracts, costly capital outlays that require equipment upgrades every two-three years, and expensive software licensing fees from ‘old guard’ technology vendors. Being customer focused means ridding European businesses and organizations of these handcuffs and democratizing technology so that anyone has access to the same, world-class technology services on demand. This brings large amounts of the latest technology resources, something that was previously a privilege of the world’s largest companies, into the hands of organizations of all sizes.

I have also seen some antiquated thinking attempting to undermine the important work that the ECP is doing in other ways.  We have heard calls in some corners to develop a cloud computing framework in Europe to protect the interests of ‘old guard’ technology vendors and the way that IT “used to be” procured leading to the same expensive contracts, just disguised as cloud. I disagree and think this goes against the ethos of the ECP’s focus which is that cloud computing should serve the customers and citizens of Europe, not shareholders of technology companies. Focusing on lowering prices for Europeans will boost the economy and prosperity of local businesses as more capital can be allocated to innovation -not activities that don’t differentiate businesses, such as the overhead of managing the underlying IT infrastructure. As a result of affordable cloud resources we are already seeing centres of innovation and excellence, emerging in London, Berlin, Barcelona and Stockholm that are beginning to rival Silicon Valley. If we continue to focus cloud computing on lowering the barrier of entry and cost of failure for customers we will see more companies experimenting and exploring things previously not possible.  More experimentation drives more invention and ultimately more centres of innovation appear. This is vital to Europe’s ongoing leadership in the world economy.

Finally, one of the core messages we have been taking to the ECP is the call to put data protection, ownership, and control, in the hands of cloud users. For cloud to succeed, and realise its potential, it is essential that customers own and control their data at all times. Recent news stories have brought this topic to the fore. Customers, governments and businesses, large and small alike, have concerns about the security, ownership and privacy of their data. If they are not addressed, these concerns have the potential to undermine the pervasive adoption of cloud computing and the resulting benefits to the European business community. At AWS we decided on day one to put this control in the hands of our customers. They own the data – they choose where to store the data and their data would never be moved to optimise the network. This means that European customers using the AWS Cloud can choose to keep their data in Europe. We also give customer’s tools and techniques to encrypt their data, both at rest and in transit, and manage their secret keys in such a way that it is the customer who completely controls who can access their data, not AWS or any other party. Content that has been encrypted is rendered useless without the applicable decryption keys.

For cloud technology to be successful, and fulfil its potential to fundamentally change the European digital landscape, it must benefit the many, not the few. We have seen this with the rapid rise of the internet and we will also see this with cloud computing if we put the power in the hands of the customer. We echo the ECP’s call to focus a cloud computing framework on customers and removing barriers and restrictions to adoption in order to pave the way for increased prosperity of European businesses and provide access to high quality, secure, and trustworthy cloud services across Europe.

Cloud computing is not a technology of the future, it is a technology of today. I commend the European Commission and the ECP in recognising the potential cloud computing has to be a job creator, a driver for the economy, and a catalyst of innovation across Europe. The launch of the Trusted Cloud Europe vision is an important milestone as it will help accelerate cloud adoption in the region while helping to ensure customer-focused tenants at the core of cloud provider’s strategies. European customers were amongst the first to adopt AWS cloud technologies when we launched in 2006 and we look forward to continuing to work with the customers and policy-makers, as we help more companies in Europe reach their potential through cloud computing.

			
		

	

	

	
	

    	

			
				

I'm excited to announce a 
new blog dedicated to AWS startups
. We're launching it on 
Medium
, itself a startup on AWS. I kicked off the blog with a Q
&
A with the 
Medium CTO Don Neufeld
. I really enjoyed Don's answers to my questions and there are some real gems in here for startup CTOs. Check it out.

We'll be keeping this blog fresh with other startup spotlights and good technical content so follow the collection and keep up.

			
		

	

	

	
	

    	

			
				

We launched 
Elastic Beanstalk
 in 2011 with support for Java web applications and Tomcat 6 in one region, and we've seen the service grow to 6 container types (Java/Tomcat, PHP, Ruby, Python, .NET, and Node.js) supported in 8 AWS regions around the world. The Elastic Beanstalk team spends a lot of time talking to AWS Developers, and in the last few months they've noticed a common theme in those conversations: developers tell us they're interested in 
Docker
, and ask if we are thinking about making it easy to run and scale Docker workloads in AWS.

Several weeks ago we made it simple to 
yum install
 Docker on your EC2 Instances running Amazon Linux, and today Elastic Beanstalk introduces the ability to deploy, manage, and scale Docker Containers. Along with the native Docker functionality you're used to - including log access, volume mapping, and environment variables - enjoy the automated monitoring, provisioning, and configuration of things like Elastic Load Balancing and Auto Scaling that Elastic Beanstalk provides.

Best of Both Worlds

When developers asked us to support Docker in Elastic Beanstalk they described a 'best of both worlds' scenario: they love Docker's impact on their development workflow. Packaging applications as Docker Images makes them portable, reliable, easy to share with others, and simple to test. They wanted to make it similarly easy to deploy and operate their Docker-based applications on AWS and take advantage of features like RDS, VPC, and IAM.

Now, developers can deploy their Docker Containers to Elastic Beanstalk and enjoy the deployment, management, and automation features that come with along with it, including log rotation, VPC integration, IAM Roles, and RDS (including fully-managed MySQL, PostgreSQL, Oracle, and SQL Server databases).

To get started with Docker and Elastic Beanstalk, check out this short video below or see 
Jeff's post
 for a few samples.
