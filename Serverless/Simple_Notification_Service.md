# Simple Notification Service

_Simple Notification Service_ (SNS) is a service that operates from the Public AWS Zone.

The main purpose of SNS is to coordinate the sending and delivery of messages.

Messages are <= 256kb payloads.

_SNS Topics_ are the base entity of SNS. They are the logical access point that acts as a communication channel.

In SNS, a Publisher sends messages to an SNS Topic.

Topics have Subscribers which receive messages.

SNS supports a wide variety of subscriber types including other AWS services such as Lambda, and SQS.

Some notable features of SNS are delivery status (with supported services), delivery retries, server side encryption, and SNS Topics being able to be used across accounts via the usage of Topic Policies.
