 # Docker Persistent Storage using Docker Volumes

## 📌 Project Overview

This lab demonstrates how Docker Volumes provide persistent storage for containers. By default, Docker containers are ephemeral, meaning any data stored inside the container is lost when the container is removed.

Using Docker Volumes, data is stored outside the container in Docker-managed storage, allowing it to persist even after the container is deleted and recreated.

---

## 🎯 Objective

- Understand Docker Persistent Storage
- Create and manage Docker Volumes
- Mount a Docker Volume inside a container
- Verify data persistence after container deletion
- Learn Docker Volume lifecycle

---

## 🏗️ Architecture

Docker Volume (mydata) is mounted to the Nginx HTML directory.

```
Docker Engine
      │
      ▼
Docker Volume (mydata)
      │
      │ Mounted
      ▼
Nginx Container
/usr/share/nginx/html
      │
      ▼
Browser
```

---

## 🛠️ Technologies Used

- Amazon Linux 2023
- Docker Engine
- Docker Volumes
- Nginx
- EC2

---

## 📋 Lab Steps

### Step 1

Install Docker

```bash
sudo dnf install docker -y
```

---

### Step 2

Create Docker Volume

```bash
docker volume create mydata
```

---

### Step 3

Verify Volume

```bash
docker volume ls
```

---

### Step 4

Inspect Volume

```bash
docker volume inspect mydata
```

---

### Step 5

Run Nginx Container with Docker Volume

```bash
docker run -d \
--name nginx-volume \
-p 8080:80 \
-v mydata:/usr/share/nginx/html \
nginx
```

---

### Step 6

Modify index.html

```bash
docker exec -it nginx-volume bash

echo "<h1>Docker Volume Lab by Amarjeet</h1>" > /usr/share/nginx/html/index.html
```

---

### Step 7

Verify in Browser

```
http://<EC2-PUBLIC-IP>:8080
```

---

### Step 8

Delete Container

```bash
docker rm -f nginx-volume
```

---

### Step 9

Run New Container with Same Volume

```bash
docker run -d \
--name nginx-volume2 \
-p 8080:80 \
-v mydata:/usr/share/nginx/html \
nginx
```

---

### Step 10

Refresh Browser

The custom webpage is still available because the data is stored in the Docker Volume.

---

## 📷 Screenshots

- Docker Installation
- Docker Volume Creation
- Docker Volume Inspection
- Running Container
- Custom index.html
- Browser Output
- Data Persistence Verification

---

## 🔑 Key Learnings

- Docker containers are ephemeral.
- Docker Volumes provide persistent storage.
- Docker manages the lifecycle of volumes.
- Data survives container deletion.
- Volumes are preferred over bind mounts for persistent application data.
- Volumes are commonly used with databases and production workloads.

---

## 🚀 Real World Use Cases

- MySQL
- PostgreSQL
- MongoDB
- Redis
- Nginx Logs
- Apache Logs
- Application Uploads
- Configuration Files

---

## 📚 Commands Used

```bash
docker volume create mydata

docker volume ls

docker volume inspect mydata

docker ps

docker rm -f nginx-volume

docker run -d -v mydata:/usr/share/nginx/html nginx
```

---

## ✅ Outcome

Successfully demonstrated Docker Persistent Storage using Docker Volumes by proving that data remains available even after the container is removed and recreated.