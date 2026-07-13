 # Docker Networking using Custom Bridge Networks

## 📌 Project Overview

This lab demonstrates Docker Networking using Custom Bridge Networks. The objective is to understand how Docker containers communicate within the same network and how network isolation prevents communication between containers in different networks.

This is one of the most important networking concepts used in Docker, Docker Compose, Amazon ECS, and Kubernetes.

---

## 🎯 Objective

- Understand Docker Networking
- Create Custom Bridge Networks
- Launch containers in different networks
- Test container-to-container communication
- Demonstrate logical network isolation

---

## 🏗️ Architecture

```
                 Docker Engine
                       │
      ┌────────────────┴────────────────┐
      │                                 │
  frontend-net                     payment-net
      │                                 │
 ┌────┴────┐                      ┌─────┴─────┐
 │         │                      │           │
Frontend  Backend             Payment     (Future DB)
Container Container           Container
```

---

## 🛠 Technologies Used

- Amazon Linux 2023
- Docker Engine
- Docker Networks
- Ubuntu Containers
- EC2

---

## Lab Steps

### Step 1

View existing Docker networks

```bash
docker network ls
```

---

### Step 2

Create Frontend Network

```bash
docker network create frontend-net
```

---

### Step 3

Create Payment Network

```bash
docker network create payment-net
```

---

### Step 4

Launch Frontend Container

```bash
docker run -dit \
--name frontend \
--network frontend-net \
ubuntu bash
```

---

### Step 5

Launch Backend Container

```bash
docker run -dit \
--name backend \
--network frontend-net \
ubuntu bash
```

---

### Step 6

Launch Payment Container

```bash
docker run -dit \
--name payment \
--network payment-net \
ubuntu bash
```

---

### Step 7

Verify Networks

```bash
docker network ls
```

---

### Step 8

Verify Running Containers

```bash
docker ps
```

---

### Step 9

Enter Frontend Container

```bash
docker exec -it frontend bash
```

Install ping utility

```bash
apt update
apt install iputils-ping -y
```

---

### Step 10

Test Communication

```bash
ping backend
```

Result

Communication Successful

---

### Step 11

Test Isolation

```bash
ping payment
```

Result

Communication Failed

---

## 📷 Screenshots

- Docker Network List
- Custom Networks Created
- Running Containers
- Network Inspection
- Successful Ping (Frontend → Backend)
- Failed Ping (Frontend → Payment)

---

## Key Learnings

- Docker provides logical network isolation.
- Containers in the same network communicate directly.
- Containers in different networks cannot communicate by default.
- Custom Bridge Networks improve security.
- Docker Networking is widely used in Microservices.
- The same concepts are used in Docker Compose, Amazon ECS, and Kubernetes.

---

## Real World Use Cases

- Frontend ↔ Backend Communication
- Microservices
- Banking Applications
- Payment Systems
- Secure Application Isolation
- Kubernetes Networking
- Amazon ECS Services

---

## Commands Used

```bash
docker network ls

docker network create frontend-net

docker network create payment-net

docker network inspect frontend-net

docker ps

docker exec -it frontend bash
```

---

## Outcome

Successfully demonstrated Docker Networking using Custom Bridge Networks by verifying communication between containers in the same network and network isolation between containers in different networks.