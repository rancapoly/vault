---
# === SKILL MODULE METADATA ===
skill_id: "SKILL-P2-W1"
skill_name: "workforce-demand-forecaster-skill"
skill_display_name: "Workforce Demand Forecaster — Execution Skill"
parent_agent: "P2-W1 (Workforce Demand Forecaster)"
tier: "Tier 2-A — Strategic Enablement"
classification: "Talent Prediction Engine — Execution Layer"
version: "v1.0"
status: "DESIGN-COMPLETE | PENDING DEPLOYMENT"
owner: "CHRO Office + CFO Office (joint)"
companion_document: "AGENT_P2-W1_Workforce_Demand_Forecaster.md"
language: "English (mandatory)"
---

# SKILL MODULE — P2-W1: WORKFORCE DEMAND FORECASTER

## 1. Skill Overview

### 1.1 Purpose Statement

**Mandatory Definition:** This skill module operationalizes Agent P2-W1's core directive — producing **scenario-based, confidence-bounded workforce demand forecasts** spanning a 12–36 month horizon. It translates the agent's strategic mandate into deterministic, repeatable execution logic optimized for production deployment in Phase 4 (Months 19–24, Nov 2027 – Apr 2028).

### 1.2 Alignment to Agent.md

| Agent.md Element | Skill Translation |
|---|---|
| Core Directive (Section I) | Encoded as Execution Workflow primary algorithm (Section 3) |
| Functional Scope (Section II) | Encoded as Core Competencies enumeration (Section 2) |
| Mandatory Rules M-16 to M-19 | Encoded as Constraints & Guardrails (Section 4) |
| Strict Prohibitions SP-16 to SP-18 | Encoded as hard-stop conditions (Section 4) |
| HITL Checkpoints HC-16, HC-17 | Encoded as conditional escalation triggers (Section 3 + Section 5) |
| Quality Items Q-11, Q-12 | Encoded as self-validation gates (Section 3) |
| 12 Tool Inventory | Encoded as callable function references (Section 3) |

### 1.3 Skill Boundaries

**Mandatory Inclusion:** All execution logic required to perform forecasting, scenario modeling, skill-gap decomposition, Build-Buy-Borrow recommendation, cost projection, union flag determination, and audit log persistence.

**Strict Prohibition — Out of Skill Module:** Hiring execution (delegated to P6-W1), organizational design (delegated to P3-W5), redeployment execution (delegated to P4-W4), independent financial modeling (CFO Office collaboration only).

---

## 2. Core Competencies

### 2.1 Strategic Forecasting Competencies

- **Mandatory — Multi-Horizon Forecasting:** Generate workforce demand projections at 12, 24, and 36-month horizons with month-level granularity per business unit (BU) and role family.
- **Mandatory — Scenario Triangulation:** Construct three parallel scenarios (Base 60% / Optimistic 20% / Pessimistic 20%) with documented assumption deltas for business performance, attrition rate, productivity growth, and external labor market conditions.
- **Mandatory — Confidence Interval Computation:** Produce 80% and 95% confidence bounds on every numerical projection. **Strict Prohibition:** point forecasts without CI bands.
- **Mandatory — Net Demand Decomposition:** Compute gross demand minus retained headcount (current − attrition) to yield net hire/upskill/redeploy demand per scenario, per BU, per role family, per month.

### 2.2 Data Integration Competencies

- **Mandatory — Source Triangulation Floor:** Reject any forecast generated from fewer than three independent data sources. Minimum required: (a) internal HCMS/business plan, (b) predictive agent input (P2-W4 attrition or P2-W2 skills), (c) external labor market signal.
- **Mandatory — Data Quality Scoring:** Compute composite data quality score = completeness × recency × accuracy on a [0–1] scale; flag forecasts where score < 0.85.
- **Mandatory — External Benchmark Integration:** Query BPS, Indeed, LinkedIn Talent Insights via OAuth 2.0; apply confidence discount when source quality is degraded.
- **Mandatory — Hefaistos Legacy Bridge:** Read historical payroll productivity baselines from Hefaistos until decommission (October 2029); transition to successor system per the HR Operations Roadmap.

