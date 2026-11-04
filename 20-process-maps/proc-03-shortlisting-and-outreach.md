---
title: "Shortlisting, Outreach and Confirmation"
status: draft
created: 2026-10-27
updated: 2026-11-04
tags: [process, shortlisting, communication, phase-1]
---

# Shortlisting, Outreach and Confirmation

## Process Overview

- **Purpose:** Fill each order with willing, eligible workers, with employer approval only where the employer requires it.
- **Trigger:** An order is recorded ([proc-02](proc-02-order-intake.md)).
- **End condition:** Enough willing, eligible workers are confirmed to cover the order. Where the employer requires approval, it has approved them.
- **Frequency:** Every order, including replacements.
- **Typical duration:** Hours. Same-day orders must close within a few hours.

## Roles Involved

| Role | Responsibility in This Process |
|---|---|
| Office staff | Shortlist, message and call workers. Send profiles to the employer |
| Worker | Accepts or declines the offer |
| Tejash Jain and office leads | Set and change the shortlisting priority order |
| Employer (some employers only) | Approves or rejects workers, or runs a trial |

## Inputs

| Input | Source | Notes |
|---|---|---|
| Order | [proc-02](proc-02-order-intake.md) | Includes position requirements and pay rate |
| Worker database | [proc-01](proc-01-worker-registration.md) | Validated workers only (Inactive or Active) |
| Priority order | Tejash Jain and office leads | Editable at any time in Phlo |

## Outputs

| Output | Destination | Notes |
|---|---|---|
| Confirmed workers for the order | Dispatch ([proc-04](proc-04-dispatch-and-replacements.md)) | |
| Message and call log | Worker and order records | |

## Current Process (as-is)

1. Staff search their own office's database for people who could fit.
2. Staff judge fit by:
   - distance from home
   - past role
   - past pay against the offered pay (example: someone who earned $24–25 is unlikely to stay at an $18 job)
3. Staff send WhatsApp messages to candidates. Openings are also posted daily on Friendly Staffing's WhatsApp Status.
4. Staff call candidates who do not reply.
5. Staff tell the candidate the job details: where it is, what it involves, the pay.
6. When a candidate agrees, staff share the details with the client. For roles such as forklift operator, this includes the licence.

## Phase 1 Process (to-be)

1. Phlo builds a ranked shortlist for the order.
   - **Eligibility filters:** Validated (Inactive or Active), valid permit, study-permit hours within the weekly cap, required licences, availability for the shift.
   - **Ranking:** the priority order set by Tejash and the office leads. There is one order for the whole business, which can be overridden for a specific client or role. They can change the factors and their order at any time in Phlo. The ranking never uses gender, age or medical status.
2. Staff review the list and select candidates. Example: five for two openings.
3. Phlo sends the offer to the selected workers by WhatsApp Business and email, with SMS as a fallback. The offer states site, date, shift and pay, and asks the worker to reply 1 for yes or 0 for no.
4. Phlo waits for replies.
   - **If no reply within about 30 minutes:** go to Exception A.
   - **If the worker replies 0 (no):** go to Exception B.
   - **If the worker replies 1 (yes):** go to step 5.
5. Phlo checks whether this employer requires approval.
   - **If not (the usual case):** the worker is confirmed and moves to dispatch ([proc-04](proc-04-dispatch-and-replacements.md)). Friendly Staffing is responsible for sending workers with the right qualifications and experience.
   - **If yes:** go to Exception C.
6. When confirmed workers cover the order, it is marked filled. Remaining yes-replies are thanked and released.

### Exception A: No Reply

A1. Phlo prompts staff to call the worker.
A2. Staff call and log the outcome on the worker's record.
A3. Return to step 4 with the worker's answer.

### Exception B: Declined or Rejected

B1. The decline or rejection is logged on the worker's record.
B2. Phlo offers the opening to the next worker on the ranked list. Return to step 3.
B3. If the list is exhausted, staff widen the search, for example to workers whose past pay was higher.

### Exception C: Employer Requires Approval or a Trial

Applies only to employers set up with their own approval process or trial. Phase 1 includes one standardised workflow for both. The detailed steps are designed with Friendly Staffing during the build.

C1. Staff send the worker's details to the employer for approval, for example by email. The request is logged against the order.
C2. Staff record the employer's decision.
   - **If approved:** the worker moves to dispatch.
   - **If rejected:** go to Exception B.
C3. For a trial, staff record the trial date and outcome; the outcome counts as the employer's decision.
C4. [UNKNOWN: what the employer sees, and what happens if it does not reply in time]

## Build Later

- Workers can log in to a portal, see open roles and apply. Applications enter the same ranked shortlist.
- Ontario job-posting rules apply to public postings: pay range, AI-screening disclosure, no Canadian-experience requirement.

## Connected Processes

- **Upstream:** [proc-01](proc-01-worker-registration.md), [proc-02](proc-02-order-intake.md).
- **Downstream:** [proc-04-dispatch-and-replacements](proc-04-dispatch-and-replacements.md).

## Systems and Tools

| Step | System/Tool | How It's Used |
|---|---|---|
| As-is 3–4 | WhatsApp, phone | Offers and follow-up |
| Phase 1 steps 1–4 | Phlo shortlist; WhatsApp Business, email and SMS providers | Ranked list, bulk offers, logged replies |
| Exception C | Email, logged in Phlo | Approval for employers that require it |

## Known Issues

| Issue | Impact | Current Workaround |
|---|---|---|
| Fit judged from memory | Unreliable placements, e.g. high past earners who leave | Staff questions |
| Total dependence on WhatsApp | Exposure to future per-message pricing | None |

## Open Questions

1. For employers that require approval: what do they see, and what happens if they do not reply? How are trials run?
2. Does AI-assisted shortlisting from the internal database trigger Ontario's AI-disclosure rule? (Specialist question.)
