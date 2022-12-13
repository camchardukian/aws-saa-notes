# VPC Sizing & Structure

A solid infrastructure platform is just as much about a good design, as it is a good technical implementation. For that reason, there are some things we should think about when designing a VPC.

## VPC Considerations

- What size should the VPC be
- What Networks can’t be used
- The needs of the application today as well as being scalable to accommodate future needs
- Resiliency

## VPC Structure

Services run from within subnets (which is where IP addresses are allocated from), not directly within the VPC.

Tiers are different types of infrastructure that run from within a VPC.

Without any further information provided, some basic guidelines to structure a VPC would be:

- Start with three subnets, but allow yourself a spare to grow into
- Start with three tiers, and again allow yourself a spare to grow into
