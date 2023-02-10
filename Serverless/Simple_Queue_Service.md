# Simple Queue Service (SQS)

SQS is a managed message queuing service provided by AWS.

Amazon SQS supports asynchronous task processing. This means that rather than one application having to invoke another one directly, our app can simply send a message into a queue where it’ll wait until the other app tries to access the queue.

There are two types of SQS queues: standard queues, and first-in first-out (FIFO) queues.

## Standard Queues

Standard queues attempt to keep messages in the same order they were sent, but this isn’t guaranteed. Standard queues also promise to deliver messages at least once, rather than exactly once.

The big benefit of standard queues, however, is that they offer excellent performance and scaling.

## FIFO Queues

FIFO queues keep messages in the same order in which they were initially sent and deliver messages exactly once.

The drawback, however, is FIFO queues only support up to 300 sent, received, or deleted messages per second, which is significantly less than standard queues.

Technically, those 300 messages mentioned above can actually be increased to 3,000 messages via the usage of batching.

FIFO queues need to have a .fifo suffix.

## Delay Queues

Delay queues provide an initial period of invisibility for messages.

These predefined periods can ensure that the processing of messages doesn’t begin until this period has expired.

## Dead Letter Queues

Dead letter queues allow for messages which are causing repeated processing errors to be moved into a separate queue called the dead letter queue.
