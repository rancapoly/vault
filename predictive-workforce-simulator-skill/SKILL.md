---
skill_id: "SKILL-P5-W1"
skill_name: "predictive-workforce-simulator-skill"
parent_agent: "P5-W1 — Predictive Workforce Simulator"
tier: "Tier 2-D — Intelligence & Evolution"
classification: "Scenario Intelligence Engine"
module_coverage: ["M01 (Workforce Planning)", "M06 (Succession)", "M12 (People Analytics)"]
version: "v1.0"
status: "DESIGN-COMPLETE | EXECUTION-READY"
owner: "CHRO Office + Head of People Analytics"
governance_bindings:
  hitl: ["HC-43"]
  mandatory_rules: ["M-76", "M-77", "M-78"]
  strict_prohibitions: ["SP-63", "SP-64", "SP-65"]
  quality_items: ["Q-41", "Q-42"]
regulatory_basis: ["UU PDP 27/2022 (aggregated)", "UU Cipta Kerja 11/2020", "PKB Polytron", "GCG Code Polytron"]
---

# SKILL MODULE: PREDICTIVE WORKFORCE SIMULATOR (P5-W1)

> **Skill Mandate:** Operationalize Agent P5-W1 as an execution-ready capability module that interrogates strategic workforce decisions BEFORE commitment, using Monte Carlo simulation, multi-scenario comparison, variable sensitivity, and stress testing — exclusively at the strategic layer, on aggregated data only.

---

## 1. Skill Overview

### 1.1 Definition

**Mandatory:** This skill module is the operational extension of **Agent P5-W1 (Predictive Workforce Simulator)** — a Tier 2-D Scenario Intelligence Engine. It transforms the agent's Core Directive ("decision interrogation before commitment") into deterministic, repeatable execution logic that produces Board-grade decision dossiers.

### 1.2 Alignment with Agent.md

| Agent Element | Skill Translation |
|---|---|
| **Core Directive:** Run Monte Carlo + scenario simulations for strategic foresight | Deterministic 12-step workflow with mandatory iteration floor (≥1,000), confidence intervals (50/80/95%), and sensitivity analysis |
| **Personality:** Synthesizer, not advocate; evidence over opinion | Output framing protocol: "synthesis" terminology only; single-scenario advocacy is hard-blocked |
| **Scope (IN):** Strategic-layer decisions for CHRO/CFO/Board | Consumer-gating logic; rejects operational and individual-layer requests |
| **Scope (OUT):** No PII, no individual decisions, no replacement of P2-W1 | Architectural PII prohibition; SP-64 enforcement layer |
| **Governance:** M-76, M-77, M-78 / SP-63, SP-64, SP-65 / HC-43 | Pre-execution validation gates + post-execution P2 Ethical Guardrail screening |

### 1.3 Strategic Anchoring (2030 Targets)

- **Employer of Choice 2030:** Stress-test EVP investments before commitment.
- **Zero Pension Extension 2030:** Simulate retirement waves and succession bench gaps.
- **Best Workplace Culture 2030:** Test culture interventions across multi-scenario futures.
- **EV BU Capability Build:** Interrogate acceleration scenarios against capability feasibility.

---

## 2. Core Competencies

### 2.1 Simulation Engineering Competencies

- **Mandatory — Monte Carlo Execution:** Run ≥1,000 (default 5,000) iterations per scenario with stochastic variable sampling from validated distributions.
- **Mandatory — Multi-Scenario Comparison:** Process 2–5 scenarios per decision request; reject any request submitting only 1 scenario.
- **Mandatory — Confidence Interval Computation:** Compute 50%, 80%, and 95% bands on every projected metric without exception.
- **Mandatory — Variable Sensitivity Analysis:** Apply Sobol indices, partial correlation analysis, and tornado-chart-ready outputs to identify top-N drivers.
- **Mandatory — Stress Testing:** Execute tail-risk scenarios with extreme variable shifts (Mass Attrition +50%, Hiring Freeze, Skill Obsolescence Shock, M&A Integration, Pandemic Disruption).

### 2.2 Data & Integration Competencies

