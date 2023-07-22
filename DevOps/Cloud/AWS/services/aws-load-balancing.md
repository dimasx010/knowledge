# AWS Elastic Load Balancing

Elastic Load Balancing automatically distributes inbound traffic among multiple destinations, e.g. EC2 instances, containers and IP addresses in one or more Availability Zones. It monitors the health of registered destinations and routes traffic only to healthy destinations. Elastic Load Balancing automatically scales load balancer capacity in response to changes in incoming traffic.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/26fa183a-2316-43b4-8d33-88284343f02b">
</p>

## Benefits de AWS Elastic Load Balancing

A load balancer distributes workloads across multiple computing resources, such as virtual servers. Using a load balancer increases application availability and fault tolerance.

You can add and remove computing resources from your load balancer as needed without disrupting the overall flow of requests to applications.

You can configure health checks, which monitor the status of computing resources, so that the load balancer only sends requests to those that are healthy. You can also move encryption and decryption tasks to the load balancer, so that computing resources can focus on their core work.

## References
- https://docs.aws.amazon.com/es_es/elasticloadbalancing/latest/userguide/what-is-load-balancing.html
