# AWS Shared Responsibility Model

Basically, it exposes the theoretical responsibility regarding the infra that we implement in that platform, in the following image we will be able to analyze the mentioned model.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d6198954-788a-4631-b63a-c4e501bd0a43">
</p>

## Responsability of AWS

AWS is responsible for the security of the cloud. This means that AWS provides security and protection to the infrastructure running the services offered in the AWS cloud. AWS is responsible for the following:

- Providing security and protection for AWS regions, Availability Zones and data centers, down to the physical security of buildings.

- Managing the hardware, software, and networking components that run AWS services, such as physical servers, host operating systems, virtualization layers, and AWS networking components

The level of AWS responsibility depends on the service. AWS classifies services into three categories. The following table provides information about each, including the AWS responsibility.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/6abdee78-04b4-461a-a77b-a9204f7e694e">
</p>

Note: Container services refer to AWS abstract application containers in the background, not Docker container services. This allows AWS to remove the responsibility of managing the platform from customers.


## Customer of client

Customers are responsible for security in the cloud. When using any AWS service, you are responsible for properly configuring the service and applications and ensuring that your data is secure.

Your level of responsibility depends on the AWS service. Some services require you to perform all necessary administration and security configuration tasks, while other more abstract services require you to only manage data and control access to resources. With the three categories of AWS services, you can define your level of responsibility for each AWS service you use.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/dbbb13ce-321b-46aa-8f10-9ac730f73367">
</p>

Due to varying levels of effort, customers should consider which AWS services they use and review the level of responsibility required to protect each service. They should also review how the shared security model aligns with the security standards of their IT environment, in addition to applicable laws and regulations.

A key concept is that customers maintain full control of the data and are responsible for managing the security related to their content. For example, you are responsible for the following:

- Choosing a region for AWS resources in accordance with data sovereignty rules.
- Implementing data protection mechanisms, such as encryption and scheduled backups
- Using access control to limit who can access AWS data and resources


## AWS responsability
AWS is responsible for protecting the infrastructure that runs all of the services offered in the AWS Cloud. This infrastructure is composed of the hardware, software, networking, and facilities that run AWS Cloud services.


## Shared responsability
Security and Compliance is a shared responsibility between AWS and the customer. This shared model can help relieve the customer’s operational burden as AWS operates, manages and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates. The customer assumes responsibility and management of the guest operating system (including updates and security patches), other associated application software as well as the configuration of the AWS provided security group firewall. Customers should carefully consider the services they choose as their responsibilities vary depending on the services used, the integration of those services into their IT environment, and applicable laws and regulations. The nature of this shared responsibility also provides the flexibility and customer control that permits the deployment. As shown in the chart below, this differentiation of responsibility is commonly referred to as Security “of” the Cloud versus Security “in” the Cloud.

![image](https://github.com/dimasx010/knowledge/assets/25352560/cff981f8-76b0-49c9-abac-40c0854bebbc)

## References
- https://aws.amazon.com/compliance/shared-responsibility-model/

