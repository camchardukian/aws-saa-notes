# AWS Global Accelerator

AWS Global Accelerator is designed to improve global network performance by offering entry points onto the global AWS transit network as close to customers as possible via the usage of anycast IP addresses.

Anycast is an IP network addressing scheme that allows multiple servers to share the same IP address, allowing for multiple physical destination servers to be logically identified by a single IP address.

The difference between Global Accelerator and CloudFront is that Global Accelerator can be used for non HTTP/HTTP applications (this means it could work with TPC/UDP applications whereas CloudFront wouldn’t be able to).

Another difference between the two is that Global Accelerator doesn’t cache content, whereas CloudFront does.

Global Accelerator improves performance simply by moving the AWS network closer to customers.
