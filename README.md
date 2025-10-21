🌾 Smart Agriculture Exchange

A trusted, low-friction digital marketplace connecting farmers directly with buyers, brands, and government agencies — ensuring verified listings, transparent deals, and fair pricing.
Built for the next generation of AgriTech innovation with real-time updates, OTP-based verification, and geotagged produce listings.

🚀 Phase 1 — Implementation Status
✅ Completed

 Project structure setup

 Frontend: React + Vite + TypeScript

 Backend: Node.js + Express + TypeScript

 Database schema: PostgreSQL + PostGIS

 OTP Authentication system

 Responsive UI with Tailwind CSS

 Multi-language (English + Hindi)

 Navigation & Routing setup

🔄 In Progress

 Farmer crop post creation

 Image upload with EXIF & geotag capture

 Automated verification checks

 Admin approval workflow

 Buyer search & filter system

 Real-time chat (Socket.io)

 Deal finalization flow

 SMS & email notification system

🛠️ Tech Stack
💻 Frontend

React 18 + TypeScript

Vite (blazing-fast build system)

Tailwind CSS

React Router DOM

React Hook Form

Axios (API communication)

Lucide React (icons)

⚙️ Backend

Node.js + Express + TypeScript

PostgreSQL + PostGIS

JWT Authentication

Socket.io (chat)

Multer + Sharp (file & image handling)

Twilio (OTP via SMS)

Nodemailer (email verification)

🗄️ Database

PostgreSQL 14+ with PostGIS

Redis (optional caching)

⚡ Prerequisites

Ensure you have:

Node.js ≥ v18

PostgreSQL ≥ v14 (with PostGIS)

Redis (optional)

Git

🚀 Quick Start
1️⃣ Clone the Repository
git clone <repository-url>
cd SmartAgricultureExchange

2️⃣ Install Dependencies
npm install
npm run install:all

3️⃣ Database Setup
# Create Database
psql -U postgres
CREATE DATABASE smart_agriculture_exchange;
\c smart_agriculture_exchange
CREATE EXTENSION postgis;
\q


Then initialize tables:

psql -U postgres -d smart_agriculture_exchange -f database/init.sql

4️⃣ Environment Configuration
Backend .env
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

Frontend .env
VITE_API_URL=http://localhost:3001/api

5️⃣ Run the Application
Development Mode
npm run dev


Frontend → http://localhost:5173

Backend API → http://localhost:3001

Health Check → http://localhost:3001/health

Separate Mode
cd backend && npm run dev
cd frontend && npm run dev

📱 Key Features
👨‍🌾 Farmer Portal

OTP-based Authentication

Crop post creation (photo + geotag)

Expert crop advice

Offline-ready PWA

Multi-language (English, Hindi, Tamil, Telugu)

Mobile-first responsive design

🧑‍💼 Buyer Portal

Advanced search & filters (crop, location, price)

Verified crop listings

Direct farmer chat

Offer & deal tracking

🛡️ Admin Portal

Post verification dashboard

Analytics overview

User & role management

Deal oversight

🔒 Security Highlights

JWT-based authentication

Rate limiting (spam prevention)

Input & file validation

Image EXIF verification

Role-based access control

HTTPS-ready configuration

🌐 Core API Endpoints
Category	Method	Endpoint	Description
Auth	POST	/api/auth/send-otp	Send OTP to phone
	POST	/api/auth/verify-otp	Verify OTP & login
	POST	/api/auth/register	Register new user
Farmer	POST	/api/farmer/crop-posts	Create crop post
	GET	/api/farmer/crop-posts	Get all posts
Buyer	GET	/api/buyer/search	Search verified crops
	POST	/api/buyer/offers	Make an offer
Admin	GET	/api/admin/posts/pending	Get pending approvals
🧪 Testing
# Backend
cd backend
npm test

# Frontend
cd frontend
npm test

📦 Production Build
npm run build
npm run build:frontend
npm run build:backend

☁️ Deployment
Frontend (Vercel / Netlify)
npm run build:frontend


Deploy the frontend/dist folder.

Backend (AWS / GCP / DigitalOcean)
npm run build:backend


Deploy the backend/dist folder and configure environment variables.

🤝 Contributing

Fork this repository

Create a new branch:

git checkout -b feature/new-feature


Commit changes:

git commit -m "Add new feature"


Push and open a Pull Request 🚀

🗺️ Roadmap
🔹 Phase 2 — Polish

 Multi-language (4+ languages)

 Offline PWA Sync

 Image CDN & thumbnails

 Basic analytics dashboard

 Escrow / payment integration

🔹 Phase 3 — Scale & Trust

 ML-based crop recognition

 Fraud detection (image + metadata)

 Logistics & transport API

 Blockchain traceability

 Farmer reputation system

📜 License

Licensed under the MIT License — see LICENSE file for details.

❤️ Built For

Farmers, buyers, and agri-innovators — empowering rural India with technology, transparency, and trust.

“Smart Agriculture Exchange — Bridging the gap between soil and software.” 🌱
