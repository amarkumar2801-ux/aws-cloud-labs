 # AWS Auto Scaling Group with Application Load Balancer (ALB)

## Project Overview

This lab demonstrates how to build a highly available and scalable web application on AWS using Auto Scaling Group (ASG) and Application Load Balancer (ALB).

The infrastructure automatically launches new EC2 instances when CPU utilization increases and terminates unnecessary instances when traffic decreases.

---

## Architecture

```
                 Internet
                     │
                     ▼
      Application Load Balancer (ALB)
                     │
                     ▼
             Target Group (HTTP:80)
                     │
                     ▼
         Auto Scaling Group (ASG)
      Min = 2 | Desired = 2 | Max = 4
             │             │
             ▼             ▼
        EC2 Instance   EC2 Instance
        Apache Server  Apache Server

CloudWatch CPU Utilization
        │
        ▼
Target Tracking Scaling Policy (50%)
```

---

## AWS Services Used

- Amazon EC2
- Launch Template
- Auto Scaling Group
- Application Load Balancer
- Target Group
- Security Groups
- CloudWatch
- VPC
- Public Subnets
- Internet Gateway

---

## Lab Objectives

- Deploy Apache web servers using Launch Template.
- Create an Auto Scaling Group.
- Configure Application Load Balancer.
- Configure Target Group Health Checks.
- Configure Target Tracking Scaling Policy.
- Automatically launch new EC2 instances during high CPU utilization.
- Automatically terminate extra instances when load decreases.

---

## Security Groups

### ALB Security Group

| Rule | Port | Source |
|------|------|--------|
| HTTP | 80 | 0.0.0.0/0 |

---

### Web Server Security Group

| Rule | Port | Source |
|------|------|--------|
| SSH | 22 | My IP |
| HTTP | 80 | ALB Security Group |

---

## Auto Scaling Configuration

| Setting | Value |
|----------|-------|
| Desired Capacity | 2 |
| Minimum Capacity | 2 |
| Maximum Capacity | 4 |
| Scaling Policy | Target Tracking |
| CPU Target | 50% |
| Instance Warm-up | 300 Seconds |

---

## Lab Workflow

1. Create Launch Template.
2. Configure User Data to install Apache.
3. Create Target Group.
4. Create Application Load Balancer.
5. Create Auto Scaling Group.
6. Attach Target Group.
7. Configure Target Tracking Scaling Policy.
8. Verify two running EC2 instances.
9. Generate CPU load using stress.
10. Verify Auto Scaling launches a third EC2 instance.
11. Verify Target Group health checks.
12. Stop CPU load.
13. Verify ASG terminates extra instance automatically.

---

## Scaling Test

Install stress

```bash
sudo dnf install stress -y
```

Generate CPU Load

```bash
stress --cpu 2 --timeout 600
```

---

## Results

✔ Launch Template Created

✔ Target Group Healthy

✔ Application Load Balancer Active

✔ Auto Scaling Group Created

✔ Two EC2 Instances Running

✔ CPU Load Generated

✔ Third EC2 Automatically Launched

✔ Scale-In Successfully Terminated Extra Instance

---

## Screenshots

01 - Launch Template

02 - Launch Template User Data

03 - Security Groups (ALB)

03 - Security Groups (Web Server)

04 - Target Group

05 - Application Load Balancer

06 - ALB Listener

07 - Auto Scaling Group

08 - Scaling Policy

09 - Initial Running Instances

10 - Target Group Healthy

11 - SSH Login

12 - Second Instance

13 - ASG Activity

14 - Running Instances (Scale Out)

15 - Terminating EC2 Instance (Scale In)

---

## Author

Amarjeet Chaudhary

AWS Solutions Architect Associate (SAA-C03) Labs 