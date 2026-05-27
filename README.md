# MySQL Workbench Stimulator Enterprise

A free, static, browser-based SQL workbench that gives learners, analysts, instructors, and small teams a MySQL Workbench-style experience without a backend server, paid database, or AI API.

**Developer:** Adewale Samson Adeagbo  
**Role focus:** Data Scientist | EdTech Builder | Virtual Tutor | AI-Augmented Solutions Developer

> The project deliberately does **not** use an AI API because API costs are not cost-effective for the intended use case. All SQL processing runs locally in the user's browser through free WebAssembly technology.

---

## What Is Included

- `index.html` — complete static application with HTML, CSS, and JavaScript.
- `README.md` — project overview and quick start.
- `DEPLOYMENT.md` — detailed deployment steps for free platforms.
- `CONTRIBUTING.md` — contribution rules and coding standards.
- `CHANGELOG.md` — release history.
- `LICENSE` — MIT license.
- `SECURITY.md` — responsible disclosure and data safety notes.
- `PRIVACY.md` — privacy behavior and local-storage explanation.
- `docs/FEATURES.md` — detailed explanation of every major feature.
- `docs/USER_GUIDE.md` — usage workflow for learners and teams.
- `docs/ARCHITECTURE.md` — technical architecture and free-tool decisions.
- `.github/workflows/static-check.yml` — free GitHub Actions validation workflow.
- `.gitignore` and `.nojekyll` — repository hygiene and GitHub Pages support.

---

## Enterprise-Enhanced Features

### 1. Local SQL Engine
Runs SQL in the browser using `sql.js` / SQLite WebAssembly. This means the application can be hosted as a static site and still execute real SQL commands.

### 2. Workbench-Style Interface
Includes management navigation, schema explorer, query tabs, SQL editor, result grid, console, performance dashboard, ERD panel, audit log, and documentation panel.

### 3. Data Import, Export, and Restore
Import CSV files into sanitized database tables, export the full database as `.sqlite`, restore `.sqlite` backups, and export query results as CSV.

### 4. Enterprise Governance Layer
The application includes a governance center, backup policy, privacy notice, local audit trail, lint warnings, and destructive-query reminders.

### 5. Performance and Explain Plan
Every query can be timed locally. The performance dashboard records query duration, row count, and SQL preview. Explain Plan helps users understand query execution behavior.

### 6. Learning and Productivity Tools
Includes sample datasets, SQL snippets, saved local queries, SQL formatter, SQL lint checker, keyboard shortcuts, visual table designer, auto charting, and ERD diagramming.

### 7. No AI API and No Backend
No OpenAI, Gemini, Claude, or any other AI API is called. No server database is required. This keeps operating cost at zero when deployed on free static hosting.

---

## Quick Start

1. Open `index.html` in a browser, or deploy the folder to GitHub Pages / Cloudflare Pages / Netlify.
2. Wait for the local SQL engine to load.
3. Run the default query:

```sql
SELECT * FROM employees LIMIT 10;
```

4. Explore sample datasets, CSV import, ERD diagram, performance dashboard, and audit log.

---

## Free Tech Stack

- HTML5, CSS3, and vanilla JavaScript
- `sql.js` SQLite WebAssembly engine from a free CDN
- Browser LocalStorage for tabs, saved queries, settings, performance, and audit trail
- Canvas API for built-in charts and ERD rendering
- GitHub Pages, Cloudflare Pages, or Netlify free tier for deployment

---

## Important Limitation

This is a client-side learning and analysis tool. It is not a replacement for a secured production database server. Do not upload private student, customer, payroll, medical, or regulated data to public repositories.
