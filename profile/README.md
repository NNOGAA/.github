# NOGA - Food Nutrition Analysis Platform

AI-powered mobile app for analyzing food nutrition through image recognition and OCR technology.

## 🎯 Overview

NOGA helps users make informed dietary choices by scanning food packaging labels and providing instant health analysis with personalized recommendations.

## 🏗️ Architecture
```
Mobile App (React Native) 
    ↓
Backend API (Node.js)
    ↓
AI Service (Python + Gemini AI)
```

## 📦 Services

| Service | Tech Stack | Purpose |
|---------|-----------|---------|
| **Mobile App** | React Native + Expo | User interface & camera |
| **Backend** | Node.js + Express + MySQL | Image upload & storage |
| **AI Service** | Python + FastAPI + Gemini AI | OCR & health analysis |

## ✨ Features

- 📸 Image-based ingredient extraction
- 🔬 Nutrition facts OCR
- 🤖 AI health summaries
- ⚠️ Preservative detection
- ✅ Auto typo correction

## 🚀 Quick Start

### Mobile App
```bash
npm install
npm start
```

### Backend
```bash
npm install
npm run dev
```

### AI Service
```bash
pip install -r requirements.txt
python main.py
```

## 🌐 Deployment

All services deployed on Railway:
- Backend: `https://noga-be-production.up.railway.app/`
- AI: `https://noga-ai-production.up.railway.app/`

## 🔑 Environment Setup

**Backend**
```env
DATABASE_URL=mysql://user:pass@host:port/db
PORT=3000
```

**AI Service**
```env
DB_HOST=host
DB_USER=user
DB_PASSWORD=pass
GOOGLE_API_KEY=your_key
```

**Mobile**
```env
EXPO_PUBLIC_API_URL=https://your-backend-url/
EXPO_PUBLIC_AI_URL=https://your-ai-url/
```

## 📊 Database

**ocr_table**
- `sessionid` - Unique session ID
- `status` - Processing status
- `ingredients` - JSON ingredients data
- `nutrition_info` - JSON nutrition data

## 🐳 Docker
```bash
docker build -t noga-backend .
docker run -p 3000:3000 --env-file .env noga-backend
```
