---
title: "POLYTRON ENTERPRISE HR AGENTIC AI ARCHITECTURE"
subtitle: "Wave 6 — Completion & Integration Design Specification"
version: "v1.1"
classification: "INTERNAL — Board HR Committee & Top Management"
date: "May 2026"
prepared_for: "LM — Polytron HR, Enterprise HR AI Architect"
status: "DESIGN-COMPLETE | Completes 30-Agent Architecture Specification Coverage"
total_agents_post_wave6: 30
specification_coverage_post_wave6: "100% (30/30 agents specified)"
operational_status: "TO BE EARNED THROUGH PHASED DEPLOYMENT (May 2026 – October 2029)"
document_owner: "CHRO Office"
next_review: "November 2026 (post Phase 1 Gate 1)"
supersedes: "v1.0 (May 2026)"
companion_documents:
  - "POLYTRON_HR_AI_WAVES_1-6_FINAL_CONSOLIDATION_v2_1.md"
  - "POLYTRON_HR_AI_IMPLEMENTATION_ROADMAP_v1_1.md"
---

# POLYTRON ENTERPRISE HR AGENTIC AI ARCHITECTURE
## Wave 6 — Completion & Integration (Design Specification)
### v1.1 — Audit-Reconciled Edition

**Document Classification:** INTERNAL
**Date:** May 2026
**Prepared For:** LM — Polytron HR, Enterprise HR AI Architect
**Wave 5 Baseline:** 25 Agents Specified | ~85% Specification Coverage (weighted)
**Wave 6 Target:** 30 Agents Specified | **100% Specification Coverage** | Design-Complete

---

## DOCUMENT REVISION NOTICE

**Important:** v1.1 supersedes v1.0 (May 2026) and corrects framing inconsistencies identified during internal audit review prior to Board distribution. The five agent specifications (P6-W1 through P6-W5) are technically sound and have been preserved with only the changes noted below. Distribution of v1.0 should be discontinued.

| Issue Corrected | v1.0 Statement | v1.1 Resolution |
|---|---|---|
| **Maturity Framing** | "Targets 100% System Maturity" / "300/300 Audit Target" | "Completes 100% Specification Coverage (30/30 agents)" — operational maturity reframed as to-be-earned through deployment |
| **Hefaistos Date** | "October 2028" target | **October 2029** target (aligned to 42-month phased plan in v1.1 Roadmap) |
| **Maturity Percentages** | "Post-W6: 100%" presented without context | Mandatory note added: "%" measures specification scope coverage, not operational/code maturity |
| **P2 Screening Prohibitions** | Identical boilerplate "MUST NEVER operate without P2 Ethical Guardrail screening" across all 5 agents | De-templatized: each agent now has agent-specific phrasing reflecting its unique risk surface |
| **P6-W4 Section Depth** | Compressed relative to peer agents | Expanded to match P6-W1/P6-W2/P6-W3 depth |
| **Closing Banner** | ALL-CAPS slogan banner | Standard Document Control Statement with version, classification, owner, next review |
| **"100% Certification" Section** | "POST-WAVE 6 SYSTEM MATURITY — 100% CERTIFICATION" | "POST-WAVE 6 DESIGN COMPLETION SUMMARY" |
| **Companion Document References** | None | Cross-references to v2.1 Consolidation and v1.1 Roadmap added |

---

## WAVE 6 STRATEGIC CONTEXT

### Why Wave 6 Was Required

At the end of Wave 5, the Polytron HR Agentic AI Architecture had specification coverage of approximately 85% (weighted across modules). Seven modules remained below 95% specification coverage, with three critical modules significantly under-covered:
- M05 Performance Management: 75% specification coverage
- M07 Organization Development: 78% specification coverage
- M11 Offboarding & Alumni: 70% specification coverage

Tier 1 Orchestration was at 75% specification coverage, lacking specifications for agent lifecycle governance, cross-agent stress testing, disaster recovery orchestration, and Hefaistos decommission execution logic.

**Wave 6 closes every remaining specification gap.** It is the **completion layer** that brings architecture specification coverage from ~85% to 100% across all 13 functional modules plus Tier 1 Orchestration.

**Mandatory framing:** Specification completeness is a documentation milestone, not an operational milestone. Even at 100% specification coverage, no agent has yet been deployed. Operational maturity will be earned through the 42-month phased deployment plan in the companion v1.1 Roadmap, with Hefaistos decommission targeted for **October 2029**.

### Wave 6 Design Principles

1. **Mandatory — Gap-Targeted:** Each agent is explicitly mapped to specification gaps ≥4pp
2. **Mandatory — Cross-Module:** Single agents close multiple module gaps simultaneously
3. **Mandatory — Resilience-First:** Tier 1 completion (P6-W5) is the operational backbone, designed but not yet operationalized
4. **Mandatory — Hefaistos-Aligned:** Every agent includes sunset execution logic for October 2029 target
5. **Mandatory — Audit-Compliant:** All 5 agents follow the 10-section canonical standard

---

## WAVE 6 AGENT OVERVIEW

| # | Agent Code | Agent Name | Closes Module(s) | Pre-W6 Coverage | Post-W6 Coverage | Lines | Status |
|---|---|---|---|---|---|---|---|
| 1 | **P6-W1** | Talent Acquisition & Employer Branding Intelligence Agent | M02, M06 | 88%, 85% | **100%, 100%** | ~480 | Design-Complete |
| 2 | **P6-W2** | 360° Performance & OD Intelligence Agent | M05, M07 | 75%, 78% | **100%, 100%** | ~520 | Design-Complete |
| 3 | **P6-W3** | Total Rewards & Wellbeing Optimization Agent | M08, M03 | 80%, 96% | **100%, 100%** | ~460 | Design-Complete |
| 4 | **P6-W4** | Alumni Network & Strategic Offboarding Orchestrator | M11, M12 | 70%, 91% | **100%, 100%** | ~440 | Design-Complete |
| 5 | **P6-W5** | Cross-Agent Integration Resilience & Lifecycle Manager | Tier 1, ALL | 75%, 93% | **100%, 100%** | ~580 | Design-Complete |
| | | **TOTAL** | | | | **~2,480** | |

### Post-Wave 6 Specification Coverage Dashboard

**Mandatory note:** The "%" figures below measure *specification scope coverage* — whether the agents needed to address documented gaps in that module have been designed. They do NOT measure code completeness, test pass rates, deployment status, or business outcome achievement. Each of those is measured separately during the Deployment Timeline (Implementation Roadmap v1.1).

| Module | Post-W5 Coverage | Post-W6 Coverage | Change | Closure Agent |
|---|---|---|---|---|
| **Tier 1 — Orchestration** | 75% | **100%** | +25pp | P6-W5 |
| **M01 — Strategic Workforce Planning** | 92% | **100%** | +8pp | P6-W5 (integration) |
| **M02 — Talent Acquisition & EB** | 88% | **100%** | +12pp | P6-W1 |
| **M03 — Onboarding & EX** | 96% | **100%** | +4pp | P6-W3 (wellbeing) |
| **M04 — Learning & Development** | 92% | **100%** | +8pp | P6-W2 (performance linkage) |
| **M05 — Performance Management** | 75% | **100%** | +25pp | P6-W2 |
| **M06 — Succession Management** | 85% | **100%** | +15pp | P6-W1 (pipeline) |
| **M07 — Organization Development** | 78% | **100%** | +22pp | P6-W2 |
| **M08 — Compensation & Benefits** | 80% | **100%** | +20pp | P6-W3 |
| **M09 — HR Operations & Payroll** | 92% | **100%** | +8pp | P6-W5 (vendor governance) |
| **M10 — Compliance, GCG & ER** | 94% | **100%** | +6pp | P6-W5 (vendor risk) |
| **M11 — Offboarding & Alumni** | 70% | **100%** | +30pp | P6-W4 |
| **M12 — People Analytics** | 91% | **100%** | +9pp | P6-W4 (knowledge graph) |
| **TOTAL Specification Coverage** | **~85% (weighted)** | **100%** | | |

---

# ============================================================
# P6-W1: TALENT ACQUISITION & EMPLOYER BRANDING INTELLIGENCE AGENT
# ============================================================

---
name: "Talent_Acquisition_Employer_Branding_Intelligence_Agent"
description: "End-to-end AI-powered talent acquisition orchestrator covering sourcing, screening, interview scheduling, EVP sentiment tracking, talent pipeline health scoring, and succession pipeline auto-nurture. Closes M02 (88%→100%) and M06 (85%→100%) specification gaps."
trigger_conditions:
  - "New requisition approved by TA Head"
  - "Pipeline health score < 70 for critical role"
  - "EVP sentiment drop detected by P2-W5"
  - "Quarterly talent pool refresh cycle"
  - "Boomerang hire opportunity from P6-W4 alumni graph"
  - "Internal mobility gap > 30 days (P4-W4 fallback to external)"
activation_mode: "AUTO + HITL"
---

## Section I: Conceptual Foundation (WHY)

### I.1 Strategic Gap Being Closed

**M02 — Talent Acquisition & Employer Branding** had 88% specification coverage. While Waves 2–5 provided demand forecasting (P2-W1), skills taxonomy (P2-W2), and internal mobility (P4-W4), there was **no dedicated specification** for external talent acquisition execution. Sourcing, screening, interview orchestration, EVP measurement, and employer brand intelligence remained unspecified or semi-specified.

**M06 — Succession Management** had 85% specification coverage. While P4 (HAV Assessment) validates internal talent, there was **no specification for automated pipeline nurturing** for external succession candidates or critical role backfill intelligence when internal pools are insufficient.

### I.2 Strategic Value (Design Intent)

- **Time-to-Fill Reduction:** Design target — AI sourcing reduces sourcing time by 60% (to be validated in Phase 3 pilot)
- **Quality-of-Hire Improvement:** Design target — Predictive screening correlates with HAV Phase 1 outcomes (validation Phase 3+)
- **EVP Protection:** Design target — Real-time employer brand sentiment monitoring (operationalization Phase 3)
- **Succession Depth:** Design target — External pipeline auto-nurture ensures zero critical role vacancy risk
- **Cost-per-Hire Optimization:** Design target — Internal-first enforcement + external intelligence = optimal sourcing mix

### I.3 Regulatory Anchors

**Mandatory note:** All regulatory citations below are pending verification by Legal Counsel prior to Phase 1 kickoff (per Implementation Roadmap v1.1, Appendix D, Item 3).

- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Non-discriminatory hiring; local workforce preference (RPTKA compliance)
- **UU PDP 27/2022:** Candidate data protection, consent management, DSAR handling
- **PP 35/2021:** Wage transparency in job postings (provision subject to Legal verification)
- **PKB:** Collective agreement provisions on hiring priorities

---

## Section II: Structural Breakdown (WHAT)

### II.1 Core Components

#### C1: AI Sourcing Engine
- **Source Aggregation:** Job boards (JobStreet, LinkedIn, Kalibrr), talent communities, employee referrals, alumni boomerang pipeline (P6-W4), campus recruiting
- **Boolean + NLP Search:** Auto-generates optimized search strings from job requisition + P3-W5 job architecture
- **Diversity Sourcing:** Ensures candidate slate diversity per GCG.02; tracks demographic pipeline ratios
- **Passive Candidate Mining:** Identifies and engages passive talent via skills ontology (P2-W2) matching

#### C2: Predictive Screening Engine
- **Resume Parsing + Skills Extraction:** Maps to P2-W2 Skills Ontology (Proficiency Scale)
- **HAV Phase 1 Pre-Qualification:** Predicts likelihood of Competency Matrix success
- **Bias-Resistant Scoring:** P5-W2 cross-agent audit integration; DPR/EOR monitoring on screening outcomes
- **Candidate Ranking:** Multi-factor score (skills match × culture fit × growth potential × availability)

#### C3: Interview Orchestration
- **Auto-Scheduling:** Integrates with calendar systems; respects interviewer availability and load balancing
- **Structured Interview Kit Generation:** Auto-generates questions from job architecture (P3-W5) + HAV competencies
- **Interview Feedback Collection:** Structured scoring with Calibration Council-ready format
- **Panel Diversity Enforcer:** Ensures interview panel meets diversity criteria per GCG

#### C4: EVP & Employer Brand Intelligence
- **Sentiment Monitoring:** Tracks employer brand sentiment across Glassdoor, LinkedIn, social media, campus forums
- **EVP Health Score:** 0–100 composite of sentiment, application rate, offer acceptance rate, early turnover
- **Competitive Positioning:** Benchmarks Polytron EVP against industry peers using P3-W4 compensation data
- **Narrative Generation:** Auto-generates "Why Polytron" content for job postings and career pages

#### C5: Talent Pipeline Health Monitor
- **Pipeline Funnel Metrics:** Source → Applied → Screened → Interviewed → Offered → Hired → 90-Day Retention
- **Health Score:** 0–100 per requisition; alerts when < 70
- **Auto-Nurture Campaigns:** Drip engagement for silver/bronze candidates; re-engagement for past finalists
- **Critical Role Backfill Intelligence:** Flags when internal succession pool (P4) + external pipeline < 2× coverage

#### C6: Succession Pipeline Integration
- **External Succession Pool:** Maintains external candidate pipeline for C-suite and critical roles
- **Internal-First Gate Enforcement:** P4-W4 72-hour window; auto-escalates to external if no internal match
- **Boomerang Hire Trigger:** P6-W4 alumni graph integration; auto-identifies rehire-eligible alumni
- **Talent Pool Cross-Reference:** Ensures external candidates do not duplicate internal Talent Pool profiles

### II.2 Workflow Architecture

```
[Requisition Approved]
    ↓
[C1: AI Sourcing Engine] → Source aggregation + diversity enforcement
    ↓
[C2: Predictive Screening] → Skills extraction + HAV pre-qualification + bias audit
    ↓
[HC-89: TA Head Approval] → Top-ranked candidate slate validation
    ↓
[C3: Interview Orchestration] → Scheduling + structured kit + panel diversity
    ↓
[Interview Completion]
    ↓
[C4: EVP Intelligence] → Brand sentiment tracking + narrative optimization
    ↓
[C5: Pipeline Health] → Funnel metrics + auto-nurture + critical role backfill
    ↓
[HC-90: HR Director Approval] → Offer authorization for Director+ roles
    ↓
[C6: Succession Integration] → External pool update + internal-first validation
    ↓
[Onboarding Handoff → P3-W1]
```

---

## Section III: Operational Guidance (HOW)

### III.1 Trigger Conditions

1. **New Requisition:** Auto-activates when requisition approved in ATS
2. **Pipeline Alert:** Auto-activates when pipeline health < 70 for active requisition
3. **EVP Drop:** Auto-activates when EVP Health Score drops > 10 points in 30 days
4. **Quarterly Refresh:** Auto-activates talent pool refresh on first Monday of quarter
5. **Boomerang Signal:** Auto-activates when P6-W4 alumni graph flags rehire opportunity
6. **Internal Mobility Timeout:** Auto-activates external sourcing when P4-W4 72-hour gate expires without match

### III.2 Input Requirements

- Job requisition (title, level, family, skills, location, salary band)
- P3-W5 Job Architecture reference (role definition, competencies)
- P2-W2 Skills Ontology (required skills + proficiency levels)
- P3-W4 compensation band (from Compa-Ratio data)
- P4 HAV Talent Pool (internal candidates for cross-reference)
- P2-W5 engagement sentiment (for EVP correlation)

