# AWS Elastic Load Balancing

Elastic Load Balancing automatically distributes inbound traffic among multiple destinations, e.g. EC2 instances, containers and IP addresses in one or more Availability Zones. It monitors the health of registered destinations and routes traffic only to healthy destinations. Elastic Load Balancing automatically scales load balancer capacity in response to changes in incoming traffic.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/aff38836-897f-4c8e-83ef-638564c95fc3">
</p>

## ELB Features

The ELB service provides a big advantage over using your own load balancing solution; primarily, you don't have to manage or operate it. You can distribute traffic from incoming applications across EC2 instances, containers, IP addresses, and AWS Lambda functions. Other key features include the following:

Since ELB can load balance on IP addresses, it can operate in hybrid mode, which means that it also load balances the servers on the premises.

ELB offers high availability. The only option you need to ensure is that the load balancer is deployed in multiple availability zones.

In terms of scalability, ELB automatically scales to meet the demand of incoming traffic. It manages incoming traffic and sends it to your backend application.

## Types of ELB

### Application load balancer (ALB)

These are some of the main features of the Application Load Balancer.

ALB routes traffic based on request data. ALB makes routing decisions based on the HTTP protocol, such as URL (/upload) path and host, HTTP headers and method, and the source IP address of the client. This enables granular routing to target groups.

ALB sends responses directly to the client. ALB has the ability to respond directly to the client with a fixed response, such as a custom HTML page. It can also send a redirect to the client, which is useful when it must redirect to a specific website or redirect a request from HTTP to HTTPS, so that it removes that work from the backend servers.

ALB uses TLS offloading. By talking HTTPS and avoiding the work of backend servers, ALB understands HTTPS traffic. To pass HTTPS traffic through ALB, an SSL certificate is provided by importing a certificate using IAM or AWS Certificate Manager (ACM) services or creating one for free with ACM. This ensures that traffic between the client and ALB is encrypted.

ALB authenticates users. With respect to the security issue, ALB can authenticate users before they are allowed to traverse the load balancer. ALB uses the OpenID Connect protocol and integrates with other AWS services to support protocols such as SAML, LDAP, Microsoft Active Directory, and so on.

ALB protects traffic. To prevent traffic from reaching the load balancer, you can configure a security group to specify supported IP address ranges.

ALB uses the rotating shift routing algorithm. ALB ensures that each server receives the same number of requests overall. This type of routing works for most applications.

ALB uses the least outstanding request routing algorithm. If requests to the backend vary in complexity where one request may need much more CPU time than another, the least pending request algorithm is more appropriate. It is also the appropriate routing algorithm to use if the destinations vary in processing capabilities. A pending request occurs when a request is sent to the backend server and a response has not yet been received.

For example, if the EC2 instances in a target group are not the same size, one server's CPU utilization will be higher than the other if the same number of requests are sent to each server using the rotating shift routing algorithm. That same server will also have more pending requests. Using the least outstanding request routing algorithm would ensure equal usage at all destinations.

ALB uses fast sessions. If requests must be sent to the same backend server because the application is stateful, use the fast session feature. This feature uses an HTTP cookie to remember on connections which server to send traffic to.

Finally, ALB is specific to HTTP and HTTPS traffic. If the application uses a different protocol, consider the network load balancer.

### Network Load Balancer (NLB)

These are some of the main features of the Network Load Balancer.

The Network Load Balancer supports TCP, UDP and TLS protocols. HTTPS uses TCP and TLS as protocols. However, NLB operates at the connection layer, so it does not understand what an HTTPS request is. It means that all the features needed to understand the HTTP and HTTPS protocol, such as routing rules based on that protocol, authentication and the least pending request routing algorithm, are not available with NLB.

NLB uses a stream hash routing algorithm. The algorithm is based on the following:

- Protocol
- Source IP address and source port
- Destination IP address and destination port
- TCP Sequence Number

If all parameters are the same, the packets are sent to exactly the same destination. If any of them are different in the following packets, the request could be sent to another destination.

NLB offers fast sessions. Unlike ALB, these sessions are based on the source IP address of the client, rather than on a cookie.

NLB supports TLS reassignment. NLB understands the TLS protocol. It can also remap TLS from backend servers, similar to the way ALB works.

NLB handles millions of requests per second. While ALB can also support this number of requests, it has to scale to reach that number. That takes time. NLB can instantly handle millions of requests per second.

NLB supports both static and elastic IP addresses. In some situations, an application client has to send requests directly to the load balancer's IP address instead of using DNS. For example, this is useful if the application cannot use DNS or if connecting clients require firewall rules based on IP addresses. In this case, NLB is the correct type of load balancer to use.

Natural language processing preserves the source IP address. NLB retains the source IP address of the client when sending traffic to the backend. With ALB, if you look at the source IP address of the requests, you will find the IP address of the load balancer. While with NLB, you would see the actual IP address of the client, required by the backend application in some cases.

### Selection among ELB types

The selection between ELB service types is made by defining which feature is required for the application. A list of the main features of load balancers is presented in the table.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/93f53569-20c8-4716-89c8-aa4b9618671f">
</p>

## References
- https://aws.amazon.com/es/elasticloadbalancing/
