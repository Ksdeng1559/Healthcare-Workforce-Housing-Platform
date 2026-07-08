# Wiki Schema: Healthcare Workforce Housing Platform (Sapperton / New Westminster)
**Created**: 2026-07-07
**Last revised**: 2026-07-07
**Owner**: Dennis Eng

## Purpose
To build an accumulating knowledge base covering (1) development deal/site evaluation, (2) BC zoning, entitlement, and housing policy, and (3) the healthcare workforce housing platform strategy centered on Sapperton, New Westminster. Audience includes external stakeholders (investors, capital partners, landowners), so every claim must be sourced and confidence marked.

Core questions this wiki answers:
- Is a given site/deal viable? (zoning, yield, financials, timeline)
- What entitlement paths and policy levers exist in New Westminster / BC?
- How do sites and policies connect to the healthcare workforce housing thesis (hospital proximity, workforce affordability)?

---

## Entity types

| Type | Description | Examples |
|------|-------------|---------|
| Site | A specific property or land assembly under evaluation | Garrett Street assembly (417–434 Garrett St) |
| Project | A named development proposal or platform initiative | Garrett Street redevelopment, Sapperton Healthcare Housing District |
| Jurisdiction | City, region, or governing area | New Westminster, Metro Vancouver, BC |
| Policy | Zoning designation, law, program, or guideline | RD zoning, RM-3, TOD guidelines, density bonus |
| Organization | Developer, government body, hospital, investor, nonprofit | City of New Westminster, Royal Columbian Hospital, Fraser Health |
| Concept | Domain term with specific meaning | FAR, CAC, DCC, land assembly, workforce housing |
| Person | Named individual with a role in the domain | City planners, sponsors, landowners |
| Dataset | Named report, study, or data source | Investment memorandum, sentiment analysis, modular research brief |

---

## Relationship types

| Relationship | Direction | Meaning |
|-------------|-----------|---------|
| `located-in` | A → B | Site/project A sits in jurisdiction B |
| `zoned-as` | A → B | Site A currently carries zoning B |
| `proposed-rezoning-to` | A → B | Site A has a proposed/target zoning B |
| `governs` | A → B | A has regulatory authority over B |
| `part-of` | A → B | A is a component of B |
| `requires` | A → B | A cannot proceed without B (approval, permit, funding) |
| `serves` | A → B | Housing/project A serves anchor institution or population B |
| `funded-by` | A → B | A receives capital from B |
| `contributes-to` | A → B | A delivers public benefit / payment to B (CACs, DCCs) |
| `supersedes` | A → B | A replaces or updates B |
| `contradicts` | A ↔ B | A and B assert opposing claims |
| `produced` | A → B | Organization/person A produced dataset/report B |

---

## Ingestion rules

### What to always extract
- All financial figures: costs ($/sq ft), revenues, unit prices, FAR, unit counts — with the assumption basis and date
- All zoning designations with jurisdiction, permitted use, FAR, and height limits
- All named approval-process steps and timeline estimates
- All named sites with addresses and lot sizes
- Public-benefit mechanisms (CACs, DCCs, density bonus, affordable housing commitments)
- Healthcare/workforce anchors (hospitals, employers) and their connection to sites

### What to skip
- Marketing adjectives without factual content ("vibrant", "modern") unless describing a concrete commitment
- Boilerplate, legalese, copyright notices
- Unattributed anecdotes

### Claim extraction standards
- Statistics must include: metric, value, applicable year/date, source
- Zoning claims must include: designation code, jurisdiction, FAR, height, status (current / proposed)
- Financial estimates must be flagged as estimates with stated assumptions ("subject to market conditions" etc.)
- Quotes attributed to named person with role

---

## Quality standards

- [ ] Every factual claim has at least one source citation
- [ ] Every entity file has a "Last confirmed" date
- [ ] Estimates clearly distinguished from verified facts (external-stakeholder audience)
- [ ] Tensions documented, not hidden
- [ ] INDEX.md current
- [ ] `_log/ingest.md` entry for every ingested source

---

## Open questions (domain-level)

- What is the land assembly cost for the Garrett Street site? (Proposal leaves it TBD)
- What are New Westminster's current (2025–2026) TOD/transit-oriented area rules post-Bill 47, and do they supersede the proposal's RM-3/TOD assumptions?
- What efficiency ratio converts buildable floor area to sellable/net area for unit-count claims?
- How does the Garrett Street deal connect financially to the healthcare workforce housing thesis (rental vs strata, AMI targets)?
- Who are the confirmed capital partners / sponsors?

---

## Revision history

| Date | Change | Trigger |
|------|--------|---------|
| 2026-07-07 | Initial schema created | Bootstrap with Garrett Street proposal PDF |
