# Aurora Serverless

Aurora Serverless is scalable via _Aurora Capacity Units (ACUs)_.

You can set a minimum and maximum number of ACUs for your cluster and Aurora will scale between them based on load.

The cluster can even go to 0 and be paused.

Aurora Serverless offers the same resilience as Aurora Provisioned (6 copies across AZs).

Aurora Serverless operates on consumption billing on a per-second basis.

Overall, Aurora Serverless is great for infrequently used applications, new applications (where we may not be able to predict their average and peak workloads), variable workloads, unpredictable workloads, development/test databases, and multi-tenant applications.
