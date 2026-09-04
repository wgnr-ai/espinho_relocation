# Espinho Healthcare + Elder-Care Landscape (Top-Priority: Leo's Care)

Last updated: 2026-09-02
Research period: 2026-09-02 (single-session live verification; all sources retrieved 2026-09-02/03)

## Informs
- docs/healthcare/ — SNS enrollment, coverage, copays, private insurance
- docs/leos-care/ — elder-care service landscape, care-plan skeleton, cost ranges
- budget/ — recurring health/elder-care cost bands for budget modeling

## Scope and Method

Live web verification only (no training-data claims). Every fact is tagged:
- **[OFFICIAL, source, date]** — government / regulator / insurer product page, fetched this session
- **[PRACTICAL, source, date]** — reputable secondary source (DECO, insurer FAQ, market data), fetched this session
- **[UNVERIFIED]** — could not be verified this session; must be confirmed before use

Citizen context: Wagner and Leo are Portuguese citizens returning from the US — this is repatriation, not immigration. No AIMA/visa steps apply to SNS enrollment. No diagnosis is assumed anywhere in this report; it maps the service landscape only.

Confidence per section: (a) High, (b) Medium-High, (c) High for product terms / Medium for prices, (d) Medium-High.

---

## (a) SNS Enrollment for PT Citizens Returning After Years Abroad

