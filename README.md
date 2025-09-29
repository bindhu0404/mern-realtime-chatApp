# MERN Real-Time Chat App

This is a **full-stack web application** built with the **MERN stack** (MongoDB, Express.js, React.js, Node.js) and **Socket.io** for real-time messaging.  
The app features JWT-based authentication, protected routes, responsive UI with **TailwindCSS** and **DaisyUI**, and global state management with **Zustand**.

🔗 **Live Demo**: [Click here to access the app](https://realtime-chatapp-8xdw.onrender.com/login)

---

## Overview

The app allows users to create an account, log in securely, and chat in real-time with other users.  
Users can manage conversations, send and receive messages instantly, and search/filter conversations.  
The dashboard is protected and only accessible after login.  
This project demonstrates a fully integrated frontend and backend with scalable architecture.

---

## Features

### Authentication & Authorization
- **User Signup/Login/Logout** with JWT-based authentication  
- Passwords securely hashed with **bcrypt**  
- Protected dashboard routes accessible only to authenticated users  
- Role-based access can be added if required in future  

### Real-Time Messaging
- Users can send and receive messages instantly using **Socket.io**  
- Messages are stored in **MongoDB**  
- Online user status displayed in real-time  

### Conversation Management (CRUD)
- Create new conversations  
- Fetch all user conversations  
- Update conversation info  
- Delete conversations  
- Search/filter conversations by user name  

### Frontend Features
- Built with **React.js**, **TailwindCSS**, and **DaisyUI**  
- Responsive design for desktop and mobile  
- Forms with client-side validation  
- Global state management using **Zustand**  

### Backend Features
- Built with **Node.js** and **Express.js**  
- **MongoDB** as the database with **Mongoose** ORM  
- REST APIs for auth, messages, and conversations  
- Error handling and input validation  
- JWT authentication middleware  

---

## Folder Structure

```
mern-chat-app/
├── backend/
│ ├── models/
│ │ ├── User.js
│ │ ├── Message.js
│ │ └── Conversation.js
│ ├── routes/
│ │ ├── auth.js
│ │ ├── messages.js
│ │ └── conversations.js
│ ├── middleware/
│ │ └── authMiddleware.js
│ ├── .env
│ ├── server.js
│ └── package.json
├── frontend/
│ ├── public/
│ ├── src/
│ │ ├── components/
│ │ ├── pages/
│ │ ├── context/
│ │ ├── App.js
│ │ └── index.js
│ ├── tailwind.config.js
│ ├── package.json
│ └── README.md
└── README.md
```


## How to Run

Run the backend and frontend locally to test the app.

```bash
# Backend
cd backend
npm install

# Create a .env file
# MONGODB_URI=<your_mongodb_atlas_connection_string>
# JWT_SECRET=<your_jwt_secret>
# PORT=5000

npm run dev

# Frontend
cd ../frontend
npm install
npm start

# Open in browser at http://localhost:3000
```

## API Endpoints (Overview)

POST   /api/auth/register      - Signup
POST   /api/auth/login         - Login
POST   /api/auth/logout        - Logout
GET    /api/profile/me         - Get user profile (protected)
POST   /api/conversations      - Create conversation
GET    /api/conversations      - Get user conversations
PUT    /api/conversations/:id  - Update conversation
DELETE /api/conversations/:id  - Delete conversation
POST   /api/messages           - Send message
GET    /api/messages/:conversationId - Get messages by conversation

## Features

User signup/login/logout with JWT
Protected dashboard routes
Real-time messaging with Socket.io
Online user status display
Search/filter conversations
CRUD operations on messages and conversations
Responsive frontend with React, TailwindCSS, DaisyUI
Global state management using Zustand
Error handling on client & server

## Notes

Backend is modular and scalable for adding new features
JWT authentication ensures secure access
Socket.io enables real-time messaging for multiple users
Frontend is responsive and can be extended with additional pages
Project structure supports full frontend-backend integration
