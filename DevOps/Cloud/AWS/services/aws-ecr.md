# Amazon Elastic Container Registry ECR

Amazon Elastic Container Registry (Amazon ECR) is an AWS-managed container image registry service that is secure, scalable, and reliable. Amazon ECR supports private repositories with resource-based permissions using AWS IAM. This allows specified users or Amazon EC2 instances to access your repositories and container images. You can use the preferred CLI to insert, extract, and manage Docker images, Open Container Initiative (OCI) images, and OCI-compliant artifacts.

The AWS Container Services team maintains a public roadmap on GitHub. It contains information about the teams' current work and allows all AWS customers to give feedback directly. For more information.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4a1c7e68-1b06-4bb8-8309-23da15c05317">
</p>

## Amazon ECR components

Amazon ECR contains the following components:

### Registry (Registro)

Each AWS account receives a private Amazon ECR registry; you can create one or more repositories in your registry and store images there. For more information

### Token of autorization

You must authenticate the client in the Amazon ECR logs as an AWS user in order for that client to be able to insert and extract images.

### Repository

An Amazon ECR repository contains Docker images, Open Container Initiative (OCI) images and OCI-compatible artifacts.

### Repository Policy

You can control access to repositories and the images they contain by policies.

### Imagen

You can insert and extract container images in the repositories and use them locally in your development system or in Amazon ECS task definitions and Amazon EKS pod specifications.

## Características de Amazon ECR

Amazon ECR offers the following features:

Lifecycle policies help manage the lifecycle of images in your repositories. You must define rules that result in the cleanup of unused images. You can test rules before applying them to the repository.

Image scanning allows identifying software vulnerabilities in container images. Repositories can be configured to scan on insertion. This ensures that each new image inserted into the repository is scanned. You can then retrieve the results of the image scan.

Replication between regions and between accounts makes it easier to have the images where you need them. It is configured as a Registry parameter and is applied on a per-region basis.

Caching rules provide a way to store caching repositories in remote public logs in your private Amazon ECR registry. Using a pull cache rule, Amazon ECR will periodically contact the remote registry to ensure that the cached image of your private Amazon ECR registry is up to date.

## References
- https://docs.aws.amazon.com/es_es/AmazonECR/latest/userguide/what-is-ecr.html


