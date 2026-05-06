# Smile Bright Bago - Setup Guide
## Converting from Wheels of Love Template

**Date:** May 6, 2026  
**Program:** Smile Bright Bago (Dental Health Program)  
**Status:** 🚧 Setup in Progress

---

## ✅ What's Been Done

1. ✅ Project structure copied from Wheels of Love
2. ✅ All files and folders created
3. ✅ Ready for customization

---

## 📋 Setup Checklist

### Step 1: Update Environment Variables
- [ ] Open `.env` file
- [ ] Keep the same Supabase credentials (shared database)
- [ ] No changes needed - same credentials work for all 3 sites!

### Step 2: Update Program Identifier
You need to change the `program` value in all API calls from `wheels-of-love` to `smile-bright-bago`

**Files to update:**
- [ ] `assets/js/main.js` - Change program value
- [ ] `admin/assets/js/dashboard.js` - Change program value
- [ ] `admin/assets/js/gallery.js` - Change program value
- [ ] `admin/assets/js/posts.js` - Change program value
- [ ] `api/gallery.js` - Change program filter
- [ ] `api/posts.js` - Change program filter
- [ ] `api/stats.js` - Change program filter

**Search and Replace:**
- Find: `'wheels-of-love'` or `"wheels-of-love"`
- Replace with: `'smile-bright-bago'` or `"smile-bright-bago"`

### Step 3: Update Branding & Content

#### A. Colors (CSS Variables)
Edit `assets/css/main.css` - Change color scheme:

**Current (Wheels of Love - Orange):**
```css
--red-main: #e05c00;
--red-dark: #c74e00;
--red-pale: #fff5ed;
```

**Suggested (Smile Bright - Blue/Teal for Dental):**
```css
--red-main: #00a8e8;  /* Bright blue */
--red-dark: #0077b6;  /* Dark blue */
--red-pale: #e6f7ff;  /* Light blue */
```

Or use dental-themed colors:
```css
--red-main: #4ecdc4;  /* Teal/mint */
--red-dark: #2a9d8f;  /* Dark teal */
--red-pale: #e8f8f7;  /* Light mint */
```

#### B. Logo & Images
- [ ] Copy `14 Smile Bright BAGO.png` to `assets/images/logo.png`
- [ ] Copy `smile bright cover.png` to `assets/images/cover.png`
- [ ] Delete old Wheels of Love images:
  - `assets/images/Wheels of LOVE - Wheelchairs of Hope.png`
  - `assets/images/wol-logo.png`
  - `assets/images/wol-logo.webp`

#### C. Text Content
Update these files with Smile Bright Bago content:

**`index.html`:**
- [ ] Line 7: Meta description
- [ ] Line 8-9: OG tags
- [ ] Line 10: Page title
- [ ] Line 13: Favicon (already updated with logo.png)
- [ ] Line 24-25: Topbar text
- [ ] Line 36: Email address
- [ ] Line 48: Brand name "❤️ Smile Bright Bago"
- [ ] Line 49: Tagline "LGU Bago City Program"
- [ ] Line 71-77: Sister site links (Heart Warriors & Wheels of Love)
- [ ] Line 95: Hero badge
- [ ] Line 96-98: Hero title
- [ ] Line 99-102: Hero description
- [ ] Line 104-108: Hero buttons
- [ ] Line 110-122: Hero stats
- [ ] Line 133-155: Hero slides content

**Key Content to Change:**
```html
<!-- FROM (Wheels of Love): -->
<div class="brand-name">❤️ Wheels of Love</div>
<div class="brand-sub">LGU Bago City Program</div>

<!-- TO (Smile Bright Bago): -->
<div class="brand-name">😁 Smile Bright Bago</div>
<div class="brand-sub">Dental Health Program</div>
```

```html
<!-- Hero Description FROM: -->
Wheels of Love is Bago City's dedicated program for persons with 
disabilities (PWDs) — providing free wheelchairs, mobility assistance...

<!-- Hero Description TO: -->
Smile Bright Bago is Bago City's dental health program — providing 
free dental check-ups, treatments, and oral health education to all residents...
```

#### D. Update All HTML Pages
- [ ] `about.html` - Update content about the dental program
- [ ] `contact.html` - Update email to `smilebright@bago.gov.ph`
- [ ] `events.html` - Keep structure, content will be added via admin
- [ ] `gallery.html` - Keep structure, content will be added via admin
- [ ] `news.html` - Keep structure, content will be added via admin
- [ ] `404.html` - Update branding

#### E. Update Manifest & Meta Files
**`manifest.json`:**
```json
{
  "name": "Smile Bright Bago",
  "short_name": "Smile Bright",
  "description": "Official Dental Health Program of Bago City LGU",
  "theme_color": "#00a8e8",
  "background_color": "#ffffff",
  "icons": [
    {
      "src": "assets/images/logo.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

**`README.md`:**
- [ ] Update title to "Smile Bright Bago"
- [ ] Update description
- [ ] Update deployment URL

### Step 4: Update Sister Site Links

All 3 sites should link to each other:

**In `index.html` navigation (around line 71):**
```html
<!-- Add both sister sites -->
<li class="nav-sister-site">
  <a href="https://heart-warriors.vercel.app" target="_blank" rel="noopener">
    <img src="assets/images/hw-logo.png" alt="Heart Warriors">
    <span>Heart Warriors</span>
  </a>
