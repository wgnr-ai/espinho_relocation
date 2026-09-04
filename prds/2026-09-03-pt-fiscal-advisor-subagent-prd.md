---
title: PRD — Espinho Relocation Sub-Agent Set (PT Fiscal Advisor + Specialty Sub-Agents)
status: open
project: espinho-relocation
assignees:
  - SysOp (wgnr_ai_sysop)
priority: high
created: 2026-09-03
due: 2026-12-31
related: docs/plans/non-crisis-move-plan.md
tags:
  - sub-agent
  - prd
  - relocation
  - espinho
  - sysop-build
---

# PRD — Espinho Relocation Sub-Agent Set

**Origin:** Wagner dos Santos, 2026-09-03, during espinho-relocation planning session.
**Routing:** Filed with SysOp (wgnr_ai_sysop) for build. Active project espinho-relocation will consume the output.
**Status:** DRAFT, awaiting SysOp prioritization and build.

## Problem

The espinho-relocation project (Orlando FL → Espinho, Portugal; target move Apr–Jun 2027) requires a level of jurisdiction-specific, frequently-changing expertise that the existing espinho-captain (orchestrator) and espinho-researcher (generalist researcher) profiles cannot sustain. Today's Wave-1 / Wave-2 research exposed three gaps where Generalist + Generalist-Researcher must defer to a human-paid professional:

1. **PT fiscal / tax advisory** (IFICI eligibility screening, entity restructure design, IRS posture, Modelo 3 / Modelo 22 filings, NIF/NISS planning, US-PT treaty tie-breaker work)
2. **PT healthcare for a 91-year-old returning senior with active cancer history** (SNS enrollment pathway, IPO Porto / oncology referral coordination, Natera Signatera continuity, prescription transfer)
3. **International pet logistics** (USDA APHIS 7001 endorsement, EU 2026/131 Animal Health Certificate, mandatory liability insurance for Pit Bull type, pet transport coordination)

Each of these would otherwise require the Principal to engage a paid professional. The Principal has requested a sub-agent set so the agents can do first-pass screening, paperwork prep, and ongoing compliance monitoring at near-zero marginal cost, escalating to a human professional only on the actual decision points.

## Goal

Build, configure, and validate a set of specialty sub-agents under the espinho-* profile family. The set covers the three gaps above plus the additional specialties surfaced by the Wave-1 and Wave-2 work. Each sub-agent must:
- Verify all facts against current 2026 Portuguese/US/IRS sources (never pattern-match from training data)
- Distinguish [OFFICIAL] / [PRACTICAL] / [UNVERIFIED] sources per the espinho-researcher standard
- Defer to a human-paid professional at any decision point that requires a binding ruling, a signed filing, or a clinical judgment
- Persist all findings to `research/YYYY-MM-DD-<topic>.md` with source tags and dates

## Scope (in scope)

Build the following five sub-agent profiles under the espinho-* family. Each profile is a specialization of espinho-researcher with its own prompt, tool surface, and verification rules.

### Sub-agent 1 — espinho-fiscal-advisor (PRIMARY ASK)

**Purpose:** First-pass PT/US fiscal advisory for relocation, entity design, ongoing compliance. The Principal has explicitly requested this profile.

**Sources of authority (use these, not training data):**
- AT (Autoridade Tributária e Aduaneira) — `at.gov.pt` / `portaldasfinancas.gov.pt`
- IRS Portugal — `irs.pt` (separate from AT for personal income tax)
- PGDL (Procuradoria-Geral Distrital de Lisboa) — published circulares, opinion letters
- OECD Model Tax Convention and PT-specific commentary
- US-PT Tax Treaty (1994) and US-PT Totalization Agreement (1989, TIAS 12121)
- IRS US — Pub 54, Pub 514, Form 5472 instructions, Form 8858 instructions
- IRC §911 (FEIE), §7701 (US person), §957/958 (CFC), §1291 (PFIC), §1297 (CFC tests)
- CIRC (Código do Imposto sobre o Rendimento das Pessoas Coletivas) art. 2 (effective management PE test)
- IFICI (NHR 2.0) — Lei 21/2024 de 5 de agosto and AT Circular 4/2025
- Decreto-Lei 7/2024 (IFICI regime) and any 2025–2026 AT rulings

