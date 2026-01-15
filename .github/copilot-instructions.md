# Copilot Instructions for TailAdmin Next.js Dashboard

## Project Overview
- **Frameworks:** Next.js 16 (App Router), React 19, TypeScript, Tailwind CSS v4
- **Purpose:** Admin dashboard template with modular UI components, authentication, charts, tables, and dark mode.
- **Structure:**
  - `src/app/`: Next.js app directory (routes, layouts, pages)
  - `src/components/`: Reusable UI and feature components (charts, tables, forms, etc.)
  - `src/context/`: React context for sidebar and theme
  - `src/hooks/`: Custom React hooks
  - `public/`: Static assets (images, icons)

## Key Patterns & Conventions
- **App Router:** Uses Next.js 16 App Router (`src/app/`). Route groups are in parentheses, e.g., `(admin)`, `(others-pages)`.
- **Layouts:** Each major section (admin, full-width, auth, error) has its own `layout.tsx` for context and UI composition.
- **Components:**
  - UI elements are grouped by type (e.g., `components/ui/alert/`, `components/charts/bar/`).
  - Feature modules (e.g., `auth/`, `calendar/`, `ecommerce/`) encapsulate related logic and UI.
- **Styling:** All styling is via Tailwind CSS utility classes. No CSS modules or styled-components.
- **State Management:** Uses React Context for sidebar and theme toggling. No Redux/MobX.
- **Authentication:** Auth forms and logic in `components/auth/`. Uses Next.js server actions and middleware for auth flows.
- **Charts:** Chart components use ApexCharts for React (see `components/charts/`).
- **Forms:** Form elements are modular and reusable (`components/form/`).


## Developer Workflows
- **Install dependencies:** `npm install` or `yarn install` (use `--legacy-peer-deps` if needed)
- **Start dev server:** `npm run dev` or `yarn dev`
- **Build for production:** `npm run build`
- **No custom test scripts provided by default.**
- **Peer dependency issues:** Use `--legacy-peer-deps` if you encounter install errors.

## Git Commit Conventions
- **All Git commit messages must follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary) specification.**
- Use commit types like `feat`, `fix`, `docs`, `refactor`, `chore`, etc., and provide a concise, meaningful description.
- Example: `feat(auth): add password reset flow`


## Integration & Extensibility
- **Add new pages:** Place in `src/app/` using Next.js routing conventions.
- **Add new components:** Place in the relevant `components/` subfolder. Follow existing folder structure and naming.
- **Dark mode:** Handled via context and Tailwind dark classes. See `ThemeContext.tsx` and `ThemeToggleButton.tsx`.
- **Sidebar:** Controlled via `SidebarContext.tsx`.

## References
- See `README.md` for setup, changelog, and versioning.
- Example patterns: `src/components/charts/`, `src/components/form/`, `src/app/(admin)/layout.tsx`

---

**For AI agents:**
- Follow the modular structure and use Tailwind for all styling.
- Prefer composition and reuse of existing components.
- When in doubt, reference similar files in the same directory.
- Do not introduce new state management libraries or styling approaches.