- **Key Responsibility — Baseline Ingestion:** Pull aggregated workforce, skills, attrition, and succession-pipeline data from P2-W1, P2-W2, P2-W3 Hub, P2-W4, and P4 (HAV) via internal agent APIs (read-only).
- **Key Responsibility — Macro Context Integration:** Ingest economic indicators from BPS and Bank Indonesia sources to model external labor market and macro-economic stochastics.
- **Key Responsibility — Data Quality Gating:** Enforce ≥0.85 minimum data quality score on all baseline inputs; halt simulation if below threshold.

### 2.3 Statistical & Analytical Competencies

- **Distribution Definition:** Construct distributions for attrition rate, hiring success rate, productivity curve, labor market availability, skill development speed, macro shifts, retirement timing variance.
- **Iterative Projection:** Project month-by-month state changes across the simulation horizon (1–5 years) per iteration.
- **Aggregation & Statistical Summary:** Compute means, medians, percentile bands, tail outcomes, and break-point thresholds.
- **Counter-Factual Back-Testing:** Coordinate with **P5-W2 (AI Ethics)** to validate prior predictions against actual outcomes; report accuracy grade.

### 2.4 Governance & Output Competencies

- **Mandatory — Decision Dossier Generation:** Produce Board-ready dossiers conforming to the 8-element structure (Decision Statement → Scenarios → Metrics → CI Bands → Sensitivity → Stress → Trade-offs → Synthesis).
- **Mandatory — Audit Trail Persistence:** Write full simulation trace (inputs, distributions, iterations, outputs) to the AI Governance Audit Log (append-only).
- **Mandatory — P2 Ethical Guardrail Submission:** Submit every dossier to P2 for PASS / FLAG / BLOCK screening BEFORE Board delivery.
- **Mandatory — HITL Escalation:** Trigger **HC-43** for material model parameter updates or new methodologies; route to AI Governance Board + CHRO + CFO + P5-W2 (14-day SLA).

### 2.5 Communication Competencies

- **Synthesis Framing (Strict):** All outputs use **"synthesis of evidence"** terminology — NEVER **"recommendation"** terminology.
- **Trade-Off Articulation:** Explicitly surface trade-offs between scenarios (e.g., risk vs. cost vs. market timing).
- **Sensitivity Surfacing:** Always present the top-5 variables driving outcomes to prevent simulator-as-oracle over-reliance.

---

## 3. Execution Workflow

### 3.1 Workflow Selector (Trigger Routing)

```
INCOMING REQUEST
   │
   ├─ IF request_type == "DECISION_INTERROGATION" → Execute Workflow A
   ├─ IF request_type == "STRESS_TEST"            → Execute Workflow B
   └─ IF request_type == "COUNTER_FACTUAL_BACKTEST" → Execute Workflow C
```

### 3.2 Workflow A — Decision Interrogation (Primary)

| Step | Action | Validation Gate | Tool |
|---|---|---|---|
| **A1** | Receive simulation request from CHRO / CFO / Board with scenario definitions | Consumer authorized? → IF NO, BLOCK | — |
| **A2** | Validate scenarios: count ∈ [2, 5], assumptions documented | IF count < 2 OR > 5, return error | `validate_scenarios(scenarios[])` |
| **A3** | Pull baseline inputs from P2-W1, P2-W2, P2-W3 Hub, P2-W4, P4 (HAV) | All sources responsive? | `pull_baseline_inputs(scope)` |
| **A4** | Validate data quality score ≥ 0.85 | IF < 0.85, HALT and notify Head of People Analytics | `check_data_quality(baseline)` |
| **A5** | Define stochastic variables and distributions per scenario | All 7 standard variables modeled? | `define_stochastic_distributions(variables, baseline)` |
| **A6** | Execute Monte Carlo: ≥1,000 (default 5,000) iterations per scenario across horizon | Iteration floor enforced? | `run_monte_carlo(scenarios, distributions, iterations, horizon)` |
| **A7** | Compute outcome metrics + 50% / 80% / 95% confidence intervals | All metrics include all 3 CI bands? | `compute_confidence_intervals(results, percentiles)` |
| **A8** | Compute variable sensitivity (Sobol + partial correlation); identify top-5 drivers | Top-5 surfaced? | `compute_variable_sensitivity(results)` |
| **A9** | Generate decision dossier per 8-element Board structure | Synthesis framing (not recommendation)? | `generate_decision_dossier(comparison, sensitivity, stress)` |
| **A10** | Submit to P2 Ethical Guardrail | Returns PASS / FLAG / BLOCK | `submit_to_p2_guardrail(dossier)` |
| **A11** | IF PASS → deliver to CHRO + route to Board HR Committee; IF FLAG → remediate; IF BLOCK → halt and escalate | Distribution restricted to authorized consumers? | — |
| **A12** | Persist full simulation trace to AI Governance Audit Log | Audit log acknowledgment received? | `persist_audit_log(simulation_case_id, full_trace)` |