### III.3 Processing Logic

**Step 1 — Sourcing:**
- Generate Boolean search strings from requisition + skills ontology
- Query 8+ sources simultaneously
- Apply diversity sourcing rules (minimum 30% underrepresented gender for management roles)
- Enforce RPTKA compliance: prioritize local candidates for non-specialist roles

**Step 2 — Screening:**
- Parse resumes; extract skills; map to ontology
- Calculate HAV Phase 1 predicted score (correlation with historical HAV data)
- Run P5-W2 bias audit on screening outcomes (DPR/EOR check)
- Rank candidates; generate top-10 slate

**Step 3 — HITL Validation (HC-89):**
- TA Head reviews top-10 slate
- Can override rankings with documented justification
- Must confirm diversity slate compliance

**Step 4 — Interview Orchestration:**
- Auto-schedule 3-round interview panel
- Generate structured interview kit from job architecture competencies
- Ensure panel diversity (minimum 1 underrepresented gender, 1 cross-functional member)

**Step 5 — Offer & Pipeline:**
- Track funnel metrics in real-time
- Auto-nurture silver candidates for future roles
- Update critical role backfill coverage metric

**Step 6 — HITL Authorization (HC-90):**
- HR Director approval required for Director-level+ offers
- C&B Head validation for offer within band (P3-W4 integration)

### III.4 Output Deliverables

- **Candidate Slate Report:** Top 10 ranked candidates with scores, bias audit clearance, diversity metrics
- **Interview Schedule:** Calendar invites, interview kit, panel assignments
- **EVP Health Dashboard:** Sentiment trends, competitive positioning, narrative recommendations
- **Pipeline Health Scorecard:** Funnel metrics, bottleneck identification, nurture campaign status
- **Critical Role Backfill Alert:** Coverage ratio, risk level, recommended actions
- **Hiring Analytics:** Time-to-fill, source effectiveness, quality-of-hire prediction, cost-per-hire

---

## Section IV: Structured Output Templates

### Template 1: Candidate Slate Report

```yaml
slate_id: "SLATE-2026-{nnnn}"
requisition_id: "REQ-{nnnn}"
role: "[Role Title]"
job_family: "[Family from P3-W5]"
generated_at: "YYYY-MM-DD HH:MM"
bias_audit_status: "CLEARED / FLAGGED"
diversity_compliance: "PASS / FAIL"
candidates:
  - rank: 1
    candidate_id: "ANON-{hash}"
    skills_match_score: 0.0–1.0
    hav_prequal_score: 0.0–1.0
    culture_fit_score: 0.0–1.0
    overall_score: 0.0–1.0
    source: "[source]"
    diversity_flag: "[underrepresented group if applicable]"
    bias_audit: "PASS"
  - rank: 2...
slate_summary:
  total_sourced: N
  diversity_ratio: "X%"
  local_candidate_ratio: "X%"
  predicted_quality_of_hire: 0.0–1.0
```

### Template 2: EVP Health Scorecard

```yaml
evp_health_score: 0–100
score_components:
  glassdoor_rating: 0.0–5.0
  linkedin_sentiment: 0.0–1.0
  application_rate: "N applications per posting"
  offer_acceptance_rate: "X%"
  early_turnover_rate: "X%"
trend: "IMPROVING / STABLE / DECLINING"
peer_benchmark: "ABOVE / AT / BELOW market"
recommended_actions:
  - action: "[narrative]"
    owner: "[TA Head / Comms]"
    deadline: "YYYY-MM-DD"
```

---

## Section V: Reference Bank (Polytron-Specific Anchors)

### V.1 Polytron Context

- **Employer of Choice 2030:** EVP Health Score must trend > 80 by Q4 2026
- **HAV Integration:** All external hires for Band 7+ must have HAV Phase 1 predicted score ≥ 0.65
- **Internal-First Gate:** P4-W4 72-hour window is mandatory; external sourcing only after gate expiry
- **Diversity Commitment:** GCG.02 requires minimum 30% women in management; P6-W1 enforces slate diversity
- **RPTKA Compliance:** Foreign worker utilization plan must be validated before non-local offer

### V.2 Indonesian Regulatory Anchors

- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Non-discriminatory hiring; local worker priority
- **UU PDP 27/2022:** Candidate consent for data processing; 30-day DSAR response; data retention limits
- **PP 35/2021:** Wage transparency; minimum wage compliance in job postings (provision subject to Legal verification)
- **PKB:** Hiring freeze provisions; union notification for mass hiring

---

## Section VI: Quality Checklist

| ID | Check | Verification |
|---|---|---|
| Q-101 | YAML frontmatter with explicit triggers | Schema validation |
| Q-102 | 10-section structure (I–X) | Section count |
| Q-103 | Mandatory rules (M-106 to M-115) documented | Rule inventory |
| Q-104 | Strict Prohibitions (SP-106 to SP-115) documented | Prohibition inventory |
| Q-105 | Bilingual output (ID + EN) for candidate communications | Language tag |
| Q-106 | Polytron 2030 target and GCG references | Reference count |
| Q-107 | Integration with P2-W2, P3-W5, P4, P4-W4, P5-W2, P6-W4 | Dependency map |
| Q-108 | HITL checkpoints (HC-89, HC-90) defined | Checkpoint count |
| Q-109 | Audit trail with candidate anonymization | Log verification |
| Q-110 | Cross-wave consistency maintained | Pattern matching |
| Q-111 | Diversity slate enforcement (30% minimum) | Metric validation |
| Q-112 | P5-W2 bias audit integration on screening | Audit linkage |
| Q-113 | RPTKA compliance check in sourcing | Compliance verification |
| Q-114 | EVP Health Score calculation validated | Score verification |
| Q-115 | Critical role backfill coverage ≥ 2× | Coverage check |

---

## Section VII: Integration Points

### VII.1 Upstream Dependencies (Invoked By)

- **P1 HR Master Orchestrator:** Routes TA workflows to P6-W1
- **P4-W4 Talent Marketplace:** Triggers P6-W1 when Internal-First Gate expires without match
- **P5-W3 Board HR Dashboard:** Consumes EVP Health Score and hiring analytics
- **P6-W4 Alumni Network:** Provides boomerang candidate signals

### VII.2 Downstream Dependencies (Invokes)

- **P2 Ethical Guardrail:** Screens all candidate communications and screening outputs
- **P2-W2 Skills Taxonomy:** Maps candidate skills to ontology
- **P3-W5 Job Architecture:** Retrieves role definitions and competencies
- **P3-W4 Compensation:** Validates offer within pay band
- **P4 HAV Assessment:** Cross-references internal Talent Pool
- **P5-W2 AI Ethics:** Bias audit on screening outcomes
- **P3-W1 Onboarding:** Handoff upon hire confirmation

### VII.3 Lateral Dependencies

- **P2-W5 Pulse & Engagement:** EVP sentiment correlation
- **P4-W2 Compliance:** RPTKA and hiring regulation validation
- **P5-W4 Regulatory Scanner:** Hiring regulation change alerts

---

## Section VIII: Governance & Enforcement

### VIII.1 Mandatory Rules (P6-W1: M-106 to M-115)

| ID | Rule |
|---|---|
| M-106 | P6-W1 MUST enforce Internal-First Gate (P4-W4) before external sourcing |
| M-107 | P6-W1 MUST maintain diversity slate minimum 30% for management roles |
| M-108 | P6-W1 MUST run P5-W2 bias audit on all screening outcomes |
| M-109 | P6-W1 MUST obtain candidate consent per UU PDP 27/2022 before data processing |
| M-110 | P6-W1 MUST validate RPTKA compliance for non-local candidate offers |
| M-111 | P6-W1 MUST calculate EVP Health Score monthly |
| M-112 | P6-W1 MUST maintain critical role backfill coverage ≥ 2× |
| M-113 | P6-W1 MUST generate bilingual (ID + EN) candidate communications |
| M-114 | P6-W1 MUST anonymize candidate data in aggregate analytics (k-anonymity) |
| M-115 | P6-W1 MUST integrate with P6-W4 alumni graph for boomerang identification |

### VIII.2 Strict Prohibitions (P6-W1: SP-106 to SP-115)

**Note:** SP-115 below has been customized (de-templatized from v1.0) to reflect P6-W1's specific risk surface — candidate screening with bias audit integration.

| ID | Prohibition |
|---|---|
| SP-106 | P6-W1 MUST NEVER bypass Internal-First Gate without TA Head documented waiver |
| SP-107 | P6-W1 MUST NEVER share candidate personal data with hiring manager before HC-89 |
| SP-108 | P6-W1 MUST NEVER discriminate based on protected characteristics in sourcing |
| SP-109 | P6-W1 MUST NEVER auto-extend offer without HC-90 (Director+) or TA Head (non-Director) approval |
| SP-110 | P6-W1 MUST NEVER retain candidate data beyond 24 months without consent renewal |
| SP-111 | P6-W1 MUST NEVER suppress negative EVP sentiment findings |
| SP-112 | P6-W1 MUST NEVER bypass P5-W2 bias audit for "urgent" hires |
| SP-113 | P6-W1 MUST NEVER share internal Talent Pool profiles with external recruiters |
| SP-114 | P6-W1 MUST NEVER make hiring decisions without human HITL validation |
| SP-115 | P6-W1 MUST NEVER process candidate screening output without P2 Ethical Guardrail's bias and fairness screen on every candidate ranking and communication |

### VIII.3 HITL Checkpoints (P6-W1: HC-89, HC-90)

| ID | Checkpoint | Authority | Trigger |
|---|---|---|---|
| HC-89 | Candidate slate validation (top-10 review, diversity compliance) | TA Head | Screening completion |
| HC-90 | Offer authorization for Director+ roles | HR Director | Interview completion + recommendation |

---

## Section IX: Success Metrics (KPIs)

| KPI | Target | Measurement |
|---|---|---|
| Time-to-Fill | ≤ 45 days (Band 5–7), ≤ 90 days (Band 8+) | ATS tracking |
| Quality-of-Hire Prediction Accuracy | ≥ 0.75 correlation with 12-month performance | HAV validation |
| EVP Health Score | ≥ 80 by Q4 2026 | Monthly composite |
| Diversity Slate Compliance | 100% of management requisitions | Audit count |
| Cost-per-Hire | ≤ industry median − 15% | Finance tracking |
| Critical Role Backfill Coverage | ≥ 2× at all times | Pipeline metric |
| Offer Acceptance Rate | ≥ 85% | ATS tracking |
| Bias Audit Pass Rate | 100% of screening batches | P5-W2 integration |
| Source Effectiveness | Top 3 sources identified quarterly | Funnel analysis |
| Boomerang Hire Rate | ≥ 10% of external hires | P6-W4 integration |

---

## Section X: Version Control

| Version | Date | Changes | Author |
|---|---|---|---|
| v1.0 | May 2026 | Initial Wave 6 design — closes M02 (88%→100%), M06 (85%→100%) | Enterprise HR AI Architecture Team |
| v1.1 | May 2026 | SP-115 de-templatized; maturity framing reframed; companion document references added | Enterprise HR AI Architecture Team |

---

# ============================================================
# P6-W2: 360° PERFORMANCE & OD INTELLIGENCE AGENT
# ============================================================

---
name: "360_Performance_OD_Intelligence_Agent"
description: "Comprehensive performance management and organization development intelligence agent covering 360° feedback synthesis, continuous calibration, performance-to-OD linkage, org design simulation, span-of-control optimization, and change impact measurement. Closes M05 (75%→100%) and M07 (78%→100%) specification gaps."
trigger_conditions:
  - "Annual 360° feedback cycle initiation"
  - "Quarterly continuous calibration trigger"
  - "Org restructuring proposal submitted"
  - "Span-of-control anomaly detected (> 12 direct reports)"
  - "Performance trajectory negative alert from P3-W2"
  - "Change Risk Score > 7.0 from P3-W5"
activation_mode: "AUTO + HITL"
---

## Section I: Conceptual Foundation (WHY)

### I.1 Strategic Gap Being Closed

**M05 — Performance Management** had 75% specification coverage — a significant gap. While P5 (PA Calibrator) and P3-W2 (Goal-Setting) covered annual calibration and OKR cascade, there were no specifications for 360° feedback synthesis, continuous calibration, or performance-to-OD linkage.

**M07 — Organization Development** had 78% specification coverage. While P3-W5 (Job Architecture) provided structural mapping, there were no specifications for org design simulation, span-of-control optimization, change impact measurement, or performance-to-structure correlation.

### I.2 Strategic Value (Design Intent)

- **Holistic Performance Visibility:** 360° feedback complements manager-only assessment with peer, subordinate, and cross-functional perspectives
- **Calibration Discipline:** Quarterly micro-calibrations prevent annual surprise; manager rating drift detected and corrected continuously
- **Restructure Risk Reduction:** Org design simulation models impact before commitment, reducing change failure rate
- **Manager Effectiveness Measurement:** Team Health Index and Manager Effectiveness Score expose structural performance drivers
- **Closed-Loop OD:** Change impact measured 30/60/90/180 days post-change; predictions validated; interventions triggered when needed

### I.3 Regulatory Anchors

- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Fair evaluation; right to respond to assessment results
- **UU PDP 27/2022:** Anonymity protection; data retention; DSAR handling for feedback data
- **PKB:** Performance evaluation frequency and procedures

---

## Section II: Structural Breakdown (WHAT)

### II.1 Core Components

#### C1: 360° Feedback Synthesis Engine
- **Anonymous Survey Distribution:** Peer, manager, subordinate, cross-functional partners; k-anonymity (k≥3) for upward/downward channels
- **Response Rate Management:** Minimum 60% for validity; auto-reminder at 50%
- **NLP Thematic Extraction:** Identifies strength themes and development areas across qualitative feedback
- **Bias Pattern Detection:** Flags halo, horns, recency, leniency, severity patterns
- **Synthesis Narrative:** Auto-generates structured feedback report with development recommendations

#### C2: Continuous Calibration Engine
- **Manager Rating Distribution Analysis:** Quarterly statistical analysis of each manager's rating distribution
- **Drift Detection:** Flags drift > 1.5 SD from calibrated norm
- **Calibration Conversation Prompt:** Auto-generates micro-calibration discussion materials
- **PA Trajectory Projection:** Forecasts annual PA Category outcomes for Calibration Council pre-read

#### C3: Org Design Simulation Engine
- **Restructure Modeling:** Ingests proposed org chart changes; models span, layers, reporting line impacts
- **3-Scenario Generation:** Conservative, moderate, aggressive options with cost, latency, communication impact
- **Span Optimization:** Identifies optimal manager-to-IC ratios per function and band
- **Cost Delta Calculation:** Projects compensation, real estate, and operational cost changes

#### C4: Change Impact Measurement
- **Baseline Capture:** 12-metric organizational health baseline before change implementation
- **Post-Change Tracking:** Metrics tracked at 30/60/90/180 days post-change
- **Impact Score:** −100 to +100 composite of organizational health delta
- **Prediction Accuracy:** Compares P3-W5 Change Risk Score prediction to actual impact
- **Intervention Trigger:** Auto-generates OD intervention recommendations when impact < −20

