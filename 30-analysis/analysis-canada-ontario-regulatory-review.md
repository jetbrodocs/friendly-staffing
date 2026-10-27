---
title: "Canada and Ontario Regulatory Review"
status: draft
created: 2026-10-27
updated: 2026-10-27
tags: [analysis, compliance, regulatory, ontario, payroll]
---

# Canada and Ontario Regulatory Review

## Summary

Friendly Staffing (1953039 Ontario Inc.) is an Ontario temporary help agency. In law it is the **employer** of every worker it places. That makes it responsible for:
- payroll deductions and remittances to the CRA
- Ontario Employment Standards Act (ESA) pay rules
- Records of Employment (ROEs)
- WSIB premiums

The inbox documents name the main rules, but they miss several that hit Phase 1 directly:
- the 2026 Ontario job-posting rules, including disclosure when AI is used to screen candidates
- the ESA limits on temp-to-perm conversion fees
- the Ontario Human Rights Code limits on what can be asked or used when screening workers
- anti-spam consent for bulk SMS and email

This is a business-analysis review, not legal advice. Every item needs confirmation by an Ontario employment/payroll specialist before build.

## Sources

**Inbox documents:**
- `00-inbox/Mind Map for Friendly Staffing Oct 2026.docx`
- `00-inbox/jetbro-draft-platform-journey-2026-10.pdf`
- `00-inbox/jetbro-draft-journey-flow-2026-10.pdf`
- `00-inbox/CCF_003355.pdf` (registration form)
- `00-inbox/23083148_260817.pdf` (Molinaro's timesheet)
- [obs-workshop-call-2026-10-21](../10-observations/obs-workshop-call-2026-10-21.md)

**Web research (2026-10-27):** secondary sources (law firms, news, payroll vendors), listed under References. The Ontario.ca ESA guide is the only primary source consulted.

## Plain-Language Primer: TD1 and TD1ON

- **What they are.** TD1 (federal) and TD1ON (Ontario) are short forms each worker fills in once when hired, and again when their situation changes. On them, the worker claims personal tax credits, such as the basic personal amount, a spouse or dependants, or being a student.
- **What they do.** The employer uses them to decide how much income tax to hold back from each paycheque. If a worker submits nothing, the employer withholds as if they claim only the basic personal amount.
- **Who needs them.** Only whoever calculates the income tax deduction. Today that is presumably QuickBooks [UNCONFIRMED].
  - If Phase 1 **shows** deductions that QuickBooks calculates, TD1s stay with QuickBooks.
  - If our system **calculates** income tax, TD1 and TD1ON collection becomes a Phase 1 onboarding step.

## Findings

### A. Payroll and tax (federal: CRA, Service Canada)

| # | Rule | Where it appears in inbox | What it means here | Phase |
|---|---|---|---|---|
| A1 | **Source deductions:** CPP (and the second-tier CPP2), EI premiums and income tax withheld from every pay, then remitted to the CRA on the employer's remittance schedule | Mind map, both Jetbro drafts | Pay rate × hours → gross → deductions → net. Rohan wants deductions "shown and managed" | Calculation and remittance: Phase 2 (payroll). Display in Phase 1: [DECISION NEEDED] |
| A2 | **TD1 / TD1ON** collected at hire | Jetbro drafts | See primer above | Follows A1 |
| A3 | **SIN** collected; 9-series SINs (temporary residents) carry an expiry date | Form: "SIN # … Valid Until" | Store SIN encrypted, and use it only for payroll and tax. Track the SIN expiry for 9-series SINs | Phase 1 (onboarding) |
| A4 | **T4 slips** issued to each worker by the end of February for the prior year | Mind map, drafts | High turnover means thousands of T4s a year | Phase 2 |
| A5 | **ROE** issued to Service Canada after an **interruption of earnings**: generally 7 consecutive days with no work and no insurable earnings, or when Service Canada asks | Drafts say "ROE issued when assignment ends" | **Draft is inaccurate.** For a temp agency, the end of one client assignment is not itself the trigger. A gap between assignments can be. The system needs to detect 7-day no-work gaps per worker | Phase 2 (data captured in Phase 1) |
| A6 | **HST (13% Ontario)** charged on client invoices, with the GST/HST number shown | Drafts | Invoice line: billable hours × bill rate + HST | Phase 2 (invoicing) |

### B. Ontario Employment Standards Act (ESA)

| # | Rule | Where it appears | What it means here | Phase |
|---|---|---|---|---|
| B1 | **Overtime** at 1.5× after **44 hours per week** | Mind map, drafts. Confirmed on the Molinaro's sheet (44:00 Reg + OT) | The weekly total must split Reg/OT at 44 hours across **all clients the worker worked at that week**, not per client [VERIFY] | Phase 1 (timesheet output) |
| B2 | **Minimum wage:** $17.95/hr general from **2026-10-01** (was $17.60) | Not in inbox | Reject or flag any pay rate below the minimum. Worth noting for the $18 example rate | Phase 1 (rate setup) |
| B3 | **Vacation pay:** minimum 4% (6% after 5 years with the employer) | Drafts | Calculated on each pay for temp workers, or accrued | Phase 2 |
| B4 | **Public holiday pay** | Mind map, drafts | Formula based on wages earned in the 4 weeks before the holiday | Phase 2 |
| B5 | **Eating period:** 30 minutes after no more than 5 hours of work; unpaid unless agreed | Drafts ("breaks per ESA minimums") | Break rules are client-specific (Rohan Q14) but must meet this floor. The "30 min lunch paid" remark from the call needs confirmation | Phase 1 (hours calculation) |
| B6 | **Three-hour rule:** a worker who regularly works more than 3 hours and is sent home early is paid at least 3 hours [VERIFY current wording] | Not in inbox | Relevant when production changes cut a shift short. The paid hours can then differ from hours worked | Phase 1 (timesheet rules) |
| B7 | **Wage statement** (pay stub) on or before each pay day | Mind map, drafts | Phase 2 output | Phase 2 |
| B8 | **Record keeping:** pay and hours records kept 3 years | Mind map ("retention controls") | Phase 1 timesheets are payroll records. Keep them for 3 years minimum | Phase 1 |
| B9 | **Assignment information.** The agency must give each worker written information about each assignment [VERIFY exact list]: <br>• agency name and contact details<br>• client name and address<br>• wage rate<br>• hours of work<br>• pay period and pay day<br>• a general description of the work | Not in inbox | The confirmation message Tejash wants (site rules, GMP) can also carry this required information | Phase 1 (confirmation message) |
| B10 | **No fees to workers** for registering, being assigned, résumé help or interview prep | Not in inbox | Confirms the current practice. The system should never bill workers | n/a |
| B11 | **Temp-to-perm fee limit.** An agency cannot charge a client a fee for hiring the worker directly unless the fee is charged within **6 months** of the worker's first day at that client. The agency cannot stop a worker from taking a direct job | Tejash: contract 4–6 months; "if they hire after one week, I charge them fees" | Tejash's practice fits the rule. The system must track each worker's **first day at each client** and only allow a fee inside that 6-month window. The sources differ on wording [VERIFY] | Phase 1 (assignment history). Fee invoicing: Phase 2 |
| B12 | **Shared liability.** The agency and the client are jointly and severally liable for the worker's unpaid regular wages and overtime [VERIFY] | Not in inbox | Accurate cross-verified timesheets protect both sides | Phase 1 |
| B13 | **Temp help agency licence.** Required to operate in Ontario since **2024-07-01**: <br>• $25,000 irrevocable letter of credit<br>• $750 fee<br>• annual renewal<br><br>Clients may not knowingly use an unlicensed agency | Mind map ("temporary help agency requirements") | Not a software feature. Confirm Friendly Staffing holds a licence and store the number for client documents | Out of scope (business) |

### C. Ontario job-posting rules (from 2026-01-01, employers with 25+ employees)

| # | Rule | What it means here | Phase |
|---|---|---|---|
| C1 | Public job postings must state the **expected pay or a pay range** | Applies to the Phase 2 job board. May also apply to openings posted on WhatsApp Status [VERIFY] | Phase 2. Advisory now |
| C2 | Postings must disclose when **AI is used to screen, assess or select** applicants | Phase 1 uses AI-assisted shortlisting. Does internal shortlisting of the existing database count as a "posting"? [VERIFY with specialist] | Phase 1 (risk) |
| C3 | Postings and application forms cannot require **Canadian experience** | Check the registration form and the job master data | Phase 1 |
| C4 | Postings must state whether there is an **existing vacancy** | Phase 2 job board | Phase 2 |
| C5 | Applicants who were **interviewed** must be told the outcome within 45 days. Keep postings 3 years [single source, VERIFY] | Probably not triggered by phone shortlisting [VERIFY] | Phase 2 |

### D. Work eligibility (federal: IRCC)

| # | Rule | Where it appears | What it means here | Phase |
|---|---|---|---|---|
| D1 | **Work permit validity and type.** The permit must be valid. An **employer-specific (closed)** permit does not allow working for an agency; open permits do [VERIFY] | Form: "Work Permit"; drafts: expiry tracking | Validation must record permit **type** and **expiry**. Flag expiring permits before shortlisting | Phase 1 |
| D2 | **Study permit off-campus cap:** 24 hours per week while classes are in session, unlimited during scheduled breaks | Form: "Student". Rohan Q16 confirmed tracking | Track each student's weekly hours **across all clients**. Shortlisting must warn before a placement would exceed 24 hours. Needs the student's academic break dates | Phase 1 |

### E. Workplace safety (WSIB, Ontario)

| # | Rule | Where it appears | What it means here | Phase |
|---|---|---|---|---|
| E1 | The temp agency, as employer, registers with WSIB and pays premiums on insurable earnings, by rate group | Mind map, drafts | Premiums come from payroll | Phase 2 |
| E2 | **Injury reporting:** the employer reports a lost-time injury within 3 days of learning of it | Mind map ("incident documentation") | Incident log per worker per client | [DECISION NEEDED] |
| E3 | Safety orientation and training records | Mind map | Matches Tejash's "standard instructions per client and position". A record that the worker received them is useful evidence | Phase 1 (instruction acknowledgement) |

**Note on the drafts:** they show a pre-shift "WSIB check" on the compliance dashboard. WSIB is the agency's own coverage, not a per-worker document, so a per-worker pre-shift check does not fit. Read it as site safety training instead.

### F. Privacy, messaging and human rights

| # | Rule | Where it appears | What it means here | Phase |
|---|---|---|---|---|
| F1 | **PIPEDA** (federal private-sector privacy law; Ontario has no provincial equivalent for this sector): consent, limited use, safeguards, access rights | Mind map ("privacy and security") | Explicit consent at registration. Consent to share profiles with clients (employer approval step, Rohan Q4). Role-based access. Encrypt SIN | Phase 1 |
| F2 | **CASL** (anti-spam): commercial electronic messages need consent, sender identification and an unsubscribe option | Not in inbox | Bulk SMS/email job offers likely fall under CASL. Consent tick box at registration, plus opt-out in every message [VERIFY: job offers to registered workers may count as an existing relationship] | Phase 1 |
| F3 | **Ontario Human Rights Code.** Employment decisions cannot be based on protected grounds, including: <br>• sex<br>• age<br>• disability<br>• place of origin<br>• record of offences (pardoned, or provincial)<br><br>Pre-offer questions about some of these are restricted | Form asks gender, date of birth, criminal record, medical limitations | **Shortlisting and AI ranking must not use gender, age or medical status.** The form may need rewording, e.g. "able to perform job requirements, with or without accommodation" instead of "medical limitations" [VERIFY] | Phase 1 (form and matching rules) |
| F4 | **AODA** accessibility: organisations with 50+ employees must meet WCAG 2.0 AA for public websites | Not in inbox | The employer portal and the website forms. Friendly Staffing likely exceeds 50 employees (about 115 workers on one client sheet) | Phase 1 (employer portal) |

## Recommendations

1. **Phase 1 must support these rules:**
   - OT split at 44 hours across all clients (B1)
   - minimum-wage check on pay rates (B2)
   - break and three-hour-rule handling in timesheets (B5, B6)
   - 3-year record retention (B8)
   - required assignment information in confirmations (B9)
   - first-day-at-client tracking for the conversion fee (B11)
   - permit type, expiry and study-permit hour caps (D1, D2)
   - consent and access controls (F1, F2)
   - no protected grounds in matching (F3)
   - accessible employer portal (F4)
2. **Decide the deductions question** before scoping: show deductions calculated by QuickBooks, or calculate them in Phase 1. This determines whether TD1/TD1ON, CPP/EI/tax tables and their yearly updates enter Phase 1.
3. **Leave statutory filing to Phase 2:** CRA remittances, T4, ROE, WSIB premiums, vacation and public holiday pay, pay stubs, HST invoicing.
4. **Book a specialist review** with an Ontario employment/payroll specialist. Cover every [VERIFY] item, especially C2 (AI disclosure), B11 (conversion fee), F3 (form questions) and D1 (permit types).
5. **Confirm the licence:** ask Tejash to confirm Friendly Staffing's temp help agency licence number.

## Open Questions

1. Does QuickBooks currently calculate CPP, EI and income tax for Friendly Staffing workers? Are TD1s collected today?
2. Does Friendly Staffing hold an Ontario temp help agency licence? What is the number?
3. How many employees does Friendly Staffing have, including assignment workers? This decides the 25+ job-posting rules and the 50+ AODA threshold.
4. When a client sends workers home early because production changed, are they paid the hours worked or a minimum?
5. Is lunch paid at any client? Tejash said "30 minutes lunch break is paid".
6. How are student workers' academic break dates known today?
7. Does Friendly Staffing keep an injury or incident log today?

## References

- Ontario.ca, *Your guide to the ESA: Temporary help agencies*: https://www.ontario.ca/document/your-guide-employment-standards-act-0/temporary-help-agencies
- Torkin Manes, *Ontario's new licensing requirements for temporary help agencies and recruiters*: https://www.torkin.com/insights/publication/ontario-s-new-licensing-requirements-for-temporary-help-agencies-and-recruiters
- DLA Piper, *New licensing regime in Ontario for recruiters and temporary help agencies*: https://dlapiper.com/en/insights/publications/2023/08/new-licensing-regime-in-ontario-for-recruiters-and-temporary-help-agencies
- NatLaw Review, *Licensing deadline for Ontario recruiters and temporary help agencies*: https://natlawreview.com/article/licensing-deadline-ontario-recruiters-and-temporary-help-agencies-draws-near-and
- Lawyers for Employers, *Increased protection for temporary workers*: https://lawyersforemployers.ca/employment-standards-update-increased-protection-temporary-workers/
- Fasken, *What Ontario employers need to know about job posting obligations for 2026*: https://www.fasken.com/en/knowledge/2025/12/what-ontario-employers-need-to-know-about-job-posting-obligations-for-2026
- HCAmag, *Ontario's new pay transparency and AI disclosure laws*: https://www.hcamag.com/ca/specialization/employment-law/ontarios-new-pay-transparency-and-ai-disclosure-laws-what-employers-need-to-know-now/535727
- Hicks Morley, *Ontario minimum wage to increase October 1, 2026*: https://hicksmorley.com/2026/04/01/ontario-minimum-wage-to-increase-october-1-2026/
- Rise People, *What is a Record of Employment (ROE)?*: https://support.risepeople.com/portal/en/kb/articles/what-is-a-record-of-employment-roe
- CIC News, *Off-campus work rules for international students: May 2026 update*: https://www.cicnews.com/2026/05/off-campus-work-rules-for-international-students-the-may-2026-update-0575792.html
