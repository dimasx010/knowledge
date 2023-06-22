# AWS Amazon Virtual Private Cloud VPC

With Amazon Virtual Private Cloud (Amazon VPC), you can launch AWS resources in a logically isolated virtual network that you have defined. This virtual network is very similar to the traditional network you would use in your own data center, but with the benefits of using the scalable AWS infrastructure.

An example VPC is shown in the diagram below. The VPC has a subnet in each availability zone of the region, EC2 instances in each subnet, and an Internet gateway to enable communication between the resources in your VPC and the Internet.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/58a81e7c-b326-4ef9-87b3-d251112db03b">
</p>

## Features
The following features help you configure a VPC to provide the connectivity your applications need:

### Virtual private clouds (VPC)
A VPC is a virtual network virtually identical to a traditional network that could operate in your own data center. Once you have created a VPC, you can add subnets.

### Subnetworks
A subnet is a range of IP addresses in your VPC. A subnet must reside in a single Availability Zone. After adding subnets, you can deploy AWS resources from your VPC.

### IP Addressing
You can assign IP addresses, IPv4 and IPv6, to VPCs and subnets. You can also incorporate your public IPv4 and IPv6 GUA addresses into AWS and assign them to your VPC resources, such as EC2 instances, NAT gateways, and network load balancers.

### Routing
Use the routing tables to determine where network traffic is routed from your subnet or gateway.

### Gateways and connection points
A gateway connects your VPC to another network. For example, use an Internet gateway to connect your VPC to the Internet. Use a VPC connection point to connect to AWS Services privately, without the use of an Internet gateway or NAT device.

### Pairing connections
Use a VPC peering connection to route traffic between the resources of two VPCs.

### Traffic replication
Copy network traffic from network interfaces and send it to security and monitoring devices for deep packet inspection.

### Transit gateways
Use a transit gateway, which acts as a central hub, to route traffic between your VPCs, VPN connections and AWS Direct Connect connections.

### VPC flow logs
Flow logs capture information about incoming and outgoing IP traffic to and from network interfaces in your VPC.

### VPN connections
Connect your VPCs to on-premises networks using AWS Virtual Private Network (AWS VPN).

## References
- https://docs.aws.amazon.com/en_en/vpc/latest/userguide/what-is-amazon-vpc.html
