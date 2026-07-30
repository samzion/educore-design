# EduCore Visual Component Styling Guidelines

## 1. Purpose

This document defines the visual styling principles for EduCore interface components [cite: 3].

It establishes standards for [cite: 3]:

- cards [cite: 3]
- buttons [cite: 3]
- tables [cite: 3]
- forms [cite: 3]
- dialogs [cite: 3]
- navigation [cite: 3]
- data presentation [cite: 3]

The goal is to create a consistent premium product experience [cite: 3].

---

# 2. Component Styling Philosophy

EduCore components should feel [cite: 3]:

- Reliable [cite: 3]
- Structured [cite: 3]
- Professional [cite: 3]
- Calm [cite: 3]

The interface should communicate [cite: 3]: *"This system handles important school operations."* [cite: 3]

---

# 3. Component Design Principles

## Principle 1: Function Before Decoration
Every component must have a clear purpose [cite: 3]. **Avoid** decorative UI elements without user value [cite: 3].

## Principle 2: Consistency Builds Confidence
The same action should look the same everywhere [cite: 3]. For example, "Create" should not appear as a blue button in one place, a green button elsewhere, or an icon-only button somewhere else [cite: 3].

## Principle 3: Reduce Visual Noise
Important information should stand out naturally [cite: 3]. Do not make everything prominent [cite: 3].

---

# 4. Border Philosophy

EduCore should use borders intentionally [cite: 3]. 

- **Preferred:** Subtle borders [cite: 3] for separation, grouping, and structure [cite: 3].
- **Avoid:** Heavy borders everywhere (e.g., every section having thick outlines) [cite: 3].

---

# 5. Shadow Philosophy

Shadows communicate elevation and should be subtle [cite: 3].

- **Use shadows for:** Dropdowns, dialogs, floating actions, and important overlays [cite: 3].
- **Avoid:** Every card having a large shadow [cite: 3]. Premium products usually rely more on spacing and hierarchy than shadows [cite: 3].

---

# 6. Card Styling

Cards are common in dashboards, but **avoid card overload** [cite: 3].

- **Good Card Usage:** Use cards for grouped information, summaries, and important actions (e.g., *School Overview*, *Payment Summary*, *Pending Approvals*) [cite: 3].
- **Avoid:** Turning every piece of information into a separate card (*Student Name Card*, *Class Card*, *Status Card*, *Guardian Card*) [cite: 3]. Prefer student profiles and information sections [cite: 3].

---

# 7. Button Styling

Buttons communicate actions [cite: 3].

- **Primary Button:** Main task (e.g., *Add Student*, *Submit Assessment*, *Record Payment*). Features strong contrast, clear label, comfortable size [cite: 3].
- **Secondary Button:** Supporting actions (e.g., *Cancel*, *Export*, *View Details*) [cite: 3].
- **Destructive Button:** Dangerous actions (e.g., *Delete*, *Deactivate*) [cite: 3].

**Button Rules:**
- Avoid multiple primary buttons competing, unclear labels, or icon-only important actions [cite: 3].
- Prefer **Verb + Object** (e.g., *Create Student* instead of just *Create*) [cite: 3].

---

# 8. Input Field Styling

Forms should feel trustworthy [cite: 3] and need clear labels, visible states, and helpful errors [cite: 3].

- **States:** Default, Focused, Filled, Error, Disabled [cite: 3].
- **Avoid:** Placeholder-only forms (e.g., avoiding just `[Enter name]` without a label like *Student Name*) [cite: 3].

---

# 9. Table Styling

Tables are critical in EduCore and should optimize scanning, comparison, and action [cite: 3].

- **Clear headers:** Users understand columns immediately [cite: 3].
- **Appropriate density:** Not too cramped, not unnecessarily spacious [cite: 3].
- **Consistent actions:** Actions should appear predictably [cite: 3].
- **Avoid:** Tables that look like spreadsheets from the 1990s [cite: 3].

---

# 10. Status Badge Styling

Status badges communicate workflow state (e.g., *Approved*, *Pending*, *Draft*, *Completed*) [cite: 3].

- **Rules:** Consistent shape, consistent meaning, readable text [cite: 3].
- **Avoid:** Using badges for everything [cite: 3].

---

# 11. Modal and Dialog Styling

Dialogs should support decisions [cite: 3] (confirmation, focused workflows, important actions like payment confirmation) [cite: 3].

- **Avoid:** Using modals for large workflows (e.g., a 20-field form inside a modal) [cite: 3]. Prefer focused confirmations [cite: 3].

---

# 12. Navigation Styling

Navigation should feel stable [cite: 3]. 

- **Sidebar:** Should communicate current location and available areas [cite: 3].
- **Active state:** Use a subtle background and a brand indicator [cite: 3].
- **Avoid:** Large colorful navigation blocks [cite: 3].

---

# 13. Empty State Styling

Empty states should guide users [cite: 3] with an illustration/icon, title, explanation, and primary action (e.g., *"No students yet. Add your first student to begin."* + `[Add Student]`) [cite: 3]. Avoid dead ends [cite: 3].

---

# 14. Loading States

Loading should preserve context using skeleton screens and progress indicators, avoiding blank screens [cite: 3].

---

# 15. Notification Styling

Notifications should be actionable and concise (e.g., *"5 assessments require approval → [Review now]"* instead of passive text like *"Assessment updated"*) [cite: 3].

---

# 16. Component Density

EduCore users handle many records, so default density should be **balanced** [cite: 3]. Avoid making it too spacious (one record per huge card) or too dense (tiny text everywhere) [cite: 3].

---

# 17. AI Agent Component Rules

AI agents must **NOT** [cite: 3]:
- ❌ create random component styles [cite: 3]
- ❌ introduce new button variants [cite: 3]
- ❌ use excessive cards [cite: 3]
- ❌ add decorative shadows [cite: 3]
- ❌ redesign existing components [cite: 3]

AI agents must [cite: 3]:
- ✓ use component library [cite: 3]
- ✓ follow tokens [cite: 3]
- ✓ preserve consistency [cite: 3]
- ✓ prioritize workflows [cite: 3]

---

# 18. Final Principle

Great products are not made by adding more visual elements. They are made by deciding: *"What deserves attention?"* [cite: 3]

EduCore components should make school operations feel simple, clear, and professional [cite: 3].
