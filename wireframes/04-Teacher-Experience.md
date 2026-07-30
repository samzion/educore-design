# EduCore Teacher Experience Wireframe Specification

## 1. Purpose

This document defines the teacher experience within EduCore [cite: x].

Teachers are responsible for:
- managing assigned classes [cite: x]
- recording attendance [cite: x]
- entering assessments [cite: x]
- accessing student information [cite: x]
- monitoring class activities [cite: x]

---

## 2. Teacher Experience Goal

The teacher should feel: *"I know what I need to do today, and I can complete it quickly."* [cite: x]

The experience should prioritize:
- speed [cite: x]
- simplicity [cite: x]
- clarity [cite: x]
- minimal interruptions [cite: x]

---

## 3. Teacher Mental Model

Teachers think in terms of:
My Classes $ightarrow$ My Students $ightarrow$ Today's Tasks $ightarrow$ Completion [cite: x]

They do not think:
- Attendance Module
- Assessment Bounded Context
- Student Entity [cite: x]

---

## 4. Teacher Entry Point

After login:
Login $ightarrow$ Teacher Dashboard [cite: x]

The dashboard answers: *"What needs my attention today?"* [cite: x]

---

## 5. Teacher Dashboard Wireframe

- **Layout**: Good morning, Mr. Ade / JSS 1 Mathematics Teacher / Today's Tasks (Attendance: JSS 1A Pending [[Take Attendance]], Assessment: Mathematics Assignment Due for submission), My Classes (JSS 1A: 32 Students, JSS 2B: 28 Students), Recent Activity (Assessment approved, Attendance submitted) [cite: x].

---

## 6. Dashboard Sections

### Section 1: Today's Tasks
- Most important area [cite: x].
- Examples: Attendance pending, Assessment scores incomplete, Upcoming class activity [cite: x].
- Priority: Tasks > Statistics [cite: x].

### Section 2: My Classes
- **Purpose**: Quick access to assigned classes [cite: x].
- **Display**: Class Name, Subject, Student Count [cite: x].
- **Actions**: Open Class [cite: x].

### Section 3: Quick Actions
- Maximum 3 actions [cite: x].
- Recommended: Take Attendance, Enter Scores, View Students [cite: x].

---

## 7. Attendance Experience

- **Goal**: Allow a teacher to complete attendance in under one minute [cite: x].
- **Entry**: Dashboard $ightarrow$ Attendance $ightarrow$ Select Class [cite: x].
- **Attendance Screen Wireframe**: JSS 1A Attendance / Date: 30 July 2026 / Student (Adebayo Daniel, Chioma Grace, Musa Ibrahim) Status (Present, Present, Absent) [[Submit Attendance]] [cite: x].

### Interaction Principles
- **Default**: Present [cite: x] (because most students are present [cite: x]).
- Teacher only changes exceptions [cite: x].
- Avoid making teachers click Present, Present, Present for every student [cite: x].

---

## 8. Attendance States

- **Before submission**: Editable [cite: x].
- **After submission**: Submitted / Awaiting correction window [cite: x].
- **Correction**: Request correction [cite: x].

---

## 9. Assessment Experience

- **Goal**: Allow teachers to record scores efficiently [cite: x].
- **Entry**: Dashboard $ightarrow$ Assessment $ightarrow$ Select Assessment [cite: x].
- **Assessment Screen Wireframe**: Mathematics Test / JSS 1A / Maximum Score: 20 / Student Score (Adebayo Daniel: 18, Chioma Grace: 15, Musa Ibrahim: 12) [[Save Draft]] [[Submit]] [cite: x].

---

## 10. Score Entry Principles

Support:
- keyboard navigation [cite: x]
- quick editing [cite: x]
- validation [cite: x]
- automatic saving where appropriate [cite: x]

Avoid opening individual student pages to enter scores [cite: x].

---

## 11. Class View

- **Purpose**: Provide teacher access to classroom information [cite: x].
- **Display**: Class: JSS 1A, Students: 32, Attendance Summary, Assessment Summary [cite: x].
- **Actions**: Take Attendance, Enter Scores, View Students [cite: x].

---

## 12. Student Information Access

Teachers should see relevant information only [cite: x].
- **Allowed**: name, class, attendance, academic information [cite: x].
- **Restricted**: sensitive medical details unless authorized [cite: x].

---

## 13. Teacher Mobile Experience

This is critical [cite: x]. Teachers may use smartphones, tablets, and shared devices [cite: x].
- **Mobile priority**: Bottom navigation (Home, Classes, Attendance, Assessment, More) [cite: x].

---

## 14. Mobile Attendance

Optimized for one-hand operation [cite: x]. Avoid small buttons, wide tables, and excessive scrolling [cite: x].

---

## 15. Teacher Empty States

- **No assigned classes**: You have no assigned classes yet. Contact your administrator [cite: x].
- **No pending tasks**: You are all caught up. No actions required [cite: x].

---

## 16. Teacher Success Criteria

A teacher should be able to:
- [x] See today's responsibilities immediately [cite: x]
- [x] Mark attendance quickly [cite: x]
- [x] Enter scores efficiently [cite: x]
- [x] Access student information [cite: x]
- [x] Understand workflow status [cite: x]

---

## 17. AI Agent Rules

When implementing teacher features, prioritize:
- speed [cite: x]
- fewer clicks [cite: x]
- mobile usability [cite: x]
- keyboard efficiency [cite: x]

Avoid:
- complex dashboards [cite: x]
- unnecessary charts [cite: x]
- administrative controls [cite: x]

---

## 18. Final Principle

The teacher experience should disappear into the workflow [cite: x]. 

A teacher should not think: *"I am using school management software."* 

They should think: *"I completed my class responsibilities."* [cite: x]
