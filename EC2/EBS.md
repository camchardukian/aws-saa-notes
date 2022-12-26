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

## EBS Snapshots

It’s possible to back up the data on our EBS volumes to Amazon S3 using snapshots. Because snapshots are stored in S3, they are region resilient.

Snapshots are incremental, the first snapshot is a full backup and any future snapshots save only the blocks on the device that have changed since the last snapshot.

Snapshots are incremental because this minimizes the time required to create the snapshot and saves on storage costs by not duplicating data.

Each snapshot contains all of the information that is needed to restore our data (from the moment the snapshot was taken) to a new EBS volume.

Snapshots can be used to migrate data to different availability zones in a region, or to different regions of AWS.

Snapshots are billed based on allocated GB of data per month.
