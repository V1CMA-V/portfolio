# Portfolio Project - Copilot Instructions

## Tech Stack & Architecture

This is an **Astro 5** static portfolio site using **Tailwind CSS v4** (with Vite plugin) and TypeScript. Language: Spanish (UI text and comments).

Key dependencies:

- `pnpm` as package manager
- `@fontsource/poppins` for typography
- Astro's strict TypeScript config

## Project Structure & Patterns

### Component Organization

- **Layouts** ([src/layouts/](src/layouts/)): Base HTML structure. `Layout.astro` includes Navbar, Footer, and global metadata
- **Sections** ([src/sections/](src/sections/)): Large page sections (Hero, Works, Skills, Phrase, Footer, Navbar)
- **Components** ([src/components/](src/components/)): Reusable UI (Card, CardProjects, Tabs, titleSection)
- **Assets/Icons** ([src/assets/icons/](src/assets/icons/)): SVG icons as `.astro` components (30+ tech stack icons)

### Path Aliases

Always use `@/*` alias for imports: `import Layout from '@/layouts/Layout.astro'`

### Styling Conventions

- **Tailwind v4** with custom CSS theme in [src/styles/global.css](src/styles/global.css)
- Custom color palette using HSL CSS variables:
  - `--color-background` (dark): `hsl(0, 0%, 6%)`
  - `--color-primary` (blue): `hsl(220, 90%, 60%)`
  - `--color-secondary` (purple): `hsl(280, 80%, 65%)`
  - `--color-accent` (pink): `hsl(340, 85%, 60%)`
  - Text hierarchy: `text-primary`, `text-secondary`, `text-tertiary`, `text-muted`
- Custom utilities: `.shadow-text` for glowing text effects
- Styled scrollbar with primary color

### Component Patterns

1. **Props with TypeScript interfaces**: Always define `interface Props` in frontmatter

   ```astro
   interface Props {
     title: string
     description: string
   }
   const { title, description } = Astro.props
   ```

2. **Icon components**: SVG wrappers in `src/assets/icons/*.astro` - import and use as components

   ```astro
   import AstroIcon from '@/assets/icons/astro.astro'
   <AstroIcon />
   ```

3. **Client-side interactivity**: Use `<script is:inline>` for vanilla JS (see [Tabs.astro](src/components/Tabs.astro))
   - Initialize on both `DOMContentLoaded` and Astro page transitions
   - Check `document.readyState === 'loading'` before adding event listener

4. **Named slots**: Use for flexible content injection (e.g., `<slot name="icon" />` in Card.astro)

## Development Workflow

```bash
pnpm install       # Install dependencies
pnpm dev          # Dev server at localhost:4321
pnpm build        # Production build to ./dist/
pnpm preview      # Preview production build
```

## Content Management

- **Skills data**: Hardcoded arrays in [src/sections/Skills.astro](src/sections/Skills.astro) with `{ name, icon }` objects
- **Projects data**: Array in [src/sections/Works.astro](src/sections/Works.astro) with title, role, timeline, image, url_site
- **Hero section**: Image in `/public/me2.webp` (portrait photo)

## Adding New Content

### New Icon

1. Create `src/assets/icons/{name}.astro` with SVG markup
2. Import in Skills.astro or where needed
3. Use consistent class: `class="icon icon-tabler..."`

### New Section

1. Create in `src/sections/NewSection.astro`
2. Import and add to [src/pages/index.astro](src/pages/index.astro) within `<Layout>`
3. Wrap in `<section>` with responsive padding/spacing classes

### Styling Changes

- Edit custom variables in [src/styles/global.css](src/styles/global.css) `@theme` block
- Use semantic color tokens (`bg-primary`, `text-text-secondary`) not raw HSL values

## Spanish Language Notes

- UI text in Spanish: "Habilidades" (Skills), "Herramientas" (Tools), "Ver todos los proyectos" (View all projects)
- Meta tags use `lang="es"` in Layout.astro
- Comments can be in Spanish or English

## Design System

- Glassmorphism effects: `bg-background/20 backdrop-blur-sm`
- Hover transitions: `transition-colors duration-300`
- Rounded corners: `rounded-lg` (8px) or `rounded-full` for buttons
- Font: Poppins with `letter-spacing: 1px` baseline
- Large typography: Hero uses `text-7xl md:text-9xl`, background text at `text-[12rem]`

## Notes

- No testing framework configured
- No backend/API - fully static site
- Icons are local components, not from icon library
- Tailwind v4 uses `@theme` instead of v3's config file
