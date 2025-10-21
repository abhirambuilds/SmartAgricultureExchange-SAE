<!-- 🌾 SMART AGRICULTURE EXCHANGE README -->
<h1 align="center">🌾 SMART AGRICULTURE EXCHANGE</h1>

<p align="center">
  <b>Empowering Farmers • Connecting Buyers • Building Trust</b>
</p>

<p align="center">
  A next-generation <b>AgriTech marketplace</b> that enables farmers to publish verified, geo-tagged crop listings and allows buyers (brands or government) to discover, connect, and trade directly — with verification, deal orchestration, and transparency.
</p>

<hr/>

<h2>🚀 Phase 1 — Implementation Status ✅</h2>

<h3>✅ Completed</h3>

<ul>
  <li>💜 <b>Project structure setup</b></li>
  <li>⚛️ <b>Frontend</b> (React + Vite + TypeScript)</li>
  <li>🌿 <b>Backend</b> (Node.js + Express + TypeScript)</li>
  <li>🗄️ <b>Database schema</b> (PostgreSQL + PostGIS)</li>
  <li>🔒 <b>OTP-based Authentication system</b></li>
  <li>🌐 <b>Multi-language Support</b> (English/Hindi)</li>
  <li>🧭 <b>Basic routing & navigation</b></li>
  <li>💻 <b>Responsive UI</b> with Tailwind CSS</li>
</ul>

<h3>⏳ In Progress</h3>

<ul>
  <li>✍️ Farmer crop post creation</li>
  <li>📸 Image upload with EXIF capture</li>
  <li>🤖 Automated verification checks</li>
  <li>🧑‍⚖️ Admin approval workflow</li>
  <li>🔍 Buyer search functionality</li>
  <li>💬 Real-time chat system</li>
  <li>🤝 Deal finalization</li>
  <li>📩 SMS and email notifications</li>
</ul>

<hr/>

<h2>🛠️ Tech Stack</h2>

<h3>🎨 Frontend</h3>

<ul>
  <li>⚛️ React 18 + TypeScript</li>
  <li>⚡ Vite (build system)</li>
  <li>🎨 Tailwind CSS</li>
  <li>🔄 React Router DOM</li>
  <li>🧾 React Hook Form</li>
  <li>🌐 Axios</li>
  <li>🧭 Lucide React (icons)</li>
</ul>

<h3>🧠 Backend</h3>

<ul>
  <li>🧩 Node.js + Express.js (TypeScript)</li>
  <li>🗃️ PostgreSQL + PostGIS</li>
  <li>🔐 JWT Authentication</li>
  <li>💬 Socket.io (real-time chat)</li>
  <li>🗂️ Multer + Sharp (file/image upload)</li>
  <li>📞 Twilio (OTP)</li>
  <li>📧 Nodemailer (emails)</li>
</ul>

<h3>🗄️ Database</h3>

<ul>
  <li>🐘 PostgreSQL 14+ with PostGIS</li>
  <li>🧱 Redis (optional caching)</li>
</ul>

<hr/>

<h2>⚙️ Prerequisites</h2>

<ul>
  <li>🟢 Node.js (v18+)</li>
  <li>🐘 PostgreSQL (v14+ with PostGIS)</li>
  <li>🧰 Git</li>
  <li>🔴 Redis (optional)</li>
</ul>

<hr/>

<h2>💻 Quick Start</h2>

<h3>1️⃣ Clone the Repository</h3>

