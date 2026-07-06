 # AWS RDS + ALB + Auto Scaling Three-Tier Web Application

## Project Overview

This project demonstrates a production-style highly available web application architecture on AWS.

The application consists of:

- Amazon EC2 Web Servers
- Apache + PHP
- Amazon RDS MySQL Database
- Application Load Balancer (ALB)
- Target Group
- Auto Scaling Group
- Launch Template
- Custom VPC
- Public & Private Subnets
- Security Groups

The application retrieves employee records from an Amazon RDS MySQL database using PHP and displays them through an Application Load Balancer.

---

## AWS Services Used

- Amazon EC2
- Amazon RDS (MySQL)
- Application Load Balancer
- Target Group
- Auto Scaling Group
- Launch Template
- Amazon VPC
- Public & Private Subnets
- Security Groups
- Internet Gateway
- Route Tables

---

## Architecture

```
                Internet
                    │
                    ▼
      Application Load Balancer
                    │
          ┌─────────┴─────────┐
          │                   │
          ▼                   ▼
     EC2 Web Server      EC2 Web Server
      Apache + PHP       Apache + PHP
          │                   │
          └─────────┬─────────┘
                    │
             Amazon RDS MySQL
```

---

## Features

- Highly Available Architecture
- Automatic Load Balancing
- Auto Scaling
- Self Healing
- Centralized Database
- Dynamic PHP Application

---

## Project Workflow

1. Created Custom VPC
2. Created Public and Private Subnets
3. Launched EC2 Web Server
4. Installed Apache and PHP
5. Created Amazon RDS MySQL Database
6. Connected EC2 with RDS
7. Created Database and Employee Table
8. Developed PHP Application
9. Created Target Group
10. Created Application Load Balancer
11. Verified ALB Routing
12. Created Launch Template
13. Created Auto Scaling Group
14. Verified Automatic Instance Launch
15. Tested High Availability by terminating an EC2 instance

---

## Result

- Web application remained available after instance replacement.
- Auto Scaling automatically launched a new EC2 instance.
- Application successfully connected to Amazon RDS.
- High Availability achieved using ALB and Auto Scaling.

---

## Skills Demonstrated

- AWS Networking
- Amazon RDS
- Linux Administration
- Apache
- PHP
- MySQL
- Load Balancing
- Auto Scaling
- High Availability
- Production Architecture
