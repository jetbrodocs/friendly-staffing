---
title: "Dispatch, No-shows and Replacements"
status: draft
created: 2026-10-27
updated: 2026-11-04
tags: [process, dispatch, replacements, phase-1]
---

# Dispatch, No-shows and Replacements

## Process Overview

- **Purpose:** Get approved workers to the right site at the right time, knowing the site rules, and recover quickly when someone does not show or leaves.
- **Trigger:** A worker is confirmed for an order ([proc-03](proc-03-shortlisting-and-outreach.md)), after employer approval where the employer requires it.
- **End condition:** The worker completes the shift, or a replacement covers it.
- **Frequency:** Every assignment, every shift.
- **Typical duration:** From confirmation to shift start, often less than 24 hours.

## Roles Involved

| Role | Responsibility in This Process |
|---|---|
| Office staff | Confirm workers, send instructions, maintain the daily list, arrange replacements |
| Worker | Attends the shift, follows site rules. Tells Friendly Staffing in advance if they cannot attend |
| Employer timekeeper | Receives the daily list, records attendance |
| Client supervisor | Reports no-shows, walk-offs and changes |

## Inputs

| Input | Source | Notes |
|---|---|---|
| Confirmed worker | [proc-03](proc-03-shortlisting-and-outreach.md) | |
| Site instructions | Client, site and position master | GMP rules, safety gear, break rules |

## Outputs

| Output | Destination | Notes |
|---|---|---|
| Confirmation and reminders | Worker | |
| Daily worker list | Employer timekeeper | Employee code, name, scheduled time |
| Assignment record | Worker record | Includes first day at the client, for the conversion fee |
| Incident record | Worker record | Advance cancellation, no-show or walk-off |

## Current Process (as-is)

1. Staff confirm with the worker directly, by WhatsApp or phone.
2. Staff tell the worker the site instructions verbally. Example: "Go with the safety suits."
3. Staff send the daily list of names, codes and times to the employer's timekeeper. This applies to the high-volume client.
4. The worker attends. The client keeps time ([proc-05](proc-05-weekly-timesheet-to-payroll.md)).
5. If a worker does not show or walks off, the client calls Friendly Staffing. Staff then find a replacement by repeating the manual search.

## Phase 1 Process (to-be)

1. Phlo confirms the assignment to the worker. The message includes:
   - site address, date, shift start and length
   - pay rate
   - the client's site rules for that position (e.g. hairnet, apron, safety suits)
   - the assignment details the ESA requires the agency to give
2. Phlo records the assignment.
   - If this is the worker's **first job**, the worker becomes **Active** and Phlo generates the permanent employee code, replacing the temporary code ([proc-01](proc-01-worker-registration.md)).
   - If this is the worker's first day at the client, that date is stored for the conversion-fee window.
3. Phlo sends reminders the day before and the morning of the shift.
4. Staff send the daily list to the employer's timekeeper from Phlo: employee code, name, shift time. With the Phlo timekeeping module, the daily list appears on the timekeeper's phone, where she marks arrivals and punches, and staff see live arrival counts (example: 55 of 60 arrived).
5. The worker attends and works the shift.
   - **If the worker works the shift:** the hours follow [proc-05](proc-05-weekly-timesheet-to-payroll.md).
   - **If the worker cancels in advance:** go to Exception A.
   - **If the worker does not show or walks off:** go to Exception D.
   - **If the client changes the shift on the day:** go to Exception B.

### Exception A: Worker Cancels in Advance (worker side)

A1. The worker tells Friendly Staffing they cannot attend. Staff log it on the worker's record with date, client and reason, and whether it met the notice period. [UNKNOWN: length of the notice period]
A2. Phlo opens a replacement order for the same position and shift.
A3. The replacement order goes to shortlisting ([proc-03](proc-03-shortlisting-and-outreach.md)).
A4. The cancellation counts in the worker's reliability history, as a no-show does. How this affects future ranking is set in the priority order ([proc-03](proc-03-shortlisting-and-outreach.md)).
A5. Staff tell the employer whether the replacement is covered.

### Exception B: Same-day Change

B1. Staff update the order ([proc-02](proc-02-order-intake.md), Exception A).
B2. Phlo notifies the affected workers of the new time or length.
B3. The timekeeper's daily list is updated and re-sent.

### Exception C: Client Hires the Worker Directly (temp-to-perm)

C1. The client tells Friendly Staffing it wants to hire the worker.
C2. Phlo shows the worker's first day at that client.
   - **If within the fee window (generally 6 months from the first day):** the conversion fee applies under the client's terms.
   - **If outside the window:** no fee.
C3. The worker's record is updated (status, end of assignment). Phlo invoices the fee (Phase 1, decided 2026-11-04).

### Exception D: No-show or Walk-off (employer side)

D1. The client reports the absence. Staff log it on the worker's record with date, client and reason.
D2. Staff contact the worker to find out what happened. The outcome is logged.
D3. Phlo opens a replacement order for the same position and shift, or the next one.
D4. The replacement order goes to shortlisting ([proc-03](proc-03-shortlisting-and-outreach.md)).
D5. The incident counts in the worker's reliability history.

## Build Later

- Nothing further. Conversion-fee invoices moved to Phase 1 on 2026-11-04.

## Connected Processes

- **Upstream:** [proc-03-shortlisting-and-outreach](proc-03-shortlisting-and-outreach.md).
- **Downstream:** [proc-05-weekly-timesheet-to-payroll](proc-05-weekly-timesheet-to-payroll.md).

## Systems and Tools

| Step | System/Tool | How It's Used |
|---|---|---|
| As-is 1–3 | WhatsApp, phone | Confirmation and lists |
| Phase 1 steps 1–4 | Phlo, messaging provider | Confirmation, reminders, daily list |

## Known Issues

| Issue | Impact | Current Workaround |
|---|---|---|
| Workers claim they were not told site rules | Incidents, client complaints | Verbal instructions |
| Walk-offs without notice | Lost hours, replacement scramble | Client calls; manual search |

## Open Questions

1. What are the conversion-fee amounts and windows per client?
2. Should a no-show or advance cancellation lower a worker's ranking, and by how much? (Set by Tejash and the office leads in the priority order.)
3. What notice period must a worker give to cancel in advance?
4. Is the worker marked Active when they accept the first offer, or on the first day worked?
5. Should workers acknowledge receipt of the site rules (a reply or a tick), as evidence?
