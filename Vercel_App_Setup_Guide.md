# Sabhi Digital - Vercel App Setup Guide
## How to Create & Deploy Your Webinar Checklist App

---

# WHAT YOU'RE BUILDING

A **simple web app** (like Google Sheets but on the internet) that:
- Shows webinar checklist
- Team marks ✓ when steps are done
- Auto-fills timestamp & name
- Works on any browser (mobile, desktop)
- Deployed on Vercel (free, fast)

**NOT a replacement for Google Sheets** — this is just a nicer interface for the same checklist.

---

# SETUP OVERVIEW (4 STEPS)

```
Step 1: Create GitHub Account
         ↓
Step 2: Create Project on Your Computer
         ↓
Step 3: Push Code to GitHub
         ↓
Step 4: Deploy to Vercel
```

---

# STEP 1: CREATE GITHUB ACCOUNT (5 minutes)

### What is GitHub?
- Free platform to store code
- Vercel uses GitHub to deploy apps
- You'll push your code here, Vercel pulls it

### How to Create:
1. Go to **https://github.com**
2. Click **"Sign up"**
3. Enter email: `aditya@sabhidigital.com`
4. Create password (something strong)
5. Create username: `sabhidigital` or `aditya-sabhi` (anything is fine)
6. Verify email (check your inbox)
7. Done ✓

---

# STEP 2: CREATE PROJECT ON YOUR COMPUTER (10 minutes)

### What You Need:
- **Node.js** installed (download from https://nodejs.org - click the big green button)
- **VS Code** (optional, but makes it easier) - https://code.visualstudio.com
- **Terminal** (command line) - built into Mac/Linux, use PowerShell on Windows

### Create the Project:

**Option A: Using Terminal (Recommended)**

1. Open Terminal (Mac/Linux) or PowerShell (Windows)
2. Navigate to where you want to save the project:
   ```
   cd Documents
   ```
3. Create a new project folder:
   ```
   mkdir webinar-checklist-app
   cd webinar-checklist-app
   ```
4. Create a Next.js project:
   ```
   npx create-next-app@latest . --typescript --tailwind --eslint
   ```
5. When asked questions, select:
   - "Would you like to use ESLint?" → **Yes**
   - "Would you like to use Tailwind CSS?" → **Yes**
   - Rest default (just press Enter)
6. Wait for it to install (2-3 minutes)

**Option B: Using VS Code GUI**
- Open VS Code
- Click File → Open Folder
- Create new folder: `webinar-checklist-app`
- Open integrated terminal (View → Terminal)
- Run the same commands above

### After Setup:
```
Your project folder structure will look like:
webinar-checklist-app/
  ├── app/
  ├── components/
  ├── package.json
  ├── tailwind.config.js
  └── ... (other files)
```

---

# STEP 3: ADD THE CODE (15 minutes)

You'll replace some files with the actual app code (I'll provide this next).

### Files to Create/Edit:

1. **`app/page.tsx`** — Main checklist display
2. **`app/layout.tsx`** — Page structure
3. **`components/Checklist.tsx`** — Checklist component
4. **`lib/data.ts`** — Sample data (clients, steps, team)

### How to Add Code:

1. Open VS Code (or your editor)
2. Open the `webinar-checklist-app` folder
3. Navigate to `app/page.tsx`
4. Delete all content
5. Copy-paste the code I'll provide
6. Save (Ctrl+S or Cmd+S)
7. Repeat for other files

### Test Locally:
```
In terminal, run:
npm run dev

Then open browser:
http://localhost:3000

You should see the checklist appear!
```

---

# STEP 4: PUSH CODE TO GITHUB (10 minutes)

### Initialize Git:
```
cd webinar-checklist-app
git init
git add .
git commit -m "Initial commit - webinar checklist app"
```

### Create GitHub Repository:
1. Go to **https://github.com/new**
2. Name: `webinar-checklist-app`
3. Description: "Webinar team checklist for Sabhi Digital"
4. Click **"Create repository"**
5. Copy the commands GitHub shows you
6. Paste them in terminal:
   ```
   git remote add origin https://github.com/YOUR_USERNAME/webinar-checklist-app.git
   git branch -M main
   git push -u origin main
   ```
7. Done ✓

---

# STEP 5: DEPLOY TO VERCEL (5 minutes)

### Connect Vercel to GitHub:

1. Go to **https://vercel.com**
2. Click **"Sign Up"**
3. Select **"Continue with GitHub"**
4. Authorize Vercel (allows it to access your GitHub)
5. After login, click **"New Project"**
6. Find and select: `webinar-checklist-app`
7. Click **"Import"**
8. Settings page appears:
   - Project name: `webinar-checklist-app`
   - Framework: Next.js (auto-selected)
   - Click **"Deploy"**
9. Wait 2-3 minutes for build
10. You'll see a URL like: `https://webinar-checklist-app.vercel.app`
11. Done ✓

### That's Your Live App!
- Share the URL with Pawan & Yuvraj
- They can open it on any browser
- It's live on the internet

---

# WHAT HAPPENS NEXT?

### When You Push Code Changes:
```
Local (Your Computer)  →  GitHub  →  Vercel (Auto-deploys)
```

1. Make changes locally
2. Run: `git add . && git commit -m "your message" && git push`
3. Vercel auto-deploys in ~1 minute
4. Your live app updates

---

# WHAT YOU'LL HAVE

✅ **Live Webinar Checklist App at:** https://webinar-checklist-app.vercel.app  
✅ **Team can access from any device** (phone, laptop)  
✅ **Mark steps ✓ and see timestamps auto-fill**  
✅ **Shows who completed each step**  
✅ **Data stored locally in browser** (or we can connect to database later)

---

# TOOLS YOU NEED (All Free)

| Tool | What It Does | Download Link |
|---|---|---|
| **Node.js** | Runs JavaScript on your computer | https://nodejs.org |
| **VS Code** | Code editor (optional) | https://code.visualstudio.com |
| **GitHub** | Store code online | https://github.com |
| **Vercel** | Deploy app live | https://vercel.com |
| **Git** | Version control (comes with Node.js) | Built-in |

---

# TROUBLESHOOTING

### "Command not found: npx"
- **Fix:** Node.js not installed. Download from nodejs.org

### "Cannot find module"
- **Fix:** Run `npm install` in terminal

### "Vercel deploy fails"
- **Fix:** Check GitHub → Settings → Vercel has permission to read repo

### "App shows blank page"
- **Fix:** Check browser console (F12) for errors

---

# NEXT: THE CODE

Once you understand this setup, I'll give you:

1. **`app/page.tsx`** — Main page
2. **`components/Checklist.tsx`** — Checklist logic
3. **`lib/data.ts`** — Sample data
4. **`.env.local`** — Any env variables (if needed)

Ready? I'll provide the code next.
