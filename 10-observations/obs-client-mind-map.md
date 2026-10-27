---
title: "Client Mind Map — Current State and Target Platform"
status: in-review
created: 2026-10-26
updated: 2026-10-26
tags: [observation, artifact, client-requirements]
---

# Client Mind Map — Current State and Target Platform

## Source

- **File:** `00-inbox/Mind Map for Friendly Staffing Oct 2026.docx`, dated 2026-10-16. This predates the 2026-10-21 workshop.
- **Voice:** written from Friendly Staffing's side ("our current setup", "for us").
- **Status (Rohan, 2026-10-26):** Tejash wants everything in it eventually. Phase 1 is narrower (see [qa-2026-10-26-rohan-scope-clarifications](qa-2026-10-26-rohan-scope-clarifications.md)).

## Stated Current State

- **Disconnected methods.** The document says there are "six major operational methods that do not fully connect", but lists five:
  1. manual recruitment
  2. spreadsheet scheduling and timesheets
  3. separate payroll software
  4. manual invoicing
  5. phone/text/email communications
- **Core problem.** The same information is transferred between people, spreadsheets, payroll and invoicing tools. The result is duplicate entry and inconsistent records.
- **Main goal.** One connected workflow from client job order to placement, approved hours, payroll and client invoice.

## Stated Handoff Problems

| Handoff | Problem stated |
|---|---|
| Client → Recruitment | Job details arrive by phone, text or email |
| Recruitment → Scheduling | Availability and job requirements are stored separately |
| Scheduling → Onboarding | Worker documents and assignment details can be incomplete |
| Timesheets → Payroll | Hours are collected manually and re-entered |
| Payroll → Invoicing | Payable and billable hours may not match |
| Invoicing → Client payment | Invoices are prepared and tracked manually |
| All → Compliance | Records are scattered across files and email |

## Stated Target Modules

1. Client and job-order management (client, site, role, shift, skills, bill rate, pay rate, approval rules)
2. Recruitment and worker database (applicants, screening, qualifications, availability, assignment history)
3. Digital onboarding and compliance (forms, acknowledgements, expiry dates, readiness check before placement)
4. Scheduling and shift dispatch (matching, confirmation, replacements)
5. Mobile time capture and approval (attendance, breaks, exceptions, client approval)
6. Payroll and statutory deductions (CPP, EI, income tax, remittances, T4, ROE)
7. Automated invoicing and collections (rates, markups, taxes, receivables, overdue follow-up)
8. Management dashboards and audit trail (fill rate, payroll exceptions, gross margin, client profitability, receivables, compliance)

**Stated design rule:** One approved time record drives both payroll and invoicing, but each is calculated independently:
- **Payroll:** approved hours × pay rate, plus OT, premiums and deductions.
- **Invoicing:** approved billable hours × bill rate, plus charges and taxes.
- Payable time and billable time may differ.

## Stated Ontario Compliance Needs

- **Payroll:** CRA payroll, T4s and ROEs.
- **Ontario employment standards:** configurable OT (44 hours/week), vacation pay, public holiday pay, wage statements.
- **Agency obligations:** temporary help agency requirements, client and assignment records.
- **Safety records:** WSIB records, safety orientation and training records.
- **Data handling:** document expiry reminders, role-based access, audit logs, backups and retention.

## Stated Implementation Plan (5 phases)

1. Standardise data.
2. Automate time and scheduling.
3. Connect payroll and invoicing.
4. Compliance and reporting.
5. Pilot at one client site before full migration.

This conflicts with Rohan's rule of exactly two phases. The pilot idea (one site, compare against the existing process) can still apply inside Phase 1.

## Stated KPIs

1. Time to fill.
2. Shift fill rate.
3. Timesheet accuracy.
4. Payroll accuracy.
5. Invoice turnaround.
6. Billing leakage.
7. Gross margin.
8. Days sales outstanding (DSO).
9. Administrative effort.
10. Compliance readiness.

## Open Questions

1. What is the sixth "operational method" the document mentions?
2. Which compliance, dashboard and KPI items go to Phase 1, which to Phase 2, and which are out of scope?
3. Does "client approval" of timesheets (module 5) mean the supervisor signature used today, or a digital approval?
