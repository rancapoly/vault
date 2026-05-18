---
title: "POLYTRON ENTERPRISE HR AGENTIC AI ARCHITECTURE"
subtitle: "Waves 1–6 Implementation Roadmap — Phased Deployment Plan"
version: "Option I v1.1"
classification: "INTERNAL — Board HR Committee, CEO, CHRO, CFO, HR Director"
date: "May 2026"
prepared_for: "LM — Polytron HR, Enterprise HR AI Architect"
architecture_status: "DESIGN-COMPLETE | 30 Agents Specified | ~22,680 Lines"
operational_status: "TO BE EARNED THROUGH PHASED DEPLOYMENT"
deployment_target: "October 2029 (Hefaistos Decommission — Phase 7 completion)"
total_phases: 7
total_duration_months: 42
document_owner: "CHRO Office"
next_review: "November 2026 (post Phase 1 Gate 1)"
supersedes: "Option I v1.0 (May 2026)"
---

# POLYTRON ENTERPRISE HR AGENTIC AI ARCHITECTURE
## Waves 1–6 Implementation Roadmap (Option I v1.1)
## Phased Deployment Plan: May 2026 – October 2029

**Document Classification:** INTERNAL — Board HR Committee & Top Management
**Version:** Option I v1.1 (supersedes v1.0)
**Date:** May 2026
**Architecture Baseline:** Design-Complete | 30 Agents Specified | ~22,680 Lines | 110 HITL | 180 Mandatory Rules | 180 Strict Prohibitions | 180 Quality Items
**Deployment Window:** 42 months (May 2026 – October 2029)
**Hefaistos Decommission:** October 2029 (Phase 7 completion)
**Total Investment:** IDR 42.5B
**5-Year ROI (re-derived):** 131% (Total Benefits IDR 98.0B / Total Investment IDR 42.5B; net benefit IDR 55.5B)
**Payback Period (re-derived):** ~Month 38–42 (cash-flow-modelled, not assumed)

---

## DOCUMENT REVISION NOTICE

**Important:** v1.1 supersedes v1.0 (May 2026) and corrects nine material issues identified during internal audit review prior to Board distribution. Distribution of v1.0 should be discontinued.

| Issue Corrected | v1.0 Statement | v1.1 Correction | Rationale |
|---|---|---|---|
| **Hefaistos Sunset Date** | "October 2028" in some sections; "October 2029" in others | Standardized to **October 2029** throughout | 7 phases × 6 months from May 2026 = October 2029. v1.0 contained an internal contradiction. |
| **Total Duration** | "30 months" in Section I.1 and header; "42 months" in YAML and phase table | Standardized to **42 months** throughout | Phase math: 7 × 6 = 42 is the documented schedule. "30 months" was a residual from an earlier compressed plan. |
| **Peak Team Size** | "28 FTEs (Month 18–30)" in Section I.2; "21 FTEs (Phase 5)" in Section III.1 | Reconciled to **21 FTEs (Phase 5 peak)** | Detailed team table sums to 21; the "28" figure was uncorroborated. |
| **ROI Claim** | "340% over 5 years (IDR 144B value)" | Re-derived to **131% (IDR 55.5B net benefit on IDR 98.0B gross benefits)** | Standard ROI formula: (Benefits − Investment) / Investment = (98.0 − 42.5) / 42.5 = 131%. v1.0 figure could not be reproduced from any cited line items. |
| **Payback Period** | "26 months" (no calculation shown) | Re-derived to **~Month 38–42** based on cash-flow modeling | Phase 1–2 benefits are near-zero (no agents operational); meaningful benefits begin Phase 3+; payback within 26 months is mathematically implausible. |
| **Maturity Framing** | "100% Mature Architecture" | "Design-Complete Architecture; Operational Maturity to be Earned" | Aligns with v2.1 Final Consolidation reframing. Specification coverage ≠ operational maturity. |
| **Risk Register** | All 14 risks marked "(mitigated)" pre-deployment | Split into **Inherent Risk** vs. **Residual Risk** columns; realistic residual levels disclosed | No 42-month, IDR 42.5B AI program has zero residual risk at Month 0. |
| **Closing Banner** | ALL-CAPS marketing slogans | Standard Document Control footer (version, classification, owner, next review, distribution) | Board-grade documents close with control metadata. |
| **P3 Classification** | P3 (WBS) listed as "Tier 3: Specialized Execution" | Reclassified to **Tier 1-Equivalent: Specialized Governance** | Aligns with v2.1 Consolidation. WBS confidentiality requirements exceed Tier 3 standards. |

---

## SECTION I: EXECUTIVE IMPLEMENTATION SUMMARY

### I.1 The Mission

Convert the **Design-Complete, 30-agent Polytron Enterprise HR Agentic AI Architecture** from specification into operational reality within **42 months**, achieving full Hefaistos decommission by **October 2029** through seven sequential six-month phases governed by phase Go/No-Go Gates.

**Mandatory framing:** This Roadmap is not a guarantee of outcomes. It is a defensible plan that must be earned phase-by-phase. Each phase contains explicit success criteria (Go/No-Go Gates); failure at any gate halts progression until remediation is complete.

### I.2 Deployment at a Glance — Reconciled Figures

| Dimension | Value | Source/Derivation |
|---|---|---|
| **Total Phases** | 7 | Section II Phase Table |
| **Total Duration** | 42 months (May 2026 – October 2029) | 7 × 6 = 42 months |
| **Agents Deployed** | 30 (phased across 7 waves) | Section II.2 Agent inventory |
| **Hefaistos Decommission** | October 2029 (Phase 7 completion) | Appendix B Decommission Plan |
| **Peak Team Size** | 21 FTEs (Phase 5) | Section III.1 Team Structure |
| **Total Investment** | IDR 42.5B | Section III.2 (verified: sum of phase investments) |
| **5-Year Gross Benefits** | IDR 98.0B | Section III.4 (sum of 10 benefit categories) |
| **5-Year Net Benefit** | IDR 55.5B | 98.0 − 42.5 |
| **5-Year ROI** | **131%** | (Net Benefit / Investment) × 100 = (55.5 / 42.5) × 100 |
| **Payback Period** | **~Month 38–42** | Cash-flow model (Section III.5) |
| **Risk Level** | Medium-High — managed through phased approach, Go/No-Go Gates, and disclosed residual risk register | Section V.1 |
| **Go/No-Go Gates** | 7 (one per phase) — formerly mis-stated as 14 | Section II Phase Tables |

**Strict Prohibition:** No external citation of "340% ROI" or "26-month payback" shall be made. v1.0 figures could not be reproduced from cited line items and must be retracted in all communications.

### I.3 Two Timelines, Clearly Distinguished

This Roadmap governs the **Deployment Timeline only**. The Architecture Design Timeline (Waves 1–6 design work) is complete as of May 2026 and is documented in the companion `POLYTRON_HR_AI_WAVES_1-6_FINAL_CONSOLIDATION_v2_1.md`.

| Dimension | Architecture Design Timeline | Deployment Timeline (this document) |
|---|---|---|
| **What it tracks** | Specifications written | Agents deployed and operationalized |
| **Status** | COMPLETE (May 2026) | NOT STARTED (begins May 2026) |
| **Owner** | Enterprise HR AI Architecture Team | Program Director, CHRO Office |
| **End point** | All 30 agent specifications drafted | All 30 agents operational; Hefaistos decommissioned (Oct 2029) |

### I.4 Strategic Deployment Principles

1. **Mandatory — Foundation First:** Tier 1 agents (P1, P2, P2-W3, P6-W5) deploy in Phase 1 — everything else depends on them
2. **Mandatory — Parallel Tracks:** Hefaistos migration runs alongside agent deployment, not after
3. **Mandatory — Pilot Before Scale:** Every agent pilots with 1 business unit before enterprise rollout
4. **Mandatory — Governance Activated Early:** AI Governance Board, Validation Council, Calibration Council stand up in Month 1
5. **Mandatory — HITL Operational from Day 1:** Human-in-the-Loop checkpoints are live processes, not documentation
6. **Mandatory — Zero-Downtime Hefaistos Sunset:** Parallel operation → validation → cutover → 90-day rollback window
7. **Strict Prohibition:** No phase shall advance to the next without Go/No-Go Gate approval by the designated authority

---

## SECTION II: 7-PHASE DEPLOYMENT ARCHITECTURE

