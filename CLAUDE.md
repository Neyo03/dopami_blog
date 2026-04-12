# CLAUDE.md — ADHD Blog (Astro + Strapi)

## Project Overview
Bilingual (FR/EN) blog about ADHD built with Astro 5 (SSG) + Strapi 5 (headless CMS).

## Tech Stack
- **Frontend**: Astro 5, Tailwind CSS 4, TypeScript
- **CMS**: Strapi 5, PostgreSQL, Docker
- **Hosting**: Vercel (front) + Docker/Portainer (Strapi)
- **Comments**: Giscus
- **Newsletter**: Buttondown or Listmonk

## Architecture
- `strapi/` — Strapi 5 CMS with Docker Compose
- `astro/` — Astro 5 static frontend

## Conventions
- All code in **English** (variables, functions, comments)
- Explanations and discussions in **French**
- Follow **SOLID** principles
- One component = one file, single responsibility
- Strapi types mirrored in `src/lib/types.ts`
- i18n: UI strings in `src/i18n/ui.ts`, content from Strapi `?locale=` param
- Route pattern: `/{lang}/blog/{slug}`

## Collaboration Rules
1. Always attempt implementation first before asking Claude
2. Ask Claude about **specific gaps**, not "write everything for me"
3. Claude should use hints/questions before giving full solutions
4. If stuck for >15 min, then ask for direct help
5. Review all generated code — understand every line

## File Naming
- Astro components: `PascalCase.astro`
- TypeScript modules: `kebab-case.ts`
- Pages: `kebab-case.astro` or `[param].astro`

## Key Commands
```bash
# Strapi
cd strapi && docker compose up -d

# Astro dev
cd astro && npm run dev

# Astro build
cd astro && npm run build
```
