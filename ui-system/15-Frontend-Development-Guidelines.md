# EduCore Frontend Development Guidelines

## 1. Purpose

This document defines the engineering standards for implementing the EduCore frontend.

It establishes:

- coding conventions
- component rules
- feature boundaries
- TypeScript practices
- state management principles
- maintainability standards

The goal is to ensure that EduCore frontend remains:

Predictable


Scalable


Maintainable


as the product grows.

---

# 2. Frontend Engineering Philosophy

EduCore frontend follows the same principle as the backend:

Clear boundaries


Explicit ownership


Controlled complexity


---

The frontend is not a collection of screens.

It is a structured product system.

---

# 3. Feature-First Architecture

The primary organization principle is:

Feature ownership.

Structure:

features/
├── students/
├── attendance/
├── assessment/
├── results/
├── finance/
└── admission/


---

Each feature owns its:

- components
- hooks
- services
- types
- validation
- tests

---

# 4. Component Organization Rules

Components are divided into:

## Shared Components

Used across the application.

Example:

components/
Button
DataTable
Modal
PageHeader


---

## Feature Components

Specific to a business capability.

Example:

features/student/components/
StudentProfileCard
EnrollmentForm


---

Rule:

Do not put feature-specific components in global folders.

---

# 5. Component Creation Rules

Before creating a component ask:

1. Does this already exist?

2. Is this reusable?

3. Does it belong globally or to a feature?

4. Is the abstraction justified?

---

Avoid:

Creating components for every small piece.

---

Bad:

StudentNameLabel.tsx


when it is only used once.

---

Good:

StudentCard.tsx


when reused.

---

# 6. Component Size Guidelines

Avoid:

Large components containing:

- API calls
- business logic
- UI rendering
- state management

---

Prefer:

Page
↓
Feature Component
↓
Shared Components


---

# 7. Naming Conventions

Use clear descriptive names.

---

Components:

PascalCase.

Example:

StudentTable.tsx


---

Hooks:

camelCase with:

use


prefix.

Example:

useStudents()


---

Services:

camelCase.

Example:

studentApi.ts


---

Types:

PascalCase.

Example:

StudentProfile


---

# 8. TypeScript Standards

TypeScript should improve reliability.

Rules:

- avoid unnecessary any
- define API types
- use explicit interfaces
- prefer type safety

---

Avoid:

```typescript
const data: any
```

Prefer:

```typescript
const student: Student
```

---

# 9. API Communication Rules

Components should not directly call APIs.

Avoid:

Component
↓
axios.get()


---

Preferred:

Component
↓
Hook
↓
Service
↓
API Client


---

# 10. State Management Rules

Separate:

## Server State

Backend data.

Examples:

- students
- payments
- assessments

---

## Client State

Application state.

Examples:

- sidebar open
- theme
- modal state

---

Do not place everything in global state.

---

# 11. Form Management Rules

Forms should use:

- reusable form patterns
- schema validation
- consistent error handling

---

Important:

Validation should exist close to the form logic.

---

# 12. Styling Rules

Styling should follow:

Design Tokens
↓
Theme
↓
Components


---

Avoid:

Random values.

Example:

Bad:

margin: 17px;


Better:

Use spacing tokens.

---

# 13. Business Logic Rules

Business rules should not live inside components.

Avoid:

```typescript
if (student.status === "ACTIVE")
```

everywhere.

Prefer:

Centralized domain helpers.

---

# 14. Page Composition Rules

Pages should compose features.

Example:

Student page:

StudentPage
↓
StudentTable
↓
StudentFilters
↓
StudentActions


---

Pages should not contain complex implementation details.

---

# 15. Error Handling Rules

Every feature must handle:

- loading
- success
- empty
- error

---

Never assume:

"The API will always work."

---

# 16. File Naming Rules

Recommended:

- `StudentTable.tsx`
- `StudentTable.test.tsx`
- `studentApi.ts`
- `studentTypes.ts`
- `useStudents.ts`

---

Files should reveal purpose immediately.

---

# 17. Import Discipline

Avoid:

deep uncontrolled imports.

Prefer:

Feature boundaries.

Example:

Good:

`features/student` imports `components/common`


---

Avoid:

Student importing internal Assessment implementation details.

---

# 18. Dependency Rules

Before adding a package:

Ask:

1. Is it necessary?

2. Does the ecosystem already solve this?

3. Does it increase complexity?

---

Avoid dependency accumulation.

---

# 19. AI Agent Development Rules

Before generating code, AI agents must:

1. Read relevant architecture documents

2. Identify owning feature

3. Inspect existing patterns

4. Reuse components

5. Follow naming conventions

6. Add tests

---

AI agents should not create isolated solutions.

---

# 20. Code Review Checklist

Reviewers should check:

## Architecture

□ Correct feature location
□ No broken boundaries

## Quality

□ Type safe
□ Reusable
□ Tested

## UX

□ Loading states
□ Error handling
□ Responsive behavior

---

# 21. Definition of Done

Frontend work is complete when:

Implemented + Tested + Responsive + Consistent + Documented

---

# 22. Final Principle

EduCore frontend should be built like a serious product.

Not:

A collection of React pages.


But:

A maintainable operating system interface.
