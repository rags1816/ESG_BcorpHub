# ESG Hub

A multi-tenant ESG assessment platform combining an ESG maturity diagnostic,
a carbon calculator, and a B Corp readiness assessment into a single
CPO/founder-facing tool, with white-label deployment for client businesses.

## What it does

- **Intake & Context:** company profile, sector, jurisdictions, target
  reporting frameworks — configures all downstream modules
- **ESG Diagnostic:** 21 questions across 6 dimensions, producing an overall
  ESG score, radar chart, and E/S/G pillar breakdown, with AI-generated
  action plans on lowest-scoring areas
- **Carbon Calculator:** full Scope 1/2/3 GHG Protocol calculator
  (all 15 Scope 3 categories), with region-specific emission factors
  (DESNZ 2025, DEFRA 2024) and three forward-looking scenarios (Business as
  Usual, Moderate Action, Ambitious Transition)
- **B Corp Readiness:** 28 questions across 5 pillars (Governance, Workers,
  Community, Environment, Customers), each mapped to a B Lab reference code,
  scored against the 80-point certification threshold
- **ESG Report:** AI-drafted disclosure reports mapped to selected reporting
  frameworks (GRI, CSRD, TCFD, etc.), exportable as PDF
- **Multi-tenant admin:** sysadmin/bizadmin/editor/viewer roles, white-label
  branding per client business, per-user AI key entry, emission factor and
  benchmark maintenance

## Status

V4. Deployed for client businesses via a frozen build
(`ESG_Hub_V4_FROZEN.html`); actively maintained by Vijay as System Admin for
i-NoCarbon and partners.

## Tech stack

Single-file application (client-facing) with a role-based multi-tenant admin
layer; data stored in browser `localStorage` per business tenant. AI via
Anthropic or Gemini, admin-provisioned or per-user key entry. Emission
factors and benchmarks maintained via the admin Maintenance tab.

## How to run

Deployed to Krystal `public_html` per client, branded via the Admin Panel.
See `ESG_Hub_V4_Admin_Guide.docx` for deployment steps and
`ESG_Hub_V4_User_Guide.docx` for the assessment walkthrough.

## Development note

Development assisted by Claude Code (Anthropic) under my direction. The
methodology, product design, and domain expertise reflected in this tool
are my own — see `METHODOLOGY.md` for the original framework.

## Related

See [`METHODOLOGY.md`](./METHODOLOGY.md) for the diagnostic scoring model,
carbon methodology, and B Corp readiness framework this tool applies.
