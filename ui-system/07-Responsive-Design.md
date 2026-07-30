# EduCore Responsive Design System

## 1. Purpose

This document defines the responsive design principles, breakpoint strategy, and multi-device adaptation rules for the EduCore platform.

It ensures that school operations remain fluid and efficient across desktops, laptops, tablets, and mobile smartphones.

> **Responsive Axiom:** Responsive design is not about shrinking desktop screens; it is about adapting operational workflows to the user's immediate context and device capabilities.

---

## 2. Device Context & User Personas

EduCore is engineered with a tiered device strategy mapped to primary user roles:

```text
┌──────────────────────────────────────────────────────────┐
│                   Device Context Matrix                  │
├─────────┬──────────────────┬─────────────────────────────┤
│ Device  │ Primary Users    │ Core Operational Activities │
├─────────┼──────────────────┼─────────────────────────────┤
│ Desktop │ Administrators,  │ Deep reporting, financial   │
│         │ Bursars, Owners  │ configuration, data analysis│
├─────────┼──────────────────┼─────────────────────────────┤
│ Tablet  │ Academic Staff,  │ Classroom workflows, marks  │
│         │ Teachers         │ entry, attendance tracking  │
├─────────┼──────────────────┼─────────────────────────────┤
│ Mobile  │ Teachers, Field  │ Quick attendance logging,   │
│         │ Operations       │ notifications, lookup tasks │
└─────────┴──────────────────┴─────────────────────────────┘
```

---

## 3. Breakpoint Strategy & Viewport Scale

EduCore uses standardized system breakpoints controlled via design tokens:

- **Mobile:** `< 600px` (Stacked single-column layouts, slide-out drawer navigation).
- **Tablet:** `600px - 1024px` (Reduced navigation, simplified panels, touch-optimized).
- **Desktop:** `> 1024px` (Full multi-column workspaces, permanent persistent sidebar).

---

## 4. Layout Transformation & Component Adaptation

### Data Table Transformation
Tables must dynamically adjust information density based on available screen real estate:

| Viewport | Table Layout Strategy | Example Display |
| :--- | :--- | :--- |
| **Desktop** | Full multi-column grid | Name | Class | Age | Guardian | Status |
| **Tablet** | Reduced metadata columns | Name | Class | Status |
| **Mobile** | Card representation / Expandable rows | Card: John Doe (JSS2A - Active) + [View Details] |

### Form & Touch Optimization
- **Single-Column Flow:** Multi-column desktop forms collapse into single-column vertical flows on mobile.
- **Touch Targets:** Interactive elements must maintain minimum touch targets ($\ge 48	ext{px}$) with adequate spacing to prevent misclicks.

---

## 5. Responsive Anti-Patterns

Avoid these common layout failures:
- ❌ **Desktop-Only Interfaces:** Assuming every user has a wide monitor.
- ❌ **Horizontal Scrolling:** Forcing users to pan sideways to read tables or forms.
- ❌ **Hiding Core Actions:** Burying primary submission or approval buttons behind nested menus on mobile.
- ❌ **Mobile as an Afterthought:** Treating small screens as unstyled fallback states.

---

## 6. AI Agent Responsive Guardrails

When generating or auditing UI components and pages, AI agents must verify:
- [ ] **Multi-Device Coverage:** Does the component specify behavior for Desktop, Tablet, and Mobile?
- [ ] **Table Degradation:** If a `DataTable` is used, does it provide a clean mobile card fallback?
- [ ] **Touch Target Compliance:** Are button and link sizes adequate for touch interaction?
- [ ] **Contextual Flow:** Is the primary workflow optimized for the user's likely device context?
