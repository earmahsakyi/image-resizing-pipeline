# 🖼️ Serverless Image Resizing Pipeline (AWS Lambda + S3 + Sharp)

## 📖 Overview
This project demonstrates how to build a **fully serverless image resizing pipeline** using **AWS Lambda**, **S3 Event Triggers**, and **Lambda Layers** with the **Sharp** image processing library.

When a new image is uploaded to a **source S3 bucket**, the event triggers a **Lambda function** that automatically resizes the image and stores it in a **destination S3 bucket** — with no servers to manage.

---

## 🧠 Architecture

**Flow:**
1. A user uploads an image to the **source S3 bucket**.
2. The S3 event notification triggers the **Lambda function**.
3. The Lambda uses **Sharp** (via a Lambda Layer) to resize the image.
4. The resized image is uploaded to the **destination S3 bucket**.
5. Logs and metrics are tracked in **Amazon CloudWatch**.

**System Diagram:**

![Uploading system system imageResize.png…]()
