---
title: "Getting familiar with the AWS Console"
teaching: 5
exercises: 15
questions:
objectives:
- "Learn how to navigate the console to find important information"
keypoints:
- "We can add parts to the lesson, by adding more markdown files"
- "You get the picture"
---

### Orientation to the AWS Management Console

It is important to get familar with some important bits of information
on the AWS console. For reference, I've annotated the figure below
with numbers.

1. Your User name and the parent account (here, uwcloudczar) are
listed here. The arrow to the right opens a menu that lets you log
out, view your billing information, account information, and other
important things.

2. AWS has a concept of availability zones (AZs) and regions. Here,
what you see is the region (Ohio). I have no idea why UWCloudCzar
selected Ohio.  At
any rate, within the Ohio region (indeed, within each region that you
can see by the menu you can pull down with the arrow) there are multiple secretly located
and incredibly secure data centers. These are called AZs.

The main reason you care about your region is because when you start
machines or use storage, you do so in a region. Later, when you look
at what machines you have running or what storage you are using, you
need to make sure that you check each region separately by navigating
through this region menu. At this point, it is sufficient to make sure
that you do everything in a single region.

>## If you want to know more 
> Regions and AZs give provide a lot of flexibility to architect computer 
> systems that will be available even if natural disasters take out 
> power to large portions of a region. 
>
>To learn more about the differerent AZs and regions you can look at 
>AWS documentation here: 
>[https://aws.amazon.com/about-aws/global-infrastructure/] (
https://aws.amazon.com/about-aws/global-infrastructure/) 


3. Here you will see the icons for  AWS services that you have
   recently used. I've been playing around already (so much for
   staying focused and taking the screen dumps) which might mean that
   my screen looks a little different than yours at this point. This
   will constantly change for you as you use AWS.

4. If you want to access a service whose icon you don't see in (3),
   you should use the pull-down menu for AWS services. 

![an image]({{site.root}}/fig/AWSServicesOrientation.png) 

### The EC2 Dashboard

To start a virtual computer in the cloud, or an instance, you need to
find your way to the Elastic Compute Cloud (EC2) dashboard. EC2 is a
web service that allows you to start virtual computers, or instances. You can do this by clicking on the
EC2 icon under "Recently visited services" or you can choose it from
the Services menu.

You will see the dashboard shown below. Key things to observe:

1. Note your region is Ohio. The EC2 resources shown are being used in
this region. You can also have EC2 resources in other regions. You can
change the region here to look at usage of resources in other
regions, but make sure to go back to Ohio.

2. Listed here are the resources that you are using. Critically, note
   that there are two running instances. This means that I have two
   virtual machines running in the Ohio region. *Note that what you see
   may be different; these instances belong collectively to all the
   students who are users under UWCloudCzar's account.

   You are also listed as having 4 Key Pairs. Key Pairs allow you to
   access an EC2 instance.

   Finally, you have 2 security groups. A security group has rules
   that allow traffic to or from associated instances (i.e., to
   prevent break-ins).

![an image]({{site.root}}/fig/EC2Console.png) 

>## If you want to know more
> To learn more about key pairs, you can read about them:
> [http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html)
>
> To learn more about security groups, see
> [http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html)
{: .callout}
   



