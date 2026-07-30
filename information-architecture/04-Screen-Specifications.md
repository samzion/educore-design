# EduCore Screen Specifications

## 1. Purpose

This document defines the requirements and purpose of EduCore application screens [cite: x].

Each screen specification identifies:
- user purpose [cite: x]
- primary users [cite: x]
- entry points [cite: x]
- required information [cite: x]
- available actions [cite: x]
- states [cite: x]
- permissions [cite: x]

This document serves as the foundation for:
- wireframes [cite: x]
- UI design [cite: x]
- frontend implementation [cite: x]
- QA testing [cite: x]

---

## 2. Screen Design Principles

Every screen must answer:
- **Why does this screen exist?** There must be a clear user goal [cite: x].
- **Who uses it?** Every screen has an intended audience [cite: x].
- **What decision or action does it support?** Screens should enable work [cite: x].

---

## 3. Screen Categories

EduCore screens are grouped into:
- Workspace Screens [cite: x]
- Operational Screens [cite: x]
- Management Screens [cite: x]
- Configuration Screens [cite: x]

---

## 4. Authentication Screens

### Login Screen
- **Purpose**: Allow authorized users to access EduCore [cite: x].
- **Users**: All roles [cite: x].
- **Entry Point**: Application URL [cite: x].
- **Information Required**: Email/username, Password [cite: x].
- **Actions**: 
  - *Primary*: Login [cite: x]
  - *Secondary*: Forgot password [cite: x]
- **States**: 
  - *Loading*: Authenticating... [cite: x]
  - *Error*: Invalid credentials [cite: x]
  - *Success*: Redirect to dashboard [cite: x]

---

## 5. Dashboard Screens

### Administrator Dashboard
- **Purpose**: Provide a complete operational overview [cite: x].
- **Primary User**: Administrator [cite: x].
- **Key Question**: "How is my school operating today?" [cite: x]
- **Information Display**: 
  - *Overview*: student count, staff count, attendance summary, financial summary [cite: x]
  - *Attention Required*: pending approvals, incomplete tasks, exceptions [cite: x]
  - *Academic*: assessment status, result readiness [cite: x]
- **Actions**: View students, Review approvals, View finance, Manage settings [cite: x].
- **States**: 
  - *New school*: Show setup guidance [cite: x].
  - *Normal operation*: Show operational insights [cite: x].

### Teacher Dashboard
- **Purpose**: Help teachers complete daily responsibilities [cite: x].
- **Key Question**: "What do I need to do today?" [cite: x]
- **Information Display**: assigned classes, today's attendance status, pending assessments, upcoming tasks [cite: x].
- **Actions**: Take attendance, Enter scores, View students [cite: x].

### Academic Head Dashboard
- **Purpose**: Monitor academic quality [cite: x].
- **Key Question**: "Is academic quality controlled?" [cite: x]
- **Information Display**: pending approvals, assessment completion, result readiness, performance trends [cite: x].
- **Actions**: Review submissions, Approve assessments, Monitor results [cite: x].

### Bursar Dashboard
- **Purpose**: Monitor financial operations [cite: x].
- **Key Question**: "What is the financial state of the school?" [cite: x]
- **Information Display**: collections, outstanding balances, recent payments, unpaid fees [cite: x].
- **Actions**: Record payment, View invoices, Generate receipts [cite: x].

---

## 6. Student Screens

### Student Directory
- **Purpose**: Find and manage students [cite: x].
- **Users**: Administrator, Academic Head, Teacher (limited) [cite: x].
- **Information Table**: admission number, name, class, status, gender [cite: x].
- **Actions**: Add student, Search, Filter, View profile, Import [cite: x].
- **States**: 
  - *Empty*: No students found [cite: x].
  - *Loading*: Fetching students [cite: x].
  - *Error*: Unable to load data [cite: x].

### Student Profile
- **Purpose**: Provide a complete student view [cite: x].
- **Sections**: 
  - *Identity*: name, admission number, photo [cite: x]
  - *Academic*: enrollment, class history [cite: x]
  - *Family*: guardians [cite: x]
  - *Health*: medical information [cite: x]
  - *Activity*: attendance, assessments, results [cite: x]
- **Actions**: Edit details, Update information [cite: x].

---

## 7. Attendance Screens

### Attendance Workspace
- **Purpose**: Allow teachers to record attendance [cite: x].
- **Information**: class, date, student list, attendance status [cite: x].
- **Actions**: Mark present, Mark absent, Submit [cite: x].
- **States**: 
  - *Before submission*: Editable [cite: x].
  - *After submission*: Locked or correction workflow [cite: x].

---

## 8. Assessment Screens

### Assessment Workspace
- **Purpose**: Manage academic assessment lifecycle [cite: x].
- **Information**: assessment details, class, subject, status [cite: x].
- **Actions**: Enter scores, Submit, Review [cite: x].
- **States**: Draft, Open, Submitted, Approved, Locked [cite: x].

---

## 9. Finance Screens

### Payment Workspace
- **Purpose**: Record and track payments [cite: x].
- **Information**: student, invoice, balance, payment history [cite: x].
- **Actions**: Record payment, Generate receipt [cite: x].
- **States**: Outstanding, Partially Paid, Paid [cite: x].

---

## 10. Admission Screens

### Applicant Workspace
- **Purpose**: Manage prospective students [cite: x].
- **Information**: applicant details, application status [cite: x].
- **Actions**: Review, Approve, Reject, Convert [cite: x].
- **States**: Applied, Under Review, Accepted, Converted [cite: x].

---

## 11. Settings Screens

### School Settings
- **Purpose**: Configure school operation [cite: x].
- **Information**: school details, academic setup, preferences [cite: x].
- **Actions**: Update settings [cite: x].

---

## 12. Common Screen Requirements

Every operational screen must support:
- **Loading State**: Clear progress indication [cite: x].
- **Empty State**: Explain what happens next [cite: x].
- **Error State**: Allow recovery [cite: x].
- **Success Feedback**: Confirm completed actions [cite: x].

---

## 13. Responsive Requirements

Every screen must define:
- **Desktop**: Full operational experience [cite: x].
- **Tablet**: Teacher-friendly workflow [cite: x].
- **Mobile**: Essential actions only [cite: x].

---

## 14. Permission Requirements

Screens must respect:
- **ADMIN**: Full access [cite: x].
- **ACADEMIC_HEAD**: Academic workflows [cite: x].
- **STAFF_TEACHER**: Assigned classes [cite: x].
- **STAFF_BURSAR**: Finance workflows [cite: x].

---

## 15. AI Agent Rule

Before implementing a screen, the AI agent must know:
- screen purpose [cite: x]
- user role [cite: x]
- workflow [cite: x]
- required states [cite: x]
- available actions [cite: x]

*Note: A screen should never be created without a defined operational purpose [cite: x].*

---

## 16. Final Principle

A screen is not a collection of components [cite: x]. 

A screen is a workspace designed around a user's responsibility [cite: x].
