# AssemblyGS project website

Static project website for **Reconstructing High-Fidelity 3D Part Assemblies via Gaussian Splatting**.

Expected site: https://assemblygs.github.io/

## Preview

Run `python -m http.server 8766` in this directory, then open http://localhost:8766/. Use HTTP rather than file:// so the browser can fetch JSON and 3D assets.

## Publish

In **Settings → Pages → Build and deployment**, select **GitHub Actions** as the Source. The workflow in `.github/workflows/pages.yml` deploys on pushes to `main` and can also be run manually. The repository visibility and account plan must support GitHub Pages.

No build step or application server is required. GitHub Actions supplies the deployment token. Only `index.html`, `demo.html`, `.nojekyll`, `demo/`, and `static/` are uploaded as the website.

## Assets and validation

The Paper button opens `static/pdf/assemblygs.pdf` (November 17 manuscript). The 166.5-second 1080p project video is `static/video/assemblygs.mp4`. Four 3D scenes are in `demo/`. Local Three.js 0.180.0 and Spark 2.3.1 dependencies, with their upstream MIT licenses, are in `static/vendor/`.

The main page loads fonts, Bulma and icon styles from external providers. The viewer requires WebGL 2. Checks covered Chromium at 320, 375, 390, 768 and 1440 CSS px, and four hardware-WebGL demos including playback, scrubbing, exact timeline endpoints, and emulated touch rotation/pinch. Physical-phone performance and Safari were not verified.
