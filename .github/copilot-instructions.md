# Copilot Instructions — Jireh Landing

## Project

Landing page for **JIREH Exportaciones y Asesorías S.A.S** — a Colombian agricultural export company specializing in avocados. Built with Astro 6.x + Tailwind CSS v4. All content is in Spanish (lang="es").

**Runtime:** Node.js >=22.12.0  
**Deployment:** Cloudflare Pages

## Commands

```bash
npm run dev          # Dev server at localhost:4321
npm run build        # Production build to ./dist/
npm run preview      # Preview production build locally
npm run astro check  # Type-check the project
```

No test runner or linter is configured.

## Architecture

Single-page site with section-based navigation (anchor links). One Astro page (`index.astro`) composes section components in order:

```
Layout.astro          # <html> shell: meta, fonts (Inter via Google Fonts), global.css import
  └─ index.astro
       ├─ Header      # Fixed nav bar with desktop/mobile menu, dark mode toggle, WhatsApp CTA
       ├─ Hero         # Full-height hero with headline and CTA buttons
       ├─ About        # Two-column: image placeholder + text with feature checklist
       ├─ Services     # 3-column grid of 6 service cards (aguacate, agrícola, certificación, análisis, asesoría, logística)
       ├─ Contact      # Two-column: contact info (WhatsApp, email, location) + form (no backend)
       └─ Footer       # Brand, quick links, social icons, copyright
```

## Key Conventions

- **Tailwind CSS v4** via `@import "tailwindcss"` in `src/styles/global.css` — no `tailwind.config` file; use Tailwind v4 CSS-first configuration
- **All styling is Tailwind utility classes** — no custom CSS files beyond `global.css` and scoped `<style>` blocks in Layout
- **Image optimization:** use `import { Image } from 'astro:assets'` with `format="webp"` for images in `src/assets/`; static files go in `public/`
- **Dark mode:** implemented via class strategy (`dark:` variants). Toggle logic is in `Header.astro` using `<script>` with `localStorage` persistence
- **No frameworks:** pure Astro components (`.astro` files), no React/Vue/Svelte. Client-side JS only via `<script>` tags in components
- **TypeScript:** strict mode (`astro/tsconfigs/strict`)
- **Brand colors:** green palette (`green-600` primary, `green-400` for dark mode accents, `green-50/100` for backgrounds)
- **WhatsApp number:** hardcoded as `573001234567` in Header and Contact components — update in both places if changed
