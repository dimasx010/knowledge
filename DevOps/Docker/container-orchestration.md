# Container orchestration

Container orchestration is the automation of most of the operations required to run workloads and services in containers. In large-scale systems, containerized applications become difficult to manage manually because they often include hundreds or even thousands of containers. Thus, container orchestration is essential to reduce the operational complexity of running containers

## Benefits of container orchestration 

- Reduces operational complexity when managing containers
- Improves security by reducing the potential for human error through automation
Enables automatic scaling and restarting of containers and clusters
- Helps IT teams automate some of the work and realize the full benefits of using containers

## Container system and popular orchestrators 

### Kubernetes

Kubernetes, also known as K8s, is an open source container system and orchestrator, originally designed by Google. Kubernetes is used to automate the deployment, scaling and management of containerized applications

[Kubernetes information](https://github.com/dimasx010/knowledge/tree/main/DevOps/Kubernetes)

### Docker Swarm

It is a tool that allows developers to deploy containers in swarm mode. A Swarm cluster consists of Docker Engine deployed on multiple nodes. Management nodes perform cluster orchestration and management. The worker nodes receive and execute tasks from the management nodes

### Nomad

Nomad es una herramienta de orquestación de cargas de trabajo de código abierto diseñada para desplegar y gestionar contenedores y aplicaciones no contenerizadas

### Apache Mesos

Apache Mesos is an orchestration platform that can run on Linux, Windows, and Mac OS X. It was initially developed at the University of California at Berkeley. Apache Mesos is used to manage clusters of nodes and runs on each node to manage resources and schedule data center tasks

## ECS(Elastic Container Service AWS)

Amazon Elastic Container Service (Amazon ECS) is a fully managed container orchestration service that makes it easy for you to deploy, manage, and scale containerized applications. Simply describe your application and the resources required, and Amazon ECS will launch, monitor, and scale it using flexible compute options with automatic integrations with other supported AWS services your application needs. Perform system operations, such as creating custom scaling and capacity rules, and view and query application log data and telemetry

