# ⚡ Quick Deploy Guide — CMC Portal to GitHub Pages

## What you need
- A free GitHub account → https://github.com/signup
- The 3 files in this folder: `index.html`, `README.md`, `.gitignore`

---

## 🖱️ Method 1: Upload via GitHub Website (easiest, no terminal)

1. **Create a new repo**
   - Go to https://github.com/new
   - Repository name: `cmc-portal`
   - Visibility: ✅ Public
   - Click **Create repository**

2. **Upload the files**
   - On the new repo page, click **"uploading an existing file"**
   - Drag all 3 files (`index.html`, `README.md`, `.gitignore`) into the upload box
   - Scroll down, click **Commit changes**

3. **Enable GitHub Pages**
   - Go to your repo → **Settings** (top tab)
   - Left sidebar → **Pages**
   - Under *Source*: select **Deploy from a branch**
   - Branch: **main** | Folder: **/ (root)**
   - Click **Save**

4. **Wait ~60 seconds**, then visit:
   ```
   https://<your-github-username>.github.io/cmc-portal/
   ```

---

## 💻 Method 2: Git Terminal

```bash
# Create the repo on GitHub first (step 1 above), then:

git clone https://github.com/YOUR_USERNAME/cmc-portal.git
cd cmc-portal

# Copy index.html, README.md, .gitignore into this folder, then:

git add .
git commit -m "🏛️ Initial CMC Portal deployment"
git push origin main
```

Then enable GitHub Pages (step 3 above).

---

## ✅ Checklist before going live

- [ ] Supabase project is created and schema SQL has been run
- [ ] `anon` role has table access (`grant all on all tables...`)
- [ ] The 3 hardcoded keys in `index.html` (line ~480) are correct
- [ ] Tested login with demo credentials locally (just open `index.html` in Chrome)
- [ ] GitHub Pages is enabled on the `main` branch

---

## 🔗 Your live URL will be:
```
https://<your-github-username>.github.io/cmc-portal/
```
