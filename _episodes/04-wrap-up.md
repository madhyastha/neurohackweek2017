---
title: "Wrap-Up"
teaching: 15
exercises: 0
questions:
- "What have we learned?"
objectives:
- "Recap what you've learned"
keypoints:
- "You should be familar with the AWS console"
- "You should be able to start an EC2 instance"
- "You should be able to find and log on to your EC2 instance"
- "You should be able to stop your EC2 instance"
---

## For More Information

AWS has excellent tutorials available in the
[Getting Started Resource Center](https://aws.amazon.com/getting-started/).

In particular, a more general [tutorial on launching a Linux Virtual
Machine](https://aws.amazon.com/getting-started/tutorials/launch-a-virtual-machine/)
is available. Note that to follow this tutorial before Neurohackweek
2017 using uwcloudczar credentials, you will need to make sure that your region is set to Oregon,
and you will only be able to start t2.small instances in the
neurohackweek security group. So there are a few additional steps in
this tutorial.

You will probably want to access neuroimaging data from your
instance. You can copy it to your instance using `scp`, but it is much
faster to store it in Amazon S3 and copy it there. To learn about S3,
look at the [Store and Retrieve a File with Amazon S3 tutorial](https://aws.amazon.com/getting-started/tutorials/backup-files-to-amazon-s3/)
## Summary

These exercises are intended just to get you familiar with the AWS
console and launching EC2 instances. However, there is much that we
haven't covered. You will probably need to start clusters and copy
data to and from the machine. We will discuss how to do that during
Neurohackweek and you will have ample time practice with less
restrictive credentials!

