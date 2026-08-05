# EduCoreOS Frontend Implementation Handoff

## Document Purpose

This document is the implementation source of truth for the EduCoreOS frontend.

It connects:

- EduCoreOS product requirements
- UX decisions
- approved high-fidelity designs
- frontend architecture
- backend API contracts

The goal is to recreate the approved designs as a production React application while maintaining consistency with the existing backend architecture.

This document should be read before implementing any frontend feature.

---

# 1. Product Overview

## EduCoreOS

EduCoreOS is a Nigerian-first School Operating System designed to replace fragmented school operations managed through paper, spreadsheets, and disconnected tools.

The platform provides a unified system for:

- School administration
- Student management
- Academic operations
- Attendance tracking
- Assessment workflows
- Finance operations
- Staff management

Initial pilot:

**Graceland International Academy (GIA)**

---

# 2. Frontend Technology Stack

The frontend implementation uses:

- React 19
- TypeScript
- Vite
- Material UI
- React Router
- TanStack Query
- Axios
- React Hook Form
- Zod

Existing project foundation:


src/

├── app/
│ ├── providers/
│ └── router/

├── api/

├── components/

├── features/

├── layouts/

├── theme/

├── hooks/

├── types/

└── utils/


Follow feature-based architecture.

Do not introduce new architectural patterns without discussion.

---

# 3. Design Philosophy

EduCoreOS should communicate:

- trust
- simplicity
- operational clarity
- professionalism
- modern African education infrastructure

The product should feel like:

"School operating infrastructure"

not:

"another school management tool."

---

# 4. Design System

## Colors

| Purpose | Value |
|-|-|
| Primary Navy | #1E3A8A |
| Primary Hover | #1E40AF |
| Accent Cyan | #06B6D4 |
| Bright Cyan | #22D3EE |
| Page Background | #F9FAFB |
| Surface | #FFFFFF |
| Border | #E5E7EB |
| Primary Text | #1E293B |
| Muted Text | #64748B |

---

## Semantic Colors

Success:


Background: #ECFDF5
Text: #047857


Warning:


Background: #FFFBEB
Text: #B45309


Danger:


Background: #FFF1F2
Text: #BE123C


Information:


Background: #EEF2FF
Text: #4338CA


---

## Typography

Primary:


Inter


Used for:

- headings
- navigation
- forms
- general UI

Secondary:


JetBrains Mono


Used for:

- IDs
- metrics
- timestamps
- technical information

---

# 5. Brand Identity

Logo:

EduCore monogram:


E → C


Characteristics:

- Navy strokes
- Cyan connection node
- EduCore wordmark
- OS suffix in JetBrains Mono cyan

Create reusable:


Logo component


Do not duplicate SVG across screens.

---

# 6. Approved Screens

The following screens were designed and reviewed using high-fidelity prototypes.

They are references for implementation.

They are not production HTML.

---

# Public Experience

## 1. Marketing Landing Page

Purpose:

Introduce EduCoreOS.

Contains:

- Hero section
- Problem statement
- Before/after comparison
- Solution pillars
- Personas
- Pricing
- CTA
- Footer


No authentication required.

---

# Authentication

## 2. Login

Purpose:

Authenticate users.

Supported roles:


ADMIN
ACADEMIC_HEAD
STAFF_TEACHER
STAFF_BURSAR
STAFF_GENERAL
APPLICANT


Important:

The UI may display role context.

Actual authorization comes from JWT claims.

Never trust frontend role hiding as security.

---

# Onboarding

## 3. School Setup Wizard

First-time school configuration.

Steps:

1. School profile
2. Session and term setup
3. Class groups
4. Student CSV import
5. Review and completion

CSV import flow:


Dry run
↓
Show validation results
↓
Confirm
↓
Commit import


---

# Internal Application

All internal screens use the common application shell.

---

# Application Shell

Reusable components:


Sidebar

AppHeader

TabSwitcher

StatusPill

StatCard

DataTable


---

## Sidebar

Specification:

Width:


232px


Style:

- white background
- right border
- active navigation highlight

Active:


background #EFF6FF
text #1E3A8A


---

## Header

Contains:

- page context
- search
- profile
- school/session controls

---

# Dashboard

Admin overview.

Contains:

- KPI cards
- trends
- activity feed
- quick actions

Data should come from APIs.

Do not calculate business metrics only in frontend.

---

# Teacher Home

Teacher daily workspace.

Contains:

- schedule
- assigned classes
- pending actions

Links into:

- attendance
- assessments

---

# Attendance Workspace

Most complete operational module.

Two experiences:

## Teacher

Features:

- class selection
- student list
- attendance marking
- remarks
- submission

## Admin

Features:

- attendance analytics
- exceptions
- trends
- notifications

Attendance statuses:


PRESENT
LATE
ABSENT
EXCUSED


---

# Students

Features:

## Student List

- search
- filtering
- pagination

## Student Profile

Tabs:


Overview
Attendance
Academics
Fees


## Registration

Sections:

- Personal information
- Academic placement
- Guardian information

---

# Academics

Modules:


Classes

Subjects

Assessment Policies

Assessments


Assessment workflow must follow backend state machine.

Never hardcode transitions.

Backend status is authoritative.

---

# Finance

Status:

Exploratory.

Backend not implemented yet.

Contains:

- Fee structures
- Invoices
- Payments

Build later behind feature flags.

---

# Administration

Contains:

- Staff management
- Settings
- Audit logs
- Reports

Audit and reports depend on future backend endpoints.

---

# 7. Backend Integration Principles

Backend:

Spring Boot Modular Monolith

Stack:

- Java 21
- Spring Boot 3.5
- PostgreSQL
- Liquibase
- JWT

Authentication:


POST /api/v1/auth/login

POST /api/v1/auth/refresh

POST /api/v1/auth/logout


---

## Security Rule

Frontend controls:

- visibility
- navigation
- user experience

Backend controls:

- authorization
- permissions
- security

---

# 8. Implementation Order

Follow this sequence:

## Phase 1

Foundation

Completed:

- React setup
- Routing
- Theme
- Providers
- Layout shell


## Phase 2

Authentication

Build:

- login
- JWT handling
- protected routes
- role-aware navigation


## Phase 3

Core Shell Refinement

Build:

- Sidebar
- Header
- Navigation
- Shared components


## Phase 4

Student Module

Reason:

Core data foundation.


## Phase 5

Attendance

Reason:

Most mature workflow.


## Phase 6

Academics


## Phase 7

Administration


## Phase 8

Finance

After backend availability.

---

# 9. Frontend Development Rules

Always:

- reuse components
- use React Query for server state
- validate forms
- type API responses
- keep business rules aligned with backend

Avoid:

- duplicated components
- hardcoded business logic
- unnecessary state management
- frontend-only authorization assumptions

---

# 10. Current Status

Completed:

✅ Product thinking  
✅ UX planning  
✅ Architecture design  
✅ High fidelity screen exploration  
✅ Frontend repository setup  
✅ React foundation  
✅ Application shell foundation  


Current focus:

Authentication implementation.
