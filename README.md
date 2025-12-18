# resume-serverless-website-hosting-s3-cloudfront
without EC2
📂 Folder Structure
resume-website-s3-cloudfront/
│
├── index.html        (Resume Page)
├── about.html        (About / Skills Page)
├── style.css
└── README.md
# Resume Website Hosting using AWS S3 & CloudFront (Serverless)

This project demonstrates hosting a **2-page HTML resume website**
using **Amazon S3** and **CloudFront** in a fully **serverless architecture**.

---

## 🚀 Project Overview

- Hosted a static resume website on Amazon S3
- Used CloudFront CDN for fast global delivery
- No EC2 or servers used (Serverless)
- Secure and scalable architecture

---

## 🛠 AWS Services Used

- Amazon S3 (Static Website Hosting)
- Amazon CloudFront (CDN)
- AWS IAM
- Route 53 (Optional)

---

## 🧱 Architecture

User → CloudFront → S3 Bucket (HTML Resume Website)

---

## 📂 Project Structure
---

## ⚙️ Steps to Deploy

### 1️⃣ Create S3 Bucket
- Create unique S3 bucket
- Disable **Block all public access**
- Enable **Static Website Hosting**
  - Index document: `index.html`
  - Error document: `index.html`

---

### 2️⃣ Upload Files
Upload:
- index.html
- about.html
- style.css

---

### 3️⃣ Add Bucket Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}

---

4️⃣ Create CloudFront Distribution

Origin: S3 bucket

Viewer protocol: Redirect HTTP to HTTPS

Default root object: index.html

📈 Benefits

Serverless Architecture

High Availability

Low Latency (CDN)

Cost Effective

👤 Author

Om Suryawanshi
GitHub: https://github.com/omsuryawanshi527
