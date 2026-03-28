# 🏛️ CMC Portal — Colombo Municipal Council
### Citizen Complaint Management System

A full-featured, mobile-responsive web portal for Colombo citizens to lodge complaints, track resolutions, and for CMC staff/admin to manage cases — powered by Supabase and Claude AI.

---

## 🚀 Live Demo (GitHub Pages)

> Once deployed: `https://<your-username>.github.io/cmc-portal/`

---

## ✨ Features

| Feature | Description |
|---|---|
| 🏠 Public Homepage | Landing page with stats, about, services & contact |
| 👤 Citizen Portal | Register, login, lodge & track complaints |
| 🛡️ Admin Dashboard | Full complaint management, staff assignment, analytics |
| 👷 Staff Portal | View assigned tasks, update status, attendance |
| 🤖 AI Assistant | Claude-powered chatbot for citizens and admins |
| 📊 Reports & Analytics | Charts, trends, department-level breakdowns |
| 📱 Mobile Responsive | Fully optimised for phones and tablets |
| 🗄️ Supabase Backend | Real-time database with persistent storage |

---

## 🗂️ Project Structure

```
cmc-portal/
├── index.html        ← The entire application (single-file)
├── README.md         ← This file
└── .gitignore        ← Standard web gitignore
```

This is a **single-file application** — everything (HTML, CSS, JavaScript) lives in `index.html`. No build step, no dependencies, no server required.

---

## ⚙️ Configuration

All credentials are hardcoded inside `index.html` near line 480:

```js
var _HC_SB_URL  = 'https://your-project.supabase.co';
var _HC_SB_KEY  = 'your-supabase-anon-key';
var _HC_ANT_KEY = 'your-anthropic-api-key';
```

To update them, open `index.html` in any text editor and replace those three values.

---

## 🗄️ Supabase Setup

Run this SQL in your Supabase **SQL Editor** (Dashboard → SQL Editor → New Query):

The SQL schema is included at the bottom of `index.html` (scroll to the very end — it's inside a `<textarea>` for reference).

Key tables:
- `accounts` — citizen user accounts
- `staff` — CMC staff records
- `complaints` — all complaint records
- `admin_requests` — escalation/edit requests
- `log` — audit trail

After running the schema, go to **Authentication → Policies** and ensure the `anon` role has read/write access, or run:
```sql
grant all on all tables in schema public to anon, authenticated;
grant all on all sequences in schema public to anon, authenticated;
```

---

## 🌐 Deploy to GitHub Pages (5 minutes)

### Option A — GitHub Website (no terminal needed)

1. Go to [github.com](https://github.com) → **New repository**
2. Name it `cmc-portal`, set to **Public**, click **Create repository**
3. Click **uploading an existing file**
4. Drag and drop both `index.html` and `README.md`
5. Click **Commit changes**
6. Go to **Settings → Pages**
7. Under *Source*, select **Deploy from a branch → main → / (root)**
8. Click **Save** — your site will be live in ~60 seconds at:
   `https://<your-username>.github.io/cmc-portal/`

---

### Option B — Git Terminal

```bash
# 1. Clone your new empty repo (create it on GitHub first)
git clone https://github.com/<your-username>/cmc-portal.git
cd cmc-portal

# 2. Copy project files in, then:
git add .
git commit -m "Initial commit — CMC Portal"
git push origin main

# 3. Enable GitHub Pages in repo Settings → Pages → main branch
```

---

## 🔐 Demo Credentials

| Role | Username / Email | Password |
|---|---|---|
| Citizen | amara@example.com | demo123 |
| Admin | admin | admin123 |
| Staff | roshan@cmc.lk | staff123 |

---

## 📱 Mobile Support

The portal is fully responsive:
- Sidebar becomes a horizontal scrollable top nav on mobile
- Modals slide up as bottom sheets
- All grids reflow to 1–2 columns
- Touch-friendly tap targets throughout

---

## 🛠️ Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS (zero dependencies, zero build step)
- **Database:** [Supabase](https://supabase.com) (PostgreSQL REST API)
- **AI:** [Anthropic Claude](https://anthropic.com) (claude-sonnet-4-20250514)
- **Fonts:** Google Fonts (Syne + DM Sans)
- **Hosting:** GitHub Pages

---

## 📄 License

© 2025 Colombo Municipal Council. All rights reserved.
