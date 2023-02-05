# Launch Configuration & Launch Templates

LCs and LTs allow us to define the configuration of EC2 instances in advance. Some configuration options include:

- AMI, Instance Type, Storage, and Key pair
- Networking and Security Groups
- Userdata and IAM Role

Neither LC nor LT are editable. They are defined once. LC do not have versions, but LT do have versions.

LT are a superset of LC and provide newer features such as placement groups, capacity reservations, and elastic graphics.

While both LC and LT can be used with Auto Scaling Groups (ASG), LT can also be used to launch EC2 instances directly via the console UI/CLI.
