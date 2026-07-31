# 📚 College Attendance Tracker

A responsive, multi-user web application to track subject-wise college attendance, calculate required/affordable absences, and sync data securely across devices using Supabase and Vercel.

![HTML5](https://img.shields.io/badge/Frontend-HTML%2FCSS%2FJS-orange)
![Supabase](https://img.shields.io/badge/Database-Supabase%20%2F%20Postgres-green)
![Vercel](https://img.shields.io/badge/Hosting-Vercel-black)

---

## ✨ Features

- **Subject-Wise Tracking:** Track theory and lab classes independently.
- **Smart Attendance Math:** Automatically calculates:
  - Attendance percentage.
  - Number of classes you can safely afford to miss.
  - Number of consecutive classes required to reach target threshold (e.g., 75%).
- **Multi-Device & Multi-User:** Built-in authentication (Email/Password) powered by Supabase.
- **Data Security:** Row Level Security (RLS) guarantees users can only view and modify their own records.
- **Mobile First:** Optimized UI for smartphones and desktop browsers alike.

---

## 🛠️ Tech Stack

- **Frontend:** Vanilla HTML5, CSS3 (CSS Variables, Grid, Flexbox), JavaScript (ES6)
- **Database & Auth:** [Supabase](https://supabase.com) (PostgreSQL)
- **Deployment:** [Vercel](https://vercel.com)

---

## 🚀 Getting Started

### 1. Database Setup (Supabase)

1. Create a free project on [Supabase](https://supabase.com).
2. Create a table named `subjects` with columns:
   - `id` (uuid, primary key)
   - `name` (text)
   - `type` (text)
   - `min_attendance` (int4)
   - `attended` (int4)
   - `missed` (int4)
   - `created_at` (timestamp)
3. Open the **SQL Editor** in Supabase dashboard and run the code provided in [`schema.sql`](./schema.sql) to set up Row Level Security (RLS).

### 2. Connect Credentials

Replace the project credentials in `index.html`:

```javascript
var SUPABASE_URL = 'YOUR_SUPABASE_URL';
var SUPABASE_ANON_KEY = 'YOUR_SUPABASE_PUBLISHABLE_KEY';
