# EduCore Design Tokens

## 1. Purpose

Design tokens are the foundational, single-source-of-truth values for color, typography, spacing, radius, elevation, borders, and motion in EduCore.

They represent reusable design choices that bridge visual design and code. By replacing hardcoded hex codes, pixel margins, and custom CSS properties with semantic tokens, the system guarantees visual consistency across all modules and prevents component fragmentation.

> **Token Principle:** Hardcoded style values (e.g., `#3478db` or `margin: 24px`) are forbidden in component code. All visual properties must reference system tokens.

---

## 2. Token Architecture & Hierarchy

EduCore design tokens use a tiered abstraction hierarchy to separate raw value assignment from semantic context:

```text
┌──────────────────────────────────────────────────────────┐
│                      Design Tokens                       │
├─────────────────┬────────────────────────────────────────┤
│ Primitive Tokens│ Hard values (e.g., Gray-900, Blue-800) │
├─────────────────┼────────────────────────────────────────┤
│ Semantic Tokens │ Intent-based mappings (e.g., surface,  │
│                 │ text.primary, action.primary)          │
├─────────────────┼────────────────────────────────────────┤
│ Component Tokens│ Local variant aliases (e.g.,           │
│                 │ button.bg.primary)                     │
└─────────────────┴────────────────────────────────────────┘
```

---

## 3. Color System & Semantic Roles

Colors in EduCore communicate operational state, hierarchy, and affordance—never decoration.

```text
┌──────────────────────────────────────────────────────────┐
│                   Semantic Color Roles                   │
├───────────────┬──────────────────────────────────────────┤
│ Neutral       │ Dominates 80%+ of surfaces, text, and    │
│               │ layout borders for high legibility.      │
├───────────────┼──────────────────────────────────────────┤
│ Brand Primary │ Applied strictly to key CTAs, active     │
│               │ selection states, and brand anchors.     │
├───────────────┼──────────────────────────────────────────┤
│ Success       │ Positive state resolution (e.g., payment  │
│               │ confirmed, grade approved).              │
├───────────────┼──────────────────────────────────────────┤
│ Warning       │ Attention required (e.g., pending        │
│               │ review, unverified attendance).          │
├───────────────┼──────────────────────────────────────────┤
│ Destructive   │ Critical errors and permanent actions    │
│               │ (e.g., record removal, payment failure). │
└───────────────┴──────────────────────────────────────────┘
```

### Color Token Mapping

| Token Name | Semantic Purpose | Fallback Value |
| :--- | :--- | :--- |
| `color.bg.canvas` | Main application workspace background | `#F8FAFC` |
| `color.bg.surface` | Standard card and container surface | `#FFFFFF` |
| `color.bg.elevated` | Modals, command menus, dropdowns | `#FFFFFF` |
| `color.text.primary` | High-contrast body copy and headings | `#0F172A` |
| `color.text.secondary` | Contextual labels, metadata, subheadings | `#475569` |
| `color.text.muted` | Placeholders, disabled states, captions | `#94A3B8` |
| `color.border.subtle` | Layout dividers, table grid lines | `#E2E8F0` |
| `color.border.default` | Form input outlines, container boundaries | `#CBD5E1` |
| `color.action.primary` | Primary action background | `#1E3A8A` |

---

## 4. Typography Scale & Hierarchy

EduCore enforces a strict, readable typography system optimized for dense operational tables, dashboards, and data input.

| Typography Token | Scale / Size | Weight | Line Height | Usage Scope |
| :--- | :--- | :--- | :--- | :--- |
| `font.display` | 32px (`2rem`) | Bold (700) | 1.2 | Main workspace headers |
| `font.heading` | 24px (`1.5rem`) | SemiBold (600) | 1.3 | Modal and section headers |
| `font.title` | 18px (`1.125rem`) | Medium (500) | 1.4 | Card and table titles |
| `font.body` | 14px (`0.875rem`) | Regular (400) | 1.5 | Standard data tables, inputs, text |
| `font.caption` | 12px (`0.75rem`) | Regular (400) | 1.4 | Secondary metadata, timestamps |
| `font.label` | 12px (`0.75rem`) | Medium (500) | 1.2 | Form field labels, status badges |

---

## 5. Spacing & Spatial Layout Scale

Spacing uses a consistent 4px scale to maintain visual rhythm across forms, tables, and page containers:

```text
┌──────────────────────────────────────────────────────────┐
│                      Spacing Scale                       │
├─────────────┬───────┬────────────────────────────────────┤
│ Token       │ Size  │ Primary Context                    │
├─────────────┼───────┼────────────────────────────────────┤
│ `space-1`   │ 4px   │ Tight component padding, icon gaps │
│ `space-2`   │ 8px   │ Inline button gaps, badge margins  │
│ `space-3`   │ 12px  │ Form item spacing, table cell gap  │
│ `space-4`   │ 16px  │ Standard card padding, input rows  │
│ `space-5`   │ 24px  │ Section gaps, panel margins        │
│ `space-6`   │ 32px  │ Workspace block separation         │
│ `space-7`   │ 48px  │ Major layout grid column gaps      │
│ `space-8`   │ 64px  │ Outer page container margins       │
└─────────────┴───────┴────────────────────────────────────┘
```

---

## 6. Radius, Border & Elevation Systems

Corner radius and shadows are used intentionally to build hierarchy and keep the UI clean and professional.

### Border Radius Scale
- **`radius.sm` (`4px`):** Small elements (badges, tag chips, checkboxes).
- **`radius.md` (`6px`):** Standard interactive controls (buttons, text fields, selects).
- **`radius.lg` (`8px`):** Surface containers (cards, side panels, data grids).
- **`radius.xl` (`12px`):** Overlays (dialog modals, action sheets).

### Elevation Scale
```text
Flat (0px)       ──> Surface cards, inline form panels
Raised (Shadow-1)──> Hover states, active dropdown menus
Floating (Shadow-2)──> Contextual dialogs, command center overlay
```

---

## 7. Motion Tokens

Motion should clarify user interaction and state changes without adding unnecessary noise:

- **`motion.fast` (`150ms ease-in-out`):** Micro-interactions (button hovers, checkbox toggles).
- **`motion.normal` (`250ms ease-in-out`):** Component transitions (dropdown overlays, accordion collapses).
- **`motion.slow` (`350ms ease-in-out`):** Page/view switches, modal open/close drawers.

---

## 8. Implementation Rules & Developer Guidance

```text
❌ Anti-Pattern (Hardcoded Styles):
const SubmitButton = styled.button`
  background-color: #1e3a8a;
  padding: 12px 24px;
  border-radius: 6px;
  color: #ffffff;
`;

✅ System Standard (Token-Driven Implementation):
const SubmitButton = styled.button`
  background-color: var(--color-action-primary);
  padding: var(--space-3) var(--space-5);
  border-radius: var(--radius-md);
  color: var(--color-text-inverse);
`;
```

---

## 9. Architectural Summary

1. **Deterministic Visual Styling:** Every visual attribute maps directly to a predefined design token.
2. **Data-Dense Optimization:** Spacing and typography scales are calibrated for fast scannability and efficient screen utilization.
3. **Institutional Personality:** Restrained usage of corner radiuses, drop shadows, and brand colors keeps the user interface calm and reliable.
4. **Maintenance Efficiency:** Updating a single token value propagates styling changes predictably across the entire platform.

Brand tokens originate from:

/brand/05-Approved-Color-Palette.md

Typography tokens originate from:

/brand/06-Typography-System.md
