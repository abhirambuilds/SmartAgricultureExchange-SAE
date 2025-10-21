<!-- 🌾 SMART AGRICULTURE EXCHANGE README -->

<h1 align="center">🌾 SMART AGRICULTURE EXCHANGE</h1>

<p align="center">
  <strong>Empowering Farmers • Connecting Buyers • Building Trust</strong>
</p>

<p align="center">
  A next-generation <strong>AgriTech marketplace</strong> that enables farmers to publish verified, geo-tagged crop listings and allows buyers (brands or government) to discover, connect, and trade directly — with verification, deal orchestration, and transparency.
</p>

<hr/>

<h2>🚀 Phase 1 — Implementation Status ✅</h2>

<h3>✅ Completed</h3>

<ul>
  <li>💜 <strong>Project structure setup</strong></li>
  <li>⚛️ <strong>Frontend</strong> (React + Vite + TypeScript)</li>
  <li>🌿 <strong>Backend</strong> (Node.js + Express + TypeScript)</li>
  <li>🗄️ <strong>Database schema</strong> (PostgreSQL + PostGIS)</li>
  <li>🔒 <strong>OTP-based Authentication system</strong></li>
  <li>🌐 <strong>Multi-language Support</strong> (English/Hindi)</li>
  <li>🧭 <strong>Routing & Navigation</strong></li>
  <li>💻 <strong>Responsive UI</strong> with Tailwind CSS</li>
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

### 🎨 Frontend
- ⚛️ React 18 + TypeScript  
- ⚡ Vite  
- 🎨 Tailwind CSS  
- 🔄 React Router DOM  
- 🧾 React Hook Form  
- 🌐 Axios  
- 🧭 Lucide React

### 🧠 Backend
- 🧩 Node.js + Express (TypeScript)  
- 🗃️ PostgreSQL + PostGIS  
- 🔐 JWT  
- 💬 Socket.io  
- 🗂️ Multer + Sharp  
- 📞 Twilio (OTP)  
- 📧 Nodemailer

### 🗄️ Database
- 🐘 PostgreSQL 14+ (PostGIS)  
- 🧱 Redis (optional)

<hr/>

<h2>⚙️ Prerequisites</h2>

- 🟢 Node.js (v18+)  
- 🐘 PostgreSQL (v14+ with PostGIS)  
- 🔴 Redis (optional)  
- 🧰 Git

<hr/>

<h2>💻 Quick Start</h2>

<h3>1️⃣ Clone the Repository</h3>

git clone &lt;repository-url&gt;  
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

<p><strong>Backend <code>.env</code>:</strong></p>

<pre>
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
</pre>

<p><strong>Frontend <code>.env</code>:</strong></p>

<pre>
VITE_API_URL=http://localhost:3001/api
</pre>

<h3>5️⃣ Run the Application</h3>

npm run dev

<p>
🌐 Frontend → http://localhost:5173<br/>
🧩 Backend → http://localhost:3001<br/>
💚 Health → http://localhost:3001/health
</p>

<hr/>

<h2>📱 Features</h2>

<h3>👨‍🌾 Farmer Portal</h3>
<ul>
  <li>🔢 OTP-based Login</li>
  <li>🌾 Crop Post Creation (photo + geotag)</li>
  <li>🧠 Expert Crop Advice</li>
  <li>🌐 Multi-language (English, Hindi, Tamil, Telugu)</li>
  <li>📶 Offline-ready PWA</li>
  <li>📱 Mobile-first UI</li>
</ul>

<h3>🧑‍💼 Buyer Portal</h3>
<ul>
  <li>🔍 Advanced Search & Filters</li>
  <li>✅ Verified Listings</li>
  <li>💬 Direct Chat with Farmers</li>
  <li>📊 Deal Management</li>
</ul>

<h3>🛡️ Admin Portal</h3>
<ul>
  <li>👁️ Post Verification</li>
  <li>📈 Analytics Dashboard</li>
  <li>👤 User Management</li>
  <li>🔒 Deal Monitoring</li>
</ul>

<hr/>

<h2>🔒 Security</h2>

<ul>
  <li>🔐 JWT Authentication</li>
  <li>🧱 Rate Limiting</li>
  <li>🧾 Input Validation</li>
  <li>📸 EXIF Image Verification</li>
  <li>🧑‍💼 Role-based Access Control</li>
  <li>🔒 HTTPS Ready</li>
</ul>

<hr/>

<h2>🌐 Core API Endpoints</h2>

<table>
  <thead>
    <tr>
      <th>Category</th>
      <th>Method</th>
      <th>Endpoint</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Auth</td><td>POST</td><td>/api/auth/send-otp</td><td>Send OTP to phone</td></tr>
    <tr><td></td><td>POST</td><td>/api/auth/verify-otp</td><td>Verify OTP & login</td></tr>
    <tr><td>Farmer</td><td>POST</td><td>/api/farmer/crop-posts</td><td>Create crop post</td></tr>
    <tr><td></td><td>GET</td><td>/api/farmer/crop-posts</td><td>Get all posts</td></tr>
    <tr><td>Buyer</td><td>GET</td><td>/api/buyer/search</td><td>Search verified crops</td></tr>
    <tr><td></td><td>POST</td><td>/api/buyer/offers</td><td>Make offer</td></tr>
    <tr><td>Admin</td><td>GET</td><td>/api/admin/posts/pending</td><td>Get pending approvals</td></tr>
  </tbody>
</table>

<hr/>

<h2>🧪 Testing</h2>

<pre>
cd backend && npm test
cd frontend && npm test
</pre>

<hr/>

<h2>📦 Build & Deployment</h2>

<strong>Build:</strong>
<pre>
npm run build
npm run build:frontend
npm run build:backend
</pre>

<strong>Deploy:</strong>
<ul>
  <li>☁️ Frontend → Vercel / Netlify (frontend/dist)</li>
  <li>⚙️ Backend → AWS / GCP / DigitalOcean (backend/dist)</li>
</ul>

<hr/>

<h2>🗺️ Roadmap</h2>

<h3>🔹 Phase 2 — Polish</h3>
<ul>
  <li>🌍 4+ Language Support</li>
  <li>📦 Offline Sync (PWA)</li>
  <li>🖼️ Image CDN + Thumbnails</li>
  <li>📊 Analytics Dashboard</li>
  <li>💳 Escrow / Payment Integration</li>
</ul>

<h3>🔹 Phase 3 — Scale & Trust</h3>
<ul>
  <li>🌾 ML-based Crop Recognition</li>
  <li>🔍 Fraud Detection</li>
  <li>🚚 Logistics Integration</li>
  <li>🔗 Blockchain Traceability</li>
  <li>⭐ Farmer Rating System</li>
</ul>

<hr/>

<h2>🤝 Contributing</h2>

<ol>
  <li>Fork this repository</li>
  <li>Create a branch → <code>git checkout -b feature/new-feature</code></li>
  <li>Commit → <code>git commit -m "Add new feature"</code></li>
  <li>Push → <code>git push origin feature/new-feature</code></li>
  <li>Open a Pull Request 🚀</li>
</ol>

<hr/>

<h2>📜 License</h2>

<p>🪪 Licensed under the <strong>MIT License</strong> — see <code>LICENSE</code> file for details.</p>

<hr/>

<h2 align="center">❤️ Built for the Farming Community</h2>

<p align="center">
  “<strong>Smart Agriculture Exchange</strong> — Bridging the gap between soil and software.” 🌱<br/>
  Crafted with 💚 by innovators for India’s digital agriculture future.
</p>
