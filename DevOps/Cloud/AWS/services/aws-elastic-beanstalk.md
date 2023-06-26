# AWS Elastic Beanstalk

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/fa28a398-7f4b-4989-a5bf-b1fa111b415e">
</p>

With Elastic Beanstalk, you can quickly deploy and manage applications in the AWS cloud without having to worry about the infrastructure that runs them. Elastic Beanstalk reduces management complexity without restricting choice and control. Simply upload the application and Elastic Beanstalk will automatically manage the details of capacity provisioning, load balancing, scaling and application health monitoring.

Elastic Beanstalk supports applications developed in Go, Java, .NET, Node.js, PHP, Python and Ruby. When you deploy your application, Elastic Beanstalk creates the selected supported platform version and provisions one or more AWS resources, such as Amazon EC2 instances, to run the application.

You can interact with Elastic Beanstalk through the Elastic Beanstalk console, the AWS Command Line Interface (AWS CLI), or eb, a higher-level CLI designed specifically for Elastic Beanstalk.

For more information on how to deploy a sample web application with Elastic Beanstalk, see Getting Started with AWS: Deploying a Web Application.

You can also perform most deployment tasks, such as resizing the Amazon EC2 instance fleet or monitoring the application, directly from the Elastic Beanstalk web interface (console).

To use Elastic Beanstalk, you must create an application, upload a version of the application as a source code package (for example, a Java.war file) to Elastic Beanstalk, and provide certain information about the application. Elastic Beanstalk automatically launches an environment and creates and configures the AWS resources needed to run the code. Once the environment is launched, you can manage it and deploy new versions of the application. The following diagram illustrates the Elastic Beanstalk workflow.

After you build and deploy your application, you can query information about it (for example, metrics, events, and the state of the environment) in the Elastic Beanstalk console, APIs, or command-line interfaces such as the unified AWS CLI.

## References
- https://docs.aws.amazon.com/en_en/elasticbeanstalk/latest/dg/Welcome.html


