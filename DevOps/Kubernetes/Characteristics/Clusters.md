# Clusters

## General

A Kubernetes cluster is a group of nodes (machines running applications). Each node can be a physical machine or a virtual machine. The node's capacity (its number of CPUs and amount of memory) is defined when the node is created

When creating a new cluster with Container Engine for Kubernetes, specify the type of cluster you want to create. You can specify

## A cluster comprises:

### Enhanced cluster

Enhanced clusters support all available features, including features not supported by basic clusters (such as virtual nodes, cluster add-on management, workload identity and additional worker nodes per cluster). Enhanced clusters come with a financially backed service level agreement (SLA)

### Basic cluster

Basic clusters support all of the core features provided by Kubernetes and Container Engine for Kubernetes, but none of the enhanced features provided by Container Engine for Kubernetes. Basic clusters include a service level objective (SLO), but no financially backed service level agreement (SLA)

## Keep the following in mind:

When using the console to create a cluster, if you do not select any enhanced features during cluster creation, you have the option to create the new cluster as a basic cluster. By default, a new cluster is created as an enhanced cluster, unless you explicitly choose to create a basic cluster

When using the CLI or API to create a cluster, you can specify whether you want to create a basic cluster or an enhanced cluster. If you do not explicitly specify the type of cluster to be created, a new cluster is created as a basic cluster by default

In the following image we can graphically analyze what the clusters would look like

![image](https://github.com/dimasx010/knowledge/assets/105082657/e59fe88d-412f-468c-af99-7fe98e116cf0)

## References
- https://docs.oracle.com/es-ww/iaas/Content/ContEng/Concepts/contengclustersnodes.htm#:~:text=Engine%20for%20Kubernetes.-,Clusters%20de%20Kubernetes,define%20al%20crear%20el%20nodo.