# Architecture Decisions

This document records the key technical decisions made during Verso's development. Each decision includes the context, the choice made, and the reasoning.

---

## ADR-001 : Monorepo structure

**Date:** April 2026
**Status :** Accepted

**Context :** Verso has three deployment targets (API, web app, mobile app) that share TypeScript types, enums, validation schemas, and business logic. Keeping them in separate repos would require publishing shared packages to a registry and manually syncing versions across repos.

**Decision :** Use a single monorepo with pnpm workspaces for package linking and Turborepo for task orchestration and caching.

**Structure :**
- `apps/` : Deployable applications (API, web, mobile)
- `packages/` : Shared libraries (types, validators, logic)

**Consequences :**
- Single `git clone` to get the full project
- Atomic commits when changing shared types
- One CI pipeline for all apps

---

## ADR-002 : Single shared package (for now)

**Date :** April 2026
**Status :** Accepted, will be revisited

**Context :** The shared code could be split into multiple packagesfrom day one. However, the exact boundaries between these packages are unclear until more code exists.

**Decision :** Start with a single `packages/shared` package with a clean barrel export. Split into multiple packages when React Native is introduced, because mobile builds cannot afford to pull in backend-only dependencies.

**Consequences :**
- Simpler setup during first phases
- Must be disciplined about not importing backend-only dependencies into shared

---

## ADR-003 : MIT license

**Date :** April 2026
**Status :** Accepted

**Context :** Verso is built in public and will be monetized as a freemium SaaS. The competitive moat is in the cross-media knowledge graph data and the deepening content corpus, not in the application code.

**Decision :** MIT license. Maximum openness for the build-in-public approach, no friction for potential contributors.

**Consequences :**
- Anyone can fork and use the code
- The data layer (knowledge graph, deepening cache) is the real moat
- Consistent with the build-in-public positioning

---

## ADR-004 : Tier-based ranking instead of numerical scores

**Date :** April 2026
**Status :** Accepted

**Context :** Ranking produces more reliable and less biased data than rating on numerical scales.

**Decision :** Replace numerical scores with a tier system (S/A/B/C/D/F) using relative positioning and optional pairwise comparison.

**Consequences :**
- No star rating anywhere in the app
- Imported ratings from external sources are converted to suggested tiers
- Tiers are never exported as numbers. They are qualitative, not quantitative

---

*This document will grow with each architectural decision. Format inspired by [Architecture Decision Records (ADR)](https://adr.github.io/).*
