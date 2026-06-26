# 🚀 Setup & Deployment Guide

## Overview

This guide walks through deploying the unified hybrid datacenters map to GitHub Pages. All files are self-contained in a single HTML file with no build process required.

---

## Prerequisites

- GitHub account (username: **DrMarioDeSean411-arch**)
- Git installed on Windows (Command Prompt or PowerShell)
- Personal Access Token (PAT) with `repo` scope
- One local folder to hold the project

---

## Step 1: Clone or Create the Repository

### Option A: Clone Existing Repository (If Already Created)

```bash
cd %USERPROFILE%\Desktop
git clone https://github.com/DrMarioDeSean411-arch/usa-datacenter-energy-map.git
cd usa-datacenter-energy-map
```

### Option B: Create New Repository from Scratch

1. **On GitHub.com:**
   - Create new repository: `usa-datacenter-energy-map`
   - Initialize with README.md
   - Add .gitignore (optional)

2. **On Windows Command Prompt:**
   ```bash
   cd %USERPROFILE%\Desktop
   git clone https://github.com/DrMarioDeSean411-arch/usa-datacenter-energy-map.git
   cd usa-datacenter-energy-map
   ```

---

## Step 2: Add Project Files

### Directory Structure

```
usa-datacenter-energy-map/
├── index_hybrid.html           (PRIMARY — Global + USA toggle)
├── index.html                  (USA only, v2.0)
├── index_global.html           (Global only)
├── README.md                   (Project overview)
├── SETUP.md                    (This file)
├── README_HYBRID_MAP.md        (Detailed methodology)
├── FORECAST_MODEL.md           (Prediction calculations)
├── HYBRID_UNIFIED_MAP.md       (Feature documentation)
├── GLOBAL_DATACENTERS.md       (Global facility list)
├── GLOBAL_VS_USA.md            (Comparison guide)
├── CLUSTERS_AND_STATES.md      (USA regional details)
├── CLUSTERS_SUMMARY.md         (USA quick reference)
├── facilities.geojson          (GPS coordinates)
├── energy_regional.csv         (Power timeseries)
└── .gitignore                  (Optional)
```

### Copy Files to Local Repo

```bash
# From Command Prompt, in usa-datacenter-energy-map/ folder:

# Copy the HTML files (from wherever you saved them)
copy C:\Users\YourUsername\Downloads\index_hybrid.html .
copy C:\Users\YourUsername\Downloads\index.html .
copy C:\Users\YourUsername\Downloads\index_global.html .

# Copy documentation files
copy C:\Users\YourUsername\Downloads\README_HYBRID_MAP.md .
copy C:\Users\YourUsername\Downloads\FORECAST_MODEL.md .
copy C:\Users\YourUsername\Downloads\HYBRID_UNIFIED_MAP.md .
copy C:\Users\YourUsername\Downloads\GLOBAL_DATACENTERS.md .
copy C:\Users\YourUsername\Downloads\GLOBAL_VS_USA.md .
copy C:\Users\YourUsername\Downloads\CLUSTERS_AND_STATES.md .
copy C:\Users\YourUsername\Downloads\CLUSTERS_SUMMARY.md .
copy C:\Users\YourUsername\Downloads\facilities.geojson .
copy C:\Users\YourUsername\Downloads\energy_regional.csv .

# Verify files are in place
dir
```

**Expected Output:**
```
index_hybrid.html
index.html
index_global.html
README.md
SETUP.md
README_HYBRID_MAP.md
FORECAST_MODEL.md
[other docs...]
```

---

## Step 3: Configure Git User (First Time Only)

```bash
# Set your Git identity (one time per machine)
git config --global user.name "Dr. Mario DeSean"
git config --global user.email "mario.booker@wgu.edu"

# Verify
git config --global user.name
git config --global user.email
```

---

## Step 4: Stage and Commit Files

```bash
# Check status
git status

# Stage all files
git add .

# Verify staging
git status

# Commit with descriptive message
git commit -m "Add unified hybrid datacenters map: global + USA views, 50-year projections (2024-2074)"

# Check log
git log --oneline
```

**Example Commit Message:**
```
Unified hybrid datacenters map: 45+ facilities, global + USA detail view, 
50-year projections (2024-2074), 7.5% CAGR existing + 2.5x growth predicted, 
corrected duplicate marker offsets and energy growth calculations
```

