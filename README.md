# Face Recognition Brain — AI Face Detector

**Fullstack AI face detection app with user auth & PostgreSQL**

[Live Demo](https://face-recognition-brain.netlify.app) • [Frontend](https://github.com/ElenaGregov/face-recognition-brain-front-end) • [Backend](https://github.com/ElenaGregov/face-recognition-brain-api-back-end)

---

## Overview

> **Final project** from Zero to Mastery (ZTM)  
> **My full rebuild & deployment:**
> - **PostgreSQL database** (designed, migrated, deployed)
> - **User auth** with bcrypt + JWT
> - **Clarifai AI API** integration
> - **Full deployment** (Render)
> - **Separate frontend & backend repos**

---

## Features

- **Face detection** via **Clarifai API**
- **User registration / login**
- **Entry counter** per user
- **PostgreSQL** for persistent user data
- Responsive UI (Tachyons)
- Loading states & error handling

---

## Tech Stack

| Technology | Badge |
|----------|-------|
| React | ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) |
| Node.js | ![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white) |
| PostgreSQL | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white) |
| Clarifai | ![Clarifai](https://img.shields.io/badge/Clarifai-FF6600?style=for-the-badge&logo=clarifai&logoColor=white) |
| Render | ![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white) |

---

## Architecture

```
[Frontend: React] 
     ↓ (REST API)
[Backend: Node.js + Express]
     ↓
[PostgreSQL Database - Render]
```

---

## Database Schema (`users` table)

```sql
id          SERIAL PRIMARY KEY
name        VARCHAR(100)
email       TEXT UNIQUE NOT NULL
entries     BIGINT DEFAULT 0
joined      TIMESTAMP NOT NULL
password    TEXT NOT NULL
```

---

## Getting Started

### 1. Frontend
```bash
git clone https://github.com/ElenaGregov/face-recognition-brain-front-end.git
cd face-recognition-brain-front-end
npm install
npm start
```

### 2. Backend + PostgreSQL
See: [face-recognition-brain-api-back-end](https://github.com/ElenaGregov/face-recognition-brain-api-back-end)

### 3. Clarifai API Key
Add to `src/App.js`:
```js
const PAT = 'your_clarifai_pat';
```

---

## My Contributions (Real Work!)

| Task | Details |
|------|-------|
| **PostgreSQL DB** | Designed schema, migrated from mock data |
| **Deployment** |  Render  |
| **Auth System** | bcrypt hashing, JWT, session persistence |
| **Bug Fixes** | CORS, async errors, mobile layout |
| **Separation** | Split into frontend + backend repos |

---

## Live Demo

[https://face-recognition-brain.netlify.app](https://face-recognition-brain.netlify.app)

> **Try it:** Register → paste any photo URL → watch AI detect faces!

---

**Built & maintained by [Elena Gregov](https://elenagregov.netlify.app)**  
Prague, CZ • Open to **junior/mid fullstack roles**
