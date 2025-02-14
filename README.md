# My AWS S3 Hosted Website

Hey there! Welcome to the README for my personal AWS S3-hosted website. This project is a key part of my **AWS Cloud Resume Challenge**, where I built and deployed a static website using various AWS services.

## What This Website Includes
- **Static Website Hosting:** My site is hosted on **Amazon S3**, making it fast and reliable.
- **CloudFront Integration:** To boost performance and security, I use **Amazon CloudFront** for content delivery.
- **Custom Domain via Route 53:** The site is accessible through a custom domain managed with **Amazon Route 53**.
- **HTTPS Security:** A secure connection is enabled using an **SSL certificate** from **AWS Certificate Manager (ACM)**.
- **Visitor Counter with DynamoDB:** Every visit is logged in **Amazon DynamoDB**, so I can track traffic.
- **Serverless Backend with Lambda & API Gateway:** A backend function powered by **AWS Lambda** and **API Gateway** updates the visitor count.
- **CI/CD Pipeline with GitHub Actions:** Any changes I make to the site get automatically deployed using **GitHub Actions**.

## Technologies I Used
- **AWS S3** – To host the static site
- **AWS CloudFront** – To distribute content efficiently
- **AWS Route 53** – For custom domain management
- **AWS Certificate Manager (ACM)** – To enable HTTPS
- **AWS DynamoDB** – For tracking visitor counts
- **AWS API Gateway** – To manage API requests
- **AWS Lambda (Python)** – To handle backend processing
- **GitHub Actions** – To automate deployments

## How to Deploy Updates
1. **Upload New Files to S3:**
   ```sh
   aws s3 sync ./website s3://your-s3-bucket-name --delete
   ```
2. **Clear CloudFront Cache (if applicable):**
   ```sh
   aws cloudfront create-invalidation --distribution-id YOUR_DISTRIBUTION_ID --paths "/*"
   ```
3. **Check Your Site:** Open your website URL and make sure everything looks good!

## What’s Next?
- Add a contact form using AWS Lambda
- Improve the site’s design with CSS/JS frameworks
- Tighten up security with better IAM role restrictions

## About Me
I'm **Hassan Ali**, and I built this website as part of my journey into cloud computing. If you're interested in AWS, feel free to connect with me!

---
Thanks for checking out my project! 🚀
