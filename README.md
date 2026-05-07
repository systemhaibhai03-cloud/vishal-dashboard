# Vishal Electricals — Outstanding Payment Dashboard

Live dashboard for tracking outstanding payments, site-wise breakups, debtor days, and deduction analysis.

## 🚀 Deployed on Vercel

Live URL will be: `https://vishal-dashboard.vercel.app` (or your custom domain)

## 📁 Files

```
vishal-dashboard/
├── index.html      ← Main dashboard (single file app)
├── vercel.json     ← Vercel deployment config
└── README.md       ← This file
```

## ⚙️ Configuration

Open `index.html` and edit the `CONFIG` block at the top:

```js
const CONFIG = {
  CSV_URL: 'YOUR_GOOGLE_SHEETS_CSV_URL',   // ← Paste your public CSV URL
  AUTO_REFRESH_MINUTES: 5,                  // ← Auto-refresh interval
  COMPANY: 'Vishal Electricals',
  AS_ON_DATE: '07 May 2026'
};
```

## 📊 Google Sheets Setup

To make dashboard pull live data:

1. Open your Google Sheet
2. Go to **File → Share → Publish to web**
3. Select sheet: **SUMMARY**
4. Format: **CSV**
5. Click **Publish** → Copy the URL
6. Paste URL in `CONFIG.CSV_URL` in `index.html`

## 🔄 Re-deploy after changes

```bash
git add .
git commit -m "Update dashboard"
git push
```
Vercel auto-deploys on every push!

## 📱 Features

- ✅ Auto-fetch from Google Sheets every 5 minutes
- ✅ 5 pages: Overview, Site-wise, Debtor Days, Deductions, Finance Weekly
- ✅ Charts: Top-10 bar, Deduction donut, Aging stacked bar, LD/SD horizontal bars
- ✅ Search & sort on all tables
- ✅ Responsive sidebar layout
- ✅ Print-ready
- ✅ Fallback to static Excel data if Sheets unavailable
