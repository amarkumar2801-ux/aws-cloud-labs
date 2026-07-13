 # AWS Cloud Resume Challenge

## Overview

The AWS Cloud Resume Challenge is a production-style serverless web application that hosts a professional resume on Amazon S3 and delivers it globally using Amazon CloudFront.

The website includes a live visitor counter powered by Amazon API Gateway, AWS Lambda, and Amazon DynamoDB. Every time a user visits the website, the visitor count is automatically incremented and displayed in real time.

---

## AWS Services Used

- Amazon S3
- Amazon CloudFront
- Origin Access Control (OAC)
- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- AWS IAM

---

## Project Architecture

User

↓

CloudFront

↓

Private Amazon S3 Bucket

↓

JavaScript Fetch API

↓

API Gateway

↓

AWS Lambda

↓

Amazon DynamoDB

---

## Features

- Professional Resume Website
- Static Website Hosting
- Global Content Delivery using CloudFront
- Private S3 Bucket with Origin Access Control (OAC)
- Serverless Visitor Counter
- REST API Integration
- Dynamic JavaScript Frontend
- Production-Oriented Architecture

---

## Workflow

1. Created a professional resume website using HTML, CSS and JavaScript.
2. Hosted the website on Amazon S3.
3. Configured Static Website Hosting.
4. Created a CloudFront Distribution.
5. Secured the S3 bucket using Origin Access Control (OAC).
6. Created a DynamoDB table to store visitor count.
7. Developed a Lambda function to increment the visitor count.
8. Created an API Gateway endpoint.
9. Connected JavaScript with API Gateway.
10. Displayed live visitor count on the website.

---

## AWS Services Flow

Visitor

↓

CloudFront

↓

Amazon S3

↓

JavaScript Fetch()

↓

API Gateway

↓

Lambda

↓

DynamoDB

---

## Technologies

- HTML
- CSS
- JavaScript
- Python
- Boto3
- AWS Lambda
- Amazon S3
- CloudFront
- DynamoDB
- API Gateway
- IAM

---

## Learning Outcomes

- Static Website Hosting
- Content Delivery Network (CDN)
- Origin Access Control (OAC)
- Serverless Architecture
- REST API
- Lambda Functions
- DynamoDB Integration
- JavaScript Fetch API
- Cloud Security Best Practices

---

## Project Status

Completed

---

## Future Improvements

- Custom Domain using Route 53
- HTTPS Certificate using ACM
- AWS WAF Integration
- CI/CD Pipeline
- Visitor Analytics Dashboard