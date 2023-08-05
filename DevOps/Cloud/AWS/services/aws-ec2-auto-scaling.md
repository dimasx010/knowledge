# Auto-Scaling - Amazon EC2

Amazon EC2 Auto Scaling helps ensure that you have the right number of Amazon EC2 instances available to handle your application load. It creates collections of EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling will ensure that the group never has fewer than those instances. You can specify the maximum number of instances in each Auto Scaling group and Amazon EC2 Auto Scaling will ensure that the group never has more than those instances. If you specify the desired capacity, when you create the group or later, Amazon EC2 Auto Scaling will ensure that the group has that number of instances. If you specify scaling policies, Amazon EC2 Auto Scaling can launch or terminate instances as your application demand increases or decreases.

For example, the following Auto Scaling group has a minimum size of one instance, a desired capacity of two instances, and a maximum size of four instances. The scaling policies you define adjust the number of instances, in minimum and maximum number of instances, based on the criteria you specify.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/a1c3e2ac-b718-43df-a169-01d80445df21">
</p>

## Benefits

Adding Amazon EC2 Auto Scaling to your application architecture is one way to get the maximum benefit from the AWS cloud. When you use Amazon EC2 Auto Scaling, your applications enjoy the following benefits:

- Improved fault tolerance. Amazon EC2 Auto Scaling can detect when an instance is down, terminate it, and launch an instance to replace it. You can also configure Amazon EC2 Auto Scaling to use multiple Availability Zones. If one Availability Zone becomes unavailable, Amazon EC2 Auto Scaling can launch instances in another to compensate.

- Better availability. Amazon EC2 Auto Scaling can help you ensure that your application always has adequate capacity to handle current traffic demand.

- Better cost management. Amazon EC2 Auto Scaling can dynamically scale capacity up and down as needed. Since you pay for the EC2 instances you use, you can save money by launching instances when you need them and terminating them when they are no longer needed.

## Configuration of EC2 Auto Scaling components

The three main components of EC2 Auto Scaling are as follows:

Configuration or Launch Template: Which resource should be automatically scaled?

EC2 Auto Scaling Group: Where should resources be deployed?

Scaling policies: When should resources be added or removed?

### Launching templates

Several parameters are required to create EC2 instances: Amazon Machine Image (AMI) ID, instance type, security group, additional Amazon Elastic Block Store (EBS) volumes, and more. EC2 Auto Scaling also requires all of this information to create the EC2 instance on your behalf when it needs to scale. This information is stored in a launch template.

You can use a launch template to manually launch an EC2 instance. You can also use it with EC2 Auto Scaling. It also supports version control, which allows you to quickly do a restore if there is a problem or you need to specify a default version. This way, while iterating on a new version, other users can continue to launch EC2 instances via the default version until you make the necessary changes.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2a07da81-0375-4fbf-b62c-d524771d495d">
</p>

You can create a launch template in one of three ways.

The fastest way to create a template is to use a current EC2 instance. The entire configuration is already defined.

Another option is to create a template from a current or previous version of a release template.

The last option is to create a template from scratch. The following options must be defined: AMI ID, instance type, key pair, security group, storage, and resource tags.

Another way to define what Amazon EC2 Auto Scaling has to scale is through a launch configuration. This is similar to the launch template, but does not allow version control when using a previously created launch configuration as a template. It also does not allow you to create it from a current EC2 instance. For these reasons, and to ensure that you get the latest Amazon EC2 features, AWS recommends using a release template instead of a release configuration.

### EC2 Auto Scaling Groups

The next component that EC2 Auto Scaling requires is an EC2 Auto Scaling group. An Auto Scaling group helps you define where EC2 Auto Scaling deploys its resources. This is where you specify Amazon VPC and the subnets on which the EC2 instance should be launched. EC2 Auto Scaling takes care of creating the EC2 instances on the subnets, so select at least two subnets that are in different availability zones.

With Auto Scaling groups, you can specify the type of purchase for EC2 instances. You can use on-demand only, spot only, or a combination of the two, allowing you to leverage spot instances with minimal administrative overhead.

To specify how many instances to launch EC2 Auto Scaling, you have three capacity settings to configure the group size.

