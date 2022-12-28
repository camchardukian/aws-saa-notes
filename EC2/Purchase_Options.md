# Purchase Options

There are a number of different ways we can purchase the infrastructure that EC2 instances run on. They are:

- **On-Demand** — The default purchasing option. Instances are isolated, but multiple customer instances run on shared hardware. Per-second billing while an instance is running. No upfront costs, but also no discounts. Ideal for unknown/short-term workloads, or apps that can’t be interrupted.

- **Spot** — Spot pricing is how AWS sells unused EC2 capacity. The spot price is based on the spare capacity at a given time, but can offer up to a 90% discount.

- **Reserved** — A commitment to use EC2 instances over a 1 or 3 year period of time. Offers cost-savings, and can be paid no-upfront, partial upfront, or all upfront.

- **Dedicated Instance** — Similar to dedicated hosts, but dedicated instances instead utilize per instance billing. Dedicated instances also do not provide us with visibility of physical characteristics such as sockets, cores, etc, whereas dedicated hosts do.

- **Dedicated Host** — A host that is dedicated to only us. Ideal for situations where software licensing is based on sockets/cores. Pay for the host, no instance charges. Also good for corporate compliance requirements.

- **EC2 Savings Plans** — An hourly commitment for a 1 or 3 year term (ex: $20/hour for 3 years). Resource usage up to the committed amount is offered at the savings plan rate, which is cheaper than the standard on-demand rate. Resource usage beyond the committed amount, however, is still charged based on the on-demand rate.
