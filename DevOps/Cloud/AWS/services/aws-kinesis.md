# AWS Kinesis

You can use Amazon Kinesis Data Streams to collect and process large streams of data records in real time. You can create data processing applications, known as Kinesis Data Streams Applications. A Kinesis Data Streams application reads data from a data stream as data records. These applications can use the Kinesis client library and can run on Amazon EC2 instances. You can send the processed logs to dashboards, use them to generate alerts, dynamically change pricing and advertising strategies, or send data to a variety of other AWSServices.

<p align="center">
  <img width="460" height="300" src="https://github.com/dimasx010/knowledge/assets/105082657/a6d3ee1b-1a23-4ae6-8ae2-404f1066e0a0">
</p>

While you can use Kinesis Data Streams to solve a variety of streaming data problems, one of its most common uses is real-time data aggregation, followed by loading the aggregated data into a data warehouse or MapReduce cluster.

The data is inserted into Kinesis data streams, ensuring durability and elasticity. The time between when a record is inserted into the stream and when it can be retrieved (put-to-getdelay) is typically less than 1 second. In other words, a Kinesis Data Streams application can start consuming stream data almost immediately after adding it. The managed service aspect of Kinesis Data Streams alleviates the operational burden of creating and running a data admission pipeline. You can create MapReduce-like streaming applications. The elasticity of Kinesis Data Streams allows you to scale the stream up or down so that you never lose data records before they are due.

Several Kinesis Data Streams applications can consume data from a stream, so that several actions can be performed simultaneously and independently, such as archiving and processing. For example, two applications can read data from the same stream. The first application calculates the running clusters and updates an Amazon DynamoDB table, while the second application compresses and archives data to a data store such as Amazon Simple Storage Service (Amazon S3). The DynamoDB table with the running clusters is passed to a dashboard, which reads it and produces up-to-the-minute reports.

The Kinesis Data Streams client library enables error-tolerant data consumption from streams and provides scaling support for Kinesis Data Streams applications.

## References
- https://docs.aws.amazon.com/en_en/streams/latest/dev/introduction.html

