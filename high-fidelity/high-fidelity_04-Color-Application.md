# EduCore Color Application Guidelines

## 1. Purpose

This document defines how colors are applied throughout the EduCore product experience [cite: 3].

It establishes [cite: 3]:

- color usage principles [cite: 3]
- semantic meaning [cite: 3]
- component application [cite: 3]
- accessibility rules [cite: 3]
- AI-agent restrictions [cite: 3]

---

# 2. Color Philosophy

EduCore uses color to communicate [cite: 3]:

```
Meaning
  ↓
Priority
  ↓
State
  ↓
Action
```

Color should not exist only for decoration [cite: 3].

---

# 3. Color System Relationship

EduCore color system has three layers [cite: 3]:

```
Brand Colors
  ↓
Semantic Colors
  ↓
Interface Colors
```

---

# 4. Brand Colors

**Purpose:** Represent EduCore identity [cite: 3].

**Used for [cite: 3]:**
- logo [cite: 3]
- primary actions [cite: 3]
- selected states [cite: 3]
- important highlights [cite: 3]

Brand colors should appear intentionally [cite: 3]. **Avoid** using brand color everywhere [cite: 3].

- **Good:** Primary action button, active navigation item, important highlight [cite: 3].
- **Bad:** Every card border, every icon, every text element [cite: 3].

---

# 5. Semantic Colors

Semantic colors communicate meaning [cite: 3].

## Success
- **Meaning:** Completed, approved, positive state [cite: 3].
- **Examples:** Payment completed, assessment approved, attendance submitted [cite: 3].
- **Usage:** Success messages, confirmation indicators, completed statuses [cite: 3].

## Warning
- **Meaning:** Requires attention [cite: 3].
- **Examples:** Outstanding payment, pending approval, incomplete record [cite: 3].
- **Usage:** Alerts, pending states, attention indicators [cite: 3].

## Error
- **Meaning:** Something failed or requires correction [cite: 3].
- **Examples:** Invalid payment, failed submission, missing required field [cite: 3].
- **Usage:** Validation, destructive errors, failed operations [cite: 3].

## Information
- **Meaning:** Helpful context [cite: 3].
- **Examples:** New feature notice, system information [cite: 3].

---

# 6. Neutral Colors

Neutral colors create the foundation [cite: 3]. Used for backgrounds, surfaces, text, borders, and tables [cite: 3].

Most of the interface should be neutral [cite: 3]. A premium product is usually **mostly neutral with intentional color** [cite: 3].

---

# 7. Background Application

Recommended hierarchy [cite: 3]:

```
Application Background
  ↓
Surface
  ↓
Elevated Surface
  ↓
Interactive Element
```

*(Example: Page background → White content area → Card surface → Button)* [cite: 3]

**Avoid** every section becoming a colored box [cite: 3].

---

# 8. Button Color Rules

- **Primary Button:** Use for main actions (e.g., *Add Student*, *Submit Assessment*, *Record Payment*) [cite: 3].
- **Secondary Button:** Use for alternative actions (e.g., *Cancel*, *Export*, *View Details*) [cite: 3].
- **Destructive Button:** Use for dangerous actions (e.g., *Delete*, *Deactivate*) [cite: 3].

**Rule:** One primary action per screen where possible [cite: 3].

---

# 9. Status Colors

Statuses should be visually consistent [cite: 3]:

- **Assessment:** Draft (Neutral), Submitted (Information), Approved (Success), Correction Required (Warning), Locked (Neutral) [cite: 3].
- **Payment:** Pending (Warning), Completed (Success), Failed (Error) [cite: 3].

---

# 10. Dashboard Color Rules

Dashboards require restraint [cite: 3]. **Avoid** different colors for every metric card [cite: 3].

- **Recommended:** Most cards are neutral [cite: 3].
- **Important exceptions:** Use semantic colors for risks, pending actions, and achievements [cite: 3].

---

# 11. Table Color Rules

Tables should prioritize scanning [cite: 3]. Use color for status and important exceptions—not every row [cite: 3].

- **Good:** Active (green badge), Pending (yellow badge) [cite: 3].
- **Avoid:** Colored backgrounds for entire rows unless necessary [cite: 3].

---

# 12. Form Color Rules

Color communicates state [cite: 3].
- **Default:** Neutral [cite: 3]
- **Focus:** Brand accent [cite: 3]
- **Valid:** Success indicator [cite: 3]
- **Invalid:** Error indicator [cite: 3]

**Avoid** using colors only to make forms attractive [cite: 3].

---

# 13. Dark Mode Consideration

Future support should be possible [cite: 3]. Therefore, do not hardcode colors; use semantic tokens (e.g., `background: surface.default` instead of `background: white`) [cite: 3].

---

# 14. Accessibility Requirements

Colors must not be the only communication method [cite: 3]. 

- **Bad:** Red means error [cite: 3].
- **Good:** Red icon + Error message + Clear text [cite: 3].

Ensure sufficient contrast, readable text, and distinguishable states [cite: 3].

---

# 15. AI Agent Color Rules

AI agents must **NOT** [cite: 3]:
- ❌ invent new colors [cite: 3]
- ❌ add gradients randomly [cite: 3]
- ❌ color every component [cite: 3]
- ❌ use brand colors as decoration [cite: 3]

AI agents must [cite: 3]:
- ✓ use approved tokens [cite: 3]
- ✓ follow semantic meaning [cite: 3]
- ✓ prioritize readability [cite: 3]
- ✓ maintain consistency [cite: 3]

---

# 16. Design Review Questions

Before approving a design, ask [cite: 3]:
- Does the color communicate something? [cite: 3]
- Can users understand without color? [cite: 3]
- Is the interface becoming visually noisy? [cite: 3]
- Is the brand used intentionally? [cite: 3]

---

# 17. Final Principle

EduCore should use color like a professional tool [cite: 3]:
- Rarely [cite: 3]
- Purposefully [cite: 3]
- Meaningfully [cite: 3]

Color should guide attention, not compete for it [cite: 3].
