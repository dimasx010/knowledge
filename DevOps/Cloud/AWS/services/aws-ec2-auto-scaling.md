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

## References
- https://docs.aws.amazon.com/en_en/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html