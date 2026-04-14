# StudyForge 📚🤖

StudyForge is a full-stack AI-powered study planner application. It takes your syllabus, deadline, and daily availability, and leverages the **Anthropic Claude API** to instantly generate an optimized, personalized study scheduled. If you miss tasks and fall behind, StudyForge's smart AI adjustment feature can seamlessly reschedule your remaining workload.

## Features ✨

- **Smart AI Planning:** Provide topics and deadlines, and Claude constructs an optimal day-by-day timetable based on your selected difficulty (Aggressive/Balanced/Relaxed) and availability.
- **Dynamic Adjustments:** Missed a few days? Use the "I'm Behind" feature to let the AI recalculate and adjust your remaining schedule automatically.
- **Analytics Dashboard:** Track subject progress, consecutive streak days, and view beautiful charts (powered by Recharts).
- **Calendar Integration:** View all tasks across all your active study plans via FullCalendar.
- **Quick Notes:** Built-in global note-taking for every subject.
- **Modern UI:** Responsive, glassmorphism design with Dark/Light mode toggle. 
- **Secure Auth:** JWT-based user authentication.

## Tech Stack 💻

- **Frontend:** React, Vite, Tailwind CSS, React Router v6, FullCalendar, Recharts, Lucide Icons, React Hot Toast
- **Backend:** Node.js, Express.js, JWT, Mongoose
- **Database:** MongoDB
- **AI Provider:** Anthropic Claude (claude-sonnet-4-20250514)

---

## Getting Started 🚀

### 1. Prerequisites
- Node.js (v18+ recommended)
- MongoDB running locally or a MongoDB Atlas URI
- An Anthropic API Key

### 2. Configure Environment Variables
Copy `.env.example` to `.env` in the root folder:
```bash
cp .env.example .env
```
Fill in your details:
```env
ANTHROPIC_API_KEY=your_claude_api_key
MONGODB_URI=mongodb://127.0.0.1:27017/studyforge
JWT_SECRET=super_secret_jwt_key
PORT=5000
CLIENT_URL=http://localhost:5173
```

### 3. Install Dependencies
From the root directory, run the installer script to install root, server, and client packages:
```bash
npm run install:all
```

### 4. Run the Application
You can run both the frontend and backend concurrently in development mode using:
```bash
npm run dev
```

- Local frontend: `http://localhost:5173`
- Local backend: `http://localhost:5000`

---

## Deployment 🌍

### Backend (Render / Railway)
1. Set up a Web Service pointing to your repository.
2. Set the Root Directory to `server/` (or run it from root with `npm start`).
3. Set your environment variables (`MONGODB_URI`, `JWT_SECRET`, `ANTHROPIC_API_KEY`, etc.).
4. Start command: `node server/index.js`

### Frontend (Vercel / Netlify)
1. Deploy the `client/` directory.
2. Build command: `npm run build`
3. Check the output directory: `dist`
4. Make sure to define the `VITE_API_URL` environment variable to point to your live backend URL.

## License
MIT License.
