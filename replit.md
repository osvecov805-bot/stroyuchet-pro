# РемонтПермь - Apartment Renovation Landing Page

## Project Overview
A static HTML landing page for a Russian apartment renovation company based in Perm. Features dynamic service cards loaded from JSON data, interactive modals, and responsive design.

## Structure
- `index.html` - Main website with embedded CSS and JavaScript for modal functionality
- `services.json` - Service data with descriptions, pricing, advantages, and includes
- `regional-config.json` - Regional pricing configuration and coefficients
- `images/` - Portfolio images directory
  - `kapremont.jpg` - Capital renovation project image
  - `novostroyka.jpg` - New construction project image
  - `sanuzel.jpg` - Bathroom renovation project image
- `.github/workflows/deploy.yml` - GitHub Actions workflow for Netlify deployment

## Tech Stack
- Pure HTML/CSS/JavaScript (no framework, no build system)
- Dynamic data loading from JSON files
- Modal windows with animations
- Responsive grid layout

## Features
- **Dynamic Services**: All 6 services loaded from `services.json`
- **Modal Details**: Click any service card to open detailed modal with:
  - Full description
  - Price information
  - Advantages list
  - What's included list
  - Call-to-action button to contact form
- **Regional Configuration**: Pricing managed through `regional-config.json`
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Smooth Animations**: Fade-in and slide-up modal animations
- **Accessible**: Modal closes on button, close icon, or clicking outside

## JSON Data Structure

### services.json
6 services with:
- `id`: unique identifier
- `title`: service name
- `shortDescription`: brief description for card
- `fullDescription`: detailed 3-5 sentence description for modal
- `priceFrom`: starting price
- `priceUnit`: price unit (руб/м², руб, руб/точка)
- `region`: service region
- `isActual`: current status
- `lastUpdate`: last update date
- `advantages`: array of 3-5 benefits
- `includes`: array of 5-8 what's included items

### regional-config.json
- Base rates for each service
- Coefficients for out-of-city, urgency, complexity
- Currency, working hours, warranty info

## Running Locally
Served with Python's built-in HTTP server:
```
python3 -m http.server 5000 --bind 0.0.0.0
```

## Recent Changes
- Added `services.json` with all 6 services and detailed data
- Added `regional-config.json` with regional pricing configuration
- Implemented dynamic service card rendering from JSON
- Added modal window system with smooth animations
- Added "Подробнее" (More Info) button to service cards
- Modal includes advantages and includes lists from JSON
- All content data stored in JSON files for easy updates
- Original design and existing sections preserved

## Deployment
Configured as a static site deployment with `publicDir: "."`.

## User Workflow
1. User sees services grid with cards
2. User hovers over card (animation feedback)
3. User clicks card or "Подробнее" button
4. Modal opens with full service details
5. User can click "Заказать расчёт" to go to contact form
6. User can close modal with X button or by clicking outside

## Future Enhancements
- Add service filters or categories
- Add comparison feature for multiple services
- Integrate form submission with backend
- Add testimonials for specific services
- Add service booking calendar
