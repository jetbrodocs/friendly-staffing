---
title: "Q&A: Tejash's Reply to the Information Request (2026-11-04)"
status: in-review
created: 2026-11-04
updated: 2026-11-04
tags: [observation, qa, payroll, bank-file, statutory, roe, t4, vacation-pay]
---

# Q&A: Tejash's Reply to the Information Request (2026-11-04)

## Source

- Tejash Jain's WhatsApp reply to Jetbro's information request ([qa-2026-11-03-rohan-meeting-clarifications](qa-2026-11-03-rohan-meeting-clarifications.md), "Information Requested"). Raw text: [tejash-reply-2026-11-04-information-request](../00-inbox/tejash-reply-2026-11-04-information-request.md).
- What the attached samples show: [obs-client-payroll-samples-2026-11-04](obs-client-payroll-samples-2026-11-04.md).
- Rohan's decisions on the follow-up questions, 2026-11-04.

## Tejash's Answers

**T1. Payroll Excel and pay stubs.** Attached.

**T2. Bank XML file.** None exists. Staff enter about **350 payments by hand into QuickBooks** for payroll, then **again by hand into the bank payment portal**, using the figures from QuickBooks.

**T3. Client invoice.** Attached.

**T4. How pay is calculated for methods A and B.**
- **Method B:** hours worked × pay rate.
- **Method A:** QuickBooks calculates the deductions. Tejash pointed to the CRA's Payroll Deductions Online Calculator as the reference.

**T5. How net pay is worked out from gross pay.** Same as T4.

**T6. Payroll in Phlo, QuickBooks for bookkeeping.** Correct.

**T7. Should Phlo take over CRA remittances, T4s, ROEs and WSIB?**
- "Everything related to payroll has to come from Phlo."
- ROEs: Phlo must produce the **ROE.BLK** file to upload to the government site.
- Only bookkeeping and accounting stay in QuickBooks.

## What This Corrects

| Earlier record | Corrected 2026-11-04 |
|---|---|
| Method A deductions are calculated in the payroll Excel, then verified in QuickBooks (Rohan, P1, 2026-11-03) | The Excel produces gross pay only. **QuickBooks calculates the method A deductions** |
| Staff export an XML file from QuickBooks and import it into the bank portal (meeting notes, 2026-11-03) | **No file exists.** Every payment is keyed twice: into QuickBooks, then into the bank portal |
| Vacation pay assumed added to each weekly pay (S6, 2026-11-03) | Vacation pay is **accrued** over an October to September year and **paid once a year** as a lump sum (sample stub) |
| Phlo calculates statutory figures; filing happens outside Phlo (S1, 2026-11-03) | Phlo produces the **filing files** as well: ROE.BLK for ROE Web, T4 slips and the T4 electronic filing file. Payments to the government are still made outside Phlo |

## Rohan's Clarification: Bill Rate (2026-11-04)

There are two rates:
- **Pay rate:** what Friendly Staffing pays the worker.
- **Bill rate:** what the client is invoiced. When creating invoices, staff **add a margin to the pay rate by hand** to derive the bill rate, which then goes on the invoice.

This replaces the 2026-11-03 note that the bill rate is independent of the pay rate and its derivation unknown. [UNKNOWN: whether the margin is a percentage or a fixed amount per hour, and whether it differs by client or position]

## Rohan's Decisions (2026-11-04)

| Question | Decision |
|---|---|
| Which bank, and what upload format does the portal accept? | Open. Settled once the main scoping starts. The bank upload file stays its own module |
| Should Phlo produce the T4 electronic filing file for CRA, as well as the slips? | **Yes** |
| What do the payment mode codes (A20, A24, A40, "A20 Only", 2D) mean, and what is rate C for? | Ask Tejash. Listed as an open question in the client document |
| Is rate B always 90% of rate A? | Ask Tejash. Listed as an open question in the client document |
| How are statutory holiday pay and bonuses decided today? | Ask Tejash. Listed as an open question in the client document |
| What is the "E3P" field on the form, and why is commute recorded? | Ask Tejash. Listed as an open question in the client document |
| Are office staff or owners paid through the same payroll? | Not answered. Kept as an internal open question |

## Rohan's Scope Decisions (2026-11-04, later the same day)

- **Client invoicing moves into Phase 1.** Weekly invoices from Phlo: billable hours × bill rate, extra charges, conversion fees, 13% HST. Invoices are pushed to QuickBooks accounts.
- **"Phase 2" is renamed "Build later".** It holds receivables tracking, the worker self-serve job portal and loaded margin and profitability reporting.
- **QuickBooks leaves payroll completely.** Bookkeeping and accounting stay in QuickBooks.
- **Timekeeping build approach is an open decision.** How Friendly Staffing's own timekeeping is built (a mobile app, or other options) is still to be decided by Jetbro. It drives the final development and implementation cost.
- [ASSUMED: receivables tracking and reminders stay in Build later, as only invoicing was named]

## Consequences for Phase 1 Scope

- **Deduction engine.** The CRA calculator has no interface Phlo can call. Phlo implements the CRA payroll deduction formulas (federal and Ontario) itself and updates them each January and July.
- **Bank upload file.** Replaces double keying of about 350 payments a week. Format depends on the bank.
- **Vacation pay accrual.** Phlo tracks each method A worker's balance, pays it once a year, and pays it out when a worker leaves (shown on the ROE).
- **Statutory files.** ROE.BLK, T4 slips and the T4 electronic filing file, remittance figures, WSIB figures.
- **Bill rate from pay rate.** Phlo derives each bill rate as pay rate plus a margin set per client and position, instead of staff adding it by hand. The invoice itself stays Phase 2.
- **Earnings types.** Hourly, overtime, statutory holiday, bonus, vacation.
- **Parallel run.** Phlo's net pay is checked against QuickBooks for at least one cycle before QuickBooks payroll is switched off.
