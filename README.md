# AWS Static Portfolio Website

This project demonstrates how to host a personal portfolio website using **Amazon S3 Static Website Hosting** with public access via a custom bucket policy.

## 🌐 Live Site

▶️ [Visit My Portfolio](http://evangelia-my-portfolio.s3-website.us-east-2.amazonaws.com)

---

## 📦 Technologies & AWS Services Used

- **Amazon S3**: Static website hosting  
- **IAM**: Bucket policy for public read access  
- **HTML/CSS**: Static web content  

---

## 🧰 Project Structure
aws-s3-static-website/
├── index.html
├── README.md


---

## 🛠️ Deployment Steps

1. Create an **S3 bucket** and enable static website hosting  
2. Unblock public access and attach this **bucket policy**:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::evangelia-my-portfolio/*"
    }
  ]
}

---

📄 index.html (Main Page Source)

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Evangelia Pissanos – AWS Cloud Portfolio</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      color: #333;
      margin: 0;
      padding: 40px;
      text-align: center;
    }
    h1 {
      color: #0073bb;
    }
    a {
      color: #0073bb;
      text-decoration: none;
      font-weight: bold;
    }
    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <h1>Hello, I'm Evangelia</h1>
  <p>Aspiring AWS Solutions Architect | AWS Certified Cloud Practitioner</p>

  <!-- 🎖️ AWS Badge Embed -->
  <div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="ae8c4d9a-3547-4e70-ae46-808588a774a1" data-share-badge-host="https://www.credly.com"></div>
  <script type="text/javascript" async src="//cdn.credly.com/assets/utilities/embed.js"></script>

  <p>Check out my projects and certifications below:</p>
  <ul style="list-style: none; padding: 0;">
    <li><a href="https://github.com/epissanos/MyPortfolio" target="_blank">GitHub Portfolio</a></li>
    <li><a href="mailto:epissanos@outlook.com">Email Me</a></li>
    <li><a href="http://linkedin.com/in/evangelia-pissanos-758b17367" target="_blank">LinkedIn Profile</a></li>
  </ul>

  <p>More AWS projects coming soon. Stay tuned!</p>
</body>
</html>

---

## 🧠 What I Learned
How to use S3 static website hosting

How to configure IAM bucket policies for public access

How to deploy a live portfolio project using only AWS services





