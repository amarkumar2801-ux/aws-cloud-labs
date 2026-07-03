 # AWS S3 Static Website Hosting Lab

## Project Overview

This project demonstrates how to host a static website using Amazon S3 Static Website Hosting.

The website is publicly accessible through the Amazon S3 Website Endpoint without requiring any web server such as Apache or Nginx.

---

## Architecture

```
            User
              │
              ▼
     S3 Website Endpoint
              │
              ▼
        Amazon S3 Bucket
        ├── index.html
        ├── style.css
        └── error.html
```

---

## AWS Services Used

- Amazon S3
- S3 Static Website Hosting
- Bucket Policy

---

## Lab Objectives

- Create an Amazon S3 Bucket
- Enable Static Website Hosting
- Upload Website Files
- Configure Bucket Policy
- Allow Public Read Access
- Host a Static Website
- Access Website using S3 Website Endpoint

---

## Project Files

```
index.html
style.css
error.html
```

---

## Lab Workflow

### Step 1

Create an S3 Bucket.

---

### Step 2

Upload website files.

- index.html
- style.css
- error.html

---

### Step 3

Enable Static Website Hosting.

```
Index Document

index.html

Error Document

error.html
```

---

### Step 4

Disable Block Public Access.

---

### Step 5

Configure Bucket Policy.

```json
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Sid":"PublicReadAccess",
      "Effect":"Allow",
      "Principal":"*",
      "Action":"s3:GetObject",
      "Resource":"arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
```

---

### Step 6

Access the Website using the S3 Website Endpoint.

---

## Project Structure

```
aws-s3-static-website-hosting-lab/
│
├── README.md
├── AWS_S3_Static_Website_Hosting_Architecture.pptx
│
└── screenshots/
    ├── 01-s3-bucket.png
    ├── 02-bucket-objects.png
    ├── 03-static-website-hosting.png
    ├── 04-bucket-policy.png
    ├── 05-public-access.png
    └── 06-static-website-running.png
```

---

## Screenshots

- S3 Bucket
- Uploaded Objects
- Static Website Hosting
- Bucket Policy
- Public Access Configuration
- Website Successfully Hosted

---

## Result

✅ Amazon S3 Bucket Created

✅ Website Files Uploaded

✅ Static Website Hosting Enabled

✅ Bucket Policy Configured

✅ Public Website Successfully Hosted

---

## Key Learning

- Amazon S3 Static Website Hosting
- Bucket Policy
- Public Access Configuration
- Website Endpoint
- Static Web Hosting on AWS

---

## Future Enhancement

This project can be extended by integrating:

- Amazon CloudFront (CDN)
- AWS Certificate Manager (ACM)
- Amazon Route 53
- Custom Domain with HTTPS

---

## Author

**Amarjeet Chaudhary**

AWS Cloud Engineer Portfolio