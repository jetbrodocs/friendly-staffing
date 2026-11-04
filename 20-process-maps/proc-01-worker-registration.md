---
title: "Worker Registration and Validation"
status: draft
created: 2026-10-27
updated: 2026-11-03
tags: [process, onboarding, worker, phase-1]
---

# Worker Registration and Validation

## Process Overview

- **Purpose:** Turn a person who walks in or is referred into a validated worker who can be offered shifts.
- **Trigger:** A worker arrives at either office, usually referred by someone who has worked with Friendly Staffing.
- **End condition:** The worker is **Validated (Inactive)**, holds a temporary code and is searchable by both offices. The permanent employee code is generated later, on the first job assignment ([proc-04](proc-04-dispatch-and-replacements.md)).
- **Frequency:** [UNKNOWN: registrations per week]
- **Typical duration:** [UNKNOWN]

## Roles Involved

| Role | Responsibility in This Process |
|---|---|
| Worker | Fills in and signs the registration form. Provides documents |
| Office staff (registering associate) | Hands out the form, verifies documents, enters the record. Accountable if a verification later proves wrong |
| Tejash Jain | Owns the employee code scheme |

## Inputs

| Input | Source | Notes |
|---|---|---|
| Registration form | Worker | Paper today. Fields listed in [obs-worker-registration-form](../10-observations/obs-worker-registration-form.md) |
| Identity and work-eligibility documents | Worker | [UNKNOWN: which documents, and whether copies are kept] |
| Referral | Existing or past worker | About 99% of workers come by referral |

## Outputs

| Output | Destination | Notes |
|---|---|---|
| Worker record | Office spreadsheet today; central worker database in Phase 1 | |
| Temporary code | Worker record | Identifies a worker before the first job. Looks different from the employee code |
| Employee code | Worker record, client lists, timesheets | Format Y MM NNN, e.g. 207 103. Generated on the first job assignment, not at registration |

## Current Process (as-is)

1. Worker arrives at one of the two Mississauga offices.
2. Staff give the worker the one-page paper registration form.
3. Worker fills in the form by hand and signs it. Pay history, references and certifications are not on the form.
4. Staff check the worker's documents. [UNVERIFIED: exact checks]
5. Staff enter the record into **their own office's** spreadsheet. The other office cannot see it.
6. Staff assign the employee code. Tejash said the code is assigned when the worker is first sent to a client, but the sample form carries the code at registration. [2026-11-03 meeting: the code is generated only when the worker is assigned the first job.]
7. Staff ask the worker to save Friendly Staffing's WhatsApp number, so the worker sees openings posted on WhatsApp Status.

## Phase 1 Process (to-be)

1. Worker fills in the registration form on Friendly Staffing's website, with no login. Alternatively, staff enter a paper form on the worker's behalf.
2. The worker gives consent on the form:
   - to storing their data
   - to their profile being shared with employers
   - to receiving job messages, with an opt-out in every message
3. The record enters the central worker database with status **Registered**.
4. Staff validate the record:
   - identity
   - SIN, and its expiry for 9-series SINs
   - residency status
   - work permit **type** (open or employer-specific) and expiry
   - study permit, if any
   - licences and certifications the worker claims (e.g. forklift)
   - payment method chosen: A (direct deduction), B (subcontractor), or both with the hours split
   - TD1 and TD1ON, for method A income tax
   - bank details for the payment file
5. Staff check whether the record is complete and valid.
   - **If valid:** go to step 6.
   - **If not:** go to Exception A.
6. Staff mark the worker **Validated**. The worker is **Inactive** until the first job. The system:
   - assigns a temporary code, which looks different from the employee code
   - records the registering associate
7. The worker becomes visible to both offices for shortlisting ([proc-03-shortlisting-and-outreach](proc-03-shortlisting-and-outreach.md)).
8. On the first job assignment, the worker becomes **Active** and the system generates the permanent employee code in Friendly Staffing's existing format ([proc-04](proc-04-dispatch-and-replacements.md), step 2).

### Exception A: Incomplete or Invalid Record

A1. Staff record what is missing or invalid.
A2. The worker is asked for the missing items. The record stays **Registered** and cannot be shortlisted.
A3. When the items arrive, return to step 4.

### Exception B: Permit Nearing Expiry (ongoing)

B1. The system flags workers whose work or study permit, or 9-series SIN, is nearing expiry.
B2. Staff contact the worker for renewal evidence.
B3. An expired permit blocks the worker from shortlisting until it is renewed.

### One-off: Data Migration at Go-live

M1. Both offices' spreadsheets are imported once.
M2. Duplicates across offices are merged. Existing employee codes are kept.
M3. Imported workers are mapped to the new statuses: workers who have worked before are Active and keep their code; validated workers who never worked are Inactive.

## Phase 2 Changes

- Workers log in to a self-serve portal to update their profile and documents ([proc-03](proc-03-shortlisting-and-outreach.md) covers browsing and applying for openings).

## Connected Processes

- **Upstream:** Referral by existing or past workers.
- **Downstream:** [proc-03-shortlisting-and-outreach](proc-03-shortlisting-and-outreach.md).
- **Related:** [analysis-canada-ontario-regulatory-review](../30-analysis/analysis-canada-ontario-regulatory-review.md) (consent, permits, Human Rights Code limits on form questions).

## Systems and Tools

| Step | System/Tool | How It's Used |
|---|---|---|
| As-is 2–5 | Paper form, office spreadsheet | Handwritten, then re-keyed per office |
| Phase 1 steps 1–3 | Website form, Phlo worker database | Single record for both offices |
| Phase 1 steps 6–8 | Phlo | Temporary code at validation; employee code at first job |

## Known Issues

| Issue | Impact | Current Workaround |
|---|---|---|
| Two office databases in silos | Smaller candidate pool, duplicate records | None |
| Many workers share names | Mix-ups | Employee code |
| Form lacks past pay, references, certifications | Staff judge fit from memory or phone calls | Verbal questions |
| Form asks gender, date of birth, criminal record, medical limits | Human Rights Code risk if used in selection | None |

## Open Questions

1. Which documents do staff verify today, and are copies kept?
2. Is there a newer version of the registration form?
3. Which digit of the employee code identifies the registering associate?
4. Should past pay rate and references be added to the Phase 1 form?
5. Is the worker's payment method (A direct deduction, B subcontractor, or both) chosen at registration or at the first job? Can it change later?
6. Does a worker who leaves and returns keep the original employee code?
