---
title: "Q&A — Rohan's Scope Clarifications (2026-10-26)"
status: in-review
created: 2026-10-26
updated: 2026-10-27
tags: [observation, qa, scope, phasing]
---

# Q&A — Rohan's Scope Clarifications (2026-10-26)

## Source

Rohan Patel (Jetbro) answered 24 follow-up questions on 2026-10-26. The questions came from a review of the 2026-10-21 workshop call with Tejash Jain ([obs-workshop-call-2026-10-21](obs-workshop-call-2026-10-21.md)), his mind map ([obs-client-mind-map](obs-client-mind-map.md)), the registration form and the Molinaro's timesheet. The answers below are Rohan's own words, lightly condensed.

**Ground rule from Rohan:** the project has exactly two phases. The exercise must end with a clear split of what Phase 1 delivers and what Phase 2 delivers.

## Scope and Phasing

**Q1. The mind map (invoicing, full payroll, compliance) is broader than the call. Which defines scope?**

Tejash wants everything in the mind map eventually. Phase 1 covers:

1. **Worker onboarding.** Forms, validations, then entry into the database.
2. **Employer request intake.** Employers submit requests online, through a URL.
3. **Shortlisting.** Tech or AI helps the Friendly Staffing team shortlist and prioritise candidates. The priority factors are not yet decided.
4. **Data migration.** Move existing manual records into the new system at go-live.
5. **Communication tracking.**
   - Track and manage messages between the Friendly Staffing team and workers.
   - Do the same for messages between the team and employers (email, call or WhatsApp).
   - The channel is not yet decided.
6. **Employer approval.** The employer approves candidates, and approved candidates go to the site.
7. **Replacements and no-shows.** If a worker can't go, the team manages a replacement. Communication about a no-show is also managed.
8. **Timekeeping and rates.** Check-in and check-out times are recorded in the system. Pay rate and bill rate are applied to the hours.
9. **Employee portal.** Rohan described one "where they can manage all of this". See the contradiction flagged under Q18.

**Phase 1 output:** accurate timesheets, cross-verified against the employer's timesheets. Pay rate and bill rate are applied to them and communicated to the employer and the employees.

**Out of Phase 1:** the team cross-verifying and making payments, creating invoices, and the QuickBooks replacement. These are Phase 2.

**Q2. Are pay rate and bill rate "after deductions"?**

No. The calculation runs step by step:
1. Hourly rate.
2. Hourly rate × hours worked.
3. Deductions are then shown and managed.

**Q3. Who keeps time?**

Today the employer's timekeeping is used. In Phase 1, Friendly Staffing takes the employer's time as correct and applies pay rate and bill rate to it. Friendly Staffing running its own timekeeping moves to Phase 2.

**Q4. Do employers approve workers?**

Yes. Friendly Staffing shares a shortlist. The employer approves the workers it prefers for the role.

**Q5. When is the employee code assigned?**

When onboarding validation is complete and the worker is marked **ready to work**.

**Q6. Do we keep the existing code scheme?**

Yes. Use Friendly Staffing's existing code structure and build rules as they are.

**Q7–Q8. Referral share and database size.**

Not relevant right now.

**Q9. Matching priority.**

Friendly Staffing will provide the priority rules when development begins.

**Q10. QuickBooks replacement.**

Phase 2.

## Operations

**Q11. Is Molinaro's the 90% client?**

Unknown.

**Q12. Staff count, office split, permissions.**

Rohan's view: these should not matter to the system.

**Q13. Invoicing.**

Phase 2, together with Friendly Staffing's own timekeeping.

**Q14. Break rules and paid time.**

These are client-specific. The client provides them. The team discusses them with the worker when the worker applies for a role or is recommended for one.

**Q15. Worker pay frequency, vacation pay, public holiday pay.**

Unknown. Ask Friendly Staffing.

**Q16. Work-permit expiry and study-permit hour caps.**

Yes, these need tracking.

**Q17. Channel preference and messaging budget.**

Unknown. Ask Friendly Staffing.

**Q18. Worker portal: browse and apply?**

Today, employers and employees create profiles, and the Friendly Staffing team validates them. When a role comes up, the team contacts the worker. A portal where workers log in, see open roles and apply is **Phase 2**.

