🌾 SMART AGRICULTURE EXCHANGE

Empowering Farmers • Connecting Buyers • Building Trust

A next-generation AgriTech marketplace that enables farmers to publish verified, geo-tagged crop listings and allows buyers (brands or government) to discover, connect, and trade directly — with verification, deal orchestration, and transparency.

🚀 Phase 1 – Implementation Status
✅ Completed

✔️ Project structure setup

⚛️ Frontend (React + Vite + TypeScript)

🧩 Backend (Node.js + Express + TypeScript)

🗄️ Database schema (PostgreSQL + PostGIS)

🔐 OTP-based Authentication system

🌐 Multi-language Support (English/Hindi)

🧭 Basic routing & navigation

📱 Responsive UI with Tailwind CSS

🔄 In Progress

✍️ Farmer crop post creation

📸 Image upload with EXIF capture

🧠 Automated verification checks

🧑‍⚖️ Admin approval workflow

🔍 Buyer search functionality

💬 Real-time chat system

🤝 Deal finalization

📩 SMS and email notifications

🛠️ Tech Stack
🎨 Frontend

⚛️ React 18 + TypeScript

⚡ Vite (build system)

🎨 Tailwind CSS

🔄 React Router

🧾 React Hook Form

🌐 Axios

🧭 Lucide React Icons

🧠 Backend

🧩 Node.js + Express.js (TypeScript)

🗃️ PostgreSQL + PostGIS

🔐 JWT Authentication

💬 Socket.io (Real-time chat)

🗂️ Multer + Sharp (File Uploads)

📞 Twilio (SMS OTP)

📧 Nodemailer (Emails)

🗄️ Database

PostgreSQL 14+ with PostGIS

Redis (optional for caching)

⚙️ Prerequisites

Before running this app, make sure you have:

🟢 Node.js (v18+)

🐘 PostgreSQL (v14+ with PostGIS)

🔴 Redis (optional)

🧰 Git

💻 Quick Start
1️⃣ Clone the Repository
git clone <repository-url>
cd SmartAgricultureExchange

2️⃣ Install Dependencies
npm install
npm run install:all

3️⃣ Database Setup
# Create database
psql -U postgres
CREATE DATABASE smart_agriculture_exchange;
\c smart_agriculture_exchange
CREATE EXTENSION postgis;
\q


Then:

psql -U postgres -d smart_agriculture_exchange -f database/init.sql

4️⃣ Configure Environment

Backend .env:

PORT=3001
FRONTEND_URL=http://localhost:5173

DB_HOST=localhost
DB_PORT=5432
DB_NAME=smart_agriculture_exchange
DB_USER=postgres
DB_PASSWORD=your_password

JWT_SECRET=your-secret-key
JWT_EXPIRE=7d

TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
TWILIO_PHONE_NUMBER=+1234567890


Frontend .env:

VITE_API_URL=http://localhost:3001/api

5️⃣ Run the Application
npm run dev


🌐 Frontend → http://localhost:5173

🧩 Backend → http://localhost:3001

💚 Health Check → http://localhost:3001/health

📱 Feature Highlights
👨‍🌾 Farmer Portal

🔢 OTP-based Login

🌾 Crop Post Creation (photo + geotag)

🧠 Crop Advice Integration

🗣️ Multi-language (English, Hindi, Tamil, Telugu)

📶 Offline-Ready PWA

📱 Mobile-first UI

🧑‍💼 Buyer Portal

🔍 Advanced Search (crop, location, price)

✅ Verified Listings

💬 Direct Chat with Farmers

📊 Deal Tracking

🛡️ Admin Portal

👁️ Post Verification

📈 Analytics Dashboard

👤 User Management

🔒 Deal Oversight

🔒 Security Features

🔐 JWT Token Authentication

🧱 Rate Limiting (Anti-Spam)

🧾 Input Validation

📸 EXIF Metadata Verification

🧑‍💼 Role-based Access Control

🔒 HTTPS Ready

🌐 Core API Endpoints
🧩 Module	Method	Endpoint	Description
Auth	POST	/api/auth/send-otp	Send OTP to phone
	POST	/api/auth/verify-otp	Verify OTP & login
Farmer	POST	/api/farmer/crop-posts	Create crop post
	GET	/api/farmer/crop-posts	Get my posts
Buyer	GET	/api/buyer/search	Search verified posts
	POST	/api/buyer/offers	Make offer
Admin	GET	/api/admin/posts/pending	Get pending approvals
🧪 Testing
cd backend && npm test
cd frontend && npm test

📦 Build & Deployment
🏗️ Build
npm run build
npm run build:frontend
npm run build:backend

☁️ Deploy

Frontend → Vercel / Netlify (frontend/dist)

Backend → AWS / GCP / DigitalOcean (backend/dist)

🧭 Roadmap
🔹 Phase 2 – Polish

🌍 Add 4+ Languages

📦 Offline Sync (PWA)

🖼️ Image CDN + Thumbnails

📊 Analytics Dashboard

💳 Escrow / Payment Integration

🔹 Phase 3 – Scale & Trust

🌾 ML-based Crop Recognition

🔍 Fraud Detection

🚚 Logistics Integration

🔗 Blockchain Traceability

⭐ Farmer Rating System

🤝 Contributing

1️⃣ Fork this repo
2️⃣ Create a feature branch → git checkout -b feature/new-feature
3️⃣ Commit → git commit -m "Add new feature"
4️⃣ Push → git push origin feature/new-feature
5️⃣ Create Pull Request 🚀

📜 License

🪪 Licensed under MIT License – See LICENSE file for details.

❤️ Built For the Farming Community

“Smart Agriculture Exchange — Bridging the gap between soil and software.” 🌱
Crafted with 💚 by innovators for India’s digital agriculture future.
