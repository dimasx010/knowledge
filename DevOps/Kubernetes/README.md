# Kubernetes information

## General
Kubernetes is a portable and extensible open source platform for managing workloads and services. Kubernetes facilitates automation and declarative configuration. It has a large and rapidly growing ecosystem. Support, tools and services for Kubernetes are widely available.


![image](https://github.com/dimasx010/knowledge/assets/25352560/476f131c-6005-4c00-a7a3-6867b917e4f0)

## What is?
Kubernetes has several features. You can think of Kubernetes as:

- A container platform
- A microservices platform
- A portable cloud platform

## Principal Kubernetes providersProviders
- Amazon Elastic Kubernetes Service (Amazon EKS)
- Azure Kubernetes Service (AKS)
- Google Kubernetes Engine (GKE)
- DigitalOcean Kubernetes (DOKS)

## Why?
When talking about services again, the power of autoscaling and administration is something extremely important, so with kubernetes we can perform in an optimal way all the administration of both scaling and management of our applications, using the tools based mainly on containers

## Characteristics
- [Pods (Minions)](https://github.com/dimasx010/knowledge/blob/main/DevOps/Kubernetes/Characteristics/Pods.md)
- [Clusters](https://github.com/dimasx010/knowledge/blob/main/DevOps/Kubernetes/Characteristics/Clusters.md)
- Services (Networking)
- Deployment
- [Nodes](https://github.com/dimasx010/knowledge/blob/nodo-kubernetes-profesional/DevOps/Kubernetes/Nodes.md)
- LoadBalancer (ingress and others)
- Package control(Helm)

## Benefits
- Multi environment with namespaces
- Agile application creation and deployment
- Continuous development, integration and deployment
- Separation of tasks between Dev and Ops
- Observability 
- Consistency between development, test and production environments
- Portability between clouds and distributions(MultiCloud)
- Distributed, elastic, loosely coupled, loosely coupled microservices
- Resource isolation
- Using package for Apps (Helm)

## Kubernetes != Docker
Yes, usually misunderstood the use or operation of kubernetes, so it is important to note that it can be used in conjunction with docker or without it, so they are two technologies with different responsibilities, one is primarily responsible for encapsulating applications and services (Docker) and another is responsible for the orchestration and deployment of containers (Kubernetes), in the culture of Docker and containers, Kubernetes would be the ship where they are running.

## Conclusion
Kubernetes is a technology that is here to stay, with so many projects based on microservices the rise in the use of cloud combined with containers, it is a perfect tool for the management and control of our projects at the operational level, even when it seems that the curve learning is a bit broad, once you have the concepts and practice, it is destroyed in our favorite tool.

## Referencias
- https://kubernetes.io/es/docs/concepts/overview/what-is-kubernetes/
- https://cloud.google.com/learn/what-is-kubernetes?hl=es-419#:~:text=Kubernetes%2C%20el%20servicio%20altamente%20confiable,comenzar%20a%20trabajar%20con%20facilidad.&text=La%20plataforma%20de%20modernizaci%C3%B3n%20de,de%20la%20nube%20como%20Kubernetes.
- https://www.redhat.com/en/topics/containers/what-is-kubernetes