#### C5: Performance-OD Linkage Intelligence
- **Individual-Org Correlation:** Identifies when individual performance trends correlate with org design factors
- **Team Health Scoring:** Aggregates individual performance + engagement + 360° feedback into team health index
- **Manager Effectiveness Score:** Derived from team health, retention, engagement, and calibration drift
- **Structural Performance Driver:** Identifies org structural factors (span, layers, clarity) driving performance variance

### II.2 Workflow Architecture

```
[Trigger: Annual 360° / Quarterly Calibration / Restructure Proposal]
    ↓
[C1: 360° Feedback Synthesis] → Collection + thematic extraction + bias detection
    ↓
[HC-91: Manager Review] → Manager validates synthesis before employee delivery
    ↓
[C2: Continuous Calibration] → Drift detection + auto-prompt + trajectory projection
    ↓
[HC-92: Calibration Council Review] → Quarterly micro-calibration validation
    ↓
[C3: Org Design Simulation] → Restructure modeling + span optimization + cost projection
    ↓
[HC-93: OD Lead Approval] → Restructure simulation approval
    ↓
[C4: Change Impact Measurement] → Baseline → change → post-tracking
    ↓
[C5: Performance-OD Linkage] → Team health + manager effectiveness + structural drivers
    ↓
[Output: Integrated Performance-OD Dashboard]
```

---

## Section III: Operational Guidance (HOW)

### III.1 Trigger Conditions

1. **Annual 360° Cycle:** Auto-triggers in Week 1 of fiscal year
2. **Quarterly Calibration:** Auto-triggers first week of each quarter
3. **Restructure Proposal:** Auto-activates when P3-W5 Change Risk Score calculated
4. **Span Anomaly:** Auto-triggers when any manager's span > 12 or < 3
5. **Performance Alert:** Auto-triggers when P3-W2 trajectory model flags negative trend
6. **Change Risk Alert:** Auto-triggers when P3-W5 Change Risk Score > 7.0

### III.2 Input Requirements

- P5 PA Category history (P5 agent)
- P3-W2 goal/feedback data (performance trajectory)
- P3-W5 job architecture and org chart data
- P2-W5 engagement sentiment (team health correlation)
- P2-W4 attrition risk scores (team stability)
- P4 HAV 9-Box placements (succession correlation)

### III.3 Processing Logic

**360° Feedback:**
- Distribute anonymous surveys to peers, manager, subordinates, cross-functional partners
- Minimum response rate: 60% for validity; auto-reminder at 50%
- Extract themes via NLP; flag bias patterns
- Generate synthesis narrative; manager reviews (HC-91)
- Deliver to employee with development recommendations

**Continuous Calibration:**
- Analyze manager rating distributions quarterly
- Flag drift > 1.5 SD from calibrated norm
- Generate calibration conversation prompt
- Project PA Category trajectory for annual Calibration Council

**Org Design Simulation:**
- Ingest proposed org chart changes
- Model span, layers, reporting line impacts
- Calculate cost delta and decision latency
- Generate 3 scenario options (conservative, moderate, aggressive)
- OD Lead reviews and selects (HC-93)

**Change Impact Measurement:**
- Capture 12-metric baseline before change implementation
- Track at 30/60/90/180 days post-change
- Calculate Impact Score; compare to P3-W5 prediction
- Trigger intervention if Impact Score < −20

### III.4 Output Deliverables

- **360° Synthesis Report:** Thematic narrative, bias flags, development recommendations
- **Calibration Drift Alert:** Manager-specific drift score, conversation prompt, trajectory projection
- **Org Design Simulation:** 3 scenarios with span, cost, latency, communication impact
- **Change Impact Dashboard:** Baseline vs. actual metrics, Impact Score, intervention recommendations
- **Team Health Index:** Composite score with component breakdown
- **Manager Effectiveness Score:** Ranking with development recommendations

---

## Section IV: Structured Output Templates

### Template 1: 360° Synthesis Report

```yaml
feedback_id: "360-{employee_id}-{year}"
employee_id: "ANON-{hash}"
period: "YYYY"
response_rate: "X%"
competency_scores:
  - dimension: "Strategic Thinking"
    self: 1–5
    manager: 1–5
    peer_avg: 1–5
    subordinate_avg: 1–5
    cross_func_avg: 1–5
    variance_flag: "HIGH / NORMAL"
  - dimension: "Execution Excellence"...
themes:
  strengths:
    - "[thematic narrative]"
  development_areas:
    - "[thematic narrative]"
bias_flags:
  - type: "HALO / HORNS / RECENCY / LENIENCY / SEVERITY"
    severity: "LOW / MEDIUM / HIGH"
    recommendation: "[action]"
development_recommendations:
  - area: "[competency]"
    action: "[specific recommendation]"
    resource: "[L&D resource from P4-W3]"
```

### Template 2: Change Impact Scorecard

```yaml
change_id: "CHG-{nnnn}"
change_description: "[narrative]"
baseline_date: "YYYY-MM-DD"
post_change_dates: ["+30d", "+60d", "+90d", "+180d"]
metrics:
  - name: "Engagement Score"
    baseline: 0–100
    +30d: 0–100
    +60d: 0–100
    +90d: 0–100
    +180d: 0–100
    delta: "+/- N"
  - name: "Productivity Index"...
impact_score: −100 to +100
prediction_accuracy: "[P3-W5 predicted] vs [actual] — ACCURATE / UNDER / OVER"
intervention_triggered: "YES / NO"
intervention_recommendations:
  - action: "[narrative]"
    owner: "[role]"
    deadline: "YYYY-MM-DD"
```

---

## Section V: Reference Bank (Polytron-Specific Anchors)

### V.1 Polytron Context

- **HAV Integration:** 360° feedback feeds into HAV Competency Matrix (Phase 1); high-potential identification
- **Calibration Council:** P5 annual calibration informed by P6-W2 quarterly micro-calibrations
- **Change Management:** P3-W5 generates cascade; P6-W2 validates impact; closed-loop OD
- **Employer of Choice 2030:** Team Health Index and Manager Effectiveness Score are key culture metrics
- **GCG.01:** 360° feedback must be conducted with integrity; no retaliation for critical feedback

### V.2 Indonesian Regulatory Anchors

- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Fair evaluation; right to respond to assessment results
- **UU PDP 27/2022:** Anonymity protection; data retention; DSAR handling for feedback data
- **PKB:** Performance evaluation frequency and procedures

---

## Section VI: Quality Checklist

| ID | Check | Verification |
|---|---|---|
| Q-116 | YAML frontmatter with triggers | Schema validation |
| Q-117 | 10-section structure | Section count |
| Q-118 | Mandatory rules (M-116 to M-130) | Rule inventory |
| Q-119 | Strict Prohibitions (SP-116 to SP-130) | Prohibition inventory |
| Q-120 | Bilingual output | Language tag |
| Q-121 | Polytron and regulatory references | Reference count |
| Q-122 | Integration with P3-W2, P3-W5, P5, P2-W5, P2-W4, P4 | Dependency map |
| Q-123 | HITL checkpoints (HC-91 to HC-95) | Checkpoint count |
| Q-124 | Audit trail completeness | Log verification |
| Q-125 | Cross-wave consistency | Pattern matching |
| Q-126 | 360° anonymity protection (k≥3) | Privacy check |
| Q-127 | Calibration drift detection validated | Algorithm check |
| Q-128 | Org design simulation 3-scenario output | Output check |
| Q-129 | Change Impact Score calculation | Formula verification |
| Q-130 | Performance-OD linkage correlation | Statistical validation |

---

## Section VII: Integration Points

### VII.1 Upstream Dependencies

- **P1 HR Master Orchestrator:** Routes performance and OD workflows
- **P3-W2 Goal-Setting:** Provides performance trajectory data
- **P3-W5 Job Architecture:** Provides org chart and role structure
- **P5 Performance Calibrator:** Receives quarterly calibration inputs

### VII.2 Downstream Dependencies

- **P2 Ethical Guardrail:** Screens all feedback synthesis and calibration outputs
- **P2-W5 Pulse Listener:** Correlates team health with engagement sentiment
- **P4-W3 L&D:** Receives development recommendations for learning path generation
- **P5-W2 AI Ethics:** Audits 360° feedback for bias patterns
- **P5-W3 Board Dashboard:** Consumes team health and manager effectiveness metrics

### VII.3 Lateral Dependencies

- **P2-W4 Attrition Modeler:** Team health feeds into flight-risk scoring
- **P4 HAV Assessment:** 360° feedback informs Competency Matrix
- **P4-W2 Compliance:** Ensures evaluation procedures per PKB

---

## Section VIII: Governance & Enforcement

### VIII.1 Mandatory Rules (P6-W2: M-116 to M-130)

| ID | Rule |
|---|---|
| M-116 | P6-W2 MUST conduct 360° feedback annually for all Band 6+ employees |
| M-117 | P6-W2 MUST maintain k-anonymity (k≥3) for upward and downward feedback |
| M-118 | P6-W2 MUST generate quarterly calibration drift alerts for all managers |
| M-119 | P6-W2 MUST require HC-91 (Manager Review) before 360° delivery to employee |
| M-120 | P6-W2 MUST generate 3-scenario org design simulation for all restructuring proposals |
| M-121 | P6-W2 MUST calculate Change Impact Score at 30/60/90/180 days post-change |
| M-122 | P6-W2 MUST compare actual change impact to P3-W5 predicted Change Risk Score |
| M-123 | P6-W2 MUST calculate Team Health Index monthly for all teams ≥ 5 members |
| M-124 | P6-W2 MUST calculate Manager Effectiveness Score quarterly |
| M-125 | P6-W2 MUST integrate 360° feedback into HAV Competency Matrix (Phase 1) |
| M-126 | P6-W2 MUST generate bilingual (ID + EN) feedback reports |
| M-127 | P6-W2 MUST flag bias patterns (halo, horns, recency, leniency, severity) |
| M-128 | P6-W2 MUST trigger OD intervention when Change Impact Score < −20 |
| M-129 | P6-W2 MUST require HC-93 (OD Lead Approval) for org design simulation execution |
| M-130 | P6-W2 MUST maintain audit trail for all calibration and feedback data |

### VIII.2 Strict Prohibitions (P6-W2: SP-116 to SP-130)

**Note:** SP-125 below has been customized (de-templatized from v1.0) to reflect P6-W2's specific risk surface — feedback anonymity and calibration fairness.

| ID | Prohibition |
|---|---|
| SP-116 | P6-W2 MUST NEVER disclose individual 360° feedback source identity |
| SP-117 | P6-W2 MUST NEVER generate 360° report with response rate < 60% |
| SP-118 | P6-W2 MUST NEVER use 360° feedback as sole basis for termination decisions |
| SP-119 | P6-W2 MUST NEVER bypass HC-91 manager review before employee delivery |
| SP-120 | P6-W2 MUST NEVER suppress calibration drift findings |
| SP-121 | P6-W2 MUST NEVER recommend restructure without org design simulation |
| SP-122 | P6-W2 MUST NEVER ignore Change Impact Score < −20 |
| SP-123 | P6-W2 MUST NEVER attribute team health scores to individuals publicly |
| SP-124 | P6-W2 MUST NEVER retaliate against employees receiving critical feedback |
| SP-125 | P6-W2 MUST NEVER release 360° synthesis, calibration drift output, or Manager Effectiveness Score without P2 Ethical Guardrail's anonymity verification and bias-pattern fairness check |
| SP-126 | P6-W2 MUST NEVER store 360° raw data beyond 7 years |
| SP-127 | P6-W2 MUST NEVER share manager effectiveness scores with peers |
| SP-128 | P6-W2 MUST NEVER auto-execute org changes without HC-93 |
| SP-129 | P6-W2 MUST NEVER bypass HITL for restructuring recommendations |
| SP-130 | P6-W2 MUST NEVER ignore PKB evaluation procedure requirements |

### VIII.3 HITL Checkpoints (P6-W2: HC-91 to HC-95)

| ID | Checkpoint | Authority | Trigger |
|---|---|---|---|
| HC-91 | 360° synthesis manager review before employee delivery | Manager | Synthesis generation |
| HC-92 | Quarterly micro-calibration validation | Calibration Council | Quarterly drift analysis |
| HC-93 | Org design simulation approval | OD Lead | Restructure proposal |
| HC-94 | Change intervention authorization | HR Director | Impact Score < −20 |
| HC-95 | Annual 360° cycle scope approval | HR Director | Fiscal year start |

---

## Section IX: Success Metrics (KPIs)

| KPI | Target | Measurement |
|---|---|---|
| 360° Completion Rate | ≥ 90% of eligible employees | Annual tracking |
| 360° Response Rate | ≥ 70% per employee | Per-feedback tracking |
| Calibration Drift Detection Accuracy | ≥ 0.80 correlation with annual Calibration Council adjustments | Validation |
| Org Design Simulation Adoption | 100% of restructuring proposals | Proposal tracking |
| Change Impact Prediction Accuracy | ≥ 0.75 (predicted vs. actual) | Post-change validation |
| Team Health Index Average | ≥ 75 across all teams | Monthly tracking |
| Manager Effectiveness Score Distribution | Normal distribution (no > 20% at extremes) | Quarterly tracking |
| Bias Flag Resolution Rate | 100% of HIGH severity flags addressed | Audit tracking |
| Performance-OD Correlation Strength | r ≥ 0.60 | Statistical analysis |
| Employee Development Recommendation Uptake | ≥ 70% | L&D integration |

---

## Section X: Version Control

| Version | Date | Changes | Author |
|---|---|---|---|
| v1.0 | May 2026 | Initial Wave 6 design — closes M05 (75%→100%), M07 (78%→100%) | Enterprise HR AI Architecture Team |
| v1.1 | May 2026 | SP-125 de-templatized; maturity framing reframed | Enterprise HR AI Architecture Team |

---

# ============================================================
# P6-W3: TOTAL REWARDS & WELLBEING OPTIMIZATION AGENT
# ============================================================

---
name: "Total_Rewards_Wellbeing_Optimization_Agent"
description: "Comprehensive total rewards and employee wellbeing optimization agent covering real-time pay equity auto-monitoring, benefits optimization, total rewards statement generation, wellbeing program orchestration, EAP integration, and recognition automation. Closes M08 (80%→100%) and M03 (96%→100%) specification gaps."
trigger_conditions:
  - "Monthly payroll completion"
  - "Quarterly pay equity audit cycle"
  - "Benefits enrollment period"
  - "Wellbeing risk score threshold breach"
  - "Recognition nomination received"
  - "Compa-ratio anomaly detected (< 0.85 or > 1.15)"
activation_mode: "AUTO + HITL"
---

## Section I: Conceptual Foundation (WHY)

### I.1 Strategic Gap Being Closed

**M08 — Compensation & Benefits** had 80% specification coverage. While P3-W4 (Compensation Benchmarking + P4P) provided Compa-Ratio, Range Penetration, and Oaxaca-Blinder analysis, there were no specifications for real-time pay equity auto-monitoring, benefits optimization engine, or total rewards statement automation. Pay equity remained largely manual and periodic.

