# S3 Security

S3 is private by default. The only identity which has any initial access to an S3 bucket is the account root user of the account that owns that bucket (the account that created it).

## S3 Bucket Policies

S3 bucket policies are a type of resource policy that are attached to a bucket.

The difference between identity policies and resource policies is that identity policies control what an identity can access.

Resource policies control who can access that resource.

The biggest benefits of resource policies is that they can provide access to other accounts, and they can provide anonymous access.

There can only be one bucket policy per bucket, but a given bucket policy can have multiple statements.

## Access Control Lists (ACLs)

ACLs are a way to apply security to objects or buckets. ACLs are in legacy usage at this point, but it’s still good to be aware of their existence.

## Block Public Access Settings

These settings provide additional protection to block public access to S3 buckets.

In ideal circumstances, these settings wouldn’t even be needed because everyone would know how to configure their S3 buckets appropriately.

These settings were added fairly recently, however, because this obviously hasn’t been the case historically with the many data leaks that have occurred through S3.
