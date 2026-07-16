 # AWS ECS Fargate with Application Load Balancer & Auto Scaling

## Overview

This lab demonstrates how to deploy a Docker container stored in Amazon ECR using Amazon ECS Fargate with an Application Load Balancer (ALB). It also implements ECS Service Auto Scaling based on CPU utilization to automatically scale the application.

---

## Objective

- Deploy Docker image from Amazon ECR
- Create Amazon ECS Fargate Cluster
- Configure Task Definition
- Create ECS Service
- Integrate Application Load Balancer
- Configure Target Group & Health Checks
- Configure ECS Service Auto Scaling
- Access application through ALB DNS

---

## AWS Services Used

- Amazon ECS
- AWS Fargate
- Amazon ECR
- Application Load Balancer (ALB)
- Target Group
- Amazon CloudWatch
- ECS Service Auto Scaling
- IAM
- VPC
- Security Groups

---

## Architecture

Docker Image

↓

Amazon ECR

↓

Task Definition

↓

ECS Service

↓

Amazon ECS Cluster

↓

Application Load Balancer

↓

Target Group

↓

Running Tasks

↓

Internet Users

---

## Workflow

1. Store Docker image in Amazon ECR
2. Create ECS Cluster
3. Create Task Definition
4. Create Target Group
5. Create Application Load Balancer
6. Create ECS Service
7. Deploy Tasks using AWS Fargate
8. Configure Auto Scaling Policy
9. Access application using ALB DNS

---

## Auto Scaling Configuration

Minimum Tasks : 2

Desired Tasks : 2

Maximum Tasks : 4

Scaling Metric : ECS Service Average CPU Utilization

Target CPU : 70%

Scale-Out Cooldown : 60 Seconds

Scale-In Cooldown : 60 Seconds

---

## Features

- High Availability
- Load Balancing
- Automatic Health Checks
- Serverless Container Deployment
- Automatic Task Recovery
- Automatic Scaling
- Production Ready Architecture

---

## Result

Successfully deployed Nginx container using Amazon ECS Fargate with:

- Amazon ECR
- Application Load Balancer
- Target Group
- Auto Scaling
- Health Checks
- Multiple Running Tasks

Application successfully accessed through ALB DNS.

---

## Learning Outcome

- Amazon ECS
- AWS Fargate
- Task Definition
- ECS Service
- Amazon ECR
- Application Load Balancer
- Target Group
- Health Checks
- ECS Service Auto Scaling
- CloudWatch Metrics