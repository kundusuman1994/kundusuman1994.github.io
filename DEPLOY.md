# How to deploy your site on GitHub Pages

## Step 1 — Customize your content

Open `index.html` in any text editor and replace all placeholder text:

| Placeholder | Replace with |
|---|---|
| `Your Name` | Suman Kundu |
| `[Your Institute]` | SISSA, Trieste |
| `[Your PhD Institution]` | TIFR, Mumbai |
| `you@institution.edu` | sukundu@sissa.it |
| Research card text | High Energy Theory |
| Publication entries | Your real papers |
| Code cards | Your GitHub repositories |

**Add your photo:**
1. Save your photo as `photo.jpg` in the same folder as `index.html`
2. Find the comment `<!-- Replace the block below with... -->`
3. Replace the entire `<div class="photo-placeholder">...</div>` block with:
   ```html
   <img src="photo.jpg" alt="Your Name">
   ```

**Add your CV PDF:**
1. Export your CV as `cv.pdf`
2. Place it in the same folder as `index.html`
3. The "Download CV" button will work automatically

---

## Step 2 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **"New repository"** (the green button)
3. Name it exactly: `yourusername.github.io`
   - Replace `yourusername` with your actual GitHub username
   - This is **important** — GitHub uses this naming convention for personal sites
4. Set it to **Public**
5. Click **"Create repository"**

---

## Step 3 — Upload your files

**Option A: Upload via browser (easiest)**
1. In your new repository, click **"Add file" → "Upload files"**
2. Drag and drop: `index.html`, `photo.jpg`, `cv.pdf`
3. Click **"Commit changes"**

**Option B: Via command line**
```bash
git init
git add index.html photo.jpg cv.pdf
git commit -m "Initial site"
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

---

## Step 4 — Enable GitHub Pages

1. In your repository, go to **Settings** → **Pages** (left sidebar)
2. Under "Source", select **"Deploy from a branch"**
3. Choose branch: **main**, folder: **/ (root)**
4. Click **Save**

Your site will be live at `https://yourusername.github.io` within 1–2 minutes.

---

## Step 5 — (Optional) Custom domain

If you have a domain like `yourname.com`:
1. In **Settings → Pages**, enter your domain under "Custom domain"
2. At your domain registrar, add a CNAME record pointing to `yourusername.github.io`

---

## Updating your site later

Just upload new versions of `index.html` (or push via git) — GitHub Pages rebuilds automatically within seconds.

---

## File structure

```
yourusername.github.io/
├── index.html    ← your website
├── photo.jpg     ← your profile photo
└── cv.pdf        ← your CV
```

That's it — no frameworks, no build tools, no dependencies. Pure HTML.
