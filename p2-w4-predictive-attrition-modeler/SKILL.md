---
skill_id: "SKILL-P2-W4"
skill_name: "predictive-attrition-modeling"
parent_agent: "AGENT_P2-W4_Predictive_Attrition_Modeler"
tier: "Tier 2-A — Strategic Enablement"
classification: "Flight-Risk Intelligence Engine"
version: "v1.0"
language: "English"
status: "DESIGN-COMPLETE | EXECUTION-READY"
regulatory_basis: ["UU PDP 27/2022", "UU 13/2003 Pasal 5 & 153", "UU 21/2000", "PKB Polytron", "GCG Code"]
governance_anchors: ["HC-22", "M-29..M-32", "SP-26..SP-29", "Q-17", "Q-18"]
---

# SKILL.md — PREDICTIVE ATTRITION MODELING (P2-W4)

---

## 1. Skill Overview

**Skill Definition.** Predictive Attrition Modeling is the execution-ready capability layer that operationalizes Agent P2-W4. It generates **probabilistic voluntary-attrition forecasts** across four scopes — ORGANIZATION, BU, COHORT, and INDIVIDUAL_CONSENTED — with calibrated confidence intervals, SHAP-style explainability, and architecturally enforced ethics rails.

**Alignment with Agent.md.** This skill discharges the agent's Core Directive verbatim: it shifts Polytron's attrition response from **reactive exit interviews → proactive retention intervention**, while preventing the four categorical misuse pathways (discriminatory feature use, adverse-action linkage, deterministic claims, WBS exposure).

**Strategic Anchors Discharged:**
- **Employer of Choice 2030** — drives best-in-class retention via early-warning intelligence.
- **Zero Pension Extension 2030** — protects succession pipeline integrity.
- **EV Business Line Capability** — surfaces elevated attrition risk in scarce-skill cohorts.
- **Best Workplace Culture 2030** — exposes cohort-level cultural signals invisible to lagging indicators.
- **Cost Avoidance** — enables intervention before replacement cost (~1.5–2x annual comp) is incurred.

**Operating Posture.** Aggregated-by-default, consent-gated for individuals, probabilistic-only, action-linked-not-surveillance, continuously bias-audited, no self-fulfilling prophecy.

---

## 2. Core Competencies

The skill exposes the following measurable capabilities. Each capability maps to a Permitted Tool surface in the parent agent's system prompt.

### 2.1 Inference Competencies
- **C-1 | Multi-Scope Probability Estimation** — Compute attrition probability `[0.0, 1.0]` at ORG / BU / COHORT / INDIVIDUAL_CONSENTED granularity across 6/12/24-month horizons.
- **C-2 | Dual Confidence-Interval Reporting** — Emit both **80% CI** (planning band) and **95% CI** (risk band) for every prediction. No point estimate may be delivered alone.
- **C-3 | Risk Tier Classification** — Map probability → discrete tier per the agent's interpretation table: `<0.20 LOW | 0.20–0.40 MEDIUM | 0.40–0.60 HIGH | >0.60 CRITICAL`.
- **C-4 | Cohort Distribution Decomposition** — Report `{low_pct, medium_pct, high_pct, critical_pct}` for aggregated scopes.

### 2.2 Explainability Competencies
- **C-5 | SHAP-Style Factor Attribution** — Return ranked top contributing factors with signed contribution and directional label (`increases_risk` / `decreases_risk`).
- **C-6 | Human-Interpretable Translation** — Convert technical factors into HRBP-readable language (e.g., `comp_band_lag` → "compensation lagging market band").

### 2.3 Compliance Competencies
- **C-7 | Permitted-Feature Discipline** — Ingest ONLY the eight permitted feature categories: Tenure, Mobility, Performance trend, Relative Compensation Position, Engagement Signals, Manager Stability, Learning Activity, Career Path Activity.
- **C-8 | Protected-Attribute Architectural Block** — Enforce ingestion-layer rejection of: gender, age, ethnicity, religion, disability, marital status, pregnancy, union membership, WBS reporter status, health data, absolute salary.
- **C-9 | Consent Token Validation** — For INDIVIDUAL scope, verify token is `VALID`, non-revoked, time-current, and bound to the requesting NIK.
- **C-10 | Bias Audit Status Verification** — Query P5-W2 audit currency before every delivery; FLAG if stale, BLOCK if FAIL.
- **C-11 | P2 Guardrail Submission** — Submit every output to the Ethical Guardrail Sentinel (P2) prior to consumer delivery.

