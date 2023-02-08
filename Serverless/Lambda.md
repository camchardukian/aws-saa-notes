# AWS Lambda

AWS Lambda is a Function-as-a-Service (FaaS).

Lambda functions are a piece of code that Lambda runs. More specifically, Lambda functions are our code plus all of the Lambda associated wrappings and configuration.

Lambda functions use a runtime (such as Python 3.8), and functions are loaded and run in a runtime environment.

With Lambda, we are billed based on the duration that our functions run.

Lambda functions can run for up to 15 minutes before they timeout.

## Lambda Networking

Lambda has two networking modes: public, and VPC networking.

### Public networking

This is the default mode. It provides access to public AWS services and the public internet.

This offers the best performance because no customer specific VPC networking is required.

The downside is that these Lambda functions will have no access to VPC based services unless public IPs are provided and security controls allow external access.

### VPC Networking

Lambda functions running in a VPC obey all VPC networking rules.

This means that they can easily access resources inside of the VPC, but they can’t access resources outside the VPC unless networking configuration exists within the VPC to allow external access.

## Lambda Security

Lambda execution roles are IAM roles attached to lambda functions which control the PERMISSIONS the Lambda function receives.

Lambda resource policies on the other hand control WHAT services and accounts can INVOKE Lambda functions.

## Lambda Logging

Lambda uses CloudWatch, CloudWatch Logs & X-Ray. Logs from Lambda executions appear in CloudWatch Logs while metrics like invocation success/failure, retries, latency, etc. are stored in CloudWatch.

One important thing to note is that CloudWatch Logs requires permissions via an Execution Role.

## Invocation Modes

Lambda functions can be invoked synchronously, asynchronously, or via event source mapping.

## Versions

Lambda functions can have versions. Versions are immutable — they never change once they’ve been published.

Versions have their own unique Amazon Resource Name (ARN).

`$Latest` can be used to point to the latest version of a Lambda function.