```bash
git clone <repository-url>
cd SmartAgricultureExchange
<h3>2️⃣ Install Dependencies</h3>
npm install
npm run install:all

<h3>3️⃣ Database Setup</h3>
psql -U postgres
CREATE DATABASE smart_agriculture_exchange;
\c smart_agriculture_exchange
CREATE EXTENSION postgis;
\q

psql -U postgres -d smart_agriculture_exchange -f database/init.sql

<h3>4️⃣ Configure Environment</h3>

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

<h3>5️⃣ Run the Application</h3>
npm run dev


🌐 Frontend → http://localhost:5173

🧩 Backend → http://localhost:3001

💚 Health → http://localhost:3001/health

<hr/> <h2>📱 Features</h2> <h3>👨‍🌾 Farmer Portal</h3> <ul> <li>🔢 OTP-based Login</li> <li>🌾 Crop Post Creation (photo + geotag)</li> <li>🧠 Expert Crop Advice</li> <li>🌐 Multi-language (English, Hindi, Tamil, Telugu)</li> <li>📶 Offline-ready PWA</li> <li>📱 Mobile-first UI</li> </ul> <h3>🧑‍💼 Buyer Portal</h3> <ul> <li>🔍 Advanced Search & Filters</li> <li>✅ Verified Listings</li> <li>💬 Direct Chat with Farmers</li> <li>📊 Deal Management</li> </ul> <h3>🛡️ Admin Portal</h3> <ul> <li>👁️ Post Verification</li> <li>📈 Analytics Dashboard</li> <li>👤 User Management</li> <li>🔒 Deal Monitoring</li> </ul> <hr/> <h2>🔒 Security</h2> <ul> <li>🔐 JWT Authentication</li> <li>🧱 Rate Limiting</li> <li>🧾 Input Validation</li> <li>📸 EXIF Image Verification</li> <li>🧑‍💼 Role-based Access Control</li> <li>🔒 HTTPS Ready</li> </ul> <hr/> <h2>🌐 Core API Endpoints</h2>
Category	Method	Endpoint	Description
Auth	POST	/api/auth/send-otp	Send OTP to phone
	POST	/api/auth/verify-otp	Verify OTP & login
Farmer	POST	/api/farmer/crop-posts	Create crop post
	GET	/api/farmer/crop-posts	Get all posts
Buyer	GET	/api/buyer/search	Search verified crops
	POST	/api/buyer/offers	Make offer
Admin	GET	/api/admin/posts/pending	Get pending approvals
<hr/> <h2>🧪 Testing</h2>
cd backend && npm test
cd frontend && npm test

<hr/> <h2>📦 Build & Deployment</h2>

Build:

npm run build
npm run build:frontend
npm run build:backend


Deploy:

☁️ Frontend → Vercel / Netlify (frontend/dist)

⚙️ Backend → AWS / GCP / DigitalOcean (backend/dist)

<hr/> <h2>🗺️ Roadmap</h2> <h3>🔹 Phase 2 — Polish</h3> <ul> <li>🌍 4+ Language Support</li> <li>📦 Offline Sync (PWA)</li> <li>🖼️ Image CDN + Thumbnails</li> <li>📊 Analytics Dashboard</li> <li>💳 Escrow / Payment Integration</li> </ul> <h3>🔹 Phase 3 — Scale & Trust</h3> <ul> <li>🌾 ML-based Crop Recognition</li> <li>🔍 Fraud Detection</li> <li>🚚 Logistics Integration</li> <li>🔗 Blockchain Traceability</li> <li>⭐ Farmer Rating System</li> </ul> <hr/> <h2>🤝 Contributing</h2> <ol> <li>Fork this repository</li> <li>Create a branch → <code>git checkout -b feature/new-feature</code></li> <li>Commit → <code>git commit -m "Add new feature"</code></li> <li>Push → <code>git push origin feature/new-feature</code></li> <li>Open a Pull Request 🚀</li> </ol> <hr/> <h2>📜 License</h2> <p>🪪 Licensed under the <b>MIT License</b> — see <code>LICENSE</code> file for details.</p> <hr/> <h2 align="center">❤️ Built for the Farming Community</h2> <p align="center"> “<b>Smart Agriculture Exchange</b> — Bridging the gap between soil and software.” 🌱<br/> Crafted with 💚 by innovators for India’s digital agriculture future. </p> ```
