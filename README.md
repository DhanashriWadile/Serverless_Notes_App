# Serverless Notes App
# 📝 Serverless Notes App on AWS

![AWS](https://img.shields.io/badge/AWS-Serverless-orange?style=for-the-badge&logo=amazonaws)
![Python](https://img.shields.io/badge/Python-Backend-blue?style=for-the-badge&logo=python)
![DynamoDB](https://img.shields.io/badge/DynamoDB-NoSQL-blue?style=for-the-badge&logo=amazondynamodb)
![Lambda](https://img.shields.io/badge/AWS-Lambda-yellow?style=for-the-badge&logo=awslambda)
![API Gateway](https://img.shields.io/badge/API-Gateway-red?style=for-the-badge&logo=amazonapigateway)
![S3](https://img.shields.io/badge/Amazon-S3-green?style=for-the-badge&logo=amazons3)

---

# 🚀 Project Overview

This project is a fully serverless Notes Application built using AWS Cloud services with user authentication and notes management functionality.

The application allows users to:

✅ Register Account  
✅ Login Securely  
✅ Add Notes  
✅ View Saved Notes  
✅ Store Notes in DynamoDB  
✅ Access APIs through API Gateway  
✅ Host Frontend using Amazon S3  

---

# 📌 AWS Services Used

| AWS Service | Purpose |
|---|---|
| AWS Lambda | Backend business logic |
| Amazon API Gateway | REST API creation |
| Amazon DynamoDB | NoSQL database |
| Amazon S3 | Static website hosting |
| AWS IAM | Access permissions |

---

# 🏗️ Project Architecture

```text
Frontend (HTML/CSS/JS Hosted on S3)
                │
                ▼
        API Gateway REST APIs
                │
                ▼
         AWS Lambda Functions
                │
                ▼
          Amazon DynamoDB
```

---

# ✨ Features

## 🔐 Authentication Features
- User Registration
- User Login
- Credential Validation
- Registration Success Popup
- Login Success Popup

---

## 📝 Notes Features
- Add Notes
- View Notes
- User-Specific Notes
- Real-Time Notes Rendering
- Note Added Success Popup

---

## 🎨 Frontend Features
- Attractive UI Design
- Background Image UI
- Responsive Layout
- Popup Notifications
- Interactive Buttons
- Dynamic Content Rendering

---

# 📂 Project Structure

```text
Serverless-Notes-App/
│
├── frontend/
│   └── index.html
│
├── lambda-functions/
│   ├── register.py
│   ├── login.py
│   ├── add_note.py
│   └── get_notes.py
│
└── README.md
```

---

# ⚙️ DynamoDB Tables

## 1️⃣ Users Table

| Attribute | Type |
|---|---|
| email | String (Partition Key) |
| password | String |

---

## 2️⃣ Notes Table

| Attribute | Type |
|---|---|
| email | String (Partition Key) |
| title | String |
| content | String |

---

# 🔥 Lambda Functions

## ✅ Register Function
Registers a new user into DynamoDB.

### Request Body
```json
{
  "email": "user@gmail.com",
  "password": "123456"
}
```

---

## ✅ Login Function
Validates user credentials.

### Request Body
```json
{
  "email": "user@gmail.com",
  "password": "123456"
}
```

---

## ✅ Add Note Function
Adds user notes into DynamoDB.

### Request Body
```json
{
  "email": "user@gmail.com",
  "title": "AWS Notes",
  "content": "Serverless applications are scalable."
}
```

---

## ✅ Get Notes Function
Fetches notes of logged-in users.

---

# 🌐 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | /register | Register User |
| POST | /login | Login User |
| POST | /add-note | Add New Note |
| GET | /get-notes | Retrieve Notes |

---

# 🎨 Frontend Preview

## 🖥️ User Interface Includes

✅ Email & Password Authentication  
✅ Register Button  
✅ Login Button  
✅ Add Notes Section  
✅ Show Notes Button  
✅ Dynamic Notes Display  
✅ Popup Alerts  

---

# 📸 Application Workflow

## 👤 User Registration
```text
User → Register → Lambda → DynamoDB → Success Popup
```

---

## 🔐 User Login
```text
User → Login → Validate Credentials → Success Popup
```

---

## 📝 Add Notes
```text
User → Add Note → Lambda → DynamoDB
```

---

## 📋 View Notes
```text
User → Fetch Notes → Display on Screen
```

---

# ☁️ S3 Static Website Hosting

The frontend is hosted using Amazon S3 Static Website Hosting.

## Deployment Steps
1. Create S3 Bucket
2. Upload index.html
3. Enable Static Website Hosting
4. Configure Bucket Permissions
5. Open Website Endpoint

---

# 🔑 IAM Permissions

Lambda functions require access to DynamoDB.

## Attached IAM Policy
```text
AmazonDynamoDBFullAccess
```

---

# 🚀 Deployment Steps

## Step 1: Create DynamoDB Tables
- Users Table
- Notes Table

---

## Step 2: Create IAM Role
Attach DynamoDB permission policy.

---

## Step 3: Create Lambda Functions
- Register Lambda
- Login Lambda
- Add Note Lambda
- Get Notes Lambda

---

## Step 4: Configure API Gateway
- Create REST APIs
- Enable CORS
- Connect Lambda functions

---

## Step 5: Host Frontend on S3
Upload frontend files and enable static hosting.

---

# 💡 Future Enhancements

- Password Hashing
- Delete Notes Feature
- Edit Notes Feature
- Dark Mode UI
- React Frontend
- Email Verification
- Mobile Responsive UI

---

# 🛡️ Security Improvements

Current project is for learning and educational purposes.

Recommended improvements:
- Encrypt Passwords
- Use HTTPS
- Store Sessions Securely
- Add Authentication Middleware

---

# 📚 Technologies Used

- HTML
- CSS
- JavaScript
- Python
- AWS Lambda
- Amazon DynamoDB
- API Gateway
- Amazon S3

---

# 🎯 Learning Outcomes

By building this project, you will learn:

✅ Serverless Architecture  
✅ REST APIs using API Gateway  
✅ AWS Lambda Functions  
✅ DynamoDB CRUD Operations  
✅ S3 Static Website Hosting  
✅ Frontend & Backend Integration  
✅ Cloud Application Deployment  

---

# 🌟 Project Highlights

✔ Fully Serverless Architecture  
✔ Cloud Native Application  
✔ Beginner Friendly AWS Project  
✔ Attractive UI Design  
✔ Real-World Implementation  
✔ Scalable and Cost Efficient  

---

# 👩‍💻 Author

## Dhanashri Wadile

AWS & Python Enthusiast passionate about Cloud Computing, DevOps, and Serverless Technologies.

---

# ⭐ Support

If you like this project:

⭐ Star this repository  
🍴 Fork this repository  
📢 Share with others  

---

# 📬 Connect

## GitHub Profile
https://github.com/DhanashriWadile

## Build • Deploy • Learn • Repeat 🚀
