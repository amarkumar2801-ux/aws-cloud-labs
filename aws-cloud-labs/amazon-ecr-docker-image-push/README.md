 # Amazon ECR - Push Docker Images

## 📌 Project Overview

This lab demonstrates how to push Docker images from an Amazon EC2 instance to Amazon Elastic Container Registry (ECR).

Amazon ECR is a fully managed container registry service provided by AWS that securely stores, manages, and distributes Docker container images.

In this lab, local Docker images were authenticated, tagged, and pushed to an Amazon ECR private repository.

---

## 🎯 Objective

- Understand Amazon ECR
- Create a Private ECR Repository
- Configure AWS CLI
- Authenticate Docker with Amazon ECR
- Tag Docker Images
- Push Images to Amazon ECR
- Verify Images in AWS Console

---

## 🏗️ Architecture

```
                Amazon EC2
                     │
                     ▼
          Local Docker Images
         (nginx / httpd)
                     │
                     ▼
            AWS CLI Authentication
                     │
                     ▼
              Docker Login to ECR
                     │
                     ▼
                 Docker Tag
                     │
                     ▼
                Docker Push
                     │
                     ▼
        Amazon Elastic Container Registry
```

---

## Technologies Used

- Amazon EC2
- Amazon Linux 2023
- Docker Engine
- AWS CLI v2
- Amazon Elastic Container Registry (ECR)

---

## Lab Steps

### Step 1

Verify Docker Images

```bash
docker images
```

---

### Step 2

Create Amazon ECR Repository

Repository Name

```
nginx-repository
```

---

### Step 3

Authenticate Docker

```bash
aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin <ACCOUNT_ID>.dkr.ecr.ap-south-1.amazonaws.com
```

---

### Step 4

Tag Local Image

```bash
docker tag nginx:latest <ACCOUNT_ID>.dkr.ecr.ap-south-1.amazonaws.com/nginx-repository:latest
```

---

### Step 5

Push Image

```bash
docker push <ACCOUNT_ID>.dkr.ecr.ap-south-1.amazonaws.com/nginx-repository:latest
```

---

### Step 6

Verify Image

AWS Console

Amazon ECR

↓

Repository

↓

Images

---

## Commands Used

```bash
docker images

aws configure

aws sts get-caller-identity

aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin <ACCOUNT_ID>.dkr.ecr.ap-south-1.amazonaws.com

docker tag nginx:latest <ACCOUNT_ID>.dkr.ecr.ap-south-1.amazonaws.com/nginx-repository:latest

docker push <ACCOUNT_ID>.dkr.ecr.ap-south-1.amazonaws.com/nginx-repository:latest
```

---

## Screenshots

- ECR Dashboard
- Repository Details
- View Push Commands
- Login Succeeded
- Docker Images
- Docker Push Success
- Images Available in Amazon ECR

---

## Key Learnings

- Amazon ECR is a private container registry.
- Docker images must be authenticated before pushing.
- Docker Tag creates a new reference to an existing image.
- Docker Push uploads local images to Amazon ECR.
- One repository can contain multiple image tags (versions).
- Amazon ECS and Amazon EKS pull images directly from Amazon ECR.

---

## Interview Questions

### What is Amazon ECR?

Amazon Elastic Container Registry (ECR) is a fully managed AWS container registry used to securely store and manage Docker images.

### Why is docker tag required?

Docker tag assigns an ECR repository URI to a local Docker image before pushing it to Amazon ECR.

### Difference between Docker Hub and Amazon ECR?

Docker Hub is a general-purpose container registry, whereas Amazon ECR is an AWS-managed registry tightly integrated with ECS and EKS.

---

## Outcome

Successfully authenticated Docker with Amazon ECR, tagged local Docker images, pushed them to Amazon ECR, and verified image availability in the AWS Console.