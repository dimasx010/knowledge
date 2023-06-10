# Deployment

## General

The Deployment tool is defined as a platform controller that has the task of offering declarative updates focused on the available ReplicaSets and pods

So, when a desired state is established in an object of this option, Deployment is in charge of carrying out, in a controlled manner, the transition between the current state of the object and the desired state indicated by the user. This implies that the pods in charge of this controller must reach this state

Among the main characteristic elements of Deployment is that it can also be defined for other tasks, such as the creation of new ReplicaSets resources, or eliminating all the existing Deployments in the system, while adopting all its resources with new Deployment controllers

It is also recommended not to directly manage the ReplicaSets resources that are part of a Deployment.

Another feature of this driver is that it has the ability to tell the Kubernetes system how to create or edit instances of pod resources that include a containerized application

This controller is also characterized by the ability to scale the number of replication pods, depending on the needs of the user's infrastructure, as well as contributing to the controlled implementation of code updates

Likewise, it has the ability to go to a previous version of Deployment in cases where it is required. It should be noted that each of these rollbacks updates the revision of the element.

This tool also has the property of automating the manual tasks and functions that tend to be repetitive and that are involved in the scaling and updating processes of the applications in production. This process automation can be translated into Deployments that run faster and have fewer errors in their activities

In addition, the status of this controller can be used to indicate that a certain deployment is stuck

Deployment is also characterized by allowing a number of different use cases within the platform. All of these cases should be covered when using the Deployment object

In addition to this, if it happens that the customer wants to deploy a use case that appears as not supported by the system, the option is available to open a new incident inside the main repository of the Kubernetes platform

_Some of the use cases normally performed by the Deployment controller are:_

## ReplicaSet deployment

One of the use cases of this controller is when the ReplicaSet is in charge of the creation of pod resources running in the background. In addition to this, the Deployment controller performs the function of verifying the deployment status of the resource in order to check whether it is ideal or not

## ReplicaSet cleaning

Another use case of the Deployment controller is that it allows you to clean up older ReplicaSet resources that are no longer needed in the system

## Scaling

Deployment also features horizontal scaling, which helps the controller increase its capacity to support different workloads

## Reference


![image](https://github.com/dimasx010/knowledge/assets/25352560/9b1c14de-9ec7-41d8-b9e6-c6b1a4e900d9)