**Q19. No-show and walk-off tracking with a replacement workflow.**

Yes.

**Q20. Temp-to-perm conversion fee.**

The system should track it. The rules are not defined yet. Ask Friendly Staffing.

**Q21. Same-day order changes.**

The Friendly Staffing team is responsible for updating confirmed workers. The exact process is still open.

**Q22. Payroll Excel sample.**

Not received yet. Ask Friendly Staffing.

**Q23. Jetbro's earlier draft documents.**

Rohan's team wrote them after the introductory call, before the 2026-10-21 workshop. Treat them as drafts that may contain errors. Copied to `00-inbox/jetbro-draft-journey-flow-2026-10.pdf` and `00-inbox/jetbro-draft-platform-journey-2026-10.pdf`. Both date from 2026-10-21 and show one unphased platform.

**Q24. Review call timing.**

Rohan will message Tejash.

## Contradictions Within These Answers

1. **Check-in/check-out in Phase 1.**
   - Q1 puts check-in/check-out recording and our own timekeeping (to cross-verify against the employer's) in Phase 1.
   - Q3 says Phase 1 accepts the employer's time as correct, and Friendly Staffing's own timekeeping is Phase 2.
2. **Employee portal in Phase 1.**
   - Q1 mentions a portal where employees "manage all of this".
   - Q18 moves the browse-and-apply portal to Phase 2.

   What does the employee do in the portal in Phase 1?
3. **Deductions.**
   - Q2 says deductions are shown and managed.
   - Q1 puts payments and payroll in Phase 2.

   Are deductions calculated in Phase 1, or only shown as a placeholder?
4. **Mind map items with no phase.** Some mind map items have no phase assigned: CRA remittances, T4s and ROEs, WSIB records, dashboards, AR collections. With only two phases, each must land in Phase 1, Phase 2 or out of scope.

## Follow-up Answers (2026-10-27)

**F1. Check-in/check-out in Phase 1.** The employer's timekeeping records check-in and check-out in Phase 1. Friendly Staffing does not run its own time capture until Phase 2. *(Resolves contradiction 1.)*

**F2. Employee portal in Phase 1.** None. Workers do not log in or use any portal in Phase 1. The Friendly Staffing team shortlists, prioritises and contacts workers directly as jobs open up. *(Resolves contradiction 2.)* Phase 1 portals are therefore the employer portal (order intake) and the internal staff system.

**F3. Deductions.** Decided 2026-10-27. Phase 1 **shows** deductions. Phase 2 **calculates** them, together with payroll. TD1/TD1ON collection therefore moves to Phase 2. Background: [analysis-canada-ontario-regulatory-review](../30-analysis/analysis-canada-ontario-regulatory-review.md). *(Contradiction 3 resolved. Open: where the Phase 1 figures come from; see Open Questions.)*

**F4. Unphased mind map items.** Rohan wants margin and profitability dashboards in Phase 1 if they are possible without payroll.
- **Phase 1:** hours-based gross spread, (bill rate − pay rate) × approved hours, per worker, order, client and week. This needs no payroll data.
- **Phase 2:** loaded margin. This subtracts employer costs that only payroll produces:
  - the employer's share of CPP and EI
  - WSIB premiums
  - 4% vacation pay
  - public holiday pay
- **Phase 2:** cash profitability (invoiced and collected).

Proposal for the remaining items, pending Rohan's confirmation:
- **Phase 2:** CRA remittances, T4, ROE, WSIB premiums, AR follow-up.
- **Phase 1:** operational counts.
- **Phase 2 or out of scope:** incident log.

## Open Questions for Friendly Staffing

1. Worker pay frequency. Is vacation pay or public holiday pay calculated today?
2. Preferred outreach channel (SMS, WhatsApp, email). Acceptable per-message cost.
3. Temp-to-perm conversion fee: period, amount, conditions.
4. Payroll Excel sample (promised on the 2026-10-21 call).
5. Matching priority factors and their order.
6. Where do the deduction figures shown in Phase 1 come from? Options: imported back from QuickBooks payroll output, or an estimate.
