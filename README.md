# DevOps-Learning---Networking

# 🌐 NGINX on AWS EC2 with Custom Domain (Route 53)

This project demonstrates how to deploy an NGINX web server on an Amazon EC2 instance and map it to a custom domain registered through AWS Route 53.

## ✅ Project Goals

- Purchase a domain via Route 53
- Launch and configure an EC2 instance
- Install and run NGINX
- Set up DNS (A record) to route traffic to the instance
- Serve the default NGINX page at: `http://nginx.Abdirahmanlearning.com`

---

## 🛠️ Tech Stack

- **AWS EC2** (Amazon Linux 2023, t2.micro)
- **NGINX**
- **AWS Route 53**
- **SSH** (with key pair access)

---

## ⚙️ Setup Steps

### 1. Domain Registration
- Purchased domain `Abdirahmanlearning.com` via Route 53.

### 2. EC2 Instance Creation
- **AMI**: Amazon Linux 2023
- **Instance Type**: t2.micro (Free Tier)
- **Network Settings**:
  - Enabled public IP assignment
  - Used default VPC and a public subnet
- **Security Group**:
  - Port 22 (SSH) — Source: 0.0.0.0/0
  - Port 80 (HTTP) — Source: 0.0.0.0/0

### 3. NGINX Installation (Manual via SSH)
sudo yum install nginx -y
sudo systemctl start nginx

### 4. DNS Setup in Route 53 

### Supporting Documentation
A separate document is included in this repository that describes the full project process with step-by-step screenshots, including:

- Domain purchase and hosted zone setup
- EC2 launch configuration
- Security group and network settings
- NGINX installation and testing
- DNS configuration in Route 53