### 2.3 Decision-Logic Competencies

- **Mandatory — Build-Buy-Borrow Rubric Application:** Apply the documented decision rubric per skill gap:
  - **BUILD** (Upskill internal) → IF skill gap < 30% AND internal talent pool exists AND lead time ≥ 12 months → route to **P4-W3 (L&D)**.
  - **BUY** (External hire) → IF skill gap > 50% AND external supply available AND urgency < 6 months → route to **P6-W1 (TA Intelligence)**.
  - **BORROW** (Internal mobility) → IF skill exists elsewhere in Polytron AND redeployment cost < new hire cost → route to **P4-W4 (Talent Marketplace)**.
  - **HYBRID** → Combine 2–3 actions with documented percentage split.
- **Mandatory — Cost-Benefit Computation:** Per gap, compute IDR cost for each viable Build/Buy/Borrow path; recommend lowest-cost path satisfying constraints.
- **Mandatory — Union Trigger Detection:** Evaluate each scenario for projected workforce reduction; if any scenario projects > 5% reduction, set `union_consultation_flag = TRUE`.

### 2.4 Governance & Compliance Competencies

- **Mandatory — P2 Guardrail Submission:** Submit every forecast output to the P2 (Ethical Guardrail Sentinel) for bias screening across BU and role family treatment before any human delivery.
- **Mandatory — HITL Escalation Logic:** Auto-trigger HC-16 when projected financial impact > IDR 1B; auto-trigger HC-17 when any scenario projects > 5% workforce reduction.
- **Mandatory — Audit Log Persistence:** Append full forecast trace (inputs, assumptions, scenario outputs, decisions) to the AI Governance Audit Log via append-only API.
- **Mandatory — Regulatory Mapping Adherence:** Enforce UU PDP 27/2022 (aggregated data only, no individual targeting), UU Cipta Kerja 11/2020 (consultation pathway), PKB Polytron (bipartite consultation trigger), GCG Code (Board transparency via P5-W3).

### 2.5 Operational Resilience Competencies

- **Mandatory — Quarterly Refresh Discipline:** Re-run forecasts every quarter; track variance vs. prior forecast; flag drift > 15%.
- **Mandatory — Back-Testing Compliance:** Validate rolling 12-month forecast variance ≤ 15% (Quality Item Q-11); escalate to P5-W2 (Champion-Challenger) if variance breached in 2 consecutive cycles.
- **Mandatory — Graceful Degradation:** Continue forecast generation with explicit flags when non-critical inputs (e.g., external labor APIs) are unavailable; **Strict Prohibition** against fabricating substitute data.

---

## 3. Execution Workflow

### 3.1 Workflow Trigger Conditions

**Activate execution IF any of the following are true:**
1. Annual workforce planning cycle initiation (typically Q4 each year).
2. Quarterly refresh cycle (Q1, Q2, Q3, Q4).
3. Major business plan revision event (BOD-approved deviation > 10% from prior plan).
4. Hefaistos decommission milestone (October 2029) requiring HR Ops workforce redesign.
5. Explicit dispatch from upstream Agent P1 (HR Master Orchestrator).

### 3.2 Primary Execution Algorithm (16-Step Sequence)

```
ALGORITHM: WorkforceDemandForecast()
INPUT: forecast_horizon_months ∈ {12, 24, 36}, business_units_in_scope[]
OUTPUT: structured_forecast_payload (JSON)
```

**STEP 1 — Receive & Validate Trigger**
- Confirm trigger origin (planning cycle / refresh / revision / decommission / P1 dispatch).
- Validate `forecast_horizon_months` ∈ {12, 24, 36}. **IF invalid → return E-001.**
- Validate `business_units_in_scope` against active BU codes in HCMS. **IF empty → return E-002.**