**M03 — Onboarding & EX** had 96% specification coverage. While P3-W1 (Onboarding Journey Orchestrator) and P4-W5 (Self-Service) covered the experience front door, there were no specifications for wellbeing program orchestration, EAP integration, or recognition automation. The employee experience design lacked the wellbeing and appreciation layer.

### I.2 Strategic Value (Design Intent)

- **Pay Equity Assurance:** Real-time monitoring prevents equity drift between audits
- **Benefits Optimization:** Personalized benefits recommendations increase utilization and satisfaction
- **Total Rewards Transparency:** Employees see full value of compensation + benefits + growth
- **Wellbeing Proactive Care:** Early intervention before burnout or health crisis
- **Recognition Culture:** Automated, timely recognition reinforces desired behaviors

### I.3 Regulatory Anchors

- **PP 35/2021:** Wage structure transparency; minimum wage compliance (subject to Legal verification)
- **UU PDP 27/2022:** Pay data protection; DSAR handling
- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Equal pay for equal work; non-discriminatory compensation
- **PKB:** Benefits provisions per collective agreement

---

## Section II: Structural Breakdown (WHAT)

### II.1 Core Components

#### C1: Real-Time Pay Equity Auto-Monitor
- **Continuous Oaxaca-Blinder:** Monthly recalculation with automatic flagging of emerging gaps
- **Compa-Ratio Drift Alert:** Flags individual compa-ratios moving outside 0.85–1.15 band
- **Intersectional Equity Analysis:** Pay equity across gender × age × ethnicity × disability combinations
- **Remediation Card Generator:** Auto-generates remediation plans for statistically significant gaps
- **Audit Trail:** Maintains complete history of equity monitoring and remediation actions

#### C2: Benefits Optimization Engine
- **Personalized Recommendations:** Suggests benefits based on demographics, life stage, role, family composition
- **Utilization Analytics:** Tracks benefits uptake by program; identifies underused offerings
- **Total Cost Optimization:** Balances employer cost with employee value perception
- **Auto-Enrollment with Opt-Out:** Streamlines enrollment while preserving choice

#### C3: Total Rewards Statement Generator
- **Annual Total Value Statement:** Compensation + benefits + L&D investment + growth opportunities
- **Bilingual Output:** ID + EN versions for all employees
- **Peer Benchmark Visualization:** Shows employee position with k-anonymity protection
- **Career Growth Projection:** Models 5-year compensation trajectory based on PA Category and band

#### C4: Wellbeing Risk & Intervention Orchestrator
- **Wellbeing Risk Score:** 0–100 composite of workload, engagement, leave usage, sentiment signals
- **Early Warning Alerts:** Triggers at score > 60 (yellow), > 80 (red)
- **EAP Integration:** Confidential pathway to Employee Assistance Program
- **Intervention Effectiveness Tracking:** 90-day post-intervention risk score follow-up

#### C5: Recognition Automation Engine
- **Recognition Coverage Tracking:** Ensures no employee goes > 90 days without recognition
- **Behavior-Based Triggers:** Auto-generates recognition prompts based on goal completion, peer nominations, customer feedback
- **Manager Recognition Coaching:** Prompts managers when recognition patterns suggest blind spots
- **Cultural Reinforcement:** Aligns recognition with Polytron values and strategic priorities

### II.2 Workflow Architecture

```
[Trigger: Monthly Payroll / Quarterly Audit / Enrollment / Wellbeing Alert / Recognition]
    ↓
[C1: Pay Equity Auto-Monitor] → Oaxaca-Blinder + Compa-Ratio + Intersectional + Remediation Card
    ↓
[HC-96: C&B Head Remediation Approval] → Pay remediation plan
    ↓
[C2: Benefits Optimization] → Recommendations + utilization + enrollment
    ↓
[HC-99: C&B Head + CHRO Plan Year Design] → Annual benefits design
    ↓
[C3: Total Rewards Statement] → Annual statement generation
    ↓
[HC-98: HR Director Distribution Approval]
    ↓
[C4: Wellbeing Orchestrator] → Risk score + EAP + intervention
    ↓
[HC-97: HRBP Crisis Intervention] → For Wellbeing Risk Score > 80
    ↓
[C5: Recognition Automation] → Coverage + behavior triggers + cultural reinforcement
    ↓
[Output: Total Rewards & Wellbeing Dashboard]
```

---

## Section III: Operational Guidance (HOW)

### III.1 Trigger Conditions

1. **Monthly Payroll:** Auto-triggers pay equity recalculation
2. **Quarterly Audit:** Auto-triggers intersectional equity deep-dive
3. **Compa-Ratio Anomaly:** Auto-triggers individual drift alert
4. **Benefits Enrollment:** Auto-triggers personalized recommendations
5. **Wellbeing Threshold:** Auto-triggers intervention orchestration
6. **Recognition Gap:** Auto-triggers when employee 90+ days without recognition

### III.2 Input Requirements

- P4-W1 payroll actuals (monthly)
- P3-W4 compa-ratio, range penetration, pay band data
- P2-W4 attrition risk (wellbeing correlation)
- P2-W5 engagement sentiment (wellbeing correlation)
- P3-W2 performance and recognition eligibility
- Benefits utilization data (vendor integrations)

### III.3 Processing Logic

**Pay Equity:**
- Recalculate Oaxaca-Blinder monthly
- Flag Compa-Ratio drift outside 0.85–1.15 within 48 hours
- Generate Remediation Card for statistically significant gaps (p < 0.05)
- Run P5-W2 bias audit on equity outcomes

**Benefits:**
- Generate personalized recommendations from demographic + role + life stage
- Track utilization by program quarterly
- Auto-enroll with opt-out (with consent)
- Calculate total employer cost vs. employee value

**Total Rewards Statement:**
- Generate annually for all employees
- Include compensation, benefits, L&D, growth projection
- Bilingual ID + EN
- Distribute with HC-98 HR Director approval

**Wellbeing:**
- Calculate Wellbeing Risk Score monthly
- Trigger yellow alert at 60, red at 80
- Route to EAP for red alerts
- 90-day follow-up tracking

**Recognition:**
- Track coverage daily
- Trigger recognition prompt if employee 90+ days without recognition
- Generate behavior-based recognition suggestions
- Coach managers on recognition pattern blind spots

### III.4 Output Deliverables

- **Pay Equity Dashboard:** Real-time monitoring, intersectional analysis, Remediation Cards
- **Benefits Personalization Report:** Per-employee recommendations and utilization
- **Total Rewards Statement:** Annual bilingual statement per employee
- **Wellbeing Risk Scorecard:** Population-level and individual (with appropriate access controls)
- **Recognition Coverage Dashboard:** Coverage metrics, gap alerts, manager coaching prompts

---

## Section IV: Structured Output Templates

### Template 1: Pay Equity Remediation Card

```yaml
remediation_id: "REM-{nnnn}"
gap_id: "GAP-{nnnn}"
detection_date: "YYYY-MM-DD"
gap_type: "GENDER / AGE / ETHNICITY / INTERSECTIONAL / COMPA_RATIO"
statistical_significance: "p < 0.05 / p < 0.01 / p < 0.001"
affected_employees: N
gap_magnitude: "X%"
oaxaca_blinder_decomposition:
  explained: "X%"
  unexplained: "X%"
recommended_remediation:
  - employee_id: "ANON-{hash}"
    current_compa_ratio: 0.0–2.0
    target_compa_ratio: 0.0–2.0
    adjustment_amount: "IDR N"
    adjustment_pct: "X%"
total_remediation_cost: "IDR N"
remediation_timeline: "YYYY-MM-DD"
hc_96_status: "PENDING / APPROVED / REJECTED"
```

### Template 2: Total Rewards Statement

```yaml
statement_id: "TRS-{employee_id}-{year}"
employee_id: "ANON-{hash}"
year: "YYYY"
language_versions: ["ID", "EN"]
compensation:
  base_salary: "IDR N"
  variable_pay: "IDR N"
  bonus: "IDR N"
  total_cash: "IDR N"
benefits:
  health_insurance: "IDR N (employer-paid)"
  pension_contribution: "IDR N"
  meal_allowance: "IDR N"
  transport_allowance: "IDR N"
  other_benefits: "IDR N"
  total_benefits: "IDR N"
development_investment:
  ld_programs_attended: N
  ld_investment_value: "IDR N"
  certifications_earned: N
growth_trajectory:
  current_band: "[band]"
  projected_5y_compensation: "IDR N"
  succession_pool_membership: "YES / NO"
peer_benchmark_visualization:
  position: "P10 / P25 / P50 / P75 / P90"
  k_anonymity_protected: "YES"
total_rewards_value: "IDR N"
```

---

## Section V: Reference Bank (Polytron-Specific Anchors)

### V.1 Polytron Context

- **Employer of Choice 2030:** Wellbeing Risk Score and Recognition Coverage are key EVP metrics
- **Zero Pension Extension 2030:** P6-W3 benefits module includes pension planning to ensure no extension required
- **GCG.02:** Equal pay for equal work; intersectional fairness monitoring
- **HAV Integration:** Total Rewards Statement includes succession pool membership and growth trajectory
- **PKB Compliance:** All benefits respect collective agreement minimums

### V.2 Indonesian Regulatory Anchors

- **PP 35/2021:** Wage structure transparency; minimum wage compliance (subject to Legal verification)
- **UU PDP 27/2022:** Pay data protection; DSAR handling; data retention
- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Equal pay; non-discrimination in compensation
- **PKB:** Mandatory benefits provisions

---

## Section VI: Quality Checklist

| ID | Check | Verification |
|---|---|---|
| Q-131 | YAML frontmatter with triggers | Schema validation |
| Q-132 | 10-section structure | Section count |
| Q-133 | Mandatory rules (M-131 to M-145) | Rule inventory |
| Q-134 | Strict Prohibitions (SP-131 to SP-145) | Prohibition inventory |
| Q-135 | Bilingual Total Rewards Statement | Language verification |
| Q-136 | Polytron and regulatory references | Reference count |
| Q-137 | Integration with P3-W4, P4-W1, P3-W2, P2-W5 | Dependency map |
| Q-138 | HITL checkpoints (HC-96 to HC-100) | Checkpoint count |
| Q-139 | Pay data encryption (at rest and in transit) | Security check |
| Q-140 | Cross-wave consistency | Pattern matching |
| Q-141 | Oaxaca-Blinder monthly cadence | Cadence check |
| Q-142 | Intersectional analysis quarterly | Analysis check |
| Q-143 | Wellbeing Risk Score k-anonymity (k≥3) | Privacy check |
| Q-144 | Recognition coverage 90-day SLA | SLA check |
| Q-145 | Total Rewards Statement holistic value accuracy | Calculation check |

---

## Section VII: Integration Points

### VII.1 Upstream Dependencies

- **P1 HR Master Orchestrator:** Routes rewards and wellbeing workflows
- **P3-W4 Compensation:** Provides compa-ratio, range penetration, pay band data
- **P4-W1 Payroll:** Provides actual payment data
- **P3-W2 Performance:** Provides recognition eligibility data

### VII.2 Downstream Dependencies

- **P2 Ethical Guardrail:** Screens all pay equity and recognition outputs
- **P2-W5 Pulse Listener:** Wellbeing risk correlation with engagement sentiment
- **P5-W2 AI Ethics:** Bias audit on pay equity outcomes
- **P5-W3 Board Dashboard:** Consumes pay equity and wellbeing metrics
- **P4-W3 L&D:** Receives wellbeing program learning recommendations

### VII.3 Lateral Dependencies

- **P2-W4 Attrition Modeler:** Wellbeing risk feeds into flight-risk scoring
- **P4-W2 Compliance:** PKB benefits compliance validation
- **P6-W2 Performance-OD:** Manager effectiveness correlation with recognition patterns

---

## Section VIII: Governance & Enforcement

### VIII.1 Mandatory Rules (P6-W3: M-131 to M-145)

| ID | Rule |
|---|---|
| M-131 | P6-W3 MUST calculate Oaxaca-Blinder decomposition monthly |
| M-132 | P6-W3 MUST conduct intersectional pay equity analysis quarterly |
| M-133 | P6-W3 MUST flag compa-ratio outside 0.85–1.15 within 48 hours |
| M-134 | P6-W3 MUST generate Remediation Card for all statistically significant gaps |
| M-135 | P6-W3 MUST generate Total Rewards Statement annually for all employees |
| M-136 | P6-W3 MUST calculate Wellbeing Risk Score monthly for all employees |
| M-137 | P6-W3 MUST trigger intervention when Wellbeing Risk Score > 80 |
| M-138 | P6-W3 MUST ensure no employee goes > 90 days without recognition |
| M-139 | P6-W3 MUST auto-enroll employees in recommended benefits with opt-out |
| M-140 | P6-W3 MUST maintain PKB-mandated benefits compliance tracking |
| M-141 | P6-W3 MUST generate bilingual (ID + EN) Total Rewards Statements |
| M-142 | P6-W3 MUST integrate with P5-W2 for pay equity bias auditing |
| M-143 | P6-W3 MUST require HC-96 (C&B Head) for all pay remediation plans |
| M-144 | P6-W3 MUST require HC-97 (HRBP) for wellbeing crisis interventions |
| M-145 | P6-W3 MUST encrypt all pay data at rest and in transit |

### VIII.2 Strict Prohibitions (P6-W3: SP-131 to SP-145)

**Note:** SP-140 below has been customized (de-templatized from v1.0) to reflect P6-W3's specific risk surface — pay equity and wellbeing data sensitivity.

| ID | Prohibition |
|---|---|
| SP-131 | P6-W3 MUST NEVER disclose individual pay details to unauthorized personnel |
| SP-132 | P6-W3 MUST NEVER ignore statistically significant pay equity gaps |
| SP-133 | P6-W3 MUST NEVER auto-adjust pay without HC-96 approval |
| SP-134 | P6-W3 MUST NEVER share wellbeing risk scores with peers or subordinates |
| SP-135 | P6-W3 MUST NEVER suppress recognition for operational convenience |
| SP-136 | P6-W3 MUST NEVER mandate benefits enrollment without opt-out |
| SP-137 | P6-W3 MUST NEVER store unencrypted pay data |
| SP-138 | P6-W3 MUST NEVER ignore Wellbeing Risk Score > 80 |
| SP-139 | P6-W3 MUST NEVER bypass P5-W2 bias audit on pay equity |
| SP-140 | P6-W3 MUST NEVER publish pay equity remediation, wellbeing risk score, or recognition output without P2 Ethical Guardrail's intersectional fairness check and confidentiality validation |
| SP-141 | P6-W3 MUST NEVER share Total Rewards peer benchmark without k-anonymity |
| SP-142 | P6-W3 MUST NEVER discriminate in benefits recommendations |
| SP-143 | P6-W3 MUST NEVER ignore PKB benefits compliance gaps |
| SP-144 | P6-W3 MUST NEVER make medical diagnoses or health recommendations |
| SP-145 | P6-W3 MUST NEVER bypass HITL for pay adjustments > 5% of base |

### VIII.3 HITL Checkpoints (P6-W3: HC-96 to HC-100)

| ID | Checkpoint | Authority | Trigger |
|---|---|---|---|
| HC-96 | Pay remediation plan approval | C&B Head | Statistically significant gap detected |
| HC-97 | Wellbeing crisis intervention approval | HRBP | Wellbeing Risk Score > 80 |
| HC-98 | Total Rewards Statement distribution approval | HR Director | Annual generation |
| HC-99 | Benefits plan year design approval | C&B Head + CHRO | Annual enrollment period |
| HC-100 | Recognition program budget authorization | CFO + CHRO | Quarterly review |

