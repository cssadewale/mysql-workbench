# Deployment Guide

This application is a static web app. It has no backend server, no paid database, and no AI API. The easiest free deployment options are GitHub Pages, Cloudflare Pages, and Netlify.

---

## Before Deployment

Confirm that your folder contains:

```text
index.html
README.md
DEPLOYMENT.md
CONTRIBUTING.md
CHANGELOG.md
LICENSE
SECURITY.md
PRIVACY.md
docs/
.github/workflows/static-check.yml
.gitignore
.nojekyll
```

Open `index.html` locally first. The SQL engine is loaded from the free jsDelivr/CDNJS-style CDN link in the file. Internet access is required for that hosted engine unless you later vendor `sql.js` files locally.

---

## Option 1: GitHub Pages

### A. Create the repository
1. Sign in to GitHub.
2. Click **New repository**.
3. Enter a repository name, for example `mysql-workbench-stimulator-enterprise`.
4. Set visibility to **Public** if you want free GitHub Pages on a public project.
5. Click **Create repository**.

### B. Upload the files
1. Open the new repository.
2. Click **Add file > Upload files**.
3. Drag all files and folders from the `enterprise` folder into GitHub.
4. Commit to the `main` branch.

### C. Enable GitHub Pages
1. Go to **Settings**.
2. Click **Pages** in the left menu.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Set **Branch** to `main` and folder to `/root`.
5. Click **Save**.
6. Wait 1–5 minutes.
7. Visit the generated URL:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY-NAME/
```

### D. Verify
1. The page should load.
2. The top-right status should show **Online (local WebAssembly)**.
3. Run:

```sql
SELECT department, COUNT(*) AS staff_count
FROM employees
GROUP BY department;
```

---

## Option 2: Cloudflare Pages

1. Push the `enterprise` folder contents to GitHub.
2. Sign in to Cloudflare.
3. Go to **Workers & Pages > Pages > Connect to Git**.
4. Select the repository.
5. Use these settings:
   - Framework preset: **None**
   - Build command: leave empty
   - Build output directory: `/` or leave default for static root
6. Click **Save and Deploy**.
7. Open the provided `*.pages.dev` URL.

---

## Option 3: Netlify Free

1. Sign in to Netlify.
2. Go to **Sites > Add new site > Deploy manually**.
3. Drag the contents of the `enterprise` folder into the deployment area.
4. Netlify will provide a free URL.
5. Optionally rename the site under **Site settings**.

---

## Option 4: Offline / Local Use

1. Copy the `enterprise` folder to your computer or Android device.
2. Open `index.html` in a modern browser.
3. If the SQL engine does not load, connect to the internet once so the CDN file can load.
4. For a fully offline production copy, download and vendor `sql-wasm.js` and `sql-wasm.wasm`, update the script path and `locateFile` path in `index.html`, and commit those files to the repository if their license requirements are met.

---

## Updating the Live Site

1. Edit files locally.
2. Test by opening `index.html`.
3. Commit and push changes to GitHub.
4. GitHub Pages / Cloudflare Pages redeploys automatically.

---

## Security and Privacy Checklist

- Do not commit real sensitive datasets.
- Use exported `.sqlite` files as private backups, not public repository files.
- Review `SECURITY.md` and `PRIVACY.md` before publishing for a school or organization.
- If used by multiple people, each user has a separate local browser database and audit trail.
