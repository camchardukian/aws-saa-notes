# R53 Hosted Zones

## Public Hosted Zones

A public hosted zone is a container that holds information about how you want to route traffic on the internet for a specific domain that is accessible from the public internet.

Externally register domains can point at the R53 Public Zone.

Public hosted zones are accessibe from both the public internet as well as any VPCs that are configured to allow DNS resolution. They are hosted on 4 name servers provided by Route 53.

There is a monthly cost for hosting a public hosted zone, as well as a small charge for each query made against it.

## Private Hosted Zones

A private hosted zone is similar to a public hosted zone in how it operates. The big difference obviously, is that a private hosted zone isn’t public.

Instead, a private hosted zone is associated with VPCs and is only accessible in those VPCs that it’s associated with.

## Split View Hosted Zones

Split view hosted zones help access an internal version of a website using the same domain name that is used publicly.

This could be useful if you wanted people outside of your organization to view a public version of your website, but wanted to allow those inside of your corporate network to be able to access an internal version of the website.
