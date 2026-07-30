# EduCore Component Library

## 1. Purpose

This document defines the standardized component inventory, interaction patterns, and operational rules for the EduCore platform.

It ensures UI consistency across administrative, academic, and financial modules, preventing redundant component creation by developers and AI agents.

> **Library Axiom:** The EduCore Component Library is an enterprise toolkit designed for high-density information processing, rapid comprehension, and predictable accessibility.

---

## 2. Component Taxonomy & Architectural Hierarchy

```text
┌──────────────────────────────────────────────────────────┐
│                   Component Taxonomy                     │
├─────────────────┬────────────────────────────────────────┤
│ Foundation      │ MUI wrappers & Design System primitives│
│                 │ (`Box`, `Stack`, `Typography`, `Icon`).│
├─────────────────┼────────────────────────────────────────┤
│ Action & Form   │ Interactive controls & input fields    │
│                 │ (`PrimaryButton`, `TextField`, `Select`)│
├─────────────────┼────────────────────────────────────────┤
│ Data Display    │ Information structure & data grids     │
│                 │ (`DataTable`, `StatCard`, `Badge`).    │
├─────────────────┼────────────────────────────────────────┤
│ Feedback & State│ System notification & progress layers  │
│                 │ (`Alert`, `Toast`, `EmptyState`).      │
├─────────────────┼────────────────────────────────────────┤
│ Workflow UI     │ Multi-step process containers          │
│                 │ (`ApprovalFlow`, `Stepper`, `FilterBar`)│
└─────────────────┴────────────────────────────────────────┘
```

---

## 3. Action & Button Hierarchy

Action components must clearly indicate task priority and operational risk:

```text
┌──────────────────────────────────────────────────────────┐
│                 Action Button Hierarchy                  │
├──────────────┬────────────────────────┬──────────────────┤
│ Variant      │ Purpose                │ Example Use Case │
├──────────────┼────────────────────────┼──────────────────┤
│ Primary      │ Dominant page action   │ Save Student,    │
│              │ (Max 1 per view container) Submit Marks   │
├──────────────┼────────────────────────┼──────────────────┤
│ Secondary    │ Supporting actions     │ Filter Data,     │
│              │                        │ Export CSV       │
├──────────────┼────────────────────────┼──────────────────┤
│ Destructive  │ Irreversible or high-  │ Delete Record,   │
│              │ risk operations        │ Revoke Access    │
├──────────────┼────────────────────────┼──────────────────┤
│ Icon Button  │ Compact inline trigger │ Table row menu,  │
│              │                        │ Close modal      │
└──────────────┴────────────────────────┴──────────────────┘
```

---

## 4. Data Display & Operational Table Rules

### Standard `DataTable` Contract
The `DataTable` component is the workhorse of administrative workflows and must support six baseline capabilities:

1. **Server-Side Pagination:** Configurable page sizes (10, 25, 50, 100 rows).
2. **Column Sorting:** Visual indicators for ascending/descending states.
3. **Multi-Parameter Filtering:** Search input, status dropdowns, date range filters.
4. **State Handling:** Dedicated skeleton loading states and clear empty state indicators.
5. **Responsive Adaptation:** Transforms from full grid (Desktop) to card view (Mobile).
6. **Row Action Menus:** Contextual menu triggers for record modification.

---

## 5. Domain Status Badge System

Status badges pair color design tokens with explicit text labels to communicate operational resolution:

```text
┌──────────────────────────────────────────────────────────┐
│                  Status Badge Mapping                    │
├─────────────┬───────────┬────────────────────────────────┤
│ State       │ Token     │ Target Workflows               │
├─────────────┼───────────┼────────────────────────────────┤
│ Active/Paid │ Success   │ Tuition paid, student enrolled │
├─────────────┼───────────┼────────────────────────────────┤
│ Pending     │ Warning   │ Awaiting verification/review   │
├─────────────┼───────────┼────────────────────────────────┤
│ Failed/Over │ Destruct  │ Payment declined, expelled     │
├─────────────┼───────────┼────────────────────────────────┤
│ Draft       │ Neutral   │ Unsubmitted marks entry        │
└─────────────┴───────────┴────────────────────────────────┘
```

---

## 6. Feedback Lifecycle Pattern

Asynchronous user interactions must systematically cycle through three feedback layers:

```text
Async Trigger ──> Loading Skeleton / Spinner ──> Toast / Alert Banner State
(Form Submit)    (Disables user action)       (Success or Error summary)
```

---

## 7. Responsive Transformation Standard

Components must gracefully degrade across device viewports:

| Component | Desktop ($\ge 1024	ext{px}$) | Tablet ($768	ext{px} - 1023	ext{px}$) | Mobile ($< 768	ext{px}$) |
| :--- | :--- | :--- | :--- |
| **Data Table** | Full multi-column grid | Hidden low-priority columns | Stacked card list view |
| **Form Layout** | Multi-column grid layout | 2-Column form grid | Single column layout |
| **Filter Panel** | Inline horizontal filter bar | Collapsible filter drawer | Bottom sheet modal |

---

## 8. AI Agent Guardrails & Evaluation Checklist

Before introducing a new UI component, AI agents must evaluate against this checklist:

- [ ] **Existence Check:** Does a functional alternative exist in Layer 1 or Layer 2?
- [ ] **Composition Rule:** Can this UI be created by composing `DataTable`, `FormSection`, and `Card`?
- [ ] **Token Alignment:** Are all surface colors, text sizes, and radii using CSS token variables?
- [ ] **No Duplicate Primitives:** Prohibits creating files like `NewButton.tsx` or `CustomTable.tsx`.