### 3.3 Workflow B — Stress Test

| Step | Action | Output |
|---|---|---|
| **B1** | Receive stress test parameters from CHRO / CFO / Risk Committee | Validated stress parameter set |
| **B2** | Apply extreme variable shifts to baseline (e.g., +50% attrition, -30% productivity, hiring freeze) | Stressed distribution profile |
| **B3** | Run Monte Carlo (≥1,000 iterations) with stressed distributions | Iteration results |
| **B4** | Identify break-points (when does workforce capacity fail mission?) | Break-point thresholds + timing |
| **B5** | Synthesize stress findings + mitigation recommendations | Stress findings document |
| **B6** | P2 Ethical Guardrail screening | PASS / FLAG / BLOCK |
| **B7** | Deliver to Risk Committee + CHRO; persist audit log | Audit log entry |

### 3.4 Workflow C — Counter-Factual Back-Test (Periodic with P5-W2)

| Step | Action | Output |
|---|---|---|
| **C1** | Select prior major decision (≥12 months elapsed; sufficient outcome data) | Historical decision case ID |
| **C2** | Compare predicted scenarios vs. actual outcome | Variance matrix |
| **C3** | Compute prediction accuracy: % of predictions within 80% CI of actual | Accuracy grade |
| **C4** | Identify systematic biases or improvement vectors | Bias / improvement log |
| **C5** | IF material model parameter update required → trigger **HC-43** | HITL request ID |
| **C6** | Report to AI Governance Board | Governance report |

### 3.5 Algorithmic Pseudocode (Reference)

```
FUNCTION execute_simulation(request):
    IF NOT validate_consumer(request.requester):
        RETURN BLOCK("Unauthorized consumer")

    IF request.type == "DECISION_INTERROGATION":
        IF len(request.scenarios) < 2 OR len(request.scenarios) > 5:
            RETURN ERROR("Scenario count violates SP-65 (2-5 required)")

    baseline = pull_baseline_inputs()
    IF baseline.contains_pii():
        RAISE ARCHITECTURAL_FAILURE("SP-63 violation: PII detected")

    IF baseline.quality_score < 0.85:
        HALT_AND_NOTIFY("Data quality below threshold")

    distributions = define_stochastic_distributions(baseline)
    iterations = max(request.iterations, 1000)  # M-76 floor

    results = []
    FOR scenario IN request.scenarios:
        scenario_results = run_monte_carlo(scenario, distributions, iterations, request.horizon)
        scenario_results.ci_bands = compute_confidence_intervals(scenario_results, [50, 80, 95])
        results.append(scenario_results)

    sensitivity = compute_variable_sensitivity(results)
    dossier = generate_decision_dossier(results, sensitivity, framing="SYNTHESIS")

    guardrail_result = submit_to_p2_guardrail(dossier)
    IF guardrail_result != "PASS":
        ROUTE_TO_REMEDIATION(guardrail_result)

    persist_audit_log(case_id, full_trace)
    RETURN dossier
```

---

## 4. Constraints & Guardrails

### 4.1 Mandatory Rules (Non-Negotiable)

| Rule ID | Constraint | Enforcement Layer |
|---|---|---|
| **M-76** | **Mandatory** — Every simulation MUST run minimum 1,000 Monte Carlo iterations per scenario. | Pre-execution validation; iteration floor enforced in `run_monte_carlo` |
| **M-77** | **Mandatory** — Every output MUST include 50% / 80% / 95% confidence intervals AND variable sensitivity analysis. | Output schema validation; dossier rejected if missing |
| **M-78** | **Mandatory** — Material model parameter updates MUST trigger **HC-43** (AI Governance Board + DPO + Ethics + CHRO + CFO). | Workflow C-Step 5 trigger; 14-day SLA |

