# Morse Code Trainer (PWA)

A self-contained, installable web app for practicing Morse code by ear —
plays tones, accepts typed or spoken answers, and works offline once installed.

## Files

- `index.html` — the app itself
- `manifest.json` — makes it installable ("Add to Home Screen")
- `sw.js` — service worker, caches the app for offline use
- `icons/` — app icons (192px and 512px)

## Why it needs real hosting

Microphone access and service workers both require HTTPS and a real
top-level domain — they don't work from a `file://` path or from most
sandboxed/embedded viewers. GitHub Pages gives you both for free.

## Deploy with GitHub Pages (free, ~10 minutes)

1. Create a new GitHub repository (public is fine and free).
2. Upload all the files in this folder, **keeping the folder structure**
   (the `icons/` folder needs to stay a subfolder).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch",
   branch `main`, folder `/ (root)`. Save.
5. Wait a minute or two, then your app will be live at:
   `https://<your-username>.github.io/<repo-name>/`
6. Open that link on your phone in Safari or Chrome. You should get a
   proper microphone permission prompt this time — Pages serves over real
   HTTPS with no restrictive permissions policy.
7. To install it as an app icon: on iOS Safari, tap Share → **Add to Home
   Screen**. On Android Chrome, tap the menu → **Install app**.

## Alternative hosts

Netlify and Vercel both work the same way (drag-and-drop the folder,
get a live HTTPS URL) if you'd rather not use GitHub.

## Sharing it with others

Once deployed, the GitHub Pages link is just a normal URL — you can
share it with anyone and they can use it in their browser or install it,
no account or app store needed.
