---
id: "ced22b63-e220-4b18-afdd-0801fbb9ed2d"
title: "AWS re:Invent Keynote Summaries « Greg Arnette"
notebook: "AWS"
created: "2014-11-16T22:04:51+00:00"
updated: "2014-11-16T22:12:55+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# AWS re:Invent Keynote Summaries « Greg Arnette

AWS re:Invent Keynote Summaries

            
			
				
Keynote 1 – Andy Jassy

TL;DR summary:

Andy Jassy announced 8 new services in the opening keynote. The AWS SVP said “the new normal is that security and compliance are becoming reasons customers are moving to the cloud.” It used to be security and compliance were reasons to stay out of the cloud. Complete 180 in prior 5 years.

Theme: AWS has already won the hearts and minds of startups and ISVs

New focus… What does the “enterprise” need to embrace the cloud?

Day 1 Keynote revealed these 8 new enterprise focused features

Amazon Aurora

Super fast, resilient SQL as a service. $.29 cents an hour. This is an attack on Oracle. 11’9s reliable, 5x faster than existing MySQL on AWS.

AWS Key Management Service

Multi-faceted fully managed encryption key service with automatic key rotation, auditing, and compliance certifications.

AWS Config

Track and “scenarioize” config changes before implementing. Very important for enterprises which are accustomed to on-premises ITIL tools and need cloud equivalents.

AWS CodeDeploy, CodeCommit and CodePipelines 
&
 Apollo

A suite of internal tools AWS has been using for 19 years now available for free to help enterprise developers more efficiently adopt new innovation practices and increase agility. “Agility” was a theme mentioned over and over. Cloud is more than low cost, it’s an agility amplifier.

AWS ServiceCatalog

Enterprises want to publish internal catalogs of approved IT cloud services and want internal groups to be self-sufficient. This service helps in that area.

Think of this as the “corporate portal to cloud.”

Amazon / AWS  Core Values (a couple of the dozen) cited in keynote:

Work backward from customer… and really mean it… don’t pay lip service to this mantra

This also means basically ignore competitors, unless customers tell you they need something a competitor is already doing.

Pioneer 
&
 Invent new technologies for the long-term

Legacy IT vendors have lost their innovation gene… AWS fills the void.

Keynote 2 – Werner Vogels

TL;DR summary:

No direct price cuts… but new features that will allow customers to save money over the long-run.

One new EC2 instance type… the C4… Optimized for CPU speed with 36 virtual cores and custom designed by Intel for AWS. Sonian can evaluate if C4 types are a better ROI for some of our workloads.

EBS volumes can now be as large at 16 terabytes. Previous limit was 1 terabyte.

EC2 Container Service makes running Docker on AWS easier than roll-your-own container orchestration framework. Adopting a container strategy allows application portability between clouds or on-premises environments. This will help Sonian deploy containers on AWS, saving DevOps time.

AWS Lambda… new service abstracts away the infrastructure underneath application code. This is “game changer” for new applications created specifically for AWS. Developers can create robust applications (web, mobile, batch) and not have to deal at all with servers or storage. No DevOps. Developers write code, upload to Lambda, and AWS automatically runs the applications when triggers occur; such as a user uploading an image to S3, or clicking a button in a mobile app. Promising millisecond response time to a trigger. This turns the AWS Cloud into a giant mainframe. No other cloud vendor is talking about anything like this capability.

In a way, Lambda leapfrogs containers, but also locks an application deeply into AWS, while containers offer portability across clouds.

				
				
Posted on November 14th, 2014 by 
Greg Arnette
 in 
Amazon Web Services
, 
Cloud Compute
 |   
No Comments »
