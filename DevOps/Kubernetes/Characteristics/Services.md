# Services

## General

First we must highlight the motivation or goal of a service

Kubernetes Pods are created and destroyed to match the state of your cluster. Pods are non-permanent resources. If you use a Deployment to run your application, it can create and destroy Pods dynamically

Each Pod gets its own IP address, however, in a Deployment, the set of Pods running at a given time may be different from the set of Pods running that application a moment later

This leads to a problem: if one set of Pods (let's call them "backends") provides functionality to other Pods (let's call them "frontends") within your cluster, how do the frontends find and keep track of which IP address to connect to, so that the frontend can use the backend part of the workload?

In Kubernetes, a Service is an abstraction that defines a logical set of Pods and a policy by which to access them (sometimes this pattern is called a microservice). The set of Pods that a Service points to is usually determined by a Selector. To learn more about other ways to define Endpoints for a Service, see Services without selectors

For example, consider a stateless backend for processing images that is running with 3 replicas. These replicas are fungible; the frontends don't care which backend to use. While the actual Pods that make up the backend may change, the frontend clients should not be aware of it, nor should they keep track of the set of backends themselves

The Service abstraction enables this decoupling

Service in Kubernetes is a REST object, similar to a Pod. Like all REST objects, you can Post a Service definition to the API server to create a new instance. The name of a Service object must be a valid RFC 1035 name

For example, suppose you have a set of Pods where each one listens on TCP port 9376 and contains the tag app.kubernetes.io/name=MyApp:

```yaml
​apiVersion: v1
kind: Service
metadata:
  name: mi-servicio
spec:
  selector:
    app.kubernetes.io/name: MyApp
  ports:
    - protocol: TCP
      port: 80
      targetPort: 9376

```

Among the types of services we have:

## ClusterIP

When you create a service of type ClusterIP, Kubernetes creates a stable IP address that can be accessed from the nodes in the cluster. The following is a manifest for a ClusterIP type service:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-cip-service
spec:
  selector:
    app: metrics
    department: sales
  type: ClusterIP # Type of Service
  ports: # Network information
  - protocol: TCP
    port: 80
    targetPort: 8080

```

## NodePort

When you create a service of type NodePort, Kubernetes provides a nodePort value. The service can then be accessed using the IP address of any node along with the nodePort value.

Here is a manifest for a service of type NodePort:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-np-service
spec:
  selector:
    app: products
    department: sales
  type: NodePort # Type of Service
  ports:
  - protocol: TCP
    port: 80
    targetPort: 8080

```

## LoadBalancer

A load balancer is used to distribute the workload between different servers or applications and can be installed on a physical or virtual infrastructure. Load balancing software thus takes the form of an application delivery controller (ADC), allowing the user to automatically scale the load according to traffic forecasts

Load balancing, as we have just seen, is just one of the possible applications of the load balancer. This technology is also particularly useful for decongesting an SSL certificate, updating groups of applications or even routing your domains

There are two types of load balancers:

### L4 load balancers or network load balancers

These load balancers process layer 4 data that are present at the network and transport level (TCP/UDP). Thus, load balancers do not focus on application information, such as content type, cookies, headers location, etc., but redirect traffic based on network layer data.

### L7 load balancers or application load balancers

Unlike L4s, these balancers redirect traffic based on application layer parameters, so they handle a higher volume of data and use a larger amount of information, including, for example, HTTP, HTTPS and SSL protocols

## References
- https://kubernetes.io/docs/concepts/services-networking/service/
- https://www.ovhcloud.com/en/public-cloud/kubernetes/kubernetes-load-balancer/
