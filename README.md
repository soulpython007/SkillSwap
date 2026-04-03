# 🌟 SkillSwap

**SkillSwap** is a peer-to-peer campus skill-sharing marketplace that connects students who want to learn new skills with those who can teach them — all within a trusted campus ecosystem.

Built for the **GDG TechSprint Hackathon**, SkillSwap leverages real-time systems, AI-powered matching, and Firebase to create a seamless learning experience.

---

## 🚀 Problem Statement

Students possess valuable skills (coding, music, languages, etc.), but there is no centralized, real-time, and trusted platform within a campus to:

* Discover peers with relevant skills
* Connect instantly
* Exchange knowledge informally

Existing solutions are:

* Paid 💸
* Global (not campus-specific) 🌍
* Outdated (notice boards, WhatsApp groups) 📌

---

## 💡 Solution Overview

SkillSwap solves this by providing a **campus-exclusive marketplace** where students can:

* Post skills they can teach (**Offers**)
* Request skills they want to learn (**Requests**)
* Get matched using **AI + tag-based logic**
* Chat and schedule sessions in real-time

---

## ✨ Features

### 🔐 Authentication

* Google Sign-In (restricted to campus domain)
* Secure and verified users

### 📌 Skill Marketplace

* Post Offers and Requests
* Tag-based categorisation (e.g., Python, Guitar, Cooking)

### 🤖 AI Smart Matching

* AI-powered suggestions and match explanations
* Improves discovery and relevance

### 💬 Real-Time Chat

* Instant messaging between users
* Powered by Firebase Realtime Database

### 📅 Session Booking

* Schedule sessions using time slots
* Structured interaction flow

### ⭐ Rating & Reputation

* Anonymous feedback system
* Builds trust within the platform

### 🔔 Notifications

* Real-time alerts for matches and updates

---

## 🛠️ Tech Stack

### Frontend

* React (Vite)
* TypeScript
* Tailwind CSS
* Zustand (State Management)

### Backend (BaaS)

* Firebase Authentication
* Cloud Firestore
* Firebase Realtime Database
* Firebase Cloud Messaging
* Firebase Hosting

### AI Integration

* Google Gemini API (for smart matching & tag suggestions)

---

## 🏗️ Architecture Overview

```
User (Browser)
   ↓
React Frontend (Vite + Zustand)
   ↓
Firebase Services
   ├── Auth (Google Sign-In)
   ├── Firestore (Listings, Bookings, Ratings)
   ├── Realtime DB (Chat)
   ├── Cloud Messaging (Notifications)
   ↓
Gemini AI (Matching + Suggestions)
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/soulpython007/SkillSwap.git
cd SkillSwap
```

---

### 2. Install Dependencies

```bash
npm install
```

---

### 3. Environment Variables

Create a `.env` file in the root directory:

```env
VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=
VITE_GEMINI_API_KEY=
```

> ⚠️ Never commit `.env` to GitHub

---

### 4. Firebase Setup

* Create a Firebase project
* Enable:

  * Authentication (Google Sign-In)
  * Firestore Database
  * Realtime Database
* Add your domain to **Authorized Domains**

---

### 5. Run Locally

```bash
npm run dev
```

Visit:

```
http://localhost:5173
```

---

### 6. Build for Production

```bash
npm run build
```

---

### 7. Deploy to Firebase

```bash
firebase deploy
```

---

## 🌐 Live Demo

👉 https://gdg-hackathon-f936d.web.app

---

## 🔐 Security Considerations

* Firebase config is public but restricted via rules
* Firestore rules enforce authenticated access
* API keys should **not be exposed in frontend**

### Recommended Improvement:

* Move Gemini API calls to backend (Firebase Functions)

---

## 📊 Data Flow

```
User Login → Firebase Auth
        ↓
Create Listing → Firestore
        ↓
Matching Logic → AI + Tags
        ↓
Chat → Realtime DB
        ↓
Booking → Firestore
        ↓
Feedback → Ratings System
```

---

## 🚀 Future Enhancements

* AI-based personalised recommendations
* Leaderboards & gamification
* Mobile application
* Resume/portfolio integration
* Advanced analytics dashboard

---

## 👥 Team

**Team NASA**

* Team Lead: Aniket Mohanty

---

## 📂 Repository Structure

```
src/
 ├── components/
 ├── pages/
 ├── services/
 ├── store/
 ├── hooks/
 ├── utils/
 ├── App.tsx
 └── main.tsx
```

---

## 🎯 Key Highlights

* Real-time full-stack application
* AI-powered matching system
* Serverless architecture (Firebase)
* Scalable and production-ready design

---

## ❤️ Acknowledgements

Built for **GDG Hackathon** with a focus on solving real campus problems using modern technologies.

---