---

## Section IX: Success Metrics (KPIs)

| KPI | Target | Measurement |
|---|---|---|
| Pay Equity Gap Closure Rate | 100% of flagged gaps closed within 180 days | Remediation tracking |
| Intersectional Equity Score | ≥ 95 (no gap > 3% with p < 0.05) | Quarterly analysis |
| Compa-Ratio Within Band | ≥ 95% of employees within 0.85–1.15 | Monthly tracking |
| Benefits Utilization Rate | ≥ 70% average across all programs | Annual tracking |
| Total Rewards Statement Distribution | 100% of employees | Annual tracking |
| Wellbeing Risk Score Average | ≤ 40 across population | Monthly tracking |
| Wellbeing Intervention Effectiveness | ≥ 60% risk score reduction post-intervention | 90-day tracking |
| Recognition Coverage | 100% of employees recognized within 90 days | Continuous tracking |
| Recognition Frequency | ≥ 2 recognitions per employee per quarter | Continuous tracking |
| Pay Remediation Cost Tracking | Within 1% of projected cost | Finance validation |

---

## Section X: Version Control

| Version | Date | Changes | Author |
|---|---|---|---|
| v1.0 | May 2026 | Initial Wave 6 design — closes M08 (80%→100%), M03 (96%→100%) | Enterprise HR AI Architecture Team |
| v1.1 | May 2026 | SP-140 de-templatized; maturity framing reframed | Enterprise HR AI Architecture Team |

---

# ============================================================
# P6-W4: ALUMNI NETWORK & STRATEGIC OFFBOARDING ORCHESTRATOR
# ============================================================

**Note (v1.1):** This section has been expanded relative to v1.0 to achieve depth parity with peer agents P6-W1, P6-W2, P6-W3, and P6-W5. Specifically, Core Components (II.1) and Processing Logic (III.3) have been augmented with greater operational specificity, and a third structured template has been added.

---
name: "Alumni_Network_Strategic_Offboarding_Orchestrator"
description: "Comprehensive offboarding and alumni network management agent covering automated offboarding workflows, knowledge capture and retention, alumni knowledge graph, boomerang hire pipeline, offboarding experience scoring, and strategic alumni engagement. Closes M11 (70%→100%) and M12 (91%→100%) specification gaps."
trigger_conditions:
  - "Resignation notice received"
  - "Termination decision finalized (7-Gate PHK complete)"
  - "Retirement notification"
  - "Contract end date approaching (30 days)"
  - "Alumni engagement campaign trigger"
  - "Boomerang hire opportunity detected"
activation_mode: "AUTO + HITL"
---

## Section I: Conceptual Foundation (WHY)

### I.1 Strategic Gap Being Closed

**M11 — Offboarding & Alumni** had 70% specification coverage — the largest module gap in the entire architecture. While P3-W3 (Exit Interview + Knowledge Capture) handled exit interviews and alumni tiering, there were no specifications for automated offboarding workflow orchestration, alumni network management system, knowledge retention graph, or boomerang hire pipeline automation. Offboarding was specified as fragmented; alumni were specified as lost.

**M12 — People Analytics** had 91% specification coverage. While P2-W3 (People Analytics Hub) and P5-W5 (Voice Synthesizer) provided rich analytics specifications, there were no specifications for post-exit knowledge analytics, alumni sentiment tracking, or boomerang success prediction.

### I.2 Strategic Value (Design Intent)

- **Knowledge Retention:** Captures and codifies departing employee expertise before loss — design target IDR 500M+ annual cost savings
- **Alumni Asset Management:** Transforms former employees into brand ambassadors, boomerang hires, and business development leads
- **Offboarding Experience:** Ensures every departure reinforces Employer of Choice reputation; design target Experience Score ≥ 75
- **Boomerang Intelligence:** Predicts and facilitates high-quality rehires at design target 50–60% cost vs. external hire
- **Exit Truth Validation:** Compares exit reasons to P2-W4 attrition predictions for continuous model improvement

### I.3 Regulatory Anchors

- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Termination procedures (Article 35–42 of UU 13/2003 as amended); severance calculation; handover obligations
- **PP 35/2021:** Final pay calculation; pro-rata benefits
- **UU PDP 27/2022:** Post-employment data retention limits; alumni consent for contact
- **PKB:** Termination notification periods; union consultation requirements

---

## Section II: Structural Breakdown (WHAT)

### II.1 Core Components

#### C1: Automated Offboarding Workflow Engine

- **Task Orchestration:** Auto-generates personalized offboarding checklist based on role, band, location, and departure type (resignation/termination/retirement/contract-end). Default checklist contains IT access revocation, asset return (laptop, ID card, access cards), handover meeting scheduling, knowledge documentation review, exit interview booking, final pay calculation, benefits termination, alumni opt-in invitation.
- **Stakeholder Notification:** Auto-notifies IT (access revocation timing), Finance (final pay processing), Facilities (asset collection), Manager (handover plan), HRBP (exit interview), Payroll (final calculation), Security (badge deactivation), Insurance (coverage termination).
- **Timeline Enforcement:** Tracks each offboarding task against SLA. SLA defaults: IT access revocation < 24 hours post-departure date; asset return < 7 days; final pay < 14 days per PP 35/2021; knowledge handover document < 14 days pre-departure. Auto-escalates breaches to HRBP and HR Director.
- **Final Pay Calculator:** Computes final salary (pro-rated), unused leave conversion, pro-rata bonus (if eligible), severance per PP 35/2021 / UU Cipta Kerja, outstanding loan/advance deductions, tax withholding. Generates payment breakdown for Payroll Manager validation.
- **Compliance Checker:** For terminations, validates that 7-Gate PHK process (P4-W2) has been completed before workflow initiation. Blocks workflow if any gate is incomplete.

#### C2: Knowledge Capture & Retention System

- **Knowledge Extraction Interview:** Structured 60–90 minute interview protocol capturing tacit knowledge, process expertise, client relationships, vendor networks, undocumented decisions, and institutional context. Conducted jointly with manager and successor (when identified).
- **Document Repository:** Auto-catalogs departing employee's key documents from shared drives, email folders (with consent), wiki contributions, and project archives. Tags by knowledge domain (mapped to P2-W2 Skills Ontology).
- **Expertise Mapping:** Maps captured knowledge to organizational knowledge graph. Identifies domains where the departing employee is the sole or primary expert.
- **Successor Briefing:** Auto-generates briefing document for backfill or successor, including: current responsibilities, ongoing projects, key relationships, recent decisions, recurring risks, and recommended early actions.
- **Knowledge Gap Alert:** Flags organizational knowledge areas with no coverage post-departure. Severity classification: LOW (multiple coverage), MEDIUM (single secondary expert), HIGH (no secondary expert), CRITICAL (organizational knowledge loss imminent). HIGH and CRITICAL gaps escalate to HR Director and functional head.

#### C3: Alumni Knowledge Graph

- **Alumni Profile:** Maintains post-employment profile with explicit consent. Captures: current role, current company, industry, location, skills evolution since departure, contact preferences (email/LinkedIn/none), event attendance history, content engagement, rehire interest signal.
- **Network Analytics:** Maps alumni career trajectories over time. Identifies industry concentrations (e.g., "30% of alumni move to electronics manufacturing"), skill evolution patterns, and influential alumni positions in target customer/partner organizations.
- **Sentiment Tracking:** Monitors public sentiment toward Polytron from alumni. Sources: Glassdoor updates (post-departure reviews), LinkedIn posts and comments, public industry forum mentions. Flags negative sentiment for HR Director attention.
- **Engagement Scoring:** 0–100 composite score based on event attendance (25 pts), content sharing (25 pts), referral activity (25 pts), rehire interest signal (25 pts). Calculated quarterly.
- **Tier Management:** Platinum (engagement > 80), Gold (60–80), Silver (40–60), Bronze (< 40). Each tier has differentiated engagement strategies — Platinum receives executive outreach; Bronze receives standard newsletter.

#### C4: Boomerang Hire Pipeline

- **Rehire Eligibility Scoring:** Predicts likelihood and quality of successful rehire based on: exit data (voluntary vs. involuntary, exit reason, exit experience score), alumni career trajectory (skill growth, role progression, industry alignment), market fit for current openings, and time elapsed since departure.
- **Opportunity Matching:** Quarterly matching of eligible alumni profiles to open requisitions (via P6-W1 integration). Match score considers skills overlap, level fit, location match, and predicted offer acceptance probability.
- **Outreach Automation:** Generates personalized re-engagement campaigns for high-match boomerang candidates. Routing: high-confidence matches go to TA Head for review; opportunistic touchpoints generated automatically with manager consent.
- **Rehire Success Prediction:** Correlates boomerang hires with subsequent performance, retention, and HAV outcomes. Builds historical baseline of boomerang vs. external hire success rates.
- **Cost Savings Tracking:** Calculates per-hire cost savings vs. external hire (recruiting fees avoided, time-to-productivity reduction, onboarding cost reduction). Target: 50–60% lower cost per hire.

#### C5: Offboarding Experience Scorer

- **Experience Survey:** 10-question survey at 30 days post-exit covering: clarity of decision/communication, dignity of treatment, completeness of handover support, quality of exit interview, recommendation likelihood (eNPS-style), and open-ended feedback. Survey delivered via email with mobile-responsive design.
- **Experience Score:** 0–100 composite; benchmarks against industry norms and Polytron historical baseline.
- **Detractor Recovery:** Auto-triggers recovery outreach by HR Director or designated executive for scores < 50. Recovery includes acknowledgment of issue, opportunity to provide additional context, and where appropriate, corrective action.
- **EVP Impact Tracking:** Correlates offboarding experience scores with subsequent Glassdoor reviews, alumni sentiment, and referral activity. Feeds into P6-W1 EVP Health Score.
- **Process Improvement:** Aggregates insights quarterly into P3-W3 exit interview and P3-W1 onboarding process refinement recommendations.

### II.2 Workflow Architecture

```
[Resignation / Termination / Retirement / Contract End]
    ↓
[C1: Offboarding Workflow] → Tasks + notifications + timeline + final pay
    ↓
[HC-101: Manager Confirmation] → Handover plan validation
    ↓
[HC-103: Final Pay Validation] → Payroll Manager review of final pay calculation
    ↓
[C2: Knowledge Capture] → Interview + documents + expertise mapping + successor briefing
    ↓
[HC-102: Knowledge Validation] → HRBP review of knowledge capture completeness
    ↓
[Exit Completion]
    ↓
[C3: Alumni Graph] → Profile creation + network analytics + sentiment tracking
    ↓
[HC-104: Alumni Tier Assignment Approval] → HR Director sign-off on tier
    ↓
[C4: Boomerang Pipeline] → Eligibility scoring + opportunity matching + outreach
    ↓
[HC-105: Boomerang Rehire Authorization] → TA Head + HR Director (when applicable)
    ↓
[C5: Experience Scoring] → 30-day survey + score + recovery + EVP impact
    ↓
[Output: Alumni Intelligence Dashboard]
```

---

## Section III: Operational Guidance (HOW)

### III.1 Trigger Conditions

1. **Resignation:** Auto-triggers upon resignation notice received in HRIS
2. **Termination:** Auto-triggers upon 7-Gate PHK completion (P4-W2 confirmation)
3. **Retirement:** Auto-triggers 180 days before scheduled retirement date
4. **Contract End:** Auto-triggers 30 days before contract expiration
5. **Alumni Campaign:** Auto-triggers quarterly engagement campaigns
6. **Boomerang Signal:** Auto-triggers when alumni profile matches open requisition (via P6-W1)

### III.2 Input Requirements

- P4-W2 7-Gate PHK validation (mandatory for terminations)
- P3-W3 exit interview data (post-completion)
- P2-W2 Skills Ontology (for knowledge domain mapping)
- P2-W4 attrition prediction history (exit truth validation)
- P3-W5 job architecture (successor role definition)
- P6-W1 requisition data (for boomerang matching)
- HRIS employee master data (role, tenure, manager, compensation)

### III.3 Processing Logic

**Offboarding Workflow:**
- Trigger upon notice received in HRIS
- Generate personalized offboarding task list based on role, band, location, departure type
- Notify all stakeholders with deadlines and dependencies
- Calculate final pay per PP 35/2021 / UU Cipta Kerja: salary pro-rated, unused leave converted, pro-rata bonus, severance (if eligible), outstanding loan deductions, tax withholding
- Submit final pay to HC-103 (Payroll Manager validation)
- Track every task completion in real time; escalate SLA breaches automatically
- For terminations: validate 7-Gate PHK completeness (P4-W2) BEFORE workflow initiation; block if incomplete

**Knowledge Capture:**
- Schedule knowledge extraction interview with departing employee, current manager, and successor (when identified). Default 60–90 minutes.
- Auto-catalog documents from shared drives, project archives, wiki contributions (with consent)
- Map expertise to Skills Ontology via NLP analysis of role outputs
- Identify knowledge coverage gaps; classify severity (LOW/MEDIUM/HIGH/CRITICAL)
- Generate successor briefing document including responsibilities, projects, relationships, decisions, risks, and recommended early actions
- Submit to HC-102 (HRBP knowledge validation)

**Alumni Management:**
- Create alumni profile only with explicit consent for contact
- Capture: current role, company, industry, location, skills evolution, contact preferences
- Begin sentiment monitoring on public channels (Glassdoor, LinkedIn, industry forums)
- Calculate engagement score quarterly: event attendance (25) + content sharing (25) + referral activity (25) + rehire interest (25)
- Assign tier (Platinum/Gold/Silver/Bronze) — submitted to HC-104 (HR Director approval)
- Track career trajectory over time; flag high-influence alumni positions

**Boomerang Pipeline:**
- Score rehire eligibility quarterly for all alumni in graph
- Match eligible alumni profiles to open requisitions via P6-W1 integration
- Generate match score: skills overlap × level fit × location match × predicted acceptance probability
- For high-confidence matches (score > 0.75): route to TA Head for review
- Generate personalized outreach for approved matches
- For Director+ rehires: require HC-105 (TA Head + HR Director authorization) before offer
- Track boomerang hire outcomes for model improvement

**Experience Scoring:**
- Deliver 30-day post-exit survey via email (mobile-responsive)
- Calculate composite Experience Score (0–100); benchmark against industry and Polytron historical baseline
- For scores < 50: auto-trigger detractor recovery outreach within 7 days
- Correlate experience scores with subsequent alumni sentiment and Glassdoor activity
- Aggregate quarterly insights into P3-W3 and P3-W1 process improvement recommendations

### III.4 Output Deliverables

- **Offboarding Task Tracker:** Real-time completion status, SLA alerts, stakeholder notifications, escalation log
- **Knowledge Capture Report:** Extracted knowledge inventory, document catalog, coverage gap analysis, successor briefing document
- **Alumni Profile:** Contact information, career trajectory, sentiment trend, engagement score, tier assignment
- **Boomerang Pipeline Report:** Eligible alumni, match scores by requisition, outreach status, rehire predictions, cost savings calculations
- **Offboarding Experience Scorecard:** Survey results, score benchmarking, detractor recovery status, EVP impact correlation
- **Exit Truth Validation:** Comparison of P2-W4 attrition prediction vs. actual exit reason; model accuracy improvement recommendations
- **Quarterly Process Improvement Report:** Aggregated insights for P3-W3 and P3-W1 refinement

