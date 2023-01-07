# EC2 Placement Groups

There are three different types of placement groups: cluster, spread, and partition.

Using these placement groups, we can influence how our EC2 instances are placed on the physical hardware AWS provides.

## Cluster Placement Groups

**Cluster Placement Groups (CPGs)** pack instances close together. This type of placement group is ideal for peak performance.

EC2 instances are placed in the same rack, and often even share the same host. This close physical proximity allows for all members to have direct connections with each other and extremely low latency.

The downside, is that CPGs offer little resilience because they locate EC2 instances so close together.

CPGs can’t span AZs, they are restricted to one AZ only and that AZ is locked in when launching the first instance.

CPGs can span VPC peers, but this does impact performance.

CPGs require a supported instance type, and it’s recommended that we use the same type of instance (though this isn’t mandatory).

It’s also highly recommended that all of the instances inside of a CPG are launched at the same time (though again, this isn’t mandatory).

## Spread Placement Groups

**Spread Placement Groups (SPGs)** keep instances separated.

There is a limit of 7 instances per AZ because of infrastructure limits. In essence, each instance runs from a different rack and there’s only so many distinct racks of hardware in each AZ.

SPGs are not supported for dedicated instances or hosts.

SPGs are ideal for when we have a small number of critical instances that need to be kept separated from each other.

## Partition Placement Groups

**Partition Placement Groups (PPGs)** arrange our EC2 instances in such a way that instances can be simultaneously grouped and spread apart.

PPGs are similar to SPGs, except for the fact that PPGs utilize partitions. Partitions are similar to SPGs in that each partition runs from a different rack, and there is a maximum of 7 partitions per AZ.

The difference, however, is that each partition can contain multiple EC2 instances. Instances can be placed in a specific partition of our choice, or we can allow AWS to auto place them.