</li>
<li class="nav-sister-site">
  <a href="https://wheels-of-love.vercel.app" target="_blank" rel="noopener">
    <img src="assets/images/wol-logo.png" alt="Wheels of Love">
    <span>Wheels of Love</span>
  </a>
</li>
```

**You'll need to:**
- [ ] Get Heart Warriors logo (`hw-logo.png`) from Heart Warriors project
- [ ] Get Wheels of Love logo (`wol-logo.png`) from Wheels of Love project
- [ ] Copy them to `assets/images/`

### Step 5: Clean Up Git History
- [ ] Delete `.git` folder (to start fresh)
- [ ] Initialize new git repository
- [ ] Create first commit

```bash
cd "c:\Users\OJTBEEG\Desktop\smile bright bago\smile-bright-bago"
Remove-Item -Recurse -Force .git
git init
git add .
git commit -m "Initial commit: Smile Bright Bago website"
```

### Step 6: Create GitHub Repository
- [ ] Go to GitHub.com
- [ ] Create new repository: `smile-bright-bago`
- [ ] Push your code:

```bash
git remote add origin https://github.com/YOUR-USERNAME/smile-bright-bago.git
git branch -M master
git push -u origin master
```

### Step 7: Deploy to Vercel
- [ ] Go to vercel.com
- [ ] Click "New Project"
- [ ] Import from GitHub: `smile-bright-bago`
- [ ] Add environment variables (same as Wheels of Love):
  - `SUPABASE_URL`
  - `SUPABASE_ANON_KEY`
- [ ] Deploy!

### Step 8: Update Other Sites
After Smile Bright is deployed, update the other 2 sites to link to it:

**Heart Warriors & Wheels of Love:**
- [ ] Add Smile Bright logo to their `assets/images/`
- [ ] Add navigation link to Smile Bright
- [ ] Commit and push

---

## 🎨 Branding Guidelines

### Smile Bright Bago Identity

**Program Focus:** Dental Health & Oral Care

**Target Audience:**
- All Bago City residents
- Children (school dental programs)
- Seniors (denture services)
- Low-income families

**Services:**
- Free dental check-ups
- Tooth extractions
- Dental fillings
- Oral health education
- School dental missions
- Denture services for seniors

**Color Palette:**
- Primary: Bright Blue (#00a8e8) - Trust, cleanliness
- Secondary: Teal/Mint (#4ecdc4) - Fresh, healthy
- Accent: White (#ffffff) - Clean, dental

**Emojis to Use:**
- 😁 Smile/Happy face
- 🦷 Tooth
- 🪥 Toothbrush
- ✨ Sparkle (for clean teeth)
- 💙 Blue heart

**Tone:**
- Friendly and approachable
- Educational but not preachy
- Encouraging good oral health habits
- Community-focused

---

## 📝 Content Suggestions

### Hero Section Stats:
- **5,000+** Patients Served
- **48** Barangays Covered
- **3** Years Active
- **10** Dental Professionals

### Services to Highlight:
1. **Free Check-ups** - Regular dental examinations for all
2. **Preventive Care** - Cleaning, fluoride treatments, sealants
3. **Restorative Services** - Fillings, extractions, root canals
4. **Denture Program** - Free dentures for qualified seniors
5. **School Missions** - Dental health education in schools
6. **Emergency Care** - Toothache relief and urgent treatments

### About Page Content:
- Mission: Promote oral health and provide accessible dental care
- Vision: A Bago City where every resident has a healthy smile
- History: When the program started, achievements
- Team: Dentists, dental hygienists, support staff

---

## 🔧 Technical Notes

### Database Setup
No database changes needed! The existing Supabase database already supports multiple programs via the `program` column.

**Your data will be isolated:**
- Smile Bright posts: `program = 'smile-bright-bago'`
- Wheels of Love posts: `program = 'wheels-of-love'`
- Heart Warriors posts: `program = 'heart-warriors'`

### API Endpoints
All API endpoints are already set up. Just change the `program` filter value.

### Admin Panel
The admin panel will work immediately after you update the `program` value. You can:
- Upload photos/videos to Smile Bright gallery
- Create news posts for Smile Bright
- Manage events
- View messages

---

## ✅ Final Checklist

Before going live:
- [ ] All "Wheels of Love" text replaced with "Smile Bright Bago"
- [ ] Colors updated to dental theme
- [ ] Logo and cover images updated
- [ ] Program identifier changed to `smile-bright-bago`
- [ ] Sister site links added (Heart Warriors & Wheels of Love)
- [ ] Contact email updated
- [ ] Meta tags and SEO updated
- [ ] Tested locally
- [ ] Pushed to GitHub
- [ ] Deployed to Vercel
- [ ] Environment variables added
- [ ] Test admin panel login
- [ ] Add initial content (1-2 posts, some gallery images)
- [ ] Test on mobile devices
- [ ] Share with team for feedback

---

## 🚀 Quick Commands

```bash
# Navigate to project
cd "c:\Users\OJTBEEG\Desktop\smile bright bago\smile-bright-bago"

# Test locally (if you have a local server)
# Option 1: Python
python -m http.server 8000

# Option 2: Node.js
npx serve

# Then open: http://localhost:8000

# Git commands
git status
git add .
git commit -m "Your message"
git push
```

---

## 📞 Need Help?

If you need assistance with any step, just ask! I can help you:
- Update specific files
- Change colors and branding
- Write content
- Set up deployment
- Troubleshoot issues

**Let's make Smile Bright Bago shine! 😁✨**