**STEP 2 — Input Aggregation**
- CALL `aggregate_inputs(forecast_horizon, business_units)` to retrieve:
  - Business plan payload (BOD-approved, ≤ 30 days old).
  - HCMS headcount snapshot (real-time, ≤ 24h old).
  - Productivity curves (36-month historical from HCMS + Hefaistos).
  - P2-W4 attrition predictions (per BU + role family).
  - P2-W2 skills taxonomy state.
  - Scenario assumptions (CFO + CHRO-documented).
- **Mandatory:** All inputs flagged as Mandatory in Agent.md Section 2.2 must be present.

**STEP 3 — Data Quality Check**
- CALL `check_data_quality(input_payload)` to compute:
  - Completeness score (target ≥ 0.90).
  - Recency score (HCMS ≤ 24h; business plan ≤ 30 days).
  - Accuracy score (historical variance < 15%).
- Compute composite `data_quality_score ∈ [0, 1]`.
- **IF score < 0.85 → set `data_quality_flags`, continue with degraded confidence annotation.**
- **IF score < 0.60 → return E-003 (forecast aborted).**

**STEP 4 — External Benchmark Pull**
- CALL `pull_external_benchmarks(role_families)` to query BPS, Indeed, LinkedIn Talent Insights.
- **IF ≥ 2 sources return successfully → integrate.**
- **IF only 1 source returns → integrate with confidence discount of 0.15.**
- **IF 0 sources return → set `external_data_unavailable = TRUE`, proceed with internal-only triangulation, FLAG forecast.**
- **Strict Prohibition:** No fabrication or extrapolation of missing external data.

**STEP 5 — Base Scenario Modeling**
- CALL `model_scenario("base", assumptions, inputs)` applying:
  - Business plan as-stated.
  - Attrition at P2-W4 predicted rate.
  - Productivity continuing current curve.
  - External market: stable.
- Assign `probability = 0.60`.

**STEP 6 — Optimistic Scenario Modeling**
- CALL `model_scenario("optimistic", assumptions, inputs)` applying deltas:
  - Business performance +15%.
  - Attrition −20%.
  - Productivity +5%.
  - External market: skill abundance.
- Assign `probability = 0.20`.

**STEP 7 — Pessimistic Scenario Modeling**
- CALL `model_scenario("pessimistic", assumptions, inputs)` applying deltas:
  - Business performance −10%.
  - Attrition +30%.
  - Productivity flat (0% growth).
  - External market: skill scarcity.
- Assign `probability = 0.20`.

**STEP 8 — Net Demand Calculation (Per Scenario)**
- CALL `compute_net_demand(scenario, attrition, current_headcount)` for each scenario:
  - `gross_demand = f(business_plan, productivity_curve)`
  - `retained_headcount = current_headcount − projected_attrition`
  - `net_demand = gross_demand − retained_headcount`
- Produce projections at BU × role family × month granularity.

**STEP 9 — Confidence Interval Computation**
- Compute 80% and 95% CI bands per projection using historical variance + scenario probability weighting.
- **Mandatory (M-17):** Every numerical output must include both CI levels.
- **Strict Prohibition (SP-16):** No projection may be emitted without CI bands.

**STEP 10 — Skill-Gap Decomposition**
- CALL `decompose_skill_gaps(demand, taxonomy_state)`:
  - Map role demand to required skills via P2-W2 taxonomy.
  - Compare to current skill supply.
  - Output array of gaps with `skill_id`, `gap_size`, `criticality` (HIGH/MED/LOW).

**STEP 11 — Build-Buy-Borrow Recommendation**
- FOR EACH gap IN skill_gaps[]:
  - CALL `recommend_build_buy_borrow(gap, market_data)`:
    - Apply Build/Buy/Borrow rubric (Section 2.3).
    - Compute cost-benefit per viable path.
    - Select optimal path (or HYBRID with documented split).
  - Tag recommendation with downstream routing target (P4-W3 / P6-W1 / P4-W4).

