# NET Study – GitHub Pages upload package

Upload **all files in this folder to the root of the `net-study` repository**.

Files:
- index.html
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png
- icon-maskable-512.png
- pdf.min.js
- pdf.worker.min.js

The two PDF files are same-origin bootstrap files. They try jsDelivr, UNPKG, then cdnjs for PDF.js 3.11.174. This removes the single-cdnjs failure point and lets the existing PWA service worker cache successful dependency requests.

After uploading, refresh the GitHub Pages site. If an old service worker is active, close/reopen the site or hard-refresh once so cache `net-study-pwa-v4-pdf-local` activates.
