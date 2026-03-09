# РемонтПермь - Apartment Renovation Landing Page

## Project Overview
A fully responsive HTML landing page for a Russian apartment renovation company. Features dynamic service cards with modals, interactive portfolio section, and JSON-driven content management.

## Tech Stack
- Pure HTML/CSS/JavaScript (no frameworks, no build system)
- Dynamic data loading from JSON files
- Modal windows with smooth animations
- Responsive grid layouts
- Object-fit image optimization

## File Structure
- `index.html` - Main website with embedded CSS/JavaScript and modal systems
- `services.json` - 6 services with pricing, descriptions, advantages, includes lists
- `regional-config.json` - Regional pricing configuration and coefficients
- `portfolio.json` - 3 portfolio projects with full descriptions
- `images/` - Portfolio image assets (kapremont.jpg, novostroyka.jpg, sanuzel.jpg)
- `.github/workflows/deploy.yml` - Netlify deployment workflow

## Features

### Services Section
- ✅ 6 services dynamically loaded from `services.json`
- ✅ Interactive modal with full details on click
- ✅ Advantages list (3-5 items each)
- ✅ What's included list (5-8 items each)
- ✅ Pricing and regional validity dates
- ✅ "Order calculation" CTA button

### Portfolio Section
- ✅ 3 completed projects with text-only cards
- ✅ Cards show: title, area, duration, work type
- ✅ "View Work" button opens detailed modal
- ✅ Full-size collage images (object-fit: contain) in modal
- ✅ Detailed project descriptions
- ✅ Project details in info grid (area, duration, type)
- ✅ Smooth modal animations with fade-in/slide-up

### Both Sections
- ✅ Beautiful modal overlays with dark backgrounds
- ✅ Close buttons (X) and click-outside closing
- ✅ Smooth animations and transitions
- ✅ Fully responsive design
- ✅ All content in JSON files (easy updates)

## JSON Data Structure

### services.json
6 services, each with:
- `id`, `title`, `shortDescription`, `fullDescription` (3-5 sentences)
- `priceFrom`, `priceUnit`, `region`, `isActual`, `lastUpdate`
- `advantages` (3-5 items), `includes` (5-8 items)

### regional-config.json
- Base rates for each service type
- Coefficients: outOfCity (1.2), urgent (1.3), complexity (1.15)
- Currency, working hours, warranty info

### portfolio.json
3 projects, each with:
- `id`, `title`, `area`, `duration`, `type`
- `image` (unused), `imageUrl` (full collage path)
- `description` (detailed project write-up)

## Running Locally
```bash
python3 -m http.server 5000 --bind 0.0.0.0
```
Then open http://localhost:5000 or use Replit preview.

## Recent Changes
- Created `portfolio.json` with 3 detailed projects
- Redesigned portfolio section with text-only cards
- Added portfolio modal system with full collage images
- All portfolio images display at full resolution (object-fit: contain)
- Professional descriptions for each completed project
- Both sections use JSON for easy content updates

## Deployment
Configured as static site with `publicDir: "."`.

## How Users Interact

### Services
1. User scrolls to "Наши услуги" section
2. Sees 6 service cards with icons and short descriptions
3. Clicks card or "Подробнее" button
4. Modal opens with full description, advantages, includes, pricing
5. Clicks "Заказать расчёт" to contact form

### Portfolio
1. User scrolls to "Наши работы" section
2. Sees 3 text cards with project info and "Смотреть работу" button
3. Clicks button
4. Modal opens with full collage image and detailed project description
5. Can close modal with X or by clicking outside

## Files to Push to GitHub
- `index.html` (completely redesigned modal systems)
- `services.json` (all service data)
- `regional-config.json` (pricing config)
- `portfolio.json` (portfolio projects)
- `replit.md` (documentation)
- `images/` folder with portfolio images

Total: 5 files + 1 directory changed/added
