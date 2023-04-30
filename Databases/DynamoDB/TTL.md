# DynamoDB TTL

_DynamoDB Time to Live (TTL)_ allows us to define a per-item timestamp to determine when an item is no longer needed.

Shortly after said time has passed, DynamoDB will delete the item from our table without consuming any write throughput.

TTL is provided at no extra cost as a means to reduce stored data volumes by retaining only the items that remain current for our workload’s needs.
