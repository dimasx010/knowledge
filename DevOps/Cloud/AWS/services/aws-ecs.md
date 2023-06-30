#  Amazon Elastic Container Service ECS

Amazon ECS is an end-to-end container orchestration service that helps you activate new containers and manage them across a cluster of EC2 instances.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/dcf88406-bccb-4f30-bed4-93482a931f80">
</p>

To run and manage containers, you need to install the Amazon ECS container agent on your EC2 instances. This agent is open source and is responsible for communicating cluster management details to the Amazon ECS service. You can run the agent on Linux and Windows AMIs. An instance with the container agent installed is often referred to as a "container instance."


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/ca997b5b-4cb3-41cb-adfe-00d641a8cd39">
</p>

Once your Amazon ECS container instances are up and running, you can perform actions including, but not limited to, launching and stopping containers, obtaining cluster health, scaling down and scaling horizontally, scheduling container placement in the cluster, assigning permissions, and meeting availability requirements.

To prepare your application to run on Amazon ECS, create a task definition. The task definition is a text file in JSON format that describes one or more containers. A task definition is similar to a blueprint where you describe the resources required to run a container, such as networking, CPU, memory, ports, images, and storage information.

