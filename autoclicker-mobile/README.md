# AutoClicker Pro v4 — Mobile Edition

A standalone Progressive Web App (PWA) converted from the Chrome extension.

## How to use

### Option A — Open directly in mobile browser
1. Copy all 3 files to a web server (or use GitHub Pages, Netlify, etc.)
2. Open the URL in Chrome (Android) or Safari (iOS)

### Option B — Open as a local file
1. Transfer `index.html` to your phone
2. Open it in Chrome (Android) — works without a server for basic use
   - Note: Service worker and PWA install won't work from `file://`

### Option C — Install as Home Screen App (recommended)
1. Host the files on any web server
2. Open in Chrome/Safari on your phone
3. **Android Chrome:** Menu (⋮) → "Add to Home screen"
4. **iOS Safari:** Share (□↑) → "Add to Home Screen"

Now it runs like a native app, full screen, no browser UI.

## Key differences from the Chrome extension

| Feature | Extension | Mobile PWA |
|---------|-----------|------------|
| Actions target | Any open tab | Same page/tab only |
| XY Picker | Mouse hover + press P | Enter coordinates manually |
| Floating bubble | Yes (overlay on game tab) | Not included |
| Persistence | chrome.storage | localStorage |
| Background timers | Service worker | Page must stay open |

## Files
- `index.html` — full app (UI + logic, self-contained)
- `manifest.json` — PWA manifest for "Add to Home Screen"
- `sw.js` — Service worker for offline support

## Tips
- Keep the screen on and the app in the foreground while running profiles
- iOS may throttle timers when the screen locks — use "Guided Access" to prevent this
- For web-based games running in another tab, open this app in a split-screen view