**Required capabilities:**
- Entity-design screening: sole trader (trabalhador independente) vs PT Lda + US branch vs continued US LLC + PT trade-name path
- IFICI eligibility screening for the Principal's specific activity mix (creative IP generation + AI services to SMBs + third-party manufacturing)
- PE / effective-management test application
- US 1040 / 5472 / 8858 / 1116 / 2555 posture recommendations
- Pre-move IRS enrollment sequence (NIF, NISS, IRS Modelo 3)
- Annual compliance check (deadline calendar: IRS Modelo 3 by Jun 30, FBAR by Apr 15 with auto-extension, Form 8938 with 1040)
- FBAR / CRS coordination, US tax compliance for PT-resident US citizens

**Boundary conditions (when to escalate to a human PT fiscal advisor):**
- Binding ruling application to AT
- Any IRS correspondence response
- Form 5472 election, US-PT treaty position statement
- Anything that requires a CRC number (CCRC certification) — the agent does not impersonate a certified advisor
- Any tax year where the Principal's income exceeds €150,000/yr (out of scope for first-pass)

### Sub-agent 2 — espinho-healthcare-senior-care

**Purpose:** Healthcare pathway research and ongoing care navigation for a returning senior with active cancer history.

**Sources of authority:**
- SNS (Serviço Nacional de Saúde) — `sns.gov.pt`
- DGS (Direção-Geral da Saúde) — clinical guidelines, oncology screening
- IPO Porto / IPO Lisboa — Portuguese Oncology Institutes
- Centro Hospitalar do Baixo Vouga (Aveiro) — nearest general tertiary to Espinho
- UCSP Espinho — primary care unit
- Hospital de Espinho (which is in Feira, owned by ULS EDV) — confirm 2026 entity status
- ARS Norte — regional health administration
- Hospital da Luz / CUF for private care pathway
- US Medicare for transition coordination (CMS, Social Security, Lisbon Federal Benefits Unit)
- Natera Inc. for ctDNA monitoring logistics

**Required capabilities:**
- SNS enrollment sequencing for a returning senior
- Tertiary-care referral pathway (UCSP → hospital → IPO)
- US medical record transfer protocol (HIPAA-compliant release, PT LGPD-compliant receipt)
- Natera Signatera continuity (US phlebotomy + FedEx to Natera US lab) OR EU-based equivalent identification
- Private insurance premium screening for age 90+ (most PT carriers decline at 65+; flag the gap and recommend direct specialist-pay or SNS-only)
- Medicare Part B suspension via Form CMS-1763 once PT residency is established
- Prescription translation framework (CUF International Patient, Hospital da Luz translator services)

**Boundary conditions (when to escalate):**
- Any clinical judgment (treatment, drug choice, screening interval)
- Binding medical-records release forms
- Any medication substitution involving narrow therapeutic index drugs

### Sub-agent 3 — espinho-pet-logistics

**Purpose:** International pet relocation and PT pet-life compliance for a dog classified as potentially dangerous under Decreto-Lei 315/2009.

**Sources of authority:**
- USDA APHIS — `aphis.usda.gov/aphis/pet-travel`
- EU Regulation 2026/131 (non-commercial pet movement) and EU 2026/848 (commercial) — in force 2026-04-22
- Direção-Geral de Alimentação e Veterinária (DGAV) — Portuguese veterinary authority
- SIAC (Sistema de Identificação e Registo Animal) — mandatory dog registration in PT
- Decreto-Lei 315/2009 — potentially dangerous dogs list and requirements
- Câmara Municipal de Espinho — municipal pet ordinance

