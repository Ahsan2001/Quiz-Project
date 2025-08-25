📘 Online Quiz Management System

This project is a web-based Online Quiz Management System developed as a mini-project for DUET.
It provides separate portals for teachers and students, with a secure backend handling authentication, quizzes, announcements, and results.

📂 Project Structure
├── duet-backend-core/         # Backend (Node.js + Express + MongoDB)
│   ├── config/                # Configuration files (DB connection, environment variables)
│   ├── controller/            # Controllers (business logic for each module)
│   │   ├── announcement/      # Handles quiz announcements
│   │   ├── auth/              # Handles login/signup and JWT auth
│   │   ├── comment/           # Handles comments/discussions
│   │   ├── lesson/            # Handles lessons in courses
│   │   ├── online-courses/    # Handles course management
│   │   ├── profile/           # Handles user profiles
│   │   └── quiz/              # Handles quiz creation, management, results
│   ├── database/              # MongoDB connection logic
│   ├── dto/                   # Data Transfer Objects (API request/response shapes)
│   ├── middlewares/           # Middleware (auth check, error handling, validation)
│   ├── models/                # Mongoose models (Teacher, Student, Quiz, Question, Result, Announcement)
│   ├── routes/                # Express routes mapping endpoints to controllers
│   ├── schema/                # Validation schemas (Joi/Zod for request validation)
│   ├── services/              # Service layer for reusable business logic
│   └── utils/                 # Utility/helper functions (token generation, constants, etc.)

├── student-portal/            # Student Frontend (React + TypeScript)
│   ├── components/            # Reusable UI components (Quiz Attempt, Announcements, Login)
│   ├── pages/                 # Pages (Home, Quiz, Results)
│   ├── redux/                 # Redux Toolkit state management
│   └── src/                   # App logic, API calls with Axios

├── teacher-portal/            # Teacher Frontend (React + TypeScript)
│   ├── components/            # Reusable UI components (Quiz Form, Dashboard, Announcement)
│   ├── pages/                 # Pages (Login, Create Quiz, Manage Quiz)
│   ├── redux/                 # Redux Toolkit state management
│   └── src/                   # App logic, API calls with Axios

🚀 Features
👨‍🏫 Teacher Portal

Teacher login & authentication
Create and manage quizzes
Add questions with multiple options and correct answers
Generate a unique quiz key
Post quiz key in Announcement Section
View results of students

👨‍🎓 Student Portal

Student login & authentication
View announcements
Start quiz using unique key
Attempt multiple-choice questions
Submit answers and view results

⚙️ Backend (duet-backend-core)

Built with Node.js + Express
Uses MongoDB for data storage
APIs for authentication, quiz creation, announcements, results
Middleware for authentication & error handling

🛠️ Tools & Technologies

Frontend: React, TypeScript (TSX), Redux Toolkit, Axios
Backend: Node.js, Express.js, JWT Authentication
Database: MongoDB Atlas (NoSQL)
Styling: Tailwind CSS, Material UI (optional)
Deployment: Vercel (frontend), Render/Heroku (backend)

🗂️ Installation & Setup
1. Clone the repository
git clone https://github.com/Ahsan2001/Quiz-Project
cd quiz-system

2. Install dependencies for backend
cd duet-backend-core
npm install
npm run dev

3. Install dependencies for student portal
cd student-portal
npm install
npm start

4. Install dependencies for teacher portal
cd teacher-portal
npm install
npm run dev



📌 Notes

Ensure MongoDB Atlas URI is configured in backend .env.
Teacher generates a quiz key → posts in announcement → students use the key to attempt quiz.
