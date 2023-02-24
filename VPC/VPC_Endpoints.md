# VPC Endpoints

There are two types of VPC endpoints: Gateway endpoints and Interface endpoints.

## Gateway Endpoints

Gateway endpoints are a type of VPC endpoint which allow private access to S3 and DynamoDB.

Gateway endpoints add ‘prefix lists’ to route tables, allowing the VPC router to direct traffic flow to the public services via the gateway endpoint.

Gateway endpoints are highly available across all AZs in a region by default.

A Gateway endpoint can only access services that are in the same region as it.

Endpoint policies are used to control what the Gateway endpoint can access.

Gateway endpoints are not accessible outside the VPC they are associated with.

## Interface Endpoints

Interface endpoints are similar to Gateway endpoints in that they provide access to AWS Public Services.

Interface endpoints provide access to pretty much all AWS services apart from DynamoDB.

Architecturally, Interface endpoints are added to specific endpoints and are NOT highly available by default.

For high availability, we need to place one Interface endpoint inside of each AZ to ensure high availability.

Network access for Interface endpoints can be controlled via security groups.

They are also compatible with endpoint policies.

Interface endpoints can only be used with TCP and IPv4.
