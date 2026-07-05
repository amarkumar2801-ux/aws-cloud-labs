 # AWS API Gateway Lab

## Overview

This lab demonstrates how to expose an AWS Lambda function as a REST API using Amazon API Gateway.

The API Gateway receives HTTP requests, forwards them to the Lambda function, and returns a JSON response to the client. This is one of the most common serverless architectures used in AWS.

---

## AWS Services Used

- Amazon API Gateway (HTTP API)
- AWS Lambda
- AWS IAM

---

## Architecture

Client (Browser/Postman)
        │
        ▼
Amazon API Gateway
        │
        ▼
Route: ANY /orders
        │
        ▼
AWS Lambda Function
        │
        ▼
JSON Response

---

## Lab Objectives

- Create an AWS Lambda function.
- Write Python code to return JSON data.
- Create an HTTP API using API Gateway.
- Create an API route.
- Integrate the route with Lambda.
- Deploy the API.
- Invoke the API from a web browser.
- Verify the JSON response.

---

## Implementation Steps

### Step 1
Created an AWS Lambda function.

### Step 2
Added Python code to return order information.

### Step 3
Created an HTTP API in Amazon API Gateway.

### Step 4
Created an API route:

ANY /orders

### Step 5
Integrated the route with the Lambda function.

### Step 6
Deployed the API using the **dev** stage.

### Step 7
Accessed the Invoke URL from the browser.

### Step 8
Verified the API returned the expected JSON response.

---

## API Endpoint

ANY /orders

Example

https://<api-id>.execute-api.ap-south-1.amazonaws.com/dev/orders

---

## Sample Response

```json
{
  "message": "Orders API",
  "orders": [
    {
      "id": 101,
      "item": "Laptop",
      "price": 65000
    },
    {
      "id": 102,
      "item": "Mouse",
      "price": 1200
    }
  ]
}
```

---

## Learning Outcomes

- Understood API Gateway architecture.
- Learned Lambda integration with API Gateway.
- Created HTTP routes.
- Understood ANY HTTP method.
- Deployed an HTTP API.
- Tested APIs using a web browser.
- Built a basic serverless REST API.

---

## Author

Amarjeet Chaudhary

AWS Solutions Architect Associate Hands-on Labs