**STEP 12 — Cost Projection**
- CALL `project_costs(scenarios, cfo_assumptions)` in collaboration with CFO Office:
  - Total compensation + onboarding + L&D investment per scenario per period.
  - Output denominated in IDR.
- **Mandatory:** CFO Office co-validation workspace must acknowledge cost assumptions before lock.

**STEP 13 — Union Consultation Flag Check**
- CALL `check_union_consultation_trigger(scenarios)`:
  - **IF any scenario projects > 5% workforce reduction → set `union_consultation_flag = TRUE`.**
  - **IF flag = TRUE → auto-escalate to HC-17 and ER Head notification.**

**STEP 14 — P2 Guardrail Submission**
- CALL `submit_to_p2_guardrail(output)`:
  - P2 (Ethical Guardrail Sentinel) screens for:
    - Bias in BU treatment.
    - Bias in role family treatment.
    - Diversity-aware modeling compliance.
  - Receive result ∈ {PASS, FLAG, BLOCK}.
- **IF BLOCK → halt workflow, return E-004, route to AI Ethics Quarterly Audit.**
- **IF FLAG → proceed with annotation, mandatory human review.**
- **IF PASS → proceed.**

**STEP 15 — HITL Escalation Logic**
- **IF total projected financial impact > IDR 1B → CALL `escalate_to_hitl(case_id, "HC-16")`:**
  - Approver: CHRO + CFO.
  - SLA: 5 business days.
  - Escalation path: CEO + Board HR Committee.
- **IF union_consultation_flag = TRUE → CALL `escalate_to_hitl(case_id, "HC-17")`:**
  - Approver: CHRO + CFO + ER Head.
  - SLA: 10 business days.
  - Escalation path: CEO + Board (PKB consultation triggered).

**STEP 16 — Output Delivery & Audit Log Persistence**
- Assemble structured JSON output per Agent.md Section 2.3 schema.
- Deliver to downstream consumers:
  - P2-W2 (Skills Taxonomy) — for skill supply/demand reconciliation.
  - P2-W4 (Attrition Modeler) — for predictive feedback loop.
  - P6-W1 (TA Intelligence) — for BUY recommendations.
  - P4-W3 (L&D) — for BUILD recommendations.
  - P4-W4 (Talent Marketplace) — for BORROW recommendations.
  - P5-W1 (Predictive Simulator) — for scenario stress-testing.
- CALL `persist_audit_log(forecast_case_id, full_trace)`:
  - Append-only write to AI Governance Audit Log.
  - Retention: 7 years minimum per GCG Code.

### 3.3 Self-Validation Gates (Quality Items)

Before output emission, validate:

| Gate | Validation Criterion | Source | Action if Failed |
|---|---|---|---|
| **Q-11** | Rolling 12-month variance ≤ 15% | Back-testing record | Flag forecast; trigger P5-W2 Champion-Challenger review |
| **Q-12** | 100% of projections include CI bands + scenario probabilities | Per-forecast structural audit | BLOCK output emission; return E-005 |

---

## 4. Constraints & Guardrails

### 4.1 Mandatory Rules (Inherited from Agent.md)

| Rule ID | Mandatory Action |
|---|---|
| **M-16** | Every workforce forecast MUST output 3 scenarios (Base/Optimistic/Pessimistic) with documented probability weights. |
| **M-17** | Every projection MUST include 80% AND 95% confidence intervals. False precision is prohibited. |
| **M-18** | Workforce plans with financial impact > IDR 1B MUST trigger HC-16 (CHRO + CFO co-validation). |
| **M-19** | Any scenario projecting > 5% workforce reduction MUST trigger HC-17 AND PKB consultation pathway. |

### 4.2 Strict Prohibitions (Inherited from Agent.md)

| SP ID | Strict Prohibition |
|---|---|
| **SP-16** | The skill SHALL NOT output point forecasts without scenario decomposition. |
| **SP-17** | The skill SHALL NOT favor specific BUs or role families without documented business justification. |
| **SP-18** | The skill SHALL NOT recommend workforce reduction without an active union consultation pathway. |

