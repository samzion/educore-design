# EduCore Color Palette Exploration

## 1. Purpose

This document records the evaluation framework, design criteria, candidate directions, and technical token mapping for the EduCore color palette.

It bridges brand strategy and frontend execution to ensure every color decision is functional, accessible, and scalable.

```text
┌──────────────────────────────────────────────────────────┐
│                    Palette Lifecycle                     │
├─────────────────┬────────────────────────────────────────┤
│ Brand Identity  │ Strategic positioning & visual tone    │
├─────────────────┼────────────────────────────────────────┤
│ Design System   │ Structured color tokens & contrast gates│
├─────────────────┼────────────────────────────────────────┤
│ Frontend Theme  │ CSS Variables (`var(--color-*)`) & MUI │
└─────────────────┴────────────────────────────────────────┘
```

---

## 2. Selection & Evaluation Criteria

Candidate palettes must pass five quality gates before adoption:

```text
┌──────────────────────────────────────────────────────────┐
│                   Evaluation Criteria                    │
├───────────────┬──────────────────────────────────────────┤
│ Brand Fit     │ Communicates institutional trust,        │
│               │ operational clarity, and intelligence.   │
├───────────────┼──────────────────────────────────────────┤
│ UI Fitness    │ Maintains readability in dense data      │
│               │ tables, forms, and analytical charts.    │
├───────────────┼──────────────────────────────────────────┤
│ Accessibility │ Exceeds WCAG AA (4.5:1 text contrast ratio)│
│               │ across all interactive states.           │
├───────────────┼──────────────────────────────────────────┤
│ Longevity     │ Avoids trendy gradients and ephemeral    │
│               │ color shifts; stays relevant for years.  │
├───────────────┼──────────────────────────────────────────┤
│ Distinction   │ Rejects generic "school blue" and dated   │
│               │ enterprise ERP gray palettes.            │
└───────────────┴──────────────────────────────────────────┘
```

---

## 3. Strategic Visual Directions

Three distinct visual directions were explored during the design phase:

```text
┌──────────────────────────────────────────────────────────┐
│                 Exploration Directions                   │
├─────────────────┬────────────────────────────────────────┤
│ Direction A     │ Trust + Stability                      │
│                 │ Deep Indigo (`#1E3A8A`) & Slate.       │
│                 │ Character: Serious, reliable, stable.  │
├─────────────────┼────────────────────────────────────────┤
│ Direction B     │ Intelligence + Growth                  │
│                 │ Cobalt (`#2563EB`) & Emerald Accents.  │
│                 │ Character: Modern, active, progressive.│
├─────────────────┼────────────────────────────────────────┤
│ Direction C     │ Premium Productivity Platform          │
│ (SELECTED)      │ Deep Slate Navy (`#0F172A`) & Crisp   │
│                 │ High-Contrast Neutral Surfaces.        │
│                 │ Character: Refined, calm, high-density.│
└─────────────────┴────────────────────────────────────────┘
```

---

## 4. Final Selected Palette & Hex Specifications

Direction C was selected as the foundational system palette.

### Brand Anchor Colors
- **Primary Brand Navy:** `#0F172A` — Used for main navigation, primary actions, and brand anchors.
- **Secondary Cobalt Accent:** `#1D4ED8` — Used for active selection highlights, secondary buttons, and focus rings.
- **Subtle Slate Highlight:** `#38BDF8` — Used for analytical metric callouts and informational badges.

### Neutral Surface System (80%+ UI Surface Area)
- **Canvas / App Background:** `#F8FAFC` (`slate-50`)
- **Surface / Card Background:** `#FFFFFF` (`white`)
- **Elevated / Overlay Surface:** `#FFFFFF` (`white` with `shadow-md`)
- **Primary Body Text:** `#0F172A` (`slate-900`) — Contrast ratio > 15:1
- **Secondary Label Text:** `#475569` (`slate-600`) — Contrast ratio > 7:1
- **Muted Placeholder Text:** `#94A3B8` (`slate-400`)
- **Borders & Table Lines:** `#E2E8F0` (`slate-200`)

### Semantic System Feedback Palette
```text
┌──────────────────────────────────────────────────────────┐
│                  Semantic Hex Values                     │
├─────────────┬───────────┬────────────────────────────────┤
│ Success     │ `#15803D` │ Payments confirmed, approved.  │
├─────────────┼───────────┼────────────────────────────────┤
│ Warning     │ `#B45309` │ Pending review, unverified.    │
├─────────────┼───────────┼────────────────────────────────┤
│ Destructive │ `#B91C1C` │ Failed actions, errors.        │
├─────────────┼───────────┼────────────────────────────────┤
│ Info        │ `#1D4ED8` │ System guidance, tooltips.     │
└─────────────┴───────────┴────────────────────────────────┘
```

---

## 5. Screen Testing Matrix

Candidate colors were validated across high-density operational views:

| Tested Interface View | Primary Validation Focus | Outcome |
| :--- | :--- | :--- |
| **Authentication Shell** | Brand confidence, trust, clean inputs | Passed |
| **Executive Dashboard** | Scannable metrics, non-fatiguing surfaces | Passed |
| **Data Grid (Table)** | Row highlight contrast, cell line subtle boundary | Passed |
| **Fee Collection Form** | Clear error indicators, prominent submit CTA | Passed |
| **Result Verification** | Distinct success/warning status chips | Passed |

---

## 6. Token & Theme Implementation Mapping

Selected hex values are exported directly into frontend theme tokens:

```text
Brand Spec               Design Token                CSS Variable / Code
Primary Navy (#0F172A) ──> color.primary.main  ──> var(--color-primary-main)
Canvas (#F8FAFC)       ──> color.bg.canvas     ──> var(--color-bg-canvas)
Success (#15803D)      ──> color.status.success ──> var(--color-status-success)
```

---

## 7. Architectural Summary

1. **Direction C Approved:** Deep Slate Navy (`#0F172A`) delivers a calm, high-contrast, professional workspace.
2. **Data-Dense Optimization:** Neutral surfaces prevent visual fatigue during prolonged use by administrative staff.
3. **Accessibility Enforced:** All selected combinations exceed WCAG AA 4.5:1 contrast ratios.
4. **Direct Code Binding:** Hex values map straight to CSS variables for UI component consumption.
