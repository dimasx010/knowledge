# Terraform Modules

As you manage your infrastructure with Terraform, increasingly complex configurations will be created. There is no intrinsic limit to the complexity of a Terraform configuration file or directory, so you can write and update your configuration files in a single directory. However, if you do so, you may experience one or more of the following problems:

Understanding the configuration files and navigating through them will become increasingly difficult.

Updating the configuration will become increasingly risky, since updating one block could bring unexpected consequences to other blocks of your configuration.

Duplication of similar configuration blocks could increase, for example, when you set up separate development, test or production environments. This will increase the load when you update those parts of your configuration.

If you want to share parts of your configuration with other projects and teams, cutting and pasting configuration blocks in different projects could lead to errors and would be a difficult operation to maintain.

In this lab, you will discover how modules can take care of these problems, as well as the structure of a Terraform module and best practices for creating and using them.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/34cde74b-edb7-4bcc-849d-1d80a6dd6685">
</p>

## What are the modules for?

These are some of the ways in which the modules allow you to solve the problems listed above:

### Organize the configuration

Modules make it easy to navigate, understand and update your configuration by grouping related parts together. Even a moderately complex infrastructure may require hundreds or thousands of configuration lines to implement. However, if you use modules, you can organize your configuration into logical components.

### Encapsulate the configuration

Another benefit of using modules is that you can encapsulate the configuration into separate logical components. Encapsulation allows you to avoid unexpected consequences (e.g., a change in one part of your configuration modifying another infrastructure by accident) and reduces the likelihood of simple errors, such as using the same name for two different resources.

### Reuse the configuration

Writing your entire configuration without using existing code can be time-consuming and error-prone. Using modules, on the other hand, can save time and reduce costly errors by reusing the configuration written by you, other members of your team, or other Terraform professionals who have published modules for you to use. You can also share the modules you write with your team or the general public so they can benefit from your hard work.

### Provide consistency and ensure that best practices are followed

Modules also help you provide consistency in your configurations. Consistency makes complex configuration parameters easier to understand, and this ensures that best practices are applied throughout your configuration. For example, cloud service providers offer several options for configuring object storage services, such as Amazon S3 (Simple Storage Service) or Google Cloud Storage buckets. Many high-profile security incidents have involved object storage with protection errors. Due to the number of complex configuration options involved, it is easy to accidentally misconfigure these services.

## References
- https://www.plainconcepts.com/es/terraform/
- https://developer.hashicorp.com/terraform/language/modules