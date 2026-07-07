# Eastern Star Study — Install on iPhone & Android

This folder is a complete Progressive Web App (PWA). Once it's hosted at a web
address, it installs to the home screen on both iOS and Android, runs full
screen like a native app, and works **offline** after the first visit. All XP,
badges, and question progress save on the device.

## Step 1 — Put it online (one time, ~2 minutes)

The easiest free option is GitHub Pages (same as your Haul Tycoon deployment):

1. Create a new GitHub repository (e.g. `oes-study`).
2. Upload everything in this folder to the repo root:
   `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`
3. In the repo: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**
4. After a minute your game is live at:
   `https://YOUR-USERNAME.github.io/oes-study/`

(Netlify Drop also works — drag the folder onto netlify.com/drop and you get a URL instantly.)

## Step 2 — Install on iPhone / iPad

1. Open the URL in **Safari** (must be Safari on iOS).
2. Tap the **Share** button (square with the up arrow).
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add**. The five-color star icon appears on your home screen.

It now launches full screen with no browser bars, and keeps working with no
internet connection.

## Step 3 — Install on Android

1. Open the URL in **Chrome**.
2. Chrome will usually show an **Install app** banner automatically — tap it.
   If not: tap the **⋮ menu → Add to Home screen / Install app**.
3. Confirm. The app appears in your app drawer and home screen.

## Notes

- Progress is stored per device (localStorage), so your phone and computer
  each keep their own XP and badges.
- If you update the game later, bump the version in `sw.js`
  (`oes-study-v1` → `oes-study-v2`) so phones fetch the new files.
- The plain `index.html` still works if you just open it directly in any
  browser — hosting is only needed for the home-screen install and offline mode.
