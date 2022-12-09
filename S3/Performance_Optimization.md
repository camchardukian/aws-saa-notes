# S3 Performance Optimization

## Single PUT Upload

By default uploads to S3 occur as a single data stream. If the stream fails, the upload will also fail and a full restart will be required.

## Multipart Upload

The minimum data size for a multipart upload is 100MB.

A multipart can be split into a maximum of 10,000 parts (each ranging for 5MB to 5GB except for the final part which is allowed to be smaller than 5MB).

One benefit of using multipart upload is that parts can fail and be restarted in isolation.

The other benefit is that multipart uploads will almost always complete more quickly than single PUT uploads of the same size.

## S3 Transfer Accleration

S3 Transfer Acceleration can speed up content transfers to and from S3 by as much as 50-500%.

It does this by utilizing Edge Locations rather than trying to transfer all of the data over the public internet.

It is a feature that is disabled by default but can be enabled on a bucket-to-bucket basis.

Using S3 Transfer Acceleration will result in minor associated fees of roughly $0.04-$0.08/GB depending on the edge locations being used.
