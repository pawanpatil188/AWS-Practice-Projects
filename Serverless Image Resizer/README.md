# 🚀 Serverless Image Resizer using Amazon S3 & AWS Lambda

---

# 📖 Project Description

This project demonstrates a **serverless image processing system** using **Amazon S3** and **AWS Lambda**.

Whenever a user uploads an image into an S3 bucket, an automatic event trigger invokes a Lambda function. The function resizes the uploaded image and stores the processed version either in the same bucket or inside a separate output folder.

The entire workflow is fully automated, scalable, cost-efficient, and does not require any server management.

---

# 🎯 Project Goals

* Automatically resize images after upload
* Implement an event-driven cloud architecture
* Remove the need for infrastructure management
* Build a scalable media processing pipeline
* Minimize manual image optimization work

---

# 🛠️ AWS Services & Tools Used

* **Amazon S3** – Stores original and resized images
* **AWS Lambda** – Handles image processing and resizing
* **IAM** – Manages access permissions for Lambda
* **CloudWatch Logs** – Tracks Lambda execution logs
* **AWS CloudShell** – Packages dependencies and deployment files

---

# 🏗️ System Architecture

## 🔹 Architecture Diagram

```text id="arch1"
      User Uploads Image
                │
                ▼
        Amazon S3 Bucket
                │
                ▼
        S3 PUT Event Trigger
                │
                ▼
        AWS Lambda Function
                │
                ▼
      Resize Image (Pillow)
                │
                ▼
      Store Resized Image in S3
```

---

# 🔄 Workflow Process

```text id="flow2"
Upload Image
      ↓
Amazon S3 Bucket
      ↓
Trigger Lambda Function
      ↓
Resize Image
      ↓
Store Resized Output
```

---

# ⚙️ Implementation Steps

# 🔹 Step 1: Create an S3 Bucket

1. Open **AWS Console**
2. Navigate to **Amazon S3**
3. Create a new bucket with a unique bucket name
4. Keep the default configuration settings

---

# 🔹 Step 2: Create an IAM Role

1. Open **IAM**
2. Navigate to **Roles**
3. Create a new role for Lambda
4. Attach the following permissions:

   * `AmazonS3FullAccess`
   * `AWSLambdaBasicExecutionRole`

---

# 🔹 Step 3: Create a Lambda Function

1. Open **AWS Lambda**
2. Create a new function
3. Select the **Python runtime**
4. Attach the previously created IAM role

---

# 🔹 Step 4: Add Lambda Function Code

1. Upload the deployment package containing the **Pillow** library
2. Add the Python script for image resizing
3. Deploy the Lambda function

---

# 🔹 Step 5: Configure S3 Event Trigger

1. Open the S3 bucket
2. Navigate to **Properties**
3. Create an **Event Notification**
4. Select:

   * **Object Created (PUT)**
5. Set the destination as the Lambda function

---

# 🔹 Step 6: Test the Workflow

1. Upload an image into the S3 bucket
2. The Lambda function automatically processes the image
3. The resized image is stored inside the output folder

---

# 📂 Project Workflow

```text id="workflow3"
Upload Image
      ↓
Amazon S3 Bucket
      ↓
Trigger Lambda Function
      ↓
Resize Image
      ↓
Save Resized Image
```