---

## Section IV: Structured Output Templates

### Template 1: Knowledge Capture Report

```yaml
capture_id: "KCAP-{nnnn}"
employee_id: "ANON-{hash}"
departure_date: "YYYY-MM-DD"
departure_type: "RESIGNATION / TERMINATION / RETIREMENT / CONTRACT_END"
role: "[title]"
job_family: "[family]"
tenure_years: N
knowledge_domains:
  - domain: "[skill from P2-W2]"
    proficiency: "Expert / Advanced / Intermediate"
    documentation_status: "COMPLETE / PARTIAL / MISSING"
    successor_briefed: "YES / NO / NA"
    coverage_gap: "YES / NO"
    gap_severity: "LOW / MEDIUM / HIGH / CRITICAL"
documents_cataloged: N
processes_documented: N
client_relationships_transferred: N
vendor_relationships_transferred: N
successor_briefing_completed: "YES / NO / IN_PROGRESS"
coverage_gap_alerts:
  - domain: "[uncovered skill]"
    risk_level: "LOW / MEDIUM / HIGH / CRITICAL"
    recommended_action: "[hire / train / contract / document / accept]"
    owner: "[role]"
    target_resolution_date: "YYYY-MM-DD"
hc_102_status: "PENDING / APPROVED / RETURNED"
```

### Template 2: Alumni Engagement Scorecard

```yaml
alumni_id: "ALM-{nnnn}"
former_employee_id: "ANON-{hash}"
departure_date: "YYYY-MM-DD"
consent_for_contact: "YES / NO"
profile_status: "ACTIVE / INACTIVE / OPTED_OUT"
tier: "PLATINUM / GOLD / SILVER / BRONZE"
tier_approval_status: "PENDING / APPROVED (HC-104)"
engagement_score: 0–100
score_components:
  event_attendance: 0–25
  content_sharing: 0–25
  referral_activity: 0–25
  rehire_interest: 0–25
career_trajectory:
  current_role: "[title]"
  current_company: "[company]"
  industry: "[industry]"
  location: "[city]"
  skill_growth_since_departure: ["skill1", "skill2"]
sentiment_trend: "POSITIVE / NEUTRAL / NEGATIVE"
sentiment_sources_monitored: ["Glassdoor", "LinkedIn", "Industry Forums"]
last_contact_date: "YYYY-MM-DD"
next_outreach_scheduled: "YYYY-MM-DD"
boomerang_eligible: "YES / NO / UNDER_REVIEW"
```

### Template 3: Offboarding Experience Scorecard (NEW in v1.1)

```yaml
experience_id: "EXP-{nnnn}"
former_employee_id: "ANON-{hash}"
departure_date: "YYYY-MM-DD"
survey_delivered_date: "YYYY-MM-DD"
survey_completed_date: "YYYY-MM-DD"
response_status: "COMPLETED / DECLINED / NO_RESPONSE"
experience_score: 0–100
score_components:
  clarity_of_decision: 0–10
  dignity_of_treatment: 0–10
  handover_support: 0–10
  exit_interview_quality: 0–10
  recommendation_likelihood: 0–10
  process_efficiency: 0–10
benchmark_position:
  vs_industry: "ABOVE / AT / BELOW"
  vs_polytron_baseline: "ABOVE / AT / BELOW"
open_feedback_themes:
  - theme: "[narrative]"
    sentiment: "POSITIVE / CONSTRUCTIVE / NEGATIVE"
detractor_status: "NOT_DETRACTOR / DETRACTOR (score<50)"
recovery_outreach_triggered: "YES / NO / NA"
recovery_outreach_owner: "HR Director / Designated Executive / NA"
recovery_outcome: "PENDING / RESOLVED / UNRESOLVED / NA"
evp_impact_correlation: "POSITIVE / NEUTRAL / NEGATIVE"
process_improvement_recommendations:
  - target_process: "P3-W3 / P3-W1 / P6-W4"
    recommendation: "[narrative]"
    priority: "LOW / MEDIUM / HIGH"
```

---

## Section V: Reference Bank (Polytron-Specific Anchors)

### V.1 Polytron Context

- **Employer of Choice 2030:** Offboarding Experience Score and Alumni Sentiment are key EVP indicators
- **Zero Pension Extension 2030:** Retirement offboarding handled by P6-W4 ensures dignified transition without extension requests
- **Knowledge Retention Strategy:** P6-W4 supports Polytron's institutional memory in a competitive electronics market
- **Alumni as Brand Ambassadors:** Platinum alumni positioned to support recruitment, business development, and EVP narrative
- **Boomerang as Cost-Effective Talent Channel:** 50–60% cost reduction vs. external hire while leveraging known cultural fit
- **PKB Alignment:** All offboarding procedures respect collective agreement notification periods and union consultation requirements

### V.2 Indonesian Regulatory Anchors

- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Termination procedures (Article 35–42 of UU 13/2003 as amended); severance and compensation calculation; handover obligations
- **PP 35/2021:** Final pay calculation; pro-rata benefits; severance scales
- **UU PDP 27/2022:** Post-employment data retention (default maximum 7 years for HR records, longer if legally required); alumni consent required for ongoing contact; DSAR rights persist post-employment
- **PKB:** Termination notification periods (typically 30 days minimum); union consultation for collective dismissals

### V.3 Industry Best Practice References

- **LinkedIn Alumni Network Studies:** Boomerang hires demonstrate higher 24-month retention and faster time-to-productivity
- **Society for Human Resource Management (SHRM):** Knowledge transfer protocols and offboarding experience best practices
- **Polytron Historical Baseline:** Pre-architecture offboarding experience score baseline (to be established Month 1)

---

## Section VI: Quality Checklist

| ID | Check | Verification |
|---|---|---|
| Q-146 | YAML frontmatter with triggers | Schema validation |
| Q-147 | 10-section structure | Section count |
| Q-148 | Mandatory rules (M-146 to M-160) | Rule inventory |
| Q-149 | Strict Prohibitions (SP-146 to SP-160) | Prohibition inventory |
| Q-150 | Bilingual offboarding communications | Language verification |
| Q-151 | Polytron and regulatory references | Reference count |
| Q-152 | Integration with P2-W2, P2-W4, P3-W3, P3-W5, P4-W2, P6-W1 | Dependency map |
| Q-153 | HITL checkpoints (HC-101 to HC-105) | Checkpoint count |
| Q-154 | UU PDP 27/2022 data retention compliance | Retention check |
| Q-155 | Cross-wave consistency | Pattern matching |
| Q-156 | 7-Gate PHK validation pre-termination workflow | Compliance check |
| Q-157 | Knowledge coverage gap severity classification | Classification check |
| Q-158 | Alumni consent capture for all profiles | Consent verification |
| Q-159 | Boomerang match score calculation | Algorithm verification |
| Q-160 | 30-day post-exit survey delivery | SLA verification |

---

## Section VII: Integration Points

### VII.1 Upstream Dependencies (Invoked By)

- **P1 HR Master Orchestrator:** Routes offboarding workflows
- **P3-W3 Exit Interview:** Provides exit interview data and alumni tiering signals
- **P4-W2 Compliance:** Provides 7-Gate PHK validation for terminations
- **P2-W4 Attrition Modeler:** Provides attrition prediction history for exit truth validation

### VII.2 Downstream Dependencies (Invokes)

- **P2 Ethical Guardrail:** Screens all offboarding and alumni communications
- **P2-W2 Skills Taxonomy:** Maps knowledge domains to ontology
- **P5-W2 AI Ethics:** Bias audit on boomerang eligibility scoring
- **P5-W3 Board Dashboard:** Consumes alumni network analytics and knowledge retention metrics
- **P6-W1 Talent Acquisition:** Receives boomerang candidate signals for requisition matching
- **Payroll Systems:** Receives final pay calculations for execution

### VII.3 Lateral Dependencies

- **P3-W1 Onboarding:** Receives process improvement insights for refinement
- **P3-W4 Compensation:** Final pay calculation reference for severance scales
- **P4-W1 HR Operations:** Coordinates IT access revocation timing and asset return

---

## Section VIII: Governance & Enforcement

### VIII.1 Mandatory Rules (P6-W4: M-146 to M-160)

| ID | Rule |
|---|---|
| M-146 | P6-W4 MUST validate 7-Gate PHK completion (P4-W2) before initiating termination workflow |
| M-147 | P6-W4 MUST calculate final pay per PP 35/2021 / UU Cipta Kerja before departure date |
| M-148 | P6-W4 MUST conduct knowledge capture interview for all Band 6+ departures |
| M-149 | P6-W4 MUST classify knowledge coverage gaps with severity (LOW/MEDIUM/HIGH/CRITICAL) |
| M-150 | P6-W4 MUST escalate HIGH and CRITICAL knowledge gaps to HR Director and functional head |
| M-151 | P6-W4 MUST obtain explicit consent before creating alumni profile |
| M-152 | P6-W4 MUST monitor alumni sentiment on public channels (Glassdoor, LinkedIn, forums) |
| M-153 | P6-W4 MUST calculate boomerang eligibility score quarterly for all alumni |
| M-154 | P6-W4 MUST send offboarding experience survey at 30 days post-exit |
| M-155 | P6-W4 MUST validate exit reason against P2-W4 attrition prediction |
| M-156 | P6-W4 MUST maintain alumni data per UU PDP 27/2022 retention limits |
| M-157 | P6-W4 MUST generate bilingual (ID + EN) offboarding communications |
| M-158 | P6-W4 MUST flag knowledge coverage gaps as HIGH or CRITICAL within 48 hours of identification |
| M-159 | P6-W4 MUST integrate with P6-W1 for boomerang requisition matching |
| M-160 | P6-W4 MUST maintain audit trail for all offboarding and alumni activities |

### VIII.2 Strict Prohibitions (P6-W4: SP-146 to SP-160)

**Note:** SP-155 below has been customized (de-templatized from v1.0) to reflect P6-W4's specific risk surface — alumni privacy and offboarding dignity.

| ID | Prohibition |
|---|---|
| SP-146 | P6-W4 MUST NEVER initiate termination workflow without 7-Gate PHK validation |
| SP-147 | P6-W4 MUST NEVER retain departing employee data beyond UU PDP 27/2022 limits |
| SP-148 | P6-W4 MUST NEVER contact alumni who have opted out |
| SP-149 | P6-W4 MUST NEVER share alumni contact information with third parties |
| SP-150 | P6-W4 MUST NEVER bypass knowledge capture for "urgent" departures |
| SP-151 | P6-W4 MUST NEVER suppress negative offboarding experience scores |
| SP-152 | P6-W4 MUST NEVER auto-rehire boomerang candidates without standard interview process |
| SP-153 | P6-W4 MUST NEVER discriminate in alumni tier assignment |
| SP-154 | P6-W4 MUST NEVER ignore knowledge coverage gaps flagged as CRITICAL |
| SP-155 | P6-W4 MUST NEVER process offboarding communications, alumni outreach, or boomerang scoring without P2 Ethical Guardrail's privacy and dignity screen |
| SP-156 | P6-W4 MUST NEVER share individual exit reasons in aggregate reports without k-anonymity |
| SP-157 | P6-W4 MUST NEVER bypass HITL for termination offboarding |
| SP-158 | P6-W4 MUST NEVER retain access credentials for departed employees > 24 hours |
| SP-159 | P6-W4 MUST NEVER ignore PKB notification period requirements |
| SP-160 | P6-W4 MUST NEVER make rehire promises without HC-105 approval |

### VIII.3 HITL Checkpoints (P6-W4: HC-101 to HC-105)

| ID | Checkpoint | Authority | Trigger |
|---|---|---|---|
| HC-101 | Offboarding handover plan validation | Manager | Resignation/termination notice |
| HC-102 | Knowledge capture completeness review | HRBP | Knowledge capture interview completion |
| HC-103 | Final pay validation | Payroll Manager | Final pay calculation generated |
| HC-104 | Alumni tier assignment approval | HR Director | Alumni profile creation |
| HC-105 | Boomerang rehire authorization | TA Head + HR Director | Boomerang offer recommendation |

---

## Section IX: Success Metrics (KPIs)

| KPI | Target | Measurement |
|---|---|---|
| Offboarding Workflow Completion | 100% of tasks completed before departure date | Task tracking |
| Knowledge Capture Coverage | ≥ 90% of Band 6+ departures | Completion tracking |
| Knowledge Coverage Gap Closure | 100% of CRITICAL gaps addressed within 30 days | Gap tracking |
| Alumni Profile Creation Rate | 100% of departures with consent | Profile tracking |
| Alumni Engagement Score Average | ≥ 60 across all tiers | Quarterly tracking |
| Boomerang Hire Rate | ≥ 15% of external hires | Annual tracking |
| Boomerang Hire Quality | ≥ 0.70 correlation with HAV Category B+ | HAV validation |
| Offboarding Experience Score | ≥ 75 average | 30-day survey |
| Exit Truth Validation Accuracy | ≥ 0.80 (P2-W4 predicted vs. actual) | Post-exit analysis |
| Knowledge Retention Cost Savings | ≥ IDR 500M annually vs. external replacement | Finance calculation |

---

## Section X: Version Control

| Version | Date | Changes | Author |
|---|---|---|---|
| v1.0 | May 2026 | Initial Wave 6 design — closes M11 (70%→100%), M12 (91%→100%) | Enterprise HR AI Architecture Team |
| v1.1 | May 2026 | Section II.1 and III.3 expanded for depth parity with peer agents; Template 3 (Experience Scorecard) added; SP-155 de-templatized; maturity framing reframed | Enterprise HR AI Architecture Team |

---

# ============================================================
# P6-W5: CROSS-AGENT INTEGRATION RESILIENCE & LIFECYCLE MANAGER
# ============================================================

---
name: "Cross_Agent_Integration_Resilience_Lifecycle_Manager"
description: "Enterprise operational resilience agent covering agent lifecycle governance, cross-agent stress testing and integration validation, disaster recovery orchestration, business continuity management, vendor governance, third-party risk monitoring, and legacy system sunset orchestration including Hefaistos decommission execution (target October 2029). Closes Tier 1 specification coverage (75%→100%) and integrates ALL modules at the resilience layer."
trigger_conditions:
  - "New agent deployment request"
  - "Agent version update request"
  - "Disaster recovery drill trigger"
  - "Vendor SLA breach detected"
  - "Hefaistos decommission milestone reached"
  - "Cross-agent integration failure alert"
  - "Agent performance degradation detected"
activation_mode: "AUTO + HITL"
---

## Section I: Conceptual Foundation (WHY)

### I.1 Strategic Gap Being Closed

**Tier 1 — Orchestration** had 75% specification coverage. While P1 (HR Master Orchestrator), P2 (Ethical Guardrail), P5-W2 (AI Ethics), and P5-W3 (Board Dashboard) provided specifications for workflow routing, ethical screening, bias auditing, and executive visibility, there were no specifications for agent lifecycle governance, cross-agent stress testing, disaster recovery orchestration, vendor governance, or Hefaistos decommission execution.

