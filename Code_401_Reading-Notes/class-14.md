# Event Driven Architecture

## [AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

### SNS

- *SNS* stands for Simple Notification Service
  - Uses a publisher / subscriber system
  - Delivers to many subscribers instantly and uses a fan out approach.

### SQS

- *SQS* stands for Simple Queue Sercive
  - This is a queueing service for message processing.
  - It can store the event and be accessed at a later time.
  - These events and messages must be polled by a client to be discovered.
  - Typically processed by a single consumer.

### When Should We Use Each One?

- Use SNS if other systems care about an event on a wider scale.
- Use SQS if your system cares about an event.
- Lets go over some examples of when we should use each.
  - Well when we look at a Credit Card Transaction flow this is what we see:
  - There is a purchase from a consumer that carries an object that looks similar to this:

```js
{
  "TransactionId": "3856294",
  "CustomerId": "CID_1345",
  "CustomerEmail": "test@test.com",
  "Amount": "50.00"
}
```

  - That is then sent to a transaction processing webservice
  - From there is needs authorization from a credit card authority service
  - Then send to the Transaction SNS topic.
  - From there the three different routes sent to are:
    - Customer Reminder Service(order was received!)
    - Transaction Analytics Queue
    - Transaction Fraud Detection Queue
