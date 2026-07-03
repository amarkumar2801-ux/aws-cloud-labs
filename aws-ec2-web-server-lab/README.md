 # 🚀 Amazon EC2 Lab

## 📌 Objective

This lab demonstrates how to launch an Amazon EC2 instance, configure networking, connect via SSH, install the Apache Web Server, and host a simple static web page.

---

# 🏗️ Services Used

- Amazon EC2
- Security Groups
- Key Pair
- Amazon Linux 2023
- Apache Web Server (httpd)

---

# 🎯 Lab Objectives

- Launch an EC2 Instance
- Create and use a Key Pair
- Configure Security Group
- Connect using SSH (MobaXterm)
- Install Apache Web Server
- Create a simple HTML webpage
- Access the webpage using Public IP
- Understand EC2 instance lifecycle

---

# 📋 Prerequisites

- AWS Account
- EC2 Key Pair (.pem)
- MobaXterm / SSH Client
- Internet Connection

---

# 🛠️ Steps Performed

### Step 1
Created an EC2 Key Pair.

### Step 2
Launched an Amazon Linux 2023 EC2 Instance.

### Step 3
Configured the Security Group.

- SSH (Port 22) → My IP
- HTTP (Port 80) → Anywhere (0.0.0.0/0)

### Step 4
Connected to the EC2 instance using SSH.

### Step 5
Updated the operating system.

```bash
sudo yum update -y
```

### Step 6
Installed Apache Web Server.

```bash
sudo yum install -y httpd
```

### Step 7
Started Apache.

```bash
sudo systemctl start httpd
```

### Step 8
Enabled Apache on boot.

```bash
sudo systemctl enable httpd
```

### Step 9
Created a simple webpage.

```bash
sudo nano /var/www/html/index.html
```

Example:

```html
<h1>Hello EC2 Lab</h1>
```

### Step 10
Accessed the webpage using the EC2 Public IP.

---

# 🌐 Validation

✔ EC2 instance launched successfully

✔ SSH connection established

✔ Apache installed successfully

✔ Web server running

✔ Website accessible using Public IP

---

# 📸 Screenshots

- EC2 Dashboard
- Running EC2 Instance
- Security Group
- SSH Connection
- Apache Installation
- Website in Browser
- Instance Details

---

# 📚 Key Learnings

- Amazon EC2 Basics
- Instance Lifecycle
- Security Group Configuration
- Linux Commands
- SSH Connectivity
- Apache Web Server Installation
- Static Website Hosting

---


### What is Amazon EC2?

Amazon EC2 (Elastic Compute Cloud) is a virtual server service provided by AWS that allows users to launch and manage scalable compute instances in the cloud.

---

### Why do we use Security Groups?

Security Groups act as virtual firewalls that control inbound and outbound traffic to EC2 instances.

---

### Difference between Stop, Start, Reboot and Terminate?

- Stop → Instance stops, EBS volume remains.
- Start → Starts a stopped instance.
- Reboot → Restarts the operating system.
- Terminate → Permanently deletes the EC2 instance.

---

### Why do we use a Key Pair?

A Key Pair provides secure SSH authentication for connecting to Linux EC2 instances.

---

### What is Apache?

Apache (httpd) is an open-source web server used to host websites and web applications.

---

# ✅ Lab Status

Completed Successfully