Minimum: refers to the minimum number of instances running in the Auto Scaling group, even if the threshold for reducing the number of instances is reached.

Maximum: indicates the maximum number of instances running in the Auto Scaling group, even if the threshold for adding new instances is reached.

Desired capacity: indicates the number of instances that should be in the Auto Scaling group. This number can only be close to or equal to the minimum or maximum. EC2 Auto Scaling automatically adds or removes instances to match the desired capacity number.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d5fee1eb-8bb1-4720-98b7-2e7791bfa82e">
</p>

When EC2 Auto Scaling removes EC2 instances because traffic is minimal, it continues to remove EC2 instances until it reaches a minimum capacity. Depending on the application, using a minimum of two is a good idea to ensure high availability, but you know how many EC2 instances your application requires as a minimum at all times. When that limit is reached, even if EC2 Auto Scaling is instructed to remove an instance, it does not do so to ensure that the minimum is maintained.

On the other hand, when traffic continues to increase, EC2 Auto Scaling keeps adding EC2 instances. It means that the cost of your application will also continue to increase. That's why you should set a maximum amount to make sure you don't go over budget.

The desired capacity is the number of EC2 instances that EC2 Auto Scaling creates at the time the group is created. If that number decreases, EC2 Auto Scaling deletes the oldest instance by default. If that number increases, EC2 Auto Scaling creates new instances via the launch template.

### Availability with EC2 Auto Scaling

Different minimum, maximum and desired capacity numbers are used to dynamically adjust the capacity. However, if you prefer to use EC2 Auto Scaling for fleet management, you can set all three settings to the same number, for example four, as shown in the image. EC2 Auto Scaling will ensure that if an EC2 instance becomes unhealthy, it replaces it to ensure that there are always four EC2 instances available. This ensures high availability for your applications.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/8ca5ac45-3bcc-40d0-8fd4-91927390a82c">
</p>

Automation with scaling policies

By default, an Auto Scaling group will be kept at the initial desired capacity. While it is possible to manually change the desired capacity, you can also use scaling policies.

In the AWS Monitoring module, you learned about Amazon CloudWatch metrics and alarms. Metrics are used to keep information about various attributes of the EC2 instance, such as CPU percentage. Alarms are used to specify an action when a threshold is reached. Metrics and alarms are what scaling policies use to know when to take action. For example, you can configure an alarm to indicate when CPU utilization exceeds 70% across the fleet of EC2 instances and trigger a scaling policy to add an EC2 instance.

Three types of scaling policies are available: simple scaling, step scaling, and target tracking.

Simple escalation policy

A simple escalation policy allows you to do exactly what is described in this module. It uses a CloudWatch alarm and specifies what to do when it is triggered. This can be a number of EC2 instances to add or remove, or a specific number on which to set the desired capacity. You can specify a percentage of the pool instead of using a number of EC2 instances, which makes the pool grow or shrink faster.

Once the scaling policy is enabled, wait for a recovery period before taking any further action. This is important because EC2 instances take time to start up, and the CloudWatch alarm could be triggered while the EC2 instance is starting up. For example, you might decide to add an EC2 instance if the CPU utilization across all instances exceeds 65%. You do not want to add more instances until the new EC2 instance accepts the traffic. However, what would happen if the CPU utilization exceeded 85% in the Auto Scaling group? Adding an instance may not be the right decision. Instead, you may want to add another step in the scaling policy. Unfortunately, a simple scaling policy can't help with that.

Stepwise scaling policy

This is where a step escalation policy is useful. Stepwise scaling policies respond to additional alarms even while a scaling activity or status check replacement is in progress. As in the previous example, you could decide to add two more instances when CPU utilization is 85% and four more instances when it is 95%.

Deciding when to add and remove instances according to CloudWatch alarms might seem like a difficult task. That's why there is the third type of scaling policy: target tracking.

Target tracking scaling policy
If the application scales based on average CPU utilization, average network utilization (in or out) or request count, this type of scaling policy is the one to use. All you have to provide is the target value to be tracked, and the necessary CloudWatch alarms are automatically created.

## References
- https://docs.aws.amazon.com/en_en/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html