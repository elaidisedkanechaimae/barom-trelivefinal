# Baromètre Macro-Financier — KEDGE

## Deploy to Vercel (free, 3 minutes)

### Step 1 — Upload to GitHub
1. Create a new repo on github.com (e.g. `barometer-kedge`)
2. Upload all these files keeping the folder structure:
   ```
   vercel.json
   api/claude.js
   public/index.html
   ```

### Step 2 — Deploy on Vercel
1. Go to **vercel.com** → sign in with GitHub
2. Click **"Add New Project"** → import your repo
3. Click **Deploy** (no build settings needed)

### Step 3 — Add your Anthropic API key
1. In Vercel dashboard → your project → **Settings → Environment Variables**
2. Add:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** your key from console.anthropic.com
3. Click **Save** → go to **Deployments** → click **Redeploy**

### Done!
Vercel gives you a URL like `https://barometer-kedge.vercel.app`  
Share that link — the teacher just clicks it, everything works. ✅

## How it works
- `public/index.html` — the full dashboard (FR/EN, charts, Z-scores)
- `api/claude.js` — serverless proxy that adds your Anthropic key server-side
- FRED data: enter your free FRED key once in the app (stored in browser)
- Yahoo Finance: fetched via CORS proxies
