# aws-serverless-multi-region-app

This project demonstrates how to build a **highly available** and **disaster-resilient** serverless application using key AWS services. It showcases a multi-region architecture using **DynamoDB Global Tables**, **Lambda**, **API Gateway**, **Route 53**, and a simple web frontend.

---

## 🌍 Features

- **Multi-region failover** using Route 53 DNS health checks
- **Serverless architecture** powered by AWS Lambda and API Gateway
- **Global data replication** using DynamoDB Global Tables
- **Frontend web app** to interact with APIs (hosted via S3 or served through API Gateway)
- **Python Lambda functions** to read/write data across regions

---

## 🛠️ Technologies Used

- **Amazon DynamoDB Global Tables**
- **AWS Lambda (Python)**
- **Amazon API Gateway**
- **Amazon Route 53**
- **IAM Roles**
- **Amazon Certificate Manager (ACM)**
- **Frontend: HTML, Bootstrap, JavaScript**

---

## 📌 Architecture Overview

[User]
↓
[Route 53 Failover DNS]
↓
[API Gateway (Primary ↔ Secondary)]
↓
[Lambda Functions]
↓
[DynamoDB Global Tables (us-east-1 ↔ us-west-2)]

---

## 🚀 Getting Started

### 1. Clone this repo

```bash
git clone https://github.com/your-username/serverless-ha-dr-lab.git
cd serverless-ha-dr-lab
```
### 2. Set up the backend

- **Create a DynamoDB table with Global Table replication**
- **Create IAM role with permissions for DynamoDB and CloudWatch**
- **Deploy Python Lambda functions (read_function.py, write_function.py) in two regions**
- **Create REST APIs via API Gateway in both regions**
- **Set up custom domains and certificates using ACM**

### 3. Configure Route 53
- **Create health checks for primary and secondary API endpoints**
- **Set up failover routing policy with DNS records (e.g. api.example.com)**

### 4. Launch the frontend
- **Update index.html with your Route 53 DNS name**
- **Host it on S3, GitHub Pages, or serve through API Gateway**


## 🧪 Testing Failover
**1. Simulate failure by disabling the API in the primary region.**

**2. Observe that traffic is redirected to the secondary region.**

**3. The frontend should remain operational without user disruption.**

---

## 📁 Project Structure

serverless-ha-dr-lab/
├── lambda/
│   ├── read_function.py
│   └── write_function.py
├── frontend/
│   └── index.html
├── diagrams/
│   └── architecture.png (optional)
└── README.md


---

### ✅ Use Cases

- **1. Building resilient web APIs**
- **2. Learning multi-region architecture on AWS**
- **3. Practicing serverless deployment strategies**
- **4. Disaster Recovery architecture patterns**

### 🙌 Acknowledgements
Based on the AWS Lab: High Availability and Disaster Recovery with Serverless Architecture. Customized and extended for learning and demonstration purposes.


