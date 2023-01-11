# Routing Policies

**Simple Routing** — Used to configure standard DNS resources, with no special Route 53 routing such as weighted or latency. Typically used to route traffic to a single resource, such as a web server.

**Weighted Routing** — Routes traffic to multiple resources based on proportions we specify.

**Multivalue Routing** — Allows us to configure Route 53 to return multiple values, such as IP addresses for our web servers, in response to DNS queries.

**Failover Routing** — Can be used with health checks to route traffic to a primary resource if it is healthy, or a secondary resource if the primary resource is unhealthy.

**Latency Routing** — Used to route users to resources with the lowest latency.

**Geolocation Routing** — Used for regional restrictions, language specific content, or load balancing across regional endpoints. This type of routing doesn’t return the closest records, it returns records that are inside of a relevant location.

**Geoproximity Routing** — Routes traffic to resources based on the location of our users and our resources. Optionally, **biases** can also be added. Biases are used to expand or shrink the geographic region from which traffic is routes to a resource.

**IP-based Routing** — A new type of routing introduced in 2022. Used to provide granular control on how users should be routed based on their IP addresses.
