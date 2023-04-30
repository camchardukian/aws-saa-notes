# DynamoDB Indexes

Secondary indexes allow for an alternative presentation of data stored in a base table.

_Local Secondary Indexes (LSIs)_ must be created with a table, and provide an alternative sort key for the data in the table.

_Global Secondary Indexes (GSIs)_ can be created at any time. They allow for defining an alternative partition key and an alternative sort key.

AWS recommends using GSIs by default, and only using LSIs when strong consistency is required.
