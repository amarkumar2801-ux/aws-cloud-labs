 # AWS Application Load Balancer (ALB) Lab

## Overview

This lab demonstrates how to deploy two EC2 web servers behind an AWS Application Load Balancer (ALB) for high availability and traffic distribution across multiple Availability Zones.

The ALB automatically distributes incoming HTTP requests to healthy EC2 instances registered in the Target Group.

---

## Architecture

```
                 Internet
                     │
                     ▼
      Application Load Balancer (ALB)
                     │
              Target Group (HTTP)
               ┌─────────────┐
               │             │
               ▼             ▼
        EC2 Web Server 1  EC2 Web Server 2
          Public AZ-1a      Public AZ-1b
```

---

## AWS Services Used

- Amazon VPC
- Public Subnets
- Internet Gateway
- Route Tables
- Security Groups
- Amazon EC2
- Application Load Balancer (ALB)
- Target Group

---

## Lab Objectives

- Create an Internet-facing Application Load Balancer
- Launch two Apache web servers
- Register EC2 instances in a Target Group
- Configure Health Checks
- Verify traffic distribution through the ALB

---

## Network Configuration

| Resource | Configuration |
|----------|---------------|
| VPC | 10.0.0.0/16 |
| Public Subnet 1 | 10.0.1.0/24 |
| Public Subnet 2 | 10.0.3.0/24 |

---

## EC2 Configuration

### Web Server 1
- Amazon Linux 2023
- Apache HTTP Server
- Custom Web Page

### Web Server 2
- Amazon Linux 2023
- Apache HTTP Server
- Custom Web Page

---

## Load Balancer Configuration

| Setting | Value |
|---------|-------|
| Type | Application Load Balancer |
| Scheme | Internet-facing |
| Listener | HTTP (80) |
| Target Group | web-tg |
| Health Check | HTTP |

---

## Security Groups

### ALB Security Group
- HTTP (80) from Anywhere

### EC2 Security Group
- HTTP (80) from ALB Security Group
- SSH (22) from My IP

---

## Verification

- Open the ALB DNS name in a browser.
- Refresh the page multiple times.
- Observe traffic being served by both EC2 instances.
- Confirm that all targets are Healthy.

---

## Learning Outcomes

- Application Load Balancer
- Target Groups
- Health Checks
- High Availability
- Multi-AZ Deployment
- Traffic Distribution
- VPC Networking
- EC2 Web Hosting

---

## Result

Successfully deployed an Application Load Balancer that distributes incoming traffic across two EC2 web servers running in different Availability Zones.