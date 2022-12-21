# EBS

_Amazon Elastic Block Store (Amazon EBS)_ provides block level storage volumes for use with EC2 instances. These volumes can be mounted as devices on our instances.

EBS is AZ-resilient. EBS is generally attached to a single EC2 instance (or other service) over a storage network.

EBS is persistent until a given volume is deleted. An EBS volume can be detached and re-attached between different EC2 instances without loss of data occurring.

EBS can provision volumes with different physical storage types, different sizes, and different performance profiles.

EBS is billed on a per GB basis (some extra charges may be applied for high performance volumes).

EBS replicates data within an AZ, but failure of an AZ still means failure of a volume.
