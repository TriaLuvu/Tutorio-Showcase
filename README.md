# 🎓 Tutorio UI Demo

Welcome to the **Tutorio UI Demo**. This repository showcases the frontend components and user interface design of Tutorio, an offline-first Progressive Web App (PWA) designed for private tutors.

🔗 **Live App:** [tutorio.duckdns.org](http://tutorio.duckdns.org)

**Note:** This is a public demo branch. All proprietary backend logic, configurations, and source code have been removed. The purpose of this repository is to demonstrate the UI architecture, design system, and component structure.

---

## 📖 What the App Does

Tutorio streamlines the daily tasks of a private tutor. It provides a centralized dashboard to:
- **Manage Students:** Keep track of contact information, hourly rates, and personalized subjects.
- **Schedule Lessons:** Set weekly availability and dynamically calculate upcoming lessons.
- **Track Finances:** Monitor lesson histories, generate debt reports, and produce professional PDF receipts.
- **Ensure Security:** Protect sensitive student data with App Lock (Biometrics/PIN) and Privacy Mode.

It is built with an **offline-first** approach, ensuring seamless usage without an internet connection, while syncing data to the cloud when online.

---

## 🛠️ Technical Stack

This project utilizes modern web technologies with a focus on speed and reliability:
- **Framework:** React 18
- **Build Tool:** Vite
- **Styling:** Vanilla CSS utilizing a Glassmorphism design system
- **State Management / Offline Storage:** Custom `localStorage` wrapper (`safeStorage`) for instantaneous offline access
- **Cloud Backend (Original App):** Firebase (Authentication & Firestore)
- **PWA Capabilities:** Service Workers for offline caching and installability

---

## ✨ Key Features & Architectural Decisions

### 1. Offline-First Architecture
To solve the problem of unreliable internet connections, the app uses standard `localStorage` as the single source of truth for the UI. Cloud syncing (via Firebase in the full version) happens asynchronously in the background. This ensures zero loading spinners when navigating the app.

### 2. Glassmorphism Design System
The UI employs a "Glassmorphism" aesthetic—deep blue backgrounds, translucent surfaces with backdrop blurs, and soft borders. This creates a premium, modern feel. The CSS is highly modular, relying on custom CSS variables (`--primary`, `--surface-opaque`, etc.) to ensure consistency.

### 3. Progressive Web App (PWA)
Tutorio is fully installable on iOS and Android. It includes custom standalone behaviors and touch-optimized components (like swipe gestures) to mimic a native app experience.

### 4. Bilingual Support
The application is architected to support dynamic language switching (English and Greek) without requiring a page reload.

---

## 🖱️ Interacting with the UI

If you were to use the fully functional application, here is how you would interact with the interface:

1. **Onboarding & Login:**
   Upon first visit, you are greeted with a landing page. After authenticating, a guided product tour introduces the main features.
2. **Dashboard Navigation:**
   The main dashboard displays quick statistics (e.g., total students, monthly revenue). A bottom navigation bar provides quick access to Core Modules: Dashboard, Calendar, and Profile.
3. **Managing Students:**
   Clicking on a student card expands it to reveal detailed information. From here, you can add subjects, record payments, or edit their schedule.
4. **Scheduling:**
   The Calendar view allows you to tap on any day to see scheduled lessons. Visual indicators (dots and colors) show which days have lessons or conflicts.
5. **Generating Reports:**
   In the Profile section, a single click on "Export Data" generates and downloads a detailed PDF report of all student debts and completed lessons.

---

*This public demo is provided for portfolio and demonstration purposes. Designed and developed by Antigravity.*
