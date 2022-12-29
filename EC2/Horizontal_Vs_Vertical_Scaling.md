# Horizontal Vs Vertical Scaling

## Vertical Scaling

An issue with vertical scaling with EC2, is that resizing an EC2 instance requires a reboot. This may serve as a disruption to users. This can make it difficult to scale up or down quickly.

Larger instances also often carry a price premium. There’s also an upper cap on performance (the maximum instance size).

The one large benefit of vertical scaling, however, is that it doesn’t require us to modify the application. Vertical scaling works for ALL applications — even monoliths.

## Horizontal Scaling

Unlike vertical scaling, horizontal scaling utilizes an increased number of instances rather than larger instances.

This has the potential to offer improved performance at a better price than vertical scaling. Horizontal scaling also can utilize load balancers to assist in scaling without the downtime we may struggle with when using vertical scaling.

One issue with horizontal scaling, however, is that it requires more thought to implement correctly.

One example of this is needing to design our application in such a way that we can effectively support user sessions even when we may constantly be switching between instances.