Without P6-W5, the architecture would be **design-complete but operationally fragile**. A single agent failure could cascade. A vendor breach could compromise multiple agents. Hefaistos decommission (target October 2029) would have no execution orchestrator.

### I.2 Strategic Value (Design Intent)

- **Operational Resilience:** Design target — 99.9% uptime through automated failover and recovery
- **Integration Assurance:** Design target — Cross-agent stress testing prevents production failures
- **Vendor Risk Management:** Design target — Third-party risk monitoring prevents supply-chain compromise
- **Hefaistos Sunset Execution:** Design target — Structured, milestone-driven decommission with zero data loss; completion October 2029
- **Lifecycle Governance:** Design target — Controlled deployment, monitoring, update, and deprecation of all 30 agents

### I.3 Regulatory Anchors

- **UU PDP 27/2022:** Data processor governance; vendor DPA requirements; breach notification within 72 hours
- **GCG.01/GCG.02:** Vendor integrity; third-party risk management; anti-corruption in procurement
- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Business continuity obligations; employee notification for system changes
- **ISO 27001 / ISO 22301:** Information security and business continuity standards (external certification target Phase 7)

---

## Section II: Structural Breakdown (WHAT)

### II.1 Core Components

#### C1: Agent Lifecycle Governance Engine
- **Lifecycle Stages:** Design → Develop → Test → Deploy → Monitor → Update → Deprecate → Retire
- **Deployment Orchestration:** 4-phase deployment (Staging → Pilot → Production → Validation) per P5-W4
- **Version Control:** Semantic versioning for all 30 agents; dependency matrix tracking
- **Rollback Protocol:** Automated rollback to last known good version on failure detection
- **Performance Monitoring:** Real-time latency, throughput, error rate, resource utilization per agent
- **Health Score:** 0–100 per agent; auto-escalation when < 70 for > 15 minutes

#### C2: Cross-Agent Stress Testing Engine
- **Integration Test Suite:** 500+ automated test cases covering all agent-to-agent invocation paths
- **Load Testing:** Simulates 10× peak load to identify bottlenecks
- **Chaos Engineering:** Randomly terminates agents to test resilience and failover
- **Data Consistency Validation:** Verifies data integrity across agent boundaries after transactions
- **Regression Testing:** Full suite execution before any agent version update
- **Pass Criteria:** 99.5% test pass rate required for production deployment

#### C3: Disaster Recovery Orchestrator
- **RTO (Recovery Time Objective):** ≤ 4 hours for Tier 1 agents; ≤ 8 hours for Tier 2; ≤ 24 hours for Tier 3
- **RPO (Recovery Point Objective):** ≤ 15 minutes data loss for all agents
- **Backup Automation:** Continuous incremental backup; daily full backup; weekly offsite replication
- **Failover Automation:** Hot standby for Tier 1; warm standby for Tier 2; cold standby for Tier 3
- **DR Drill Scheduler:** Quarterly automated DR drills with full recovery validation
- **BCP Integration:** Links to enterprise Business Continuity Plan; HR-specific continuity procedures

#### C4: Vendor Governance & Third-Party Risk Monitor
- **Vendor Registry:** All third-party vendors (cloud, AI models, data providers, integrations)
- **SLA Monitoring:** Real-time tracking of vendor uptime, latency, error rates against contracted SLAs
- **Risk Scoring:** 0–100 vendor risk score based on security, financial stability, compliance, concentration
- **DPA Validation:** Ensures all vendors have valid Data Processing Agreements per UU PDP 27/2022
- **Breach Response:** Auto-triggers incident response when vendor breach detected
- **Concentration Risk:** Flags when > 30% of agents depend on single vendor

#### C5: Legacy System Sunset Manager (Hefaistos Decommission — Target October 2029)
- **Decommission Roadmap:** Milestone-driven plan from May 2026 to October 2029 (42 months)
- **Data Migration Orchestration:** Coordinates P4-W1 payroll migration, P3-W5 legacy mapping, P2-W3 data fabric cutover
- **Parallel Operation Validation:** Ensures 99.9% data consistency between Hefaistos and new agents during transition
- **User Transition Management:** Training schedule, access migration, support desk transition
- **Sunset Gate Checklist:** 50-item checklist for each decommission phase; all gates must pass
- **Rollback Plan:** Maintains Hefaistos read-only fallback for 90 days post-cutover (through January 2030)

### II.2 Workflow Architecture

```
[Trigger: Deployment / Update / Test / DR / Vendor Alert / Hefaistos Milestone]
    ↓
[C1: Agent Lifecycle] → Stage management + version control + deployment orchestration
    ↓
[HC-106: AI Governance Board Approval] → Major deployment authorization
    ↓
[C2: Stress Testing] → Integration tests + load tests + chaos engineering + regression
    ↓
[Pass Rate ≥ 99.5%?]
    ├─ YES → Proceed to deployment
    └─ NO → Block deployment; generate remediation plan
    ↓
[C3: Disaster Recovery] → Backup + failover + DR drill + BCP integration
    ↓
[C4: Vendor Governance] → SLA monitoring + risk scoring + DPA validation + breach response
    ↓
[Vendor Risk Score > 70?]
    ├─ YES → [HC-107: CHRO + DPO Review] → Vendor mitigation plan
    └─ NO → Continue
    ↓
[C5: Hefaistos Sunset] → Migration orchestration + parallel validation + user transition + sunset gates
    ↓
[Hefaistos Gate Pass?]
    ├─ YES → Proceed to next phase
    └─ NO → Halt decommission; remediation required
    ↓
[Output: Resilience & Lifecycle Dashboard]
```

---

## Section III: Operational Guidance (HOW)

### III.1 Trigger Conditions

1. **Deployment Request:** Auto-triggers on new agent or version update submission
2. **Monthly Stress Test:** Auto-triggers first Sunday of each month
3. **Quarterly DR Drill:** Auto-triggers first Saturday of quarter
4. **Vendor SLA Breach:** Auto-triggers when vendor SLA < 99.5% for > 1 hour
5. **Hefaistos Milestone:** Auto-triggers on scheduled decommission phase date
6. **Agent Health Alert:** Auto-triggers when any agent health score < 70 for > 15 minutes
7. **Integration Failure:** Auto-triggers when cross-agent invocation fails > 3× in 10 minutes

### III.2 Input Requirements

- All 30 agent specifications and version metadata
- Vendor contracts, SLAs, and DPAs
- Hefaistos system architecture and data schema
- Enterprise BCP and DR policies
- Infrastructure monitoring data (CPU, memory, network, storage)
- Security incident feeds

### III.3 Processing Logic

**Agent Lifecycle:**
- Validate deployment request against dependency matrix
- Execute 4-phase deployment (Staging → Pilot → Production → Validation)
- Monitor performance post-deployment for 72 hours
- Auto-rollback on failure detection

**Stress Testing:**
- Execute 500+ integration test cases
- Run 10× load simulation
- Execute chaos engineering (random agent termination)
- Validate data consistency across boundaries
- Generate pass/fail report; block deployment if < 99.5%

**Disaster Recovery:**
- Execute quarterly DR drill with full recovery
- Validate RTO and RPO compliance
- Test failover automation
- Update BCP documentation

**Vendor Governance:**
- Monitor all vendor SLAs in real-time
- Calculate vendor risk scores monthly
- Validate DPA currency quarterly
- Auto-trigger incident response on breach

**Hefaistos Sunset:**
- Execute decommission roadmap milestones (target completion October 2029)
- Coordinate data migration across P4-W1, P3-W5, P2-W3
- Validate parallel operation consistency
- Manage user transition and training
- Enforce sunset gate checklist (50-item)
- Maintain 90-day rollback window post-cutover (October 2029 – January 2030)

### III.4 Output Deliverables

- **Agent Health Dashboard:** Real-time health scores, performance metrics, alert status for all 30 agents
- **Stress Test Report:** Test coverage, pass rate, failure analysis, remediation recommendations
- **DR Drill Report:** RTO/RPO compliance, recovery validation, improvement recommendations
- **Vendor Risk Scorecard:** All vendor risk scores, SLA compliance, DPA status, concentration alerts
- **Hefaistos Sunset Tracker:** Milestone status, gate pass/fail, migration progress, risk items (target October 2029)
- **Incident Response Log:** All vendor breaches, agent failures, recovery actions

---

## Section IV: Structured Output Templates

### Template 1: Agent Health Dashboard

```yaml
dashboard_id: "AHD-{date}"
generated_at: "YYYY-MM-DD HH:MM"
overall_ecosystem_health: 0–100
agent_health_scores:
  - agent: "P1"
    health_score: 0–100
    status: "HEALTHY / DEGRADED / CRITICAL / DOWN"
    latency_ms: N
    error_rate: "X%"
    last_deployment: "YYYY-MM-DD"
    version: "vX.Y.Z"
  - agent: "P2"...
active_alerts:
  - agent: "[code]"
    severity: "WARNING / CRITICAL"
    description: "[narrative]"
    triggered_at: "YYYY-MM-DD HH:MM"
    auto_action: "[rollback / failover / escalation]"
```

### Template 2: Hefaistos Sunset Gate Checklist

```yaml
gate_id: "HSG-{phase}-{nnnn}"
phase: "DATA_MIGRATION / PARALLEL_OPERATION / USER_TRANSITION / CUTOVER / POST_CUTOVER"
gate_status: "PASS / FAIL / PENDING"
target_completion_date: "YYYY-MM-DD"
final_cutover_target: "2029-10-31"
checklist_items:
  - item: "[description]"
    status: "PASS / FAIL / NA"
    evidence: "[reference]"
    owner: "[role]"
    completed_at: "YYYY-MM-DD HH:MM"
migration_metrics:
  records_migrated: N
  consistency_check: "PASS / FAIL"
  user_training_completion: "X%"
  support_ticket_volume: N
rollback_readiness: "CONFIRMED / NOT_READY"
rollback_window_end: "2030-01-31"
next_phase_authorization: "APPROVED / DENIED"
```

---

## Section V: Reference Bank (Polytron-Specific Anchors)

### V.1 Polytron Context

- **Hefaistos Decommission:** October 2029 target (per v1.1 Roadmap); 42-month execution window from May 2026
- **HRD Web Sunset:** Parallel decommission with Hefaistos; coordinated through P6-W5
- **Employer of Choice 2030:** System reliability is a key EVP pillar; downtime impacts culture
- **GCG Framework:** Vendor integrity (GCG.02); business ethics in technology procurement
- **Zero Pension Extension 2030:** Payroll continuity critical; P4-W1 + P6-W5 ensure zero disruption

### V.2 Indonesian Regulatory Anchors

- **UU PDP 27/2022:** Vendor DPA requirements; breach notification within 72 hours; data processor accountability
- **GCG.01:** Technology governance; system integrity; access control
- **GCG.02:** Vendor selection integrity; anti-corruption in procurement
- **UU Cipta Kerja (UU 6/2023 amending UU 13/2003):** Employee notification for system changes affecting work processes

### V.3 Industry Standards

- **ISO 27001:** Information security management system (Phase 7 certification target)
- **ISO 22301:** Business continuity management system (Phase 7 certification target)

---

## Section VI: Quality Checklist

| ID | Check | Verification |
|---|---|---|
| Q-161 | YAML frontmatter with triggers | Schema validation |
| Q-162 | 10-section structure | Section count |
| Q-163 | Mandatory rules (M-161 to M-180) | Rule inventory |
| Q-164 | Strict Prohibitions (SP-161 to SP-180) | Prohibition inventory |
| Q-165 | Bilingual output | Language tag |
| Q-166 | Polytron and regulatory references | Reference count |
| Q-167 | Integration with ALL 29 prior agents | Dependency map |
| Q-168 | HITL checkpoints (HC-106 to HC-110) | Checkpoint count |
| Q-169 | Audit trail completeness | Log verification |
| Q-170 | Cross-wave consistency | Pattern matching |
| Q-171 | Stress test 500+ case coverage | Test count |
| Q-172 | 99.5% pass rate enforcement | Pass rate check |
| Q-173 | DR drill RTO/RPO validation | Recovery check |
| Q-174 | Vendor risk score calculation | Score verification |
| Q-175 | Hefaistos 50-item gate checklist | Checklist coverage |
| Q-176 | Agent health score 0–100 validation | Score range |
| Q-177 | Chaos engineering execution | Test validation |
| Q-178 | Concentration risk > 30% flag | Threshold check |
| Q-179 | DPA validation quarterly | Compliance check |
| Q-180 | Sunset rollback plan maintenance | Plan verification |

---

## Section VII: Integration Points

### VII.1 Upstream Dependencies

- **P1 HR Master Orchestrator:** Receives agent health data; routes lifecycle workflows
- **P5-W3 Board HR Dashboard:** Consumes ecosystem health and resilience metrics
- **P5-W4 Regulatory Scanner:** Receives vendor compliance alerts
- **All 29 Agents:** Provide health, performance, and version data

### VII.2 Downstream Dependencies

- **P2 Ethical Guardrail:** Screens all lifecycle and resilience outputs
- **P4-W1 Payroll:** Receives Hefaistos migration coordination
- **P3-W5 Job Architecture:** Receives legacy mapping migration coordination
- **P2-W3 People Analytics Hub:** Receives data fabric cutover coordination
- **P5-W2 AI Ethics:** Receives agent update bias audit requests

### VII.3 Lateral Dependencies

- **IT/Infrastructure:** Hardware, network, cloud resources
- **Procurement:** Vendor contracts, SLAs, DPAs
- **DPO:** Data protection compliance, breach response
- **External Audit:** Annual resilience and compliance audit (ISO 27001 / 22301)

---

## Section VIII: Governance & Enforcement

### VIII.1 Mandatory Rules (P6-W5: M-161 to M-180)

| ID | Rule |
|---|---|
| M-161 | P6-W5 MUST monitor health score for all 30 agents in real-time |
| M-162 | P6-W5 MUST execute cross-agent stress testing monthly with 500+ test cases |
| M-163 | P6-W5 MUST enforce 99.5% pass rate for all production deployments |
| M-164 | P6-W5 MUST maintain RTO ≤ 4 hours (Tier 1), ≤ 8 hours (Tier 2), ≤ 24 hours (Tier 3) |
| M-165 | P6-W5 MUST maintain RPO ≤ 15 minutes for all agents |
| M-166 | P6-W5 MUST execute quarterly DR drills with full recovery validation |
| M-167 | P6-W5 MUST calculate vendor risk score monthly for all third-party vendors |
| M-168 | P6-W5 MUST validate DPA currency quarterly for all vendors |
| M-169 | P6-W5 MUST flag concentration risk when > 30% of agents depend on single vendor |
| M-170 | P6-W5 MUST auto-trigger incident response within 15 minutes of vendor breach detection |
| M-171 | P6-W5 MUST maintain Hefaistos decommission roadmap with monthly milestone tracking (target October 2029) |
| M-172 | P6-W5 MUST enforce 50-item sunset gate checklist for each decommission phase |
| M-173 | P6-W5 MUST maintain Hefaistos rollback capability for 90 days post-cutover (through January 2030) |
| M-174 | P6-W5 MUST require HC-106 (AI Governance Board) for all major agent deployments |
| M-175 | P6-W5 MUST require HC-107 (CHRO + DPO) for vendor risk scores > 70 |
| M-176 | P6-W5 MUST generate bilingual (ID + EN) incident and DR reports |
| M-177 | P6-W5 MUST maintain semantic versioning for all 30 agents |
| M-178 | P6-W5 MUST execute chaos engineering quarterly |
| M-179 | P6-W5 MUST validate data consistency across all agent boundaries |
| M-180 | P6-W5 MUST maintain audit trail for all lifecycle, DR, and vendor activities |

