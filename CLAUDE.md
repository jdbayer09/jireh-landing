# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Jireh Exportaciones y Asesorias S.A.S landing page built with Astro 6.x for optimal page load performance. The site showcases company information, services, and contact details for Jireh, a company specializing in exporting Colombian agricultural products with a focus on avocados (aguacate).

**Brand colors:** Green (verde) - reflecting the agricultural and avocado business

**Runtime:** Node.js >=22.12.0

**Deployment:** Cloudflare Pages

## Commands

```bash
npm install          # Install dependencies
npm run dev          # Start dev server at localhost:4321
npm run build        # Build production site to ./dist/
npm run preview      # Preview build locally before deploying
npm run astro add    # Add Astro integrations
npm run astro check  # Type check the project
```

## Architecture

- `src/pages/` - Astro pages (file-based routing)
- `src/components/` - Reusable Astro components
- `src/layouts/` - Page layout components
- `public/` - Static assets served directly
- `src/assets/` - Imported assets (processed by Astro)

## Configuration

- `astro.config.mjs` - Astro configuration
- `tsconfig.json` - TypeScript config (extends `astro/tsconfigs/strict`)

## VS Code

- Astro VS Code extension recommended (`astro-build.astro-vscode`)
- Launch config available for running dev server from editor
