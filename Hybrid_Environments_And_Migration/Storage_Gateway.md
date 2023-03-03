# Storage Gateway

Storage Gateway is a product which can be used for migrations from on-premises to AWS, extensions of a datacenter into AWS, storage tiering, disaster recovery, and replacement of backup systems.

Storage Gateway can be used in Volume, Tape, and File modes.

## Storage Gateway - Volume

Storage Gateway Volume mode can be run in one of two sub-modes.

### Volume Stored

All data is stored locally. This mode is great for ‘full disk’ backups of servers.

This mode is great for disaster recovery because it can be used to create EBS volumes in AWS using its EBS Snapshots.

The weakness of this mode is that it doesn’t improve datacenter capacity.

### Volume Cached

All data is stored in AWS Managed part of S3, and then the frequently accessed data is cached locally.

## Storage Gateway Tape - Virtual Tape Library (VTL)

Storage Gateway in VTL mode allows for replacing a tape-based backup solution with one that uses S3 and Glacier rather than physical tape media.

## Storage Gateway - File

Bridges on-premises file storage and S3 storage via Mount Points available over via NFS or SMB.

Files stored into a mount point, are visible as objects in an S3 bucket.

File Gateway doesn’t support _Object Locking_. This means that theoretically, two people could edit/overwrite the same file at the same time and data could be lost.