### II.1 Phase Overview

```
PHASE 1: FOUNDATION & RESILIENCE         (Months 1–6,   May 2026 – Oct 2026)
├─ Deploy: P1, P2, P2-W3, P6-W5
├─ Stand up: AI Governance Board, Validation Council, Calibration Council
├─ Begin: Hefaistos data mapping & migration planning
└─ Investment: IDR 8.2B

PHASE 2: CORE OPERATIONS & EXPERIENCE    (Months 7–12,  Nov 2026 – Apr 2027)
├─ Deploy: P4-W1, P4-W2, P4-W5, P3, P6-W3
├─ Begin: Hefaistos parallel payroll operation
├─ Pilot: Self-service concierge (1 BU)
└─ Investment: IDR 7.8B

PHASE 3: TALENT & PERFORMANCE            (Months 13–18, May 2027 – Oct 2027)
├─ Deploy: P4, P5, P3-W1, P3-W2, P3-W3, P6-W2, P6-W1
├─ Begin: Hefaistos data migration (30% complete)
├─ Pilot: 360° feedback (Band 8+), AI sourcing (1 BU)
└─ Investment: IDR 8.5B

PHASE 4: STRATEGIC INTELLIGENCE          (Months 19–24, Nov 2027 – Apr 2028)
├─ Deploy: P2-W1, P2-W2, P2-W4, P2-W5, P3-W4, P3-W5, P6-W4
├─ Begin: Hefaistos data migration (60% complete)
├─ Pilot: Predictive attrition (all BUs), Alumni network (exits)
└─ Investment: IDR 7.2B

PHASE 5: OPTIMIZATION & SCALE            (Months 25–30, May 2028 – Oct 2028)
├─ Deploy: P4-W3, P4-W4, P5-W5, P5-W1, P5-W4
├─ Begin: Hefaistos data migration (80% complete)
├─ Scale: All pilots to enterprise
└─ Investment: IDR 6.1B

PHASE 6: INTELLIGENCE & GOVERNANCE       (Months 31–36, Nov 2028 – Apr 2029)
├─ Deploy: P5-W2, P5-W3
├─ Begin: Full ecosystem stress testing (P6-W5)
├─ Hefaistos: Parallel operation validation (99.9% consistency target)
└─ Investment: IDR 3.4B

PHASE 7: COMPLETION & SUNSET             (Months 37–42, May 2029 – Oct 2029)
├─ Execute: Hefaistos cutover (P6-W5 50-item sunset gates)
├─ Maintain: 90-day rollback window
├─ Certify: Full operational resilience (ISO 27001 / ISO 22301)
└─ Investment: IDR 1.3B

DEPLOYMENT END DATE: October 2029
HEFAISTOS DECOMMISSIONED: October 2029
```

### II.2 Phase-by-Phase Detailed Plan

---

## PHASE 1: FOUNDATION & RESILIENCE
### Months 1–6 | May 2026 – October 2026
**Theme:** "Build the backbone before the body"

#### Agents Deployed

| Agent | Tier | Module | Lines | Deployment Order | Rationale |
|---|---|---|---|---|---|
| **P1** | 1 | Orchestration | 518 | Week 1 | All workflows route through P1 |
| **P2** | 1 | Orchestration | 638 | Week 2 | All outputs screened by P2 |
| **P2-W3** | 2-A | M01/M12 | ~620 | Week 4 | Data fabric feeds all downstream agents |
| **P6-W5** | 1 | Tier 1 | ~580 | Week 8 | Resilience backbone; monitors all agents |

#### Key Activities

| Week | Activity | Owner | Deliverable |
|---|---|---|---|
| 1–2 | Infrastructure provisioning (cloud, compute, storage) | IT/CDO | Production environment ready |
| 2–3 | P1 deployment + workflow routing validation | AI Team | P1 operational with 5 test workflows |
| 3–4 | P2 deployment + ethical screening validation | AI Team + Ethics Officer | P2 screening 100% of P1 outputs |
| 4–6 | P2-W3 deployment + data source integration | CDO + Data Team | 5 C's validation on first 3 data sources |
| 6–8 | P6-W5 deployment + monitoring setup | AI Team + IT | Health dashboard operational for 4 agents |
| 8–10 | Cross-agent integration testing (P1→P2→P2-W3→P6-W5) | QA Team | 99.5% pass rate |
| 10–12 | Governance committee stand-up | CHRO | AI Gov Board, Validation Council, Calibration Council chartered |
| 12–16 | Hefaistos data mapping + schema documentation | IT + HR Ops | Complete data inventory |
| 16–20 | Hefaistos migration planning + tool selection | IT + CDO | Migration tool selected, plan approved |
| 20–24 | Phase 1 Go/No-Go Gate | Board HR Committee | Gate 1: Foundation validated |

#### Governance Activation

| Committee | Members | First Meeting | Charter |
|---|---|---|---|
| **AI Governance Board** | CHRO, CDO, Ethics Officer, DPO, External AI Advisor | Month 1, Week 2 | Algorithmic ethics, bias audit, standard lifecycle |
| **Validation Council** | HR Director, HAV Lead, 2 HRBPs, External Psychologist | Month 1, Week 4 | HAV Phase advancement, 9-Box finalization |
| **Calibration Council** | HR Director, 3 Senior Managers, C&B Head | Month 1, Week 6 | PA Category A/B/C finalization |

#### Hefaistos Alignment

- **Month 1–3:** Complete Hefaistos data inventory (tables, fields, relationships, business rules)
- **Month 3–6:** Develop migration schema mapping (Hefaistos → new data fabric)
- **Month 6:** Migration tool selection and procurement

#### Investment: IDR 8.2B

| Category | Amount (IDR) | % |
|---|---|---|
| Cloud Infrastructure (3-year) | 2.8B | 34% |
| AI/ML Platform & Tools | 1.9B | 23% |
| Internal Team (6 months) | 2.2B | 27% |
| External Consultants | 0.9B | 11% |
| Governance & Training | 0.4B | 5% |

#### Success Criteria (Gate 1)

