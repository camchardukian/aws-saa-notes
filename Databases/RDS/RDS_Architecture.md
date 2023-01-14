# Relational Database Service (RDS) Architecture

RDS is a Database Server as a Service (DBSaaS). This means, we pay money and in exchange we get a database server.

The difference between a database server and a database, is that multiple databases can exist on a single database server.

We are able to use RDS with a number of DB engines such as MySQL, MariaDB, PostgreSQL, Oracle, and Microsoft SQL Server.

RDS is a managed service, which means that when using it we generally don’t have any access to the OS or SSH.

RDS instances can have multiple databases. Every RDS instance has its own dedicated storage provides by EBS.

## Fees

There are a number of factors that influence the cost of using RDS. These include:

1. The instance size & type (billed per second).
1. Whether multiple AZs are used or not.
1. The type and amount of storage.
1. The amount of data transferred in and out of the instance.
1. The amount of backup/snapshot storage.
1. Any applicable licensing costs.