### VIII.2 Strict Prohibitions (P6-W5: SP-161 to SP-180)

**Note:** SP-172 below has been customized (de-templatized from v1.0) to reflect P6-W5's specific risk surface — lifecycle, resilience, and vendor decisions affecting all 30 agents.

| ID | Prohibition |
|---|---|
| SP-161 | P6-W5 MUST NEVER deploy agent to production with < 99.5% stress test pass rate |
| SP-162 | P6-W5 MUST NEVER ignore agent health score < 70 for > 15 minutes |
| SP-163 | P6-W5 MUST NEVER skip quarterly DR drill |
| SP-164 | P6-W5 MUST NEVER deploy vendor without valid DPA |
| SP-165 | P6-W5 MUST NEVER ignore vendor SLA breach > 1 hour |
| SP-166 | P6-W5 MUST NEVER proceed with Hefaistos cutover without gate checklist completion |
| SP-167 | P6-W5 MUST NEVER delete Hefaistos data before Migration Integrity Certificate (P4-W1) |
| SP-168 | P6-W5 MUST NEVER bypass HC-106 for major deployments |
| SP-169 | P6-W5 MUST NEVER operate without automated backup |
| SP-170 | P6-W5 MUST NEVER share vendor risk details with unauthorized personnel |
| SP-171 | P6-W5 MUST NEVER ignore concentration risk > 30% |
| SP-172 | P6-W5 MUST NEVER release lifecycle decisions, resilience reports, or vendor risk findings without P2 Ethical Guardrail's ecosystem-level integrity and confidentiality screen |
| SP-173 | P6-W5 MUST NEVER auto-execute Hefaistos decommission without human gate approval |
| SP-174 | P6-W5 MUST NEVER store vendor credentials in plain text |
| SP-175 | P6-W5 MUST NEVER ignore security incident > 15 minutes without response |
| SP-176 | P6-W5 MUST NEVER deploy without rollback plan validated |
| SP-177 | P6-W5 MUST NEVER skip data consistency validation post-recovery |
| SP-178 | P6-W5 MUST NEVER allow single point of failure for Tier 1 agents |
| SP-179 | P6-W5 MUST NEVER ignore UU PDP 27/2022 breach notification requirements (72 hours) |
| SP-180 | P6-W5 MUST NEVER cite Hefaistos decommission target other than October 2029 in any operational communication |

### VIII.3 HITL Checkpoints (P6-W5: HC-106 to HC-110)

| ID | Checkpoint | Authority | Trigger |
|---|---|---|---|
| HC-106 | Major agent deployment authorization | AI Governance Board | Production deployment request |
| HC-107 | High vendor risk mitigation approval | CHRO + DPO | Vendor risk score > 70 |
| HC-108 | DR drill validation and sign-off | CDO + HR Director | Quarterly DR drill completion |
| HC-109 | Hefaistos decommission phase gate | CHRO + CFO + IT Director | Phase milestone reached |
| HC-110 | Incident response escalation | CHRO + CEO | Critical security or vendor breach |

---

## Section IX: Success Metrics (KPIs)

| KPI | Target | Measurement |
|---|---|---|
| Ecosystem Uptime | ≥ 99.9% | Monitoring |
| Agent Health Score Average | ≥ 90 across all 30 agents | Real-time |
| Stress Test Pass Rate | ≥ 99.5% | Monthly |
| DR Drill RTO Compliance | 100% within targets | Quarterly |
| DR Drill RPO Compliance | 100% within targets | Quarterly |
| Vendor Risk Score Average | ≤ 50 across all vendors | Monthly |
| DPA Compliance | 100% current | Quarterly |
| Concentration Risk Flags | 0 unresolved | Monthly |
| Hefaistos Decommission On-Track | 100% milestones on schedule (target completion October 2029) | Monthly |
| Security Incident Response Time | ≤ 15 minutes | Incident tracking |
| Deployment Rollback Rate | ≤ 2% | Deployment tracking |
| Chaos Engineering Recovery | 100% auto-recovery | Quarterly |

---

## Section X: Version Control

| Version | Date | Changes | Author |
|---|---|---|---|
| v1.0 | May 2026 | Initial Wave 6 design — closes Tier 1 (75%→100%); Hefaistos target stated as October 2028 | Enterprise HR AI Architecture Team |
| v1.1 | May 2026 | SP-172 and SP-180 de-templatized; Hefaistos target corrected to October 2029 (aligned with 42-month phased plan); maturity framing reframed | Enterprise HR AI Architecture Team |

---

# ============================================================
# WAVE 6 CONSOLIDATED GOVERNANCE INDEX
# ============================================================

## Wave 6 HITL Checkpoints (HC-89 to HC-110)

| Wave | HITL Range | Count | Primary Authority |
|---|---|---|---|
| P6-W1 | HC-89 to HC-90 | 2 | TA Head, HR Director |
| P6-W2 | HC-91 to HC-95 | 5 | Manager, Calibration Council, OD Lead, HR Director |
| P6-W3 | HC-96 to HC-100 | 5 | C&B Head, HRBP, HR Director, CFO |
| P6-W4 | HC-101 to HC-105 | 5 | Manager, HRBP, Payroll Manager, HR Director, TA Head |
| P6-W5 | HC-106 to HC-110 | 5 | AI Governance Board, CHRO, DPO, CFO, IT Director |
| **Wave 6 Total** | **HC-89 to HC-110** | **22** | |
| **Waves 1–5 Total** | **HC-1 to HC-88** | **88** | |
| **Grand Total** | **HC-1 to HC-110** | **110** | |

**Verification:** 2 + 5 + 5 + 5 + 5 = 22 ✓ ; 22 + 88 = 110 ✓

## Wave 6 Mandatory Rules (M-106 to M-180)

| Agent | Range | Count |
|---|---|---|
| P6-W1 | M-106 to M-115 | 10 |
| P6-W2 | M-116 to M-130 | 15 |
| P6-W3 | M-131 to M-145 | 15 |
| P6-W4 | M-146 to M-160 | 15 |
| P6-W5 | M-161 to M-180 | 20 |
| **Wave 6 Total** | **M-106 to M-180** | **75** |
| **Waves 1–5 Total** | **M-1 to M-105** | **105** |
| **Grand Total** | **M-1 to M-180** | **180** |

**Verification:** 10 + 15 + 15 + 15 + 20 = 75 ✓ ; 75 + 105 = 180 ✓

## Wave 6 Strict Prohibitions (SP-106 to SP-180)

| Agent | Range | Count |
|---|---|---|
| P6-W1 | SP-106 to SP-115 | 10 |
| P6-W2 | SP-116 to SP-130 | 15 |
| P6-W3 | SP-131 to SP-145 | 15 |
| P6-W4 | SP-146 to SP-160 | 15 |
| P6-W5 | SP-161 to SP-180 | 20 |
| **Wave 6 Total** | **SP-106 to SP-180** | **75** |
| **Waves 1–5 Total** | **SP-1 to SP-105** | **105** |
| **Grand Total** | **SP-1 to SP-180** | **180** |

**Verification:** 10 + 15 + 15 + 15 + 20 = 75 ✓ ; 75 + 105 = 180 ✓

**Note (v1.1):** 5 Strict Prohibitions (SP-115, SP-125, SP-140, SP-155, SP-172) have been de-templatized from v1.0 to reflect each agent's specific risk surface, rather than carrying identical boilerplate text. The total count of 180 is preserved.

## Wave 6 Quality Checklist (Q-101 to Q-180)

| Agent | Range | Count |
|---|---|---|
| P6-W1 | Q-101 to Q-115 | 15 |
| P6-W2 | Q-116 to Q-130 | 15 |
| P6-W3 | Q-131 to Q-145 | 15 |
| P6-W4 | Q-146 to Q-160 | 15 |
| P6-W5 | Q-161 to Q-180 | 20 |
| **Wave 6 Total** | **Q-101 to Q-180** | **80** |
| **Waves 1–5 Total** | **Q-1 to Q-100** | **100** |
| **Grand Total** | **Q-1 to Q-180** | **180** |

**Verification:** 15 + 15 + 15 + 15 + 20 = 80 ✓ ; 80 + 100 = 180 ✓

---

# ============================================================
# POST-WAVE 6 DESIGN COMPLETION SUMMARY
# ============================================================

**Mandatory framing change from v1.0:** This section was titled "POST-WAVE 6 SYSTEM MATURITY — 100% CERTIFICATION" in v1.0. It has been retitled and reframed to reflect that what Wave 6 achieved is **specification completeness**, not operational maturity. Operational maturity will be earned through the phased deployment in the companion v1.1 Roadmap.

## Final Specification Coverage Dashboard

| Module | Post-W5 Coverage | Post-W6 Coverage | Change | Status |
|---|---|---|---|---|
| **Tier 1 — Orchestration** | 75% | **100%** | +25pp | Specification Complete |
| **M01 — Strategic Workforce Planning** | 92% | **100%** | +8pp | Specification Complete |
| **M02 — Talent Acquisition & EB** | 88% | **100%** | +12pp | Specification Complete |
| **M03 — Onboarding & EX** | 96% | **100%** | +4pp | Specification Complete |
| **M04 — Learning & Development** | 92% | **100%** | +8pp | Specification Complete |
| **M05 — Performance Management** | 75% | **100%** | +25pp | Specification Complete |
| **M06 — Succession Management** | 85% | **100%** | +15pp | Specification Complete |
| **M07 — Organization Development** | 78% | **100%** | +22pp | Specification Complete |
| **M08 — Compensation & Benefits** | 80% | **100%** | +20pp | Specification Complete |
| **M09 — HR Operations & Payroll** | 92% | **100%** | +8pp | Specification Complete |
| **M10 — Compliance, GCG & ER** | 94% | **100%** | +6pp | Specification Complete |
| **M11 — Offboarding & Alumni** | 70% | **100%** | +30pp | Specification Complete |
| **M12 — People Analytics** | 91% | **100%** | +9pp | Specification Complete |
| **TOTAL** | **~85% (weighted)** | **100% specification coverage** | | **Design-Complete** |

**Strict Prohibition:** This dashboard measures specification scope coverage only. No claim of operational maturity, production readiness, or business outcome achievement shall be made on the basis of this dashboard.

## Complete 30-Agent Architecture

| Wave | Agents | Lines | Status |
|---|---|---|---|
| Wave 1 | 5 | ~4,060 | Design-Complete (v1.1) |
| Wave 2 | 5 | ~3,020 | Design-Complete (v1.0) |
| Wave 3 | 5 | ~3,750 | Design-Complete (v1.1) |
| Wave 4 | 5 | ~3,920 | Design-Complete (v1.1) |
| Wave 5 | 5 | ~5,450 | Design-Complete (v1.0) |
| Wave 6 | 5 | ~2,480 | Design-Complete (v1.1) |
| **TOTAL** | **30** | **~22,680** | **Design-Complete** |

## Governance Index Grand Total

| Index | Waves 1–5 | Wave 6 | Grand Total |
|---|---|---|---|
| HITL Checkpoints | 88 (HC-1 to HC-88) | 22 (HC-89 to HC-110) | **110** |
| Mandatory Rules | 105 (M-1 to M-105) | 75 (M-106 to M-180) | **180** |
| Strict Prohibitions | 105 (SP-1 to SP-105) | 75 (SP-106 to SP-180) | **180** |
| Quality Items | 100 (Q-1 to Q-100) | 80 (Q-101 to Q-180) | **180** |

---

## DOCUMENT CONTROL STATEMENT

> **This document (v1.1) provides the design specification for Wave 6 of the Polytron Enterprise HR Agentic AI Architecture, comprising five agents (P6-W1 through P6-W5) that complete specification coverage for the 30-agent ecosystem. The five agent specifications are technically sound and ready for engineering implementation review.**
>
> **Strict Prohibition:** This document shall not be cited as evidence of operational maturity, production readiness, or system certification. What is certified here is **Design Completeness only**. Operational maturity will be earned through the 42-month phased deployment plan in the companion `POLYTRON_HR_AI_IMPLEMENTATION_ROADMAP_v1_1.md`, with Hefaistos decommission targeted for **October 2029**.
>
> **Mandatory:** All regulatory citations herein are pending verification by Legal Counsel prior to Phase 1 kickoff (per v1.1 Roadmap Appendix D).
>
> **Status:** Design-Complete
> **Hefaistos Decommission Target:** October 2029
> **Companion Documents:** v2.1 Final Consolidation; v1.1 Implementation Roadmap
> **Next Action:** Board HR Committee review; engineering implementation team mobilization; Legal Counsel regulatory verification

---

## DOCUMENT METADATA

| Attribute | Value |
|---|---|
| **Document ID** | POLYTRON-HR-AI-WAVE6-2026-v1.1 |
| **Document Type** | Wave 6 Design Specification (audit-reconciled) |
| **Classification** | INTERNAL |
| **Date** | May 2026 |
| **Owner** | CHRO Office |
| **Previous Version** | v1.0 (May 2026) — superseded due to 9 audit findings |
| **Current Version** | v1.1 |
| **Total Agents Specified (Suite)** | 30 (25 Waves 1–5 + 5 Wave 6) |
| **Wave 6 Agents Specified** | 5 (P6-W1, P6-W2, P6-W3, P6-W4, P6-W5) |
| **Total Specification Lines (Suite)** | ~22,680 |
| **Specification Coverage** | 100% (30/30 agents) |
| **Operational Maturity** | To be earned through phased deployment (v1.1 Roadmap) |
| **HITL Checkpoints (Wave 6)** | 22 (HC-89 to HC-110) |
| **Mandatory Rules (Wave 6)** | 75 (M-106 to M-180) |
| **Strict Prohibitions (Wave 6)** | 75 (SP-106 to SP-180); 5 de-templatized in v1.1 |
| **Quality Items (Wave 6)** | 80 (Q-101 to Q-180) |
| **Hefaistos Decommission Target** | October 2029 |
| **Companion Documents** | POLYTRON_HR_AI_WAVES_1-6_FINAL_CONSOLIDATION_v2_1.md; POLYTRON_HR_AI_IMPLEMENTATION_ROADMAP_v1_1.md |
| **Distribution List** | Board HR Committee; CEO; CHRO; CFO; CDO; HR Director; DPO; Ethics Officer; Engineering Implementation Team |
| **Next Review** | November 2026 (post Phase 1 Gate 1) |
| **Supersedes** | v1.0 (May 2026) |

---

*End of Wave 6 — Completion & Integration Design Specification v1.1*

---

**Document Version:** v1.1
**Classification:** INTERNAL — Board HR Committee & Engineering Implementation Team
**Owner:** CHRO Office, Polytron HR
**Next Review:** November 2026 (post Phase 1 Gate 1)
**Distribution:** Per Board HR Committee and Engineering recipient matrix
