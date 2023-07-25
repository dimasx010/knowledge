# Amazon Elastic Block Store - Amazon EBS

Amazon Elastic Block Store (Amazon EBS) is an easy-to-use, scalable, high-performance block storage service designed for Amazon Elastic Compute Cloud (Amazon EC2).

In the following image we can analyze the schema of the mentioned service

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b9bad3e9-834a-4ed6-ab2b-d6997b3dbb98">
</p>

Amazon EBS also handles the creation of storage volumes so that they can be attached to Amazon EC2 instances. After this process, you can build file systems on top of the volumes, run a database, or assign them to one of the uses available for block storage, such as a hard disk.

The Amazon EBS system includes a series of properties and features that enable its operation, including its usefulness for working in situations where data must be kept accessible quickly and where long-term persistence is required.

It should also be noted that this tool offers different types of volumes, which are located in a certain availability zone, where they are automatically replicated in order to guarantee their protection against individual component errors. These volumes are also designed to offer high availability.

Amazon EBS billing is carried out taking into account only what is provisioned with the tool. Regarding volume storage, it is worth clarifying that these are billed according to the amount of GNs provisioned per month until the stored capacity is released. These costs may increase for volumes with special features, such as higher-than-reference throughput or supporting IOPS.


## Amazon EBS volume types

Amazon EBS volumes are organized into two main categories: solid state disks (SSDs) and hard disk drives (HDDs). SSDs provide high performance for random input and output (I/O), while HDDs provide high performance for sequential I/O. AWS offers two types of each.

The following chart can help you decide which EBS volume is the right choice for your workload.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/9ce19cc2-ee98-45e7-9425-be6a99ac9d47">
</p>

## Advantages of Amazon EBS

Here are the benefits of using Amazon EBS.

- High availability: When you create an EBS volume, it is automatically replicated to your Availability Zone to prevent data loss due to single points of failure.

- Data persistence: Storage persists even when the instance does not.

- Data encryption: All EBS volumes support encryption.

- Flexibility: EBS volumes support on-the-fly changes. You can change the volume type, volume size, and IOPS capacity without stopping the instance.

- Backups: Amazon EBS provides the ability to create backups of any EBS volume.

## Amazon EBS Snapshots

Mistakes happen. One mistake is not backing up data and then inevitably losing it. To prevent this from happening to you, always back up your data, even in AWS.

Because EBS volumes are made up of the data on your Amazon EC2 instance, you must back up these volumes, called "snapshots".

EBS snapshots are incremental backups that only keep the blocks of the volume that have changed after the most recent snapshot. For example, if you have 10 GB of data on a volume and only 2 GB of data has changed since the last snapshot, only the 2 GB that has changed is written to Amazon Simple Storage Service (Amazon S3).

When you take a snapshot of any of your EBS volumes, the backups are redundantly stored in multiple Availability Zones using Amazon S3. AWS manages this aspect of the backup storage in Amazon S3, so you do not have to interact with Amazon S3 to work with your EBS snapshots. You manage them in the Amazon EBS console, which is part of the Amazon EC2 console.

EBS snapshots can be used to create multiple new volumes, whether they are in the same Availability Zone or in a different Availability Zone. When you create a new volume from a snapshot, it is an exact copy of the original volume at the time the snapshot was taken.

## References
- https://aws.amazon.com/es/ebs/
- https://keepcoding.io/blog/que-es-amazon-ebs/
