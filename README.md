# BirdieLab — Golf Performance

A clean, installable golf practice and shot-log PWA designed for iPhone.

## Included in this first web release
- Premium light/dark interface with restrained graphite and red accents.
- Camera preview using browser camera permissions.
- Browser video clip recording and download (if supported).
- Club selector preloaded with the user's current bag categories.
- Manual shot entry for ball speed, carry, launch angle, direction and notes.
- Local shot history, session averages and CSV export.
- Home Screen / PWA manifest and service worker.

## Important measurement limitations
This is the first functional interface and practice-log release, not yet an automatic launch monitor. Shot metrics are manually entered and are clearly not camera-verified. Browser camera frame rate is device/browser-dependent and this app does not promise 240 FPS capture. Ball speed, launch, spin and carry automation require a separate calibrated computer-vision implementation and validation against a trusted launch monitor.

## Publish with GitHub Pages
1. Upload the contents of this folder to the root of your GitHub repository (not the enclosing folder).
2. In GitHub, open Settings → Pages.
3. Under Build and deployment, choose Deploy from a branch.
4. Choose `main` and `/ (root)`, then Save.
5. Wait for the Pages URL to appear. Open it in Safari on iPhone.
6. In Safari, tap Share → Add to Home Screen.

Camera access requires HTTPS; GitHub Pages provides HTTPS. Shot data is stored locally in the browser on the device and is not synced between devices. Export CSV periodically to back it up.
