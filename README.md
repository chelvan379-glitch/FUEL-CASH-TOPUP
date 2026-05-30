# ⛽ FUEL CASH TOPUP PWA

A Progressive Web App (PWA) for managing fuel cash top-up claims in telecom site operations.

## Features

- ✅ **Full Offline Support** — IndexedDB permanent storage, works without internet
- 📊 **Dashboard** — Live stats: total claims, monthly totals, permanent vs temporary vehicles
- 📋 **Entry Form** — Add claims with: No, Date, Plate, Vehicle Type, Car Type, Reason, Amount
- 📗 **Excel Export** — Generates `.xlsx` file matching the approved claim format with SUM formula
- 💬 **WhatsApp Sharing** — Share summary via WhatsApp
- 💾 **JSON Backup/Restore** — Export & import full database backup
- 🖨️ **Print Summary** — Printable claim summary page
- 📱 **Installable** — Add to home screen on Android/iOS

## File Structure

```
fuel-pwa/
├── index.html      ← Main app (all-in-one)
├── manifest.json   ← PWA manifest
├── sw.js           ← Service worker (offline caching)
├── icon-192.png    ← App icon (192×192)
├── icon-512.png    ← App icon (512×512)
└── README.md
```

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g., `fuel-topup`)
2. Upload all files to the repo root
3. Go to **Settings → Pages**
4. Set **Source** to `main` branch, root `/`
5. Click **Save** — your app will be live at:
   `https://yourusername.github.io/fuel-topup/`

## Install as PWA (Android)

1. Open the GitHub Pages URL in Chrome
2. Tap the **⋮ menu → "Add to Home Screen"**
3. Tap **Install**
4. App appears on home screen — works offline!

## Excel Format (Output)

| No | Date | No Plate | Permanent/Temporary | Car Type | Reason | Cash Amount (RM) |
|----|------|----------|---------------------|----------|--------|------------------|
| 1  | 3/2/2026 | VNB7516 | Permanent | Triton 4WD | Scheduled servicing... | RM 185.70 |
| ... | | | | | TOTAL: | =SUM(...) |

## Tech Stack

- Vanilla HTML/CSS/JS (zero dependencies for core app)
- [SheetJS (xlsx)](https://sheetjs.com/) for Excel generation
- IndexedDB for offline storage
- Service Worker for PWA caching
- Google Fonts (Barlow Condensed + Barlow)

## License

MIT — Free for personal and commercial use.
