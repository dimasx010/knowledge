# AWS Fargate

AWS Fargate technology can be used on Amazon ECS to run containers without having to manage servers or clusters of Amazon EC2 instances. With Fargate, you no longer have to provision, configure, or scale VM clusters to run your containers. This eliminates the need to choose server types, decide when to scale clusters, or optimize cluster sets.

By running Amazon ECS tasks and services with the Fargate launch type or a Fargate capacity provider, the application is packaged into containers, operating system, CPU and memory requirements are specified, IAM and networking policies are defined, and the application is launched. Each Fargate task has its own isolation boundary and does not share the underlying kernel, CPU resources, memory resources or elastic network interface with another task.

For information about the Fargate architecture, see Using the Fargate Launch Type in the Amazon Elastic Container Service Developer Guide.

This topic describes the different components of Fargate tasks and services, and mentions special considerations for using Fargate with Amazon ECS.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b245c481-a508-45ee-88b6-77673cf87412">
</p>

## Components

### Clusteres

An Amazon ECS cluster is a logical grouping of tasks or services. You can use clusters to isolate applications. When tasks run in Fargate, Fargate also manages the cluster resources.

### Task definitions

A task definition is a text file that describes one or more containers that make up the application. It is in JSON format. It can be used to describe up to ten containers. The task definition functions as a schema for your application. It specifies various parameters for the application. For example, you can use it to specify parameters for the operating system, which containers to use, which ports to open for the application, as well as which data volumes are to be used with the containers in the task. The specific parameters available for task definition depend on the needs of the specific application.

It is not necessary for the entire application stack to be in a single task definition. In fact, we recommend that you extend your application to several task definitions. For that, you can combine related containers into their own task definitions, each representing a single component.

### Tasks

A task is the instance created from a task definition within a cluster. After you create a task definition for your application within Amazon ECS, you can specify the number of tasks to run in the cluster. You can run a standalone task or run a task as part of a service.

### Servicies

You can use an Amazon ECS service to simultaneously run and maintain the desired number of tasks in an Amazon ECS cluster. The way it works is that, should any of the tasks fail or stop for any reason, the Amazon ECS service scheduler launches another instance based on the task definition. It does this to replace it to maintain the desired number of tasks in the service.

## References
- https://aws.amazon.com/es/fargate/
