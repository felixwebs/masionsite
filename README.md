# MAISON — Exceptional Properties

A luxury real estate website featuring a curated collection of extraordinary homes in the world's most coveted addresses. Built as a pure HTML/CSS/JS multi-page site with a Supabase backend for dynamic property listings.

---

## Pages

| File | Description |
|------|-------------|
| `index.html` | Homepage — hero, featured listings, neighbourhoods, process, testimonials |
| `properties.html` | Full property listings/search page |
| `property.html` | Individual property detail view |
| `about.html` | Company story, team, and values |
| `contact.html` | Enquiry and office contact information |
| `admin.html` | Admin dashboard for managing listings |

---

## Features

- **Dynamic listings** — Properties fetched from Supabase and rendered in a magazine-style grid
- **Custom cursor** — Smooth animated cursor with lag effect
- **Page transitions** — Silky overlay animation between pages
- **Scroll reveal** — Elements animate in as they enter the viewport
- **Sticky nav** — Transparent header that frosts on scroll
- **Animated ticker** — Live-style marquee of recent listing activity
- **Testimonial carousel** — Rotating client quotes with fade transitions
- **Mobile menu** — Full-screen overlay navigation for small screens
- **Cookie consent** — Banner with granular preference controls (Essential / Analytics / Marketing)
- **Responsive design** — Graceful layout adaptation from desktop to mobile

---

## Tech Stack

- **Frontend:** Vanilla HTML5, CSS3, JavaScript (no frameworks)
- **Fonts:** Cormorant Garamond, Jost (via Google Fonts)
- **Backend/DB:** [Supabase](https://supabase.com) (PostgreSQL)
- **Images:** [Unsplash](https://unsplash.com)

---

## Supabase Setup

The site connects to a Supabase project for property data. The `properties` table should include the following columns:

| Column | Type | Description |
|--------|------|-------------|
| `id` | uuid / int | Unique property ID |
| `title` | text | Property name |
| `location` | text | City or neighbourhood |
| `price` | numeric | Raw price value |
| `price_display` | text | Formatted price string (e.g. `€4,200,000`) |
| `bedrooms` | int | Number of bedrooms |
| `images` | text[] | Array of image URLs |
| `badge` | text | Optional label (e.g. `New Listing`, `Just Sold`) |
| `status` | text | `for_sale`, `for_rent`, `sold`, etc. |
| `sort_order` | int | Display order on homepage |

Update the Supabase URL and anon key in `index.html` (and other pages) if connecting to a different project.

---

## Design Tokens

The colour palette is defined as CSS custom properties in each page's `<style>` block:

```css
--cream:    #F6F3EE   /* Page background */
--warm:     #EDE8DF   /* Secondary background */
--charcoal: #1C1C1C   /* Dark sections, footer */
--ink:      #2E2B27   /* Body text */
--muted:    #8A8278   /* Secondary text */
--gold:     #B89B6A   /* Accent */
--gold-lt:  #D4BC94   /* Light accent */
--white:    #FDFCFA   /* Cards, light sections */
```

---

## Getting Started

No build step required — open any `.html` file directly in a browser, or serve with any static file server:

```bash
# Python
python -m http.server 8000

# Node (npx)
npx serve .
```

Then visit `http://localhost:8000`.

---

## Deployment

This site is fully static and can be deployed to any static hosting provider:

- **GitHub Pages** — push to a repo and enable Pages in settings
- **Netlify** — drag and drop the folder or connect the repo
- **Vercel** — `vercel --prod` from the project root

---

## License

© 2026 Maison. All rights reserved.