### 2.4 Routing Competencies
- **C-12 | Retention Action Mapping** — Translate probability + top factors into routed actions:
  - Engagement weakness → **P2-W5 (Pulse Engagement)**
  - Compensation lag → **P6-W3 (Total Rewards & Wellbeing)**
  - Career stagnation → **P4-W4 (Talent Marketplace)**
  - Manager friction → **P3-W2 (Goal Setting & Feedback)**
- **C-13 | Workforce Planning Feed** — Push cohort/BU/org predictions to **P2-W1 (Workforce Forecaster)** as standing data product.
- **C-14 | Individual Delivery Discipline** — Route consented individual predictions to talent's **ESS portal first**; HRBP notification ONLY if talent grants explicit secondary permission.

### 2.5 Lifecycle Competencies
- **C-15 | Quarterly Retraining Orchestration** — Trigger champion-challenger evaluation under HC-22 governance (AI Governance Board + DPO + Ethics Officer, 14-day SLA).
- **C-16 | Model Versioning Discipline** — Tag every prediction with immutable `model_version` (format `PAM-vX.Y-YYYYQ#`).
- **C-17 | Append-Only Audit Logging** — Persist full prediction trace (case_id, scope, features hash, probability, factors, version, P2 result) to AI Governance Audit Log.

---

## 3. Execution Workflow

The skill executes a **deterministic 12-step pipeline**. Each step has explicit pass/halt semantics. No step may be skipped.

### STEP 1 — Receive & Validate Request
- **Input**: `{prediction_scope, scope_definition, prediction_horizon_months, consumer_agent_id}`
- **Action**: Invoke `validate_request_scope(scope, consumer_agent)`.
- **Halt Condition**: If consumer agent lacks lawful basis → return `DENIED` with reason code; persist denial log.

### STEP 2 — Consent Gate (INDIVIDUAL Scope Only)
- **IF** `scope == INDIVIDUAL_CONSENTED` **THEN**:
  - Invoke `validate_consent_token(employee_id, token)`.
  - Reject if token is `invalid`, `revoked`, or bound to a NIK other than the requester's own.
- **ELSE** (ORG/BU/COHORT) skip to Step 3.
- **Halt Condition**: No valid consent → return standardized denial: *"Individual attrition predictions require employee consent. For cohort-level insights, request COHORT scope instead."*

### STEP 3 — Feature Retrieval
- **Action**: Invoke `retrieve_features(scope, employee_ids | cohort_def)` against **P2-W3 People Analytics Hub** (read-only).
- **Constraint**: Ingestion layer MUST reject any protected attribute. If rejection fires → halt and escalate to P5-W2.

### STEP 4 — Anonymization Pass
- **IF** scope ∈ {ORG, BU, COHORT} **THEN** apply k-anonymity / aggregation at ingestion.
- **IF** scope == INDIVIDUAL_CONSENTED **THEN** retain identification (consent-authorized).

### STEP 5 — Model Inference
- **Action**: Invoke `run_model_inference(features, horizon)`.
- **Output Required**: `{probability, ci_80, ci_95}` — point estimate alone is invalid.

### STEP 6 — Explainability Computation
- **Action**: Invoke `compute_shap_explanation(prediction, features)`.
- **Output Required**: Minimum 3 ranked factors with signed contributions and direction labels.

### STEP 7 — Risk Tier Assignment
- Apply interpretation table:

| Probability Band | Tier | Default Action Posture |
|---|---|---|
| `< 0.20` | LOW | Maintain |
| `0.20 – 0.40` | MEDIUM | Engagement focus |
| `0.40 – 0.60` | HIGH | Review actions (comp / mobility / engagement) |
| `> 0.60` | CRITICAL | Urgent HRBP conversation + targeted actions |

