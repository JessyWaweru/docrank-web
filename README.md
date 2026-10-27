<div align="center">

# 🩺 DocRank · Web

### Find a doctor people actually trust.

**React + TypeScript app for searching, rating and saving specialists across Nairobi, Kisumu and Mombasa.**

[![Live Demo](https://img.shields.io/badge/🔴_Live_Demo-DocRank-0d9488?style=for-the-badge)](https://doctor-search-frontend.onrender.com)
[![Backend](https://img.shields.io/badge/Backend_Repo-docrank--api-0f172a?style=for-the-badge&logo=github)](https://github.com/JessyWaweru/docrank-api)

![React 19](https://img.shields.io/badge/React_19-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite_7-646CFF?logo=vite&logoColor=white)
![Tailwind 4](https://img.shields.io/badge/Tailwind_4-06B6D4?logo=tailwindcss&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?logo=shadcnui&logoColor=white)
![Radix](https://img.shields.io/badge/Radix_UI-161618?logo=radixui&logoColor=white)

<sub>⏳ Free-tier hosting: the first load may take ~45s while the API wakes up.</sub>

</div>

---

## 📸 Screenshots

| 🗂️ Directory | 🩺 Profile & reviews |
|:---:|:---:|
| ![Listing](screenshots/01_doctor_listing.png) | ![Detail](screenshots/02_doctor_detail_1_desktop.png) |
| 🔐 **Register (OTP)** | 🔖 **Saved doctors** |
| ![Register](screenshots/03_register_desktop.png) | ![Saved](screenshots/04_saved_desktop.png) |

## ✨ What makes it feel fast

- 🔍 **Debounced live search** (300ms) across name, specialty, hospital and location, so there's no request spam on every keystroke
- 🔖 **Optimistic saves**: the heart fills instantly and the navbar badge updates live, then syncs with the API (and rolls back if the request fails)
- 🩺 **Tabbed profile modal**: contact info, reviews and your own rating form, all without leaving the list
- 🏠 **No login wall**: top-rated doctors are visible straight away; you only sign in to review or save

## 🔐 Auth flow

Register → enter the **6-digit OTP** from your inbox → you're logged in with a JWT.

An Axios interceptor attaches `Bearer <token>` to every request, and React Context (`AuthContext`, `SavedContext`) keeps the session and saved list in sync across the app. Forgotten password? Same OTP flow.

## 🗺️ Pages

| Route | Page |
|---|---|
| `/` | Hero + top-rated doctors |
| `/doctors` | Search, filter & rank |
| `/saved` · `/my-reviews` | Your saved doctors · your reviews 🔐 |
| `/login` · `/register` · `/forgot-password` · `/reset-password` | Auth |

## 🚀 Run it locally

```bash
git clone https://github.com/JessyWaweru/docrank-web.git
cd docrank-web
npm install
npm run dev                # → http://localhost:5173
```

Set `VITE_API_URL` to your backend (defaults to `http://localhost:8000/api`), and run [docrank-api](https://github.com/JessyWaweru/docrank-api) alongside it.

---

<div align="center">

**Built by Jessy Bryan Waweru**: actuary by training, full-stack engineer by obsession.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jessy-waweru-b8051a288)
[![Email](https://img.shields.io/badge/Email-EA4335?logo=gmail&logoColor=white)](mailto:bryanjessywaweru@gmail.com)
[![GitHub](https://img.shields.io/badge/More_projects-181717?logo=github)](https://github.com/JessyWaweru)

</div>
