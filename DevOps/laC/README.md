# Infrastructure as code laC

Infrastructure as Code (IaC) allows the infrastructure to be managed and prepared through code, rather than through manual processes.

With this type of infrastructure, you create configuration files that contain the specifications you need, making it easy to edit and distribute configurations. It also ensures that you always prepare the same environment. Infrastructure as code codifies and documents your specifications to facilitate configuration management, and helps you avoid ad hoc and undocumented changes.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/6b72487b-895b-4c12-9875-6138b51f584b">
</p>

Version control is an important aspect of infrastructure-as-code that you should apply to your configuration files, just as you would to any other software source code file. Implementing infrastructure-as-code also allows you to break it into modular elements that will be combined in different ways through automation.

By automating infrastructure preparation with infrastructure-as-code, developers will not have to manually prepare and manage servers, operating systems, storage or any other elements each time they develop or deploy an application. Coding your infrastructure provides you with a template that you can follow during preparation. While it can still be done manually, an automation tool like Red Hat® Ansible® Automation Platform can do it for you.

## The difference between declarative and imperative approaches to Infrastructure as Code

There are two ways to approach Infrastructure as Code: through a declarative approach or an imperative approach. 

The declarative approach defines the desired state of the systems, which includes the resources you need and the properties those systems should have, and the Infrastructure as Code tool will take care of setting it up for you. 

It also lists the current state of your system objects, which makes it easier to disassemble the infrastructure.

In contrast, the imperative approach defines specific commands to achieve the desired configuration, which must be executed in the correct order. 

Many infrastructure-as-code tools use a declarative approach and will prepare the desired infrastructure automatically. Therefore, if you make changes to the desired state, a declarative IaC tool will implement them for you; but if you use an imperative tool, you must figure out how to apply those changes.

Most infrastructure-as-code tools can operate with both approaches, but tend to give priority to one of them.

## Advantages of Infrastructure as Code

Infrastructure preparation has always been a time-consuming and costly manual process. Today, its management has moved away from physical hardware in data centers, although it can still be part of the elements of your business, but in general there has been a move towards virtualization, containers and cloud computing. 

With the latter, the number of infrastructure elements increased and more applications began to be released to production on a regular basis. In addition, it requires the infrastructure to be commissioned, scaled up and taken down frequently. Without an Infrastructure-as-Code practice, it becomes increasingly difficult to manage the expansion of the current infrastructure.

Infrastructure-as-code allows your company to manage IT infrastructure needs while improving consistency and reducing errors and manual configuration.

### Advantages:
- Cost reduction
- Increased speed of implementation
- Decrease in the number of errors
- Increased uniformity of the infrastructure
- Elimination of configuration mismatches

## Referencias
- https://www.redhat.com/es/topics/automation/what-is-infrastructure-as-code-iac