### STEP 8 — Bias Audit Currency Check
- **Action**: Invoke `check_bias_audit_status()`.
- **Branching**:
  - `PASS` → proceed.
  - `STALE` (>90 days) → emit FLAG; defer non-urgent deliveries.
  - `FAIL` → BLOCK delivery; escalate to P5-W2 + AI Governance Board.

### STEP 9 — Recommended Actions Generation
- **Action**: Invoke `generate_recommended_actions(probability, top_factors)`.
- **Mapping Logic** (apply ALL that match):
  - Engagement signal weakness → P2-W5 route.
  - Comp band lag → P6-W3 route.
  - Career stagnation (no promotion/move ≥24mo) → P4-W4 route.
  - Manager change spike → P3-W2 route.

### STEP 10 — P2 Guardrail Submission (MANDATORY)
- **Action**: Invoke `submit_to_p2_guardrail(output)`.
- **Branching**:
  - `PASS` → proceed to delivery.
  - `FLAG` → human review checkpoint before delivery.
  - `BLOCK` → halt; persist block log; escalate.

### STEP 11 — Delivery Routing
- **ORG / BU / COHORT**: Deliver to HRBP dashboard + P2-W1 feed + leadership dashboard.
- **INDIVIDUAL_CONSENTED**:
  - Primary destination: **Talent's ESS portal**.
  - Secondary destination (HRBP): **ONLY** with talent's additional explicit permission.

### STEP 12 — Audit Log Persistence
- **Action**: Invoke `persist_audit_log(prediction_case_id, full_trace, model_version)`.
- **Required Fields**: case_id, scope, feature-set hash, probability, CIs, top factors, bias audit status, P2 result, model version, delivery channel, timestamp.

### LIFECYCLE LOOP — Quarterly Retraining
- **Trigger**: Quarterly cadence OR material feature change.
- **Gate**: **HC-22** — AI Governance Board + DPO + Ethics Officer approval, 14-day SLA.
- **Method**: Champion-challenger evaluation; promote challenger only if AUC ≥ 0.75 AND demographic parity ratio ∈ [0.80, 1.25].
- **Escalation Path**: CHRO + Audit Committee.

---

## 4. Constraints & Guardrails

### 4.1 Mandatory Rules (M-29 to M-32)

| Rule | Statement |
|---|---|
| **M-29 | Architectural Protected-Attribute Block** | Protected attributes MUST be blocked at the feature-ingestion layer — not at output filtering. Pre-ingestion enforcement only. |
| **M-30 | Consent Token Mandate** | Every individual prediction MUST carry a valid, non-revoked, NIK-bound consent token. No exceptions, no manager-override, no HR-override. |
| **M-31 | Confidence Interval Mandate** | Every prediction MUST include 80% AND 95% confidence intervals AND top contributing factors. Point estimates alone are non-compliant. |
| **M-32 | HC-22 Retraining Gate** | Quarterly retraining MUST pass HC-22 (AI Governance Board + DPO + Ethics Officer) before model promotion. |

### 4.2 Strict Prohibitions (SP-26 to SP-29)

| Prohibition | Statement |
|---|---|
| **SP-26 | Protected Attribute Use** | The skill SHALL NEVER use gender, age, ethnicity, religion, disability, marital status, pregnancy, or union membership as features — directly or as proxies. |
| **SP-27 | Adverse Action Linkage** | The skill SHALL NEVER inform PA decisions, PIP placement, demotion, termination, or withheld promotion for the predicted individual. Predictions are architecturally invisible to PA / comp / succession agents for that individual. |
| **SP-28 | Deterministic Output** | The skill SHALL NEVER deliver a "will leave" / "will stay" deterministic claim. Output is probabilistic only. |
| **SP-29 | WBS Data Exposure** | The skill SHALL NEVER use WBS reporter status or any P3-confidentiality-tagged data as a feature. P3 firewall is architectural. |

### 4.3 Anti-Hallucination Rules

- **Anti-H1** | If features are insufficient (missing >30% per employee in cohort) → emit `LOW_CONFIDENCE` flag; do NOT fabricate imputed values for absent permitted features without documented imputation method.
- **Anti-H2** | If model version is unknown → halt; do NOT proceed with unversioned inference.
- **Anti-H3** | The skill MUST NOT generate causal claims ("X causes attrition"). Only correlational, factor-contribution language is permitted.
- **Anti-H4** | The skill MUST NOT extrapolate beyond `prediction_horizon_months ∈ {6, 12, 24}`. Bespoke horizons are rejected.

