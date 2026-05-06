# GitHub & Vercel Setup Guide
## Smile Bright Bago - Quick Reference

---

## ✅ Step 1: Create GitHub Repository

1. Go to: **https://github.com**
2. Click: **"+" icon** (top right) → **"New repository"**
3. Fill in:
   - **Repository name:** `smile-bright-bago`
   - **Description:** `Smile Bright Bago - Dental Health Program Website`
   - **Visibility:** Public
   - ❌ **DO NOT** check "Initialize with README"
4. Click: **"Create repository"**

---

## ✅ Step 2: Push Code to GitHub

After creating the repository, GitHub will show you commands. Use these:

```bash
# Add all files
git add .

# Create first commit
git commit -m "Initial commit: Smile Bright Bago website"

# Add remote (replace YOUR-USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR-USERNAME/smile-bright-bago.git

# Push to GitHub
git branch -M master
git push -u origin master
```

### Copy-Paste Commands (PowerShell):
```powershell
cd "c:\Users\OJTBEEG\Desktop\smile bright bago\smile-bright-bago"
git add .
git commit -m "Initial commit: Smile Bright Bago website"
git remote add origin https://github.com/YOUR-USERNAME/smile-bright-bago.git
git branch -M master
git push -u origin master
```

**Note:** Replace `YOUR-USERNAME` with your actual GitHub username!

---

## ✅ Step 3: Deploy to Vercel

1. Go to: **https://vercel.com**
2. Click: **"Add New"** → **"Project"**
3. Click: **"Import Git Repository"**
4. Select: **`smile-bright-bago`** from your GitHub repos
5. Click: **"Import"**

### Configure Project:

**Framework Preset:** Other (or leave as detected)

**Root Directory:** `./` (leave as is)

**Build Command:** Leave empty (static site)

**Output Directory:** Leave empty

### Environment Variables (IMPORTANT!):

Click **"Environment Variables"** and add these 2 variables:

```
Name: SUPABASE_URL
Value: [Copy from Wheels of Love .env file]

Name: SUPABASE_ANON_KEY
Value: [Copy from Wheels of Love .env file]
```

**Where to find these values:**
- Open: `c:\Users\OJTBEEG\Desktop\wheels of love\wheels-of-love\.env`
- Copy the values for `SUPABASE_URL` and `SUPABASE_ANON_KEY`

6. Click: **"Deploy"**

---

## 🎯 Complete Flow Diagram:

```
1. GitHub
   ├─ Create repository: smile-bright-bago
   └─ Copy the git remote URL

2. Local Computer
   ├─ git add .
   ├─ git commit -m "Initial commit"
   ├─ git remote add origin [URL]
   └─ git push

3. Vercel
   ├─ Import from GitHub
   ├─ Add environment variables (SUPABASE_URL, SUPABASE_ANON_KEY)
   └─ Deploy

4. Result
   └─ Live site: smile-bright-bago.vercel.app
```

---

## 📋 Checklist:

### GitHub:
- [ ] Created repository `smile-bright-bago`
- [ ] Copied git remote URL
- [ ] Pushed code successfully

### Vercel:
- [ ] Imported GitHub repository
- [ ] Added `SUPABASE_URL` environment variable
- [ ] Added `SUPABASE_ANON_KEY` environment variable
- [ ] Deployed successfully
- [ ] Site is live

### Testing:
- [ ] Visit your Vercel URL
- [ ] Check if site loads correctly
- [ ] Test admin login (same credentials as Wheels of Love)
- [ ] Upload a test image to gallery
- [ ] Verify it only shows in Smile Bright (not in other sites)

---

## 🔑 Important Notes:

### Same Credentials:
✅ Use the **SAME** Supabase credentials as Wheels of Love and Heart Warriors
✅ All 3 sites share the same database
✅ Data is separated by the `program` column

### Environment Variables:
```
SUPABASE_URL = https://your-project.supabase.co
SUPABASE_ANON_KEY = eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

### Deployment URL:
After deployment, your site will be at:
```
https://smile-bright-bago.vercel.app
```

Or a custom domain if you set one up.

---

## 🚨 Common Issues:

### Issue 1: "Permission denied" when pushing
**Solution:** Make sure you're logged into GitHub in your terminal
```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

### Issue 2: "Repository not found"
**Solution:** Check the remote URL
```bash
git remote -v
# If wrong, remove and re-add:
git remote remove origin
git remote add origin https://github.com/YOUR-USERNAME/smile-bright-bago.git
```

### Issue 3: Vercel deployment fails
**Solution:** Check environment variables are set correctly

### Issue 4: Site shows Wheels of Love content
**Solution:** You need to update the `program` value in the code (see SETUP_GUIDE.md)

---

## 📞 Next Steps After Deployment:

1. **Update Program Identifier**
   - Change `'wheels-of-love'` to `'smile-bright-bago'` in all JS files
   - See SETUP_GUIDE.md for details

2. **Update Branding**
   - Change colors
   - Update logo
   - Update text content

3. **Test Everything**
   - Admin login
   - Upload content
   - Check mobile responsiveness

4. **Update Sister Sites**
   - Add Smile Bright logo to Heart Warriors
   - Add Smile Bright logo to Wheels of Love
   - Add navigation links

---

## ✅ You're Done!

Once deployed, you'll have:
- ✅ Smile Bright Bago on GitHub
- ✅ Smile Bright Bago live on Vercel
- ✅ Connected to same Supabase database
- ✅ Ready to customize and add content

**Total Cost: $0/month** 🎉
