---
title: "Payroll, Invoice and Timesheet Samples from Friendly Staffing"
status: in-review
created: 2026-11-04
updated: 2026-11-04
tags: [observation, artifact, payroll, pay-stub, vacation-pay, roe, t4, invoicing, timekeeping, registration]
---

# Payroll, Invoice and Timesheet Samples from Friendly Staffing

## Source

Tejash Jain sent ten files on 2026-11-04 in reply to Jetbro's information request. His written answers are in [qa-2026-11-04-tejash-information-reply](qa-2026-11-04-tejash-information-reply.md). Raw reply and file list: [tejash-reply-2026-11-04-information-request](../00-inbox/tejash-reply-2026-11-04-information-request.md).

The files hold SINs, pay figures, names and addresses. They stay in `00-inbox/` and are git-ignored. This note records structure only: no worker names, SINs or account numbers.

**Redaction note:** the black boxes on the T4 and ROE samples cover the image only. The SINs and the CRA payroll account number are still in the PDF text layer.

## 1. Payroll Excel (`Report file.xlsx`)

Two sheets.

**Data sheet: one row per worker.**

| Column | Notes |
|---|---|
| Employee code | "Y MM NNN" format, e.g. "607 123" |
| Full name | Some names carry a suffix such as "- 1" or "- 18" [UNKNOWN: meaning] |
| Phone | |
| Payment mode | Values seen: `A`, `B`, `A20`, `A24`, `A40`, `A20 Only`, `2D` [UNKNOWN: meaning of the numbered codes] |
| Commute | Car or Bus [UNKNOWN: why it is recorded] |
| Position | Short codes: FL, GL, M/C, Palletizer, Skill |
| First day of work | Date |
| Pay rate A | Entered by hand, e.g. $17.60 to $22.45 |
| Pay rate B | Formula: **rate A × 0.9** |
| Pay rate C | Formula: **rate A × 0.85** [UNKNOWN: what rate C is used for] |
| Client | Empty in the sample |

**Weekly time sheet: one row per worker per timesheet page.**

- Header: "Payment on" date (a Friday, 2026-08-14 in the sample).
- Columns: timesheet page code (R1, RA10, Z1, Z2, Z6, RA6), position, employee code, name, mode (looked up from the data sheet).
- Hours are entered by hand in four columns: type A regular, type A overtime, type B regular, type B overtime.
- Pay formula, per method: regular hours × rate + overtime hours × 1.5 × rate. Overtime pay is always 1.5 times the pay rate in the sheet.
- Totals: regular, overtime and total hours; total pay A; total pay B.
- A second block (type, name, regular hours, overtime hours, invoice number) is laid out for invoicing but empty.

**What the sheet does not do:** it calculates **gross pay only**. No CPP, EI, income tax or vacation pay appears in it.

**Split example:** a worker on mode `2D` has 16 regular hours under A and 28 regular hours plus 5.33 overtime hours under B. All the overtime sits under B.

## 2. QuickBooks pay stubs (three `.xps` files)

All three are QuickBooks "Employee Paystub" documents, paid by "DirectPay".

### Weekly pay stub (method A worker)

- Pay period Sunday 2026-09-13 to Saturday 2026-09-19. Cheque date Friday 2026-09-25: paid six days after the week ends.
- Hours shown as hours:minutes: 41:05 at $17.60 = $723.07.
- Withholdings: CPP employee, EI employee, and a single "Federal Income Tax" line.
- Year-to-date earnings lines: Hourly, Overtime, Statutory Holiday, Bonus ($500).
- No vacation pay line on the weekly stub.

**Check against 2026 rates:**
- CPP: ($723.07 − $3,500 ÷ 52) × 5.95% = $39.02. Matches.
- EI: $723.07 × 1.63% = $11.79. Matches.
- Income tax $74.34 is close to federal plus Ontario tax combined for this pay. The single "Federal Income Tax" line appears to include Ontario tax. [UNVERIFIED]

### Vacation pay stub ("once a year")

- Pay period 2025-10-01 to 2026-09-30. Cheque date 2026-11-06.
- One earnings line, "Vac.", with CPP, EI and income tax withheld.
- **Vacation pay is accrued over a year running October to September and paid as one lump sum**, about five weeks after the year closes.
- This answers the open question of whether vacation pay is added to each weekly pay: it is not.

