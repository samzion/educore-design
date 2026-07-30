# EduCore Frontend Implementation Guide

## 1. Purpose

This document defines the implementation principles and workflow for building the EduCore frontend.

It provides a practical guide for:

* frontend engineers
* UI/UX designers
* AI coding agents
* technical reviewers

The goal is to ensure every frontend implementation aligns with EduCore's product vision, design system, and engineering standards.

---

# 2. EduCore Frontend Vision

EduCore frontend is not a collection of independent screens.

It is:

> A unified operational workspace where schools manage academic and administrative activities efficiently.

Every implementation decision should improve:

* clarity
* speed
* confidence
* usability

---

# 3. Before Implementation Begins

No feature should begin implementation from a screenshot or isolated requirement.

Before coding, understand:

## Product Context

Read:

```
brand/
```

Understand:

* product identity
* positioning
* visual direction

---

## User Context

Read:

```
information-architecture/
wireframes/
```

Understand:

* who uses the feature
* what problem it solves
* where it fits in the workflow

---

## Design Context

Read:

```
high-fidelity/
ui-system/
```

Understand:

* visual rules
* components
* tokens
* interaction standards

---

# 4. Required Implementation Reading

For every frontend feature, the engineer or AI agent should review:

## Foundation

```
ui-system/

01-Design-System-Foundation.md
02-Design-Tokens.md
```

---

## Components

```
ui-system/

03-Component-Strategy.md
05-Component-Library.md
```

---

## Layout

```
ui-system/

06-Layout-System.md
07-Responsive-Design.md
```

---

## UX Behaviour

```
ui-system/

08-Data-Display-and-Information-Design.md
10-Authentication-and-Authorization-UX.md
11-Role-Based-UI-Strategy.md
20-Frontend-Product-Experience-Principles.md
```

---

## Engineering Standards

```
ui-system/

15-Frontend-Development-Guidelines.md
16-Frontend-Implementation-Roadmap.md
19-AI-Agent-Frontend-Implementation-Protocol.md
21-Frontend-Implementation-Readiness-Review.md
```

---

# 5. Frontend Architecture Principles

## Feature-Based Organization

Frontend structure should follow business capabilities.

Example:

```
features/

├── students/

├── attendance/

├── assessment/

├── results/

└── finance/
```

---

Avoid organizing the entire application only by technical type.

Avoid:

```
components/
pages/
utils/
```

as the primary structure.

---

# 6. Component Philosophy

Components should be:

* reusable
* predictable
* maintainable
* consistent

Before creating a new component:

Ask:

1. Does this already exist?
2. Can an existing component support this through variants?
3. Is this truly reusable?

---

Prefer:

```
StudentTable
AttendanceGrid
PaymentSummary
```

over:

```
GenericTable123
NewCardVersion
CustomStudentBox
```

---

# 7. UI Implementation Rules

Every screen should consider:

## Data States

* loading
* success
* empty
* error

---

## User Actions

* primary action
* secondary action
* destructive action

---

## Permissions

Who can:

* view?
* create?
* update?
* approve?
* delete?

---

## Responsive Behaviour

The experience should work across:

* desktop
* tablet
* mobile

---

# 8. Design System Rules

Frontend implementation must use:

* approved colors
* typography tokens
* spacing tokens
* component library
* layout patterns

Do not:

* hardcode random values
* create one-off styles
* introduce unrelated UI patterns

---

# 9. Backend Alignment

Frontend structure should align with backend domain boundaries.

Example:

Backend:

```
Student bounded context
```

Frontend:

```
features/students
```

---

Frontend should understand:

* API contracts
* permissions
* workflow states

---

# 10. AI Agent Implementation Rules

AI agents working on EduCore must:

## Before Coding

Read relevant documentation.

Understand:

* user workflow
* existing components
* architecture

---

## During Coding

Must:

* reuse existing patterns
* follow folder structure
* use design tokens
* maintain consistency

---

Must not:

* invent new designs
* create duplicate components
* replace architecture decisions
* introduce unnecessary dependencies

---

# 11. Feature Implementation Workflow

Recommended workflow:

```
Requirement

↓

User workflow understanding

↓

Design reference review

↓

Component identification

↓

Frontend implementation

↓

Testing

↓

UX review

↓

Acceptance
```

---

# 12. Frontend Definition of Done

A feature is complete when:

## Functional

✓ User workflow works

✓ API integration works

✓ Permissions are respected

---

## Experience

✓ Matches design system

✓ Responsive

✓ Clear interactions

✓ Proper feedback

---

## Quality

✓ Loading handled

✓ Empty state handled

✓ Error state handled

✓ Tested

---

# 13. Final Principle

The frontend is the daily workspace of school operators.

The objective is not to create impressive screens.

The objective is to create a system users can confidently rely on.

EduCore frontend standard:

```
Consistent

Clear

Reliable

Human-centered
```
