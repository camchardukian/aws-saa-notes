# CloudFront

CloudFront is a Content Delivery Network (CDN) within AWS.

## CloudFront Behaviors

Caching policies, allowed HTTP methods, and viewer access can be configured on a behavior basis.

## Time To Live (TTL)

Objects cached by CloudFront have a default TTL of 24 hours.

It’s also possible to set minimum TTL and maximum TTL values that will be applied across all objects.

Different headers can also be used to set TTLs, but if the values indicated in these headers is outside the range of the minimum/maximum TTLs, the minimum/maximum TTL would then be applied.

Here are the headers we can use in more detail:

```
Origin Header: Cache-Control max-age (seconds)

Origin Header: Cache-Control s-maxage (seconds)

Origin Header: Expires (Date & Time)
```

The above headers can be set to use Custom Origins (via the web server or our application) or S3 (via object metadata).

## Cache Invalidation

Cache invalidations are performed on a distribution.

CloudFront distributions tell CloudFront where we want content to be delivered from, and the details about how to track and manage content delivery.

Cache invalidations are applied to all edge locations within that distribution.

Cache invalidations take a little bit of time to take effect.

Versioned file names can be useful for quickly identifying what specific image was used when we view our logs in CloudWatch, and it also results in us not needed to be overly dependent on using cache invalidations.

```
example_v1.jpg
example_v2.jpg
```

## CloudFront & SSL

CloudFront supports SSL by default via the following certificate:

> \*.cloudfront.net

However, this default SSL certificate cannot be used if we’re taking advantage of the Alternate Domain Names feature and using a DNS Provider such as Route53 to point our Alternate Domain Name at our CloudFront Distribution.

Fortunately, we can generate or import an SSL certificate using _AWS Certificate Manager_ (ACM).

_Server Name Identification_ (SNI) is an extension for the TLS protocol to indicate a hostname in the TLS handshake.

Very old browsers don’t support SNI, but most major browsers seem to have started supporting it around 2005-2006.

If we want to use SSL with old browsers, CloudFront offers dedicated IPs for an extra fee (currently $600/month/distribution).

## CloudFront Origin Types

CloudFront origins are the location where content is stored, and from which CloudFront gets content to serve to users.

## Securing CloudFront & S3

An _Origin Access Identity_ (OAI) is a type of identity that can be associated with CloudFront Distributions that utilize S3 Origins.

OAIs can be used in S3 Bucket Policies to allow access from an OAI, but implicitly deny everything else.

OAIs are generally used to ensure no direct access to S3 objects is allowed when using private CloudFront Distributions.

To secure CloudFront Distributions that use custom origins, we can either require custom headers or use the publicly available IP ranges of CloudFront to create a firewall around our custom origin(s).

## Private Distributions

CloudFront is capable of running in two security modes in regards to content:

1. Public — This is the default mode, and it results in open access to objects. When using this mode, content is available to any viewer.
1. Private — If this mode is configured, requests require a signed cookie or signed URL.
