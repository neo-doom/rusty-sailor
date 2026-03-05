# Sailing Fitness Tracker — PWA Setup Guide

A 10-week fitness tracker built as a Progressive Web App (PWA) that you can install on your phone and use offline at the gym. Your progress is saved locally on your device.

---

## What you'll need

- A **GitHub account** (free) — sign up at [github.com](https://github.com) if you don't have one
- About **10 minutes**
- No coding knowledge required — just follow the steps below

---

## Step-by-step deployment

### 1. Create a new GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name it something like `sailing-fitness` (the exact name doesn't matter)
3. Set it to **Public** (required for free GitHub Pages hosting)
4. **Do NOT** check "Add a README file" — leave it empty
5. Click **Create repository**

### 2. Upload the app files

1. On your new empty repository page, click the **"uploading an existing file"** link (it appears in the instructions on the page)
2. Drag and drop **all the files and folders** from the project:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icons/` folder (containing `icon-192.png` and `icon-512.png`)
3. Scroll down and click **"Commit changes"**

### 3. Enable GitHub Pages

1. In your repository, click **Settings** (gear icon, top menu)
2. In the left sidebar, click **Pages**
3. Under **"Source"**, select **"Deploy from a branch"**
4. Under **"Branch"**, select **main** and leave the folder as **/ (root)**
5. Click **Save**
6. Wait 1–2 minutes, then refresh the page — you'll see a green banner with your site URL:
   ```
   https://YOUR-USERNAME.github.io/sailing-fitness/
   ```

### 4. Install on your phone

**iPhone (Safari):**
1. Open the URL from Step 3 in **Safari** (must be Safari, not Chrome)
2. Tap the **Share button** (square with arrow)
3. Scroll down and tap **"Add to Home Screen"**
4. Tap **Add** — the app icon will appear on your home screen

**Android (Chrome):**
1. Open the URL in **Chrome**
2. You should see a banner saying "Add Sailing Fitness Tracker to Home screen" — tap it
3. If no banner appears, tap the **three-dot menu (⋮)** → **"Install app"** or **"Add to Home screen"**

---

## How it works

- **Tap any exercise** to check it off
- **"Mark All"** button completes an entire day
- **Week tabs** scroll horizontally across all 10 weeks
- **Day tabs** show each workout within a week
- **Workout Notes** section lets you jot down weights, feelings, adjustments (saved per week)
- **Progress** is shown at overall, week, and day levels
- **Works offline** — once loaded, no internet needed at the gym
- **Data persists** in your phone's browser storage (localStorage)

---

## Troubleshooting

**"My progress disappeared"**
- Make sure you're always opening the app the same way (home screen icon)
- Don't clear your browser data/cache — that erases localStorage
- On iPhone, avoid "Private Browsing" mode

**"I can't install it on my home screen"**
- iPhone: Must use Safari, not Chrome or other browsers
- Android: Must use Chrome
- Make sure the GitHub Pages URL is working first

**"The site says 404"**
- Double-check that GitHub Pages is enabled (Settings → Pages)
- Make sure `index.html` is in the root of your repository (not inside a subfolder)
- Wait 2–3 minutes after enabling Pages — it takes a moment to deploy

---

## Updating the app

If you ever need to update (e.g., modify exercises), just edit `index.html` on GitHub and commit. The service worker will pick up changes on the next visit when you're online. Your saved progress won't be affected.
