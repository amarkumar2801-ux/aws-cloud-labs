 # AWS CloudFront + S3 Static Website Lab

## Overview

This project demonstrates how to host a static website on Amazon S3 and improve its global performance and security using Amazon CloudFront.

CloudFront caches website content at AWS Edge Locations, reducing latency and improving website loading speed for users worldwide.

---

## Services Used

- Amazon S3
- Amazon CloudFront

---

## Architecture

```
User
   │
   ▼
CloudFront Distribution
   │
   ▼
Amazon S3 Website Endpoint
   │
   ▼
Static Website Files
```

---

## Steps Performed

1. Created an S3 Bucket.
2. Uploaded website files.
3. Enabled Static Website Hosting.
4. Configured Bucket Policy for public access.
5. Verified the website using the S3 Website Endpoint.
6. Created a CloudFront Distribution.
7. Used the S3 Website Endpoint as the CloudFront Origin.
8. Waited for the distribution to deploy.
9. Verified the website using the CloudFront Domain.
10. Verified cache using browser developer tools.

---

## Validation

- Website accessible via S3 Website Endpoint.
- Website accessible via CloudFront Distribution.
- HTTPS enabled through CloudFront.
- Cache verified using:

```
X-Cache: Hit from cloudfront
```

```
Age: > 0
```

---

## AWS Services

- Amazon S3
- Amazon CloudFront

---

## Learning Outcomes

- Static Website Hosting
- S3 Bucket Policy
- CloudFront Distribution
- Edge Locations
- Website Caching
- HTTPS Delivery
- Cache Validation
- Global Content Delivery