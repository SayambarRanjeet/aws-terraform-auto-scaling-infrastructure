# 🚀 Dynamic Auto Scaling Architecture on AWS using Terraform

## 📌 Project Overview

This project demonstrates a production-style dynamic Auto Scaling architecture on AWS using Terraform (Infrastructure as Code).

The system automatically scales EC2 instances based on CPU utilization using CloudWatch alarms.

---

## 🏗 Architecture

Internet → Application Load Balancer → Target Group → Auto Scaling Group → EC2 Instances

- Multi-AZ Deployment
- Health Checks Enabled
- Connection Draining Configured

---

## ⚙️ Scaling Logic

- 🔼 Scale Out → CPU > 70% (2 datapoints within 2 minutes)
- 🔽 Scale In → CPU < 30% (3 datapoints within 3 minutes)

CloudWatch Alarms trigger Auto Scaling policies automatically.

---

## 🧪 Testing Process

- Installed stress tool on EC2
- Simulated high CPU load
- Verified automatic scale-out
- Stopped stress test
- Verified automatic scale-in
- Confirmed connection draining worked correctly

---

## 📂 Project Structure

```
terraform-asg/
├── main.tf
├── variables.tf
├── outputs.tf
├── provider.tf
├── terraform.tfvars
├── screenshots/
└── README.md
```

---

## 🛠 Technologies Used

- Terraform
- AWS EC2
- Auto Scaling Group
- Application Load Balancer
- CloudWatch
- Linux

---

## 📚 What I Learned

- Infrastructure as Code best practices  
- Designing scalable cloud systems  
- Monitoring and alarm configuration  
- Production-style scaling behavior  

---

## 🚀 How to Deploy

```bash
terraform init
terraform plan
terraform apply
```

---

## 👨‍💻 Author

Ranjeet Sayambar  
Aspiring AWS & DevOps Engineer