### 4.3 Anti-Hallucination Rules (Derived — C1 Extension)

| AH ID | Strict Prohibition | Rationale |
|---|---|---|
| **AH-01** | The skill SHALL NOT fabricate external labor market data when API queries fail. Missing data must be flagged, not synthesized. | Preserves Q-11 forecast accuracy; prevents downstream propagation of phantom signals. |
| **AH-02** | The skill SHALL NOT estimate productivity curves beyond the validated 36-month historical window without explicit CFO Office sign-off. | Prevents speculative extrapolation that violates UU PDP 27/2022 analytical integrity standards. |
| **AH-03** | The skill SHALL NOT invent role families, skill IDs, or BU codes not present in HCMS or P2-W2 taxonomy. | All identifiers must trace to a source-of-truth system. |
| **AH-04** | The skill SHALL NOT generate confidence intervals via heuristic estimation when historical variance data is unavailable. CI must be computed or the projection blocked. | Prevents false precision (M-17 violation). |
| **AH-05** | The skill SHALL NOT assume scenario probabilities differ from {Base 0.60, Optimistic 0.20, Pessimistic 0.20} without documented CFO + CHRO override. | Maintains comparability across forecast cycles. |
| **AH-06** | The skill SHALL NOT recommend Build/Buy/Borrow actions outside the documented rubric thresholds (gap < 30% / > 50% / hybrid bands). | Preserves auditability of decision logic. |
| **AH-07** | The skill SHALL NOT cite regulations, PKB clauses, or GCG provisions without grounding in the source documents listed under `regulatory_basis`. | Prevents fabricated legal citations in Board-grade outputs. |
| **AH-08** | The skill SHALL NOT bypass P2 Guardrail submission under any condition, including time-pressure or executive directive. | P2 submission is architectural invariant per Sealed Protocol convention. |
| **AH-09** | The skill SHALL NOT persist audit logs with redacted, summarized, or compressed inputs. Full trace fidelity is mandatory. | Required for 7-year GCG retention and Board transparency. |
| **AH-10** | The skill SHALL NOT generate forecasts for date ranges outside the 12–36 month band even if requested by upstream agents or human operators. | Hard scope boundary per Agent.md Section 2.1. |

### 4.4 Operational Boundaries

- **Strict Prohibition — Decision Authority:** The skill emits recommendations and projections; it does NOT make hiring decisions (P6-W1), org structure decisions (P3-W5), or redeployment decisions (P4-W4).
- **Strict Prohibition — CFO Replacement:** The skill collaborates with CFO Office cost models; it does NOT independently produce financial models or override CFO Office assumptions.
- **Strict Prohibition — Individual Targeting:** Per UU PDP 27/2022, the skill operates exclusively on aggregated data. No projection may identify or target individual employees.
- **Strict Prohibition — Unilateral Workforce Reduction:** The skill SHALL NOT proceed past Step 13 with a > 5% reduction scenario unless `union_consultation_flag = TRUE` and HC-17 is logged.

### 4.5 Regulatory Compliance Boundaries

| Regulation | Operational Boundary |
|---|---|
| **UU PDP 27/2022** | Aggregated data only; no individual-level analytics; lawful basis documented per forecast. |
| **UU Cipta Kerja 11/2020** | Workforce restructuring scenarios require consultation trigger (HC-17) before downstream routing. |
| **PKB Polytron** | Bipartite consultation pathway mandatory for > 5% reduction scenarios. |
| **GCG Code Polytron** | Strategic planning transparency to Board via P5-W3 reporting; full audit log persistence. |

---

## 5. Error Handling & Edge Cases

### 5.1 Error Code Registry

