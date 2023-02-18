# AWS Certificate Manager (ACM)

AWS Certificate Manager (ACM) is a service which allows for the creation, management, and renewal of certificates.

ACM can run as either a public or private Certificate Authority (CA).

ACM can either generate or import certificates.

If ACM generates a certificate, it can renew said certificate for us.

If we import a certificate into ACM, we are responsible for renewing the certificate.

It’s also important to note that certificates can only be deployed out to supported services.

ACM can NOT be used with EC2.

ACM is a regional service.

Certificates cannot leave the region they are generated or imported in.

For most services, the certificate needs to be located in the same region as the service (if the service is in ap-southeast-2 then the ACM would also need to be in ap-southeast-2).

For global services such as CloudFront, however, the ACM would need to be located in ’us-east-1’.
