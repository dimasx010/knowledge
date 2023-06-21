# AWS Simple Notification Service (SNS)

Amazon Simple Notification Service (Amazon SNS) is a managed service that provides message delivery from publishers to subscribers (also known as producers and consumers). Publishers communicate asynchronously with subscribers by sending messages to a topic, which is a logical access point and communication channel. Customers can subscribe to the SNS topic and receive published messages via a supported endpoint type, such as Amazon Kinesis Data Firehose, Amazon SQS, AWS Lambda, HTTP, email, mobile push notifications, and mobile text messages (SMS).

<p align="center">
  <img width="460" height="300" src="https://github.com/dimasx010/knowledge/assets/105082657/3fc37c2d-0b04-4015-b05f-181bc5483ae3">
</p>

## Basic features and functions

In Amazon SNS, you benefit from the following basic features and functions:

### Application-to-application messaging

Application-to-application messaging supports subscribers such as Amazon Kinesis Data Firehose delivery streams, Lambda functions, Amazon SQS queues, HTTP/S endpoints, and AWS event forking pipelines. For more information, see Using Amazon SNS for Application-to-Application (A2A) Messaging.

### Notifications of application to person

With application-to-person notifications, you provide user notifications to subscribers, such as mobile applications, cell phone numbers, and email addresses. For more information, see Using Amazon SNS for Application-to-Person (A2P) Messaging.

### Standard and FIFO issues

Use a FIFO topic to ensure strict message ordering, define message groups, and avoid message duplication. Only Amazon SQS FIFO queues can subscribe to a FIFO topic. For more information, see Message ordering and de-duplication (FIFO topics).

Use a standard topic when message delivery ordering and potential message duplication are not critical. All supported delivery protocols can subscribe to a standard topic.

### Durability of messages

Amazon SNS uses a number of strategies that work together to provide durability of messages:

### Published messages are stored in several servers and data centers separated by geographic area.

If a subscribed endpoint is not available, Amazon SNS runs a delivery retry policy.

To retain messages that are not delivered before the delivery retry policy ends, you can create a queue of failed messages.

### Message analysis and archiving

You can subscribe Kinesis Data Firehose delivery streams to SNS topics, allowing you to send notifications to other archiving and analytics endpoints, such as Amazon Simple Storage Service (Amazon S3) buckets, Amazon Redshift tables, and others.

### Message attributes

With message attributes, you can provide any arbitrary metadata about the message. Amazon SNS Message Attributes.

### Message filtering

By default, each subscriber receives all messages posted in the topic. To receive a subset of the messages, a subscriber must assign a filter policy to the topic subscription. A subscriber can also define the scope of the filtering policy to enable either payload-based or attribute-based filtering. The default value for the filter policy scope is MessageAttributes. When the attributes of the incoming message match the attributes of the filter policy, the message is delivered to the subscribed endpoint. Otherwise, the message is filtered. When the scope of the filtering policy is MessageBody, the attributes of the filtering policy are matched against the payload. For more information, see Filtering Messages in Amazon SNS.

### Message security

With server-side encryption, the contents of messages stored in Amazon SNS topics are protected using encryption keys provided by AWS KMS. For more information, see Encryption at Rest.

You can also establish a private connection between Amazon SNS and Virtual Private Cloud (VPC). For more information, see Network-to-Network Traffic Privacy.

## References
- https://docs.aws.amazon.com/en_en/sns/latest/dg/welcome.html
- https://docs.aws.amazon.com/en_en/sns/latest/dg/welcome-features.html
