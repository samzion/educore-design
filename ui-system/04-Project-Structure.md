# EduCore Frontend Project Structure

## 1. Purpose

This document defines the repository organization, folder taxonomy, dependency flow, and bounded-context alignment for the EduCore frontend application (`educore-frontend`).

It establishes structural guardrails to ensure that the codebase remains maintainable, feature-oriented, and scalable as EduCore expands from a single-school application to a multi-tenant SaaS platform.

> **Architecture Axiom:** The frontend directory is organized around product capabilities and domain boundaries—not technical file types. Features own their components, hooks, services, and types.

---

## 2. Master Repository Layout

```text
educore-frontend/
└── src/
    ├── app/          # Next.js App Router (Routes, Pages, Layout framing, Providers)
    ├── features/     # Domain Bounded Contexts (Feature-specific logic & UI)
    ├── components/   # System & Foundation UI Components (Domain-agnostic Layer 1 & 2)
    ├── layouts/      # Application shells (Dashboard, Auth, Workspace layouts)
    ├── services/     # Shared HTTP infrastructure, API client & interceptors
    ├── hooks/        # Shared technical React hooks (useDebounce, useMediaQuery)
    ├── stores/       # Application UI state (Auth session, theme, notifications)
    ├── lib/          # Utilities, formatters, date helpers, validation tools
    ├── types/        # Global TypeScript interfaces & API envelope contracts
    ├── styles/       # Design System tokens, MUI theme configuration & globals
    └── config/       # Environment variables & runtime application flags
```

---

## 3. Dependency Flow & Architecture Hierarchy

To prevent circular dependencies and spaghetti code, imports must strictly flow downward:

```text
┌──────────────────────────────────────────────────────────┐
│                    Dependency Hierarchy                  │
├─────────────────┬────────────────────────────────────────┤
│ 1. App Router   │ `src/app/`                             │
│                 │ (Routes, Page composition)             │
├─────────────────┼────────────────────────────────────────┤
│ 2. Feature Tiers│ `src/features/*`                       │
│                 │ (Student, Finance, Assessment, etc.)   │
├─────────────────┼────────────────────────────────────────┤
│ 3. Shared Tiers │ `src/components/`, `src/services/`,    │
│                 │ `src/lib/`, `src/hooks/`               │
└─────────────────┴────────────────────────────────────────┘
```

> **Strict Rule:** Shared UI components (`src/components/`) and utilities (`src/lib/`) must **NEVER** import from feature modules (`src/features/*`).

---

## 4. Feature Bounded Context Anatomy

Each business domain resides inside `src/features/{feature-name}` and owns its technical assets:

```text
src/features/student/
├── components/     # Feature UI (StudentTable, GuardianCard, EnrollmentForm)
├── hooks/          # Domain hooks (useStudents, useStudentEnrollment)
├── services/       # Domain API client calls (studentService.ts)
├── schemas/        # Zod validation schemas (studentSchema.ts)
├── types/          # Domain TypeScript interfaces (student.ts)
├── constants/      # Feature flags & static domain lists
└── index.ts        # Public API export barrel file
```

### Feature Boundary Rules
Features must not directly import internal modules from sibling features:

```text
❌ PROHIBITED:
import { InternalCard } from '@/features/student/components/InternalCard'; // Inside finance module

✅ APPROVED:
import { SharedStudentSummary } from '@/components/domain/SharedStudentSummary';
```

---

## 5. State Management & API Client Rules

```text
┌──────────────────────────────────────────────────────────┐
│               State & Data Layer Strategy                │
├──────────────────┬───────────────────────────────────────┤
│ Server State     │ Managed via React Query / SWR.        │
│                  │ (Do not store entities in Redux/Zustand│
│                  │ stores like `students[]` or `fees[]`).│
├──────────────────┼───────────────────────────────────────┤
│ Application UI   │ Managed via Zustand / Context stores. │
│ State            │ (Auth token, sidebar collapse state,  │
│                  │ active theme mode, toast stack).      │
├──────────────────┼───────────────────────────────────────┤
│ Service Client   │ Feature APIs call `src/services/apiClient.ts`│
│                  │ with interceptors for auth tokens.    │
└──────────────────┴───────────────────────────────────────┘
```

---

## 6. AI Agent Repository Guidelines

When creating or refactoring code, AI agents and engineers must adhere to the following checklist:

- [ ] **Feature Placement:** Does this file belong inside a feature module (`src/features/`) or a shared directory (`src/components/`)?
- [ ] **Export Control:** Does the feature export public components via `index.ts`?
- [ ] **Dependency Guard:** Is a shared component importing from a feature module? (Prohibited)
- [ ] **Server State:** Is domain data being improperly cached in global Zustand stores instead of server state queries?
- [ ] **Naming Standards:** Are folder and file names strictly kebab-case/camelCase according to convention?

---

## 7. Architectural Summary

1. **Domain Cohesion:** Feature folders mirror business capabilities, maintaining parity with Spring Boot microservices/bounded contexts.
2. **Clean Separation:** UI Primitives $ightarrow$ System Components $ightarrow$ Feature Modules $ightarrow$ App Routes.
3. **Predictable Scalability:** Clear file boundaries allow teams and AI agents to add features without triggering cross-module regression.
