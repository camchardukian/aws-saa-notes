# Default Virtual Private Cloud

## Amazon VPC Basics

- An Amazon VPC allows us to launch AWS resources into a virtual private network that we've defined.

* A VPC exists within one account and one region.

* VPCs are configured to be private and isolated by default, though they can be configured otherwise.

* The two types of VPCs are default and custom VPCs. While there is only one default VPC per region, it's possible to have many custom VPCs in a given region.

## Default VPC Basics

- There is one default VPC per region, though it can be removed and recreated. This means that in theory, a region could be without a default VPC.

- The default VPC CIDR is always 172.31.0.0/16. CIDR is an abbreviation for _Classless Inter-Domain Routing_, an IP addressing scheme that helps to reduce the size of routing tables and make more addresses available within organizations.

* Subnets of the default VPC are assigned public IPv4 addresses.

* The default VPC has access to features such as the _Internet Gateway_ (IGW), _Security Groups_ (SGs), and _Network Access Control Lists_ (NACLs).

* It is best practice not to use the default VPC for production apps.
