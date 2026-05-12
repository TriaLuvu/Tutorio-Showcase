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

---

# 🎓 Tutorio UI Demo (Ελληνικά)

Καλώς ήρθατε στο **Tutorio UI Demo**. Αυτό το αποθετήριο παρουσιάζει τα συστατικά του frontend και τον σχεδιασμό της διεπαφής χρήστη του Tutorio, μιας Progressive Web App (PWA) εφαρμογής με προσέγγιση offline-first, σχεδιασμένης για ιδιαίτερα μαθήματα (καθηγητές).

🔗 **Live App:** [tutorio.duckdns.org](http://tutorio.duckdns.org)

**Σημείωση:** Αυτό είναι ένα δημόσιο demo branch. Όλη η ιδιόκτητη λογική του backend, οι ρυθμίσεις και ο πηγαίος κώδικας έχουν αφαιρεθεί. Σκοπός αυτού του αποθετηρίου είναι να επιδείξει την αρχιτεκτονική του UI, το σύστημα σχεδιασμού και τη δομή των components.

---

## 📖 Τι κάνει η Εφαρμογή

Το Tutorio απλοποιεί τις καθημερινές εργασίες ενός καθηγητή. Παρέχει ένα κεντρικό dashboard για:
- **Διαχείριση Μαθητών:** Παρακολούθηση πληροφοριών επικοινωνίας, ωριαίων αμοιβών και εξατομικευμένων μαθημάτων.
- **Προγραμματισμό Μαθημάτων:** Καθορισμός εβδομαδιαίας διαθεσιμότητας και δυναμικός υπολογισμός επερχόμενων μαθημάτων.
- **Παρακολούθηση Οικονομικών:** Παρακολούθηση ιστορικού μαθημάτων, δημιουργία αναφορών οφειλών και παραγωγή επαγγελματικών αποδείξεων σε PDF.
- **Διασφάλιση Ασφάλειας:** Προστασία ευαίσθητων δεδομένων μαθητών με Κλείδωμα Εφαρμογής (Βιομετρικά/PIN) και Λειτουργία Απορρήτου (Privacy Mode).

Είναι χτισμένη με προσέγγιση **offline-first**, διασφαλίζοντας απρόσκοπτη χρήση χωρίς σύνδεση στο διαδίκτυο, ενώ συγχρονίζει τα δεδομένα στο cloud όταν υπάρχει σύνδεση.

---

## 🛠️ Τεχνολογικό Stack

Αυτό το έργο χρησιμοποιεί σύγχρονες τεχνολογίες ιστού με έμφαση στην ταχύτητα και την αξιοπιστία:
- **Framework:** React 18
- **Build Tool:** Vite
- **Styling:** Vanilla CSS χρησιμοποιώντας ένα σύστημα σχεδιασμού Glassmorphism
- **Διαχείριση Κατάστασης (State Management) / Αποθήκευση Εκτός Σύνδεσης (Offline Storage):** Προσαρμοσμένος wrapper για το `localStorage` (`safeStorage`) για άμεση πρόσβαση εκτός σύνδεσης
- **Cloud Backend (Αρχική Εφαρμογή):** Firebase (Authentication & Firestore)
- **Δυνατότητες PWA:** Service Workers για προσωρινή αποθήκευση (caching) εκτός σύνδεσης και δυνατότητα εγκατάστασης

---

## ✨ Βασικά Χαρακτηριστικά & Αρχιτεκτονικές Αποφάσεις

### 1. Offline-First Αρχιτεκτονική
Για να λύσει το πρόβλημα των αναξιόπιστων συνδέσεων στο διαδίκτυο, η εφαρμογή χρησιμοποιεί το τυπικό `localStorage` ως τη μοναδική πηγή αλήθειας (single source of truth) για το UI. Ο συγχρονισμός στο cloud (μέσω Firebase στην πλήρη έκδοση) γίνεται ασύγχρονα στο παρασκήνιο. Αυτό εξασφαλίζει μηδενική αναμονή φόρτωσης (loading spinners) κατά την πλοήγηση στην εφαρμογή.

### 2. Σύστημα Σχεδιασμού Glassmorphism
Το UI χρησιμοποιεί την αισθητική "Glassmorphism"—βαθιά μπλε φόντα, ημιδιαφανείς επιφάνειες με θόλωμα (backdrop blurs) και απαλά περιγράμματα. Αυτό δημιουργεί μια premium, μοντέρνα αίσθηση. Το CSS είναι εξαιρετικά modular, βασιζόμενο σε προσαρμοσμένες μεταβλητές CSS (`--primary`, `--surface-opaque`, κ.λπ.) για να εξασφαλίσει συνοχή.

### 3. Progressive Web App (PWA)
Το Tutorio είναι πλήρως εγκαταστάσιμο σε iOS και Android. Περιλαμβάνει προσαρμοσμένες αυτόνομες συμπεριφορές (standalone behaviors) και components βελτιστοποιημένα για αφή (όπως χειρονομίες σάρωσης/swipe gestures) για να μιμείται την εμπειρία μιας εγγενούς (native) εφαρμογής.

### 4. Δίγλωσση Υποστήριξη
Η εφαρμογή είναι σχεδιασμένη ώστε να υποστηρίζει δυναμική εναλλαγή γλώσσας (Αγγλικά και Ελληνικά) χωρίς να απαιτείται επαναφόρτωση της σελίδας.

---

## 🖱️ Αλληλεπίδραση με το UI

Αν χρησιμοποιούσατε την πλήρως λειτουργική εφαρμογή, ορίστε πώς θα αλληλεπιδρούσατε με τη διεπαφή:

1. **Onboarding & Σύνδεση:**
   Κατά την πρώτη επίσκεψη, σας υποδέχεται μια σελίδα προορισμού (landing page). Μετά την ταυτοποίηση, μια καθοδηγούμενη περιήγηση προϊόντος παρουσιάζει τα κύρια χαρακτηριστικά.
2. **Πλοήγηση στο Dashboard:**
   Το κύριο dashboard εμφανίζει γρήγορα στατιστικά (π.χ. συνολικοί μαθητές, μηνιαία έσοδα). Μια κάτω μπάρα πλοήγησης (bottom navigation bar) παρέχει γρήγορη πρόσβαση στις Βασικές Ενότητες (Core Modules): Dashboard, Calendar (Ημερολόγιο) και Profile (Προφίλ).
3. **Διαχείριση Μαθητών:**
   Κάνοντας κλικ στην κάρτα ενός μαθητή, αυτή αναπτύσσεται για να αποκαλύψει λεπτομερείς πληροφορίες. Από εκεί, μπορείτε να προσθέσετε μαθήματα, να καταγράψετε πληρωμές ή να επεξεργαστείτε το πρόγραμμά τους.
4. **Προγραμματισμός:**
   Η προβολή Ημερολογίου (Calendar) σας επιτρέπει να πατήσετε σε οποιαδήποτε ημέρα για να δείτε τα προγραμματισμένα μαθήματα. Οπτικές ενδείξεις (κουκκίδες και χρώματα) δείχνουν ποιες ημέρες έχουν μαθήματα ή συγκρούσεις στο πρόγραμμα.
5. **Δημιουργία Αναφορών:**
   Στην ενότητα Προφίλ, ένα απλό κλικ στο "Εξαγωγή Δεδομένων" (Export Data) δημιουργεί και κατεβάζει μια λεπτομερή αναφορά PDF όλων των οφειλών των μαθητών και των ολοκληρωμένων μαθημάτων.

---

*Αυτό το δημόσιο demo παρέχεται για σκοπούς χαρτοφυλακίου (portfolio) και επίδειξης. Σχεδιάστηκε και αναπτύχθηκε από την Antigravity.*
