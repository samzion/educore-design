# EduCore Component Strategy

## 1. Purpose

This document defines the architectural guidelines, ownership boundaries, MUI customization rules, and reuse principles for frontend components in EduCore.

It ensures that both developers and AI collaborators maintain a clean, maintainable, and scalable component hierarchy.

> **Strategy Axiom:** Frontend components in EduCore reflect the same intentional architecture as the backend services. They enforce strict layer boundaries, clean APIs, and clear bounded context ownership.

---

## 2. Component Hierarchy & Architectural Layers

EduCore components are structured into four functional tiers to prevent architectural decay:

```text
┌──────────────────────────────────────────────────────────┐
│                   Component Architecture                 │
├─────────────────┬────────────────────────────────────────┤
│ Layer 4: Pages  │ Compose complete application views     │
│                 │ (`StudentManagementPage`).             │
├─────────────────┼────────────────────────────────────────┤
│ Layer 3: Feature│ Business-domain-aware UI components    │
│                 │ (`StudentProfileCard`, `GuardianList`).│
├─────────────────┼────────────────────────────────────────┤
│ Layer 2: System │ Reusable application-level patterns    │
│                 │ (`DataTable`, `FilterBar`, `PageHeader`).│
├─────────────────┼────────────────────────────────────────┤
│ Layer 1: Foundation wrappers around MUI primitives and │
│                 │ design tokens (`PrimaryButton`, `Icon`).│
└─────────────────┴────────────────────────────────────────┘
```

---

## 3. Layer Definitions & Guidelines

### Layer 1: Foundation Components
- **Role:** Atomic wrappers around Material UI primitives and EduCore Design System tokens.
- **Rules:** Zero business logic. Must be domain-agnostic and usable anywhere.
- **Example:** `<PrimaryButton>`, `<SurfaceCard>`, `<BaseTypography>`.

### Layer 2: System Components
- **Role:** Standardized product UI patterns shared across the entire application shell.
- **Rules:** Understands application UX conventions (tables, modals, status chips), but zero specific domain knowledge.
- **Example:** `<DataTable />` (Good) vs. `<StudentPaymentTable />` (Bad for Layer 2).

### Layer 3: Feature Components
- **Role:** Business-specific UI elements scoped within feature modules (`features/student/`, `features/finance/`).
- **Rules:** Understands domain data, feature workflows, and entity schemas.
- **Example:** `<ScoreEntryGrid>`, `<ApprovalTimeline>`, `<GuardianList>`.

### Layer 4: Page Components
- **Role:** Complete operational views coordinating layout, workflows, and data fetching.
- **Rules:** Delegates visual representation to components; delegates business rules to custom hooks and services.
- **Example:** `<AssessmentWorkspacePage />`, `<FinanceDashboardPage />`.

---

## 4. MUI Customization & Token Integration

EduCore leverages MUI for accessibility primitives, base behaviors, and layout infrastructure while superimposing the EduCore Design System layer.

```text
┌──────────────────────────────────────────────────────────┐
│              MUI Anti-Pattern vs. Standard               │
├───────────────────────────────────┬──────────────────────┤
│ ❌ PROHIBITED AD-HOC STYLING      │ ✅ APPROVED TOKEN    │
├───────────────────────────────────┼──────────────────────┤
│ `<Button sx={{ bg: '#123456',     │ `<PrimaryButton>` or │
│   borderRadius: '20px' }}>`       │ theme-configured     │
│                                   │ MUI tokens.          │
└───────────────────────────────────┴──────────────────────┘
```

---

## 5. Separation of Concerns & Data Flow

Components must delegate business logic, state calculations, and asynchronous requests to custom hooks and service layers:

```text
Component UI View ──> Custom Hook ──> Service Layer ──> Backend API
(AssessmentScore)   (useScores)      (scoreService)    (Spring Boot)
```

---

## 6. Component Creation & AI Agent Rules

Before creating a component, AI agents and developers must execute the Component Evaluation Gate:

```text
┌──────────────────────────────────────────────────────────┐
│               Component Evaluation Gate                  │
├──────────────────────────────────────────────────────────┤
│ 1. Does this pattern already exist in Layer 1 or 2?      │
│ 2. Can an existing component be extended via props?      │
│ 3. Will this component repeat across features?           │
└──────────────────────────────────────────────────────────┘
```

> **AI Restriction:** AI agents must never introduce duplicate primitives (e.g., `NewButton`, `CustomModal`, `SpecialTable`) without architectural justification.

---

## 7. Quality Checklist

Before merging component code:
- [ ] Adheres to Layer boundaries (Foundation $ightarrow$ System $ightarrow$ Feature $ightarrow$ Page).
- [ ] Maps directly to EduCore Design Tokens (`var(--color-*)`).
- [ ] Meets WCAG AA accessibility standards.
- [ ] Exposes a clean, object-oriented API contract.
- [ ] Separates UI rendering from hooks and services.
