 # AWS Serverless Employee CRUD API

## Overview

This project demonstrates how to build a complete Serverless REST API using AWS services.

The application performs CRUD (Create, Read, Update, Delete) operations on an Employee database without managing any servers.

## Services Used

- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- IAM
- Postman

---

## Architecture

Client
↓
API Gateway
↓
AWS Lambda (Python)
↓
Amazon DynamoDB (Employees Table)

---

## Features

✔ Create Employee (POST)

✔ Read Employees (GET)

✔ Update Employee (PUT)

✔ Delete Employee (DELETE)

✔ Serverless Architecture

✔ REST API

---

## DynamoDB Table

Table Name

Employees

Partition Key

EmployeeId (String)

---

## API Endpoints

POST /employee

Creates a new employee.

GET /employee

Returns all employee records.

PUT /employee

Updates an existing employee.

DELETE /employee

Deletes an employee.

---

## Workflow

1. Create DynamoDB Employees table.
2. Create IAM Role with DynamoDB permissions.
3. Create Lambda Function using Python.
4. Connect Lambda with DynamoDB.
5. Implement CRUD operations.
6. Create API Gateway.
7. Create GET, POST, PUT and DELETE routes.
8. Deploy API.
9. Test APIs using Browser and Postman.

---

## Technologies

- Python
- Boto3
- AWS Lambda
- API Gateway
- DynamoDB
- IAM
- REST API
- Postman

---

## Learning Outcome

- Built a complete Serverless Application.
- Learned REST API development.
- Integrated Lambda with DynamoDB.
- Used API Gateway to expose REST endpoints.
- Tested APIs using Browser and Postman.