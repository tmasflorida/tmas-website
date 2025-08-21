# TMAS Website (Static Deploy)

This repo contains the static HTML/CSS/JS files for the TMAS website, generated from the Next.js source repo (`tmas-website-source`).

## Purpose
- Hosts the exported static site for deployment on Vercel.
- Should only contain files from the `out/` folder after export.

## Workflow
1. All development happens in the source repo (`tmas-website-source`).
2. After building and exporting the site, the static files are copied here.
3. Any push to this repo triggers Vercel to redeploy the site.

## How to Update
1. In the source repo, run:
   ```bash
   npm run build
   npm run export
   ./build-and-deploy.sh
   ```
2. The script will copy the latest static files here and push changes.
3. Vercel will automatically redeploy.

## Notes
- Do **not** edit files here directly. All changes should come from the source repo export.
- If Vercel errors with “No Next.js version detected”, ensure only static files are present.

## Structure
- HTML files for each page
- Static assets (images, CSS, JS)
- No source code or config files for Next.js

---
For development, see the documentation in the source repo (`tmas-website-source`).
