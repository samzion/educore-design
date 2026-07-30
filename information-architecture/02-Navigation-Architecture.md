# EduCore Navigation Architecture

## 1. Purpose

This document defines the navigation structure of EduCore.

It establishes:

- primary navigation
- secondary navigation
- role-based visibility
- navigation principles
- user movement patterns

The goal is to ensure users can quickly reach the tasks relevant to their responsibilities.

---

# 2. Navigation Philosophy

EduCore navigation follows:

```
Role

↓

Responsibility

↓

Task

↓

Action
```

Users should not navigate based on system architecture.

They navigate based on their daily work.

---

# 3. Global Application Structure

The application consists of:

```
Global Navigation

+

Contextual Navigation

+

Task Actions
```

---

# 4. Global Navigation

Available throughout the application.

```
Dashboard

Students

Attendance

Assessment

Results

Finance

Admissions

Promotion

Settings
```

Visibility depends on user role.

---

# 5. Application Shell

Desktop layout:

```
┌──────────────────────────────────┐
│ Header                           │
├────────────┬─────────────────────┤
│            │                     │
│ Sidebar    │ Main Workspace      │
│            │                     │
│            │                     │
└────────────┴─────────────────────┘
```

---

# 6. Sidebar Principles

The sidebar should:

- show important destinations
- avoid overwhelming users
- highlight current location
- support quick switching

---

Avoid:

```
20+ menu items
```

---

Prefer:

```
5-8 meaningful destinations
```

---

# 7. Administrator Navigation

## Primary Navigation

```
Dashboard

Students

Attendance

Assessment

Results

Finance

Admissions

Promotion

Settings
```

---

Administrator question:

"How is my school operating?"

---

Administrator needs visibility into:

- student population
- academic performance
- attendance issues
- finances
- staff operations

---

# 8. Academic Head Navigation

## Primary Navigation

```
Dashboard

Students

Assessment

Results

Attendance

Reports
```

---

Academic Head question:

"Is academic quality controlled?"

---

Priority actions:

- review assessments
- approve results
- monitor performance
- identify academic issues

---

# 9. Teacher Navigation

## Primary Navigation

```
Dashboard

My Classes

Attendance

Assessment

Students
```

---

Teacher question:

"What do I need to do today?"

---

Priority actions:

- mark attendance
- enter scores
- view students
- manage assigned classes

---

# 10. Bursar Navigation

## Primary Navigation

```
Dashboard

Finance

Students

Reports
```

---

Bursar question:

"What is the financial state of the school?"

---

Priority actions:

- record payments
- check balances
- generate receipts
- review outstanding fees

---

# 11. Contextual Navigation

Some navigation appears only inside a workflow.

Example:

Student Profile:

```
Student Overview

Enrollment

Guardians

Medical

Attendance

Assessments

Results
```

---

This avoids cluttering the main sidebar.

---

# 12. Action Navigation

Important actions should be visible where users need them.

Example:

Student List:

```
+ Add Student

Import Students

Export
```

---

Assessment:

```
Create Assessment

Enter Scores

Submit
```

---

# 13. Navigation States

Every navigation item should support:

## Default

User has not selected it.

---

## Active

Current location.

---

## Disabled

User does not have permission.

---

## Hidden

Not relevant to role.

---

# 14. Mobile Navigation

Mobile should prioritize:

Most frequent tasks.

Example Teacher:

```
Home

Attendance

Classes

Assessment

More
```

---

Avoid forcing desktop navigation onto mobile.

---

# 15. Search as Navigation

EduCore should support global search.

Users should be able to find:

- students
- applicants
- payments
- assessments

---

Search reduces navigation complexity.

---

# 16. Navigation Rules

A user should ideally reach any common task within:

```
3 clicks or fewer
```

---

Examples:

Teacher marking attendance:

```
Dashboard

↓

Attendance

↓

Class
```

---

Bursar finding payment:

```
Dashboard

↓

Finance

↓

Student Payment
```

---

# 17. Navigation Anti-Patterns

Avoid:

❌ Technical module names

Example:

"Assessment Bounded Context"

---

Prefer:

"Assessments"

---

Avoid:

❌ Showing everything to everyone

---

Avoid:

❌ Deep navigation trees

---

# 18. AI Agent Rules

Before creating a page:

AI must identify:

- user role
- navigation location
- entry point
- next action

---

A page without a clear navigation purpose should not be created.

---

# 19. Final Principle

EduCore navigation should feel like:

```
A well-organized workspace

not

a collection of software modules.
```
