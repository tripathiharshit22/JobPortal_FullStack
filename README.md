# JobPortal_FullStack

A full-stack Job Portal application (React + Vite frontend, Node/Express backend) for posting jobs, applying to jobs, user authentication and simple admin features.  
This repository contains two main folders: `frontend` (client) and `backend` (server).

---

## 📑 Table of Contents
- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [Prerequisites](#prerequisites)
- [Environment Variables](#environment-variables)
- [Local Setup & Run](#local-setup--run)
  - [Backend (server)](#backend-server)
  - [Frontend (client)](#frontend-client)
- [Build & Deploy](#build--deploy)
- [Testing](#testing)
- [Troubleshooting](#common-troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 📖 About
This project is a full-stack Job Portal allowing companies to post jobs, candidates to browse & apply, and admins to manage listings and users.  
It's structured to separate frontend and backend so you can develop and deploy them independently.

---

## ✨ Features
- User registration & login (candidates, employers/admin)
- Job posting, editing, deleting (employers)
- Browse & filter jobs (candidates)
- Apply for jobs (resume upload or profile-based apply)
- Dashboard(s) for users and employers
- RESTful APIs for frontend consumption
- JWT-based authentication
- Role-based access control
- Optional Cloudinary integration for file storage

---

## 🛠 Tech Stack
- **Frontend:** React, Vite, React Router
- **Backend:** Node.js, Express
- **Database:** MongoDB (Mongoose)
- **Authentication:** JWT
- **File Storage:** Cloudinary / Local
- **Dev Tools:** Nodemon, ESLint, Prettier

---

## 📂 Repository Structure
/ (root)
├─ backend/ # Node/Express API
│ ├─ controllers/
│ ├─ models/
│ ├─ routes/
│ ├─ utils/
│ ├─ package.json
│ └─ server.js
├─ frontend/ # React + Vite app
│ ├─ src/
│ ├─ public/
│ ├─ package.json
│ └─ vite.config.js
└─ README.md


---

## ⚙️ Prerequisites
Make sure you have installed:
- Node.js (v18+ recommended)
- npm or yarn
- MongoDB (local or Atlas cluster)
- (Optional) Cloudinary account

---

## 🔑 Environment Variables
Create a `.env` file in the **backend** folder with:

PORT=8000

MONGO_URI=<your-mongodb-connection-string>

SECRET_KEY=<your-jwt-secret>

CLOUD_NAME=<optional>

API_KEY=<optional>

API_SECRET=<optional>





---

## 🚀 Local Setup & Run

### Backend (server)
```bash
cd backend
npm install
npm run dev   # or node server.js
Frontend (client)
bash
Copy code
cd frontend
npm install
npm run dev
Frontend runs at: http://localhost:5173

📦 Build & Deploy
Frontend
bash
Copy code
cd frontend
npm run build
Deploy dist/ folder to Netlify / Vercel / static hosting.

Backend
Set env vars on server (Heroku / Render / AWS etc.)

Run:

bash
Copy code
cd backend
npm start
Use pm2 or systemd for production.

🧪 Testing
(If tests are added)

bash
Copy code
cd backend
npm run test
🛠 Common Troubleshooting
nodemon not recognized → install globally:

bash
Copy code
npm i -g nodemon
Cloudinary errors → check uploadOnCloudinary export in utils file.

CORS issues → enable CORS middleware in backend.

🤝 Contributing
Fork repo

Create branch: git checkout -b feature/your-feature

Commit: git commit -m "feat: added feature"

Push: git push origin feature/your-feature

Open Pull Request

📜 License
MIT License (update if using another).