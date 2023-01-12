# Database Transaction Models

The [CAP theorem](https://en.wikipedia.org/wiki/CAP_theorem) (also called Brewer’s theorem after computer scientist Eric Brewer), states that a database or distributed data store is only capable of delivering two of the following:

- Consistency — Every read receives the most recent write or an error.
- Availability — Every request receives a (non-error) response, without the guarantee that it contains the most recent write.
- Partition Tolerance — The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes.

A product/service like RSD utilizes the ACID transaction model. While very reliable, this model limits scaling.

1. Atomic — ALL or NO components of a transaction SUCCEED or FAIL.
1. Consistent — Transactions move the database from one valid state to another — nothing in-between is allowed.
1. Isolated — If multiple transactions occur at once, they don’t interfere with each other. Each executes as if it’s the only one.
1. Durable — Once committed, transactions are durable. This means that they are stored on non-volatile memory, and are resistant to power outages or crashes.

A product/service like DynamoDB utilizes the BASE transaction model. While somewhat less reliable, this model promotes excellent performance and scaling capabilities.

1. Basically Available — READ and WRITE operations are available ‘as much as possible’ but without any consistency guarantees.
1. Soft State — The database doesn’t enforce consistency, this is offloaded onto the application/user.
1. Eventually Consistent — If we wait long enough, reads from the system will be consistent.
