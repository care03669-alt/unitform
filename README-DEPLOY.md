# unitform — deploy to GitHub + Vercel

This is a static website. No build command or environment variables are required.

## 1) Publish the source on GitHub
1. Create a new repository named `unitform` at https://github.com/new.
2. Keep it Public if you want GitHub Pages on the free plan.
3. Extract this ZIP and upload the CONTENTS of this folder to the repository root (not an extra nested folder).
4. Commit to the `main` branch.

## 2) Enable GitHub Pages (optional second host)
1. Open the repository → Settings → Pages.
2. Under Build and deployment, choose `Deploy from a branch`.
3. Select branch `main`, folder `/ (root)`, then Save.
4. GitHub will show the Pages URL in the same settings panel.

## 3) Deploy on Vercel (recommended primary host)
1. Sign in at https://vercel.com/ using GitHub.
2. Choose Add New → Project and import the `unitform` repository.
3. Framework Preset: Other.
4. Build Command: leave empty; Output Directory: `.` (root).
5. Click Deploy. Vercel will provide a `*.vercel.app` URL.

Every push to `main` will trigger a new Vercel deployment automatically. GitHub Pages may take a few minutes to publish after enabling it.

## Notes
- No Node.js build is needed; this is plain HTML/CSS/JS.
- `vercel.json` contains minimal static-site routing settings.
- Some functions rely on browser support or external services/CDNs; see README.md for details.
- Do not add API keys or secrets to client-side JavaScript.
