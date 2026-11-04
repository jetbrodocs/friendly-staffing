# Project Configuration

## Project Description

Friendly Staffing (1953039 Ontario Inc.) is a temp-to-perm staffing agency with two offices in Mississauga, Ontario. It places mostly newly arrived immigrant workers with clients such as food plants and warehouses. Today it runs on paper forms, per-office spreadsheets, WhatsApp and QuickBooks. This project documents current operations and scopes a Phlo-built system as Phase 1 plus a "Build later" list (renamed from Phase 2 on 2026-11-04). The end goal is a proposal to Friendly Staffing for an end-to-end staffing and recruitment platform covering scope, timeline and cost only; detailing within the scope comes later. Phase 1 (re-phased 2026-11-03, target go-live 20 January 2027 (moved from 15 January on 2026-11-04; confirmation asked by 7 November 2026, start 16 November)): worker onboarding, employer order intake, shortlisting, communication tracking (WhatsApp Business, email, SMS fallback), approvals and trials for the employers that need them, dispatch/replacements, Friendly Staffing's own timekeeping on phones (a separate module; how it is built, e.g. a mobile app, is an open Jetbro decision that drives the development cost), and payroll in Phlo: payment methods A and B, deductions, pay stubs, the bank upload file (bank and format to be confirmed) and everything else related to payroll: vacation pay accrual, CRA remittance figures, ROE.BLK files for ROE Web, T4 slips and the T4 electronic filing file, WSIB figures (payments to the government made outside Phlo), and client invoicing (bill rate = pay rate + margin, extra charges, conversion fees, HST; added 2026-11-04), with final amounts and invoices pushed to QuickBooks, which stays for bookkeeping. Build later: receivables, the worker self-serve job portal and loaded-margin reporting. Commercial model: one-time development and implementation cost over about 2 months, then an AMC, hosting separate, plus an estimated monthly running cost; no Phlo licence. Amounts are kept outside git.

## Domain Glossary

| Term | Definition |
|---|---|
| Pay rate | Hourly rate Friendly Staffing pays the worker, before deductions. Rate A is set per worker; in the payroll Excel rate B = rate A × 0.9 and rate C = rate A × 0.85. Overtime pay = 1.5 × rate |
| Bill rate | Hourly rate the client pays Friendly Staffing for a position. Derived from the pay rate plus a margin that staff add by hand when invoicing. Overtime bill rate is about 1.5 times the regular bill rate |
| Employee code | 6-digit worker ID, written "Y MM NNN" (year digit, month, then staff and serial). Generated when the worker is assigned their first job |
| Temporary code | Identifier for a validated worker before the first job. Looks different from the employee code |
| Worker status | Registered → Validated (Inactive) → Active. Active from the first job assignment |
| Payment method | A = direct deduction (treated as an employee; government deductions apply). B = subcontractor (no deductions). The worker chooses A, B or both |
| Payroll Excel | Friendly Staffing's weekly sheet of workers by employer, with rates and payment method; produces gross pay only (QuickBooks calculates method A deductions) and is the basis for invoices |
| Payment mode codes | Values in the payroll Excel beyond A and B: A20, A24, A40, "A20 Only", 2D. Meaning to be confirmed with Tejash |
| Vacation pay | 4%, accrued over an October to September year and paid once a year as a lump sum |
| ROE.BLK | ROE Web bulk upload file for Records of Employment |
| Order | A client's request for workers (count, position, shift time, date) |
| Temp-to-perm / conversion | Client hires a placed worker onto its own payroll. A fee applies if this happens before the contract period ends |
| Survival job | Interim work new immigrants take before finding work in their field |
| GMP | Good Manufacturing Practice: site rules at food clients (hairnet, apron, no eating on the floor) |
| Timekeeper | Person at the client site recording worker in/out times |

## Skills

This project includes skills installed in `.claude/skills/`. Claude Code auto-discovers these from their descriptions. You can also invoke them manually. Each skill that owns a folder names that folder explicitly — so output never has to be guessed.

| Skill | Owns folder | Trigger |
|---|---|---|
| `/documentation-writer` | — (all output) | Always apply as baseline for all documentation output |
| `/observation-capture` | `10-observations/` | Capturing observed reality or Q&A exchanges |
| `/process-mapping` | `20-process-maps/` | Building sequential flows from observations |
| `/analysis` | `30-analysis/` | Deep-dives, comparisons, or tech-stack/implementation decisions |
| `/solution-design` | `40-solution-design/` | Writing PRDs / requirements (after tech stack is decided) |
| `/screen-specs` | `40-solution-design/<prd>/screen-specs/` | Per-screen UX detail derived from a PRD |
| `/scope` | `scope/` | Writing the independent stakeholder sign-off document |
| `/documentation-reviewer` | — (method) | Reviewing/auditing docs; findings fold back into source docs |
| `jetbro-brand` | — (all styled output) | Always active — applies to all styled/visual output (HTML, PDF, slides, reports) |

