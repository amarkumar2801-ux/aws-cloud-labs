 # AWS Simple Queue Service (SQS) Lab

## 📌 Objective

The objective of this lab is to understand how Amazon SQS works by creating a Standard Queue, sending messages, receiving messages using polling, understanding Visibility Timeout, monitoring Receive Count, and deleting messages after successful processing.

---

## AWS Services Used

- Amazon SQS

---

## Lab Overview

In this lab, a Standard Queue was created to simulate asynchronous message processing. Messages were sent to the queue, received using polling, observed during the Visibility Timeout period, and finally deleted after successful processing.

---

## Lab Steps

### Step 1

Created an Amazon SQS Standard Queue.

### Step 2

Sent a sample message to the queue.

Example:

```
Order ID: 1001
Customer: Amarjeet
Product: Laptop
Payment: Success
Status: Pending Dispatch
```

### Step 3

Received the message using **Poll for Messages**.

### Step 4

Observed the **Visibility Timeout** behavior.

The received message became temporarily invisible to other consumers for the configured timeout period.

### Step 5

Verified that the **Receive Count** increased when the message was not deleted and was received again after the Visibility Timeout expired.

### Step 6

Deleted the message after successful processing.

### Step 7

Verified that the queue became empty.

---

## Message Lifecycle

```
Producer
    │
    ▼
Send Message
    │
    ▼
Amazon SQS Queue
    │
    ▼
Receive (Poll)
    │
    ▼
Visibility Timeout
    │
    ▼
Delete Message
```

---

## Screenshots

- Queue Created
- Message Sent
- Message Received
- Visibility Timeout Demonstration
- Receive Count Increased
- Message Deleted
- Queue Empty

---

## Key Learnings

- Amazon SQS Standard Queue
- Producer and Consumer
- Message Queue
- Polling
- Visibility Timeout
- Receive Count
- Message Deletion
- Reliable Message Processing

---

## Result

Successfully created an Amazon SQS Standard Queue.

Verified the complete message lifecycle from sending a message to receiving, processing, and deleting it.

Observed Visibility Timeout behavior and Receive Count increment when the message was not deleted.

---

## Real-World Use Case

Amazon SQS is widely used to decouple applications.

Example:

- Order Processing
- Payment Processing
- Image Processing
- Background Jobs
- Microservices Communication
- Event-Driven Architectures

---

## Author

**Amarjeet Chaudhary**

AWS Cloud Engineer Portfolio