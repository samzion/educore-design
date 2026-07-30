# EduCore Application Shell Wireframe Specification

## 1. Purpose

The application shell defines the persistent interface structure that surrounds all EduCore screens [cite: x].

It establishes:
- navigation structure [cite: x]
- workspace layout [cite: x]
- global actions [cite: x]
- user context [cite: x]
- responsive behaviour [cite: x]

The shell should provide consistency across all features [cite: x].

---

## 2. Experience Goal

The application shell should feel like:
- **A professional school operations workspace** [cite: x]

Not:
- **A collection of disconnected admin pages** [cite: x]

---

## 3. Shell Structure

Desktop layout:
- Header [cite: x]
- Sidebar Navigation + Workspace Area [cite: x]

---

## 4. Header Design

- **Purpose**: Provide global context and frequently used actions [cite: x].
- **Header Contents**:
  - *Left*: EduCore Logo, School Context (e.g., EduCore / Graceland International Academy) [cite: x]
  - *Right*: Search, Notifications, Help, User Menu [cite: x]

---

## 5. School Context

The user should always know: *"Which school am I operating?"* [cite: x]
- **MVP**: Single school context (Display: Graceland International Academy) [cite: x].
- **Future SaaS**: Support School Selector, Campus Selector [cite: x].

---

## 6. Global Search

- **Purpose**: Reduce navigation effort [cite: x]. Users should quickly find students, applicants, payments, and assessments [cite: x].
- **Search Support**: "Search anything..." [cite: x]
- **Future Capability**: Command palette style experience (e.g., `Ctrl + K`) [cite: x].

---

## 7. Notification Centre

- **Purpose**: Surface important events [cite: x].
- *Examples*:
  - Teacher: Assessment approved [cite: x]
  - Administrator: 5 payments pending review [cite: x]
  - Academic Head: 3 assessments awaiting approval [cite: x]
- Avoid notifications for everything; show only actionable information [cite: x].

---

## 8. User Menu

- **Contains**: Profile, Account Settings, Preferences, Logout [cite: x].
- Should display Name and Role (e.g., Samuel Kayode / Administrator) [cite: x].

---

## 9. Sidebar Navigation

- **Purpose**: Provide access to major operational areas [cite: x].
- **Design Rules**: Sidebar should remain predictable, show current location, and avoid excessive options [cite: x].
- **Recommended structure**: Dashboard, Students, Attendance, Assessment, Results, Finance, Admissions, Promotion, Settings [cite: x].

---

## 10. Sidebar States

- **Expanded**: Desktop default (shows Icon + Label) [cite: x].
- **Collapsed**: Optional (shows Icons only) [cite: x].
- **Active**: Current page highlighted [cite: x].
- **Restricted**: Hidden or disabled based on role [cite: x].

---

## 11. Workspace Area

The workspace is where features appear. Every page should follow:
Page Header $ightarrow$ Context $ightarrow$ Primary Action $ightarrow$ Content $ightarrow$ Secondary Actions [cite: x]

---

## 12. Page Header Pattern

Contains Title, Description, and Primary action (e.g., Students / Manage student records and enrollment / [+ Add Student]) [cite: x].

---

## 13. Breadcrumbs

Use only when useful (e.g., Students $ightarrow$ Adebayo Daniel $ightarrow$ Medical Information) [cite: x]. Avoid unnecessary breadcrumbs [cite: x].

---

## 14. Desktop Experience

Target: Laptop-first (common in school offices, administrator desks, bursar offices) [cite: x]. Optimize for tables, workflows, and productivity [cite: x].

---

## 15. Tablet Experience

Important for teachers [cite: x]. Adapt with collapsed sidebar and horizontal scrolling or priority columns for tables [cite: x].

---

## 16. Mobile Experience

Mobile is task-focused [cite: x]. 
- **Navigation**: Bottom Navigation or Drawer Menu [cite: x].
- **Priority actions**:
  - Teacher: Attendance, Assessment, Classes [cite: x]
  - Administrator: Dashboard, Students, Notifications [cite: x]

---

## 17. Loading State

The shell should appear immediately (Navigation visible, Content skeleton loading) [cite: x]. Do not show blank screens [cite: x].

---

## 18. Empty State

Example: No students yet. Add your first student to begin managing records. [Add Student] [cite: x]

---

## 19. Error State

Example: Unable to load students. Try again. [Retry] [cite: x]

---

## 20. AI Agent Implementation Rules

Before creating any page, the AI agent must reuse:
- application shell [cite: x]
- navigation patterns [cite: x]
- page header pattern [cite: x]
- spacing rules [cite: x]

Do not create independent layouts [cite: x].

---

## 21. Final Principle

The EduCore shell should make every feature feel like part of one operating system [cite: x]. 

Users should never feel: *"I entered another module."* They should feel: *"I am still inside EduCore."* [cite: x]
