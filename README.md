# Advanced-Task02
🔐 User Authentication System

A secure backend authentication system built using Node.js, Express, MongoDB, and JWT.
This project implements user registration, login, password hashing, and protected routes using JSON Web Token authentication.



📌 Project Description

This project demonstrates how to implement a secure authentication system for a web application. It allows users to register, log in, and access protected routes using JWT-based authentication.

Passwords are securely hashed before storing in the database, and user sessions are managed using JSON Web Tokens.



🚀 Features
	•	User Registration
	•	User Login
	•	Password Hashing using bcrypt
	•	JWT Token Generation
	•	Protected Routes
	•	Error Handling
	•	MongoDB Database Integration



🛠️ Technologies Used
	•	Node.js
	•	Express.js
	•	MongoDB
	•	Mongoose
	•	bcryptjs
	•	jsonwebtoken
	•	dotenv
	•	cors



📂 Project Structure
auth-project/
│
├── models/
│   └── User.js
├── routes/
│   └── authRoutes.js
├── middleware/
│   └── authMiddleware.js
├── server.js
└── .env

⚙️ Installation & Setup

1️⃣ Clone the repository
git clone <your-repository-link>
cd auth-project

2️⃣ Install dependencies
npm install

3️⃣ Create a .env file
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

4️⃣ Run the server
npm run dev

Server will run on:
http://localhost:5000

🔐 API Endpoints

🔹 Register User

POST /api/auth/register

Request Body:
{
  "username": "testuser",
  "email": "test@gmail.com",
  "password": "123456"
}

🔹 Login User

POST /api/auth/login

Request Body:
{
  "email": "test@gmail.com",
  "password": "123456"
}

🔹 Get Profile (Protected Route)

GET /api/profile

Headers:
Authorization: Bearer <token>

🔒 Security Features
	•	Passwords are hashed using bcrypt
	•	JWT tokens expire after a set time
	•	Protected routes require valid authentication token
	•	Sensitive data (password) is not returned in responses



🧪 Testing

API endpoints can be tested using Postman.