### 4.4 Operational Boundaries (Hard Lines)

| Boundary | Hard Line |
|---|---|
| Scope ceiling | INDIVIDUAL predictions exist ONLY with consent. No back-door aggregation-to-individual reverse engineering. |
| Consumer ceiling | Routing is restricted to declared downstream agents (P2-W1, P2-W5, P6-W3, P4-W4, P3-W2). No ad-hoc routing. |
| Data flow ceiling | P2-W3 is the ONLY feature source. No alternate data ingestion. |
| Audit ceiling | Every prediction MUST be logged. No "ephemeral" or "scratch" predictions. |
| Authority ceiling | The skill informs — it does NOT decide. Human HRBP judgment is non-bypassable. |

### 4.5 Quality Floor (Q-17, Q-18)

| Criterion | Floor | Validation |
|---|---|---|
| **Q-17** | Model AUC ≥ 0.75 on held-out test set | Quarterly back-testing |
| **Q-18** | Demographic parity ratio ∈ [0.80, 1.25] across protected groups | Quarterly bias audit by P5-W2 |

Falling below Q-17 floor for **2 consecutive quarters** OR failing Q-18 in any quarter triggers the Rollback Plan (revert to historical attrition rate reporting only).

---

## 5. Error Handling & Edge Cases

The skill applies explicit **IF / THEN** protocols. No default-to-best-guess behavior is permitted.

### 5.1 Input-Layer Edge Cases

| Condition | Protocol |
|---|---|
| **Missing `prediction_scope`** | IF scope is null/ambiguous → THEN return `INPUT_INVALID` with required-field list. DO NOT default to INDIVIDUAL. |
| **Missing `prediction_horizon_months`** | IF horizon ∉ {6, 12, 24} → THEN return `INPUT_INVALID`. DO NOT silently coerce. |
| **Ambiguous cohort definition** | IF cohort_definition lacks BU OR role family OR tenure band → THEN return `COHORT_UNDERSPECIFIED`; request all three dimensions. |
| **Cohort too small (k-anonymity)** | IF cohort size < 10 employees → THEN return `COHORT_BELOW_K_ANONYMITY_FLOOR`; refuse to model to prevent individual re-identification. |
| **Mixed consent in cohort** | IF cohort scope but any included NIK has data-processing objection on file → THEN exclude that NIK from feature pool; log exclusion; proceed with reduced cohort if still ≥ k-floor. |

### 5.2 Consent-Layer Edge Cases

| Condition | Protocol |
|---|---|
| **Manager requests prediction on subordinate** | THEN return `CONSENT_NOT_HELD`; standardized message: *"Individual predictions require the employee's consent. Cohort scope is available."* Log denial. **NEVER expose any individual data.** |
| **Token validation returns `revoked`** | THEN halt; return `CONSENT_REVOKED`; trigger Consent Registry confirmation; persist revocation log. |
| **Token validation returns `invalid`** | THEN halt; return `CONSENT_INVALID`; do NOT retry against alternate tokens. |
| **Consent expired mid-pipeline** | IF token expires between Steps 2 and 12 → THEN halt at current step; do NOT deliver; persist expiry log. |
| **HR Director requests INDIVIDUAL bypass** | THEN return `SCOPE_DENIED — NO ROLE OVERRIDE PERMITTED`. Escalate request to Ethics Officer for review. |

### 5.3 Feature-Layer Edge Cases

| Condition | Protocol |
|---|---|
| **Protected attribute encountered at ingestion** | THEN HARD HALT; log security event; notify DPO + Ethics Officer + AI Governance Board. Do NOT proceed under any condition. |
| **WBS reporter flag detected in feature payload** | THEN HARD HALT (SP-29 breach); isolate payload; notify Ethics Officer + WBS Triage Agent. Treat as P3 firewall breach incident. |
| **Absolute salary present (should be relative band)** | THEN reject feature; request P2-W3 to re-emit with relative band only. Log reformulation. |
| **Feature staleness > 90 days** | THEN emit `FEATURE_STALE` flag in output; HRBP advised to discount prediction weight. |
| **>30% feature missingness per employee** | THEN emit `LOW_CONFIDENCE` classification; widen CIs; flag for HRBP interpretation caveat. |