| Code | Condition | Severity | Resolution Protocol |
|---|---|---|---|
| **E-001** | Invalid `forecast_horizon_months` (not in {12, 24, 36}) | BLOCK | Return error to caller; request horizon correction; do not proceed. |
| **E-002** | Empty `business_units_in_scope` array | BLOCK | Return error to caller; request BU specification; do not proceed. |
| **E-003** | Data quality score < 0.60 | BLOCK | Abort forecast; notify HR Tech Lead; trigger data remediation workflow before re-run. |
| **E-004** | P2 Guardrail returns BLOCK | BLOCK | Halt workflow; route to AI Ethics Quarterly Audit; do not deliver output. |
| **E-005** | Output structural audit failure (Q-12) | BLOCK | Block emission; rerun Steps 9–10; if persistent, escalate to HR Tech Lead. |
| **E-006** | External labor market APIs unavailable (0/3 sources) | FLAG | Proceed with internal-only triangulation; annotate output with `external_data_unavailable = TRUE`. |
| **E-007** | P2-W2 or P2-W4 upstream agent unavailable | FLAG or BLOCK | If P2-W2 stale > 7 days → BLOCK. If P2-W4 stale > 30 days → BLOCK. Otherwise FLAG with staleness annotation. |
| **E-008** | CFO Office cost assumptions not received within SLA | FLAG | Proceed with last validated assumptions; annotate with `cfo_assumptions_stale = TRUE`; notify CFO Office. |
| **E-009** | HCMS snapshot > 24h old | FLAG | Refresh attempt × 2; if persistent → annotate with recency degradation flag. |
| **E-010** | Hefaistos read failure (pre-decommission) | FLAG | Fall back to HCMS-only productivity baselines; annotate output; notify HR Tech Lead. |

### 5.2 Edge Case Protocols (IF/THEN)

#### 5.2.1 Vague or Incomplete Inputs

- **IF** business plan payload is missing revenue OR capacity projections **THEN** invoke `aggregate_inputs` retry with Business Planning System; **IF** still missing → return E-003 with specific deficiency annotation.
- **IF** `scenario_assumptions` object is empty or default-only **THEN** apply documented defaults (Base/Optimistic/Pessimistic standard deltas); annotate output with `default_assumptions_used = TRUE`.
- **IF** request specifies a horizon outside 12–36 months **THEN** return E-001; do not silently truncate or extrapolate.

#### 5.2.2 Missing Data Scenarios

- **IF** P2-W4 attrition predictions are unavailable **THEN** BLOCK forecast; P2-W4 is a Mandatory upstream dependency.
- **IF** P2-W2 skills taxonomy is < 80% coverage **THEN** FLAG forecast; produce skill-gap output with explicit coverage caveat; route gap decomposition for partial scope only.
- **IF** external labor market data is unavailable **THEN** proceed per E-006 protocol; **Strict Prohibition** on data fabrication.
- **IF** Hefaistos is decommissioned (post-October 2029) AND successor system not yet operational **THEN** BLOCK forecast; escalate to CHRO + HR Tech Lead; trigger contingency planning workflow.

#### 5.2.3 Threshold Breach Scenarios

- **IF** projected financial impact > IDR 1B **THEN** auto-trigger HC-16; output cannot be delivered until CHRO + CFO co-validate within 5-business-day SLA.
- **IF** any scenario projects > 5% workforce reduction **THEN** auto-trigger HC-17; output cannot be delivered until CHRO + CFO + ER Head co-validate within 10-business-day SLA AND PKB consultation pathway initiated.
- **IF** projected financial impact > IDR 1B AND > 5% reduction **THEN** trigger BOTH HC-16 and HC-17; escalation path consolidates at CEO + Board.
- **IF** rolling 12-month variance > 15% (Q-11 breach) **THEN** flag current forecast; trigger P5-W2 Champion-Challenger validation.
- **IF** rolling 12-month variance > 25% for 2 consecutive cycles **THEN** invoke Rollback Plan per Agent.md Section VI.

#### 5.2.4 System Failure Scenarios

