# RDS Security

SSL/TLS is available for RDS, and can even be made mandatory.

For an Amazon RDS encrypted DB instance, all logs, backups, and snapshots are encrypted. RDS uses an AWS KMS key to encrypt these resources.

A read replica of an RDS encrypted instance must be encrypted using the same KMS key as the primary DB instance if both are in the same AWS region.

If they are in different AWS regions, the read replica would be encrypted using the KMS key for that AWS region.

It’s important to note that encryption cannot be removed from an RDS instance once it has been encrypted.

If using RDS with Oracle or SQL Server, _Transparent Data Encryption_ (TDE) is supported.
