# EBS

_Amazon Elastic Block Store (Amazon EBS)_ provides block level storage volumes for use with EC2 instances. These volumes can be mounted as devices on our instances.

EBS is AZ-resilient. EBS is generally attached to a single EC2 instance (or other service) over a storage network.

EBS is persistent until a given volume is deleted. An EBS volume can be detached and re-attached between different EC2 instances without loss of data occurring.

EBS can provision volumes with different physical storage types, different sizes, and different performance profiles.

EBS is billed on a per GB basis (some extra charges may be applied for high performance volumes).

EBS replicates data within an AZ, but failure of an AZ still means failure of a volume.

## EBS Volume Types

### SSD

**General Purpose SSD (GP2)** — Good for boot volumes, low-latency interactive apps, development, and testing. Currently the default. Credit architecture.

**General Purpose SSD (GP3)** — 3,000 IOPS & 125 MiB/s. Expected to be the default in the future. Good for virtual desktops, medium sizec single instance databases such as MSSQL Server, low-latency interactive apps, development, testing, and boot volumes.

**Provisioned IOPS SSD (io1/2)** — Good for high performance, latency sensitive workloads, I-O-intensive NoSQL, and relational databases.

### HDD

**Throughput Optimized HDD (st1)** — A low-cost HDD designed for frequently accessed, throughput-intensive workloads. Good for Big Data, data warehouses, log processing.

**Cold HDD (sc1)** — The lowest-cost HDD designed for less frequently accessed workloads. Good for saving money if you have archives or other data that requires fewer scans per day.
