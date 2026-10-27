# Project Configuration

## Project Description

Friendly Staffing (1953039 Ontario Inc.) is a temp-to-perm staffing agency with two offices in Mississauga, Ontario. It places mostly newly arrived immigrant workers with clients such as food plants and warehouses. Today it runs on paper forms, per-office spreadsheets, WhatsApp and QuickBooks. This project documents current operations and scopes a Phlo-built system in exactly two phases. Phase 1: worker onboarding, employer order intake, shortlisting, communication tracking, dispatch/replacements, and cross-verified timesheets with pay/bill rates. Phase 2: Friendly Staffing's own timekeeping, invoicing, payroll/payments (QuickBooks replacement) and the worker self-serve job portal.

## Domain Glossary

| Term | Definition |
|---|---|
| Pay rate | Hourly rate Friendly Staffing pays the worker, before deductions |
| Bill rate | Hourly rate the client pays Friendly Staffing for a position; fixed per client and position |
| Employee code | 6-digit worker ID, written "Y MM NNN" (year digit, month, then staff and serial). Assigned when the worker is validated and marked ready to work |
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
| Platform architecture (Phlo-branded, A4, 15 pages) | HTML source: `scope/phlo-friendly-staffing-architecture.html`. Review copy: https://claude.ai/artifact/TbPdDSSTccQMVzM1Qg65Xi | Regenerate the PDF from the HTML with headless Chrome. The PDF is kept outside the repo at `~/Desktop/Jetbro/Phlo for Friendly Staffing - Platform Architecture.pdf` |

## Project-Specific Rules

- Exactly two phases. Every requirement must be tagged Phase 1, Phase 2 or out of scope.
- Spell the platform "Phlo" (transcripts render it as "Flow").
- Jetbro's pre-workshop draft documents are unreliable drafts; the 2026-10-21 workshop and Rohan's 2026-10-26 answers take precedence.