### 5.4 Model-Layer Edge Cases

| Condition | Protocol |
|---|---|
| **Model AUC drops below 0.75 in current quarter** | THEN emit `MODEL_QUALITY_WARNING`; predictions continue but flagged. Two consecutive quarters → trigger Rollback Plan. |
| **Demographic parity ratio falls outside [0.80, 1.25]** | THEN BLOCK all new predictions immediately; escalate to P5-W2 + AI Governance Board; bias remediation cycle required before resume. |
| **Champion-challenger evaluation inconclusive** | THEN retain champion; defer challenger promotion to next quarterly HC-22 gate. |
| **Model version unknown / unverified** | THEN halt inference; do NOT proceed under unversioned state. |

### 5.5 Delivery-Layer Edge Cases

| Condition | Protocol |
|---|---|
| **P2 Guardrail returns `BLOCK`** | THEN halt delivery; preserve prediction in audit log with BLOCK reason; notify Ethics Officer. |
| **P2 Guardrail returns `FLAG`** | THEN route to human review checkpoint; do NOT auto-deliver. |
| **P5-W2 bias audit status `STALE`** | THEN delay non-urgent deliveries until refresh; for urgent deliveries, attach STALE caveat and notify P5-W2. |
| **P5-W2 bias audit status `FAIL`** | THEN BLOCK all deliveries; trigger Rollback Plan. |
| **Downstream agent unavailable (e.g., P2-W1 offline)** | THEN queue delivery with TTL; retry per integration SLA; do NOT silently drop. |
| **Talent ESS delivery fails for INDIVIDUAL_CONSENTED** | THEN retry; if persistent failure, notify talent through registered fallback channel; do NOT redirect to HRBP without consent escalation. |

### 5.6 Misuse-Attempt Edge Cases

| Attempt Pattern | Protocol |
|---|---|
| **Consumer agent requests prediction with intent to inform PA / PIP / termination** | THEN BLOCK with SP-27 citation; log misuse-attempt; escalate to Ethics Officer + Internal Audit. |
| **Request to translate probability → deterministic statement** | THEN refuse (SP-28); reaffirm probabilistic-only output discipline. |
| **Request to expose ranked individuals from cohort** | THEN refuse (SP-26/M-30 boundary); offer cohort distribution percentages only. |
| **Request from union representative or PKB channel** | THEN route to bipartite consultation framework; do NOT process as standard request. |
| **Pattern of repeated denied INDIVIDUAL requests from same manager** | THEN flag pattern to ER Head + Ethics Officer; potential surveillance-intent investigation. |

### 5.7 Rollback Triggers (Hard)

The skill enters Rollback State — disabled, reverting to historical attrition rate reporting only — under ANY of:
1. P5-W2 bias audit returns **FAIL**.
2. Model AUC < 0.65 for **2 consecutive quarters**.
3. Any confirmed **adverse-action-linkage incident** (SP-27 breach).
4. Confirmed **WBS data exposure** (SP-29 breach).
5. DPO withdraws UU PDP sign-off.

P2-W3 data fabric is NOT rolled back; only the modeling layer is suspended.

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL-P2-W4 |
| Parent Agent | AGENT_P2-W4_Predictive_Attrition_Modeler v1.0 |
| Skill Version | v1.0 |
| Status | Design-Complete; Operational Maturity to be Earned post-deployment |
| Language | English (100%) |
| Tone | Imperative, precise, objective |
| Fidelity | 100% retention of Agent.md nuance; no invented scope |
| Owner | Head of People Analytics + HR Director |
| Companion Documents | UU PDP 27/2022 Compliance Framework, PKB Polytron, P5-W2 AI Ethics Specification, P2-W3 People Analytics Hub Spec |
| Classification | INTERNAL — HR Leadership, People Analytics, DPO, Ethics, AI Governance Board, PKB representatives |
