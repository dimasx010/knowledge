# Amazon S3 - Amazon Simple Storage Service

Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. Customers of all sizes and industries can use Amazon S3 to store and protect any amount of data for a variety of use cases, such as data lakes, websites, mobile applications, backup and restore, archiving, enterprise applications, IoT devices, and big data analytics. Amazon S3 provides management capabilities so you can optimize, orchestrate, and configure access to your data to meet your specific business, organizational, and compliance requirements.

Amazon S3 offers several types of storage designed for different use cases. For example, you can store critical production data in S3 Standard for frequent access, save costs by storing infrequently accessed data in S3 Standard-IA or S3 One Zone-IA, and archive data at the lowest costs in S3 Glacier Instant Retrieval, S3 Glacier Flexible Retrieval, and S3 Glacier Deep Archive.

You can store data with changing or unknown access patterns in S3 Intelligent-Tiering, which optimizes storage costs by automatically moving data between four access tiers when access patterns change. It works with object storage in four access tiers: two low-latency access tiers optimized for frequent and infrequent access and two optional file access tiers designed for asynchronous access, which are optimized for unusual access.

For more information, see Using Amazon S3 Storage Classes. For more information about S3 Glacier Flexible Retrieval, see the Amazon S3 Glacier Developer Guide.

## Manage storage

Amazon S3 has storage management capabilities that you can use to manage costs, meet regulatory requirements, reduce latency, and store multiple different copies of your data to meet compliance requirements.

- S3 Lifecycle: Define lifecycle settings to manage objects and store them economically throughout their lifecycle. You can transition objects to other S3 storage classes or expire end-of-life objects.

- S3 Object Lock: Prevent Amazon S3 objects from being deleted or overwritten for a specified period of time or indefinitely. Object Lock can be used to meet regulatory requirements that require write-once read-multiple (WORM) storage or simply to add another layer of protection to prevent object changes and deletions.

S3 Replication - Replicate objects and their respective metadata and object tags to one or more target buckets in the same or different AWS Regions to reduce latency, compliance, security and other use cases.

S3 Batch Operations: Manage billions of objects at scale with a single S3 API request or with a few clicks in the Amazon S3 console. You can use Batch Operations to perform operations such asCopy, Lambda InvokeAWSFunction, andRestore on millions or billions of objects.

## The operating model would be as follows:

Amazon S3 is an object storage service that stores data as objects within buckets. An object is a file and any metadata that describes that file. A bucket is a container for objects.

To store data in Amazon S3, you must first create a bucket and specify a bucket name and AWS Region. Then you upload data to that bucket as objects in Amazon S3. Each object has a key(orKeyName), which is the unique identifier of the object within the bucket.

S3 provides features that you can configure to support your specific use case. You can use S3 Versioning to maintain multiple versions of an object in a bucket and restore objects that are accidentally deleted or overwritten.

Buckets and the objects they contain are private and can only be accessed if access permissions are explicitly granted. You can use bucket policies, AWS Identity and Access Management (IAM), access control lists (ACLs) and S3 access points to manage access.

## Amazon S3 Use Cases

Amazon S3 is a widely used storage service, with many more use cases than can fit on one screen. The following list summarizes some of the most common ways to use Amazon S3:

- Backup and storage - Amazon S3 is a natural place to back up files because it is highly redundant. As mentioned in the last unit, AWS stores EBS snapshots in S3 to take advantage of high availability.

- Media hosting: Because you can store unlimited objects and each individual object can be up to 5TB, Amazon S3 is an ideal place to host video, photo, and music uploads.

- Software delivery: You can use Amazon S3 to host software applications that customers can download.

- Data lakes: AmazonS3 is the optimal foundation for a data lake because of its virtually unlimited scalability. You can increase storage from gigabytes to petabytes of content and pay only for what you use.
Static websites: You can configure your S3 bucket to host a static website of HTML, CSS and client-side scripts.

Static content: Because of the unlimited scaling, support for large files, and the fact that you can access any object over the Web at any time, Amazon S3 is the perfect place to store static content.

## Choosing the right connectivity option for resources

