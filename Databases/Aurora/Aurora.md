# Amazon Aurora

Amazon Aurora utilizes clusters where the architecture consists of a single primary instance along with 0 or more replicas.

Aurora replicas can help with both availability and read operations at the same time.

This alone is an improvement over RDS where you’re forced to choose between availability and read scaling.

Aurora doesn’t use local storage, it uses cluster volumes for storage. This results in faster provisioning, as well as improved availability and performance.

The storage system used in Aurora is more resilient than the one found in typical RDS instances.

## Costs

There is no free-tier option. Aurora tends to be a better value than RDS, though there are some exceptions.

Aurora storage is all SSD based, and is billed based on what’s used.

Compute resources are charged hourly based on how many seconds of computing power were used, and the minimum charge is 10 minutes.

Storage costs are determined by how many GB were consumed that month as well as an I/O cost per request.

## Backups

Backups in Aurora work in mostly the same way as RDS. Restores are used to create a new cluster.

If enabled, a feature called ‘Backtrack’ can be used which allows in-place rewinds to a previous point in time.

This means that if our data gets corrupted we can fix this issue without having to restore to a new cluster and reconfigure our DB endpoints.

Aurora also has a feature called ‘Fast clones’, which can be used to make a new database much faster than a traditional DB copy.

The way this feature works is that instead of copying all the data, the fast clone references the original DB and simply writes the differences between itself and the original DB, as well as the the differences between the current state of the original DB vs the state of the original DB at the moment it was cloned.
