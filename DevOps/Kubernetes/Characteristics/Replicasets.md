# Replicasets

## General

The purpose of a ReplicaSet is to maintain a stable set of Pod replicas running at all times. Thus, it is used on numerous occasions to guarantee the availability of a specific number of identical Pods

A ReplicaSet is defined with fields, including a selector indicating how to identify the Pods it can acquire, a number of replicas indicating how many Pods it should manage, and a pod template specifying the data of the new Pods it should create to achieve the expected number of replicas. A ReplicaSet then achieves its purpose by creating and deleting as many Pods as necessary to reach the expected number. When a ReplicaSet needs to create new Pods, it uses its Pod template

The link that a ReplicaSet has to its Pods is through the Pod's field called metadata.ownerReferences, which indicates which resource owns the current object. All Pods acquired by a ReplicaSet have their own ReplicaSet identification information in their ownerReferences field. And it is through this link that the ReplicaSet knows the status of the Pods it is managing and acts accordingly

A ReplicaSet identifies the new Pods to be acquired using its selector. If there is a Pod that has no OwnerReference or where OwnerReference is not a controller, but matches the selector of the ReplicaSet, it will be immediately acquired by that ReplicaSet

A ReplicaSet ensures that a specified number of replicas of a Pod are running at all times. However, a Deployment is a higher level concept that manages ReplicaSets and provides declarative updates to the Pods along with many other useful features. Therefore, the use of Deployments is recommended over the direct use of ReplicaSets, unless you need a custom update orchestration or do not need the updates at all

## References
- https://kubernetes.io/es/docs/concepts/workloads/controllers/replicaset/
