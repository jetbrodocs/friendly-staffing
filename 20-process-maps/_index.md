---
title: "Process Maps Index"
status: active
updated: 2026-11-03
---

# Process Maps

Each map shows the current process (as-is), the Phase 1 process (to-be) and what Phase 2 changes. Sources are in `10-observations/`.

## Main Flow

```
Worker registration ──► Validated (Inactive) ─┐
                                              ├─► Shortlist ─► Offer ─► [Employer approval, some employers only] ─► Dispatch (first job: Active + employee code) ─► Shift (Phlo timekeeping) ─► Phlo payroll, stubs, bank XML ─► QuickBooks accounts (P1) / client invoice (P2)
Client order intake (add / edit / delete) ────┘                                                                    ▲                │
                                                                                                                   └── replacement ◄┘ worker cancels / no-show / walk-off
```

## Sub-processes

1. [Worker registration and validation](proc-01-worker-registration.md): form, validation, Registered → Validated (Inactive) → Active, temporary and employee codes, data migration
2. [Client order intake](proc-02-order-intake.md): all channels, changes, cancellations, replacement orders
3. [Shortlisting, outreach and confirmation](proc-03-shortlisting-and-outreach.md): editable priority order, bulk offers, 1/0 replies, call prompts, approval for some employers
4. [Dispatch, no-shows and replacements](proc-04-dispatch-and-replacements.md): confirmations, first-job activation, site rules, daily list, worker- and employer-side no-shows, temp-to-perm
5. [Weekly timesheet to payroll and invoicing](proc-05-weekly-timesheet-to-payroll.md): own timekeeping, checks, payment methods A and B, payroll, stubs and bank XML in Phlo (Phase 1); invoicing (Phase 2)
