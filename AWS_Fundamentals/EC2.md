# EC2 Basics

_Elastic Compute Cloud_ (EC2) is basically the default starting point in our tool box for any compute requirement in AWS.

It is an _Infrastructure as a Service_ (IaaS) that provides scalable computing power inside the AWS cloud.

EC2 is a service that's by default and one that uses VPC networking.

EC2 is AZ resilient, meaning our EC2 instance is likely to fail if the AZ its located in fails.

EC2 offers temporary data storage inside of _instance store volumes_ as well as persistent storage volumes using _Amazon Elastic Block Store_ (Amazon EBS).

## EC2 Instance Lifecycle & Billing

At a high level, an EC2 instance is composed of CPU, memory, disk, and networking.

A running instance will utilize all four of these and thus generate costs more quickly.

Stopped instances are less useful, but they are significantly cheaper as the only resource they use is the disk.

Terminated instances are the only state in the EC2 instance lifecycle that generate no charges.

## Amazon Machine Images (AMIs)

An _Amazon Machine Image_ (AMI) is a supported and maintained image provided by AWS that provides the information necessary to start an instance.

AMIs can be created from EC2 instances, or they can be used to create EC2 instances.

AMIs can be set as public, owner-only, or explicit (where only explicitly specified AWS accounts are able to use it).

AMIs also contain a boot volume. A boot volume is essentially the portion of a hard drive containing the operating system, its supporting file system, and instructions to boot the operating system.

AMIs always contain a boot volume, but they may also contain other volumes.

## Connecting to EC2 Instances

EC2 instances utilize a public key hosted on the instance paired with a private key held by us (that we’re given 1 and only 1 opportunity to download).
