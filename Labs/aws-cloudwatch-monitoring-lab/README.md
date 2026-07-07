 # AWS CloudWatch Monitoring Lab

## Project Overview

This project demonstrates how to monitor an Amazon EC2 instance using Amazon CloudWatch. The lab covers enabling detailed monitoring, creating a CloudWatch Alarm, generating CPU load using the Linux `stress` utility, and observing automatic alarm state changes.

---

## Architecture

```
                    Amazon EC2 Instance
                           │
                  CPU Utilization Metrics
                           │
                           ▼
                  Amazon CloudWatch
                           │
                 CloudWatch Alarm
              Threshold > 50% CPU
                           │
          OK → IN ALARM → OK
```

---

## AWS Services Used

- Amazon EC2
- Amazon CloudWatch

---

## Lab Objectives

- Launch an EC2 instance
- Enable Detailed Monitoring
- Monitor CPU Utilization
- Create a CloudWatch Alarm
- Generate CPU Load using stress
- Observe Alarm State Changes

---

## Project Workflow

### Step 1

Launch an EC2 instance.

### Step 2

Enable Detailed Monitoring.

### Step 3

Connect to the instance using SSH.

### Step 4

Install the stress package.

```bash
sudo dnf install stress -y
```

### Step 5

Generate CPU load.

```bash
stress --cpu 2 --timeout 300
```

### Step 6

Monitor CPU Utilization in Amazon CloudWatch.

### Step 7

Create a CloudWatch Alarm.

Configuration:

- Metric: CPUUtilization
- Statistic: Average
- Threshold: Greater than 50%
- Evaluation Period: 1 Minute

### Step 8

Observe Alarm State

```
OK
↓
IN ALARM
↓
OK
```

---

## Screenshots

- EC2 Instance Running
- Detailed Monitoring Enabled
- Stress Command Running
- CPU Utilization Graph
- CloudWatch Alarm Created
- Alarm State - IN ALARM
- Alarm State - OK

---

## Learning Outcomes

- Amazon CloudWatch Metrics
- Detailed Monitoring
- CPU Monitoring
- CloudWatch Alarm
- Alarm Thresholds
- Alarm State Changes
- EC2 Performance Monitoring

---

## Result

Successfully monitored EC2 CPU utilization using Amazon CloudWatch.

Generated CPU load using the Linux stress utility.

Verified automatic CloudWatch Alarm state transitions:

- OK
- IN ALARM
- OK

---

## Future Enhancements

- Amazon SNS Email Notifications
- EC2 Auto Recovery
- Auto Scaling Integration
- CloudWatch Dashboard
- CloudWatch Logs
- EventBridge Integration

---

## Author

**Amarjeet Chaudhary**

AWS Cloud Engineer Portfolio