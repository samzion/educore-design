# EduCore Layout System

## 1. Purpose

This document defines the layout principles, structural patterns, and spatial hierarchy used throughout the EduCore platform.

It ensures that administrative, academic, and financial modules deliver a cohesive, workspace-oriented experience rather than a collection of disconnected admin screens.

> **Layout Axiom:** EduCore layouts are engineered for operational clarity and cognitive focus. Everything important is visible; everything unnecessary is removed.

---

## 2. Core Application Shell Architecture

The primary application layout is structured into three persistent functional tiers:

```text
┌──────────────────────────────────────────────────────────┐
│                Application Shell Layout                  │
├─────────────────┬────────────────────────────────────────┤
│ Sidebar Nav     │ Persistent navigation & role-based     │
│                 │ module access (`src/layouts/sidebar`). │
├─────────────────┼────────────────────────────────────────┤
│ Top Header      │ Institutional context, school session, │
│                 │ notifications & profile menu.          │
├─────────────────┼────────────────────────────────────────┤
│ Main Workspace  │ Spacious, focused content region       │
│                 │ (`PageHeader`, `FilterBar`, `Content`).│
└─────────────────┴────────────────────────────────────────┘
```

---

## 3. Sidebar Navigation & State Matrix

The sidebar provides access to major operational modules while adapting to viewport constraints:

```text
┌──────────────────────────────────────────────────────────┐
│                 Sidebar State Guidelines                 │
├─────────────┬─────────────────────┬──────────────────────┤
│ State       │ Viewport Target     │ Display Elements     │
├─────────────┼─────────────────────┼──────────────────────┤
│ Expanded    │ Desktop default     │ Icon + Text Label    │
├─────────────┼─────────────────────┼──────────────────────┤
│ Collapsed   │ Compact desktop     │ Icon Only (Tooltip)  │
├─────────────┼─────────────────────┼──────────────────────┤
│ Mobile      │ Viewports < 768px   │ Slide-out Drawer Nav │
```

---

## 4. Standard Page Composition Pattern

Every operational module view follows a strict vertical hierarchy to maintain predictable navigation:

```text
Page Container
├── Page Header (Title, Subtitle Context, Primary Action Button)
├── Filter & Action Bar (Optional search input, status filters, date range)
├── Main Workspace Content (DataTable, Grid, or Form Sections)
└── Supporting Information / Pagination Footers
```

---

## 5. Dashboard Composition & Anti-Patterns

Dashboards must answer **"What requires attention?"** rather than serving as card storage:

- **Summary Metrics:** High-level KPIs (Total Enrolled, Outstanding Fees, Active Assessments).
- **Action Items:** Pending approvals, unresolved flags, urgent tasks.
- **Recent Activity:** Audit log streams and recent system events.

> **Anti-Pattern Warning:** Avoid "card soup"—the practice of wrapping every individual metric and data point in arbitrary cards with excessive borders.

---

## 6. Spacing & Whitespace System

All layouts must strictly utilize the EduCore design token spacing scale:
- **Whitespace Principle:** Whitespace is an intentional design tool used to establish cognitive calm, hierarchy, and focus. Never fill empty space unnecessarily.
- **Token Compliance:** Zero inline magic numbers or random margins (`margin: 17px`); use spacing tokens (`spacing(2)`, `spacing(4)`).

---

## 7. AI Agent Layout Guardrails

Before generating a new page or workspace layout, AI agents and engineers must verify:
- [ ] **Pattern Match:** Does this page follow the standard `PageHeader` $ightarrow$ `FilterBar` $ightarrow$ `DataTable` structure?
- [ ] **Role Scope:** Does the layout reflect the appropriate user role (Administrator vs. Teacher vs. Bursar)?
- [ ] **Token Alignment:** Are all padding and margin dimensions derived from design system spacing tokens?
- [ ] **Clarity & Focus:** Is the primary user action clearly visible at the top-right of the page header?
