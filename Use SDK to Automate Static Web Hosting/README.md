# 🌐 Static Website Hosting Automation using Amazon S3 & boto3

---

# 📖 Project Description

This project explains two different approaches for hosting a static website on AWS:

### 🔹 Manual Deployment

Hosting the website directly through the AWS Management Console by creating and configuring an S3 bucket manually.

### 🔹 Automated Deployment

Using the Python SDK **boto3** to automate the complete hosting process including:

* Bucket creation
* File upload
* Static website hosting configuration

The main purpose of this project is to show how automation simplifies deployment and minimizes manual configuration work.

---

# 🎯 Project Goals

* Deploy a static website using Amazon S3
* Learn the manual hosting process through AWS Console
* Automate deployment using Python and boto3
* Understand the difference between manual and automated workflows
* Create a scalable and cost-efficient hosting solution

---

# 🛠️ Technologies & AWS Services Used

* **Amazon S3** – Static website hosting
* **boto3** – AWS SDK for Python
* **IAM** – Access and permission management
* **AWS CLI** – Credential configuration

---

# 🏗️ System Architecture

## 🔹 Simplified Architecture Diagram

```text
        Website Files
              │
      ┌───────┴────────┐
      │                │
      │                │
Manual Upload      Python Script
(AWS Console)        (boto3 SDK)
      │                │
      └───────┬────────┘
              ▼
        Amazon S3 Bucket
              │
              ▼
    Static Website Hosting
              │
              ▼
       Public Website URL
```

---

# 🔄 Workflow Architecture

```text
Website Files
      ↓
Amazon S3 Bucket
      ↓
Enable Static Hosting
      ↓
Public Website Endpoint
```

---

# ⚙️ Implementation Process

# 🔹 Method 1: Manual Deployment using AWS Console

## Step 1: Create an S3 Bucket

1. Open **AWS Console**
2. Navigate to **Amazon S3**
3. Click on **Create Bucket**
4. Enter a unique bucket name
5. Create the bucket

---

## Step 2: Disable Public Access Block

1. Open the bucket
2. Go to **Permissions**
3. Disable **Block Public Access**

---

## Step 3: Upload Website Files

Upload the required website files such as:

```text
index.html
style.css
```

---

## Step 4: Enable Static Website Hosting

1. Open bucket **Properties**
2. Enable **Static Website Hosting**
3. Set the index document as:

```text
index.html
```

---

## Step 5: Configure Bucket Policy

Add a bucket policy to allow public read access for website files.

---

## Step 6: Access the Website

Use the generated **S3 Static Website Endpoint URL** to access the hosted website.
