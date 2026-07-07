 # AWS CloudTrail Lab

## 📌 Objective

The objective of this lab is to configure AWS CloudTrail for auditing AWS account activities. CloudTrail was used to capture management API events and store them in an Amazon S3 bucket for long-term logging and security auditing.

---

## 🛠️ Services Used

- AWS CloudTrail
- Amazon S3
- Amazon EC2

---

## 📖 Lab Overview

In this lab, I created a Multi-Region CloudTrail and configured it to store log files in an Amazon S3 bucket. I verified that AWS API activities were successfully recorded in CloudTrail Event History and stored as compressed JSON log files inside the S3 bucket.

---

## 🔧 Steps Performed

### Step 1: Created CloudTrail
- Created a new Multi-Region Trail.
- Enabled management event logging.
- Configured Amazon S3 as the log storage destination.

### Step 2: Verified Trail
- Confirmed the trail was successfully created.
- Verified CloudTrail started logging events.

### Step 3: Generated AWS Activity
- Started an EC2 instance.
- Generated AWS management API events.

### Step 4: Verified Event History
- Opened CloudTrail Event History.
- Verified events such as:
  - CreateTrail
  - StartLogging
  - PutEventSelectors
  - StartInstances
  - CreateBucket
  - PutBucketPolicy

### Step 5: Verified S3 Log Storage
- Opened the CloudTrail S3 bucket.
- Verified CloudTrail generated compressed `.json.gz` log files.

### Step 6: Verified Log Contents
- Downloaded and extracted a CloudTrail log file.
- Opened the JSON log.
- Verified event details including:
  - Event Name
  - Event Source
  - User Identity
  - Event Time
  - AWS Region
  - Source IP Address
  - Request Parameters

---

## 📊 Architecture

```
                AWS User
                    │
                    ▼
             AWS API Request
                    │
                    ▼
              AWS CloudTrail
              ┌─────────────┐
              │ Event History │
              └──────┬──────┘
                     │
                     ▼
             Amazon S3 Bucket
          (Compressed JSON Logs)
```

---

## ✅ Outcome

- Successfully configured AWS CloudTrail.
- Captured AWS Management API events.
- Verified Event History.
- Stored audit logs in Amazon S3.
- Verified CloudTrail JSON log files.

---

## 📚 Key Learnings

- CloudTrail records AWS API activities.
- Event History provides the last 90 days of management events.
- Trails continuously deliver logs to Amazon S3.
- CloudTrail logs are stored as compressed JSON (`.json.gz`) files.
- CloudTrail is primarily used for auditing, security, compliance, and troubleshooting.

---

## 📁 Screenshots

- CloudTrail Trail Created
- Event History
- StartInstances Event Details
- S3 CloudTrail Log Files
- CloudTrail JSON Log File