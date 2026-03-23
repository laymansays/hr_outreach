# 🎓 HR Outreach Tracker — Bangalore 2026

> A clean, minimal dashboard for Training & Placement Coordinators to manage outreach to HR / Talent Acquisition professionals in Bangalore.  
> Built for **BCA college placement teams** targeting entry-level & internship hiring in IT, Data, Finance, Sales, and Operations.

---

## ✨ Features

- **10 HR Contacts** fetched via Vibe Prospecting (Explorium) — real data from Bengaluru
- **Smart Search Bar** — filter by Company Name (required), Website (optional), Location (default: Bengaluru)
- **Live Card Filtering** — real-time filtering as you type
- **LinkedIn Preview Dropdown** — 4-step outreach workflow with profile preview
- **Copy Outreach Message** — one-click copy of your connect note
- **Outreach Status Tracker** — mark contacts as Pending / Contacted / Replied
- **Stats Bar** — live counts update as you track progress

---

## 🚀 Deploy to Vercel

### Option A — Vercel CLI (Recommended)

```bash
# 1. Install Vercel CLI globally
npm install -g vercel

# 2. Navigate to this project folder
cd hr-outreach-tracker

# 3. Login to Vercel
vercel login

# 4. Deploy (follow the prompts)
vercel

# 5. For production deployment
vercel --prod
```

> When prompted:
> - **Set up and deploy?** → `Y`
> - **Which scope?** → Select your account
> - **Link to existing project?** → `N`
> - **Project name** → `hr-outreach-tracker` (or any name you like)
> - **In which directory is your code?** → `./` (press Enter)
> - **Override settings?** → `N`

---

### Option B — Vercel Dashboard (No CLI needed)

1. Go to **[vercel.com](https://vercel.com)** and sign in
2. Click **"Add New Project"**
3. Upload this folder as a **ZIP** or push it to a GitHub repo and import
4. Vercel will auto-detect it as a static site
5. Click **Deploy** — done! 🎉

---

### Option C — GitHub + Vercel (Best for updates)

```bash
# 1. Create a GitHub repo and push
git init
git add .
git commit -m "Initial commit: HR Outreach Tracker"
git remote add origin https://github.com/YOUR_USERNAME/hr-outreach-tracker.git
git push -u origin main

# 2. Go to vercel.com → New Project → Import from GitHub
# 3. Select your repo → Deploy
# Every future `git push` auto-deploys!
```

---

## 🗂 Project Structure

```
hr-outreach-tracker/
├── public/
│   └── index.html        ← Main dashboard (all-in-one)
├── vercel.json           ← Vercel deployment config
├── package.json          ← Project metadata + dev script
└── README.md             ← This file
```

---

## 🖥 Run Locally

```bash
# Install dev dependency
npm install

# Start local server at http://localhost:3000
npm run dev
```

---

## 📝 Outreach Message

The default connect note used in the dashboard:

> *"Hi, good day. I work with BCA students trained in AWS & Cloud fundamentals, ready for entry-level roles. Open to connecting for hiring opportunities."*

You can change this in `public/index.html` — search for `const MSG =` near the top of the `<script>` block.

---

## 🔧 Customise Contacts

All contact data lives in the `DATA` array inside `public/index.html`.  
Each contact object has these fields:

```js
{
  id: 1,
  init: "M",                          // Avatar initial
  grad: "linear-gradient(...)",        // Avatar background
  name: "Full Name",
  title: "Job Title",
  company: "Company Name",
  website: "company.com",
  email: "email@company.com",          // null if not available
  li: "https://linkedin.com/in/...",
  focus: ["Tag 1", "Tag 2", "Tag 3"],  // Hiring focus tags
  xp: "Short bio / experience line"
}
```

---

## 🛠 Tech Stack

- **Pure HTML + CSS + Vanilla JS** — zero dependencies, zero build step
- **Google Fonts** — Instrument Serif, DM Mono, Outfit
- **Data source** — Vibe Prospecting (Explorium) via Claude AI

---

## 📄 License

MIT — free to use, modify, and share.
