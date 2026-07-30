# EduCore Motion and Interaction Design Guidelines

## 1. Purpose

This document defines the motion and interaction principles for EduCore [cite: 3].

It establishes standards for [cite: 3]:

- animations [cite: 3]
- transitions [cite: 3]
- feedback states [cite: 3]
- loading experiences [cite: 3]
- micro-interactions [cite: 3]

The goal is to create an interface that feels [cite: 3]:
- responsive [cite: 3]
- intelligent [cite: 3]
- trustworthy [cite: 3]

---

# 2. Motion Philosophy

EduCore motion should communicate [cite: 3]:
- Change [cite: 3]
- Feedback [cite: 3]
- Relationship [cite: 3]
- Progress [cite: 3]

Motion should never exist only because *"It looks cool."* [cite: 3]

---

# 3. Product Motion Personality

EduCore motion should feel [cite: 3]:

- **Calm:** No distracting movement [cite: 3].
- **Predictable:** Users understand what happened [cite: 3].
- **Fast:** Interactions should feel immediate [cite: 3].
- **Professional:** Suitable for school operations [cite: 3].

---

# 4. Motion Principles

## Principle 1: Motion Should Have Purpose
Every animation should answer: *"What user problem does this solve?"* [cite: 3]
- **Good:** A menu smoothly opening (shows relationship) [cite: 3].
- **Bad:** Animated dashboard decorations (no operational value) [cite: 3].

## Principle 2: Preserve User Context
When information changes, the user should understand where it went [cite: 3]. For example, deleting a record should follow a confirmation → removal → feedback flow rather than instant disappearance [cite: 3].

## Principle 3: Respect User Attention
Motion should not interrupt work [cite: 3]. Avoid bouncing elements, flashing notifications, and excessive transitions [cite: 3].

---

# 5. Interaction Feedback

Every important action requires feedback [cite: 3]. When a user clicks *Submit Attendance*, the system should communicate processing and then success, never leaving users wondering *"Did it work?"* [cite: 3]

---

# 6. Button Interactions

Buttons should have clear states: Default, Hover, Pressed, Loading, Disabled, Success [cite: 3].
- **Before:** *Submit Assessment* [cite: 3]
- **During:** *Saving...* [cite: 3]
- **After:** *Saved ✓* [cite: 3]

---

# 7. Form Interactions

Forms should guide users [cite: 3]. Field validation should be specific (e.g., *"Guardian phone number is required"*) rather than vague messages like *"Invalid input"* [cite: 3].

---

# 8. Page Transitions

Navigation should feel connected with subtle transitions (page content fade, loading skeleton replacement) [cite: 3]. Avoid full-screen animations between pages [cite: 3].

---

# 9. Loading Experiences

Loading is a trust moment [cite: 3]. Avoid blank screens; instead, use **Skeleton Loading** so the user understands the system is working [cite: 3].

---

# 10. Data Update Feedback

When records change, show clear confirmation (e.g., attendance saved successfully, payment recorded with receipt generated, scores submitted for review) [cite: 3].

---

# 11. Modal Interactions

Dialogs should enter and exit naturally with a subtle appearance and clear focus, avoiding large dramatic animations [cite: 3].

---

# 12. Table Interactions

Tables contain important operational data, supporting row hover, sorting feedback, and filtering feedback while avoiding unexpected row jumping [cite: 3].

---

# 13. Dashboard Interactions

Dashboard elements should help discovery (e.g., clicking metric cards like *Outstanding Fees* to view students), avoiding clickable elements without indication [cite: 3].

---

# 14. Notifications

Notifications should support action (e.g., *"3 assessments need review → [Review]"*) and take the user directly to the task [cite: 3].

---

# 15. Success Moments

Important milestones deserve confirmation (e.g., student successfully created with admission number `GIA/26/0001`, or payment complete with receipt ready) [cite: 3]. Avoid celebration animations for normal operations [cite: 3].

---

# 16. Error Interactions

Errors should help recovery [cite: 3]. 
- **Good:** *"Payment could not be saved. Reason: Duplicate transaction reference. Try another reference."* [cite: 3]
- **Bad:** *"Error occurred."* [cite: 3]

---

# 17. Accessibility Considerations

Motion must support reduced motion preferences, keyboard navigation, and screen readers, and must not be required to understand the interface [cite: 3].

---

# 18. AI Agent Motion Rules

AI agents must **NOT** [cite: 3]:
- ❌ add animations everywhere [cite: 3]
- ❌ create flashy transitions [cite: 3]
- ❌ animate decorative elements [cite: 3]
- ❌ use motion as compensation for poor UX [cite: 3]

AI agents must [cite: 3]:
- ✓ add motion only with purpose [cite: 3]
- ✓ preserve workflow clarity [cite: 3]
- ✓ maintain professional tone [cite: 3]
- ✓ respect accessibility [cite: 3]

---

# 19. Final Principle

EduCore motion should feel like a helpful assistant acknowledging your actions—not a website trying to impress you [cite: 3].
