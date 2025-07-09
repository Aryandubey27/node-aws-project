# AWS EC2 & S3 Web Hosting Project: Node.js Image Gallery

## 👨‍💻 Project by: Aryan Dubey  
**Email:** ripul2k@gmail.com  
**GitHub:** [Aryandubey27](https://github.com/Aryandubey27)

---

## 📌 Objective

This project demonstrates hosting a Node.js web application on an AWS EC2 instance and serving an image gallery using publicly accessible images from an Amazon S3 bucket.

---

## 🛠️ Prerequisites

- AWS Account
- Basic knowledge of Node.js and Express
- IAM Role with SSM (AWS Systems Manager) access
- Custom Virtual Private Cloud (VPC)

---

## 🌐 Architecture Overview

- **Amazon EC2:** Hosts the Node.js application
- **Amazon S3:** Hosts publicly accessible images
- **AWS Systems Manager (SSM):** Used for secure EC2 instance access without SSH
- **VPC:** Isolated network environment for security

---

## 📦 Resources Used

### ✅ EC2 Instance

- Ubuntu AMI
- Node.js & npm
- Express.js
- Deployed Node.js image gallery app

### ✅ S3 Bucket

- Uploaded 3+ images
- Set images to **public access**
- Public S3 image URLs used in the app

---

## 🚀 Step-by-Step Setup

### 1. **IAM Role & SSM Access**
- Created IAM role with `AmazonSSMManagedInstanceCore` policy
- Attached role to EC2 instance
- Accessed EC2 using **AWS Systems Manager > Session Manager**

---

### 2. **VPC Configuration**
- Created a custom VPC with:
  - Public subnet
  - Internet Gateway
  - Route table with outbound internet access
  - Security group allowing port 80 and 22 (if needed)

---

### 3. **EC2 Setup**
- Launched Ubuntu instance
- Updated and installed packages:

```bash
sudo apt update
sudo apt install nodejs npm -y


