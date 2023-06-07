# Scaling

Cloud scalability in cloud computing refers to the ability to increase or decrease IT resources as needed to meet changing demand. Scalability is one of the hallmarks of the cloud and the primary driver of its exploding popularity with businesses.

## Vertical Scaling ⬆️

Vertical scaling has a lot to do with the application server hardware. It is achieved in a very simple way: by increasing the server's resources. Mainly in terms of processing power, memory and storage. This type of scaling is quite simple to achieve, since it only requires an intervention in the hardware of the equipment, increasing the resources or even changing the server completely. However, the benefit that can be obtained is also limited.

### Advantages
- Ease of implementation and configuration
- Does not require a specific design in the application and its architecture to work
- Can be more economical

### Disadvantages
- It is limited to the capacity of a single server
- It does not provide benefits in relation to high availability

## Horizontal scaling ➡️

Horizontal scaling is achieved by increasing the number of servers serving an application. To do this, a group of different servers is configured to handle requests together (this is called a cluster) and the workload is distributed among them through a balancer. Each of these servers is known as a node and scaling is done by simply adding a new node to the cluster

This scaling is much more powerful, but nevertheless requires more configuration to be done, not only to create the server network of a cluster, but also to realize an application architecture, at the software level, capable of adapting to this type of operation

### Advantages

- Scaling is virtually infinite
- Allows high availability
- Allows correct load balancing between servers

### Disadvantages

- Requires further configuration, which can be difficult to implement
- Requires the application to be built to support vertical scaling
- Although more powerful and better performing, it tends to be a less cost-effective option, as it requires multiple servers