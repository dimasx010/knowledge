# OpenShift - Service Mesh

A service mesh, such as the open source Istio project, is used to control the exchange of data between the different parts of an application. Unlike other systems that also manage this communication, the service mesh is a visible and specific layer of the infrastructure integrated to the application, which can record whether the different parts interact well or not, in order to facilitate the optimization of communications and avoid downtime as an application grows.

The parts of the application are called a "service" and depend on each other to provide users with what they want. If someone uses an online store's application to buy a product, they need to know if the item is available. Therefore, the service that connects to the company's inventory database must communicate with the product's web page, which in turn must communicate with the user's online shopping cart. If the store wants to offer more benefits, it could design a service that recommends products to users within the application. This new service will communicate with a database of product tags to provide recommendations and, in addition, it should communicate with the same inventory database that the product page needed; in other words, it is a large number of independent and reusable parts.

Modern applications are often divided up in this way: as a network of services in which each service performs a specific business function. But what happens if some services, such as the retail store's inventory database, are overloaded with requests? Then the service mesh comes into play, which directs requests from one service to another to optimize the joint operation of the parts.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/686934c2-c697-4bae-aca7-22c9e3d24848">
</p>

## Operation of service grids

The service mesh does not add new functionality to the application runtime environment; applications always need rules that specify how requests are transferred from point A to B, regardless of their architecture. What distinguishes the service mesh is that the rules governing communication between services are not found within each service, but are extracted and placed in an infrastructure layer.

To this end, the service mesh is integrated into the application as a set of network proxies. Proxies are a common concept in enterprise IT: if you access this web page from a work computer, it is very likely that you have used a proxy.

When the request for this page is sent, it is first received by your company's web proxy.

Once the request passes the proxy's security measure, it is sent to the server hosting this page.

The page is then returned to the proxy and rechecked for security measures.

Finally, it is sent from the proxy to you.

In a service mesh, requests are sent between microservices by proxies in their own infrastructure layer. For this reason, the individual proxies that form a service mesh are sometimes referred to as "sidecars," since they run alongside, rather than within, each of the services. Together, these sidecar proxies, which are separate from each service, form a network.

Without a mesh of services, each microservice must be coded to include the rules that will govern communication between services, which distracts developers from business goals. It also means that communication errors are more difficult to diagnose because the rules for communication between services are hidden within each service.