# Vercel Deployment Guide
## Smile Bright Bago - Step by Step

---

## 🚀 Step-by-Step Instructions

### Step 1: Go to Vercel
1. Open browser: **https://vercel.com**
2. Click **"Log in"** (if needed)

---

### Step 2: Create New Project
1. Click **"Add New..."** button (top right corner)
2. Select **"Project"**

---

### Step 3: Import Repository
1. Look for **`smile-bright-bago`** in the list
2. Click **"Import"** button next to it

**If you don't see it:**
- Click "Adjust GitHub App Permissions"
- Grant Vercel access to your repositories
- Refresh the page

---

### Step 4: Configure Project Settings

**Leave these as default:**
- ✅ Project Name: `smile-bright-bago`
- ✅ Framework Preset: Other
- ✅ Root Directory: `./`
- ✅ Build Command: (empty)
- ✅ Output Directory: (empty)
- ✅ Install Command: (empty)

---

### Step 5: Add Environment Variables ⚠️ IMPORTANT!

Click **"Environment Variables"** to expand the section.

You need to add **2 variables**:

#### Variable 1: SUPABASE_URL
```
Name: SUPABASE_URL
Value: [Get from Supabase dashboard - see below]
```

#### Variable 2: SUPABASE_ANON_KEY
```
Name: SUPABASE_ANON_KEY
Value: [Get from Supabase dashboard - see below]
```

---

## 🔑 How to Get Supabase Credentials

### Option 1: From Wheels of Love Vercel
1. Go to: **https://vercel.com**
2. Click on **"wheels-of-love"** project
3. Click **"Settings"** tab
4. Click **"Environment Variables"** in left sidebar
5. You'll see:
   - `SUPABASE_URL`
   - `SUPABASE_ANON_KEY`
6. Click the eye icon to reveal values
7. Copy and paste them to Smile Bright Bago

### Option 2: From Supabase Dashboard
1. Go to: **https://supabase.com**
2. Click on your project
3. Click **"Settings"** (gear icon, bottom left)
4. Click **"API"** in the left menu
5. You'll see:
   - **Project URL** → This is your `SUPABASE_URL`
   - **anon public** key → This is your `SUPABASE_ANON_KEY`
6. Copy these values

---

## 📋 Environment Variables Checklist

Before clicking Deploy, make sure:

- [ ] `SUPABASE_URL` is added
- [ ] `SUPABASE_ANON_KEY` is added
- [ ] Both values are correct (no extra spaces)
- [ ] Values are the SAME as Wheels of Love and Heart Warriors

**These MUST be the same credentials for all 3 sites!**

---

### Step 6: Deploy!

1. Click **"Deploy"** button
2. Wait 1-2 minutes for deployment
3. You'll see a success screen with your URL!

---

## ✅ After Deployment

### Your site will be live at:
```
https://smile-bright-bago.vercel.app
```

### Test the deployment:
1. Visit the URL
2. Check if the site loads
3. Try logging into admin panel (same credentials as Wheels of Love)
4. Upload a test image to gallery
5. Verify it only shows in Smile Bright (not in other sites)

---

## 🎯 Quick Reference

### Environment Variables Needed:
```
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

### Where to get them:
- **Vercel:** wheels-of-love project → Settings → Environment Variables
- **Supabase:** Dashboard → Settings → API

### Important Notes:
- ✅ Use SAME credentials as Wheels of Love
- ✅ Use SAME credentials as Heart Warriors
- ✅ All 3 sites share one database
- ✅ Data is separated by `program` column

---

## 🚨 Common Issues

### Issue 1: "Environment variables not set"
**Solution:** Make sure you added both `SUPABASE_URL` and `SUPABASE_ANON_KEY`

### Issue 2: "Cannot connect to database"
**Solution:** Check that the values are correct (no extra spaces or quotes)

### Issue 3: "Site shows Wheels of Love content"
**Solution:** You need to update the `program` value in the code (see SETUP_GUIDE.md)

### Issue 4: "Admin login doesn't work"
**Solution:** Use the same credentials as Wheels of Love admin

---

## 📞 Next Steps After Deployment

1. **Update Program Identifier**
   - Change `'wheels-of-love'` to `'smile-bright-bago'` in all JS files
   - See SETUP_GUIDE.md for details

2. **Update Branding**
   - Change colors to dental theme (blue/teal)
   - Update logo and cover images
   - Update all text content

3. **Test Everything**
   - Admin login
   - Upload content
   - Check mobile responsiveness
   - Verify data isolation

4. **Update Sister Sites**
   - Add Smile Bright logo to Heart Warriors
   - Add Smile Bright logo to Wheels of Love
   - Add navigation links

---

## ✅ Deployment Checklist

- [ ] Logged into Vercel
- [ ] Created new project
- [ ] Imported smile-bright-bago from GitHub
- [ ] Added SUPABASE_URL environment variable
- [ ] Added SUPABASE_ANON_KEY environment variable
- [ ] Clicked Deploy
- [ ] Deployment successful
- [ ] Site is live
- [ ] Tested admin login
- [ ] Ready to customize!

---

## 🎉 You're Done!

Once deployed, you'll have:
- ✅ Smile Bright Bago live on Vercel
- ✅ Connected to Supabase database
- ✅ Same admin credentials as other sites
- ✅ Ready to customize and add content

**Total time: 5-10 minutes**
**Total cost: $0/month**

---

**Need help?** Just ask! 😊
