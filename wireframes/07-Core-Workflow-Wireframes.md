# EduCore Core Workflow Wireframes

## 1. Purpose

This document defines the major operational workflows in EduCore [cite: 1].

These workflows connect [cite: 1]:

- users [cite: 1]
- screens [cite: 1]
- actions [cite: 1]
- system states [cite: 1]

The goal is to ensure the interface reflects real school operations [cite: 1].

---

# 2. Workflow Design Principles

## Principle 1: Show Progress

Users should always understand [cite: 1]:

- current state [cite: 1]
- completed actions [cite: 1]
- next step [cite: 1]

---

## Principle 2: Make Ownership Clear

Every workflow should show [cite: 1]:

*Who acts next?* [cite: 1]

**Example (Assessment):** [cite: 1]
```
Teacher
  ↓
Academic Head
  ↓
Results Process
```

---

## Principle 3: Prevent Operational Errors

Important actions require [cite: 1]:

- validation [cite: 1]
- confirmation [cite: 1]
- clear feedback [cite: 1]

---

# 3. Student Creation Workflow

## Goal

Create a complete student record [cite: 1].

## Users

Administrator [cite: 1]

## Entry Point

```
Students → Add Student
```

---

## Flow

```
Basic Information
  ↓
Guardian Information
  ↓
Enrollment Details
  ↓
Medical Information
  ↓
Review
  ↓
Create Student
```

---

## Step 1: Basic Information

Collect [cite: 1]:
- name [cite: 1]
- date of birth [cite: 1]
- gender [cite: 1]
- contact details [cite: 1]

---

## Step 2: Guardian Information

Collect [cite: 1]:
- guardian name [cite: 1]
- relationship [cite: 1]
- contact [cite: 1]

---

## Step 3: Enrollment

Collect [cite: 1]:
- academic session [cite: 1]
- class group [cite: 1]

**System generates:** Admission Number (e.g., `GIA/26/0001`) [cite: 1]

---

## Step 4: Review

Display summary [cite: 1]:
- Student Information [cite: 1]
- Guardian Information [cite: 1]
- Enrollment Details [cite: 1]

---

## Success State

- Student successfully created [cite: 1].
- Admission number generated [cite: 1].

---

# 4. Attendance Workflow

## Goal

Allow teachers to record attendance efficiently [cite: 1].

## User

Teacher [cite: 1]

## Flow

```
Select Class
  ↓
Load Students
  ↓
Mark Attendance
  ↓
Review
  ↓
Submit
```

---

## Attendance Interface

```
==================================================
JSS 1A | 30 July 2026
--------------------------------------------------
Student              Status
Daniel               Present
Grace                Present
Musa                 Absent

[Submit Attendance]
==================================================
```

**Important UX Rule:** Default state is **Present**. The teacher modifies exceptions [cite: 1].

---

## Success State

Attendance submitted successfully [cite: 1].

## Correction Flow

```
Request Correction
  ↓
Approval
  ↓
Edit
  ↓
Resubmit
```

---

# 5. Assessment Workflow

## Goal

Manage assessment lifecycle [cite: 1].

## Users

- Teacher [cite: 1]
- Academic Head [cite: 1]

## Complete Flow

```
Create Assessment
  ↓
Open Assessment
  ↓
Enter Scores
  ↓
Submit
  ↓
Review
  ↓
Approve
  ↓
Lock
```

---

## Assessment States

```
DRAFT → OPEN → SUBMITTED → REOPENED → APPROVED → LOCKED → ARCHIVED
```

---

## Teacher View

Shows [cite: 1]:
- My Assessments
- Mathematics Test
- Status: Draft
- `[Continue]`

---

## Academic Head View

Shows [cite: 1]:
- Pending Approval
- Mathematics Test
- Teacher: Mr Ade
- Class: JSS 1A
- `[Review]`

---

## Review Screen

Contains [cite: 1]:
- assessment details [cite: 1]
- student scores [cite: 1]
- summary statistics [cite: 1]
- comments [cite: 1]

**Actions:** Approve | Request Correction [cite: 1]

---

## Success State

- **Approved:** Assessment approved [cite: 1].
- **Returned:** Correction requested [cite: 1].

---

# 6. Result Generation Workflow

## Goal

Produce official student reports [cite: 1].

## Users

- Academic Head [cite: 1]
- Administrator [cite: 1]

## Flow

```
Assessments Completed
  ↓
Calculate Results
  ↓
Review Results
  ↓
Approve
  ↓
Publish
```

---

## Result Preparation Screen

```
==================================================
Term Results (Completion: 85%)
--------------------------------------------------
Class       Status
JSS 1A      Ready
JSS 1B      Incomplete
==================================================
```

---

## Result Review

Shows [cite: 1]:
- Student: Adebayo Daniel [cite: 1]
- Subjects: Mathematics 85, English 78, Science 90 [cite: 1]

**Actions:** Approve Results | Return for Review [cite: 1]

---

# 7. Payment Workflow

## Goal

Record school fee payments [cite: 1].

## User

Bursar [cite: 1]

## Flow

```
Find Student
  ↓
View Balance
  ↓
Record Payment
  ↓
Confirm
  ↓
Generate Receipt
```

---

## Payment Confirmation

Before completion [cite: 1]:

```
Confirm Payment
- Student: Daniel
- Amount:  ₦50,000
- Method:  Transfer

[Confirm]
```

## Success

- Payment recorded [cite: 1].
- Receipt generated [cite: 1].

---

# 8. Admission Conversion Workflow

## Goal

Convert applicant into student [cite: 1].

## Users

Administrator [cite: 1]

## Flow

```
Applicant Created
  ↓
Review Application
  ↓
Accept
  ↓
Create Student
  ↓
Assign Class
```

## Applicant States

```
APPLIED → UNDER_REVIEW → ACCEPTED → CONVERTED
```

---

# 9. Cross-Workflow Status Design

All major workflows should expose [cite: 1]:
- **Current State:** e.g., *Submitted* [cite: 1]
- **Next Action:** e.g., *Awaiting Academic Approval* [cite: 1]
- **Responsible Person:** e.g., *Academic Head* [cite: 1]

---

# 10. Workflow Notifications

Notifications should support action [cite: 1].

- **Good:** "3 assessments require approval [cite: 1] → [Review now]"
- **Bad:** "Assessment updated" (without action) [cite: 1].

---

# 11. Workflow History

Important workflows should show history [cite: 1]:

```
Assessment:
- Created by Teacher
- Submitted
- Reviewed by Academic Head
- Approved
```

This creates trust [cite: 1].

---

# 12. AI Agent Rules

Before implementing any workflow, AI must define [cite: 1]:
- states [cite: 1]
- transitions [cite: 1]
- user responsible [cite: 1]
- success outcome [cite: 1]
- failure handling [cite: 1]

*Never build workflows as disconnected forms.* [cite: 1]

---

# 13. Final Principle

EduCore is not a collection of screens [cite: 1]. It is a collection of school operations [cite: 1].

The frontend should make those operations visible, understandable, and easy to complete [cite: 1].
