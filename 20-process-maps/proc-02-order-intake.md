---
title: "Client Order Intake"
status: draft
created: 2026-10-27
updated: 2026-10-27
tags: [process, orders, client, phase-1]
---

# Client Order Intake

## Process Overview

- **Purpose:** Capture each client request for workers accurately, once, whatever channel it arrives on.
- **Trigger:** A client supervisor asks for workers, or changes an existing request.
- **End condition:** The order is recorded and handed to shortlisting.
- **Frequency:** Several times a day. Same-day changes are common at the high-volume client.
- **Typical duration:** Lead time is often less than 24 hours ("Tomorrow I need 8 AM for one day").

## Roles Involved

| Role | Responsibility in This Process |
|---|---|
| Client supervisor | Places and changes orders |
| Tejash Jain | Takes many orders by phone. Posts them to staff |
| Office staff | Record orders and act on them |

## Inputs

| Input | Source | Notes |
|---|---|---|
| Order | Client supervisor | Phone, text, email, or a WhatsApp group set up for that supervisor |
| Order change | Client supervisor | Example: the 3 PM shift moved to 5 PM as a 12-hour shift |
| Client and position terms | Agreement with client | Bill rate per position. Contracts are not binding, as clients use up to three agencies |

## Outputs

| Output | Destination | Notes |
|---|---|---|
| Order | Shortlisting ([proc-03](proc-03-shortlisting-and-outreach.md)) | Client, site, position, count, date, shift start and length |

## Current Process (as-is)

1. Client supervisor sends the order by phone, text, email or the supervisor's WhatsApp group.
   - Tejash moved high-volume orders to written WhatsApp groups. Phone orders led to confusion, such as 8 o'clock versus 10 o'clock.
2. Tejash (or the receiving staff member) posts the order in the internal staff WhatsApp group "order friendly".
3. Staff in each office pick it up and start searching their own database.
4. If the client changes the order, the change arrives the same way. Staff adjust the people already scheduled.

## Phase 1 Process (to-be)

0. **Set-up, once per client:** staff record the client, its sites and its supervisors. For each position they record:
   - bill rate
   - default pay rate
   - requirements (e.g. forklift licence)
   - break rules
   - site instructions (GMP, safety gear)
   - conversion-fee terms
1. The order arrives:
   - **Employer portal (online form via URL):** the order lands in Phlo directly. Go to step 3.
   - **Email:** Phlo reads the order inbox and drafts an order for staff to confirm. Go to step 2.
   - **Phone, text or WhatsApp:** staff enter the order, or paste the WhatsApp message into Phlo. Go to step 2.
2. Staff check and complete the order: client, site, position, number of workers, date, shift start and length.
3. Phlo loads the position's rates, requirements and site rules onto the order.
4. Every message with the employer about the order is logged against it.
5. The order goes to shortlisting.

### Exception A: Same-day Change

A1. The client changes the time, length or number of workers.
A2. Staff update the order in Phlo. The change and its source are logged.
A3. Phlo lists the confirmed workers affected. Staff notify them, and the timekeeper's daily list is updated ([proc-04](proc-04-dispatch-and-replacements.md)).
A4. If more workers are needed, the extra openings return to shortlisting.

### Exception B: Replacement Order

B1. A no-show or walk-off creates a replacement order automatically ([proc-04](proc-04-dispatch-and-replacements.md), Exception A).
B2. The replacement order goes straight to shortlisting.

## Phase 2 Changes

- No change to intake. Automatic reading of WhatsApp groups remains under assessment.

## Connected Processes

- **Upstream:** Client relationship and position set-up.
- **Downstream:** [proc-03-shortlisting-and-outreach](proc-03-shortlisting-and-outreach.md).

## Systems and Tools

| Step | System/Tool | How It's Used |
|---|---|---|
| As-is 1–2 | Phone, WhatsApp groups, email | Orders and internal hand-off |
| Phase 1 step 1 | Employer portal, email reading, manual entry | One order record per request |

## Known Issues

| Issue | Impact | Current Workaround |
|---|---|---|
| Orders spread across channels | Missed or misread orders | Per-supervisor WhatsApp groups |
| WhatsApp groups cannot be read automatically (encryption) | Staff re-key orders | Copy and paste in Phase 1 |
| Frequent same-day changes | Wrong people at the wrong time | Phone calls |

## Open Questions

1. Who in the Friendly Staffing team owns updating confirmed workers after a change? Rohan: the team is responsible, but the process is open.
2. Will clients use the employer portal, or will most orders still arrive by phone and WhatsApp?
3. What are the conversion-fee terms per client?