**Required capabilities:**
- USDA APHIS 7001 endorsement process and timing (vet visit within 10 days of EU entry, microchip before rabies vaccine)
- EU 2026/131 Animal Health Certificate vs. older EU pet passport (in force 2026-04-22; old passport invalid for non-EU residents)
- Airline cargo booking (TAP Cargo, Delta Cargo, AA Cargo; United closed to civilian pet cargo in 2026)
- Snub-nosed breed verification (the Principal's Leo has a solid black nose, NOT brachycephalic — relevant for airline acceptance)
- Decreto-Lei 315/2009 compliance: mandatory third-party liability insurance, muzzle/short-leash public rules, câmara municipal registration, possibly municipal additional requirements
- PT pet insurance (Fidelidade, Médis Pet, Tranquilidade, PetPlan PT) for medium-large dog
- Espinho beach ordinance for dogs (seasonal access rules)

**Boundary conditions (when to escalate):**
- Booking a specific cargo flight (requires confirmed carrier policy and a vet contact)
- Câmara municipal additional requirements (requires direct contact)
- Any breed classification dispute (requires a canine genetic test or municipal sign-off)

### Sub-agent 4 — espinho-real-estate (proposed)

**Purpose:** Espinho-area rental and purchase research, with currency / mortgage / IMT (property transfer tax) modeling.

**Sources of authority:**
- Idealista, Imovirtual, Casa.pt — listings (live scraping allowed, with rate-limit and attribution per the platform terms)
- Banco de Portugal — Euribor rates, mortgage LTV guidance
- Autoridade Tributária — IMT brackets, imposto de selo rates
- Conservatória do Registo Predial — title search, encumbrance status
- Decreto-Lei 81/2020 (NRAU) and Lei 9-A/2026 (Mais Habitação amendments) — rental law
- DECO — tenant rights

**Required capabilities:**
- Listings monitoring (Idealista API or scrape, with alert thresholds)
- IMT / imposto de selo / notary / registry cost calculation for any specific listing
- Mortgage pre-screening for non-resident US citizen (Novo Banco, CGD, BCP, BPI non-resident channels)
- NRAU deposit and lease term rules
- Espinho + Santa Maria da Feira + Ovar + Esmoriz comparison for rental and purchase
- Currency sensitivity (USD/EUR) on monthly housing cost

**Boundary conditions:**
- Never executes a viewing booking (requires Principal consent)
- Never executes an offer (requires Principal consent)
- Formal mortgage simulation (requires bank application by Principal)

### Sub-agent 5 — espinho-ip-contracts (proposed)

**Purpose:** Contract drafting, MSA review, and IP classification for the WGNR business operating in PT while contracting as WGNR, LLC in the US.

**Sources of authority:**
- US-PT treaty (Art. 6 / 12 / 13 — IP income, royalties, alienation)
- INPI Portugal (Instituto Nacional da Propriedade Industrial) — IP registration
- US Copyright Office / USPTO
- WIPO Madrid System for international IP
- CIRC art. 4, 14, 17 (PT corporate tax treatment of IP income)
- IFICI and Patent Box regimes (PT has a Patent Box for IP income)

**Required capabilities:**
- Contract review: which clauses in the WGNR MSAs are problematic for PT-side operation (governing law, venue, IP assignment, indemnity, limitation of liability)
- PT IP registration pathway for the WGNR / wgnr.ai / WGNR Sounds / kelle.ai trademarks
- US-PT royalty-withholding tax modeling for any IP-licensing structure
- Patent Box eligibility screening (if WGNR develops any patentable IP — AI models, software, design systems)
- DBA-equivalent (estabelecimento) trade-name registration sequence at Conservatória

**Boundary conditions:**
- Never signs a contract on the Principal's behalf
- Never registers IP without explicit Principal authorization
- Formal US-PT treaty position requires a CCRC-registered fiscal advisor

## Out of scope

- Anything that requires a binding AT ruling or signed IRS correspondence (human fiscal advisor only)
- Clinical judgments (human clinician only)
- US state-specific filings outside Florida (the Principal's domicile)
- US expat CPA work (this is a separate, US-side human-CPA task; the sub-agents prepare inputs only)
- Direct interaction with the IRN / AT / IRS portals that require a CRC or PTIN number
- Anything that requires the Principal to be physically present in a specific country (vet visit, bank KYC, etc.)

## Success criteria

The sub-agent set is considered successful when:

1. **Wave-1 time-to-compressed-by-2x**: a research request that currently takes 8–12 minutes for the espinho-researcher should complete in 3–6 minutes for the specialty sub-agents (smaller prompt, focused tool surface, no need to load full relocation context each time).
2. **Source-tag discipline**: every fact in every sub-agent output is tagged [OFFICIAL/PRACTICAL/UNVERIFIED] with a URL and a date verified.
3. **Boundary discipline**: zero sub-agent attempts to impersonate a certified advisor or sign anything on the Principal's behalf; every escalation is explicit and the human professional's contact is identified.
4. **Cost reduction**: the Principal's paid-professional spend drops by 50–80% on the categories covered by the sub-agents, with the remaining spend concentrated on the actual decision points.
5. **Compliance continuity**: FBAR, IRS, AT, SNS, DGAV, and USDA APHIS obligations are tracked across calendar year 2026 → 2028 with deadline reminders dispatched via the existing scheduler infrastructure.

## Architecture and dependencies

- Each sub-agent is a profile entry in the active wgnr_ai_sysop project, distributed via the existing prompt profile mechanism.
- Each sub-agent loads the espinho-researcher base instructions as a foundation, then layers on its specialty tool surface and source whitelist.
- The Principal's active project espinho-relocation consumes the sub-agents via `call_subordinate(profile="espinho-<specialty>")`.
- A consolidated sub-agent registry is maintained in the active wgnr_ai_sysop project under `agents/espinho-<specialty>/AGENTS.md` (DOX convention).

## Acceptance criteria

- [ ] All five sub-agent profiles registered in wgnr_ai_sysop/agents/
- [ ] Each sub-agent prompt includes: (a) the verification discipline spec, (b) the source whitelist for its domain, (c) the boundary conditions, (d) the escalation path to a human professional
- [ ] Each sub-agent's tool surface is explicitly enumerated (per wOS Directive D4 — scheduled dispatch scopes its agents; this same discipline applies to all dispatches)
- [ ] Test scenarios (10 per sub-agent, per wOS Directive D1 enforcement standard) documented in `agents/espinho-<specialty>/tests/`
- [ ] Sub-agents are documented in the active wgnr_ai_sysop Child DOX Index
- [ ] Build is reversible: the sub-agents can be uninstalled via the standard plugin-removal mechanism

## Open questions for SysOp

- Model routing: per wOS Directive D2, the most expensive model makes decisions; the cheapest model that can follow specs does the work. Espinho-fiscal-advisor and espinho-healthcare-senior-care probably want the expensive model. Espinho-pet-logistics, espinho-real-estate, espinho-ip-contracts can run on the cheaper model.
- Tool surface: which tools do these profiles need beyond the default? Should they have direct read access to the espinho-relocation `research/` folder?
- Memory scoping: do these sub-agents share memory with espinho-researcher (sibling agents) or get isolated memory (federated)?
- Update cadence: PT regulations change frequently. What's the auto-update mechanism for the source whitelists?

## Time and effort estimate

- Sub-agent 1 (fiscal-advisor): 2 days build + 1 day test (highest priority)
- Sub-agent 2 (healthcare-senior-care): 1.5 days build + 1 day test (second priority — father's move is on the critical path)
- Sub-agent 3 (pet-logistics): 1 day build + 0.5 day test (third priority)
- Sub-agent 4 (real-estate): 1 day build + 0.5 day test
- Sub-agent 5 (ip-contracts): 1 day build + 0.5 day test

Total: 6.5 days build + 3.5 days test = 10 days effort, parallelizable to ~3 weeks elapsed with one developer.

## Author and sign-off

- **Author:** Espinho Captain (orchestrator), 2026-09-03
- **Principal approval:** Wagner dos Santos, 2026-09-03 (verbal during session; will confirm after PRD review)
- **SysOp review needed:** prioritization, model routing decisions, tool-surface enumeration
