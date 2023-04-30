# DynamoDB Backups

With On-Demand backups, backups are performed manually and full backup copies of the table are retained until we manually remove them.

If we enable _Point-in-time Recovery (PITR)_ on a table, a continuous record of changes allows us to create a new DynamoDB table using the data from any point in the 35 day recovery window.
