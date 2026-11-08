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


## Version 1.1 update
- Added an in-app HOW TO guide with safe phone placement, framing, lighting and repeatable practice tips.
- Camera preview is portrait-first (9:16) and requests a portrait capture format where supported.
- PWA manifest requests portrait orientation. Some iOS Safari camera/browser behavior may ignore capture constraints; this does not guarantee a particular frame rate or automatic launch measurements.

### Updating the live GitHub Pages app
Upload the updated files from this package to the same repository root and commit the changes. Replace files with the same names. Then reload the app in Safari; if the installed Home Screen version shows the old build, close it fully and reopen after the service worker refreshes, or clear Safari website data for the site.


## v1.2 camera orientation update
- Requests a portrait 9:16 camera stream where supported.
- Uses crop-and-scale where supported and fills the portrait preview frame, cropping a landscape source rather than letterboxing it.
- Updates the service-worker cache version so the new camera styling and behavior are picked up after deployment.


## v1.3 iPhone camera orientation fix
- Detects landscape camera streams and rotates the live preview 90 degrees to fill the portrait frame.
- Recalculates preview geometry when the device orientation or viewport changes.
- This fixes the live preview; native recorded clip orientation may still vary by iPhone/browser.
