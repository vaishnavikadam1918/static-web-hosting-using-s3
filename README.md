## ☁️ Cloud Project: Static Website Hosting on AWS S3 
 
# 🌐 Static Website Hosting on AWS S3

## 📌 Project Overview

### This project demonstrates how to host a static website using Amazon S3.
The website consists of static files (HTML, CSS, JavaScript, and images) and is deployed on S3 with public access enabled.

## 🚀 Features

Host static files (HTML, CSS, JS, Images).

Publicly accessible via S3 website endpoint.

Error handling with a custom error page.

Scalable and highly available solution.

Optional: Integrate with Route 53 (Custom Domain) and CloudFront (HTTPS).

## ⚙️ Steps to Deploy

### 1️⃣ Create an S3 Bucket

Go to AWS S3 Console.

Create a new bucket with a unique name.

Uncheck Block all public access.

### 2️⃣ Upload Website Files

Upload index.html, style.css, script.js, and images to the bucket.

### 3️⃣ Enable Static Website Hosting

In Properties, enable Static Website Hosting.

Set:

Index document → index.html

Error document → error.html

### 4️⃣ Configure Bucket Policy

Add the following policy (replace with your bucket name):

{
  "Version": "2012-10-17",
  
  "Statement": [
  
    {
    
      "Sid": "PublicReadGetObject",
      
      "Effect": "Allow",
      
      "Principal": "*",
      
      "Action": "s3:GetObject",
      
      "Resource": "arn:aws:s3:::your-bucket-name/*"
      
    }
    
  ]
  
}

### 5️⃣ Access the Website

Copy the Bucket Website Endpoint from S3 properties.

Open it in your browser. 🎉

## 📂 Project Structure

#### 📁 my-static-website
 ├── index.html
 
 ├── style.css
 
 └── images/

## 🔮 Future Enhancements

Add a custom domain using Route 53.

Enable HTTPS with CloudFront + ACM.

Automate deployment with AWS CLI or CI/CD pipeline.

## ✅ Conclusion

By following this project, we successfully hosted a static website on Amazon S3, making it publicly accessible and highly scalable without managing any servers.