**Layering:** `documentation-writer` is the foundation — it loads automatically for any writing task. `jetbro-brand` is always active for any styled or visual output. Specialized skills layer on top based on context.

**Skill priority:** This is a documentation project, not a code project. Always prefer this project's documentation skills over general-purpose coding skills (e.g., superpowers, test-driven-development, frontend-design). Do not invoke coding-oriented skills unless the user explicitly asks for code.

## Folder Structure

**Strict purpose, flexible order.** Each folder's *purpose* is enforced — put a document only in the folder whose purpose it matches. The *order* between folders is flexible: you can write scope after process maps, or after analysis, or jump back to observations any time. The numbered prefixes are for grouping and sorting, not a mandatory sequence. **Each folder has an entry rule — check it before writing there.**

| Folder | Purpose | Entry rule (what belongs / does NOT) |
|---|---|---|
| `00-inbox/` | Raw notes, uploads, unprocessed material | Anything raw. No rule. |
| `10-observations/` | Observed reality + Q&A exchanges | Belongs: what was observed or what people told you. NOT: analysis, conclusions, flows. |
| `20-process-maps/` | Sequential process flows, user journeys, data flow | Belongs: a sequence/flow built from observations. NOT: raw captures, design, analysis. |
| `30-analysis/` | Deep-dives only — research, comparisons, **tech-stack/implementation decisions** (optional) | Belongs: a genuine deep-dive or a tech decision. NOT: routine notes, observations, process steps. |
| `40-solution-design/` | PRDs, requirements, data model, architecture. One folder per PRD: `prd-NN-<name>/` with `prd.md` + `screen-specs/` | 🔒 **Guard: do NOT start until the tech stack/implementation approach is decided (in `30-analysis/`).** |
| `60-change-logs/` | Records of changes made to the system over time | Belongs: a record of a change to the system. NOT: review/gap-analysis findings (those fold into source docs). |
| `scope/` | Independent stakeholder sign-off doc(s) — exports to branded PDF | 🔒 **Must be self-contained — references nothing else in the project.** |

## Team

| Name | Role | Notes |
|---|---|---|
| Tejash Jain | Promoter, Friendly Staffing (client) | Appears as "Priya Jain" in the 2026-10-21 Fathom transcript |
| Rohan Patel | Jetbro, engagement lead | |
| Honey Darji | Jetbro | Attended the 2026-10-21 workshop |

## Branding

All styled or visual output (HTML pages, PDF documents, slides, reports, dashboards) must use JetBro brand guidelines from `.claude/skills/jetbro-brand/`. This includes:

- **Colors:** Use the JetBro palette (accent `#c45a32`, text `#1a1a1a`, etc.)
- **Typography:** Bricolage Grotesque for headings, Outfit for body text, Space Mono for code/data
- **Logo:** Include from `jetbro-brand/logo.svg` where appropriate
- **Accent line:** Use the signature gradient separator between sections
- **CSS tokens:** Import from `jetbro-brand/tokens.css` for web output

Plain markdown files (observations, process maps, analysis, screen specs) do not need visual branding — the brand applies when producing formatted deliverables (scope PDFs, reports, slides).

## Date Awareness (read this on every session)

Documents carry `created:` and `updated:` dates in their frontmatter. These matter — not everyone checks git history.

- **When writing/editing any doc:** always set `updated:` to today's date. A stale date is worse than none.
- **When reading any doc:** note its `updated:` date relative to today. If it is old, treat the content as **possibly outdated** — verify before relying on it, especially for decisions, tech choices, and scope. Do not assume an old document reflects the current state.
- **Git is the source of truth** for when a file actually changed: `git log -1 --format=%cs <file>`. If it disagrees with the frontmatter, trust git.

## Client Deliverables

| Deliverable | Where | Notes |
|---|---|---|
| Proposal: scope, architecture, timeline and commercials (Phlo-branded, A4, 17 pages) | HTML source: `scope/phlo-friendly-staffing-architecture.html`. Review copy: https://claude.ai/artifact/TbPdDSSTccQMVzM1Qg65Xi | Regenerate the PDF from the HTML with headless Chrome. The repo copy replaces the commercials page with "shared separately" (the repo is public); the review copy and the PDF carry the amounts. The PDF is kept outside the repo at `~/Desktop/Jetbro/Phlo for Friendly Staffing - Proposal.pdf` |

## Project-Specific Rules

- Every requirement is tagged Phase 1, Build later or out of scope. Do not call the later work "Phase 2" in new documents.
- Spell the platform "Phlo" (transcripts render it as "Flow").
- Jetbro's pre-workshop draft documents are unreliable drafts; the 2026-10-21 workshop and Rohan's 2026-10-26 answers take precedence.
