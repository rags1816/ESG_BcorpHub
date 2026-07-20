# ESG Hub — Methodology

## Origin

Developed by Vijay L Narasimhan / i-NoCarbon, 2025–26, to give client
businesses a single platform covering ESG maturity, carbon accounting, and
B Corp readiness — three assessments typically run separately — with a
multi-tenant structure so i-NoCarbon can deploy and white-label it for
multiple clients from one codebase.

## Problem this solves

Businesses assessing ESG maturity, measuring carbon footprint, and preparing
for B Corp certification typically use three disconnected tools, re-entering
similar company context each time and losing the ability to see how the
three assessments relate. ESG Hub runs all three from one intake, with
results feeding a single governance/report layer, and supports deploying
the same platform to multiple client businesses under their own branding.

## Built on / credited frameworks

- **B Corp Impact Assessment (BIA)** — the B Corp Readiness module's 28
  questions are drawn from and reference official B Lab codes; the tool
  covers 28 core BIA questions (max 186 pts) against the official BIA's
  200+ sector-dynamic questions. Positioned explicitly as pre-work: "Score
  85+ here before starting the official BIA."
- **GHG Protocol** — the Carbon Calculator's Scope 1/2/3 structure follows
  the GHG Protocol's standard categorisation, including all 15 Scope 3
  categories
- **DESNZ (2025) and DEFRA (2024)** — UK government emission factor sources,
  cited per-factor in the in-app Sources & Methodology panel
- **Maturity-model self-assessment approach** — the ESG Diagnostic's
  underlying scoring logic follows the same maturity-model pattern used by
  B Corp's BIA, the UN Global Compact self-assessment, and GRI Readiness
  tools (see the ESG Diagnostic Toolkit methodology for the detailed scoring
  mechanics shared with this module)
- **Reporting framework references:** CSRD (EU Directive 2022/2464), TCFD
  (FSB 2017/2021), GRI (2021 Universal Standards), SBTi (Corporate Net-Zero
  Standard v1.1), CDP (2023), SFDR (EU 2019/2088), BRSR (SEBI 2021), SECR
  (BEIS 2019) — used to drive the Framework Recommender and Report module

## Core framework (your original model)

**Unified intake → three assessments → single governance layer:** a single
Intake & Context step (sector, jurisdiction, size, reporting frameworks)
configures the ESG Diagnostic, Carbon Calculator, and B Corp Readiness
modules simultaneously, rather than requiring separate setup for each.

**Recommendation engine:** ESG Diagnostic recommendation cards are
sorted by gap size against sector average (not raw score), each showing
estimated cost to move up one maturity level and which B Corp BIA pillar it
affects — explicitly linking the diagnostic and B Corp modules rather than
treating them as separate outputs.

**Data-driven recommendation gating:** Carbon Calculator recommendations
only appear for categories where the user has entered data — a deliberate
design choice to avoid generating advice (e.g. an EV fleet recommendation)
for activities not applicable to the business.

**Multi-tenant governance model:** sysadmin (platform-wide), bizadmin
(own-business user management), editor, and viewer roles allow i-NoCarbon
to deploy the same underlying platform to multiple client businesses, each
with independently managed users and white-label branding, from a single
maintained codebase.

## Inputs → Process → Outputs

- **Inputs:** company profile (sector, size, jurisdiction), 21 ESG
  diagnostic answers, Scope 1/2/3 carbon data, 28 B Corp readiness answers
- **Process:** maturity scoring against sector benchmarks; GHG
  Protocol-based carbon calculation; BIA-referenced B Corp scoring; AI
  layer (optional) for action plans and disclosure drafting
- **Outputs:** ESG score + radar/pillar breakdown, carbon totals + scenario
  projections, B Corp readiness score against the 80-point threshold,
  exportable ESG disclosure report, CPO-facing governance rollup

## Why this approach (rationale)

Running ESG maturity, carbon accounting, and B Corp readiness from one
intake removes duplicated data entry and lets recommendations reference
across modules (e.g. a diagnostic gap explicitly tied to the BIA pillar it
affects) — something three separate point tools can't do. The multi-tenant
structure means the underlying assessment logic stays centrally maintained
(one place to update emission factors or B Corp question codes) while still
supporting white-labelled, independently-managed client deployments.

## Version history

- V4 [current]: unified Intake → Diagnostic → Carbon → B Corp → Report flow;
  multi-tenant sysadmin/bizadmin/editor/viewer roles; white-label branding;
  JSON export/import for diagnostic and BIA answers
