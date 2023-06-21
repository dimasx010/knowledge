# AWS Simple Queue Service (SQS) 

Amazon Simple Queue Service, also known as Amazon SQS, is one of the services offered by the AWS infrastructure and focuses on message queue management.

The Amazon SQS tool stands out as the oldest service of Amazon Web Service and is characterized by the fact that it is completely managed by the system.

In addition, this service enables the tuning and decoupling of the scale of distributed systems, serverless applications and microservices.

<p align="center">
  <img width="460" height="300" src="https://github.com/dimasx010/knowledge/assets/105082657/9733a979-75a7-447a-96cf-eadf094e5d6c">
</p>

Other important features of Amazon SQS include:

## Fully managed

One of the main features of Amazon Simple Queue Service is that it is fully managed by the AWS cloud infrastructure, which means that it avoids the hassle and overhead associated with managing and operating message-oriented middelware. This helps developers using its services to focus on their activities and differentiation of work.

### Amazon SQS API

One of the features of Amazon SQS is that it includes the option of a generic web services API Application Programming Interface, allowing access through any of the programming languages supported by the AWS SDK.

### Durability

Amazon SQS stores messages on multiple servers to ensure durability and security.

### Reliability

Amazon Simple Queue Service is also responsible for blocking messages during processing so that different producers can send messages while multiple consumers can receive them.

### Other features

Other relevant features of the Amazon Simple Queue Service include:

- Scales from 1 message per second to 10,000 per second.
- Default retention: 4 days, maximum 14 days.
- No limits on the number of messages that can exist.
- Low latency (10ms to publish and receive).
- Allows scaling horizontally with the number of consumers.
- Can have duplicate messages.
- Can include messages in disorder.
- Set a limit of 256 KB per message sent.

## References
- https://docs.aws.amazon.com/en_en/sns/latest/dg/welcome.html
- https://docs.aws.amazon.com/en_en/sns/latest/dg/welcome-features.html
