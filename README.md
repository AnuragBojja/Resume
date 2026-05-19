# Anurag Bojja — Resume

A simple static site that displays my latest resume PDF with a one-click download button. Deployed via GitHub Pages so the link never changes — I just push an updated PDF.

## Files

- `index.html` — the page (PDF viewer + download button)
- `AnuragBojja-Resume-DevSecOps.pdf` — the resume itself

## Local preview

Just open `index.html` in a browser. (For the "Last updated" badge to work the file needs to be served over HTTP — but everything else works from a `file://` URL.)

```bash
# Optional: run a local server
python -m http.server 8080
# then visit http://localhost:8080
```

## Deploy to GitHub Pages

1. Create a new repo on GitHub (e.g. `resume`) and push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial resume site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/resume.git
   git push -u origin main
   ```
2. On GitHub: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / **/ (root)** → **Save**
3. Wait ~1 minute. Your site will be live at:
   `https://<your-username>.github.io/resume/`

## Updating the resume

Whenever I update the PDF:

```bash
# Replace the PDF file, then:
git add AnuragBojja-Resume-DevSecOps.pdf
git commit -m "Update resume"
git push
```

GitHub Pages will redeploy automatically in under a minute, and anyone with the link gets the latest version.

> **Tip:** Keep the PDF filename the same (`AnuragBojja-Resume-DevSecOps.pdf`) so the link in `index.html` keeps working without edits.
