# Buckets - Amazon S3

In Amazon S3, you store objects in containers called "buckets". You cannot upload any object, not even a single snapshot, to Amazon S3 without first creating a bucket. When you create a bucket, you specify at least two details: the AWS region in which you want the bucket to be located and the bucket name.

To choose a region, you will typically select a region that you have used for other resources, such as compute. When you choose a region for the bucket, all objects you place in the bucket will be stored redundantly on multiple devices, in multiple availability zones. This level of redundancy is designed to provide Amazon S3 customers with 99.99999999999% durability and 99.99% availability for objects for a given year.

When you choose a bucket name, it must be unique across all AWS accounts. AWS prevents you from choosing a bucket name already chosen by someone else in another AWS account. Once you choose a name, that name is yours, and no one else can claim it unless you delete the bucket, which then frees the name for others to use.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d045922e-5251-4f9b-8074-4687c734695c">
</p>

AWS uses the bucket name as part of the object identifier. In S3, each object is identified by a URL as shown.

After http://, you can see the bucket name. In this example, the bucket is named doc. Next, the identifier uses the service provider and the s3 service name, amazonaws. After that, there will be an implicit folder inside the bucket named 2006-03-01 and the object inside the folder named AmazonS3.html. The object name is often referred to as the "key name".

There can be folders inside the buckets to help you organize the objects. However, remember that no real file hierarchy supports this on the backend. Instead, it is a flat structure where all files and folders are on the same level. The use of buckets and folders implies a hierarchy, which creates an understandable organization for users.

## S3 bucket policies

Like IAM policies, Amazon S3 bucket policies are defined in JSON format. The difference is that IAM policies are attached to users, groups and roles, while S3 bucket policies are only attached to S3 buckets. S3 bucket policies specify which actions are allowed or denied in the bucket.

For example, if you have a bucket named "employeebucket", you can attach an S3 bucket policy to it that allows another AWS account to place objects in that bucket.

Alternatively, if you want to allow anonymous readers to read employeebucket objects, you can apply a policy to that bucket that allows anyone to read the objects in the bucket via "Effect":Allow on the "Action:["s3:GetObject"]".

This is an example of what the S3 bucket policy would look like.

```json
{
"Version":"2012-10-17",
"Statement":[{
"Sid":"PublicRead",
"Effect":"Allow",
"Principal": "*",
"Action":["s3:GetObject"],
"Resource":["arn:aws:s3:::employeebucket/*"]
}]
}
```
S3 bucket policies can only be placed in buckets and cannot be used for folders or objects. However, the policy that is placed in the bucket applies to all objects in that bucket.

You should use S3 bucket policies in the following situations:

You need an easy way to access S3 between accounts, without using IAM roles.

Your IAM policies run up against the defined size limit. S3 bucket policies have a higher size limit.

