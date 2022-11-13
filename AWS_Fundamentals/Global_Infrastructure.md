# Global Infrastructure

Amazon's cloud computing resources are hosted in multiple locations across the globe.

These locations are composed of _AWS Regions_, _Availability Zones_, and _Local Zones_.

An AWS Region is a geographic area.

Every AWS Region has multiple, isolated locations known as Availability Zones (AZs).

AZs are physical locations made up of one or more data centers.

Local zones are data centers located in or near densely populated area and thus are able to provide single-digit millisecond, low-latency performance for the area.

_Edge locations_ are also AWS data centers, but they are used primarily for the caching of data rather than being used for hosting servers, big data processing, etc.

## Resilience

Within AWS services can be globally resilient, region resilient, or AZ resilient.

### Globally Resilient

A service operates globally with a single database and its data is replicated between regions.

Theoretically, it would take almost the entire world failing for this type of service to experience a full outage.

With this type of service, you don't need to select a region.

Examples of globally resilient services are IAM and Route 53.

### Region Resilient

Region resilient services operate in a single region and have one set of data per region.

Services of this type typically duplicate their data amongst multiple availability zones.

This type of service will experience an outage if all of the availability zones a service has servers/data in fail, or if the entire region fails.

### AZ Resilient

Services that offer this type of service fail most easily, because they will fail if that individual AZ fails.
