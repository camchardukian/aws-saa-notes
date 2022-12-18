# Security Groups

_Security Groups (SGs)_ are stateful. One weakness of SGs, however, is that they have no explicit DENY. They are only able to ALLOW or implicit DENY.

This means that SGs are not able to block specific bad actors. This is why SGs are often used with NACLs.

SGs are attached to network interfaces. In the context of AWS, _Elastic Network Interfaces (AWS ENIs)_ are virtual network cards attached to EC2 instances that help facilitate network connectivity for instances.

SGs also have some advanced features such as Logical References and Self References that are worth noting.
