# 🏥 Secure Patient Report Delivery System Using AWS SNS & VPC

This project demonstrates how hospitals can securely deliver patient reports online.  
The goal is to ensure that sensitive medical data is **encrypted, private, and only accessible to the intended patient** via mobile notifications.

In this solution, a **private EC2 instance** hosts the report, and messages are delivered securely through **Amazon SNS**, protected inside a **custom Amazon VPC** created using CloudFormation.

---

## 🚀 Project Overview

Hospitals need a secure way to send patient reports digitally.  
This system enables:

- Patients to receive notifications about their medical reports  
- Private message publishing inside a VPC  
- Secure access to reports hosted on a private EC2  
- Controlled IAM permissions  
- SNS-based alerting for patients

This prevents exposure of sensitive medical records and ensures delivery only to the intended recipient.

---

## 🎯 Key Highlights

### ✔ 1. **VPC Creation Using AWS CloudFormation**
A fully customized VPC was deployed using a YAML CloudFormation template, containing:

- Public & private subnets  
- Route tables  
- Internet gateway  
- NAT gateway  
- Security groups  

### ✔ 2. **SNS Integrated With VPC (Private Access)**
SNS was configured manually to:

- Allow private publishing from inside the VPC  
- Create IAM role + trust relationship for SNS  
- Create SNS topic  
- Add mobile subscription for receiving alerts  

### ✔ 3. **Private Report Publishing**
- A private EC2 instance (inside the VPC’s private subnet) hosts the report.
- The EC2 publishes report URLs/messages to SNS.
- SNS delivers the notification only to the intended patient’s number/email.
- IAM secures the publishing rights.

---

## 📁 Project Structure
