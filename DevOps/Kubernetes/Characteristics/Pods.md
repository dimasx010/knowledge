# Pods (Minions)

## General
Pods are the smallest and most basic objects that can be deployed in Kubernetes. A pod represents a single instance of a running process in your cluster

Pods contain one or more containers, such as Docker containers. When a pod runs multiple containers, the containers are managed as a single entity and share pod resources

The pods also have shared network and storage resources for their containers

### Network

Pods are assigned unique IP addresses automatically. Pod containers share the same network namespace, including IP address and network ports. Containers in a pod communicate with each other within the pod on local communication

### Storage

Pods can specify a set of shared storage volumes that can be shared between containers

You can think of a pod as a self-contained, isolated "logical host" that owns the systemic needs of the application for which it runs

The purpose of a pod is to run a single instance of your application in your cluster. However, it is not recommended to create individual pods directly

## Pod life cycle

Pods are ephemeral. They are not designed to run forever and when a pod is terminated, it cannot be recovered. In general, pods do not disappear until a user or controller deletes them

Pods do not "heal" or repair themselves. For example, if a pod is programmed on a node that later fails, the pod is deleted. Similarly, a pod does not replace itself if it is ejected from a node for some reason

Each pod has a PodStatus API object, which is represented by a pod's status field. Pods publish their phase in the status: phase field. A pod's phase is a high-level summary of the pod's current state

When you run kubectl get pod to inspect a pod running in your cluster, the pod can be in one of the following phases:

- Pending: The cluster created and accepted the pod, but one or more of its containers are not yet running. This phase includes time spent programming on a node and downloading images
- Running: the pod was linked to a node and all containers were created. At least one container is running, is in the process of starting, or is being restarted
- Successful: all containers in the pod were successfully terminated. Finished pods are not restarted.
- Failed: all containers in the pod terminated and at least one container failed. A container "fails" if it exits with a non-zero status
- Unknown: The state of the pod cannot be determined

Because pods are ephemeral, it is not necessary to create pods directly. Similarly, because pods cannot repair or replace themselves, it is not recommended to create pods directly

Instead, you can use a controller, such as an Implementation, which creates and manages pods for you. Controllers are also useful for deploying updates, such as changing the version of an application running in a container, since the controller manages the entire update process for you

## Referencies
- https://cloud.google.com/kubernetes-engine/docs/concepts/pod?hl=es-419#:~:text=Google%20Kubernetes%20Engine.-,%C2%BFQu%C3%A9%20es%20un%20pod%3F,como%20los%20contenedores%20de%20Docker.