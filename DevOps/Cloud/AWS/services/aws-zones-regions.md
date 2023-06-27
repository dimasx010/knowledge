# AWS Regions and Availability Zones

These locations are made up of so-called local zones, as well as AWS regions and availability zones. So although these terms are often worked together, each can be defined individually as follows:

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/c32efc96-f935-4e63-ab99-9ceaf3e24e8c">
</p>

## AWS Regions

AWS regions refer to independent geographic areas or physical locations where Amazon Web Service groups its data centers. It is here that the user can get their services up and running.

So each group of these logical data centers is known as an availability zone, and a single AWS infrastructure region includes two or more of these zones to provide its services.

AWS regions refer to separate geographic areas or physical locations where Amazon Web Service groups its data centers. This is where the user can pick up their services.

So each group of these logical data centers is known as an availability zone, and a single AWS infrastructure region includes two or more of these zones to provide its services.

Likewise, we must take into account a series of aspects to select the regions, which are as follows: 

- Compliance: we must analyze whether there is a delimitation in terms of data management according to a location, i.e., if we are working in Canada, and there is legislation that requires data to be stored in Canadian territory. 

- Latency: basically the less distance between users and infra in theory we would have better performance. 

- Prices: this may vary from one region to another. 

- Availability of services: we must see if the region contemplates the services we want. 

## AWS Availability Zones

Amazon Web Service AWS Availability Zones refers to one or more independent data centers with their own physical security, cooling and connection through redundant networks with very low latency and high bandwidth levels.

As we have already mentioned, the relationship between AWS availability regions and zones is that two or more zones must be in the same region in order for it to function.

It should be noted that these Amazon Web Service availability zones are sufficiently physically isolated from each other so that, in the event of electrical or operational failures in one of the zones, the other is not affected.

This isolation allows users to build their applications and deployments in a way that ensures they are highly available, as long as workloads are distributed across different availability zones.

In addition, these zones allow users to operate databases and multiple production applications with a high level of fault tolerance and scalability, and with two or more zones per region, these benefits are guaranteed to be greater than those offered by a single data center.

## References
- https://keepcoding.io/blog/regiones-y-zonas-de-disponibilidad-de-aws/
- https://aws.amazon.com/en/about-aws/global-infrastructure/?p=ngi&loc=1