# EduCore Academic Head Experience Wireframe Specification

## 1. Purpose

This document defines the Academic Head experience within EduCore [cite: x].

The Academic Head is responsible for:
- monitoring academic activities [cite: x]
- reviewing assessments [cite: x]
- approving submissions [cite: x]
- ensuring academic quality [cite: x]
- supervising result readiness [cite: x]

---

## 2. Academic Head Experience Goal

The Academic Head should feel: *"I have control over academic quality and can quickly identify where attention is needed."* [cite: x]

The experience should prioritize:
- visibility [cite: x]
- review efficiency [cite: x]
- confidence [cite: x]
- quality control [cite: x]

---

## 3. Academic Head Mental Model

Academic Heads think in terms of:
Academic Activity $ightarrow$ Review $ightarrow$ Decision $ightarrow$ Quality Assurance [cite: x]

They do not think:
- Open Assessment Module
- Manage Assessment Entity [cite: x]

---

## 4. Academic Head Entry Point

After login:
Login $ightarrow$ Academic Head Dashboard [cite: x]

The dashboard answers: *"What requires academic attention today?"* [cite: x]

---

## 5. Academic Head Dashboard Wireframe

- **Layout**: Good morning, Academic Head / Graceland International Academy / Attention Required (8 Assessments Awaiting Approval, 3 Classes Missing Scores, 2 Result Issues Detected), Academic Overview (Assessment Completion: 86%, Result Readiness: 72%), Recent Academic Activity (Mathematics Assessment Submitted, JSS 2 Results Approved) [cite: x].

---

## 6. Dashboard Sections

### Section 1: Approval Queue
- The highest priority area [cite: x].
- Examples: Pending Assessments, Pending Results, Correction Requests [cite: x].
- Every item should provide owner, class, subject, submitted date, and current status [cite: x].

### Section 2: Academic Health
- **Purpose**: Provide operational visibility [cite: x].
- Examples: Assessment completion (JSS 1 Mathematics Completed), Missing work (SS2 Biology Scores incomplete) [cite: x].

### Section 3: Quick Actions
- Examples: Review Assessment, View Results, Check Class Performance [cite: x].
- Maximum 3-5 actions [cite: x].

---

## 7. Assessment Approval Experience

- **Goal**: Allow academic review without unnecessary friction [cite: x].
- **Entry**: Dashboard $ightarrow$ Approval Queue $ightarrow$ Assessment [cite: x].
- **Approval Queue Wireframe**: Assessment Approvals / Filters (Term | Subject | Class | Teacher) / Data table (Assessment | Class | Teacher | Status) [cite: x].

---

## 8. Assessment Review Screen

- **Purpose**: Allow informed approval decisions [cite: x].
- **Layout**: Assessment Details (Mathematics Test / JSS 1A / Teacher: Mr Ade), Score Summary (Average Score, Highest Score, Lowest Score), Student Scores table (Daniel: 18, Grace: 15), Actions ([[Approve]], [[Request Correction]]) [cite: x].

---

## 9. Approval Actions

### Approve
- **Meaning**: Assessment has passed academic review [cite: x].
- **System response**: Assessment approved. Available for result processing [cite: x].

### Request Correction
- **Requires**: Reason [cite: x] (e.g., Missing scores for 3 students) [cite: x].

---

## 10. Result Monitoring Experience

- **Goal**: Ensure results are complete before publication [cite: x].
- **Result Readiness Screen**: Term Results / Completion: 85% / Class status table (JSS 1A: Complete, JSS 1B: Pending, SS1: Complete) / Actions: Review, Follow Up, Publish [cite: x].

---

## 11. Academic Reports Experience

- **Purpose**: Understand academic performance [cite: x].
- **Possible insights**: subject performance, class performance, assessment completion, score distribution [cite: x].
- Reports should support decisions; avoid decorative analytics [cite: x].

---

## 12. Correction Workflow

- **Flow**: Academic Head $ightarrow$ Request Correction $ightarrow$ Teacher Receives Task $ightarrow$ Teacher Updates $ightarrow$ Academic Head Reviews Again [cite: x].
- The system should make ownership clear [cite: x].

---

## 13. Permission Boundaries

- **Academic Head can**: Review assessments, Approve academic workflows, View academic records, Monitor performance [cite: x].
- **Academic Head cannot**: Modify financial data, Change school configuration, Manage system roles [cite: x].

---

## 14. Mobile Experience

- Mobile supports quick approvals, notifications, and monitoring [cite: x].
- **Priority**: Approvals, Notifications, Reports [cite: x].
- Heavy review workflows remain desktop/tablet optimized [cite: x].

---

## 15. Empty States

- **No pending approvals**: Everything is reviewed. No academic actions required [cite: x].
- **No results ready**: Results are still being prepared [cite: x].

---

## 16. Success Criteria

Academic Head should be able to:
- [x] Identify academic issues quickly [cite: x]
- [x] Review submissions efficiently [cite: x]
- [x] Approve or return work [cite: x]
- [x] Monitor result readiness [cite: x]
- [x] Maintain academic standards [cite: x]

---

## 17. AI Agent Rules

When implementing Academic Head features, prioritize:
- workflows [cite: x]
- approval clarity [cite: x]
- status visibility [cite: x]
- auditability [cite: x]

Avoid:
- excessive dashboards [cite: x]
- unnecessary charts [cite: x]
- unrestricted editing [cite: x]

---

## 18. Final Principle

The Academic Head experience should feel like a quality control centre for academic operations [cite: x], not another administrative dashboard [cite: x].
