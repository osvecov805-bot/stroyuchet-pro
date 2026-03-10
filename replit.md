# РемонтПермь - Apartment Renovation Landing Page

## Project Overview
A premium dark-themed landing page for a Russian apartment renovation company (РемонтПермь) in Perm, Russia. Features a full-screen hero, interactive quiz calculator, service/portfolio modals, scroll animations, and JSON-driven content.

## Tech Stack
- Pure HTML/CSS/JavaScript (single file, no frameworks, no build system)
- Dynamic data loading from JSON files via fetch()
- IntersectionObserver-based scroll animations
- CSS custom properties for theming
- Responsive design with mobile hamburger menu

## Color Scheme
- Background: #0f0f1a (near-black), #1a1a2e (dark blue)
- Accent: #f5a623 (gold), #ffd700 (light gold)
- Cards: #1c1c30, #252540
- Text: white (#fff), gray (#9ca3af, #d1d5db)

## File Structure
- `index.html` - Complete website (CSS + JS embedded)
- `services.json` - 6 services with pricing, descriptions, advantages, includes
- `regional-config.json` - Regional pricing configuration
- `portfolio.json` - 3 portfolio projects with descriptions and image paths
- `attached_assets/` - Portfolio collage images (used in modals)
- `images/` - Additional image assets

## Sections (in order)
1. **Sticky Header** - Dark, logo left, nav center, phone right, hamburger on mobile
2. **Hero** - Full-screen, subtitle, headline, 3 features with icons, CTA buttons, stats
3. **Quiz Calculator** - 5-step interactive form (object type, area, repair type, timing, contact)
4. **Principles** - 4 cards (01-04) with gold number overlays
5. **Services** - Grid of 6 cards from services.json, modals with full details
6. **Portfolio** - Grid of 3 text cards from portfolio.json, modals with full collage images
7. **Work Stages** - 6-step vertical timeline
8. **Measure Form** - Name/phone form with dynamic counter (5/3/2 based on time of day)
9. **Reviews** - 3 review cards with gold stars
10. **Contacts** - Phone, email, social links, Yandex Maps iframe
11. **Footer** - Social icons, nav links, copyright

## JSON Data Structure

### services.json
6 services, each with:
- `id`, `title`, `shortDescription`, `fullDescription`
- `priceFrom`, `priceUnit`, `region`, `isActual`, `lastUpdate`
- `advantages` (3-5 items), `includes` (5-8 items)

### portfolio.json
3 projects, each with:
- `id`, `title`, `area`, `duration`, `type`
- `imageUrl` (path to collage in attached_assets/)
- `description` (detailed project write-up)

## Contact Info
- Phone: +7 (952) 330-99-44
- Email: remont.perm.159@yandex.ru
- Telegram: https://t.me/VKProtarget1
- VK: https://vk.ru/club236479775

## Running Locally
```bash
python3 -m http.server 5000 --bind 0.0.0.0
```

## Deployment
Configured as static site with `publicDir: "."`.

## Key Implementation Details
- Both forms (quiz + measure) connected to Netlify Forms via fetch POST
- Quiz tracks selected answers in `quizAnswers` object across all 5 steps
- Hidden quiz form in HTML for Netlify form detection (name="quiz")
- Measure form: name="measure" with honeypot spam protection
- Success messages: gold gradient text with checkmark icon and fade-in animation
- Measure counter: shows 5 before noon, 3 afternoon, 2 evening
- Service/portfolio modals close on X button or overlay click
- Scroll animations use single shared IntersectionObserver
- All content updates can be made via JSON files without touching HTML
