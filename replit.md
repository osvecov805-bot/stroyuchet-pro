# РемонтПермь - Apartment Renovation Landing Page

## Project Overview
A static HTML landing page for a Russian apartment renovation company based in Perm. Single-file website with no build system or dependencies.

## Structure
- `index.html` - Single-page website with embedded CSS and JavaScript
- `images/` - Portfolio images directory
  - `kapremont.jpg` - Capital renovation project image
  - `novostroyka.jpg` - New construction project image
  - `sanuzel.jpg` - Bathroom renovation project image
- `.github/workflows/deploy.yml` - GitHub Actions workflow for Netlify deployment (original CI)

## Tech Stack
- Pure HTML/CSS/JavaScript (no framework, no build system)
- Self-contained single file

## Running Locally
Served with Python's built-in HTTP server:
```
python3 -m http.server 5000 --bind 0.0.0.0
```

## Recent Changes
- Added portfolio section images (replaced gradient placeholders with actual photos)
- Updated CSS for `.portfolio-img` to use `object-fit: cover` for proper image scaling
- Portfolio images now display 220px height with full width coverage

## Deployment
Configured as a static site deployment with `publicDir: "."`.

## GitHub Push
Pending: Manual push of changes to GitHub
- Modified: `index.html` (portfolio HTML + CSS updates)
- Added: `images/kapremont.jpg`, `images/novostroyka.jpg`, `images/sanuzel.jpg`
- Command: `git add index.html images/ && git commit -m "Add portfolio images and update HTML" && git push origin main`
