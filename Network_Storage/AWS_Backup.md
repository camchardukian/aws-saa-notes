# AWS Backup

AWS Backup is a fully managed data-protection (backup/restore) service. The product is capable of consolidating management by being configured across multiple accounts and multiple regions.

AWS Backup supports a wide range of AWS products.

Here are some key concepts related to this service:

- **Backup Plans** — Determine the frequency, window, lifecycle, vault, region copy, and other settings for backups.

- **Resources** — What resources are backed up.

- **Vaults** — The backup destination (container).

- **Vault Lock** — An optional feature that can be helpful in giving additional security and control over backup vaults. When a lock is active, the vault configuration cannot be altered or deleted by a customer, account/data owner, or AWS.

- **On-Demand** — Backups can be created manually if/when necessary.

- **PITR** — For some resources, AWS Backup supports continuous backups and point-in-time recovery (PITR).
