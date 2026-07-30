# EduCore User Journeys

## 1. Purpose

This document defines the major user journeys within EduCore.

It describes:
- user goals
- starting points
- required steps
- system responses
- successful outcomes

The goal is to ensure every workflow reflects how schools actually operate.

---

## 2. Journey Design Principles

EduCore workflows should be:

- **Task-oriented**: Users should complete real work, not navigate software.
- **Guided**: Complex processes should provide clear progression.
- **Efficient**: Common tasks should require minimal effort.
- **Transparent**: Users should always understand current status, next action, and expected outcome.

---

## 3. User Personas

Primary MVP users:

- **Administrator**: "Understand and manage the entire school operation."
- **Academic Head**: "Maintain academic quality and control."
- **Teacher**: "Complete daily teaching responsibilities efficiently."
- **Bursar**: "Maintain accurate financial records."

---

## 4. Journey: Administrator First Login

- **Goal**: Allow a school administrator to quickly understand EduCore and begin operating.
- **Entry Point**: Login
- **Flow**: Login $ightarrow$ Dashboard $ightarrow$ Review School Setup $ightarrow$ Configure Academic Information $ightarrow$ Create Staff Accounts $ightarrow$ Begin Operations
- **Important Information**: Dashboard should show school profile status, setup completion, and pending actions.
- **Successful Outcome**: Administrator understands what needs to happen next.

---

## 5. Journey: Teacher Taking Attendance

- **Goal**: Allow teachers to record daily attendance quickly.
- **Entry Point**: Teacher Dashboard
- **Flow**: Open Dashboard $ightarrow$ View Today's Classes $ightarrow$ Select Class $ightarrow$ Open Attendance $ightarrow$ Mark Students Present/Absent $ightarrow$ Submit Attendance
- **System Response**: Show successful submission, timestamp, and correction option.
- **Success Outcome**: Attendance record is stored and available for reporting.

---

## 6. Journey: Teacher Entering Assessment Scores

- **Goal**: Allow teachers to submit student scores accurately.
- **Entry Point**: Assessment Dashboard
- **Flow**: View Assigned Assessments $ightarrow$ Select Assessment $ightarrow$ Select Class $ightarrow$ Enter Scores $ightarrow$ Review $ightarrow$ Submit
- **System States**: Draft $ightarrow$ Submitted $ightarrow$ Approved $ightarrow$ Published
- **Success Outcome**: Scores enter the approval workflow.

---

## 7. Journey: Academic Head Approving Assessment

- **Goal**: Ensure academic quality control.
- **Entry Point**: Approval Queue
- **Flow**: View Pending Assessments $ightarrow$ Open Submission $ightarrow$ Review Scores $ightarrow$ Approve OR Request Correction
- **System Response**: 
  - *Approved*: Assessment locked for next stage.
  - *Correction*: Returned to teacher.
- **Success Outcome**: Only verified academic records progress.

---

## 8. Journey: Administrator Reviewing School Performance

- **Goal**: Understand school operation.
- **Entry Point**: Administrator Dashboard
- **Flow**: Open Dashboard $ightarrow$ Review Key Indicators $ightarrow$ Identify Issues $ightarrow$ Navigate Into Detail $ightarrow$ Take Action
- **Dashboard Insights Examples**: Attendance concerns, pending approvals, fee collection status, and student population.

---

## 9. Journey: Bursar Recording Payment

- **Goal**: Maintain accurate financial records.
- **Entry Point**: Finance Dashboard
- **Flow**: Search Student $ightarrow$ View Outstanding Balance $ightarrow$ Record Payment $ightarrow$ Generate Receipt $ightarrow$ Update Balance
- **Success Outcome**: Financial record is updated immediately.

---

## 10. Journey: Administrator Adding Student

- **Goal**: Create a student record.
- **Entry Point**: Students
- **Flow**: Student List $ightarrow$ Add Student $ightarrow$ Enter Information $ightarrow$ Add Guardian $ightarrow$ Confirm Enrollment $ightarrow$ Generate Admission Number
- **Success Outcome**: Student becomes available across attendance, assessment, and results.

---

## 11. Journey: Admission Conversion

- **Goal**: Convert an applicant into a student.
- **Flow**: Applicant List $ightarrow$ Review Applicant $ightarrow$ Approve Admission $ightarrow$ Create Student Record $ightarrow$ Assign Class
- **Success Outcome**: Applicant becomes active student.

---

## 12. Journey: Result Generation

- **Goal**: Generate official student reports.
- **Flow**: Academic Session Complete $ightarrow$ Review Assessments $ightarrow$ Calculate Results $ightarrow$ Generate Reports $ightarrow$ Approve $ightarrow$ Publish
- **Success Outcome**: Students receive official results.

---

## 13. Cross-Journey Principles

Every workflow should answer:
- **Where am I?** (Clear location)
- **What am I doing?** (Clear task)
- **What happens next?** (Clear progression)
- **What went wrong?** (Clear recovery)

---

## 14. Workflow States

Important operations should expose states:
- **Assessment**: Draft, Submitted, Approved, Locked
- **Payment**: Pending, Completed, Reversed
- **Admission**: Applied, Under Review, Accepted, Converted

---

## 15. AI Agent Guidance

Before implementing any workflow, AI must identify:
- user goal
- starting point
- required steps
- possible errors
- completion state

*Note: Do not design pages independently of workflows.*

---

## 16. Final Principle

EduCore should not make users think: *"Which module do I open?"*

It should make them think: *"What do I need to accomplish?"*

The interface should guide them there.
