# Copilot Instructions for AI Agents

## Project Overview
- **Framework**: Nuxt 4 with TypeScript, using compatibility version 4
- **UI Library**: shadcn-vue with reka-ui as the base component library
- **Styling**: Tailwind CSS v4 with CSS variables, OKLCH color space, and zinc base colors
- **Architecture**: File-based routing in `app/pages/`, components in `app/components/ui/`
- **Package Manager**: pnpm (preferred), with overrides for rolldown-vite

## Key Dependencies & Modules
- **Core**: `nuxt@^4.1.0`, `vue@^3.5.16`, `shadcn-nuxt@2.2.0`
- **UI**: `reka-ui@^2.3.1`, `lucide-vue-next@^0.515.0`, `class-variance-authority@^0.7.1`
- **Styling**: `@tailwindcss/vite@^4.1.10`, `tailwind-merge@^3.3.1`, `clsx@^2.1.1`
- **Modules**: `@nuxt/eslint`, `@nuxt/fonts`, `@nuxt/icon`, `@nuxt/image`, `@nuxt/scripts`, `@nuxt/test-utils`
- **Forms**: `@vee-validate/zod@^4.15.1`, `zod@^4.1.3`
- **Utilities**: `@vueuse/core@^13.7.0`, `@unovis/vue@^1.6.0`, `@tanstack/vue-table@^8.21.3`

## Key Workflows
- **Install dependencies**: `pnpm install` (preferred), or `npm/yarn/bun` as alternatives
- **Start dev server**: `pnpm dev` (runs `nuxt dev`)
- **Build for production**: `pnpm build` (runs `nuxt build`)
- **Generate static site**: `pnpm generate` (runs `nuxt generate`)
- **Preview production build**: `pnpm preview` (runs `nuxt preview`)
- **Post-install**: `pnpm install` automatically runs `nuxt prepare`

## Project Structure & Patterns
- **Pages**: File-based routing in `app/pages/` (e.g., `index.vue` → `/`)
- **Components**: shadcn pattern in `app/components/ui/` with folder structure:
  ```
  app/components/ui/button/
    Button.vue
    index.ts (exports component and variants)
  ```
- **Component Variants**: Use `class-variance-authority` with `cva()` function in index.ts files
- **Styling**: CSS variables in `app/assets/css/tailwind.css` with OKLCH colors and dark mode support
- **Utilities**: `cn()` function in `app/lib/utils.ts` combines `clsx` and `tailwind-merge`
- **TypeScript**: Strict typing with path aliases (`@/*` → `./app/*`)
- **Icons**: Lucide icons via `@nuxt/icon` module

## Component Architecture
- **Base Components**: Built on reka-ui primitives with shadcn styling
- **Variant System**: Each component has variants defined in `index.ts` using `cva()`
- **Props Interface**: Extends reka-ui `PrimitiveProps` with variant and size options
- **Styling**: Uses `cn()` utility to merge Tailwind classes with component variants
- **Example**: Button component in `app/components/ui/button/` with variants: default, destructive, outline, secondary, ghost, link

## Conventions & Integration
- **Component Imports**: Use path aliases (`@/components/ui/button` → `app/components/ui/button`)
- **shadcn Configuration**: "new-york" style, TypeScript enabled, CSS variables, no prefix
- **Color System**: OKLCH color space with semantic color variables (primary, secondary, etc.)
- **Dark Mode**: CSS variables automatically switch based on `.dark` class
- **Animation**: Uses `tw-animate-css` for additional animations
- **Forms**: VeeValidate with Zod schemas for form validation
- **Tables**: TanStack Vue Table for data tables
- **Charts**: Unovis Vue for data visualization

## Examples
- **Adding a new shadcn component**: Use `npx shadcn-vue@latest add <component>` then move to `app/components/ui/`
- **Creating component variants**: Define in `index.ts` using `cva()` with variants object
- **Using CSS variables**: Reference `--primary`, `--background`, etc. in Tailwind classes
- **Dark mode styling**: Use `dark:` prefix for dark mode variants

## References
- `README.md`: Basic setup and run instructions
- `nuxt.config.ts`: Nuxt modules and shadcn configuration
- `components.json`: shadcn-vue configuration and aliases
- `app/components/ui/button/`: Complete shadcn component pattern example
- `app/assets/css/tailwind.css`: CSS variables and theme configuration
- `app/lib/utils.ts`: Utility functions for class merging

---

Keep instructions concise and project-specific. When in doubt, follow the shadcn-vue documentation and existing component patterns in `app/components/ui/`.