### Eligibility
1. Any person with Portuguese nationality may enroll at a centro de saúde; foreign nationals with residence authorization also may. **[OFFICIAL, gov.pt "Inscrever-se no centro de saúde" service page, retrieved 2026-09-02 — https://www.gov.pt/servicos/inscrever-se-no-centro-de-saude]**
2. Portuguese emigrants/returnees keep full SNS access and do not pay for care as residents; the Dec 2023 RNU reform (Despacho 1668/2023) reorganized *family-team assignment*, not entitlement. Access is universal; financial responsibility rules are separate. **[OFFICIAL, portugal.gov.pt Ministry of Health communiqué, 2023-12-13, retrieved 2026-09-02 — https://portugal.gov.pt/gc23/comunicacao/comunicados/emigrantes-portugueses-continuarao-a-ter-pleno-acesso-ao-sns]**
3. Timing: enrollment happens in person at the centro de saúde of the residential area; a utente (SNS) number is issued at enrollment if not already held. **[OFFICIAL, gov.pt, retrieved 2026-09-02]**

### Which centro de saúde serves Espinho
4. Espinho's public primary-care unit is **UCSP Espinho** (with USF Espinho inside it), part of **Unidade Local de Saúde de Gaia/Espinho, E.P.E.** under ARS Norte. **[OFFICIAL, BI-CSP (bicsp.min-saude.pt) unit listings for UCSP Espinho and USF Espinho under ULS Gaia/Espinho, retrieved 2026-09-02]**
5. UCSP Espinho address: **Rua 37, nº 700, 4500-330 Espinho** (document dated June 2023; confirm at ULSGE before visiting). **[PRACTICAL, ARS Norte unit-schedule document (via Scribd mirror, 06/2023), retrieved 2026-09-02 — address stale-flagged]**
6. Hospital reality: the Espinho/Gaia hospital network is **ULS Gaia/Espinho E.P.E.** (created Jan 2024, merging CHVNG/E hospitals with the Gaia/Espinho health centers), including Hospital Eduardo Santos Silva in Gaia (active emergency obstetric service, Oct 2025 press). **[OFFICIAL, sns.gov.pt entity page listing (title/snippet), retrieved 2026-09-02]** **[PRACTICAL, Público, 2025-10-06, retrieved 2026-09-02]** Note: **Hospital São Sebastião (Santa Maria da Feira)** is the seat of a *different* entity, ULS Entre Douro e Vouga (ULS EDV) — geographically close to Espinho but not the ULS that owns UCSP Espinho. **[PRACTICAL, SMN + justnews.pt reporting on ULS EDV, retrieved 2026-09-02]**

### Documents and process
7. Required: Portuguese ID (Cartão de Cidadão), SNS utente number (or get it on the spot), and residential address details; the service is run by ACSS. **[OFFICIAL, gov.pt, retrieved 2026-09-02]**
8. If mandatory registration data is missing, SNS contacts the utente through the contacts provided; if 90 days pass without contact, the registration lapses and must be redone. **[PRACTICAL, DECO PROteste guide on centro de saúde registration, retrieved 2026-09-02]**
9. Bring US medical records (vaccination history, medication list, recent labs) — recommended practice for the first consulta; no official requirement found. **[UNVERIFIED — practice-level advice, not from an official source]**

### Assigned-facility reality and wait times
10. The Ministry acknowledges known health-workforce scarcity: many people still lack an assigned family-health team, and the RNU reform prioritizes assignment "to those who most need it." **[OFFICIAL, portugal.gov.pt communiqué, 2023-12-13, retrieved 2026-09-02]**
11. Typical wait time for a family doctor assignment in the Espinho/Gaia catchment: **[UNVERIFIED — no dated public figure retrieved this session; query BI-CSP utente-coverage statistics or ULSGE at enrollment]**
12. Interim reality: care is delivered by the UCSP team (nurse triage, same-day slots) and SNS 24 line (808 24 24 24) regardless of doctor assignment. **[OFFICIAL structure: gov.pt + ERS referral guidance, retrieved 2026-09-02]**

---

## (b) SNS Coverage, Copays, and the Medication System

### Coverage and copays (taxas moderadoras)
1. Copays are only charged at **hospital emergency services accessed without prior SNS referral** (since 1 June 2022 regime change). **[PRACTICAL, DECO PROteste, retrieved 2026-09-02]** **[OFFICIAL, ERS FAQ "Taxas moderadoras do SNS", retrieved 2026-09-02 — https://www.ers.pt/pt/utentes/perguntas-frequentes/faq/taxas-moderadoras-do-sns/]**
2. Referral to an emergency department comes via Linha SNS 24 (808 24 24 24) triage or the centro de saúde; referred arrivals and admissions via urgency are exempt. **[OFFICIAL, ERS FAQ, retrieved 2026-09-02]**
3. Exemption categories include: pregnant women, minors, ≥60% incapacity (atestado médico de incapacidade multiuso), economic hardship, blood/organ donors, firefighters, transplant patients, registered unemployed (with subsidy ≤1,5×IAS), and others. **[OFFICIAL, ERS FAQ, retrieved 2026-09-02]**
4. 2026 parameters: IAS = **€537,13**; economic-hardship exemption threshold = **€805,70/month** per household head count basis (1,5×IAS). **[OFFICIAL, ERS FAQ, retrieved 2026-09-02]**
5. Governing value legislation: current copay values set under **Portaria n.º 480-A/2025/1 (30 Dec 2025)**; SNS price tables re-approved by **Portaria n.º 274/2026/1 (25 June 2026)**. **[OFFICIAL, ERS FAQ citations; Diário da República entry title, retrieved 2026-09-02]**
6. Euro values per act (e.g., specialty consult €7): **[UNVERIFIED — secondary snippets only; the governing portaria text could not be fetched this session. Do not budget from these numbers.]** One referenced ceiling: in urgency-admission contexts the user charge "cannot exceed €40". **[PRACTICAL, CGD Saldo Positivo page, retrieved 2026-09-02]**
7. Practical effect for a couple of two adults: routine centro de saúde care costs €0; an unreferred hospital ER visit costs a copay per person unless exempt (Leo may qualify for ≥60% incapacity exemption depending on assessment — see open questions). **[OFFICIAL structure, ERS; household application is analysis]**

### Medications (comparticipação) and senior continuity
8. Chronic-disease prescriptions: no package limits anymore; a prescription covers up to **12 months** of chronic medication; pharmacies dispense up to **2 months** at a time; renewal can be requested via the SNS 24 personal area, email, or the centro de Saúde administrative desk. **[OFFICIAL, sns.gov.pt "Medicação para doenças crónicas" (page updated 2023-11-13 — content date-flagged, still the published rule at retrieval), retrieved 2026-09-02]**
9. Free medication (100% state comparticipação) applies only to seniors receiving the **Complemento Solidário para Idosos (CSI)**. **[PRACTICAL, DECO PROteste, article 2024-06-26, retrieved 2026-09-02]**
10. Pensioners under the **Regime Especial de Comparticipação de Medicamentos (RECM)** (annual income < 14 minimum wages, certificate presented annually at the centro de saúde) get raised reimbursement tiers: 95% / 84% / 52% instead of 90% / 69% / 37%. **[PRACTICAL, DECO PROteste, 2024-06-26, retrieved 2026-09-02]**
11. Standard SNS reimbursement tiers for prescribed medicines: 90% / 69% / 37% by therapeutic class (generic substitution maximizes coverage). **[PRACTICAL, DECO, 2024-06-26 — tier structure cited inside RECM comparison, retrieved 2026-09-02]**
12. CSI income limits: single ≤ €7,208/year, couple ≤ €12,614/year; retirement age 66y4m (2024 figures). **[PRACTICAL, DECO, 2024-06-26 — figures stale-flagged, reverify for 2026 thresholds]**
13. US-to-PT medication continuity: prescriptions from US providers are not valid in PT pharmacies; continuity requires a first PT consult (private or SNS) to re-prescribe. **[UNVERIFIED — logical/legal-practice inference, confirm with a PT pharmacist or UCSP]**

---

## (c) Private Health Insurance for 2 Adults (One Senior)

### Senior-specific products (verifiable today)

**Médis Vintage / Ageas "Saúde Sénior" (same product family, cosseguro Ageas+Médis)**
- Subscription age **55–75**; **no permanence age limit**. From **€49,20/month** (quote base: 57-year-old, Vintage option). **[OFFICIAL, medis.pt/seguros-de-saude/vintage + ageas.pt Saúde Sénior product page, retrieved 2026-09-02]**
- Waiting periods (carências): 60 days ambulatory (consults/exams), 90 days hospitalization, 180 days grave illness (Plus only); not applied for accidents. **[OFFICIAL, medis.pt, retrieved 2026-09-02]**
- Cost-sharing: **50% of the medical act within the Rede Médis** (8,000+ facilities) for hospitalization and ambulatory; **no out-of-network reimbursement**; consult copay €17; home doctor visit €25; check-up €40. **[OFFICIAL, ageas.pt copayment tables, retrieved 2026-09-02]**
- Built-in home-care assistance after hospitalization (esp. relevant for Leo): physiotherapy at home (5 sessions Vintage / 10 Plus), home nursing (5/10), home hygiene/cleaning (5/10 days), home meal delivery (5/10 days), 1 home lab draw, 1 medicine delivery, 2 non-urgent transports. **[OFFICIAL, medis.pt Vintage coverage table, retrieved 2026-09-02]**
- Chronic disease: insurable — "if you have a chronic disease you can have Médis; preexisting conditions will be considered for use of the insurance." **[OFFICIAL, medis.pt FAQ, retrieved 2026-09-02]**

**Multicare 60+ (Fidelidade product, sold via CGD)**
- Two families: 60+ **Activcare** (subscribe from 61; **no medical exam or questionnaire**) and 60+ Multicare (61–70, with Individual Health Questionnaire). **[OFFICIAL, CGD product page oferta-multicare-60-mais, retrieved 2026-09-02]**
- No permanence age limit across the 60+ range; hospitalization capital up to **€200,000** (60+ Multicare 2); ambulatory capital **€2,000**; free periodic check-up (60d carência, then every 2 years); Medicina Online 24/7; **reimbursement of SNS taxas moderadoras** on some options; ~700-provider partner network including home-care and residential partners. **[OFFICIAL, CGD, retrieved 2026-09-02]**
- Subscription requires health questionnaire or phone medical interview for standard Multicare (per Multicare FAQ); Activcare avoids this. **[OFFICIAL, multicare.pt FAQ, retrieved 2026-09-02]**

### Market context for the second adult (Wagner)
- Standard health plans commonly cap first subscription at 60–70 years; Ageas Saúde Família allows subscription to age 70 (options 1–3) with a €750 annual franchise on hospitalization after 70 if subscribed 55+. **[OFFICIAL, ageas.pt FAQ, retrieved 2026-09-02]**
- General rule of thumb from consumer bodies: subscription limits of 60/65/70 depending on insurer; senior-specific products start at 55. **[PRACTICAL, DECO + ACP guidance, retrieved 2026-09-02]**

### Premium ranges by age band
- Verified single data point: Médis Vintage from €49,20/month at age 57. **[OFFICIAL, medis.pt, retrieved 2026-09-02]**
- Broader premium bands by age for Multicare/Médis/AdvanceCare/CUF plans: **[UNVERIFIED — requires per-carrier simulation (Multicare simulator; DECO simulator) with exact ages; do not budget from memory]**
- Reddit community data point (anecdotal, 3 people incl. teenager): €121/month in 2022 rising yearly. **[PRACTICAL, r/literaciafinanceira thread, retrieved 2026-09-02 — anecdotal, weight low]**

### How SNS + private combine in practice
- SNS remains the universal base (free primary care, emergency, hospitalization); private insurance is used for **faster elective specialist access and choice of doctor/facility** within the insurer network. **[PRACTICAL, DECO/Ajuda Real guides, retrieved 2026-09-02]**
- Senior products lean on **copayment/rede convencionada** (fixed discounted prices) rather than full reimbursement — out-of-network care is typically not covered in senior plans (Médis senior: 0% out-of-network). **[OFFICIAL, ageas.pt FAQ "comparticipações fora da Rede", retrieved 2026-09-02]**
- Multicare 60+ options can additionally reimburse SNS copays (taxas moderadoras), stitching the two systems together. **[OFFICIAL, CGD, retrieved 2026-09-02]**
- Emergency care still routes through SNS 24 / INEM regardless of insurance (insurers direct suspected emergencies to SNS). **[OFFICIAL structure: ERS + Ageas COVID-era guidance still stating SNS routing, retrieved 2026-09-02]**

---

## (d) Elder-Care Services: Espinho / Aveiro District

### The anchor institution: Santa Casa da Misericórdia de Espinho (SCME)
- SCME runs, for seniors: **Serviço de Apoio Domiciliário (home care), Centro de Dia (day center), Cuidar 24 (24h care program), and ERPI (residential care)**. **[OFFICIAL, scme.pt homepage navigation + senior section, retrieved 2026-09-02 — https://scme.pt]**
- SCME's SAD operates under a **cooperation agreement (acordo de cooperação) with Segurança Social**, i.e., it is a comparticipado (state-subsidized) social response with income-based family cost-sharing. **[OFFICIAL, SCME SAD Regulamento Interno PDF (2020 — date-flagged), retrieved 2026-09-02]**

### Public / IPSS vs private options and costs
- **SAD (home care) via IPSS/Misericórdias** (like SCME): subsidized by Segurança Social; the family pays a **comparticipação familiar calculated from household income**; frequent waiting lists and limited hours. **[OFFICIAL mechanism: gov.pt SAD service description (search-sourced snippet; full page blocked this session), retrieved 2026-09-02]** + **[PRACTICAL, via-senior 2026 guide, retrieved 2026-09-02]**
- **Private home-care market prices (2026 national guide)**: €7–12/hour; 4–8 h/day packages €400–900/month; night support €40–70/night; 24h live-out €1,200–2,500/month; live-in caregiver €1,000–1,800/month plus board. **[PRACTICAL, via-senior "Quanto Custa o Apoio Domiciliário 2026" (2026-01-20), retrieved 2026-09-02]**
- **Care homes (ERPI/lar), Jan 2026 national averages**: €1,852/month overall (+10% YoY); shared room €1,672; single room €2,035; Porto district average €2,014; average entry fee (jóia) €1,741 and deposit (caução) €1,684 — though 75,5% of network facilities charge no jóia and 78% no caução. Nursing-24h facilities from ~€2,190/month. **[PRACTICAL, Lares Online 2026 price table (2026-02-04), retrieved 2026-09-02]**
- **Continuity-of-care (RNCCI)**: convalescence/rehab/palliative units and **Equipas Comunitárias de Cuidados Continuados** are accessed by referral — from hospital via the discharge-management team (EGA→ECL) or from the community via USF/UCSP health professionals → Equipa Coordenadora Local. Family cannot self-admit; the entry point is the UCSP team. **[OFFICIAL, sns.gov.pt Cuidados Continuados page (updated 2021-04-28 — date-flagged), retrieved 2026-09-02]**
- **Informal caregiver support**: Estatuto do Cuidador Informal exists; principal-caregiver subsidy with household income cap of 1,3×IAS = **€698,27** (2026); from 2026 the subsidy no longer counts as income for other benefits. **[PRACTICAL, Montepio explainer 2026-03-19, single source — Medium confidence, retrieved 2026-09-02]**
- **Service directory**: Carta Social (cartasocial.pt) is the national registry to locate IPSS responses by concelho. **[OFFICIAL, cartasocial.pt, retrieved 2026-09-02]**

### Accessibility and transit
- SCME facilities are within Espinho concelho (urban, flat coastal town); specific facility accessibility ratings (step-free access, adapted transport) and municipal paratransit options: **[UNVERIFIED — not retrieved this session; requires SCME contact + Câmara Municipal de Espinho query]**

---

## Draft Leo Care-Plan Skeleton

*No diagnosis assumed. Sequence is designed so each step's outputs feed the next.*

### Phase 0 — Before leaving Orlando (T-6 to T-2 months)
1. Assemble US medical file: medication list (active ingredients, not brand names), vaccination record, recent labs/imaging reports, doctor's summary letter. *(No official requirement — practice-level.)* **[UNVERIFIED practice advice]**
2. Check medication availability: cross-reference each active ingredient on INFARMED's public medicine search; identify PT equivalents or alternatives to discuss with the first PT doctor. **[Action derived from INFARMED registry existence — INFARMED, retrieved 2026-09-02]**
3. Simulate senior insurance quotes (Médis Vintage vs Multicare 60+ Activcare) with Leo's exact age — Activcare needs no questionnaire; Vintage has richer home-care benefits. **[OFFICIAL product terms above]**

### Phase 1 — Arrival (T+0 to T+2 weeks)
4. Enroll both at **UCSP Espinho** (Rua 37 nº 700 — address stale-flagged, confirm) with Cartão de Cidadão + proof of address; obtain/reinstate utente numbers. **[OFFICIAL, gov.pt]**
5. Register SNS 24 personal-area accounts (prescription visibility + renewal requests). **[OFFICIAL, sns.gov.pt]**
6. Subscribe the chosen senior insurance for Leo on day 1 (carências clock starts: 60/90/180 days). **[OFFICIAL, medis.pt]**

### Phase 2 — First 90 days
7. First UCSP consult: present US records; get chronic prescriptions re-issued under PT system (12-month validity, 2-month pharmacy dispensing). **[OFFICIAL rules, sns.gov.pt]**
8. Ask UCSP about: family-doctor assignment timeline; incidence of Leo possibly needing an atestado médico de incapacidade multiuso (≥60% would exempt all copays — only pursue if clinically applicable). **[OFFICIAL, ERS]**
9. Meet SCME social services: tour Centro de Dia and SAD; ask current comparticipação-familiar quote for Leo's income situation and current waiting-list status. **[OFFICIAL, SCME exists with these services]**
10. If Wagner's income profile could ever approach RECM/CSI thresholds at pension age, keep annual-income documentation habit. **[PRACTICAL, DECO]**

### Phase 3 — Steady state (T+3 months onward)
11. Layered support model to cost (illustrative bands, all national 2026 data):
    - Layer 1 (universal): SNS primary care €0 + medications at RECM/standard tiers
    - Layer 2 (senior insurance): ~€50+/month (Médis from €49,20 at 57; exact at Leo's age [UNVERIFIED until simulated]) + 50% in-network cost-sharing
    - Layer 3 (home support, if/when needed): SCME SAD income-based comparticipação OR private €7–12/h, €400–900/mo (4–8h/day)
    - Layer 4 (residential fallback, if ever needed): lar/ERPI from ~€1,672 (shared, national avg) — Porto district avg €2,014
12. Escalation path if dependency increases: UCSP/USF referral → Equipa Coordenadora Local → RNCCI units or Equipa Comunitária de Cuidados Continuados. **[OFFICIAL, sns.gov.pt]**

### Approximate monthly cost envelope (2 adults, EUR, 2026 data)
| Line | Low | High | Basis |
|---|---|---|---|
| SNS care | €0 | €0 | [OFFICIAL gov.pt] |
| Copays (unreferred ER, non-exempt) | €0 | ~€40/event ×2 adults | [PRACTICAL CGD ceiling; per-act values UNVERIFIED] |
| Senior insurance (Leo) | ~€50 | to simulate | [OFFICIAL Médis base price at 57] |
| Adult insurance (Wagner) | to simulate | to simulate | [UNVERIFIED] |
| Medications (chronic, standard tiers) | 10% | 63% of retail by class | [PRACTICAL DECO tiers] |
| Home care if needed (private) | €400 | €2,500 | [PRACTICAL via-senior 2026] |

---

## Open Questions for the Family
1. **Leo's age and health profile for insurance pricing** — premium bands need exact age + carrier simulation; Médis quote tool + Multicare simulator produce real numbers in minutes.
2. **Medication list** — which active ingredients does Leo take daily? Determines (i) PT availability, (ii) which reimbursement tier applies, (iii) whether any need private prescription bridging.
3. **Income structure after the move** — pension source(s), PT tax residency timing. Determines RECM eligibility later, SNS copay exemption (hardship unlikely but incapacity route possible), and SCME SAD comparticipação quote.
4. **Incapacity status** — does Leo already hold any US disability documentation that could support a PT atestado médico de incapacidade multiuso application (≥60% = full copay exemption)? Only relevant if clinically warranted.
5. **Preferred support model** — day-center socialization (Centro de Dia SCME) vs home-based support (SAD/private hourly) vs family-led care with informal-caregiver statute for Wagner (subsidy €, income cap €698,27 — 2026).
6. **Housing accessibility** — single-level/elevator requirement feeding the housing workstream search parameters.

## Verification Gaps (not checked this session — explicit per policy)
- Exact 2026 taxa moderadora euro table (Portaria 480-A/2025/1 text unfetchable; DR page blocked). Impact: budget precision on ER visits only.
- UCSP Espinho current phone/hours (BI-CSP page 500-error; ARS Norte PDF is 06/2023).
- Family-doctor assignment wait statistics for ULSGE (BI-CSP stats pages not fetched).
- Carrier premium simulations at exact ages (requires interactive simulators).
- SCME current price list, vacancy status, facility accessibility audit, and Câmara Municipal de Espinho paratransit details (requires direct contact — next research step).
- CSI 2026 income thresholds (2024 figures cited, stale-flagged).

## Source Register (all retrieved 2026-09-02/03)
- gov.pt — Inscrever-se no centro de saúde: https://www.gov.pt/servicos/inscrever-se-no-centro-de-saude
- portugal.gov.pt — Emigrantes/SNS communiqué (2023-12-13): https://portugal.gov.pt/gc23/comunicacao/comunicados/emigrantes-portugueses-continuarao-a-ter-pleno-acesso-ao-sns
- ERS — Taxas moderadoras FAQ: https://www.ers.pt/pt/utentes/perguntas-frequentes/faq/taxas-moderadoras-do-sns/
- Diário da República — Portaria 274/2026/1 (title verified, content blocked): https://diariodarepublica.pt/dr/detalhe/portaria/274-2026-1138714124
- sns.gov.pt — Medicação doença crónica: https://www.sns.gov.pt/medicacao-doenca-cronica/ ; Cuidados Continuados: https://www.sns.gov.pt/sns-saude-mais/cuidados-continuados/ ; ULS Gaia/Espinho entity page (blocked, listing verified)
- BI-CSP — UCSP Espinho / USF Espinho listings: https://bicsp.min-saude.pt (unit pages under ARS Norte / ULS Gaia/Espinho)
- medis.pt — Seguro Saúde Vintage: https://www.medis.pt/seguros-de-saude/vintage/
- ageas.pt — Saúde Sénior: https://www.ageas.pt/particulares/produtos/saude/saude-senior/
- CGD — Multicare 60+: https://www.cgd.pt/Particulares/Seguros/pages/oferta-multicare-60-mais.aspx
- multicare.pt — 60+ product + FAQ: https://multicare.pt/proteger/saude-individual-e-familiar/multicare-60-mais
- scme.pt — Santa Casa da Misericórdia de Espinho: https://scme.pt ; SAD Regulamento Interno (2020): scme.pt/wp-content/uploads/2020/04/Regulamento-Interno-SAD.pdf
- via-senior.com — Apoio Domiciliário 2026 guide (2026-01-20): https://via-senior.com/quanto-custa-o-apoio-domiciliario-em-portugal-guia-2026/
- laresonline.pt — 2026 price table (2026-02-04): https://www.laresonline.pt/pt/blog/tabela-de-precos-lares-online-2026/
- DECO PROteste — medicamentos gratuitos idosos (2024-06-26): https://www.deco.proteste.pt/saude/medicamentos/noticias/medicamentos-gratuitos-idosos-tem-direito ; centro de saúde registration guide; isenção taxas moderadoras
- Montepio — cuidador informal subsidy (2026-03-19): https://www.montepio.org/ei/mais-recentes/subsidio-de-apoio-ao-cuidador-informal/
- CGD — Isenção taxas moderadoras: https://www.cgd.pt/Site/Saldo-Positivo/leis-e-impostos/Pages/isencao-de-taxas-moderadoras.aspx
- cartasocial.pt — national social-response registry
- Público (2025-10-06) — ULSGE hospital activity; SMN/justnews — ULS EDV/Hospital São Sebastião mapping; RTP — Gaia/Espinho urgências/SNS24 triage