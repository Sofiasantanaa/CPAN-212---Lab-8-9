## NorthStar Insurance Platform

This is a full-stack insurance management platform built with modern web technologies. The system implements secure authentication, role-based access control (RBAC), and real-world insurance workflows such as policies, claims, amendments, and reductions.

## Features

JWT Authentication
Role-Based Access Control (RBAC)
User Profile Management
Policy Management
Claims and Amendments
HTTPS Secure Communication
Admin Role Management

## Tech Stack

## Frontend

Next.js
React -TypeScript

## Backend

Node.js
Express

## Database

MongoDB

## Project Structure

/backend 
/frontend

## Installation & Setup

Clone the repository git clonehttps://github.com/Sofiasantanaa/CPAN-212---Lab-8-9.git 
cd YOUR-REPO

## Backend Setup

# Navigate to backend 
cd backend-api
# Install dependencies 
npm install
# Configure environment variables
Create a .env file in the backend folder:

PORT=5000 
MONGO_URI=your_mongodb_connection 
JWT_SECRET=your_secret

# Seed roles (IMPORTANT)
Before running the backend, seed the initial roles:

node src/seed/roles.seed.js 
npm run seed

This will create initial roles such as:

- ADMIN
- CUSTOMER
- AGENT
- UNDERWRITER
- ADJUSTER
  
# Run backend with HTTPS 
npm run dev

Server will run at:

https://localhost:PORT

# Frontend Setup

# Navigate to frontend
cd frontend
# Install dependencies 
npm install
#Run frontend 
npm run dev
Frontend will run at:

http://localhost:3000

#Authentication

- Users log in with email and password
- Backend returns a JWT token
- Token is used to access protected routes

# Authorization (RBAC)

Access is controlled based on user roles:

- ADMIN → Full system access 
- CUSTOMER → Own data only
- AGENT → Create policies
- UNDERWRITER → Approve amendments
- ADJUSTER → Process claims

# User Profiles

Users can:

- View their own profile
-  Update personal information
-  Access role-specific features

# HTTPS Security

The backend uses HTTPS to:

- Encrypt communication
- Protect sensitive data
- Ensure secure authentication

# Testing

The application has been tested for:

- Valid and invalid login
- Token validation
- Role-based access control
- Protected routes
- Business workflows
