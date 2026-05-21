# Serverless-Notes-Saver-App
# 📝 Serverless Notes App with Authentication on AWS

![AWS](https://img.shields.io/badge/AWS-Serverless-orange?style=for-the-badge&logo=amazonaws)
![Python](https://img.shields.io/badge/Python-Backend-blue?style=for-the-badge&logo=python)
![DynamoDB](https://img.shields.io/badge/DynamoDB-NoSQL-blue?style=for-the-badge&logo=amazondynamodb)
![Lambda](https://img.shields.io/badge/AWS-Lambda-yellow?style=for-the-badge&logo=awslambda)
![API Gateway](https://img.shields.io/badge/API-Gateway-red?style=for-the-badge&logo=amazonapigateway)
![S3](https://img.shields.io/badge/Amazon-S3-green?style=for-the-badge&logo=amazons3)

---

# 🚀 Serverless Notes App

A fully serverless Notes Application built using AWS Cloud Services with user authentication, note management, and attractive frontend UI.

This project allows users to:

✅ Register Account  
✅ Login Securely  
✅ Add Notes  
✅ View Personal Notes  
✅ Store Data in DynamoDB  
✅ Host Frontend on Amazon S3  
✅ Use AWS Lambda for Backend Logic  
✅ Access APIs through API Gateway  

---

# 📌 Project Architecture

```text
User Interface (S3 Hosted Website)
            │
            ▼
     API Gateway (REST APIs)
            │
            ▼
      AWS Lambda Functions
            │
            ▼
        DynamoDB Tables
```

---

# 🧰 AWS Services Used

| Service | Purpose |
|---|---|
| AWS Lambda | Backend serverless functions |
| Amazon API Gateway | REST API management |
| Amazon DynamoDB | NoSQL database |
| Amazon S3 | Frontend hosting |
| AWS IAM | Permissions management |

---

# ✨ Features

## 👤 Authentication System
- User Registration
- User Login
- Credential Validation
- Login Success Popup
- Registration Success Popup

---

## 📝 Notes Management
- Add Notes
- Retrieve User Notes
- Store Notes in DynamoDB
- Dynamic Notes Display

---

## 🎨 Frontend UI
- Responsive Design
- Clean Interface
- Popup Notifications
- Real-Time Updates

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
| userId | String (Partition Key) |
| noteId | String (Sort Key) |
| note | String |

---

# 🔥 Lambda Functions

## ✅ Register Function
Stores new user credentials in DynamoDB.

### Input
```json
{
  "email": "user@gmail.com",
  "password": "123456"
}
```

---

## ✅ Login Function
Verifies user credentials.

### Input
```json
{
  "email": "user@gmail.com",
  "password": "123456"
}
```

---

## ✅ Add Note Function
Adds user notes into DynamoDB.

### Input
```json
{
  "userId": "user@gmail.com",
  "note": "My first note"
}
```

---

## ✅ Get Notes Function
Retrieves notes of logged-in user.

### API Request
```text
GET /get-notes?userId=user@gmail.com
```

---

# 🌐 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | /register | Register User |
| POST | /login | Login User |
| POST | /add-note | Add New Note |
| GET | /get-notes | Fetch User Notes |

---

# 🎨 Frontend Features

✅ Attractive UI  
✅ Success Popup Alerts  
✅ Responsive Layout  
✅ Dynamic Notes Rendering  
✅ User-Friendly Design  

---

# ☁️ S3 Static Website Hosting

The frontend is hosted using Amazon S3 Static Website Hosting.

### Steps:
1. Create S3 Bucket
2. Upload `index.html`
3. Enable Static Website Hosting
4. Configure Bucket Policy
5. Access Website URL

---

# 🔐 IAM Role Configuration

Lambda functions require permissions to access DynamoDB.

### Attached Policy:
```text
AmazonDynamoDBFullAccess
```

---

# 🚀 Deployment Steps

## Step 1: Create DynamoDB Tables
- Users
- Notes

---

## Step 2: Create IAM Role
Attach DynamoDB access policy.

---

## Step 3: Create Lambda Functions
- Register Function
- Login Function
- Add Note Function
- Get Notes Function

---

## Step 4: Configure API Gateway
Create REST APIs and enable CORS.

---

## Step 5: Upload Frontend to S3
Host application using static website hosting.

---

# 📸 Application Workflow

## 👤 User Registration
```text
User → Register → DynamoDB → Success Popup
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

## 📋 Fetch Notes
```text
User → Get Notes → Display Notes
```

---

# 💡 Future Improvements

- JWT Authentication
- Password Hashing
- Delete Notes Feature
- Edit Notes Feature
- React Frontend
- Dark Mode UI
- AWS Cognito Integration

---

# 🛡️ Security Improvements

Currently passwords are stored as plain text for learning purposes.

Recommended improvements:
- Use bcrypt hashing
- Use JWT tokens
- Enable HTTPS
- Add Authentication Middleware

---

# 🎯 Learning Outcomes

By completing this project, you will learn:

✅ Serverless Architecture  
✅ AWS Lambda  
✅ API Gateway  
✅ DynamoDB Operations  
✅ S3 Static Hosting  
✅ IAM Roles & Permissions  
✅ Frontend-Backend Integration  
✅ REST API Development  

---

# 📚 Technologies Used

- HTML
- CSS
- JavaScript
- Python
- AWS Lambda
- DynamoDB
- API Gateway
- Amazon S3

---

# 🌟 Project Highlights

✔ Fully Serverless  
✔ Cost Efficient  
✔ Scalable Architecture  
✔ Cloud Native Application  
✔ Beginner Friendly AWS Project  
✔ Real-World Use Case  

---

# 👩‍💻 Author

## Dhanashri Wadile

Passionate about Cloud Computing, AWS, Python, and DevOps technologies.

---

# ⭐ Support

If you like this project:

🌟 Star the repository  
🍴 Fork the project  
📢 Share with others  

---

# 📬 Connect

## GitHub Profile

https://github.com/DhanashriWadile

## Build • Learn • Deploy • Repeat 🚀
