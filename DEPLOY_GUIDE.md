# How to Deploy to GitHub Pages — Step by Step

## First time setup (takes ~10 minutes)

### Step 1 — Create a GitHub account
Go to https://github.com and sign up if you don't have an account.

### Step 2 — Create a new repository
1. Click the **+** button (top right) → **New repository**
2. Name it: `[your-username].github.io`
   - Example: if your username is `ethanmac`, name it `ethanmac.github.io`
3. Set it to **Public**
4. Click **Create repository**

### Step 3 — Upload your files
On the repository page:
1. Click **uploading an existing file** (or drag and drop)
2. Upload ALL files from this folder:
   - `index.html` ← this is your website
   - `README.md`
   - `_config.yml`
   - `.gitignore`
   - `CNAME` (only if you have a custom domain)
3. Scroll down, click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repo → **Settings** tab
2. Scroll to **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Branch: **main**, Folder: **/ (root)**
5. Click **Save**

### Step 5 — View your live site
- Wait ~60 seconds
- Visit: `https://[your-username].github.io`
- That's it — your site is live!

---

## Making updates later

### Easy way (browser only):
1. Go to your GitHub repo
2. Click `index.html`
3. Click the pencil ✏️ icon to edit
4. Make your changes
5. Click **Commit changes**
6. Site updates automatically in ~60 seconds

### Power user way (with GitHub Desktop app):
1. Download GitHub Desktop: https://desktop.github.com
2. Clone your repo to your computer
3. Edit `index.html` in any text editor
4. In GitHub Desktop: write a commit message → **Commit** → **Push**

---

## Custom domain setup (optional)

If you own a domain like `ethanmaclelland.com`:

1. Edit the `CNAME` file — replace the comment with just your domain:
   ```
   ethanmaclelland.com
   ```
2. Log into your domain registrar (GoDaddy, Namecheap, etc.)
3. Add these DNS records:
   ```
   Type: A    Name: @    Value: 185.199.108.153
   Type: A    Name: @    Value: 185.199.109.153
   Type: A    Name: @    Value: 185.199.110.153
   Type: A    Name: @    Value: 185.199.111.153
   Type: CNAME  Name: www  Value: [your-username].github.io
   ```
4. In GitHub repo → Settings → Pages → enter your custom domain
5. Check **Enforce HTTPS**
6. DNS can take up to 24 hours to propagate

---

## Troubleshooting

**Site not showing up?**
- Make sure the repo is named exactly `[username].github.io`
- Make sure the file is named `index.html` (not `Index.html` or `homepage.html`)
- Give it a few minutes and hard refresh (Cmd+Shift+R / Ctrl+Shift+R)

**Changes not appearing?**
- GitHub Pages can take 1-2 minutes to rebuild
- Hard refresh your browser cache

**404 error?**
- Double-check Settings → Pages is enabled
- Make sure branch is set to `main`
