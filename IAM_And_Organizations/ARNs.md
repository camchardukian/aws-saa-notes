# Amazon Resource Names (ARNs)

ARNs uniquely identify AWS resources.

They are used when it’s necessary to unambiguously identify a resource across all of AWS such as in IAM policies, Amazon Relational Database Service (Amazon RDS) tags, and API calls.

ARNs generally follow one of these formats:

```
arn:partition:service:region:account-id:resource-id

arn:partition:service:region:account-id:resource-type/resource-id

arn:partition:service:region:account-id:resource-type:resource-id
```

**Partition** — A partition is a group of AWS Regions. Each AWS account is scoped to one partition.

**Service** — The service namespace that identifies the AWS product.

**Region** — The Region code, `us-east-2` for example.

**Account-id** — The name of the AWS account that owns the resource (minus any hyphens).

**Resource-type** — The type of resource such as vpc for a virtual private cloud (VPC).

**Resource-id** — The resource identifier. This could be the name, ID, or resource path.
