# Amazon Machine Image AMI - Amazon EC2

In the traditional infrastructure world, the process of getting a server up and running consists of installing an operating system from disks, drives or installation wizards over the network. In the AWS cloud, installing the operating system is not your responsibility. Instead, it is integrated into the AMI of your choice.

In addition, when you use an AMI, you can select storage mappings, architecture type (such as 32-bit, 64-bit or 64-bit ARM) and additional installed software.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/635c8f1a-477b-4299-816c-69439feae6a5">
</p>

## Relationship between AMIs and EC2 instances

EC2 instances are live instances of what is defined in an AMI, just like a cake is a live instance of a cake recipe. If you are familiar with software development, you can also see this type of relationship between a class and an object.

A class is something you model and define, while an object is something you interact with. In this case, the AMI is how you model and define the instance, while the EC2 instance is the entity you interact with, where you can install the web server and deliver content to users.

When you launch a new instance, AWS allocates a virtual machine running on a hypervisor. Next, the AMI you selected is copied to the root device volume, which contains the image used to boot the volume. In the end, you get a server to which you can connect and where you can install additional packages and software. In the example, you install a web server along with the properly configured source code of the employee directory application.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/6c64359a-a1fa-49b8-8aaa-b293a654354e">
</p>

One advantage of using AMIs is that they are reusable. You can choose a Linux-based AMI and configure the HTTP server, application packages and additional software you need to run the application. If you want to create a second EC2 instance with the same configurations, you could go through the entire instance creation and configuration process to match the configuration to the first instance. Alternatively, you could create an AMI from the running instance and use the AMI to start a new instance. In this way, the new instance would have the same settings as the current instance because the settings set in the AMIs are the same.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/c17a6e14-6717-4eaf-b401-c645182e433f">
</p>

