# Amazon Machine Image AMI - Amazon EC2
Amazon Elastic Compute Cloud (Amazon EC2) provides scalable compute capacity in the Amazon Web Services (AWS) cloud. Using Amazon EC2 eliminates the need to initially invest in hardware, so you can develop and deploy applications in less time. You can use Amazon EC2 to launch as many virtual servers as you need, configure security and networking, and manage storage. Amazon EC2 allows you to scale up or down to handle changes in requirements or spikes in popularity, reducing the need to forecast traffic.

Amazon EC2 offers the following features:

- Virtual computing environments, known as instances.

- Preconfigured templates for instances, known as Amazon Machine Images (AMIs), which package the parts you need for the server (including the operating system and additional software)

- Various CPU, memory, storage, and network capacity configurations for instances, known as instance types

- Secure login information for instances with key pairs (AWS stores the public key and you store the private key in a secure location)

- Storage volumes for temporary data that is deleted when an instance is stopped, terminated or put into hibernation, known as instance store volumes

Amazon EC2 offers the following features:

- Virtual computing environments, known as instances.

- Preconfigured templates for instances, known as Amazon Machine Images (AMIs), which package the parts you need for the server (including the operating system and additional software).

- Various CPU, memory, storage, and network capacity configurations for instances, known as instance types

- Secure login information for instances with key pairs (AWS stores the public key and you store the private key in a secure location)

- Storage volumes for temporary data that is deleted when an instance is stopped, terminated or put into hibernation, known as instance store volumes

- Persistent storage volumes for data using Amazon Elastic Block Store (Amazon EBS), known as Amazon EBS volumes

- Multiple physical locations for resources, such as Amazon EBS instances and volumes, known as availability regions and zones

- A firewall that allows you to specify the protocols, ports, and IP address ranges that instances can reach through the use of security groups

- Static IPv4 addresses for dynamic cloud computing, known as elastic IP addresses

- Metadata, known as tags, that you can create and assign to Amazon EC2 resources.

- Virtual networks that you can create that are logically isolated from the rest of the AWS cloud and that you can optionally connect to your own network, known as virtual private clouds (VPCs).

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/405e227c-fa26-4ac0-a01f-bc0eabf4625e">
</p>

## Amazon EC2 Instance Types

Amazon EC2 instances are a combination of virtual processors (vCPUs), memory, networking, and in some cases, graphics processing units (GPUs) and instance storage. When you create an EC2 instance, you have to choose how much of each of these components you need.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/90f014e1-0041-4d70-a711-c88d409aca1d">
</p>

AWS offers a variety of instances that differ in performance. Some instances provide more capacity than others. For general information about the capacity details of a particular instance, you should refer to the instance type. Instance types consist of a prefix that identifies the type of workloads they are optimized for, followed by a size. For example, the instance type c5.large can be broken down as follows:

- c5 defines the instance family and generation number. In this case, the instance belongs to the fifth generation of instances of an instance family optimized for generic computation.

- large sets the amount of capacity of the instance.

## EC2 instance locations

By default, EC2 instances are placed in a network called "Amazon Virtual Private Cloud (Amazon VPC) default". This network was created so that you can easily get started using Amazon EC2 without learning how to create and configure a VPC.

Any resources you place in the default VPC will be public and accessible over the Internet, so you should not place customer data or private information in it.

Once you are more familiar with networking in AWS, you should change this default configuration to choose your own custom VPCs and restrict access with additional routing and connectivity mechanisms.

## Design for high availability

In the network, the instance is in an Availability Zone of your choice. As you learned earlier, AWS services that are in the scope of the Availability Zone level must be designed with high availability in mind.

While EC2 instances are typically reliable, two is better than one, and three is better than two. Specifying instance size provides an advantage when designing the architecture because you can use a larger number of smaller instances instead of larger ones.

If your frontend only has a single instance and an instance error occurs, the application is disabled. On the other hand, if the workload is distributed across 10 instances and a failure occurs on one, you only lose 10 percent of your fleet, and application availability is barely affected.

When architecting any application for high availability, consider using at least two EC2 instances in two separate availability zones.

## EC2 instance lifecycle

An EC2 instance switches between different states from the time it is created until it is terminated.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4cba3a38-f3b5-4e38-93be-d288d776c614">
</p>

## Price

One of the ways to reduce costs with Amazon EC2 is to choose the right pricing option for running your applications. AWS offers three main purchasing options for EC2 instances: on-demand, reserved, and spot instances.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/f6afe37c-abd4-4ce1-9047-e761dada3616">
</p>

### Pay-per-use with on-demand instances

With on-demand instances, you pay for compute capacity with no long-term commitments. Billing starts when the instance is running and stops when the instance is in a stopped or terminated state. The price per second for a running on-demand instance is fixed.

For applications that require servers to run all the time, you are less likely to benefit from the on-demand pricing model, simply because there is no situation where you have to shut down the servers. For example, you may want the web server hosting the frontend of your corporate directory application to run 24 hours a day, every day so that users can access the website at any time. Even if there are no users logged on to your web site, you don't want to shut down the servers that support the site in the face of possible user activity.

If the servers cannot be stopped, consider using a reserved instance to save costs.

### Reserve capacity with reserved instances (RI)

RIs provide you with a significant discount compared to the price of On-Demand instances. RIs offer a discounted hourly rate and an optional capacity reservation for EC2 instances. You can choose from three payment options: full upfront payment, partial upfront payment or no upfront payment. You can select a 1-year or 3-year term for each of these options.

Depending on the option you choose, you receive a different discount.

Full prepayment offers a higher discount than partial down payment instances.
Partial down payment instances offer a greater discount than no down payment.
No down payment offers a higher discount than on-demand instances.
On-demand and no down payment instances are similar in that no down payment is required in either case. However, there is an important difference. When you choose an on-demand instance, you stop paying for the instance when you stop or terminate it. When you stop an IR, you continue to pay for it because you committed to a 1-year or 3-year term.

Reserved Instances are associated with an instance type and availability zone based on how you reserve them. The discount applied for a Reserved Instance purchase is not directly associated to a specific instance ID, but to an instance type.

### Cost savings with spot instances

Another way to pay for EC2 instances is through spot instances. Amazon EC2 spot instances allow you to leverage unused EC2 capacity in the AWS cloud. They are available at up to 90% discount compared to on-demand pricing.

With spot instances, you set a limit to the instance hourly payout. This is compared to the current spot price that AWS defines. If the amount you pay is higher than the current spot price and there is capacity, you will receive an instance. While these are very promising from a billing standpoint, you must take into account some architectural considerations to use them effectively.

One consideration is that the spot instance could be interrupted. For example, if AWS determines that capacity is no longer available for a particular spot instance or if the spot price exceeds the amount you are willing to pay, AWS will give you a 2-minute warning before interrupting the instance. This means that any application or workload running on a spot instance must be able to be interrupted.

Because of this unique consideration, inherently fault-tolerant workloads are often good candidates for use with spot instances. These include big data, containerized workloads, continuous integration and delivery (CI/CD), web servers, high-performance computing (HPC), image and media rendering, and other test and development workloads.