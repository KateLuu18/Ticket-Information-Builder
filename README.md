# Nexus TIB — Ticket Information Builder

Internal tool for Service Owners at GPP / VNG Games to design ticket forms for the Nexus platform.

## 🚀 Deploy

This is a single-file static HTML app served via `serve`. Auto-deployed via Railway when code is pushed to the connected branch.

### Local test

```bash
npm install
npm start
# Opens at http://localhost:3000
```

### Production (Railway)

Railway auto-detects Node.js, runs `npm install` then `npm start`. The `serve` package serves `index.html` on the port Railway assigns via `$PORT`.

## 📦 Update workflow

1. Edit `index.html` locally
2. `git add . && git commit -m "..." && git push`
3. Railway auto-builds & deploys (~30s)
4. Refresh production URL to see changes

## 🗂️ Tech stack

- Single-file HTML + Tailwind CDN + vanilla JS
- CDN dependencies: Tailwind, html2pdf.js, JSZip, Google Fonts (Inter)
- Storage: browser `localStorage` (per-user, per-browser)
- No backend / database needed

## 🔒 Data privacy

All form designs are stored in the user's browser `localStorage`. Nothing is sent to the server. Each user sees only their own designs.
