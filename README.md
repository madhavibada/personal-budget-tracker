# Personal Budget Tracker (Microsoft Excel)

Automated budget workbook to monitor income and expenses.

## What’s included

| File | Purpose |
|------|---------|
| `Personal_Budget_Tracker.xlsx` | Main workbook (open in Excel or Google Sheets) |

## Features

- **Transactions** — Income and expense entries.
- **Dashboard** — KPI-style summaries using **SUM**, **IF**, and **AVERAGE** (income, expenses, savings rate, category rollups).
- **Budget plan** — Planned vs actual and variance.
- **Charts** — Visuals for category-wise spending (e.g. bar and pie charts).

## Run locally

1. Clone or download this repository.
2. Open `Personal_Budget_Tracker.xlsx` in **Microsoft Excel** or **Google Sheets**. Formulas update when you edit data.

## Live preview on GitHub (browser)

After the code is on GitHub and **GitHub Pages** is enabled, open your Pages URL. The site embeds the workbook in **Excel for the web** via Microsoft’s viewer.

**Requirements:** The repository should be **public** so the viewer can load the raw `.xlsx` URL.

### Enable GitHub Pages

1. On GitHub: **Settings → Pages**.
2. **Build and deployment**: Source = **Deploy from a branch**.
3. Branch = **main**, folder = **/ (root)** → Save.
4. After the site builds, open: `https://madhavibada.github.io/personal-budget-tracker/`

If your default branch is not `main`, change the `branch` value in `index.html` (see the script at the bottom) to match.

---

## Push updates from Windows (Option A — **madhavibada** account)

GitHub does **not** accept your account password for Git over HTTPS. Use a **Personal Access Token (PAT)** as the password.

### 1. Create a token (signed in as **madhavibada**)

1. GitHub → profile → **Settings**.
2. **Developer settings** → **Personal access tokens**.
3. **Tokens (classic)** → **Generate new token (classic)** → name it → scope **`repo`** → **Generate** → **copy** the token (shown once).

### 2. Stop Windows from using the wrong GitHub user

If Git previously used another account (for example **divitisanthoshi**):

1. **Win** → search **Credential Manager** → open it.
2. **Windows Credentials**.
3. Remove entries like **`git:https://github.com`** (or other GitHub-related items).

### 3. Push from this folder

In **PowerShell**:

```powershell
cd "c:\Users\santh\OneDrive\Desktop\Personal_Budget_Tracker"
git add .
git commit -m "Your message"
git push -u origin main
```

When prompted:

- **Username:** `madhavibada`
- **Password:** paste the **PAT** (not your GitHub password).

### 4. Confirm

Open [https://github.com/madhavibada/personal-budget-tracker](https://github.com/madhavibada/personal-budget-tracker) and refresh — your files should appear.

**Security:** Do not commit the PAT or share it in chat or screenshots. If it leaks, revoke it under **Developer settings → Personal access tokens** and create a new one.

**If you don’t control the madhavibada account:** use collaborator write access on the repo, or push to a repository you own instead.

## License

Use and modify for personal or portfolio use.
