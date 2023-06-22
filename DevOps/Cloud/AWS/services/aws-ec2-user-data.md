# User-data - Amazon EC2

Basically User-data allows us to execute commands on the linux instance (EC2) during its launch.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/9437d8f0-923e-44ef-94a8-b7c7f173faa9">
</p>

When you launch an instance on Amazon EC2, you have the option to stream user data to the instance that can be used to perform common automated configuration tasks and even run scripts after the instance starts. You can pass two types of user data to Amazon EC2: shell scripts and cloud-init directives. You can also pass this data in the instance launch wizard as plain text, as a file (this is useful for launching instances with command line tools) or as base64 encoded text (for API calls). For example we can install a LAMP infra in the mentioned instance once we launch it.

## References
- https://docs.aws.amazon.com/en_en/AWSEC2/latest/UserGuide/user-data.html