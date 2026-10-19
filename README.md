# Tipsy Nails

Single-page website for **Tipsy Nails**, a nail studio in Coral Gables, Florida. The page introduces the studio, lists spa services, and shows how to visit or get in touch.

## Stack

- [Astro](https://astro.build) 4 for the page and layout
- React for the sticky header and mobile menu
- Tailwind CSS for styling
- [AOS](https://michalsnik.github.io/aos/) for scroll animations

## Getting started

From the project root:

```sh
npm install
npm run dev
```

The site runs at [http://localhost:4321](http://localhost:4321).

## Scripts

| Command | Action |
| :------ | :----- |
| `npm install` | Install dependencies |
| `npm run dev` | Start the local dev server |
| `npm run build` | Type-check and build the production site into `./dist/` |
| `npm run preview` | Preview the production build locally |
| `npm run astro -- --help` | Show Astro CLI help |

## Project structure

```text
/
├── favicon.svg
├── src/
│   ├── components/
│   │   ├── Header.jsx       Sticky navigation and social links
│   │   ├── Sidebar.jsx      Mobile menu
│   │   ├── Hero.astro       Opening banner and booking button
│   │   ├── Services.astro   Service highlights
│   │   ├── About.astro      Studio story
│   │   ├── Contact.astro    Email, phone, address, hours, and map
│   │   ├── Reviews.astro    Optional Google reviews fetch (not on the page)
│   │   └── Footer.astro
│   ├── images/
│   ├── layouts/
│   │   └── Layout.astro     Title, meta tags, and local business schema
│   ├── pages/
│   │   └── index.astro      Home page
│   ├── styles/
│   └── utils/
│       └── aos.js
├── astro.config.mjs
└── package.json
```

Astro turns each file in `src/pages/` into a route. Images used by the page live in `src/images/`.

## Contact details on the site

| | |
| :-- | :-- |
| Email | hello@tipsynails.com |
| Phone | (305) 555-0142 |
| Address | 220 Miracle Mile, Suite 4, Coral Gables, FL 33134 |
| Hours | Tue–Sat 10:00 AM – 7:00 PM, Sun 11:00 AM – 4:00 PM |
| Instagram | [@tipsynails.studio](https://www.instagram.com/tipsynails.studio/) |

Update those values together in:

- `src/components/Contact.astro` for the contact section and map
- `src/components/Header.jsx` and `src/components/Sidebar.jsx` for the phone, WhatsApp, and Instagram links
- `src/layouts/Layout.astro` for the page title, description, and schema.org details

Booking buttons scroll to the contact section (`#contact`).
