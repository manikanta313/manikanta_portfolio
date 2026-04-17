# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Artifacts

### Portfolio (`artifacts/portfolio`)
- **Type**: React + Vite, frontend-only (no backend)
- **Preview path**: `/`
- **Purpose**: Personal portfolio for Veligatla Venkata Manikanta — Social Media Manager / Content Creator
- **Theme**: Dark (#0D0D0D), coral-red accent, Inter/Poppins fonts
- **Key dependencies**: framer-motion, react-intersection-observer, react-icons, lucide-react
- **Profile image**: `artifacts/portfolio/src/assets/images/portrait.png` (AI-generated, replace with real photo)
- **Portfolio images**: `artifacts/portfolio/src/assets/images/portfolio-1..4.png`
- **Personal info**: Manikanta's real name, experience, skills, contact details included

### API Server (`artifacts/api-server`)
- **Type**: Express 5 backend
- **Preview path**: `/api`

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
