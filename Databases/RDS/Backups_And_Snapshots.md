# RDS Automatic Backups & Snapshots

Both automated backups and snapshots use AWS Managed S3 Buckets for storage. The benefit of using S3 for storage is that the data being stored becomes regionally-resilient.

Our DBs can be backed up either automatically or manually.

DB snapshots can be performed either manually or automatically.

Both automated backups and snapshots are taken of the RDS instance, which means all of the databases within it.

Snapshots remain even after we delete an RDS instance. They’re only deleted if we delete them manually or via some other external process.

Automated backups occur once per day, and can occur at a time of our choosing or a time chosen randomly by AWS.

Automated backups can be retained from 0 days to 35 days. If retention is set to 0 days, automated backups will be disabled.

RDS can be configured to replicate backups to another region (both snapshots and transaction logs). Charges apply for both the cross-region data copy as well as the storage in the destination region.

Backups can be restored, but it’s important to note that restores aren’t fast. For that reason, restore time is something that needs to be considered when recovery time objective (RTO) planning.