### Monthly salary stub (2017)

- An owner's monthly salary. CPP and income tax withheld; no EI.
- Shows a second pay frequency (monthly) and an EI-exempt employee. [UNKNOWN: whether office staff or owners are still paid through this payroll]

## 3. Client invoice (Molinaro's, 2026-08-31)

- A QuickBooks invoice template from 1953039 Ontario Inc., with the GST/HST number.
- One line per **position**, each with a regular bill rate and an overtime bill rate. The overtime bill rate is about 1.5 times the regular one.
- About 25 position lines across sanitation, sauce making, lab, maintenance mechanics (four levels), shipping and receiving, forklift and supply chain.
- Non-hour charges on the same invoice: **safety shoes** and **consulting fees**.
- HST at 13%. Terms: due 3 days after receipt.
- Footer: the service period (a part week, 23 to 25 August) and "For QA, Cleaning and Shipping/Receiving".
- Invoice number format: "26 105".
- Each bill rate is the worker's pay rate plus a margin that staff add by hand (Rohan, 2026-11-04).

## 4. Record of Employment (ROE)

- Issued electronically through ROE Web ("Service Canada has already received a copy").
- Pay period type W (weekly). Employer payroll reference number shown.
- Boxes used: first day worked, last day paid, final pay period end, total insurable hours, total insurable earnings, insurable earnings for each pay period (up to 53 boxes), reason code (E: quit), expected recall (unknown), contact, issuer.
- Box 17 (vacation pay, statutory holiday pay and other monies paid on separation) is blank in this sample.
- The sample was issued in October 2021 for employment that ended in July 2020.
- Tejash wants Phlo to produce the **ROE.BLK** file, ROE Web's bulk upload format.

## 5. T4 slips (2025)

- Two standard T4 slips, two copies on each page.
- Boxes used: 14 employment income, 16 CPP, 16A second CPP, 18 EI, 22 income tax (zero in both), 24 EI insurable earnings, 26 CPP pensionable earnings, 10 province (ON), 45 dental benefits (code 1).
- Both samples are small annual amounts, typical of short assignments.

## 6. Timesheets: two more formats

### Molinaro's department sheet (handwritten, faxed)

- The same Molinaro's template as before ([obs-client-timesheet-molinaros](obs-client-timesheet-molinaros.md)), one sheet per department (Screening; QC Sanitation).
- Week Sunday 2026-10-18 to Saturday 2026-10-24.
- Per day: sign-in, sign-out and hours. Columns for regular and overtime hours.
- "Each employee must initial to acknowledge in and out time." Supervisor signature and date on each page.
- Corrections from the previous week are written in ("0.50 last week").
- The fax header date (April 2026) is wrong, so fax timestamps cannot be trusted.

### Zebra Packaging sheet (typed by Friendly Staffing)

- Header: Friendly Staffing name and contact, "Week Starting: 25-Oct-26".
- Workers grouped by shift: Days, Afternoons, Nights. Name with employee code in brackets.
- Daily hours in decimals, Sunday to Saturday. Total, regular and overtime ("after 44 hrs reg").
- A position or cost code per worker: WH-PRINT Helper, HEADOFFICE, WH-GLUE Helper.
- "Approved By" with the client's name and signature, dated 2026-11-03. A handwritten note confirms the head-office rows.
- So for some clients, **Friendly Staffing prepares the sheet and the client signs it off**.

**Employer sign-off:** both formats carry the client's signature before Friendly Staffing processes them.

## 7. Registration form (11 August 2026 version)

- Same fields as the older form ([obs-worker-registration-form](obs-worker-registration-form.md)).
- Both office addresses in the letterhead.
- An unlabelled **"E3P"** field at the top right [UNKNOWN: meaning].
- No employee code field on this version.

## Open Questions

1. What do the payment mode codes A20, A24, A40, "A20 Only" and 2D mean?
2. Is rate B always 90% of rate A? What is rate C (85%) used for?
3. How are statutory holiday pay and bonuses decided today?
4. What is the "E3P" field on the form? Why does the worker list record commute?
5. What do the name suffixes ("- 1", "- 18") and the timesheet page codes (R1, RA10, Z1) mean?
6. Are office staff or owners paid through the same payroll?
