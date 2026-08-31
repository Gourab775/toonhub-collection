# ToonHub â€” 3D Collection Showcase

Interactive 3D figurine showcase with immersive carousel, dynamic theming, and responsive layout. Built as a high-performance React experience for collectible commerce and product storytelling.

Live Demo: `https://toonhub-collection.vercel.app` Â· Category: E-Commerce / Interactive Showcase Â· Stack: React 19, TypeScript, Vite, Tailwind CSS v4

---

## Overview

ToonHub presents a curated 3D collection through a center-stage carousel. Each collectible drives its own background palette, grain texture, and panel tones while users navigate with keyboard or touch. The experience is tuned for retail storytelling â€” bold typography, fluid transitions, and mobile-first responsiveness.

## Features

- **Immersive carousel** â€” Center/left/right/back roles with scale, blur, and opacity transitions (650ms cubic-bezier)
- **Dynamic theming** â€” Per-item background (`#F4845F`, `#6BBF7A`, etc.) with smooth color interpolation
- **Responsive & accessible** â€” Mobile (60% hero) / Desktop (92% hero) layouts, touch/swipe, keyboard nav, `prefers-reduced-motion` ready
- **Performance optimised** â€” Image preloading, `will-change`, grain SVG data URI, no external 3D runtime
- **Design system** â€” Tailwind CSS v4, `lucide-react` icons, Anton + Inter typography

## Tech Stack

- **Frontend:** React 19.2, TypeScript 6, Vite 8, Tailwind CSS 4.3, Lucide React
- **Build:** Vite + Oxlint, `tsc -b` for type checking
- **Styling:** Utility-first CSS, custom transitions, SVG grain filter

## Project Structure

```
.
â”œâ”€ src/
â”‚  â”œâ”€ components/
â”‚  â”‚  â””â”€ HeroSection.tsx   # Carousel logic, role mapping, transitions, theming
â”‚  â”œâ”€ App.tsx              # App shell
â”‚  â”œâ”€ main.tsx             # Entry
â”‚  â””â”€ index.css            # Global styles
â”œâ”€ public/                 # Static assets
â”œâ”€ index.html              # Vite entry HTML
â”œâ”€ vite.config.ts          # Vite + Tailwind + React plugin
â”œâ”€ tsconfig.json           # TS configs
â””â”€ package.json
```

## Getting Started

```bash
# Install
npm install

# Dev (http://localhost:5173)
npm run dev

# Build
npm run build

# Preview
npm run preview

# Lint
npm run lint
```

Node.js 18+ recommended.

## Deployment

Static output in `dist/` after build. Deploy to any static host:

- **Vercel / Netlify:** Build command `npm run build`, output `dist`
- **GitHub Pages:** `npm run build` then publish `dist`
- **Cloudflare Pages:** Framework preset `Vite`

No environment variables required.

## Customization

- **Collection items:** Edit `IMAGES` in `src/components/HeroSection.tsx` â€” `src`, `bg`, `panel` per item
- **Typography:** Anton for display (`3D SHAPE`), Inter for UI â€” change in component `fontFamily`
- **Theme & motion:** Adjust `TRANSITION` constant and `styleMap` roles for timing/easing
- **Branding:** Replace `TOONHUB` labels and `DISCOVER IT` CTA in `HeroSection.tsx`

## Performance Notes

- Preloads 4 hero images on mount; add `loading="lazy"` if collection grows
- Grain is inline SVG data URI â€” no extra request
- For production, enable `oxlint-tsgolint` type-aware rules per `.oxlintrc.json`

## License

MIT â€” free for personal and commercial use.

