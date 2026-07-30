# EduCore Bursar Experience Wireframe Specification

## 1. Purpose

This document defines the Bursar experience within EduCore.

The Bursar is responsible for:

- monitoring fee collection
- recording payments
- tracking outstanding balances
- generating receipts
- maintaining financial accuracy

---

# 2. Bursar Experience Goal

The Bursar should feel:

"I always know the financial position of the school and can confidently manage payments."

---

The experience should prioritize:

- accuracy
- transparency
- speed
- accountability

---

# 3. Bursar Mental Model

Bursars think in terms of:

```
Student
  ↓
Fee Obligation
  ↓
Payment
  ↓
Balance
  ↓
Receipt
```

---

They do not think:

- Finance Module
- Payment Entity
- Invoice Aggregate

---

# 4. Bursar Entry Point

After login:

```
Login
  ↓
Bursar Dashboard
```

---

The dashboard answers:

*What is the current financial state?*

---

# 5. Bursar Dashboard Wireframe

```
==================================================
Good morning, Bursar
Graceland International Academy
--------------------------------------------------
Financial Overview
- Total Expected Fees: ₦25,000,000
- Collected:           ₦18,500,000
- Outstanding:         ₦6,500,000

Attention Required
- 45 Outstanding Payments
- 12 Recent Payments Pending Review

Quick Actions
[Record Payment]   [Find Student]   [Generate Report]
==================================================
```

---

# 6. Dashboard Sections

## Section 1: Financial Summary

**Purpose:** Provide immediate financial visibility.

**Display:**
- expected fees
- collected amount
- outstanding amount
- collection percentage

*Avoid:* Overcomplicated accounting metrics.

---

## Section 2: Attention Required

**Examples:**
- Students with overdue fees
- Incomplete payment records
- Recent payment issues

Every item should lead to action.

---

## Section 3: Quick Actions

**Primary actions:**
- Record Payment
- Search Student
- View Balances

*Maximum:* 3-5 actions.

---

# 7. Student Financial Profile

## Goal

Provide complete financial context for one student.

---

**Entry:**
```
Finance → Search Student
```

---

**Screen Layout:**

```
==================================================
Student: Adebayo Daniel
Class: JSS 1A

Fee Summary
- Term Fee: ₦150,000
- Paid:     ₦100,000
- Balance:  ₦50,000

Payment History
Date        Amount
10/07       ₦50,000
20/07       ₦50,000

[Record Payment]
==================================================
```

---

# 8. Record Payment Experience

## Goal

Allow fast and accurate payment recording.

---

**Entry:**
```
Student Profile → Record Payment
```

---

**Flow:**
```
Select Student 
  ↓ 
Confirm Fee 
  ↓ 
Enter Payment Details 
  ↓ 
Review 
  ↓ 
Confirm 
  ↓ 
Generate Receipt
```

---

# 9. Payment Entry Screen

```
==================================================
Record Payment
--------------------------------------------------
Student:            Adebayo Daniel
Outstanding Balance: ₦50,000
Payment Amount:     [                ]
Payment Method:     [ Cash | Transfer | POS ]
Reference:          [                ]

[Review Payment]
==================================================
```

---

# 10. Payment Confirmation

Financial actions require confirmation.

---

**Before saving:**

```
Please confirm:
- Student: Adebayo Daniel
- Amount:  ₦50,000
- Method:  Bank Transfer

[Confirm]   [Cancel]
```

*Avoid accidental submissions.*

---

# 11. Receipt Experience

## Goal

Provide proof of transaction.

---

**Receipt Output:**

```
==================================================
EduCore
Payment Receipt
--------------------------------------------------
Student:   Adebayo Daniel
Amount:    ₦50,000
Date:      30 July 2026
Reference: PAY-000123

[Print]   [Share]
==================================================
```

---

# 12. Outstanding Balance Management

## Goal

Identify students requiring follow-up.

---

**Screen:**

```
==================================================
Outstanding Payments
Filters: [Class] [Amount Range] [Term]
--------------------------------------------------
Student       Balance
Daniel        ₦50,000
Grace         ₦75,000

[View Student]   [Record Payment]
==================================================
```

---

# 13. Financial Reports

**Purpose:** Support school decisions.

**Examples:**
- collection summary
- outstanding balances
- payment history

**Reports should answer:**
- How much has been collected?
- What remains outstanding?
- Where are the gaps?

---

# 14. Payment States

Every payment must have visible status:
- Pending
- Completed
- Confirmed
- Reversed

*Never hide financial state.*

---

# 15. Error Prevention

Financial screens must include:

- **Validation:** Amount cannot exceed balance (unless allowed), required payment reference, and duplicate detection.
- **Confirmation:** Before irreversible actions.
- **Audit:** Record who performed actions.

---

# 16. Bursar Mobile Experience

Mobile supports:
- searching students
- checking balances
- recording simple payments

**Priority:**
1. Search Student
2. Record Payment
3. View Receipt

*Complex reports remain desktop-first.*

---

# 17. Permission Boundaries

**Bursar can:**
- ✓ Record payments
- ✓ View financial records
- ✓ Generate receipts
- ✓ View balances

**Bursar cannot:**
- ✗ Modify academic results
- ✗ Manage users
- ✗ Change system configuration

---

# 18. Empty States

- **No payments:** "No payment records yet."
- **No outstanding balances:** "All fees are up to date."

---

# 19. Success Criteria

The Bursar should be able to:
- ✓ Find any student's financial status quickly
- ✓ Record payments confidently
- ✓ Produce receipts
- ✓ Track outstanding fees
- ✓ Maintain accurate records

---

# 20. AI Agent Rules

When implementing finance workflows:
- **Prioritize:** accuracy, confirmations, audit trails, clear states.
- **Avoid:** generic finance dashboards, unnecessary complexity, unclear payment flows.

---

# 21. Final Principle

The Bursar experience should create confidence.

Every financial action should feel:
- Clear
- Confirmed
- Traceable
