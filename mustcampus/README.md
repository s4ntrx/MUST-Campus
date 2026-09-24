# MUST Campus

> Your campus life, all in one place — Meru University of Science & Technology

A mobile-first Progressive Web App (PWA) for MUST students. Works offline, installable on Android and iOS, no backend required.

---

## 🚀 Deploy to Vercel (websites only — no terminal)

### Step 1 — Create GitHub Repo
1. Go to **https://github.com** → **New repository**
2. Name it `mustcampus` (or any name you prefer)
3. Set to **Public** or **Private**
4. ✅ Add a README file
5. Click **Create repository**

### Step 2 — Upload all files
In your new repo, click **Add file → Upload files** and upload everything from this ZIP:
```
index.html
manifest.json
sw.js
vercel.json
.gitignore
README.md
icons/
  icon-192.png
  icon-512.png
```
Click **Commit changes**.

### Step 3 — Deploy on Vercel
1. Go to **https://vercel.com** → Sign in with GitHub
2. Click **Add New Project**
3. Select your `mustcampus` repo → click **Import**
4. Framework Preset: **Other** (leave as is)
5. Click **Deploy** → wait ~30 seconds
6. Your app is live at `https://mustcampus-xxx.vercel.app` 🎉

### Step 4 — Custom domain (optional)
In Vercel dashboard → your project → **Settings → Domains** → add your domain.

---

## 📱 Install as App (PWA)

**Android (Chrome):**
1. Open the Vercel URL in Chrome
2. Tap the 3-dot menu → **Add to Home Screen**
3. Tap **Add** — it installs like a real app

**iOS (Safari):**
1. Open the Vercel URL in Safari
2. Tap the **Share** button (box with arrow)
3. Tap **Add to Home Screen** → **Add**

---

## 🛡️ Admin Panel

After registering, become admin by opening your browser console (F12) on the live site:

```javascript
// Run this in the browser console after logging in
let users = JSON.parse(localStorage.getItem('mc_users') || '[]');
let me = users.find(u => u.email === 'YOUR_EMAIL_HERE');
if (me) {
  me.role = 'admin';
  localStorage.setItem('mc_users', JSON.stringify(users));
  console.log('✅ You are now admin! Log out and back in.');
} else {
  console.log('❌ User not found. Make sure you registered first.');
}
```

Log out and back in → Profile tab → scroll down → **Admin Panel** appears.

**Admin capabilities:**
- 👥 View all registered users, ban/unban with reason
- 🚩 Review flagged content (posts reported by users)
- 📰 View and delete any post

---

## ✨ Features

- **Campus Feed** — Posts, likes, comments, pull-to-refresh, 9 seed posts
- **Chat** — Message list, full chat window with keyboard fix
- **Campus Connect** — Swipe/match, WhatsApp groups, advertisements
- **Events** — Featured event, upcoming list, add events
- **Clubs** — 8 default clubs + create your own, join/leave, club posts
- **Profile** — Edit name/photo/bio/course, academic info, notifications, privacy
- **Admin Panel** — Ban users, remove posts, review reports
- **PWA** — Works offline, installable on Android & iOS
- **Persists everything** — localStorage engine, survives page refresh and re-login

---

## 🔧 Tech Stack

- Pure HTML + CSS + JavaScript (no frameworks, no build step)
- localStorage for data persistence
- Service Worker for offline support
- PWA manifest for installability

---

## 📁 File Structure

```
mustcampus/
├── index.html        ← Complete app (2,481 lines)
├── manifest.json     ← PWA manifest
├── sw.js             ← Service worker (offline support)
├── vercel.json       ← Vercel deployment config
├── .gitignore
├── README.md
└── icons/
    ├── icon-192.png  ← PWA icon
    └── icon-512.png  ← PWA icon (large)
```

---

## 📝 Updating the App

1. Make changes to `index.html` on GitHub (click ✏️ pencil icon)
2. Commit changes
3. Vercel auto-deploys in ~30 seconds — no manual action needed

---

*MUST Campus · Foundation of Innovations · Meru University of Science & Technology*
