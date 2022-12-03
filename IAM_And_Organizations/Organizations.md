# AWS Organizations & Service Control Policies (SCPs)

## AWS Organizations

_AWS Organizations_ is a global service that allows us to manage multiple AWS accounts.

The main benefit of using AWS Organizations is that it offers consolidated billing and we can enjoy price benefits from aggregated usage (volume discounts).

**Organization Units** are a group of AWS accounts within an organization. One Organization Unit can contain other Organizations Units — thus creating a hierarchy.

## Service Control Policies (SCPs)

Service Control Policies (SCPs) are a type of policy used inside of organizations to manage permissions in one’s organization.

Permissions aren’t actually granted by SCPs. What SCPs offer instead is a type of guardrail on the actions that an account’s administrator can delegate to IAM users and roles inside of the affected accounts.

In essence, what an account is actually able to do is the intersection between what is allowed by the SCP and what is allowed by the IAM/resource-based policies.

Note: SCPs don’t affect users or roles in the management account. They affect only the member accounts in one's organization.
