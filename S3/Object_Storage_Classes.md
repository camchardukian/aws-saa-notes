# S3 Object Storage Classes

## S3 Standard

- Default storage class
- Data is replicated across at least 3 regions
- Provides eleven “nines” of durability (1 object loss/10,000,000 objects/10,000 years)
- GB/m fee for data stored, fee per GB transferred out charge, price per 1,000 requests
- Should be used for frequently accessed data which is important and non-replaceable

## S3 Standard IA (Infrequent Access)

- Roughly half the storage cost of S3 standard
- Higher per GB data retrieval fee
- Minimum duration charge of 30 days (objects can be stored for less time, but the minimum of 30 days still applies for billing
- Minimum capacity charge of 128KB/object
- Should be used for long-lived data that is important but infrequently accessed

## S3 One Zone-IA

- Similar to S3 Standard IA, but cheaper and less resilient due to only using one AZ within the region
- Should be used for long-lived data which is non-critical, replaceable if lost, and infrequently accessed

## S3 Glacier Instant

- Similar to S3 Standard IA, but cheaper storage, more expensive retrieval, and longer minimum storage duration
- Should be used for long-lived data that is only accessed roughly once per quarter and needs millisecond retrieval time

## S3 Glacier Flexible

- Very cheap, but requires minutes or hours to access data

- Objects cannot be made publicly accessible, any access of data (beyond object metadata) requires a retrieval process

- Should be used for archival data where frequent or realtime access isn’t needed (e.g. yearly)

## S3 Glacier Deep Archive

- Similar to S3 Glacier Flexible, but with longer retrieval times of roughly 12-48 hours
- Should be used for archival data that rarely if ever needs to be accessed

## S3 Intelligent-Tiering

- Monitors and automatically moves any objects between different tiers based on their usage.
- Has a monitoring and automation cost per 1,000 objects
- Should be used for long-lived data with changing or unknown usage patterns
