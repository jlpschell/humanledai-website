# VERCEL-DEPLOY.md - Deploy Your Site to Vercel

This guide walks you through deploying your Human Led AI website to Vercel after building it in Antigravity IDE.

---

## Overview

**What we're doing:**
1. Export your site code from Antigravity
2. Push it to GitHub (free storage for code)
3. Connect GitHub to Vercel (free hosting)
4. Connect your domain (humanledai.net)

**Total cost:** $0 (using free tiers)
**Time needed:** About 30 minutes first time, 5 minutes for future updates

---

## Step 1: Create Accounts (One-Time Setup)

### GitHub Account
1. Go to https://github.com
2. Click "Sign Up"
3. Use your email, create username and password
4. Verify your email

### Vercel Account
1. Go to https://vercel.com
2. Click "Sign Up"
3. Choose "Continue with GitHub" (easiest - links them automatically)
4. Authorize Vercel to access your GitHub

---

## Step 2: Export from Antigravity

*Note: These steps may vary slightly depending on Antigravity's current interface.*

### Option A: If Antigravity has GitHub integration
1. In Antigravity, look for "Deploy" or "Export" button
2. Choose "Push to GitHub"
3. Name your repository: `humanledai-website`
4. Click confirm

### Option B: If you need to download and upload manually
1. In Antigravity, find "Export" or "Download Code"
2. Download the ZIP file to your computer
3. Extract the ZIP file
4. Continue to Step 3 (manual upload)

---

## Step 3: Get Code into GitHub

### If Antigravity pushed directly (Option A above):
- Skip to Step 4, your code is already in GitHub

### If you downloaded a ZIP (Option B above):

**Using GitHub.com (no terminal needed):**

1. Go to https://github.com
2. Click the "+" icon in top right → "New repository"
3. Name it: `humanledai-website`
4. Keep it Public (free)
5. Click "Create repository"
6. On the next page, click "uploading an existing file"
7. Drag all the files from your extracted folder into the browser
8. Click "Commit changes"

---

## Step 4: Connect to Vercel

1. Go to https://vercel.com/dashboard
2. Click "Add New..." → "Project"
3. You'll see your GitHub repositories listed
4. Find `humanledai-website` and click "Import"
5. Vercel auto-detects your framework (Astro, React, etc.)
6. Click "Deploy"
7. Wait 1-2 minutes for build to complete

**You now have a live site!** Vercel gives you a URL like:
`humanledai-website.vercel.app`

---

## Step 5: Connect Your Domain (humanledai.net)

### In Vercel:
1. Go to your project dashboard in Vercel
2. Click "Settings" tab
3. Click "Domains" in the left sidebar
4. Type `humanledai.net` and click "Add"
5. Vercel shows you DNS records to add

### In Your Domain Registrar:
*Where you bought humanledai.net (GoDaddy, Namecheap, Google Domains, etc.)*

1. Log into your domain registrar
2. Find DNS settings or "Manage DNS"
3. Add the records Vercel tells you to add:

**Usually these two:**
| Type | Name | Value |
|------|------|-------|
| A | @ | 76.76.21.21 |
| CNAME | www | cname.vercel-dns.com |

4. Save changes
5. Wait 10 minutes to 24 hours for DNS to update (usually under 1 hour)

### Verify in Vercel:
1. Go back to Vercel → Settings → Domains
2. Click "Refresh" next to your domain
3. When it shows green checkmark, you're live!

---

## Step 6: Enable HTTPS (Automatic)

Vercel automatically provides free HTTPS (the secure padlock icon).

Once your domain is connected, it sets this up automatically. No action needed.

---

## Future Updates (After Initial Setup)

Once everything is connected, updating your site is simple:

### If Antigravity is connected to GitHub:
1. Make changes in Antigravity
2. Push to GitHub
3. Vercel automatically rebuilds and deploys (within 1-2 minutes)

### If updating manually:
1. Download new code from Antigravity
2. Go to your GitHub repository
3. Upload changed files
4. Vercel automatically rebuilds

---

## Troubleshooting

### "Build failed" in Vercel
- Check the build logs (Vercel shows them)
- Usually a missing file or wrong framework detected
- Ask Claude Code to help diagnose

### Domain not working
- DNS changes can take up to 24 hours
- Make sure you added the records exactly as Vercel specified
- Check for typos in the DNS records

### Site looks wrong after deploy
- Clear your browser cache (Ctrl+Shift+R)
- Check if all files were uploaded
- Compare local version to live version

---

## Quick Reference Commands

If you ever need to use terminal (Claude Code), here are the key commands:

```bash
# Install Vercel CLI (one time)
npm install -g vercel

# Deploy from terminal
vercel

# Deploy to production
vercel --prod

# Check deployment status
vercel ls
```

---

## Summary Checklist

| Step | Status |
|------|--------|
| GitHub account created | ☐ |
| Vercel account created | ☐ |
| Site code exported from Antigravity | ☐ |
| Code uploaded to GitHub | ☐ |
| GitHub repo connected to Vercel | ☐ |
| First deploy successful | ☐ |
| Custom domain added in Vercel | ☐ |
| DNS records added at registrar | ☐ |
| Domain verified and live | ☐ |
| HTTPS working (padlock icon) | ☐ |

---

## You're Done!

Your site is now:
- ✅ Hosted professionally on Vercel
- ✅ Available at humanledai.net
- ✅ Secure with HTTPS
- ✅ Fast for visitors everywhere
- ✅ Easy to update in the future

**Future Jay appreciates you setting this up right.**
