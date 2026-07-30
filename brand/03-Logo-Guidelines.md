# EduCore Logo Guidelines

## 1. Purpose

This document defines the architectural specification and usage standards for the EduCore logo system.

As the central identifier of the platform, the logo must maintain brand recognition, structural balance, and legibility across all touchpoints, including the web app shell, mobile application icons, transactional emails, and printed documents.

> **Logo Axiom:** The EduCore logo is not merely a school mark; it represents the intelligence layer behind modern educational institutions—restrained, precise, scalable, and structured.

---

## 2. Logo System Components

The logo system consists of six coordinated assets to handle various layout constraints and display density:

```text
┌──────────────────────────────────────────────────────────┐
│                    Logo Architecture                     │
├──────────────────┬───────────────────────────────────────┤
│ Primary Logo     │ Default lockup (Symbol + Wordmark)    │
├──────────────────┼───────────────────────────────────────┤
│ Logo Mark        │ Standalone geometric symbol / icon    │
├──────────────────┼───────────────────────────────────────┤
│ Wordmark         │ Standalone typography treatment       │
├──────────────────┼───────────────────────────────────────┤
│ Mobile App Icon  │ Touch-optimized high-contrast icon    │
├──────────────────┼───────────────────────────────────────┤
│ Favicon          │ Micro-scale (16x16 / 32x32) symbol    │
├──────────────────┼───────────────────────────────────────┤
│ Monochrome       │ Single-color fallback (Black / White) │
└──────────────────┴───────────────────────────────────────┘
```

---

## 3. Symbolic Conceptual Pillars

Logo explorations must derive form from four core operational themes:

```text
┌──────────────────────────────────────────────────────────┐
│                   Conceptual Theme Matrix                │
├───────────────┬──────────────────────────────────────────┤
│ Core          │ Central operational hub supporting all   │
│               │ school workflows.                        │
├───────────────┼──────────────────────────────────────────┤
│ Connection    │ Interlocking networks bridging teachers, │
│               │ students, admins, and financial data.    │
├───────────────┼──────────────────────────────────────────┤
│ Growth        │ Upward vector indicating educational and │
│               │ institutional progress.                  │
├───────────────┼──────────────────────────────────────────┤
│ Structure     │ Clean geometric framework bringing order │
│               │ to operational complexity.               │
└───────────────┴──────────────────────────────────────────┘
```

---

## 4. Visual Traits & Form Guidelines

### Design Characteristics
- **Minimal Geometry:** Pure shapes (circles, squares, precision angles) for maximum scalability.
- **Strong Silhouette:** Instantly recognizable form that remains readable in monochrome or ultra-low resolutions.
- **Balanced Proportions:** Mathematical grid symmetry to instill institutional trust and stability.
- **Timeless Simplicity:** Free of ephemeral design trends, excessive gradients, or skeuomorphic textures.

---

## 5. Clear Space & Minimum Scale Standard

To preserve visual authority, the logo must always maintain explicit margin padding and adhere to hard scale limits:

```text
Clear Space Rule:
Clear space surrounding the logo must equal at least 50% of the total mark height (X).

 ┌──────────────────────────────────────┐
 │               [ 0.5X ]               │
 │ [ 0.5X ]   ┌────────────┐   [ 0.5X ] │
 │            │  EduCore   │            │
 │            └────────────┘            │
 │               [ 0.5X ]               │
 └──────────────────────────────────────┘
```

### Scale Hierarchy
- **Web/Desktop App Shell Header:** `32px` vertical height.
- **Mobile Navigation Header:** `24px` vertical height.
- **Browser Favicon:** `16px` x `16px` / `32px` x `32px` (Logo Mark only).
- **Print / Document Headers:** Minimum `15mm` height.

---

## 6. Logo Usage & Application Rules

```text
┌──────────────────────────────────────────────────────────┐
│                   Logo Usage Rules                       │
├───────────────────────────────────┬──────────────────────┤
│ ❌ PROHIBITED                     │ ✅ MANDATORY         │
├───────────────────────────────────┼──────────────────────┤
│ • Distortion or uneven stretching │ • Preserve aspect    │
│   of logo proportions.            │   ratio always.      │
│ • Custom drop shadows, glows, or  │ • Flat color fills   │
│   outer bevel effects.            │   using brand tokens.│
│ • Unapproved color combinations.  │ • High contrast vs   │
│   background surface.             │                      │
│ • Low-contrast surface placements.│ • Clear space        │
│   enforced on all sides.          │                      │
└───────────────────────────────────┴──────────────────────┘
```

---

## 7. AI Generation Prompt Protocol

When utilizing generative AI tools for concept exploration, avoid generic prompts that output traditional educational clichés.

```text
❌ Anti-Pattern Prompt:
"Create a school logo with a book and graduation cap."

✅ System Standard Prompt:
"Create a premium technology platform mark for a modern school operating system. The symbol should utilize minimal geometric forms to represent connection, structural stability, and growth. Avoid graduation caps, books, pencils, or traditional badges."
```

---

## 8. Architectural Summary

1. **Brand Representation:** The logo represents a high-performance operating system, not a traditional academic badge.
2. **System Flexibility:** Deploy specialized asset variants (Primary, Mark, Monochromatic) optimized for specific UI contexts.
3. **Rigid Quality Controls:** Enforce clear space padding and contrast standards to maintain visual confidence across the platform.
