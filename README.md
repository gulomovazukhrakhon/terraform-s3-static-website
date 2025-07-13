# 🌐 Terraform AWS S3 Static Website Hosting with CloudFront

Host your static website on **AWS S3** with secure, fast, and scalable delivery through **CloudFront CDN** – all provisioned with **Terraform**. This project automates the entire setup so you can deploy your site in minutes.

---

## 📑 Table of Contents

- [📦 Features](#-features)
- [🛠️ Infrastructure Overview](#️-infrastructure-overview)
- [📁 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
  - [1️⃣ Prerequisites](#1-prerequisites)
  - [2️⃣ Clone the Repository](#2-clone-the-repository)
  - [3️⃣ Place Your Website Files](#3-place-your-website-files)
  - [4️⃣ Initialize Terraform](#4-initialize-terraform)
  - [5️⃣ Deploy Infrastructure](#5-deploy-infrastructure)
  - [6️⃣ Access Your Website](#6-access-your-website)
- [🧹 Clean Up](#-clean-up)
- [⚠️ Notes](#️-notes)

---

## 📦 Features

✨ **One Command Deployment** – Provision S3, CloudFront, and upload your site in minutes  
🔒 **HTTPS Enabled** – Serve your website securely with SSL via CloudFront  
📂 **Automatic File Upload** – Syncs all files in `website/` directory to S3  
🌎 **Global Delivery** – Faster content delivery with AWS CloudFront CDN  
🧹 **Easy Cleanup** – Destroy resources easily when not needed  

---

## 🛠️ Infrastructure Overview

| Service       | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| **AWS S3**    | Hosts your static website files with public read access                     |
| **CloudFront**| Distributes content over HTTPS with caching and HTTP→HTTPS redirection      |
| **Terraform** | Automates provisioning of infrastructure                                    |

---

## 📁 Project Structure
```bash
├── main.tf # Terraform configuration for S3 and CloudFront
├── website/ # Local folder containing website files (HTML, CSS, JS, etc.)
└── README.md # Project documentation
```

---

## 🚀 Getting Started

### 1️⃣ Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/downloads) (v1.0+ recommended)
- [AWS CLI](https://aws.amazon.com/cli/) configured (`aws configure`)
- An AWS account with permissions to create S3 buckets and CloudFront distributions

---

### 2️⃣ Clone the Repository

```bash
git clone https://github.com/gulomovazukhrakhon/terraform-s3-static-website.git
cd terraform-s3-static-website
```

---

### 3️⃣ Place Your Website Files
Put all your static site files (HTML, CSS, JS, images, etc.) in the website/ directory.

---

### 4️⃣ Initialize Terraform
```bash
terraform init
```

---

### 5️⃣ Deploy Infrastructure
```bash
terraform apply
```
Approve when prompted.

---

### 6️⃣ Access Your Website
Once deployment is complete, Terraform will output two URLs:

- 🌐 website_url	CloudFront HTTPS URL
- 🪣 s3_url	S3 static website endpoint

---

## 🧹 Clean Up
To destroy all AWS resources created by Terraform:

```bash
terraform destroy
```

---

## ⚠️ Notes
- 🚨 This setup makes your S3 bucket publicly readable for website hosting. Don’t use it for private data.
- 🔑 CloudFront uses the default AWS SSL certificate. To use a custom domain, integrate with ACM certificates.

---

## 📜 License
This project is licensed under the MIT License.