Everything in Amazon S3 is private by default. It means that only the user or AWS account that created the resource can see all S3 resources, such as buckets, folders, and objects. Amazon S3 resources are private and protected to begin with.

If you decide that you want everyone on the Internet to see your photos, you can choose to make buckets, folders, and objects public. A public resource means that everyone on the Internet can see it. Most of the time, you don't want permissions to be all or nothing. Typically, you want to take a more granular approach to how you provide access to resources.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d38dd44c-3020-4f0b-9bc3-657a006ac0e5">
</p>

## Amazon S3 encryption

Amazon S3 enforces encryption in transit (as it travels to and from Amazon S3) and at rest. To protect data at rest, you can use encryption in the following ways:

- Server-side encryption: Allows Amazon S3 to encrypt the object before storing it on disks in your data centers, and then decrypt it as it downloads the objects.

- Client-side encryption: You can encrypt the client-side data and then upload the encrypted data to Amazon S3. In this case, you manage the encryption process, the encryption keys, and all related tools.

For encryption in transit, you can use client-side encryption or Secure Sockets Layer (SSL).

## Amazon S3 version control

As described above, Amazon S3 identifies objects in part by object name. For example, when you upload a photo of an employee to Amazon S3, you might name the object "employee.jpg" and store it in a folder named "employees". If you do not use Amazon S3 version control, every time you upload an object named "employee.jpg" to the employees folder, it will overwrite the original file.

This can be a problem for several reasons, including the following:

- The file name employee.jpg is a common name for an employee photo object. You or someone else who has access to the bucket may not have intended to overwrite it, but once overwritten, the original file cannot be accessed.

You may want to keep different versions of employee.jpg. Without version control, if you wanted to create a new version of employee.jpg, you would have to upload the object and choose another name for it. Having multiple objects with slight differences in naming variations can cause confusion and clutter in S3 buckets.

To counteract these problems, you can use S3 version control. Version control retains multiple versions of a single object in the same bucket. This preserves previous versions of an object without using different names, which helps to recover files from accidental deletions, accidental overwrites or application errors.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/48bf65b3-3935-47f6-bae4-ec4a388899a2">
</p>

If you enable version control for a bucket, Amazon S3 automatically generates a unique version ID for the object. In a bucket, for example, you can have two objects with the same key, but different version IDs, such as employeephoto.gif (version 111111) and employeephoto.gif (version 121212).

Version control-enabled buckets allow you to recover objects from accidental deletion or overwriting.

Deleting an object does not permanently remove the object. Instead, Amazon S3 places a marker on the object showing that you tried to delete it. If you want to restore the object, you can remove the marker, and the object is restored.

If you overwrite an object, it results in a new version of the object in the bucket. You still have access to previous versions of the object.

## Version control states

Buckets can have one of the following three states:

- No version (default): No new or current object in the bucket has a version.

- Version control enabled: Version control is enabled for all objects in the bucket.

- Version control suspended: Version control is suspended for new objects. None of the new objects in the bucket will have a version. However, all current objects retain object versions.

The version control status is applied to all objects in the bucket. Storage costs are incurred on all objects in the bucket, including all versions. To reduce the amount of your Amazon S3 bill, you may want to delete older versions of objects when they are no longer needed.

## Automating level transitions with object lifecycle management

If you keep manually moving objects, such as employee photos, from one storage layer to another, you may want to automate the process with a lifecycle policy. By defining a lifecycle policy setting for an object or a group of objects, you can choose to automate two actions: transition and expiration actions.

Transition actions define when objects should be moved to another storage class.

Expiration actions define when objects expire and when they should be permanently deleted.

For example, you can transition the objects to the S3 Standard - Infrequent Access storage class 30 days after creating them or archive the objects in the S3 Glacier storage class 1 year after creating them.

The following use cases are good options for lifecycle management:

- Periodic records: if you upload periodic records to a bucket, the application may need them for 1 week or 1 month. After that period, you may want to delete them.

- Data with changes in access frequency: Some documents are accessed frequently for a limited period of time. Subsequently, they will be accessed infrequently. At some point, you may not need real-time access to this data, but organization or regulatory requirements may require archiving for a specific period. After that period, you can delete it.