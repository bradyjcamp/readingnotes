# AWS Events

## SQS and SNS Basics

- [Decouple and Scale Applications Using Amazon SQS and Amazon SNS](https://www.youtube.com/watch?v=UesxWuZMZqI)
- All modern applications utilize some sort of messaging system.
- This can be to the vender, company, or the consumer.

### Amazon SQS

- This is Amazon's Simple Queue Service
  - This is a queueing service for message processing.
  - It can store the event and be accessed at a later time.
  - These events and messages must be polled by a client to be discovered.
  - Typically processed by a single consumer.

### Amazon SNS

- This is Amazon's Simple Notification Service
  - Uses a publisher / subscriber system
  - Delivers to many subscribers instantly and uses a fan out approach.

## [AWS Differences Between SQS and SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

![Graph](../img/SQS-vs-SNS.png)

### Use Cases

- Choose SNS if:
  - You would like to be able to publish and consume batches of messages.
  - You would like to allow same message to be processed in multiple ways.
  - Multiple subscribers are needed.
- Choose SQS if:
  - You need a simple queue with no particular additional requirements.
  - Decoupling two applications and allowing parallel asynchronous processing.
  - Only one subscriber is needed.
  - [Quoted from medium.com](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)
  