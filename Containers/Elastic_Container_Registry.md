# Elastic Container Registry (ECR)

**Amazon Elastic Container Registry (ECR)** allows us to easily store, share, and deploy our container software anywhere.

ECR is a fully managed container registry offering high-performance hosting that allows us to reliably deploy application images and artifacts from anywhere.

It’s similar to Docker Hub, but specifically for AWS.

Each AWS account has a public and private registry.

Public registries offer read-only access to everyone, but read-write requires permissions.

Private registries on the other hand, require permissions for any reading or writing.

Each registry can have many repositories. Each repository can contain many images. A given image can have several tags.

Some important features of ECR are:

- Integration with IAM
- Image scanning
- Nearly real-time metrics via CloudWatch
- API Action logging in CloudTrail
- Event logging in EventBridge
- Replication of images, both cross-region and cross-account
