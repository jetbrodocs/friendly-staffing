---
title: "Workshop Call with Tejash Jain (2026-10-21)"
status: in-review
created: 2026-10-26
updated: 2026-10-27
tags: [observation, interview, workshop, operations]
---

# Workshop Call with Tejash Jain (2026-10-21)

**Source:** `00-inbox/workshop-call-2026-10-21-fathom-transcript.md` (raw transcript) and `00-inbox/workshop-call-2026-10-21-fathom-summary.md` (Fathom's AI summary). This file is the structured capture of that call.

## Location / Station

- **Area:** Remote video call, recorded on Fathom (58 min)
- **Station/Cell:** n/a
- **Address/Building:** Friendly Staffing offices, Mississauga, Ontario (see [obs-worker-registration-form](obs-worker-registration-form.md))

**Attendees:**
- Tejash Jain, promoter of Friendly Staffing. He joined under the display name "Priya Jain", so the transcript labels him that way.
- Rohan Patel (Jetbro).
- Honey Darji (Jetbro).

## Activity

Tejash described how Friendly Staffing fills client orders today. The steps are:
1. Taking the order.
2. Finding workers.
3. Messaging them.
4. Dispatching them.
5. Collecting hours.
6. Preparing payroll.

He also described the system he wants. This document records what he said. Rohan's later phase decisions are in [qa-2026-10-26-rohan-scope-clarifications](qa-2026-10-26-rohan-scope-clarifications.md).

## Business Model (as described)

- **Type of agency.** Friendly Staffing is a **temp-to-perm** agency. A worker typically works at a client for 4–6 months. If the worker is good, the client hires them onto its own payroll.
- **Conversion fee.** If the client hires after the contract period, Tejash charges nothing. If the client hires early (for example, after one week), he charges a fee.
- **Workers.** Mostly new immigrants looking for "survival jobs" until they find work in their own field. Tejash said "pretty much 99%" come via referral.
- **Database segments.** About 3,000–5,000 records in three groups:
  - **Active:** worked recently.
  - **Not available:** worked before, not working now.
  - **Past:** has left.

  Past workers still matter. When a new opening is announced, they refer relatives who have just arrived.
- **Contracts.** "Contract do not hold any value." Many clients use up to three agencies, so the contract only records the agreed bill rate. Tejash does not want contracts in the system.
- **Rates.**
  - **Pay rate:** the hourly rate paid to the worker.
  - **Bill rate:** the hourly rate charged to the client.
  - The bill rate is fixed per position for the client. If no worker accepts the usual pay rate, Tejash may raise the pay rate for one worker (example: $18 → $18.15). The client does not pay the extra.
- **Billing and payroll timing.** Weekly. All hours from all clients for the week are collected, payroll is prepared, and invoices go to clients.

## Inputs

| Input | Source | Format | Notes |
|---|---|---|---|
| Client order | Client supervisor | Phone call, text, email, or a dedicated WhatsApp group per supervisor | Example: "10 people at 8 o'clock, 8 at 10 o'clock". Tejash created per-supervisor WhatsApp groups so orders are in writing and staff errors can be traced |
| Order changes | Client supervisor | Phone / WhatsApp, same day | Example: the 3 PM shift moved to 5 PM as a 12-hour shift. The 8 AM shift moved to 10 AM as a 10-hour shift |
| Worker profile | Worker | Paper registration form | See [obs-worker-registration-form](obs-worker-registration-form.md) |
| Client timesheet | Client timekeeper / supervisor | Paper, faxed weekly | See [obs-client-timesheet-molinaros](obs-client-timesheet-molinaros.md) |

## Outputs

| Output | Destination | Format | Notes |
|---|---|---|---|
| Job offer message | Shortlisted workers | WhatsApp message, then a phone call if no reply | Also posted daily on Friendly Staffing's WhatsApp Status |
| Daily worker list | Client timekeeper | List with employee code, name, scheduled time | Sent for the high-volume client |
| Weekly hours per worker | Payroll | Excel | Taken into QuickBooks for payroll |
| Weekly invoice | Client | [UNKNOWN: format] | Based on hours worked |

## People

| Role | Count | Shift/Schedule | Notes |
|---|---|---|---|
| Tejash Jain (promoter) | 1 | Takes client calls throughout the day | Left the call twice to take client calls |
| Office staff | "All three staff" | [UNKNOWN] | Watch the order WhatsApp group, search the database, call workers |
| Offices | 2 | n/a | Each office keeps its own database, and neither can see the other's |
| On-site timekeeper (high-volume client) | [UNKNOWN] | Client site | Tejash: "happening at client's site, but done by my employee". He trains the workers placed there |

## Timing

- **Lead time:** Often less than 24 hours. Example: "Tomorrow I need [someone at] 8 AM for one day." An order placed last evening was rescheduled this morning.
- **Order size:** From 1 worker to dozens.
- **Volume swing:**
  - High-volume client: 60–100% up or down.
  - Smaller clients: ±1–2 people.
- **Payroll cycle:** Weekly.

## Current Shortlisting Process (as described)

1. Tejash posts the order in the staff WhatsApp group "order friendly".
2. Staff search their own office's database.
3. Staff send WhatsApp messages to candidates, then call those who don't reply.
4. Staff judge fit by:
   - distance from home
   - past role
   - past pay compared with the offered pay

   Example: a worker who earned $24–25 is unlikely to stay at an $18 job, so "don't hire him".

## Desired System (Tejash's words, condensed)

1. **One database for both offices.** Staff at either office see the same records.
2. **Shortlist on entry.** When an order is entered, the system screens the database for eligible candidates and lists them in priority order:
   1. Active and working at this client now ("worked yesterday").
   2. Worked before, still looking.
   3. Others.
   4. Workers whose past pay is well above the offer go to the bottom, contacted only when everyone else is exhausted.
3. **Bulk offer and replies.** Staff tick candidates (for example, 5 for 2 openings) and send an offer. Workers reply "1" for yes and "0" for no.
4. **No-reply alert.** If there is no reply in about 30 minutes, the system prompts staff to call.
5. **Confirmation and instructions.** Staff accept a "yes" and the order is filled. The worker then automatically receives the client- and position-specific instructions.
   - Example: GMP rules at a food plant, such as hairnet, apron, no eating on the floor.
   - Example: safety suits.
6. **Reminders.** Email and text reminders, like a car-service booking: on booking, the day before, and the morning of.
7. **Employer portal.** Clients submit requirements on the Friendly Staffing website.
8. **WhatsApp group intake (desired).** Orders posted in a supervisor's WhatsApp group feed the system automatically. Fallback: staff copy and paste the message into the system.
9. **Tablet timekeeping at the client site (Phase 2 in the call).**
   - Shows the day's scheduled list.
   - Records arrival, punch-in, breaks and punch-out.
   - Sends the worker a confirmation of each punch, so the worker can't dispute hours later.
   - Shows office staff live arrival counts (example: 55 of 60 arrived).
10. **Weekly payroll Excel.** Per worker: hours, regular/OT split, rate, gross. Government deductions were "not focus at this time" in the call.
11. **Payroll software.** A later stage, to replace QuickBooks.

## Problems and Workarounds

| Problem | Frequency | Current Workaround | Impact |
|---|---|---|---|
| Two office databases in silos | Constant | Staff search only their own office | Smaller candidate pool, duplicate effort |
| Many workers share names (e.g. 20 "Manpreet Singh/Kaur") | Constant | Tejash created the employee code | Code is the only reliable identifier |
| Order times confused (8 vs 10 o'clock) | Recurring | Orders moved to written WhatsApp groups | Wrong people at wrong time |
| Worker walks off without telling the supervisor | Recurring (example the day before the call) | Client calls for a replacement for the next day and the day after | Lost hours, client goodwill |
| Workers claim they were not told site rules (e.g. safety suits) | Recurring | Verbal instructions | On-site incidents, client complaints |
| Total dependence on WhatsApp | Constant | None | Tejash fears per-message pricing: "one cent will cost me like $10,000" |
| QuickBooks cost rose from about $250 to $8,000 [UNKNOWN: per year?], with plans to charge per employee | Annual | None | Per-employee pricing does not suit high-turnover temp staffing |
| Hours disputes | [UNKNOWN] | Worker initials each day on the paper sheet | Disputes after the fact |

## Systems

| System | Used For | Notes |
|---|---|---|
| WhatsApp (status, groups, direct messages) | Job posts, staff coordination, client orders | Free today. Tejash fears future pricing |
| Spreadsheets | Worker database, weekly hours | One per office |
| QuickBooks | Payroll | Cost escalating |
| Client punch machines (smaller clients) | Hours | Fingerprint machines |

## Open Questions

1. How is a worker marked inactive versus past? Is there a time rule?
2. What are the conversion fee amounts and conditions?
3. Does the weekly cycle run Sunday–Saturday (the timesheet's column order) or Monday–Sunday?
