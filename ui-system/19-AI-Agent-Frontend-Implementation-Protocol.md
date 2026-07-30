# EduCore AI-Agent Frontend Implementation Protocol

## 1. Purpose

This document defines how AI coding agents should contribute to EduCore frontend development.

It establishes:

- required context before implementation
- decision-making rules
- implementation workflow
- validation expectations
- quality standards

The goal is to ensure AI-generated code maintains EduCore's product and engineering standards.

---

# 2. AI Development Philosophy

AI agents are contributors, not autonomous decision makers.

The agent must behave like:

A senior frontend engineer
working within
an established product system

---

The goal is not:

"Generate working code."

The goal is:

"Extend EduCore consistently."

---

# 3. Required Context Before Implementation

Before writing code, the AI agent must understand:

## Product Context

Read:

Frontend Vision

Product Requirements

Relevant Domain Context

---

## Architecture Context

Read:

Frontend Architecture
Project Structure
API Integration Strategy

---

## UX Context

Read:

Design System
Component Library
Layout System
Workflow Guidelines

---

## Backend Context

Read:

Relevant backend bounded context.

Example:

Student feature:

Student Domain Documentation
Student API Contracts

---

# 4. Implementation Decision Process

Before creating UI, AI should answer:

## Question 1

Who is the user?

Example:

Teacher

Administrator

Bursar

---

## Question 2

What task are they trying to complete?

Example:

"Record attendance"

not:

"Use attendance module"

---

## Question 3

What information do they need?

---

## Question 4

What action should be easiest?

---

## Question 5

What workflow state exists?

---

# 5. Implementation Sequence

AI should follow:

Understand
↓
Design
↓
Reuse
↓
Implement
↓
Validate

---

# 6. Understand Existing Code First

Before creating files:

Inspect:

- existing components
- hooks
- services
- patterns

---

Never assume:

"The project does not have this yet."

---

# 7. Reuse Before Creating

Preferred:

Existing Component
↓
Extend
↓
Create New Only If Necessary

---

Avoid:

Duplicate components.

Examples:

StudentTable
StudentsTable
StudentDataGrid

---

# 8. UI Quality Requirements

AI-generated UI must satisfy:

## Professional Appearance

Not:

Default template dashboard

---

Should reflect:

- spacing discipline
- hierarchy
- intentional layouts
- appropriate density

---

## Operational Clarity

Every screen should answer:

"What should the user do next?"

---

# 9. Component Creation Rules

Before creating a component:

Explain:

Purpose
Why it exists
Why existing components cannot solve it

---

---

# 10. API Implementation Rules

AI must:

- use existing API client
- use feature services
- use typed responses
- handle loading
- handle errors

---

Forbidden:

Direct API calls inside components.

---

# 11. State Management Rules

AI must classify state:

## Server State

Use appropriate data fetching patterns.

---

## UI State

Keep local where possible.

---

Do not introduce global state unnecessarily.

---

# 12. Responsive Requirements

Every generated screen must consider:

Desktop:

How does it work?

Tablet:

How does it adapt?

Mobile:

What changes?

---

AI must not create desktop-only interfaces.

---

# 13. Testing Requirements

Every feature implementation should consider:

## Component Tests

Important UI behavior.

---

## Feature Tests

Important workflows.

---

## Edge Cases

Examples:

- empty data
- loading
- errors
- permission restrictions

---

# 14. Backend Alignment Rules

AI must respect backend boundaries.

Example:

Do not combine:

Student

Finance

Assessment

into one frontend feature because they appear together visually.

---

Respect:

Backend bounded contexts.

---

# 15. Documentation Updates

When introducing significant patterns:

Update:

- architecture docs
- component documentation
- decisions log

---

The documentation should evolve with the product.

---

# 16. Validation Before Completion

AI must verify:

## Architecture

□ Correct feature location

□ No broken boundaries

---

## UX

□ Clear user goal

□ Proper workflow

□ Responsive behavior

---

## Engineering

□ Type safety

□ Tests

□ Error handling

---

# 17. Forbidden AI Behaviors

AI agents must not:

❌ Create generic dashboards

❌ Ignore design system

❌ Duplicate components

❌ Hardcode business rules in UI

❌ Skip loading states

❌ Skip error states

❌ Assume backend permissions

❌ Create unnecessary dependencies

---

# 18. Prompt Template for AI Implementation

Recommended prompt structure:

You are implementing a feature in EduCore.
Before coding:

Review:

Frontend architecture documents

Design system rules

Relevant backend bounded context

Identify:

user role

workflow

required components

API contracts

Implement following:

feature structure

existing patterns

responsive requirements

Validate:

tests

UX consistency

error handling

---

# 19. Senior Engineer Standard

AI output should be reviewed as if produced by:

A junior-to-mid engineer

with the reviewer checking:

- architecture
- UX
- maintainability

---

# 20. Final Principle

AI should accelerate EduCore development.

It should not define EduCore's identity.

The product vision, architecture, and standards remain the source of truth.

AI writes faster.
Standards decide better.
