# EduCore Application Map

## Purpose

This document defines the complete structure of the EduCore application.

It identifies every major capability, feature, page, and operational area that forms the EduCore School Operating System.

It serves as the master blueprint for:

- Product Design
- UX Design
- Wireframing
- Frontend Development
- Backend Integration
- QA Planning

---

# Design Philosophy

The application is organised around how schools operate—not around technical modules.

Users should be able to navigate naturally based on their daily responsibilities.

Every page must support a real operational task.

---

# Top-Level Application Structure

```
Authentication

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

# Authentication

Purpose:

Provide secure access to EduCore.

Pages:

- Login
- Forgot Password
- Reset Password
- Session Expired

---

# Dashboard

Purpose:

Provide an operational overview based on the logged-in user's role.

Pages:

- Administrator Dashboard
- Academic Head Dashboard
- Teacher Dashboard
- Bursar Dashboard

---

# Students

Purpose:

Manage the student lifecycle after admission.

Pages:

- Student Directory
- Student Profile
- Enrollment Details
- Guardians
- Medical Information

---

# Attendance

Purpose:

Support daily attendance operations.

Pages:

- Attendance Dashboard
- Take Attendance
- Attendance History
- Attendance Corrections

---

# Assessment

Purpose:

Manage continuous assessment and examination workflows.

Pages:

- Assessment Dashboard
- Assessment Policies
- Assessment Templates
- Assessments
- Score Entry
- Approval Queue
- Archived Assessments

---

# Results

Purpose:

Generate and publish academic results.

Pages:

- Results Dashboard
- Result Generation
- Student Results
- Report Cards
- Publication Centre
- Published Results

---

# Finance

Purpose:

Manage school financial operations.

Pages:

- Finance Dashboard
- Fee Structures
- Invoices
- Payments
- Receipts
- Outstanding Balances

---

# Admissions

Purpose:

Manage applicants before they become students.

Pages:

- Applicants
- Applicant Details
- Review
- Admission Decisions
- Convert to Student

---

# Promotion

Purpose:

Manage academic progression.

Pages:

- Promotion Dashboard
- Promotion Rules
- Promotion Preview
- Execute Promotion
- Promotion History

---

# Settings

Purpose:

Manage school configuration.

Pages:

School

- School Information
- Academic Calendar
- Branding

Users

- Staff Accounts
- Roles
- Permissions

System

- Preferences
- Notifications
- Profile

---

# Supporting Features

Accessible from multiple areas:

- Global Search
- Notifications
- Activity Timeline
- User Profile
- Help & Support

---

# Application Relationships

```
Authentication
        │
        ▼
Dashboard
        │
 ┌──────┼───────────────┐
 ▼      ▼               ▼

Students Attendance Assessment
 │         │            │
 └────┬────┴────┬───────┘
      ▼         ▼

    Results   Promotion

Finance

Settings
```

---

# Principles

The application should:

- feel task-oriented
- minimise unnecessary navigation
- reduce context switching
- maintain consistency across modules
- expose only relevant actions to each role

---

# Out of Scope (MVP)

The following are intentionally excluded from the first pilot unless required by GIA:

- Parent Portal
- Student Portal
- Mobile Application
- Website CMS
- Learning Management System (LMS)
- Library Management
- Hostel Management
- Transport Management

These may be introduced as future bounded contexts after the MVP pilot.
