# DynamoDB Streams

DynamoDB Streams are a 24 hour rolling window of time ordered changes to items in a DynamoDB table.

Streams are enabled on a per table basis, and record any INSERTS, UPDATES, and DELETES.

When items change, an event is generated and that event contains the data which changed. An action can then be taken using that data.

This type of architecture is called a ‘Trigger’ and it can be implemented using DynamoDB Streams along with Lambda.
