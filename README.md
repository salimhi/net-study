# NET Study – GitHub Pages + Android PWA

This folder is ready to upload to a GitHub repository and publish with GitHub Pages.

## Publish on GitHub Pages
1. Create a new GitHub repository (for example `net-study`).
2. Upload **all files and folders in this package** to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then Save.
6. Wait for GitHub Pages to show the public HTTPS URL.

## Install on Android
1. Open the GitHub Pages URL in Chrome on Android.
2. Tap **Install NET Study App** in Settings, or use Chrome **⋮ → Install app / Add to Home screen**.
3. The app opens in a standalone window and uses the same browser storage as the hosted site.

## Important migration note
Data stored in a local `file://` copy does not automatically move to the GitHub Pages origin. Before switching, use **Settings → Export Master Backup** in the old copy. Then open the hosted/PWA version and use **Import Master Backup**.

## PDF renderer
The existing Android PDF.js fallback remains in the app. Its CDN resources are runtime-cached by the service worker after they are successfully fetched. The first internal PDF render can therefore still require internet access.

## Updating later
Replace `index.html` (and other changed files) in the repository and commit. GitHub Pages redeploys automatically. If a PWA update appears stale, close and reopen the installed app; the service worker uses network-first navigation and updates its cached page.


## Flat-root upload version
All files in this package are intentionally placed in one directory. Upload every file to the repository root; do not create an icons folder.
