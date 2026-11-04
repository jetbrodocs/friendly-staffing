---
title: "Follow-up Meeting with Friendly Staffing"
status: in-review
created: 2026-11-03
updated: 2026-11-03
tags: [observation, meeting, worker-status, shortlisting, approval, replacements, orders, pay-type, payroll, invoicing]
---

# Follow-up Meeting with Friendly Staffing

## Source

Rohan Patel's notes from the follow-up meeting with the Friendly Staffing team, shared 2026-11-03. Raw notes: [rohan-notes-2026-11-03-client-meeting](../00-inbox/rohan-notes-2026-11-03-client-meeting.md). Rohan's answers to the follow-up questions are in [qa-2026-11-03-rohan-meeting-clarifications](qa-2026-11-03-rohan-meeting-clarifications.md). Rohan shared the notes in two parts: part 1 covers operations (sections 1 to 6), part 2 covers pay and invoicing (sections 7 to 12).

## Observations

### 1. Employee code and worker status

- The employee code is created only when the worker is assigned **their first job**, not before.
- Before the first job, the worker is **Inactive**. On the first assignment, the worker becomes **Active** and the code is generated.
- Until then, a **temporary code** can identify the worker.
- **Changes:** the 2026-10-26 answer (Q5) that the code is assigned at Ready to Work.

### 2. Shortlisting and priority order

- The logic for shortlisting and prioritising candidates must stay **dynamic**.
- Friendly Staffing must be able to change the priority order themselves.
- **Changes:** the earlier assumption that priority rules are supplied once, at development start.

### 3. Two kinds of workers: contractual and direct deduction

- Workers are either **contractual** or **direct deduction**.
- They are paid differently. See section 9.

### 4. Employer approval is the exception, not the rule

- In most cases the employer does **not** approve workers before they are sent.
- Friendly Staffing is responsible for sending workers with the right qualifications and experience for the employer's requirements.
- Some employers have their own approval process, or run **trials**. These need a separate approval workflow. Approval may happen over email.
- Trials may happen physically or in another way. Trials are to be scoped later.
- **Changes:** the Phase 1 flow, which had employer approval of every shortlisted worker as a standard step.

### 5. No-shows and replacements, from both sides

- A replacement or no-show can be raised by the **worker** or by the **employer**.
- Friendly Staffing staff have actions to perform when a worker does not show, so that a replacement is arranged.
- **Changes:** the Phase 1 flow, which covered only the employer reporting a no-show.

### 6. Orders can be added to, edited or deleted

- Employers often change their requirements as the job date approaches.
- Staff must be able to add, edit or delete an employer's request.
- **Changes:** the Phase 1 flow, which covered changes but not deletion.

## Part 2: Pay and Invoicing Today

### 7. Time capture

- A **timekeeper at every job location** manages punch-ins and punch-outs every day.
- At the end of the week, Friendly Staffing receives the week's attendance and hours as a timesheet PDF. Example: [obs-client-timesheet-molinaros](obs-client-timesheet-molinaros.md).
- **Differs from:** the 2026-10-21 workshop, where smaller clients were said to use fingerprint punch machines. [UNVERIFIED: whether both arrangements exist]

### 8. The payroll Excel sheet

- The timesheet data is entered into an **Excel sheet**.
- The sheet is a database of Friendly Staffing's workers, grouped under employer names.
- For each worker it holds:
  - the going rate for the job the worker is on
  - the rate at which the worker is a contractor, or the rate at which they are employed
  - the payment method the worker prefers
- Regular and overtime rates differ.
- The sheet produces each worker's **gross pay**.
- This is the payroll Excel sample Friendly Staffing has been asked for. [UNKNOWN: sample still awaited]

### 9. Two payment methods

| | Payment method A: direct deduction | Payment method B: subcontractor |
|---|---|---|
| How the worker is treated | As an employee ("full-time employees") | As a subcontractor |
| Government deductions | Applied | None |

- Workers are often given the choice of payment method.
- A worker can choose **A, B, or both**.
- Processing gives a **final figure after deductions** for each worker. It is used both for the accounts and for the bank payment.
- [UNKNOWN: where the method A deductions are calculated: in the Excel sheet or in QuickBooks]
- [UNKNOWN: how pay is split when a worker chooses both]

### 10. QuickBooks pay stub and bank payment

1. Once the method A and method B figures are ready, staff create a **pay stub in QuickBooks** for each worker.
2. Under the employer, staff enter:
   - the worker's name
   - hours worked
   - payment type (A or B)
   - the final pay for that payment type
3. Staff record the transaction.
4. Staff export an **XML file** from QuickBooks. The XML is preferred over a QuickBooks summary.
5. Staff import the XML into the **bank portal**, which processes the payments.

Rohan's summary of the purpose: the worker's correct gross pay is recorded, the right deductions are applied for the chosen payment method, QuickBooks holds the right transactions, and the bank receives the right figures for the right workers.

### 11. Client invoicing

- The same Excel sheet, built from the timesheets, is used to **invoice clients**.
- There are very few clients, so invoices are recorded manually in QuickBooks.
- QuickBooks generates the invoice. It is sent to the employer, who pays it.

### 12. Frequency and margin

- Payroll and invoicing both run **weekly**.
- Friendly Staffing's **margin is yet to be decided**, and how it works is not yet fully understood.
