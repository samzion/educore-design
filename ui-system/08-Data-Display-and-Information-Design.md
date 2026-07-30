# EduCore Data Display and Information Design

## 1. Purpose

This document defines the principles, patterns, and operational standards for presenting, organizing, and interacting with complex school data across the EduCore platform.

It establishes rules for tables, lists, dashboards, search, filtering, sorting, pagination, and data states.

> **Data Axiom:** EduCore transforms raw school data into meaningful operational information. The system must never merely store data; it must help educators and administrators understand what is happening, what requires attention, and what action to take.

---

## 2. Information Design Philosophy

To maximize operational efficiency, information displays must adhere to three core pillars:

```text
┌──────────────────────────────────────────────────────────┐
│              Information Design Hierarchy                │
├─────────────────┬────────────────────────────────────────┤
│ Clarity over    │ Prioritize important and useful data   │
│ Density         │ over raw field dumps.                  │
├─────────────────┼────────────────────────────────────────┤
│ Context before  │ Establish "What am I looking at?"      │
│ Detail          │ before exposing granular fields.       │
├─────────────────┼────────────────────────────────────────┤
│ Action-Oriented │ Connect data directly to workflows     │
│ Data            │ (e.g., "23 Pending → Review now").     │
└─────────────────┴────────────────────────────────────────┘
```

---

## 3. Data Table Standards & Contract

Tables are core workhorses for students, attendance, assessments, and payments. Every operational table must support:

1. **Global Search:** Fast, forgiving search supporting natural queries (e.g., student name, admission number, or class).
2. **Multi-Parameter Filtering:** Contextual filters (status, date range, class) positioned above the grid.
3. **Column Sorting:** Ascending/descending sorting for key attributes (name, date, amount).
4. **Pagination Controls:** Configurable page sizing for large datasets.
5. **Contextual Row Actions:** Inline triggers (`View`, `Edit`, `Approve`, `Archive`).
6. **Robust Data States:** Meaningful empty states with calls-to-action, skeleton loaders, and error recovery views.

---

## 4. Dashboard & Metric Presentation

Dashboards are operational command centers, not random collections of widgets.

- **Metric Design Rule:** Every metric card must present **Value** (e.g., 1,250 Students), **Context** (+8% from last session), and an **Action** (View Enrollment).
- **Chart Restraint:** Use charts exclusively for trends, comparisons, and patterns—never for simple numbers or decorative fill.
- **Anti-Pattern Warning:** Avoid "card soup" and unmonitored metric sprawl.

---

## 5. Financial & Assessment Data Rules

### Financial Data Clarity
- Must clearly expose **amounts**, **payment status**, **due dates**, and **outstanding balances**.
- Never obscure payment failures or overdue statuses.

### Assessment Workflow Visibility
- Scores must be paired with clear workflow states (`Draft`, `Submitted`, `Approved`, `Published`).
- Approval timelines must be transparent to academic leads.

---

## 6. AI Agent Data Design Guardrails

Before generating data-heavy screens or tables, AI agents must verify:
- [ ] **User Goal:** What specific decision is this screen supporting?
- [ ] **Information Hierarchy:** Are secondary and raw database fields appropriately hidden or expandable?
- [ ] **State Handling:** Do empty, loading, and error states provide clear paths for recovery?
- [ ] **Mobile Adaptation:** Does the data table degrade cleanly into mobile card lists?