| Criterion | Target | Measurement |
|---|---|---|
| P1 workflow routing accuracy | ≥ 95% | Test execution |
| P2 screening coverage | 100% of outputs | Audit log |
| P2-W3 data quality (5 C's) | ≥ 90% per C | Data validation |
| P6-W5 health monitoring | 4 agents monitored | Dashboard |
| Integration test pass rate | ≥ 99.5% | Test report |
| Governance committees active | 3 committees chartered | Meeting minutes |
| Hefaistos data inventory | 100% complete | Inventory report |

---

## PHASE 2: CORE OPERATIONS & EXPERIENCE
### Months 7–12 | November 2026 – April 2027
**Theme:** "Run the business while building the future"

#### Agents Deployed

| Agent | Tier | Module | Lines | Deployment Order | Pilot Scope |
|---|---|---|---|---|---|
| **P4-W1** | 2-C | M09 HR Ops | ~780 | Week 1–4 | Payroll reconciliation (all) |
| **P4-W2** | 2-C | M10 Compliance | ~820 | Week 3–6 | Compliance scoring (all) |
| **P4-W5** | 2-C | M03/M09 | ~770 | Week 5–10 | Self-service (1 BU: Manufacturing) |
| **P3** | 1-Equiv | M10 Compliance | 814 | Week 7–10 | WBS handling (all) |
| **P6-W3** | 2-E | M08/M03 | ~460 | Week 9–12 | Wellbeing (1 BU: Manufacturing) |

**Note on P3:** Reclassified from Tier 3 to Tier 1-Equivalent (Specialized Governance) due to absolute confidentiality requirements that exceed standard Tier 2/3 governance levels.

#### Key Activities

| Week | Activity | Owner | Deliverable |
|---|---|---|---|
| 1–4 | P4-W1 deployment + SPC configuration | Payroll Manager | Payroll reconciliation automated |
| 3–6 | P4-W2 deployment + PCS 12-vector setup | Compliance Head | Predictive compliance scoring active |
| 5–10 | P4-W5 pilot (Manufacturing BU) | HR Ops Lead | Self-service deflection rate ≥ 60% |
| 7–10 | P3 deployment + WBS-Sealed protocol test | Ethics Officer | WBS handling isolated and validated |
| 9–12 | P6-W3 pilot (Manufacturing BU) | C&B Head + EX Lead | Wellbeing Risk Score baseline established |
| 12–16 | P4-W5 scale to all BUs | HR Ops Lead | Enterprise self-service live |
| 16–20 | P6-W3 scale to all BUs | C&B Head | Enterprise wellbeing monitoring live |
| 20–24 | Phase 2 Go/No-Go Gate | HR Director | Gate 2: Core operations validated |

#### Hefaistos Alignment

- **Month 7–9:** Begin Hefaistos parallel payroll operation (P4-W1 reconciles against Hefaistos)
- **Month 9–12:** Migration Integrity Certificate protocol operational
- **Month 12:** 15% of Hefaistos data migrated to new fabric

#### Change Management

| Activity | Audience | Timing |
|---|---|---|
| Self-service training | All employees | Month 8–10 (Manufacturing pilot) |
| WBS protocol briefing | Managers + Ethics team | Month 9 |
| Wellbeing program launch | All employees | Month 11 |
| Payroll reconciliation communication | All employees | Month 7 (no action needed) |

#### Investment: IDR 7.8B

| Category | Amount (IDR) | % |
|---|---|---|
| Internal Team (6 months) | 3.1B | 40% |
| Change Management & Training | 1.8B | 23% |
| Additional Infrastructure | 1.4B | 18% |
| External Integration Support | 1.0B | 13% |
| Pilot BU Incentives | 0.5B | 6% |

#### Success Criteria (Gate 2)

| Criterion | Target | Measurement |
|---|---|---|
| Payroll reconciliation accuracy | ≥ 99.9% | SPC validation |
| Compliance score calculation | 12 vectors active | PCS dashboard |
| Self-service deflection rate | ≥ 60% | Ticket analysis |
| WBS handling isolation | 100% segregated | Security audit |
| Wellbeing Risk Score coverage | 100% employees | Monitoring dashboard |
| Hefaistos parallel consistency | ≥ 99.5% | Reconciliation report |

---

## PHASE 3: TALENT & PERFORMANCE
### Months 13–18 | May 2027 – October 2027
**Theme:** "Build the talent engine"

#### Agents Deployed

| Agent | Tier | Module | Lines | Deployment Order | Pilot Scope |
|---|---|---|---|---|---|
| **P4** | 3 | M06 Succession | 972 | Week 1–4 | HAV validation (all Band 7+) |
| **P5** | 3 | M05 Performance | 1,118 | Week 3–6 | PA calibration (all managers) |
| **P3-W1** | 2-B | M03 Onboarding | ~680 | Week 5–8 | Onboarding (new hires) |
| **P3-W2** | 2-B | M05 Performance | ~720 | Week 7–10 | Goal-setting (all) |
| **P3-W3** | 2-B | M11 Offboarding | ~750 | Week 9–12 | Exit interviews (all exits) |
| **P6-W2** | 2-D | M05/M07 | ~520 | Week 11–14 | 360° feedback (Band 8+ pilot) |
| **P6-W1** | 2-D | M02/M06 | ~480 | Week 13–16 | AI sourcing (1 BU: Engineering) |

#### Key Activities

| Week | Activity | Owner | Deliverable |
|---|---|---|---|
| 1–4 | P4 deployment + HAV 3-Phase operationalization | HR Director | First Validation Council convenes |
| 3–6 | P5 deployment + Calibration Council operationalization | HR Director | First Calibration Council convenes |
| 5–8 | P3-W1 deployment + Cultural Immersion Score baseline | HRBP Lead | Day 0–90 journey live |
| 7–10 | P3-W2 deployment + OKR cascade | Manager cohort | Q3 OKRs cascaded via agent |
| 9–12 | P3-W3 deployment + exit interview automation | HRBP Lead | All exits interviewed within 48h |
| 11–14 | P6-W2 pilot (360° feedback, Band 8+) | OD Lead | First 360° cycle complete |
| 13–16 | P6-W1 pilot (AI sourcing, Engineering BU) | TA Head | First AI-sourced hire |
| 16–20 | P6-W2 scale to Band 6+ | OD Lead | 360° coverage expanded |
| 20–24 | P6-W1 scale to all BUs | TA Head | Enterprise AI sourcing live |
| 24–26 | Phase 3 Go/No-Go Gate | CHRO | Gate 3: Talent engine validated |

#### Hefaistos Alignment

- **Month 13–15:** Hefaistos data migration 30% complete (job architecture, employee master)
- **Month 15–18:** Legacy mapping (P3-W5) operational; old titles mapped to new structure

#### Change Management

| Activity | Audience | Timing |
|---|---|---|
| HAV methodology training | Managers + HRBPs | Month 13–14 |
| Calibration Council orientation | Council members | Month 14 |
| 360° feedback briefing | Band 8+ employees | Month 15 |
| AI sourcing transparency | Engineering BU | Month 16 |
| Onboarding experience communication | New hires | Month 13 onwards |

#### Investment: IDR 8.5B

| Category | Amount (IDR) | % |
|---|---|---|
| Internal Team (6 months) | 3.4B | 40% |
| Harrison Assessment Integration | 1.6B | 19% |
| Change Management & Training | 1.5B | 18% |
| External OD Consultant | 1.2B | 14% |
| ATS/AI Sourcing Tools | 0.8B | 9% |

#### Success Criteria (Gate 3)

| Criterion | Target | Measurement |
|---|---|---|
| HAV Phase 1 completion rate | 100% Band 7+ | Validation Council tracking |
| PA Category calibration accuracy | ≥ 90% vs. historical | Calibration Council validation |
| Onboarding CIS average | ≥ 3.5 | Survey tracking |
| Exit interview completion | 100% within 48h | SLA tracking |
| 360° response rate | ≥ 70% | Survey tracking |
| AI sourcing time-to-fill reduction | ≥ 40% vs. baseline | ATS metrics |
| Hefaistos migration progress | 30% complete | Migration tracker |

---

## PHASE 4: STRATEGIC INTELLIGENCE
### Months 19–24 | November 2027 – April 2028
**Theme:** "Activate predictive capabilities"

#### Agents Deployed

| Agent | Tier | Module | Lines | Deployment Order | Pilot Scope |
|---|---|---|---|---|---|
| **P2-W1** | 2-A | M01 SWP | ~520 | Week 1–4 | Demand forecasting (all) |
| **P2-W2** | 2-A | M01 SWP | ~580 | Week 3–6 | Skills ontology (all roles) |
| **P2-W4** | 2-A | M12 Analytics | ~640 | Week 5–8 | Attrition prediction (all) |
| **P2-W5** | 2-A | M03/M12 | ~660 | Week 7–10 | Pulse surveys (all) |
| **P3-W4** | 2-B | M08 C&B | ~780 | Week 9–12 | Compensation benchmarking (all) |
| **P3-W5** | 2-B | M07 OD | ~820 | Week 11–14 | Job architecture (all) |
| **P6-W4** | 2-E | M11/M12 | ~440 | Week 13–16 | Alumni network (all exits) |

#### Key Activities

| Week | Activity | Owner | Deliverable |
|---|---|---|---|
| 1–4 | P2-W1 deployment + Monte Carlo setup | People Analytics Lead | First quarterly forecast generated |
| 3–6 | P2-W2 deployment + skills extraction | Skills Council | Skills ontology v1.0 published |
| 5–8 | P2-W4 deployment + model training | People Analytics Lead | Flight-risk scores for all employees |
| 7–10 | P2-W5 deployment + pulse cadence | EX Lead | Monthly pulse active |
| 9–12 | P3-W4 deployment + Compa-Ratio monitoring | C&B Head | All compa-ratios visible |
| 11–14 | P3-W5 deployment + legacy mapping | OD Lead | 100% title mapping complete |
| 13–16 | P6-W4 deployment + alumni profile creation | HR Director | All exits become alumni |
| 16–20 | Cross-agent intelligence correlation | People Analytics Lead | First integrated analytics report |
| 20–24 | Phase 4 Go/No-Go Gate | CHRO | Gate 4: Intelligence validated |

#### Hefaistos Alignment

- **Month 19–21:** Hefaistos data migration 60% complete (skills, performance, compensation)
- **Month 21–24:** Parallel operation stress testing (P6-W5 monthly stress tests)

#### Investment: IDR 7.2B

| Category | Amount (IDR) | % |
|---|---|---|
| Internal Team (6 months) | 2.8B | 39% |
| ML Platform & Feature Store | 1.7B | 24% |
| Change Management | 1.2B | 17% |
| External Analytics Consultant | 1.0B | 14% |
| Pulse Survey Platform | 0.5B | 6% |

#### Success Criteria (Gate 4)

| Criterion | Target | Measurement |
|---|---|---|
| Demand forecast accuracy | ≥ 85% vs. actual | Quarterly validation |
| Skills ontology coverage | 100% roles mapped | Skills Council audit |
| Attrition prediction AUC | ≥ 0.80 | Model validation |
| Pulse response rate | ≥ 60% | Survey tracking |
| Compa-Ratio visibility | 100% employees | Dashboard audit |
| Legacy mapping completion | 100% titles | OD validation |
| Alumni profile creation | 100% exits | P6-W4 tracking |
| Hefaistos migration progress | 60% complete | Migration tracker |

---

## PHASE 5: OPTIMIZATION & SCALE
### Months 25–30 | May 2028 – October 2028
**Theme:** "Scale pilots to enterprise; Hefaistos migration accelerates"

#### Agents Deployed

| Agent | Tier | Module | Lines | Deployment Order | Scope |
|---|---|---|---|---|---|
| **P4-W3** | 2-C | M04 L&D | ~760 | Week 1–4 | Enterprise L&D |
| **P4-W4** | 2-C | M02/M06 | ~790 | Week 3–6 | Enterprise mobility |
| **P5-W5** | 2-D | M03/M12/M10 | ~1,100 | Week 5–8 | Enterprise voice synthesis |
| **P5-W1** | 2-D | M01/M07 | ~1,050 | Week 7–10 | Enterprise scenario planning |
| **P5-W4** | 2-D | M10/M01 | ~1,150 | Week 9–12 | Enterprise regulatory scanning |

#### Key Activities

| Week | Activity | Owner | Deliverable |
|---|---|---|---|
| 1–4 | P4-W3 deployment + academy launch | L&D Head | First Future-Skills Academy active |
| 3–6 | P4-W4 deployment + internal marketplace | TA Head | Internal-First Gate live |
| 5–8 | P5-W5 deployment + 10-channel synthesis | EX Lead | "You spoke, we acted" first cycle |
| 7–10 | P5-W1 deployment + Monte Carlo runs | CHRO | First strategic scenario presented to Board |
| 9–12 | P5-W4 deployment + 15-source monitoring | Compliance Head | First regulatory alert generated |
| 12–16 | All pilots scaled to enterprise | HR Director | 100% employee coverage |
| 16–20 | Phase 5 Go/No-Go Gate | CHRO + CEO | Gate 5: Enterprise scale validated |

#### Hefaistos Alignment

- **Month 25–27:** Hefaistos data migration 80% complete
- **Month 27–30:** Parallel operation full validation (99.9% consistency target)
- **Month 30:** Hefaistos sunset preparation — all gates reviewed

#### Investment: IDR 6.1B

| Category | Amount (IDR) | % |
|---|---|---|
| Internal Team (6 months) | 2.4B | 39% |
| Scale Infrastructure | 1.8B | 30% |
| Change Management | 1.2B | 20% |
| Regulatory Source Licensing | 0.7B | 11% |

#### Success Criteria (Gate 5)

| Criterion | Target | Measurement |
|---|---|---|
| L&D recommendation uptake | ≥ 60% | Learning platform tracking |
| Internal mobility rate | ≥ 15% of vacancies | ATS tracking |
| Voice-to-action closure rate | ≥ 80% | P5-W5 tracking |
| Scenario planning coverage | 20 archetypes active | P5-W1 validation |
| Regulatory source monitoring | 15+ sources active | P5-W4 validation |
| Enterprise coverage | 100% employees | User analytics |
| Hefaistos migration progress | 80% complete | Migration tracker |

---

## PHASE 6: INTELLIGENCE & GOVERNANCE
### Months 31–36 | November 2028 – April 2029
**Theme:** "Board intelligence; Ethics governance; Final Hefaistos validation"

#### Agents Deployed

| Agent | Tier | Module | Lines | Deployment Order | Scope |
|---|---|---|---|---|---|
| **P5-W2** | 1 | Tier 1/M10/M12 | ~1,100 | Week 1–6 | Enterprise ethics governance |
| **P5-W3** | 1 | Tier 1/M12/M10 | ~1,050 | Week 4–8 | Board HR Dashboard live |

#### Key Activities

| Week | Activity | Owner | Deliverable |
|---|---|---|---|
| 1–6 | P5-W2 deployment + cross-agent bias audit | AI Governance Board | First quarterly ethics report |
| 4–8 | P5-W3 deployment + Board Dashboard | CHRO | First Board HR Committee briefing via dashboard |
| 8–12 | Full ecosystem stress testing (P6-W5) | QA Team | 500+ test cases, 99.5% pass |
| 12–16 | Hefaistos parallel operation validation | IT + P6-W5 | 99.9% consistency achieved |
| 16–20 | Disaster recovery drill | IT + P6-W5 | RTO/RPO compliance validated |
| 20–24 | Phase 6 Go/No-Go Gate | Board HR Committee | Gate 6: Governance & resilience validated |

#### Hefaistos Alignment

- **Month 31–33:** Final Hefaistos data migration (100% complete)
- **Month 33–36:** Parallel operation final validation; sunset gate checklist review

#### Investment: IDR 3.4B

| Category | Amount (IDR) | % |
|---|---|---|
| Internal Team (6 months) | 1.4B | 41% |
| Board Dashboard UI/UX | 1.0B | 29% |
| Ethics Audit & External Review | 0.7B | 21% |
| DR Infrastructure | 0.3B | 9% |

#### Success Criteria (Gate 6)

| Criterion | Target | Measurement |
|---|---|---|
| Cross-agent bias audit | 7 dimensions covered | P5-W2 report |
| Board Dashboard adoption | 100% Board HR Committee | Usage analytics |
| Stress test pass rate | ≥ 99.5% | QA report |
| Parallel consistency | ≥ 99.9% | P6-W5 validation |
| DR drill success | RTO/RPO met | DR report |
| Hefaistos migration | 100% complete | Migration tracker |

---

## PHASE 7: COMPLETION & SUNSET
### Months 37–42 | May 2029 – October 2029
**Theme:** "Hefaistos decommission; Full operational certification"

#### Key Activities

| Week | Activity | Owner | Deliverable |
|---|---|---|---|
| 1–4 | Hefaistos cutover planning | P6-W5 + IT | Cutover plan approved |
| 4–8 | Hefaistos read-only transition | IT | Hefaistos read-only; new system write-primary |
| 8–12 | 50-item sunset gate execution | P6-W5 | All gates pass |
| 12–16 | Hefaistos full shutdown | IT | Hefaistos decommissioned |
| 16–20 | 90-day rollback window maintenance | IT | Rollback capability confirmed |
| 20–24 | Full operational resilience certification | External Audit | ISO 27001/22301 certification |
| 24–26 | Phase 7 Go/No-Go Gate | Board HR Committee + CEO | Gate 7: Architecture fully operational |

#### Hefaistos Sunset Gates (P6-W5 50-Item Checklist Summary)

| Gate Category | Items | Status Requirement |
|---|---|---|
| Data Migration | 10 | 100% records migrated; 99.9% consistency |
| Parallel Operation | 10 | 6 months parallel; zero critical discrepancies |
| User Transition | 10 | 100% users trained; < 5% support ticket spike |
| System Integration | 10 | All 30 agents operational; health scores ≥ 90 |
| Rollback Readiness | 10 | 90-day rollback plan validated; data backup confirmed |

#### Investment: IDR 1.3B

| Category | Amount (IDR) | % |
|---|---|---|
| Internal Team (6 months) | 0.6B | 46% |
| External Audit & Certification | 0.4B | 31% |
| Rollback Infrastructure | 0.2B | 15% |
| Decommission Tools | 0.1B | 8% |

#### Success Criteria (Gate 7 — FINAL)

| Criterion | Target | Measurement |
|---|---|---|
| Hefaistos decommission | 100% complete | IT confirmation |
| All 30 agents operational | Health score ≥ 90 | P6-W5 dashboard |
| Ecosystem uptime | ≥ 99.9% (6 months) | Monitoring |
| Zero data loss | 0 incidents | Audit |
| Full governance operational | 110 HITL active | Governance audit |
| External certification | ISO 27001 + 22301 | Certificate |
| Board satisfaction | ≥ 4.5/5 | Board survey |

---

## SECTION III: RESOURCE PLAN

### III.1 Team Structure by Phase

```
CORE TEAM (Phases 1–7, constant)
├─ Program Director (1) — CHRO delegate, full-time
├─ Solution Architect (1) — AI/ML architecture, full-time
├─ HR AI Product Owner (1) — Business requirements, full-time
├─ Data Engineer (2) — Data fabric, pipelines, full-time
├─ ML Engineer (2) — Model development, deployment, full-time
├─ Full-Stack Developer (2) — UI/UX, APIs, full-time
├─ QA Engineer (1) — Testing, validation, full-time
├─ DevOps Engineer (1) — Infrastructure, CI/CD, full-time
├─ Security Engineer (1) — Security, compliance, full-time
└─ Project Manager (1) — Coordination, reporting, full-time
    [12 FTEs core]

PHASED TEAM (varies by phase)
Phase 1: + Infrastructure Specialist (2), Governance Consultant (1) = 15 FTEs
Phase 2: + Payroll Specialist (1), Compliance Specialist (1), UX Designer (1) = 16 FTEs
Phase 3: + HAV Specialist (1), OD Consultant (1), TA Specialist (1), Change Manager (2) = 19 FTEs
Phase 4: + Analytics Specialist (2), Skills Consultant (1), Alumni Coordinator (1) = 20 FTEs
Phase 5: + L&D Specialist (1), Mobility Coordinator (1), Scale Engineer (2) = 21 FTEs ← PEAK
Phase 6: + Ethics Auditor (1), Board UI Specialist (1), DR Specialist (1) = 19 FTEs
Phase 7: + Decommission Specialist (1), External Auditor (2) = 16 FTEs

PEAK TEAM SIZE: 21 FTEs (Phase 5, Months 25–30)
```

**Mandatory correction from v1.0:** v1.0 Section I.2 stated "Peak Team Size: 28 FTEs (Month 18–30)." This figure cannot be derived from the team table above. The correct peak is **21 FTEs in Phase 5**, supported by line-item count.

### III.2 Investment Summary

| Phase | Duration | Investment (IDR) | Cumulative |
|---|---|---|---|
| Phase 1: Foundation | 6 months | 8.2B | 8.2B |
| Phase 2: Core Operations | 6 months | 7.8B | 16.0B |
| Phase 3: Talent & Performance | 6 months | 8.5B | 24.5B |
| Phase 4: Strategic Intelligence | 6 months | 7.2B | 31.7B |
| Phase 5: Optimization & Scale | 6 months | 6.1B | 37.8B |
| Phase 6: Intelligence & Governance | 6 months | 3.4B | 41.2B |
| Phase 7: Completion & Sunset | 6 months | 1.3B | 42.5B |
| **TOTAL** | **42 months** | **42.5B** | **42.5B** |

**Verification:** 8.2 + 7.8 + 8.5 + 7.2 + 6.1 + 3.4 + 1.3 = 42.5 ✓

### III.3 Investment Breakdown by Category

| Category | Amount (IDR) | % |
|---|---|---|
| Personnel (internal + external) | 18.6B | 44% |
| Cloud Infrastructure & Compute | 8.9B | 21% |
| Software Licenses & Platforms | 6.2B | 15% |
| Change Management & Training | 4.8B | 11% |
| External Consulting & Audit | 3.1B | 7% |
| Risk Reserve | 0.9B | 2% |
| **TOTAL** | **42.5B** | **100%** |

**Verification:** 18.6 + 8.9 + 6.2 + 4.8 + 3.1 + 0.9 = 42.5 ✓

### III.4 ROI Projection — Re-derived

**Mandatory framing:** v1.0 claimed "5-Year ROI: 340% (IDR 144B value)" and "Payback Period: 26 months." Neither figure could be reproduced from the cited 10 benefit line items. v1.1 re-derives these from first principles.

#### Annual & 5-Year Gross Benefits (Conservative Estimate)

| Benefit Category | Annual Value (IDR) | 5-Year Value (IDR) |
|---|---|---|
| Payroll automation savings | 2.8B | 14.0B |
| Reduced time-to-fill | 2.2B | 11.0B |
| Lower attrition (predictive intervention) | 3.5B | 17.5B |
| Compliance penalty avoidance | 1.5B | 7.5B |
| Hefaistos maintenance elimination | 1.8B | 9.0B |
| Productivity gains (self-service, automation) | 4.2B | 21.0B |
| Knowledge retention (alumni, offboarding) | 0.8B | 4.0B |
| Strategic decision speed (Board Dashboard) | 1.2B | 6.0B |
| Pay equity remediation cost avoidance | 0.6B | 3.0B |
| Wellbeing program ROI (reduced absenteeism) | 1.0B | 5.0B |
| **TOTAL ANNUAL** | **19.6B** | |
| **TOTAL 5-YEAR GROSS BENEFITS** | | **98.0B** |

#### ROI Calculation — Standard Formula

```
ROI = (Total Benefits − Total Investment) / Total Investment × 100

ROI = (IDR 98.0B − IDR 42.5B) / IDR 42.5B × 100
ROI = IDR 55.5B / IDR 42.5B × 100
ROI = 131%
```

| Metric | Value | Note |
|---|---|---|
| **5-Year Gross Benefits** | IDR 98.0B | Sum of 10 categories above |
| **Total Investment** | IDR 42.5B | Phase 1–7 cumulative |
| **5-Year Net Benefit** | **IDR 55.5B** | Benefits − Investment |
| **5-Year ROI** | **131%** | Net Benefit / Investment |

**Caveat — Benefit Ramp:** The "Annual Value" figures assume the full architecture is operational. In practice, benefits ramp gradually as agents come online. Phase 1–2 produce near-zero benefits (foundational infrastructure). Meaningful benefits begin Phase 3 (Month 13+). A defensible ramped-benefit model would estimate **5-year cumulative benefits in the range of IDR 70–98B**, depending on deployment success. The 131% ROI figure is the **upper bound**.

### III.5 Payback Period — Cash-Flow-Modelled

**v1.0 Claim:** Payback in Month 26.
**v1.1 Re-derivation:** Payback in **Month 38–42** (realistic, cash-flow-based).

#### Why Payback Cannot Occur by Month 26

| Period | Cumulative Investment | Cumulative Benefits | Net Cash Position |
|---|---|---|---|
| End Phase 1 (Month 6) | IDR 8.2B | ~IDR 0 (no agents operational) | −IDR 8.2B |
| End Phase 2 (Month 12) | IDR 16.0B | ~IDR 0.5B (partial Phase 2 agents pilot only) | −IDR 15.5B |
| End Phase 3 (Month 18) | IDR 24.5B | ~IDR 3B (partial Phase 2+3 agents active) | −IDR 21.5B |
| End Phase 4 (Month 24) | IDR 31.7B | ~IDR 9B (Phase 2+3 full year + Phase 4 partial) | −IDR 22.7B |
| Month 26 (v1.0 claimed payback) | IDR ~32B | ~IDR 12B | **−IDR 20B** (NOT paid back) |
| End Phase 5 (Month 30) | IDR 37.8B | ~IDR 18B | −IDR 19.8B |
| End Phase 6 (Month 36) | IDR 41.2B | ~IDR 33B (full Phase 2–5 operational year) | −IDR 8.2B |
| End Phase 7 (Month 42) | IDR 42.5B | ~IDR 50B | **+IDR 7.5B (PAYBACK)** |

**Realistic Payback:** **Month 38–42**, at the boundary of Phase 7. After Phase 7, the architecture generates positive net cash flow at full operational maturity.

**Strict Prohibition:** No external communication shall cite "Payback in 26 months." This figure is unsupported.

---

## SECTION IV: DEPENDENCY MAP

### IV.1 Technical Dependencies

```
[Infrastructure] ──→ [P1, P2, P2-W3, P6-W5] ──→ [All other agents]
    │
    ├─ Cloud provisioning (Month 1)
    ├─ Network configuration (Month 1–2)
    ├─ Security baseline (Month 1–3)
    └─ Monitoring setup (Month 2–4)

[Data Fabric] ──→ [P2-W3] ──→ [P2-W1, P2-W4, P2-W5, P3-W4, P5-W1, P5-W3, P5-W5]
    │
    ├─ HRIS data ingestion (Month 2–4)
    ├─ Payroll data ingestion (Month 4–6)
    ├─ Engagement data ingestion (Month 6–8)
    └─ External data sources (Month 8–12)

[Hefaistos Migration] ──→ [P4-W1, P3-W5, P2-W3] ──→ [All agents]
    │
    ├─ Schema mapping (Month 1–6)
    ├─ Data migration 15% (Month 7–12)
    ├─ Data migration 30% (Month 13–18)
    ├─ Data migration 60% (Month 19–24)
    ├─ Data migration 80% (Month 25–30)
    ├─ Data migration 100% (Month 31–36)
    └─ Cutover & decommission (Month 37–42) — TARGET: October 2029
```

### IV.2 Organizational Dependencies

| Dependency | Resolution | Timeline |
|---|---|---|
| AI Governance Board charter | CHRO + Board Chair approval | Month 1 |
| DPO appointment/confirmation | Board approval | Month 1 |
| Ethics Officer role clarity | HR Director + CHRO | Month 1 |
| Union consultation (PKB alignment) | ER Head + Union | Month 2–3 |
| IT resource allocation | CIO + CHRO | Month 1 |
| Budget approval | CFO + Board | Month 1 |
| Change management capacity | HR Director + Comms | Month 2 |
| Vendor procurement process | Procurement + Legal | Month 2–4 |

### IV.3 Regulatory Dependencies

| Dependency | Resolution | Timeline |
|---|---|---|
| UU PDP 27/2022 compliance audit | DPO + External counsel | Month 3–6 |
| GCG framework AI addendum | Ethics Officer + Legal | Month 2–4 |
| PKB AI clause negotiation | ER Head + Union | Month 3–6 |
| RPTKA compliance validation | Compliance Head | Ongoing |
| Data localization confirmation | DPO + IT | Month 2 |

---

## SECTION V: RISK REGISTER — INHERENT vs. RESIDUAL

### V.1 Risk Register (Reframed)

**Mandatory framing:** v1.0 marked all 14 risks as "(mitigated)" at Month 0. This was implausible and would not survive auditor scrutiny. v1.1 separates **Inherent Risk** (before controls) from **Residual Risk** (after controls), disclosing realistic residual levels. Two additional risks have been added (R-15 and R-16) based on audit review.

#### Legend
- **Inherent Risk (I):** Risk level if no controls were applied
- **Residual Risk (R):** Realistic risk level after planned controls
- Scale: L (Low) / M (Medium) / H (High) / C (Critical)

| ID | Risk | Inherent (Prob × Impact) | Mitigation | Residual (Prob × Impact) | Owner |
|---|---|---|---|---|---|
| R-1 | Hefaistos data migration complexity | **H × C** | Parallel migration; Migration Integrity Certificate; phased cutover; P6-W5 sunset gates | **M × H** | CDO |
| R-2 | Change resistance from HR team | **H × H** | Change management; training; pilot programs; "You spoke, we acted" demonstration | **M × M** | HR Director |
| R-3 | Model drift in predictive agents | **M × M** | Continuous monitoring; quarterly retraining; HITL validation; P6-W5 lifecycle governance | **L × M** | People Analytics Lead |
| R-4 | Regulatory change during deployment | **H × H** | P5-W4 Regulatory Horizon Scanner; 30-day advance filing; shadow testing | **M × H** | Compliance Head |
| R-5 | Bias in algorithmic decisions | **M × C** | P5-W2 cross-agent bias audit; intersectional analysis; explainability scoring; P2 always-on screening | **L × H** | AI Governance Board |
| R-6 | Data quality issues in legacy systems | **H × M** | P2-W3 5 C's validation; data cleansing; feature store quality gates; P6-W5 stress testing | **M × M** | Data Engineer |
| R-7 | Integration failure between agents | **H × H** | P1 orchestration; P2 screening; P6-W5 monthly stress testing; 99.5% pass gate | **M × M** | Solution Architect |
| R-8 | Board/CEO adoption of dashboard | **M × M** | Executive training; Decision Card demonstration; predictive governance alerts; quarterly briefings | **L × M** | CHRO |
| R-9 | WBS reporter trust in AI handling | **M × H** | P3 absolute segregation; P5-W2 WBS AI Concern channel; non-retaliation guarantee; Ethics Officer visibility | **L × H** | Ethics Officer |
| R-10 | Vendor/technology dependency & concentration | **H × H** | P6-W5 vendor governance; multi-cloud strategy; open standards; concentration risk < 30% | **M × M** | CDO |
| R-11 | Key personnel departure during deployment | **M × H** | Knowledge documentation; cross-training; vendor support contracts; P6-W4 alumni knowledge retention | **M × M** | HR Director |
| R-12 | Budget overrun | **H × H** | Phased investment; 2% risk reserve; monthly budget tracking; scope prioritization | **M × M** | CFO |
| R-13 | Cybersecurity breach | **M × C** | Security Engineer; ISO 27001; encryption; access control; incident response plan; P6-W5 DR | **L × C** | Security Engineer |
| R-14 | Union opposition to AI in HR processes | **H × H** | Union consultation; PKB alignment; transparency; HITL emphasis; job security guarantees | **M × M** | ER Head |
| **R-15** (NEW) | **Silent model accuracy degradation below tolerance** | **H × H** | ML Operations framework; model SLA monitoring; quarterly recalibration; kill-switch authority defined | **M × M** | CDO + DPO |
| **R-16** (NEW) | **Cloud provider concentration / single-region failure** | **M × C** | Multi-region architecture; quarterly DR drills; alternate provider contracts for Tier 1 | **L × H** | CDO + Security |

**Key residual risk disclosure:** **Six risks remain at Medium-High (M×H) or higher residual level even after planned controls.** These cannot be eliminated by Month 0 documentation; they require active management throughout the 42-month program. This is the realistic risk profile of an enterprise-scale AI deployment.

### V.2 Risk Mitigation Framework (Updated)

```
RESIDUAL RISK LEVEL MATRIX (Post-Mitigation)
┌─────────────────┬─────────────────┬─────────────────┐
│   LOW IMPACT    │  MEDIUM IMPACT  │   HIGH IMPACT   │
├─────────────────┼─────────────────┼─────────────────┤
│ Low Prob:       │ Low Prob:       │ Low Prob:       │
│ Monitor         │ Monitor         │ Plan Contingency│
│                 │ (R-3, R-8)      │ (R-5, R-9, R-13,│
│                 │                 │  R-16)          │
├─────────────────┼─────────────────┼─────────────────┤
│ Medium Prob:    │ Medium Prob:    │ Medium Prob:    │
│ Monitor         │ Active Mitigation│ Active Mitigation│
│                 │ (R-2, R-6, R-7, │ (R-1, R-4)      │
│                 │  R-10, R-11,    │                 │
│                 │  R-12, R-14,    │                 │
│                 │  R-15)          │                 │
├─────────────────┼─────────────────┼─────────────────┤
│ High Prob:      │ High Prob:      │ High Prob:      │
│ Active Mitigation│ ACTIVE MGT     │ CRITICAL PATH   │
│                 │                 │                 │
└─────────────────┴─────────────────┴─────────────────┘
```

**Strict Prohibition:** No risk shall be moved to "Closed" status without explicit Steering Committee approval and documented evidence that the residual risk has been reduced to acceptable level.

---

## SECTION VI: GOVERNANCE OPERATIONALIZATION

### VI.1 HITL Operationalization

| HITL Range | Frequency | Operational Owner | System Support |
|---|---|---|---|
| HC-1 to HC-12 (Wave 1) | Event-triggered | HR Director | P1 workflow routing |
| HC-13 to HC-22 (Wave 2) | Quarterly | HR Director / CDO | P2-W3 feature store |
| HC-23 to HC-32 (Wave 3) | Event-triggered | HRBP / Manager | P3-W1, P3-W2 workflows |
| HC-33 to HC-55 (Wave 4) | Monthly / Event | Payroll / Compliance / HR Ops | P4-W1, P4-W2, P4-W5 |
| HC-56 to HC-88 (Wave 5) | Quarterly / Event | CHRO / CEO / Board | P5-W1, P5-W3, P5-W4 |
| HC-89 to HC-110 (Wave 6) | Event-triggered | TA Head / OD Lead / C&B Head / AI Gov Board | P6-W1, P6-W2, P6-W3, P6-W5 |

### VI.2 Committee Meeting Cadence

| Committee | Frequency | Chair | Members | Agenda |
|---|---|---|---|---|
| **AI Governance Board** | Monthly | CHRO | CDO, Ethics Officer, DPO, External Advisor | Bias audits, ethical standards, deployment approvals |
| **Validation Council** | Quarterly | HR Director | HAV Lead, 2 HRBPs, External Psychologist | 9-Box placements, Talent Pool decisions |
| **Calibration Council** | Semi-annually | HR Director | 3 Senior Managers, C&B Head | PA Category A/B/C finalization |
| **Skills Council** | Quarterly | CDO | L&D Head, TA Head, 2 HRBPs | Skills ontology, proficiency calibration |
| **WBS Council** | As needed | Ethics Officer | Legal, ER Head, HR Director | Reportable conduct investigation |
| **Change Council** | Per change | OD Lead | HR Director, Comms, IT, Union rep | Restructure approval, cascade planning |

### VI.3 Audit Trail Requirements

| Requirement | Implementation | Verification |
|---|---|---|
| Input/output hashing | All agent transactions | P6-W5 monitoring |
| Version control | Semantic versioning all agents | P6-W5 lifecycle |
| HITL timestamp logging | All checkpoint interactions | P1 audit log |
| Model retraining records | Quarterly model updates | P6-W5 stress tests |
| Bias audit records | Quarterly P5-W2 reports | AI Gov Board archive |
| Regulatory filing records | P5-W4 pre-generator | Compliance archive |
| Data retention compliance | UU PDP 27/2022 limits | DPO audit |

---

## SECTION VII: SUCCESS METRICS & MILESTONES

### VII.1 Phase Milestones — Reconciled Dates

| Phase | Milestone | Target Date | KPI |
|---|---|---|---|
| 1 | Foundation live | Oct 2026 | 4 agents operational |
| 2 | Core operations live | Apr 2027 | 9 agents operational; self-service pilot |
| 3 | Talent engine live | Oct 2027 | 16 agents operational; HAV + PA active |
| 4 | Intelligence live | Apr 2028 | 23 agents operational; predictive analytics |
| 5 | Enterprise scale | Oct 2028 | 28 agents operational; all pilots scaled |
| 6 | Governance live | Apr 2029 | 30 agents operational; Board Dashboard |
| 7 | **Hefaistos sunset** | **Oct 2029** | 30 agents; Hefaistos decommissioned; ISO certified |

### VII.2 Maturity Trajectory (Operational Deployment)

**Mandatory framing:** This is **Operational Maturity Trajectory**, distinct from Architecture Design Coverage (which is already 100% as of May 2026). Operational maturity is earned phase-by-phase.

| Month | Agents Live | Modules ≥ 75% Operational | Operational Maturity | Hefaistos Migration |
|---|---|---|---|---|
| 6 | 4 | 4 | 35% | 0% |
| 12 | 9 | 7 | 55% | 15% |
| 18 | 16 | 10 | 72% | 30% |
| 24 | 23 | 12 | 85% | 60% |
| 30 | 28 | 13 | 93% | 80% |
| 36 | 30 | 13 | 97% | 100% |
| 42 | 30 | 13 | **100%** | **Decommissioned** |

### VII.3 Business Outcome Targets

| Outcome | Baseline | Year 1 | Year 2 | Year 3 |
|---|---|---|---|---|
| Time-to-Fill (days) | 65 | 55 | 45 | 40 |
| Quality-of-Hire (HAV score) | 0.62 | 0.68 | 0.72 | 0.75 |
| eNPS | +12 | +20 | +30 | +40 |
| Attrition Rate | 18% | 15% | 12% | 10% |
| Pay Equity Gap | 8.5% | 5.0% | 3.0% | 1.5% |
| Compliance Gap Window | 45 days | 30 days | 15 days | 7 days |
| Self-Service Deflection | 35% | 50% | 65% | 75% |
| Recognition Coverage | 45% | 70% | 85% | 95% |
| Wellbeing Risk (avg) | 55 | 48 | 42 | 38 |
| Hefaistos Dependency | 100% | 85% | 50% | 0% |

---

## SECTION VIII: IMPLEMENTATION GOVERNANCE

### VIII.1 Steering Committee

| Role | Responsibility | Meeting Frequency |
|---|---|---|
| **CHRO (Chair)** | Strategic direction, escalation, Board liaison | Weekly (Month 1–12), Bi-weekly (Month 13+) |
| **CFO** | Budget, ROI tracking, investment approval | Monthly |
| **CDO** | Technical architecture, data, infrastructure | Weekly |
| **HR Director** | Operational delivery, HR team readiness | Weekly |
| **DPO** | Privacy, compliance, UU PDP 27/2022 | Bi-weekly |
| **Ethics Officer** | GCG, bias, WBS, ethical standards | Monthly |
| **External Advisor** | Independent review, best practice, audit | Quarterly |

### VIII.2 Escalation Matrix

| Level | Trigger | Escalation Path | Response Time |
|---|---|---|---|
| 1 | Agent health < 70 for 15 min | Auto-alert → DevOps → Solution Architect | 30 minutes |
| 2 | Integration test failure | QA → Solution Architect → CDO | 4 hours |
| 3 | Budget variance > 10% | PM → CFO → CHRO | 24 hours |
| 4 | Regulatory alert (Red) | Compliance Head → CHRO → CEO | 2 hours |
| 5 | Security incident | Security Engineer → CDO → CHRO → CEO | 15 minutes |
| 6 | Hefaistos migration blocker | CDO → CHRO → CEO → Board | 4 hours |
| 7 | WBS breach / ethics violation | Ethics Officer → CHRO → Board Chair | 1 hour |

### VIII.3 Change Control

| Change Type | Authority | Process | Documentation |
|---|---|---|---|
| Agent deployment | AI Governance Board | 4-phase deployment (P6-W5) | Deployment record |
| Agent version update | AI Governance Board | Stress test → pilot → production | Version log |
| HITL checkpoint change | CHRO | Committee review → approval | Governance update |
| Data source addition | CDO | Schema review → 5 C's validation → integration test | Data catalog |
| Vendor change | CDO + Procurement | Risk assessment → DPA → P6-W5 integration | Vendor registry |
| Hefaistos milestone change | CEO + Board | Sunset gate review → approval | Gate record |

---

## SECTION IX: APPENDICES

### Appendix A: Agent Deployment Sequence

| Order | Agent | Phase | Week | Dependencies |
|---|---|---|---|---|
| 1 | P1 | 1 | 1–2 | Infrastructure |
| 2 | P2 | 1 | 2–3 | P1 |
| 3 | P2-W3 | 1 | 4–6 | P1, P2, Infrastructure |
| 4 | P6-W5 | 1 | 6–8 | P1, P2, P2-W3 |
| 5 | P4-W1 | 2 | 1–4 | P1, P2, P2-W3 |
| 6 | P4-W2 | 2 | 3–6 | P1, P2, P2-W3 |
| 7 | P4-W5 | 2 | 5–10 | P1, P2, P2-W3, P4-W2 |
| 8 | P3 | 2 | 7–10 | P1, P2 |
| 9 | P6-W3 | 2 | 9–12 | P1, P2, P2-W3, P4-W1 |
| 10 | P4 | 3 | 1–4 | P1, P2, P2-W3 |
| 11 | P5 | 3 | 3–6 | P1, P2, P4 |
| 12 | P3-W1 | 3 | 5–8 | P1, P2, P2-W3 |
| 13 | P3-W2 | 3 | 7–10 | P1, P2, P3-W1 |
| 14 | P3-W3 | 3 | 9–12 | P1, P2, P4-W2 |
| 15 | P6-W2 | 3 | 11–14 | P1, P2, P3-W2, P5 |
| 16 | P6-W1 | 3 | 13–16 | P1, P2, P2-W2, P4-W4 |
| 17 | P2-W1 | 4 | 1–4 | P1, P2, P2-W3 |
| 18 | P2-W2 | 4 | 3–6 | P1, P2, P2-W3 |
| 19 | P2-W4 | 4 | 5–8 | P1, P2, P2-W3, P2-W5 |
| 20 | P2-W5 | 4 | 7–10 | P1, P2, P2-W3 |
| 21 | P3-W4 | 4 | 9–12 | P1, P2, P2-W3, P4-W1 |
| 22 | P3-W5 | 4 | 11–14 | P1, P2, P2-W3, P4 |
| 23 | P6-W4 | 4 | 13–16 | P1, P2, P3-W3, P2-W4 |
| 24 | P4-W3 | 5 | 1–4 | P1, P2, P2-W2, P2-W3 |
| 25 | P4-W4 | 5 | 3–6 | P1, P2, P2-W3, P3-W5 |
| 26 | P5-W5 | 5 | 5–8 | P1, P2, P2-W3, P2-W5 |
| 27 | P5-W1 | 5 | 7–10 | P1, P2, P2-W1, P2-W3 |
| 28 | P5-W4 | 5 | 9–12 | P1, P2, P4-W2, P2-W3 |
| 29 | P5-W2 | 6 | 1–6 | P1, P2, All Tier 2 agents |
| 30 | P5-W3 | 6 | 4–8 | P1, P2, All Tier 2 agents, P5-W2 |

### Appendix B: Hefaistos Decommission Detailed Plan — Aligned to October 2029

| Month | Milestone | P6-W5 Gate | Deliverable |
|---|---|---|---|
| 1–6 | Schema mapping complete | Gate 0 | Migration plan approved |
| 7–12 | 15% data migrated | Gate 1 | Migration Integrity Certificate #1 |
| 13–18 | 30% data migrated | Gate 2 | Migration Integrity Certificate #2 |
| 19–24 | 60% data migrated | Gate 3 | Migration Integrity Certificate #3 |
| 25–30 | 80% data migrated | Gate 4 | Migration Integrity Certificate #4 |
| 31–36 | 100% data migrated | Gate 5 | Migration Integrity Certificate #5 |
| 37–39 | Parallel operation validation | Gate 6 | 99.9% consistency report |
| 40–41 | Read-only transition | Gate 7 | Hefaistos read-only confirmed |
| **42 (Oct 2029)** | **Full shutdown** | **Gate 8** | **Hefaistos decommission certificate** |
| 42–45 (post-Oct 2029) | Rollback window maintained | Gate 9 | 90-day rollback capability confirmed |
| 45 (Jan 2030) | Final certification | Gate 10 | ISO 27001/22301 certification |

**Mandatory clarification:** v1.0 Appendix B carried inconsistent milestone month numbers. v1.1 anchors all milestones to the May 2026 start date, with Hefaistos full shutdown at **Month 42 (October 2029)**. The 90-day rollback window and final certification extend into **Q1 2030**.

### Appendix C: Training & Change Management Plan

| Audience | Training Content | Delivery | Timing |
|---|---|---|---|
| All Employees | Self-service portal, wellbeing apps | E-learning + Helpdesk | Month 8–12 |
| Managers | HAV, Calibration, 360°, Goal-setting | Workshop + Coaching | Month 13–18 |
| HRBPs | All agent workflows, HITL checkpoints | Certification program | Month 7–24 |
| HR Ops | Payroll reconciliation, compliance, helpdesk | Technical training | Month 7–12 |
| TA Team | AI sourcing, EVP intelligence, boomerang pipeline | Workshop + System training | Month 16–20 |
| C&B Team | Pay equity, benefits optimization, total rewards | Technical training | Month 25–30 |
| Board HR Committee | Dashboard navigation, Decision Cards, risk register | Executive briefing | Month 31–33 |
| AI Governance Board | Bias audit, ethical standards, deployment governance | Certification | Month 1–3 |

### Appendix D: Pre-Phase 1 Mandatory Actions (NEW)

Before Phase 1 deployment begins, the following must be completed:

| # | Action | Owner | Deadline |
|---|---|---|---|
| 1 | Board HR Committee approval of v1.1 Roadmap and v2.1 Architecture Certification | CHRO | Prior to Phase 1 kickoff |
| 2 | External independent validation audit of 30-agent architecture | CHRO + CFO | Prior to Phase 1 kickoff |
| 3 | Legal Counsel verification of every regulatory citation | Legal + DPO | Prior to Phase 1 kickoff |
| 4 | Union (PKB) consultation initiation — present architecture, request impact assessment | ER Head | Month 1–2 of Phase 1 |
| 5 | DPO formal sign-off on UU PDP 27/2022 compliance design for all 30 agents | DPO | Prior to Phase 1 kickoff |
| 6 | AI Governance Board charter ratification by Board HR Committee | CHRO + Board Chair | Month 1 of Phase 1 |
| 7 | ML Operations framework drafted (model SLA, kill-switch authority, explanation protocol per UU PDP 27/2022) | CDO + DPO | Prior to Phase 1 kickoff |
| 8 | PKB Impact Matrix completed (30 agents × PKB clauses × engagement type) | ER Head | Month 2 of Phase 1 |

---

## DOCUMENT CONTROL STATEMENT

> **This document (Option I v1.1) defines the 42-month phased deployment plan for the Polytron Enterprise HR Agentic AI Architecture, targeting full Hefaistos decommission by October 2029. The plan is supported by reconciled financial figures (IDR 42.5B investment, 131% 5-year ROI, ~Month 38–42 payback), an architecture that is Design-Complete as of May 2026, and a governance framework comprising 110 HITL checkpoints, 180 mandatory rules, 180 strict prohibitions, and 180 quality items.**
>
> **Strict Prohibition:** This document shall not be modified, redistributed in altered form, or cited with figures other than those documented herein. v1.0 figures (340% ROI, 26-month payback, 30-month duration, October 2028 sunset, 28 FTE peak) are formally retracted.
>
> **Mandatory:** Phase advancement requires Go/No-Go Gate approval by the designated authority. No phase shall begin until the prior phase Gate has been formally passed and minuted.
>
> **Architecture Status:** Design-Complete
> **Deployment Status:** Awaiting Phase 1 Pre-Authorization (Appendix D actions)
> **Hefaistos Decommission Target:** October 2029
> **Next Action:** Board HR Committee approval; commission external validation audit; complete Appendix D pre-Phase 1 actions

---

## DOCUMENT METADATA

| Attribute | Value |
|---|---|
| **Document ID** | POLYTRON-HR-AI-IMPL-ROADMAP-2026-v1.1 |
| **Document Type** | Implementation Roadmap |
| **Classification** | INTERNAL — Board HR Committee & Top Management |
| **Date** | May 2026 |
| **Owner** | CHRO Office |
| **Previous Version** | Option I v1.0 (May 2026) — superseded due to 9 audit findings |
| **Current Version** | Option I v1.1 (audit-reconciled) |
| **Architecture Baseline** | Waves 1–6 Design-Complete | 30 Agents | ~22,680 Lines |
| **Deployment Window** | 42 months (May 2026 – October 2029) |
| **Hefaistos Decommission** | October 2029 (Phase 7 completion) |
| **Total Investment** | IDR 42.5B (verified) |
| **5-Year Gross Benefits** | IDR 98.0B (verified, sum of 10 categories) |
| **5-Year Net Benefit** | IDR 55.5B |
| **5-Year ROI** | 131% (re-derived, audited) |
| **Payback Period** | ~Month 38–42 (cash-flow-modelled) |
| **Peak Team Size** | 21 FTEs (Phase 5) |
| **Go/No-Go Gates** | 7 (one per phase) |
| **Risk Items** | 16 (14 original + R-15 model drift + R-16 cloud concentration) — disclosed at Inherent and Residual levels |
| **HITL / Mandatory / Strict Prohibition / Quality Items** | 110 / 180 / 180 / 180 (defined in companion v2.1 Certification) |
| **Companion Document** | POLYTRON_HR_AI_WAVES_1-6_FINAL_CONSOLIDATION_v2_1.md |
| **Distribution List** | Board HR Committee; CEO; CHRO; CFO; CDO; HR Director; DPO; Ethics Officer; ER Head |
| **Next Review** | November 2026 (post Phase 1 Gate 1) |
| **Next Action** | Board HR Committee approval → complete Appendix D pre-Phase 1 actions → Phase 1 initiation |
| **Supersedes** | Option I v1.0 (May 2026) |

---

*End of Waves 1–6 Implementation Roadmap v1.1*

---

**Document Version:** Option I v1.1
**Classification:** INTERNAL — Board HR Committee & Top Management
**Owner:** CHRO Office, Polytron HR
**Next Review:** November 2026 (post Phase 1 Gate 1)
**Distribution:** Per Board HR Committee recipient matrix
