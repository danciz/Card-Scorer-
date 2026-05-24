# 🃏 Family Card Scorer Pro

A fun, colourful score tracker built for family game nights. Works as a web app and can be installed on Android and iOS as a PWA.

![Card Scorer Preview](https://img.shields.io/badge/PWA-Ready-6bcb77?style=for-the-badge&logo=pwa)
![Tests](https://img.shields.io/badge/Tests-459%2F459%20Passing-4d96ff?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-ffd93d?style=for-the-badge)

---

## ✨ Features

- **Multi-player support** — 1 to 16 players, each with a unique colour & emoji avatar
- **Two game modes** — Highest score wins or Lowest score wins
- **Target score** — Set a target to trigger automatic win detection
- **Tie detection** — Correctly handles ties across any number of players
- **Round-by-round scoring** — Add scores per round with an undo button
- **Live leaderboard** — Updates in real time with 🥇🥈🥉 medals
- **Save & Resume** — Save mid-game and pick up exactly where you left off
- **Use Last Players** — One tap to carry your player list into a new game
- **Game History** — Last 20 rounds/sessions logged automatically
- **Offline support** — Full PWA with service worker caching
- **Installable** — Add to home screen on Android and iOS

---

## 🚀 Live Demo

> **[Play it here →](https://danciz.github.io/Card-Scorer-/)**
> *(Replace with your GitHub Pages URL after deployment)*

---

## 📁 File Structure

```
card-scorer-/
├── index.html                  # Main app (single file)
├── manifest.json               # PWA manifest
├── sw.js                       # Service worker (offline support)
├── icons/
│   ├── icon-192.png            # PWA icon (192×192)
│   └── icon-512.png            # PWA icon (512×512)
├── .github/
│   └── workflows/
│       └── pages.yml           # Auto-deploy to GitHub Pages
└── README.md
```

---

## 🛠️ Deploy to GitHub Pages

### Option A — Automatic (recommended)

1. Create a new repo on GitHub (e.g. `card-scorer`)
2. Upload all files from this folder
3. Go to **Settings → Pages**
4. Under **Source**, select **GitHub Actions**
5. Push to `main` — the workflow deploys automatically

Your app will be live at:
```
https://YOUR-USERNAME.github.io/card-scorer/
```

### Option B — Manual (no workflow needed)

1. Create a new repo on GitHub
2. Go to **Settings → Pages**
3. Under **Source**, select **Deploy from a branch**
4. Choose `main` branch, `/ (root)` folder
5. Save — GitHub deploys within ~60 seconds

---

## 📱 Install as Android App (TWA / Bubblewrap)

Once deployed to GitHub Pages, you can package it as an Android APK using Google's [Bubblewrap CLI](https://github.com/GoogleChromeLabs/bubblewrap):

```bash
# Install Bubblewrap
npm i -g @bubblewrap/cli

# Initialise from your live PWA URL
bubblewrap init --manifest https://YOUR-USERNAME.github.io/card-scorer/manifest.json

# Build the APK
bubblewrap build
```

This generates a signed APK you can sideload or submit to the Play Store.

---

## 📱 Install on iOS

1. Open the app URL in **Safari**
2. Tap the **Share** button
3. Tap **Add to Home Screen**
4. Tap **Add**

The app will appear on your home screen and run in full-screen standalone mode.

---

## 🧪 Tests

All game logic is covered by an automated test suite (459 tests, 100% passing):

```bash
node test_game.js
```

Tests cover:
- Score calculation and accumulation (1–16 players)
- Win detection (high/low modes, ties, edge cases)
- Undo, round reset, and multi-round flows
- Save & resume round-trips
- Last players persistence
- History logging and 20-entry cap
- Invalid input handling
- Corrupt save recovery

---

## 🎮 How to Play

1. **Setup** — Enter a game name, choose High or Low wins, set an optional target score, and add player names
2. **Score** — Each round, enter each player's score in the input box and press Enter/Return
3. **Undo** — Tap ↺ to remove a player's last score entry
4. **Next Round** — Tap 🔄 to log the round and reset scores for the next round
5. **Save** — Tap 💾 any time to save progress (survives closing the browser/app)
6. **End Game** — Tap ✅ to log the final result and return to setup

---

## 📄 License

MIT — free to use, modify, and distribute.
