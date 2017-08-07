---
title: "Launching an EC2 Instance"
teaching: 15 
exercises: 0 
questions:
- "How  do we start EC2 instances"
objectives: 
- "Learn how to launch an EC2 instance and log in to it"
- "Learn how to stop this instance"
keypoints: 
- "AWS EC2 instances with a wide range of software can be started on demand"

---


### Launching an EC2 Instance

To launch an EC2 instance, you can click on the blue "Launch Instance"
button from the EC2 dashboard. This will bring up the "Step 1: Choose
an Amazon Machine Image (AMI)" dashboard as shown below.

![an image]({{site.root}}/fig/Step1AMI.png)

An AMI is a template that describes (probably most importantly) the
operating system that you wish to run and the applications that should
be installed on your instance. In other words, you can choose an AMI
that has all or most of the software that you want to use already
installed so that you don't need to struggle with complex software
configurations (unless you want to). Some of these AMIs are available
on the AWS Marketplace (see the left menu under Quick Start).

When we begin the class, you will have a lot more options for starting
instances from the AWS Marketplace. For example, the NITRC
Computational Enviroment includes all of the most popular neuroimaging
analysis tools. There is also a version  of the NITRC computational
neuroimaging environment specifically for processing the
Human Connectome Project Computational Environment. 

However, even in the Quick Start menu shown above, you have many
options. Note those that are "free tier eligible". With your
Neurohackweek credentials you will only be able to start AMIs with
this label.

Amazon Linux is maintained and optimized for AWS for use on EC2. Let
us begin by launching an Amazon Linux AMI. Choose "Select" at the
right for this image in the top row. You will now be asked to choose
an instance type.

![an image]({{site.root}}/fig/Step1AMI.png)

If you were launching a real machine, here you would make a decision
about what resources you need to run your applications. AWS provides a
list of instance types that describe the number of virtual CPUs,
memory, storage and network performance that the instance will have
when launched. We will talk more about how to make choices here in
Neurohackweek, but for now you only have permission to launch the
"t2.small" instance type in Oregon. So select the third row and
select step 3, Configure instance. 

![an image]({{site.root}}/fig/Step2Type.png)

>## If you want to know more
>You can read more about instance types
>[https://aws.amazon.com/ec2/instance-types/](https://aws.amazon.com/ec2/instance-types/).
>For neuroimaging processing, you probably will be best off with
>either the Compute Optimized or Memory Optimized types. Start with
>the Compute Optimized unless you know or learn that your application
>doesn't fit into the memory available on those instance
>types. Otherwise, if you have a GPU accelerated application, you can
>look at the Accelerated Computing instances.


For the moment, you can leave all these settings alone and move on to
step 4, "Add Storage". AWS instances can have different types of
storage (optimized for different purposes) and this storage can be
different sizes. Disks are called "Volumes". 

1. For a simple machine configuration, your default volume type will
   be "Root". This means that this volume will hold all the system
   software that you want to install, in addition to any data that you
   will be processing. You can leave this unchanged.

2. The next thing to note now is the size, which is in
   gigabytes. If you are processing a lot of data, or if your software
   install takes up a lot of space, you may need to specify a larger
   volume here. Alternatively, if you run out of space, you can resize
   the volume on the fly.

3. Note that the volume type, by default, is General Purpose
   SSD. Alternatively you can specify a type of volume, "Provisioned
   IOPs", that can support many more I/O operations (e.g. reads,
   writes) per second. You probably don't need anything too fast or
   fancy for neuroimaging applications that are good candidates for
   running in the cloud, so you can probably leave this as is.

4. This tiny, tiny check box is really important! Although with your
   neurohackweek account you don't pay anything, if you were using
   your own account, you would pay separately for the storage
   (volumes) that you use and for the AMIs that you run. This checkbox
   means that this volume will be deleted when you terminate your AWS
   instance. You probably want this behavior, so that you are not
   charged for lingering root volumes for AWS instances whose lifetime
   is over.

![an image]({{site.root}}/fig/Step4Storage.png)

Now move on to step 5, "Add Tags". Click on the "Add Tag" button.
Here you can give your AMI a name to help you find it among all the
other AMIs started by your classmates. I've done this here by typing
"Name" in the key field and "madhyastha-student-testing" (not even
using most of my 255 characters!) to associate that tag with my
instances and volumes.

![an image]({{site.root}}/fig/Step5Tags.png)

Now you can click on "Review and Launch".
You will need to review your instance launch details, but you can move
forward to Launch. Note that you will get a message saying that your
instance configuration is not eligible for the free usage tier, but
that's ok, we set it up that way.

Here you will be asked for a key pair. Recall that a key pair allows
you to access an EC2 instance. If you are following along this
tutorial for the first time you will not have an existing key
pair. You will need to choose "Create a new key pair".

Note that when you do that, you see a little blue warning telling you
that you need to download the private key file (*.pem) to a secure and
accessible location. If you don't do this, you won't be able to log on
to your instance.

Give your key pair a meaningful name  and download it to somewhere you
can find it on your computer.

![an image]({{site.root}}/fig/KeyPair.png)

