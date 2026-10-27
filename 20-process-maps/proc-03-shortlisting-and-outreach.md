---
title: "Shortlisting, Outreach and Employer Approval"
status: draft
created: 2026-10-27
updated: 2026-10-27
tags: [process, shortlisting, communication, phase-1]
---

# Shortlisting, Outreach and Employer Approval

## Process Overview

- **Purpose:** Fill each order with willing, eligible workers whom the employer approves.
- **Trigger:** An order is recorded ([proc-02](proc-02-order-intake.md)).
- **End condition:** The employer has approved enough workers to cover the order.
- **Frequency:** Every order, including replacements.
- **Typical duration:** Hours. Same-day orders must close within a few hours.

## Roles Involved

| Role | Responsibility in This Process |
|---|---|
| Office staff | Shortlist, message and call workers. Send profiles to the employer |
| Worker | Accepts or declines the offer |
| Employer | Approves or rejects shortlisted workers |

## Inputs

| Input | Source | Notes |
|---|---|---|
| Order | [proc-02](proc-02-order-intake.md) | Includes position requirements and pay rate |
| Worker database | [proc-01](proc-01-worker-registration.md) | Only Ready to Work workers |

## Outputs

| Output | Destination | Notes |
|---|---|---|
| Approved workers for the order | Dispatch ([proc-04](proc-04-dispatch-and-replacements.md)) | |
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
   - **Eligibility filters:** Ready to Work, valid permit, study-permit hours within the weekly cap, required licences, availability for the shift.
   - **Ranking:** Friendly Staffing's priority rules (to be supplied at development start). The ranking never uses gender, age or medical status.
2. Staff review the list and select candidates. Example: five for two openings.
3. Phlo sends the offer to the selected workers by SMS, WhatsApp or email (channel to be decided). The offer states site, date, shift and pay, and asks the worker to reply 1 for yes or 0 for no.
4. Phlo waits for replies.
   - **If no reply within about 30 minutes:** go to Exception A.
   - **If the worker replies 0 (no):** go to Exception B.
   - **If the worker replies 1 (yes):** go to step 5.
5. Staff share the worker's profile with the employer.
6. The employer reviews the profile.
   - **If approved:** the worker moves to dispatch ([proc-04](proc-04-dispatch-and-replacements.md)).
   - **If rejected:** go to Exception B.
7. When approved workers cover the order, it is marked filled. Remaining yes-replies are thanked and released.

### Exception A: No Reply

A1. Phlo prompts staff to call the worker.
A2. Staff call and log the outcome on the worker's record.
A3. Return to step 4 with the worker's answer.

### Exception B: Declined or Rejected

B1. The decline or rejection is logged on the worker's record.
B2. Phlo offers the opening to the next worker on the ranked list. Return to step 3.
B3. If the list is exhausted, staff widen the search, for example to workers whose past pay was higher.

## Phase 2 Changes

- Workers can log in to a portal, see open roles and apply. Applications enter the same ranked shortlist.
- Ontario job-posting rules apply to public postings: pay range, AI-screening disclosure, no Canadian-experience requirement.

## Connected Processes

- **Upstream:** [proc-01](proc-01-worker-registration.md), [proc-02](proc-02-order-intake.md).
- **Downstream:** [proc-04-dispatch-and-replacements](proc-04-dispatch-and-replacements.md).

## Systems and Tools

| Step | System/Tool | How It's Used |
|---|---|---|
| As-is 3–4 | WhatsApp, phone | Offers and follow-up |
| Phase 1 steps 1–4 | Phlo shortlist, messaging provider | Ranked list, bulk offers, logged replies |
| Phase 1 steps 5–6 | Email with secure link, or the employer portal | Employer approval |

## Known Issues

| Issue | Impact | Current Workaround |
|---|---|---|
| Fit judged from memory | Unreliable placements, e.g. high past earners who leave | Staff questions |
| Total dependence on WhatsApp | Exposure to future per-message pricing | None |

## Open Questions

1. What priority rules and order will Friendly Staffing supply?
2. Which outreach channel: SMS, WhatsApp Business or email?
3. What exactly does the employer see when approving a profile?
4. Does AI-assisted shortlisting from the internal database trigger Ontario's AI-disclosure rule? (Specialist question.)
