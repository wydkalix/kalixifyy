# Kalixify Music

A responsive, installable Progressive Web App (PWA) prototype. It is ad-free and uses no paid APIs. It includes a demo catalog, audio player, search, liked songs, and browser-saved playlists.

## Run locally

You need Node.js installed. From this folder run:

```bash
npx serve .
```

Open the local URL printed in the terminal. For PWA installation, use HTTPS hosting (or localhost while testing). Opening `index.html` directly as a file will not enable the service worker.

## Install on Android

1. Deploy the files to an HTTPS static host such as GitHub Pages or Cloudflare Pages.
2. Open the deployed URL in Chrome on your Android phone.
3. Open Chrome's menu (⋮) and choose **Install app** or **Add to Home screen**.
4. Launch Kalixify from the new home-screen icon.

## Deploy with GitHub Pages

1. Create a GitHub repository and upload the contents of this folder.
2. In repository **Settings → Pages**, enable deployment from your branch or GitHub Actions.
3. For a repository URL such as `username.github.io/kalixify-app/`, set Vite-style base paths only if you later migrate to Vite. This current static app uses relative paths.
4. Open the published HTTPS URL on your phone.

## Important limits

- Included tracks are external sample streams for demonstration, not a licensed commercial music catalog. Their availability depends on the host and internet connection.
- This prototype stores playlists and liked songs in the current browser's local storage. It does not sync across devices and has no user accounts yet.
- The service worker caches the app shell, not full music tracks. Offline music, background playback reliability, artist/album search, account sync, and a broad licensed catalog need further implementation.
- Only stream music you own or have permission to distribute. This project does not bypass Spotify or other services' access controls.

## Suggested next production steps

1. Add authentication and a cloud database for user playlists.
2. Integrate a licensed/open music catalog and track metadata.
3. Add audio session handling, Media Session metadata, and more reliable mobile background controls.
4. Add import/export of Kalixify playlists (optional; no Spotify import is required).
5. Package for Play Store with a Trusted Web Activity or native Android wrapper if desired.
