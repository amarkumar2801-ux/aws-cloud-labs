 # AWS SNS CloudWatch Alarm Lab

## 📌 Objective

The objective of this lab is to integrate Amazon CloudWatch with Amazon SNS to receive automatic email notifications whenever an EC2 instance crosses a predefined CPU utilization threshold.

---

## AWS Services Used

- Amazon EC2
- Amazon CloudWatch
- Amazon SNS

---

## Lab Overview

In this lab, a CloudWatch Alarm was integrated with an Amazon SNS topic. When the EC2 CPU utilization exceeded 50%, CloudWatch automatically triggered the alarm and Amazon SNS sent an email notification. When the CPU utilization returned below the threshold, CloudWatch changed the alarm state back to OK and another notification was sent.

---

## Lab Steps

### Step 1

Created an Amazon SNS Standard Topic.

### Step 2

Created an Email Subscription.

### Step 3

Confirmed the subscription through the confirmation email.

### Step 4

Published a test message to verify SNS email delivery.

### Step 5

Configured the existing CloudWatch Alarm to send notifications to the SNS topic.

### Step 6

Generated high CPU utilization using the Linux stress utility.

```bash
stress --cpu 2 --timeout 300
```

### Step 7

Verified that CloudWatch Alarm changed from:

```
OK
↓

IN ALARM
```

### Step 8

Verified that Amazon SNS automatically delivered an email notification.

### Step 9

After CPU utilization dropped below the threshold, verified that the alarm returned to:

```
IN ALARM
↓

OK
```

and Amazon SNS sent a recovery email.

---

## Screenshots

- SNS Topic Created
- Email Subscription Confirmed
- SNS Test Email
- CloudWatch Alarm Configuration
- CPU Utilization Spike
- CloudWatch Alarm - IN ALARM
- ALARM Email Notification
- OK Email Notification

---

## Key Learnings

- Amazon SNS Topics
- Email Subscription
- SNS Message Delivery
- CloudWatch Alarm Integration
- Automatic Email Notifications
- CPU Threshold Monitoring
- Production Alerting Workflow

---

## Result

Successfully integrated Amazon CloudWatch with Amazon SNS.

Verified automatic email notifications when the CloudWatch Alarm entered the **IN ALARM** state and again when the alarm returned to the **OK** state.

---

## Real-World Use Case

Production environments use CloudWatch and Amazon SNS to notify DevOps and Cloud Engineers whenever critical events such as high CPU utilization, memory issues, application failures, or infrastructure problems occur.

---

## Author

**Amarjeet Chaudhary**

AWS Cloud Engineer Portfolio