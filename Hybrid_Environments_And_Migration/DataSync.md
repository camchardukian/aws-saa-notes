# AWS DataSync

AWS DataSync is a data transfer service that can transfer large scale data (large amounts of data or high quantity of files) to and from AWS.

DataSync keeps metadata (e.g. permissions/timestamps) and also has built in data validation so that you can confirm your data post-transfer matches the original data.

Schedules can be set to ensure the transfer of data occurs during or outside of specific time periods.

AWS DataSync Agents are software used to read or write to on-premises data stores using NFS or SMB.

Agents run on a virtualization platform such as VMWare and communicate with AWS DataSync Endpoints.
