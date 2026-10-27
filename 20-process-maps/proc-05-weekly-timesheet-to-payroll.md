---
title: "Weekly Timesheet to Payroll"
status: draft
created: 2026-10-27
updated: 2026-10-27
tags: [process, timekeeping, payroll, quickbooks, phase-1, phase-2]
---

# Weekly Timesheet to Payroll

## Process Overview

- **Purpose:** Turn each week's worked hours into accurate pay for workers and billable hours for clients.
- **Trigger:** The work week ends. The employer's signed timesheet arrives.
- **End condition:**
  - **Phase 1:** verified, rated hours are handed to QuickBooks, and deductions are shown back.
  - **Phase 2:** workers are paid and clients invoiced.
- **Frequency:** Weekly, for every worker at every client.
- **Typical duration:** The fax arrives Monday about 8 AM. [UNKNOWN: time to payroll]

## Roles Involved

| Role | Responsibility in This Process |
|---|---|
| Employer timekeeper / supervisor | Records in and out times. Signs each page |
| Worker | Initials each day to acknowledge the times |
| Office staff | Capture and verify the timesheet. Prepare the payroll file |
| QuickBooks (Phase 1) | Calculates payroll and statutory deductions; handles CRA, WSIB, T4 and ROE |

## Inputs

| Input | Source | Notes |
|---|---|---|
| Weekly timesheet | Employer timekeeper | Paper, handwritten, faxed. See [obs-client-timesheet-molinaros](../10-observations/obs-client-timesheet-molinaros.md) |
| Assignments | [proc-04](proc-04-dispatch-and-replacements.md) | Who was scheduled where, when |
| Pay rate and bill rate | Position master, or an exception agreed with the worker | |

## Outputs

| Output | Destination | Notes |
|---|---|---|
| Weekly payroll file | QuickBooks | Format to match Tejash's sample (awaited) |
| Deductions and net pay | Phlo worker record | Imported from QuickBooks |
| Hours summary | Employer and worker | |
| Margin report | Tejash | (Bill rate − pay rate) × hours, before employer costs |

## Current Process (as-is)

1. Workers sign in and out on the client's system:
   - smaller clients use fingerprint punch machines
   - the high-volume client uses a physical timekeeper and Friendly Staffing's paper sheet
2. Each worker initials each day. The supervisor signs each page.
3. The weekly sheets are faxed to Friendly Staffing on Monday morning. Example: 17 pages, about 115 workers, Molinaro's, week of 2026-08-10.
4. Staff read the handwritten sheets and total regular hours and overtime (above 44 hours) per worker.
5. Staff prepare an Excel sheet per worker: hours, rate, gross.
6. Staff take the Excel into QuickBooks, which runs payroll and statutory deductions.
7. Staff prepare client invoices from the same hours. [UNVERIFIED: how invoices are prepared today]

## Phase 1 Process (to-be)

1. The employer's timekeeper sends the signed weekly timesheet. **The employer's record is the source of truth in Phase 1.**
2. Staff upload the scan to Phlo and enter each worker's daily in and out times against their assignments.
3. Phlo checks the hours:
   - worked hours match a confirmed assignment
   - break rules for the client and position, at or above the ESA eating-period minimum
   - overtime after 44 hours, counted across **all clients** the worker worked for that week
   - minimum pay rules, e.g. the three-hour rule when a shift is cut short
   - study-permit weekly hour cap
   - pay rate at or above Ontario minimum wage ($17.95/hr from 2026-10-01)
4. Phlo flags any exceptions.
   - **If exceptions:** go to Exception A.
   - **If none:** go to step 5.
5. Phlo applies rates: pay rate × hours and bill rate × hours, split into regular and overtime.
6. Phlo flags any assignment where the pay rate is above the bill rate.
7. Phlo produces the weekly payroll file for QuickBooks.
8. Staff load the file into QuickBooks, which runs payroll:
   - CPP, EI and income tax
   - vacation and public holiday pay
   - remittances, T4, ROE and WSIB
9. Staff import the QuickBooks payroll results into Phlo. Deductions and net pay are **shown** on each worker's weekly record.
10. Phlo sends the hours summary to the employer and to each worker.
11. Phlo updates the margin report: (bill rate − pay rate) × hours by worker, order, client and week, before employer costs.

### Exception A: Hours Do Not Check

A1. Staff review the flagged line: missing punch, hours without an assignment, a break below the minimum, or a study-permit cap breach.
A2. Staff resolve it with the employer. The conversation is logged.
A3. Staff correct the entry. Return to step 3.

## Phase 2 Changes

1. **Own timekeeping:** a tablet at the client site records punches and breaks, and confirms each punch to the worker. Phlo compares its record with the employer's.
2. **Digital approval:** the employer approves the hours in Phlo instead of signing and faxing.
3. **Payroll in Phlo:** this replaces QuickBooks. It covers:
   - TD1/TD1ON, CPP, EI, income tax
   - vacation and public holiday pay
   - pay stubs and the bank deposit file
   - CRA remittances, T4, ROE (triggered by 7-day earnings interruptions) and WSIB premiums
4. **Invoicing:** bill rate × approved billable hours, plus 13% HST, plus conversion fees. Receivables are tracked and reminders sent.
5. **Reporting:** loaded margin after employer costs, and profitability by client.
6. **Cut-over:** QuickBooks year-to-date payroll history is imported, and one cycle runs in parallel before QuickBooks is retired.

## Connected Processes

- **Upstream:** [proc-04-dispatch-and-replacements](proc-04-dispatch-and-replacements.md).
- **Downstream:** QuickBooks payroll (Phase 1); invoicing and payments (Phase 2).
- **Related:** [analysis-canada-ontario-regulatory-review](../30-analysis/analysis-canada-ontario-regulatory-review.md).

## Systems and Tools

| Step | System/Tool | How It's Used |
|---|---|---|
| As-is 1–3 | Client punch machines, paper sheet, fax | Time capture |
| As-is 5–6 | Excel, QuickBooks | Payroll |
| Phase 1 steps 2–7 | Phlo | Capture, checks, rates, export |
| Phase 1 steps 8–9 | QuickBooks, Phlo | Payroll run, deductions shown |

## Known Issues

| Issue | Impact | Current Workaround |
|---|---|---|
| Handwritten, faxed sheets | Slow, error-prone re-keying; OCR unreliable | Manual reading |
| Hours in hours:minutes | Conversion errors | Manual conversion |
| QuickBooks cost rose from about $250 to $8,000, with per-employee pricing planned | Unsuited to high-turnover staffing | Phase 2 replacement |
| Hours disputes | Rework, worker complaints | Worker initials per day |

## Open Questions

1. What format is Tejash's weekly payroll Excel (sample awaited)?
2. How often are workers paid, and how?
3. Is lunch paid at any client? What do the three rows per worker on the timesheet mean?
4. How are invoices prepared today?
5. Can QuickBooks payroll results be exported in a form Phlo can import each week?
