# EduCore Color System

## 1. Purpose

This document defines the brand color strategy and semantic color taxonomy for EduCore.

It ensures visual consistency across the web application shell, mobile apps, transactional documents, marketing platforms, and future product extensions.

> **Color Axiom:** EduCore is an operational platform where information density and task clarity take precedence over visual decoration. Color communicates state, focus, and hierarchy—it is never used purely for decoration.

---

## 2. Information & Color Hierarchy

In EduCore, visual focus follows a strict four-tiered functional hierarchy:

```text
┌──────────────────────────────────────────────────────────┐
│                     Color Hierarchy                      │
├─────────────────┬────────────────────────────────────────┤
│ 1. Information  │ Neutral tones dominate surfaces and    │
│                 │ body copy for optimal scannability.    │
├─────────────────┼────────────────────────────────────────┤
│ 2. Action       │ Primary brand tones signal interactive │
│                 │ controls and key pathways.             │
├─────────────────┼────────────────────────────────────────┤
│ 3. Status       │ Semantic colors communicate state      │
│                 │ resolution (success, warning, error).  │
├─────────────────┼────────────────────────────────────────┤
│ 4. Expression   │ Secondary/accent tones highlight       │
│                 │ features, insights, or brand anchors.  │
└─────────────────┴────────────────────────────────────────┘
```

---

## 3. Brand & Accent Color Architecture

Brand colors represent the identity anchor of EduCore, driving primary actions, selected navigation, and institutional highlights.

```text
┌──────────────────────────────────────────────────────────┐
│                   Brand Color Taxonomy                   │
├───────────────┬──────────────────────────────────────────┤
│ Primary Brand │ Deep navy / cobalt tone instilling       │
│               │ institutional trust, stability, and      │
│               │ operational clarity.                     │
├───────────────┼──────────────────────────────────────────┤
│ Secondary     │ Slate / teal accents providing depth for │
│               │ feature highlights and data callouts.    │
├───────────────┼──────────────────────────────────────────┤
│ Accent        │ Used sparingly to draw immediate user    │
│               │ attention to high-value insights or      │
│               │ system announcements.                    │
└───────────────┴──────────────────────────────────────────┘
```

---

## 4. Neutral Surface & Typography Scale

Neutral colors form over 80% of the UI surface area, reducing eye fatigue during intensive administrative, grading, or billing workflows.

```text
┌──────────────────────────────────────────────────────────┐
│                   Neutral Color Layers                   │
├──────────────────┬───────────────────────────────────────┤
│ Canvas / BG      │ Base workspace background.            │
├──────────────────┼───────────────────────────────────────┤
│ Surface          │ Cards, containers, data tables.       │
├──────────────────┼───────────────────────────────────────┤
│ Elevated Surface │ Modals, popovers, dropdown menus.     │
├──────────────────┼───────────────────────────────────────┤
│ Primary Text     │ Headings, key table metrics, values.  │
├──────────────────┼───────────────────────────────────────┤
│ Secondary Text   │ Subtitles, labels, metadata captions. │
├──────────────────┼───────────────────────────────────────┤
│ Muted Text       │ Placeholders, disabled control text.  │
├──────────────────┼───────────────────────────────────────┤
│ Border / Divider │ Subtle cell dividers and panel borders.│
└──────────────────┴───────────────────────────────────────┘
```

---

## 5. Semantic Feedback Palette

Semantic colors convey platform state resolution and operational alerts:

```text
┌──────────────────────────────────────────────────────────┐
│                   Semantic Roles & Usage                 │
├─────────────┬────────────────────────────────────────────┤
│ Success     │ Completed actions, approved grades, fee    │
│             │ payments confirmed.                        │
├─────────────┼────────────────────────────────────────────┤
│ Warning     │ Attention required, pending approvals,     │
│             │ unverified attendance, unpaid balances.    │
├─────────────┼────────────────────────────────────────────┤
│ Error       │ Failed actions, invalid form entries,      │
│             │ payment rejections, system exceptions.     │
├─────────────┼────────────────────────────────────────────┤
│ Information │ Neutral announcements, guidance tooltips,  │
│             │ platform updates.                          │
└─────────────┴────────────────────────────────────────────┘
```

### Multimodal Feedback Standard
To ensure WCAG AAA accessibility, **never rely on color alone** to convey meaning. Always pair color with text labels, icons, or visual indicators:

```text
❌ Non-Compliant (Color-Only):
Green Text = Approved | Red Text = Rejected

✅ Accessibility Compliant (Multimodal Indicator):
✓ Approved (Success Token)
● Pending Review (Warning Token)
⚠ Action Required / Error (Destructive Token)
```

---

## 6. Data Visualization Standards

Charts and analytics panels in dashboards must enforce coherent, predictable color mappings:

- **Financial Analytics:** Standardized palette mapping for *Fee Receipts*, *Outstanding Balances*, and *Projected Revenue*.
- **Academic Performance:** Distinct color scales comparing student grade distribution, attendance trends, and class benchmarks.
- **Accessibility:** High-contrast hues distinguishable for colorblind users (deuteranopia/protanopia).

---

## 7. Color Usage Rules & Anti-Patterns

```text
┌──────────────────────────────────────────────────────────┐
│                   Color Application Gate                 │
├───────────────────────────────────┬──────────────────────┤
│ ❌ PROHIBITED ANTI-PATTERNS       │ ✅ MANDATORY RULE    │
├───────────────────────────────────┼──────────────────────┤
│ • Overly colorful "rainbow"       │ • Neutral tones      │
│   dashboards and cards.           │   dominate 80%+ UI.  │
│ • Using brand primary colors for  │ • Reserve primary for│
│   decorative card borders.        │   key CTAs & focus.  │
│ • Low-contrast text on colored    │ • Enforce WCAG AA    │
│   badge backgrounds.              │   4.5:1 contrast.    │
│ • Color changes without state     │ • Color must convey  │
│   or semantic meaning.            │   meaningful state.  │
└───────────────────────────────────┴──────────────────────┘
```

---

## 8. Dark Mode Readiness

All color assignments map strictly to semantic CSS tokens (e.g., `var(--color-bg-canvas)`), ensuring seamless future dark mode support without hardcoded color refactoring.

---

## 9. Architectural Summary

1. **Information First:** Neutral surfaces minimize cognitive fatigue during dense data entry and review.
2. **Accessible Semantics:** Multimodal indicators combine status colors with clear icons and text labels.
3. **Restrained Identity:** Brand colors are reserved for interactive elements, navigation anchors, and key calls to action.
