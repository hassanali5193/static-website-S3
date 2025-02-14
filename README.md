# static-website-S3
# AWS S3 Hosted Website

This repository contains the files for my static website hosted on **Amazon S3** as part of my **AWS Cloud Resume Challenge**.

## Features
- **Static Website Hosting:** The website is hosted on an **S3 bucket** with public access enabled for read permissions.
- **CloudFront Integration:** To improve performance and security, the site is served via **Amazon CloudFront**.
- **Route 53 Domain Name:** The website is accessible using a custom domain through **Amazon Route 53**.
- **HTTPS Security:** The website uses an **SSL certificate** from **AWS Certificate Manager (ACM)**.
- **DynamoDB Visitor Counter:** The visitor count is stored and retrieved from **Amazon DynamoDB**.
- **Lambda & API Gateway:** Serverless backend using **AWS Lambda** and **API Gateway** to update the visitor counter.
- **CI/CD Pipeline:** The website is updated via **GitHub Actions**, automatically deploying changes to S3.

## Technologies Used
- **AWS S3** – Static website hosting
- **AWS CloudFront** – Content delivery network (CDN)
- **AWS Route 53** – Domain management
- **AWS Certificate Manager (ACM)** – SSL/TLS certificate
- **AWS DynamoDB** – NoSQL database for visitor count
- **AWS API Gateway** – API endpoint for backend
- **AWS Lambda (Python)** – Backend function
- **GitHub Actions** – CI/CD for automatic deployment

## How to Deploy
1. **Upload Files to S3:**
   ```sh
   aws s3 sync ./website s3://your-s3-bucket-name --delete
   ```
2. **Invalidate CloudFront Cache (if using CloudFront):**
   ```sh
   aws cloudfront create-invalidation --distribution-id YOUR_DISTRIBUTION_ID --paths "/*"
   ```
3. **Verify Deployment:** Open your website URL to ensure updates are live.

## Future Improvements
- Implement a contact form using AWS Lambda
- Improve website design with CSS/JS frameworks
- Enhance security with IAM role restrictions

## Author
**Hassan Ali**

---
This README outlines the structure and deployment details of my AWS S3-hosted static website.
