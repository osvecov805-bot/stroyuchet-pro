# РемонтПермь - Apartment Renovation Landing Page

## Project Overview
A static HTML landing page for a Russian apartment renovation company based in Perm. Single-file website with no build system or dependencies.

## Structure
- `index.html` - Single-page website with embedded CSS and JavaScript
- `.github/workflows/deploy.yml` - GitHub Actions workflow for Netlify deployment (original CI)

## Tech Stack
- Pure HTML/CSS/JavaScript (no framework, no build system)
- Self-contained single file

## Running Locally
Served with Python's built-in HTTP server:
```
python3 -m http.server 5000 --bind 0.0.0.0
```

## Deployment
Configured as a static site deployment with `publicDir: "."`.