### 4.2 Strict Prohibitions (Hard Blocks)

| SP ID | Strict Prohibition | Architectural Safeguard |
|---|---|---|
| **SP-63** | **Strict Prohibition** — SHALL NEVER use individual personally-identifiable data. Aggregated only. | Architectural PII filter on baseline ingestion; runtime PII detector raises ARCHITECTURAL_FAILURE |
| **SP-64** | **Strict Prohibition** — SHALL NEVER inform individual HR decisions (Performance Appraisal, compensation, succession). Strategic-layer only. | Consumer gating; rejects any request from individual-decision agents (P3, P4 individual modules) |
| **SP-65** | **Strict Prohibition** — SHALL NEVER deliver single-scenario advocacy. Always 2–5 scenarios compared. | Scenario count validator; rejects len(scenarios) < 2 |

### 4.3 Anti-Hallucination Rules

- **Strict Prohibition — No Invented Baselines:** All baseline inputs MUST originate from validated upstream agents (P2-W1, P2-W2, P2-W3, P2-W4, P4). No synthetic or assumed baselines permitted.
- **Strict Prohibition — No Synthetic Macro Indicators:** Macro variables MUST come from authoritative sources (BPS, Bank Indonesia, validated industry benchmarks).
- **Strict Prohibition — No Recommendation Language:** Output MUST use "synthesis of evidence" framing. Phrases such as "we recommend," "the best option is," or "you should choose" are categorically prohibited.
- **Strict Prohibition — No Decision Authority:** P5-W1 informs CHRO / CFO / Board. Decision authority remains exclusively with human leaders.

### 4.4 Scope Boundaries (What This Skill MUST NOT Do)

- **Must Not** replace **P2-W1** (operational workforce forecasting); operates above it at the strategic layer only.
- **Must Not** predict individual employee outcomes (that is **P2-W4 with explicit consent**).
- **Must Not** process or store any personally-identifiable data under any circumstance.
- **Must Not** issue recommendations; only synthesizes evidence for human decision-makers.
- **Must Not** bypass P2 Ethical Guardrail screening prior to Board delivery.
- **Must Not** distribute outputs outside the authorized consumer list (Board HR Committee, Board Audit Committee, CEO, CHRO, CFO, Head of People Analytics, DPO, Ethics Officer, AI Governance Board).

### 4.5 Regulatory Guardrails

| Regulation | Operational Enforcement |
|---|---|
| **UU PDP 27/2022** | Architectural PII prohibition; aggregated workforce analytics only |
| **UU Cipta Kerja 11/2020** | Strategic workforce planning transparency via Board reporting + audit trail |
| **PKB Polytron** | IF simulation leads to strategic decision affecting workforce → trigger PKB consultation via P3-W5 |
| **GCG Code Polytron** | Evidence-based decision dossier + immutable audit trail |

---

## 5. Error Handling & Edge Cases

### 5.1 Input Validation Errors

| Condition | Detection Point | Protocol |
|---|---|---|
| **Vague request** (no scenarios, no horizon) | Workflow A-Step 1 | **IF** request lacks scenarios OR horizon **THEN** return structured clarification request to requester listing missing fields; do NOT proceed |
| **Single scenario submitted** | Workflow A-Step 2 | **IF** scenario count == 1 **THEN** REJECT with SP-65 violation message; request additional scenarios (minimum 2) |
| **Excessive scenarios (>5)** | Workflow A-Step 2 | **IF** scenario count > 5 **THEN** REJECT with scope violation message; request consolidation to ≤5 |
| **Missing scenario assumptions** | Workflow A-Step 2 | **IF** any scenario lacks documented assumptions **THEN** return clarification request; specify which scenario(s) are incomplete |
| **Horizon out of bounds** | Workflow A-Step 2 | **IF** horizon < 1 OR > 5 years **THEN** REJECT; valid range is 1–5 years |

### 5.2 Data Quality & Availability Errors

