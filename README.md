# YAZDAQ Consistency Tracker — PWA Deployment

## Files in this folder
```
index.html      ← main app (PWA-ready, iOS-optimized)
manifest.json   ← PWA metadata (name, icon, theme)
sw.js           ← service worker (offline support)
icon-192.png    ← app icon (generate below)
icon-512.png    ← app icon large (generate below)
```

---

## Step 1 — Generate App Icons

You need two icon files. Easiest way:

1. Go to https://favicon.io/favicon-generator/
2. Settings:
   - Text: **YZ**
   - Background: **Rounded**
   - Background color: `#09090b`
   - Font color: `#22c55e`
   - Font family: any bold sans-serif
3. Download and rename:
   - Save a 192×192 PNG as `icon-192.png`
   - Save a 512×512 PNG as `icon-512.png`
4. Put both files in this same folder.

---

## Step 2 — Create a GitHub Repo

1. Go to https://github.com → click **New repository**
2. Name it: `yazdaq-tracker` (or anything)
3. Set to **Public**
4. Do NOT initialize with README
5. Click **Create repository**

---

## Step 3 — Upload Files

On the repo page, click **uploading an existing file** (or drag & drop):

Upload all 5 files:
- `index.html`
- `manifest.json`
- `sw.js`
- `icon-192.png`
- `icon-512.png`

Click **Commit changes**.

---

## Step 4 — Enable GitHub Pages

1. In your repo → click **Settings** tab
2. Left sidebar → **Pages**
3. Under "Branch" → select `main`, folder `/root`
4. Click **Save**
5. Wait ~60 seconds

Your app will be live at:
```
https://YOUR-USERNAME.github.io/yazdaq-tracker/
```

---

## Step 5 — Install on iPhone

1. Open Safari on your iPhone (must be Safari, not Chrome)
2. Navigate to your GitHub Pages URL
3. Tap the **Share** button (box with arrow pointing up)
4. Scroll down → tap **Add to Home Screen**
5. Name it `YAZDAQ` → tap **Add**

It now appears on your home screen like a native app — full screen, no browser bar, dark themed.

---

## Notes

- **Data persists** in localStorage — closing the app doesn't wipe anything
- **Works offline** — once loaded, the service worker caches everything
- **Auto weekly reset** — logs clear every Monday, habits stay
- **iOS safe areas** — notch and home bar are handled automatically
- To update the app, just re-upload `index.html` to GitHub — changes go live in ~30 seconds
