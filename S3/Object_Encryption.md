# Object Encryption

S3 doesn’t offer encryption at a bucket level. Encryption occurs at an object level.

## Server-Side Encryption

There are three types of server-side encryption that can be used with S3.

These different options have different tradeoffs in regards to trust, overhead, cost, resource consumption, etc.

1. Server-Side Encryption With Customer-Provided Keys (SSE-C)
1. Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)
1. Server-Side Encryption With KMS KEYS Stored in AWS Key Management Service (SSE-KMS)
