# Copilot Instructions for AI Agents

## Project Overview
- This is a Nuxt 3 minimal starter using TypeScript, Tailwind CSS, and shadcn/ui components.
- Main app code is in `app/` (pages, components, assets, utils).
- UI components follow the shadcn/ui pattern, organized under `app/components/ui/` (e.g., `button/Button.vue`).
- Server-side logic (if any) is in `server/`.

## Key Workflows
- **Install dependencies:** Use `pnpm install` (preferred), or `npm/yarn/bun` as alternatives.
- **Start dev server:** `pnpm dev` (or `npm run dev`, etc.).
- **Build for production:** `pnpm build`.
- **Preview production build:** `pnpm preview`.

## Project Structure & Patterns
- **Pages:** Use file-based routing in `app/pages/` (e.g., `index.vue` for `/`).
- **Components:** Place reusable UI in `app/components/ui/`. Each component may have its own folder and `index.ts` for exports.
- **Styling:** Tailwind CSS is configured in `app/assets/css/tailwind.css`.
- **Utilities:** Shared logic in `app/lib/utils.ts`.
- **TypeScript:** Project uses strict typing via `tsconfig.json`.
- **Nuxt Config:** Main config in `nuxt.config.ts`.

## Conventions & Integration
- **Component imports:** Use path aliases as configured in `tsconfig.json`.
- **Follow shadcn/ui conventions** for component structure and styling.
- **No custom test or lint scripts** are defined; use standard Nuxt/TypeScript/Tailwind workflows.
- **External docs:** Refer to [Nuxt docs](https://nuxt.com/docs/getting-started/introduction) for framework details.

## Examples
- To add a new button variant, create a new file in `app/components/ui/button/` and export it in `index.ts`.
- To add a new page, create a `.vue` file in `app/pages/`.

## References
- `README.md`: Basic setup, build, and run instructions.
- `nuxt.config.ts`: Nuxt and module configuration.
- `app/components/ui/`: shadcn/ui component pattern reference.

---

Keep instructions concise and project-specific. When in doubt, follow the structure and patterns in the `app/` directory and shadcn/ui documentation.
