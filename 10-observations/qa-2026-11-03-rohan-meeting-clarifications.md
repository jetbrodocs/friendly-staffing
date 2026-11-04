---
title: "Q&A: Rohan's Meeting Clarifications (2026-11-03)"
status: in-review
created: 2026-11-03
updated: 2026-11-03
tags: [observation, qa, worker-status, shortlisting, approval, orders, proposal]
---

# Q&A: Rohan's Meeting Clarifications (2026-11-03)

## Source

Rohan Patel (Jetbro) answered two rounds of follow-up questions on 2026-11-03: seven questions after part 1 of the follow-up meeting notes, and payroll questions after part 2 ([obs-client-meeting-2026-11-03](obs-client-meeting-2026-11-03.md)). The answers below are Rohan's own words, lightly condensed.

## Purpose of the Exercise

Rohan set the goal for the observations and the process-map updates:

- The output is a **proposal to Friendly Staffing** for an end-to-end staffing and recruitment platform.
- The proposal gives **scope, timeline and cost. Nothing else.**
- Detailing within the scope happens later.

## Answers

**Q1. Should the temporary code look different from the permanent employee code? Does a returning worker keep the code?**

It can look different; that is fine.
[UNKNOWN: whether a worker who leaves and returns keeps the original code]

**Q2. How do Inactive and Active relate to the current statuses?**

The sequence is: **Registered → Validated (Inactive) → Active**.
[UNKNOWN: whether Active is set when the worker accepts the first offer or on the first day worked]

**Q3. Who can change the shortlisting priority order?**

Tejash Jain and the office leads.
[UNKNOWN: whether there is one order for the business, or one per client or position]

**Q4. What is the difference between contractual and direct-deduction workers?**

Answered in part 2 of the meeting notes ([obs-client-meeting-2026-11-03](obs-client-meeting-2026-11-03.md), section 9):

- **Payment method A (direct deduction):** the worker is treated as an employee and government deductions apply.
- **Payment method B (subcontractor):** no deductions apply.
- Workers choose the method. A worker can choose A, B or both.

**Q5. Where an employer requires approval, what does it approve, and what happens if it does not reply?**

The approval workflow is yet to be created.

**Q6. When a worker cancels in advance, is there a notice period, and does it count against the worker like a no-show?**

Yes.
[UNKNOWN: the length of the notice period]

**Q7. If an employer deletes an order after workers are confirmed or have arrived, are workers paid anything? Is the employer charged?**

- Employers typically never cancel once workers have arrived.
- Cancellation after confirmation can happen.
- There is no cancellation fee as such.

## Payroll Answers and Phase Change

**P1. Where are method A deductions calculated today?**

In the payroll Excel. They are then verified in QuickBooks.

**P2. When a worker uses both methods, how is pay split?**

- By hours. Regular hours are split, and so are overtime hours.
- The split does not change week to week.
- The system must allow the split to be changed later.

**P3. Which bank, and what XML format?**

Not known yet and not needed for the proposal. Keep the bank file as its own task or module.

**P4. Can the pay rate differ between method A and method B for the same job?**

Details not known yet. The estimate should allow for the variability, with slightly more hours.

**P5. Can overtime pay and bill rates be set separately rather than as 1.5 times the regular rate?**

Yes, they can be.

**Other points Rohan added:**

- **No workers are paid outside the bank file.** Method A and method B workers are all paid through the bank.
- **Pay rate and bill rate are independent.** Gross pay, deductions and pay stubs all use the pay rate. The bill rate is agreed separately between Friendly Staffing and each client. How bill rates are derived is not yet understood.
- **Timekeeping:** every site has a timekeeper today. Friendly Staffing's own timekeeping must be a separate module inside Phlo. It stays in scope now; whether it is built later can be agreed later.
- **QuickBooks cost:** Friendly Staffing pays about CAD 8,000 a year to QuickBooks for payroll and accounts. Removing payroll from QuickBooks reduces this considerably.

## Decision: Payroll, Bank File and Timekeeping Move to Phase 1

Tejash recommended, in the last call, that payroll finalisation and pay stubs move into Phlo, with the final amounts then pushed to QuickBooks accounts, which records the transactions. Rohan asked to move timekeeping, payroll management and the bank XML from Phase 2 into Phase 1. Jetbro confirmed on 2026-11-03.

| Moves to Phase 1 | Stays in Phase 2 |
|---|---|
| Own timekeeping (separate module, tablet at site) | Client invoicing and receivables |
| Payroll: payment methods A and B, hour split, CPP/EI/tax, vacation and holiday pay | Worker self-serve job portal |
| TD1/TD1ON at onboarding | Loaded margin and profitability reporting |
| Pay stubs | |
| Bank XML payment file (own task, format to be confirmed) | |
| Final amounts pushed to QuickBooks accounts | |

Rohan confirmed the Phase 2 column: the worker job portal, client invoicing and receivables, and loaded margin and profitability all stay in Phase 2.

**Supersedes:** the 2026-10-26 decision (follow-up F3) that Phase 1 only shows deductions calculated by QuickBooks.

**QuickBooks keeps the books:** bookkeeping and journal entries stay in QuickBooks. Only payroll calculation and pay-stub creation move to Phlo.

**Statutory figures (decided later the same day):** Phlo calculates remittance amounts and produces T4s, ROEs and WSIB figures in Phase 1. The actual payments to and from the government are made outside Phlo.

## Information Requested from Friendly Staffing

- payroll Excel and pay-stub samples
- a bank XML file (redacted)
- a client invoice
- how method A and method B pay is calculated
- how net pay is calculated from gross pay
- whether vacation pay is added to each weekly pay (asked of Tejash separately)

## Scope, Sizing and Timeline Answers

**S1. Statutory filing.** The calculation happens in Phlo. Payments to and from the government stay outside Phlo. Remittance figures, T4, ROE and WSIB are in scope (Phase 1).

**S2. Messaging channels.** WhatsApp Business and email, with SMS as a fallback.

**S3. Employer approval and trials.** Most employers need no approval. Where an employer requires approval or a trial, a separate, standardised workflow is built. It is in the Phase 1 scope.

**S4. Priority order.** One order for the whole business, which can be overridden for specific clients or roles.

**S5. Employer sign-off on hours.** Rohan asked whether timesheets are approved and signed by the employer before they reach Friendly Staffing. The Molinaro's sample shows a supervisor signature on every page and worker initials on every day ([obs-client-timesheet-molinaros](obs-client-timesheet-molinaros.md)). [UNVERIFIED: whether every client signs, and whose employee the timekeeper is]

**S6. Vacation pay.** Assumed added to each weekly pay. To be confirmed with Tejash.

**S7. Users and timekeeping.**
- 4 to 5 Friendly Staffing staff will use Phlo.
- No tablets. The timekeeper manages attendance on her phone.
- Workers sign for their hours on their own phones.
- The attendance workflow is still to be designed: marking present and absent, breaks, punching in and out.

**S8. Volume.** 300 to 400 workers paid in a typical week.

**S9. Data migration.** Both offices' spreadsheets, the payroll Excel, and QuickBooks year-to-date payroll history.

**S10. Language.** English only. [UNKNOWN: hosting region]

**S11. Target go-live.** 15 January 2027.

**S12–S13. Commercial model.** Recorded separately, outside git.