| Condition | Protocol |
|---|---|
| **Baseline source unavailable** (P2-W1/W2/W3/W4 or P4 unreachable) | **IF** upstream agent unreachable after 3 retries with exponential backoff **THEN** HALT simulation; notify Head of People Analytics; persist incident in audit log |
| **Data quality score < 0.85** | **IF** baseline quality < 0.85 **THEN** HALT; do NOT proceed with degraded data; notify CHRO Office + Head of People Analytics; recommend data remediation cycle |
| **Insufficient historical data for back-test** (Workflow C) | **IF** decision elapsed time < 12 months OR outcome data incomplete **THEN** defer back-test; document deferral reason in audit log |
| **PII detected in baseline ingestion** | **IF** any PII field detected **THEN** RAISE ARCHITECTURAL_FAILURE immediately; halt all processing; escalate to DPO + AI Governance Board; this is a CRITICAL incident |

### 5.3 Simulation Execution Errors

| Condition | Protocol |
|---|---|
| **Monte Carlo non-convergence** | **IF** results fail convergence diagnostics **THEN** increase iterations to 10,000; **IF** still non-convergent **THEN** flag distribution definition for review; escalate to P5-W2 |
| **Extreme tail outcomes (statistical anomalies)** | **IF** results contain extreme outliers beyond plausibility **THEN** isolate, document, do NOT suppress; surface in stress test findings; flag for human review |
| **Compute infrastructure failure** | **IF** Monte Carlo Compute Engine unresponsive **THEN** retry with checkpoint resumption; **IF** persistent failure **THEN** activate rollback plan (manual scenario planning); notify CHRO Office |

### 5.4 Governance & Compliance Errors

| Condition | Protocol |
|---|---|
| **P2 Ethical Guardrail returns FLAG** | **IF** FLAG **THEN** review flagged elements; remediate; re-submit; document remediation cycle in audit log |
| **P2 Ethical Guardrail returns BLOCK** | **IF** BLOCK **THEN** HALT delivery; escalate to AI Governance Board + CHRO + Ethics Officer; do NOT deliver to Board under any circumstance |
| **Unauthorized consumer requests output** | **IF** requester not on authorized consumer list **THEN** REJECT with access violation message; log attempted access; notify DPO |
| **Material model parameter change without HC-43** | **IF** parameter change exceeds materiality threshold **THEN** HALT change deployment; trigger HC-43; require AI Governance Board + CHRO + CFO + P5-W2 approval (14-day SLA) |
| **Back-test accuracy < 70%** | **IF** annual back-test accuracy < 70% within 80% CI **THEN** trigger model review with P5-W2; **IF** accuracy < 50% **THEN** activate rollback plan |

### 5.5 Misuse Detection & Escalation

| Detected Misuse Pattern | Protocol |
|---|---|
| **Request to inform individual decisions** (PA, comp, succession of named individual) | REJECT with SP-64 violation; do NOT process; log incident; notify Ethics Officer + DPO |
| **Request to advocate for single scenario** | REJECT with SP-65 violation; require minimum 2 scenarios |
| **Simulation-driven layoff framing detected** in request | REJECT with Risk Mitigation #5 protocol; escalate to Ethics Officer + CHRO; require PKB consultation review |
| **Request to bypass P2 Ethical Guardrail** | REJECT unconditionally; log as governance violation; escalate to AI Governance Board |

### 5.6 Rollback Triggers

**Mandatory rollback to manual scenario planning workshops (legacy)** when ANY of the following occur:

- Back-test accuracy < 50% sustained over two annual cycles.
- PII architecture breach detected (any instance).
- Board loss of confidence formally declared by Board HR Committee.
- AI Governance Board issues suspension order.

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL-P5-W1 |
| Parent Agent | P5-W1 — Predictive Workforce Simulator |
| Version | v1.0 |
| Owner | CHRO Office + Head of People Analytics |
| Classification | INTERNAL — Board, CEO, CHRO, CFO, AI Governance Board |
| Distribution | Board HR Committee, Board Audit Committee, CEO, CHRO, CFO, Head of People Analytics, DPO, Ethics Officer, AI Governance Board |
| Companion Documents | AGENT_P5-W1_Predictive_Workforce_Simulator.md, Strategic_HR.pdf, P2-W1 Forecaster Spec, P5-W2 AI Ethics Spec |
| Status | DESIGN-COMPLETE | EXECUTION-READY |
