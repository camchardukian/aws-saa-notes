# AWS Public Vs Private Services

As someone working with AWS it's important to understand the three different network zones:

## Public Internet

This zone has direct access to general internet services.

It can connect to the public AWS zone using the internet as transit.

## AWS Public Zone

This zone sits between the public internet and the AWS private zone.

We may expect to find things such as S3 buckets here.

## AWS Private Zone

This zone is where EC2 instances reside.

EC2 instances can utilize the Internet Gateway to access the public internet.

In general this zone is isolated from the other zones unless configured otherwise.
