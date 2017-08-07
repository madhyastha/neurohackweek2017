---
title: "What are Amazon Web Services?"
teaching: 15
exercises: 0
questions:
- "And why do we care?"
objectives:
- "Understand why we would want to use cloud computing"
- "Log on with neurohackweek credentials"
keypoints:
- AWS reduces time to science
- AWS is probably cheaper than purchasing and maintaining dedicated hardware

---

### What are Amazon Web Services?

Amazon provides a set of secure computational services (e.g. disk
space, computers) on a pay-as-you go basis. This incredibly large set
of services allows one to architect your own computer system "in the
cloud" (i.e., in remote and centralized data centers). You can create
a virtual computer system and then destroy it, paying only for the
time you use it and for the storage you occupy. In Neurohackweek we
will discuss only three or four of the thousands of services available.

### Why do we want to use cloud computing, particularly in neurohackweek?

AWS is useful for many reasons. First, you are probably used to having
your own computer, ready for you when you need it. If you
have had the experience of sharing a large cluster with others, you
know what it is like to have to submit a job and wait for it to
execute. You feel happy if it completes before you've forgotten what
you were doing. AWS takes care of the sharing and gives you the resources
that you need to complete your job on demand. You pay for the
resources that you use.

Not only does this reduce your wait time and improve strained relationships
with cluster hogging co-workers, but it is cost-effective. When you purchase
a computer, you are paying for all the time that that computer could
potentially be used (and cost of a service contract, a system
administrator, housing it, cooling it, keeping
it powered up and networked). For most analyses, you only need a small
fraction of that time. 

Practically, in neurohackweek AWS will provide you the computers and
storage that you need to conduct your analyses. We will give you
login credentials so that you can learn how to use AWS without worrying about
having to provide a credit card.


### Logging in to the AWS console using your neurohackweek credentials

Go to the web site [https://uwcloudczar.signin.aws.amazon.com/console](https://uwcloudczar.signin.aws.amazon.com/console)
You will see a login screen as follows.

![an image]({{site.root}}/fig/CloudCzarLogin.png)

For the User Name and Password, enter the
user name and password provided to you for this workshop. You will be
immediately prompted to change your password.

![an image]({{site.root}}/fig/ChangePassword.png)


At this point you will find yourself in the AWS management console.

![an image]({{site.root}}/fig/AfterLogin.png)

>## If you want to know more
>Your credentials indicate that you are an "Identity and Access
>Management" (IAM) user within the UW cloudczar account. IAM is a web
>service that allows you to create users under your account and limit
>what they can do. For example, a lab head might create IAM users for
>each of their students and staff with permissions to perform the tasks
>needed for their research. The bill, and the breakdown of who used what, can be seen by
>the lab head.
[http://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html](http://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)

{: .callout}


