# AWS Accounts

## AWS Accounts Overview

An AWS Account is a container for identities (users), and resources.

By default new IAM identities start off with no permissions.

## Account Creation

Using the plus operator we can create email aliases in Gmail that point to our main Gmail account.

This allows us to bypass the painful process of having to create a unique email address for each AWS account we want to create.

## MFA

It's easy to setup MFA on AWS using a virtual MFA device.

I've found using Google Authenticator to be really easy and convenient.

## IAM Basics

IAM is a global service.

IAM lets us create 3 different types of identity objects:

1. **Users** -- Identities which represent humans or applications that need access to our account.
1. **Groups** -- Collection of related users e.g. development team, finance, or HR
1. **Roles** -- Can be used by AWS services, or for granting external access to our account.

## IAM Access Keys

We can use access keys to interact with AWS accounts via CLI tools.

An IAM user can have zero, one, or two access keys.

Access keys can be created, deleted, made inactive or made active.

By default access keys are in an active state after creation.

IAM users are the only type of identity that can utilize access keys.

Generally it's not recommended to give the root user access keys.

When using the AWS CLI, we can use _named profiles_ to configure multiple AWS accounts.