---

## Step 5: Push to GitHub

### Using Personal Access Token (Recommended)

```bash
# Push to GitHub using HTTPS + PAT
git push -u origin main
```

**When prompted for credentials:**
- **Username**: DrMarioDeSean411-arch
- **Password**: [Paste your Personal Access Token here]
  - (If clipboard doesn't work: right-click → Paste)

**Expected Output:**
```
Enumerating objects: 42, done.
Counting objects: 100% (42/42), done.
Delta compression using up to 8 threads
Compressing objects: 100%
Writing objects: 100%
remote: Resolving deltas: 100%
To https://github.com/DrMarioDeSean411-arch/usa-datacenter-energy-map.git
 * [new branch]      main -> main
Branch 'main' set to track remote branch 'main' from 'origin'.
```

### Or: Using SSH (Alternative)

If you've set up SSH keys:

```bash
# Check if SSH is configured
ssh -T git@github.com

# If working, you can use:
git remote set-url origin git@github.com:DrMarioDeSean411-arch/usa-datacenter-energy-map.git
git push -u origin main
```

---

## Step 6: Enable GitHub Pages

1. **Go to GitHub.com → Repository Settings:**
   - https://github.com/DrMarioDeSean411-arch/usa-datacenter-energy-map/settings

2. **Navigate to "Pages" section (left sidebar)**

3. **Configure:**
   - **Source**: Branch `main`, Root folder `/`
   - **Custom Domain**: (Leave blank unless you have custom domain)
   - Click **Save**

4. **Wait 2-3 minutes** for GitHub to build and deploy

---

## Step 7: Verify Deployment

### Live URLs (Auto-generated by GitHub Pages)

Once deployed, access the maps at:

**Primary (Recommended):**
```
https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/index_hybrid.html
```

**Alternative Views:**
```
https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/index.html
https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/index_global.html
```

**Root redirect (if index.html in root):**
```
https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/
```

### Test the Map

1. **Open in browser**: Paste primary URL above
2. **Verify functionality:**
   - ✅ Map loads (satellite imagery visible)
   - ✅ Markers appear (colored circles for facilities)
   - ✅ Timeline slider responds (drag left/right)
   - ✅ Click a marker (popup shows facility details)
   - ✅ Toggle "🌍 Global" vs "🇺🇸 USA" view
   - ✅ Power/Water metrics update as you drag timeline

3. **Test on mobile:**
   - Open same URL on smartphone/tablet
   - Verify zoom/pan works
   - Verify popups are readable

---

## Step 8: Update Documentation

### Update README.md in Root

Edit `README.md` to point users to the interactive map:

```markdown
# Global Datacenters Intelligence Map

Interactive visualization of 45+ cloud infrastructure facilities worldwide with 
50-year energy & water projections (2024-2074).

## 🗺️ View the Map

**Live Map (Recommended):**
[Global + USA Hybrid View](https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/index_hybrid.html)

**Alternative Views:**
- [USA Detail Only](https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/index.html)
- [Global Only](https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/index_global.html)

## 📖 Documentation

See [README_HYBRID_MAP.md](./README_HYBRID_MAP.md) for detailed methodology and data sources.

## 🔧 Setup & Deployment

See [SETUP.md](./SETUP.md) for local development and deployment instructions.
```

---

## Step 9: Future Updates

### To Update the Map with New Data

```bash
# From command line, in usa-datacenter-energy-map/ folder:

# Edit files (e.g., add new facility to index_hybrid.html)
# Then:

git status                  # Check what changed
git add index_hybrid.html   # Stage changes
git commit -m "Add new datacenters to map: Tokyo expansion + Mumbai facility"
git push origin main        # Push to GitHub

# GitHub Pages auto-updates within 2-3 minutes
```

### Rollback to Previous Version

```bash
# View commit history
git log --oneline

# Rollback to a specific commit
git revert <commit-hash>
git push origin main
```

---

## Troubleshooting

### Problem: "fatal: not a git repository"

**Solution:**
```bash
# Make sure you're in the correct folder
cd %USERPROFILE%\Desktop\usa-datacenter-energy-map

# If folder doesn't exist, re-clone:
git clone https://github.com/DrMarioDeSean411-arch/usa-datacenter-energy-map.git
cd usa-datacenter-energy-map
```

### Problem: "Authentication failed for HTTPS push"

**Solution:**
```bash
# Use Personal Access Token, not GitHub password
# Generate new PAT: Settings → Developer Settings → Personal access tokens → Tokens (classic)
# Scopes needed: repo (full control of private repositories)

# When git asks for password, paste the PAT
git push origin main
```

### Problem: "Please tell me who you are" error

**Solution:**
```bash
git config --global user.name "Dr. Mario DeSean"
git config --global user.email "mario.booker@wgu.edu"
```

### Problem: Map shows blank / markers don't load

**Possible Causes:**
1. Browser cache not updated → Hard refresh (Ctrl+Shift+R)
2. CDN links not accessible → Check network tab (F12 → Network)
3. JavaScript error → Check console (F12 → Console)

**Solution:**
```bash
# Hard refresh in browser
Ctrl + Shift + R  (Windows/Linux)
Cmd + Shift + R   (Mac)
```

### Problem: GitHub Pages not updating after push

**Solution:**
1. Wait 2-3 minutes (GitHub Pages rebuilds)
2. Check Settings → Pages (verify "main" branch selected)
3. Check Actions tab for build errors
4. Force browser refresh (Ctrl+Shift+R)

---

## Local Testing (Optional)

### Run Locally Before Pushing

To test `index_hybrid.html` locally without uploading:

```bash
# Option 1: Open directly in browser
C:\path\to\index_hybrid.html

# Option 2: Start local web server (Python)
python -m http.server 8000
# Then open: http://localhost:8000/index_hybrid.html

# Option 3: Live Server (VS Code extension)
# Right-click → Open with Live Server
```

---

## GitHub Pages Limitations

### What Works ✅
- Static HTML/CSS/JavaScript
- No server-side code needed
- Free hosting (GitHub account required)
- Custom domain optional
- HTTPS automatic

### What Doesn't Work ❌
- Database connections
- Backend server code
- PHP/Python/Node.js execution
- File uploads

**This project:** ✅ Works perfectly (static HTML only)

---

## File Size & Performance

### Current Deployment

```
index_hybrid.html:  95 KB
index.html:         58 KB
index_global.html:  41 KB
Documentation:      ~150 KB
Total:              ~350 KB
```

**Load Time:** <2 seconds (typical)
**Bandwidth:** Negligible (static files, CDN cached)

---

## Academic Citation

For papers/presentations citing this work:

```bibtex
@misc{desean2026datacenters,
  author = {DeSean, Mario},
  title = {Global Datacenters Intelligence Map: 
           Unified visualization of 45+ cloud infrastructure facilities 
           with 50-year sustainability projections (2024-2074)},
  url = {https://github.com/DrMarioDeSean411-arch/usa-datacenter-energy-map},
  year = {2026},
  note = {GitHub Pages deployment}
}
```

---

## Support & Issues

### Report Issues
- GitHub Issues: https://github.com/DrMarioDeSean411-arch/usa-datacenter-energy-map/issues
- Email: mario.booker@wgu.edu

### Request Features
- Submit via GitHub Issues with label `enhancement`
- Describe new data, visualizations, or metrics

---

## Maintenance Schedule

| Task | Frequency | Owner |
|------|-----------|-------|
| Update facility data | Quarterly | Dr. DeSean |
| Revise projections | Annually | Dr. DeSean |
| Security patches | As needed | GitHub Dependabot |
| Documentation review | Bi-annually | Dr. DeSean |

---

## Success Checklist

- [ ] Repository created on GitHub
- [ ] Files copied to local folder
- [ ] Git configured (user.name, user.email)
- [ ] Files staged and committed
- [ ] Pushed to GitHub (`git push`)
- [ ] GitHub Pages enabled in Settings
- [ ] Map accessible at public URL
- [ ] All markers visible on map
- [ ] Timeline slider functional
- [ ] View toggle (Global/USA) working
- [ ] Documentation links working
- [ ] Shared link with colleagues/advisors

---

## Final Notes

1. **No build step required** — HTML is served directly
2. **All data embedded** — No external API calls
3. **Works offline** — Download HTML and open locally
4. **Mobile friendly** — Responsive design on all devices
5. **Browser support** — Works on any modern browser (Chrome, Firefox, Safari, Edge)

---

**Status:** ✅ Ready to deploy  
**Last Updated:** June 2026  
**Estimated Deployment Time:** 5-10 minutes total
