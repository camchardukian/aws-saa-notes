# IAM Identity Policies

A policy is an object in AWS that can be associated with an identity or resource to define their permissions.

_Identity-based policies_ are attached to an IAM user, group, or role. These policies let you specify what that identity can do (its permissions).

Policies can be be specified using policy documents created using JSON.

It’s important to note that the precedence for permissions is deny-allow-deny.

This precedence is important for when permission effects clash.

For example, if an explicit deny clashes with an explicit allow, the deny will take precedence.

If an explicit allow clashes with an implicit deny, however, then the allow would take precendence.

When setting permissions for identities in AWS we can use AWS managed policies, customer managed policies, or inline policies.

In most cased managed policies should be used as they are reusable, easily maintainable, allow for versioning/roll backs, and allow for permission delegation management.

Inline policies are useful if you have a very specific case, and you want to make sure the permissions defined in the policy are not inadvertently attached to another entity.

## AWS Managed Policies

An _AWS managed policy_ is a standalone policy that is created and administered by AWS.

In this context, standalone policy means that the policy has its own _Amazon Resource Name (ARN)_ that includes the policy name.

The benefit of AWS managed policies is that they are designed to provide permissions for many common use cases.

The downside is that they cannot be customized.

## Customer Managed Policies

Standalone policies that you administer in your own AWS account are referred to as _customer managed policies_.

By attaching the policy to an entity, we give that entity the permissions that are defined in the policy.

## Inline Policies

_Inline policies_ are policies that are embedded in an IAM identity.
