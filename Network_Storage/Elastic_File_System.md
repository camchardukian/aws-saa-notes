# Elastic File System (EFS)

EFS is an AWS managed implementation of NFS, which allows for the creation of shared ‘file systems’ which can be mounted within multiple EC2 instances.

EFS can play an essential part in building scalable and resilient systems.

EFS is a private service. By default, it’s isolated to the VPC it’s provisioned into.

EFS is for Linux only.

EFS has two performance modes. _General Purpose_ which is used in almost every case, and _Max I/O_ for the rare cases where maximizing I/O is the highest priority (even if it may come at the cost of latency.