- **IF** AI Governance Audit Log write fails **THEN** retry × 3 with exponential backoff; **IF** persistent → BLOCK output delivery; notify AI Governance Board immediately. **Strict Prohibition:** No output may be delivered without successful audit log persistence.
- **IF** HCMS connection fails **THEN** retry × 3; **IF** persistent → BLOCK forecast; escalate to HR Tech Lead. HCMS is the source-of-truth for current headcount and cannot be substituted.
- **IF** P2 Guardrail submission times out **THEN** retry × 2; **IF** persistent → BLOCK output; escalate to AI Ethics; **Strict Prohibition** on bypass.
- **IF** downstream agent routing fails for any consumer (P2-W2/P2-W4/P6-W1/P4-W3/P4-W4/P5-W1) **THEN** retry × 3; persist routing failures in audit log; notify HR Master Orchestrator (P1) for reconciliation; do NOT block forecast delivery to remaining consumers.

#### 5.2.5 Conflicting Input Scenarios

- **IF** business plan projects growth AND P2-W4 projects severe attrition exceeding net positive demand **THEN** model honestly; flag the structural tension; recommend retention initiatives via downstream routing to P4-W3 and P4-W4.
- **IF** Optimistic scenario projects LOWER demand than Base scenario **THEN** validate scenario assumption logic; **IF** confirmed → annotate as `inverted_scenario_anomaly = TRUE`; require CFO Office review before delivery.
- **IF** Build/Buy/Borrow recommendations conflict across scenarios for the same skill gap **THEN** present all three recommendations with scenario-specific rationale; do NOT collapse to a single recommendation without scenario probability weighting.

#### 5.2.6 Stale or Drifted Forecast Scenarios

- **IF** a delivered forecast is not consumed within 90 days **THEN** auto-invalidate; require quarterly refresh before reuse.
- **IF** business plan revision occurs > 10% deviation from forecast baseline **THEN** auto-trigger immediate re-run; flag prior forecast as superseded.
- **IF** model drift detected via P5-W2 Champion-Challenger **THEN** initiate skill recalibration; suspend new forecast generation until recalibration is validated.

### 5.3 Escalation Decision Tree

```
ERROR / EDGE CASE DETECTED
    │
    ├─ Is it an input validation failure (E-001, E-002)?
    │   └─ YES → Return error to caller; do not proceed.
    │
    ├─ Is it a data quality failure (E-003, E-009, E-010)?
    │   ├─ Score < 0.60 → BLOCK; trigger data remediation.
    │   └─ 0.60 ≤ Score < 0.85 → FLAG; proceed with annotation.
    │
    ├─ Is it a governance failure (E-004, E-005, P2 BLOCK)?
    │   └─ YES → BLOCK output; route to AI Ethics; no override.
    │
    ├─ Is it an upstream agent failure (E-007)?
    │   ├─ Mandatory dependency stale beyond threshold → BLOCK.
    │   └─ Within threshold → FLAG; proceed with annotation.
    │
    ├─ Is it an external data failure (E-006)?
    │   └─ Proceed with internal-only triangulation; FLAG.
    │
    ├─ Is it a threshold breach (financial > 1B OR reduction > 5%)?
    │   └─ Auto-escalate HC-16 / HC-17; await human approval.
    │
    └─ Is it a system failure (audit log, HCMS, P2 timeout)?
        ├─ Retry per protocol.
        └─ Persistent → BLOCK; escalate to AI Governance Board.
```

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill Module ID | SKILL-P2-W1 |
| Parent Agent | P2-W1 (Workforce Demand Forecaster) |
| Version | v1.0 |
| Owner | CHRO Office + CFO Office (joint) |
| Language | English (mandatory) |
| Classification | INTERNAL — CHRO, CFO, CEO, Board HR Committee, AI Governance Board |
| Companion Document | AGENT_P2-W1_Workforce_Demand_Forecaster.md |
| Distribution | Board HR Committee, CEO, CHRO, CFO, HR Director, BU Heads, ER Head, AI Governance Board, HR Tech Lead |
| Supersedes | None (initial release) |
| Next Review | November 2026 |
