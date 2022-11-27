# IAM Groups & Roles

## IAM Groups

IAM Groups are containers for Users. You cannot log-in to IAM Groups. They’re used solely for organizing IAM Users.

Users can be members of up to 10 IAM Groups.

There isn’t a hard limit for the number of users in a particular group (except indirectly a limit of 5,000 because of 5,000 being the maximum number of IAM users in a single AWS account).

Groups cannot be nested, but an account can have up to 300 groups (though this number can sometimes be increased by contacting AWS support).

## IAM Roles

An IAM Role is one of two types of identities inside an AWS account (the other being IAM Users).

If you’re not sure of how many principals will use an identity, it may be a good use case of IAM Roles.

IAM Roles are generally used on a temporary basis.

IAM Roles have two types of policies that can be attached to them:

- **Trust Policy** — Controls which identities can assume that role.

- **Permissions Policy** — Controls which actions and resources the role can use.
