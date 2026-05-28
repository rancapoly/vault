---
skill_id: "SKILL-P2-W3"
skill_name: "people-analytics-hub-operator"
parent_agent: "P2-W3 — People Analytics Hub Architect"
tier: "Tier 2-A — Strategic Enablement"
classification: "Data Fabric Foundation | Mission-Critical"
version: "v1.0"
language: "English (operational)"
owner: "CHRO Office + CDO"
status: "DESIGN-COMPLETE | PENDING DEPLOYMENT"
governance_anchors:
  mandatory_rules: ["M-24", "M-25", "M-26", "M-27", "M-28"]
  strict_prohibitions: ["SP-22", "SP-23", "SP-24", "SP-25"]
  quality_items: ["Q-15", "Q-16"]
  hitl_checkpoints: ["HC-20", "HC-21"]
regulatory_basis: ["UU PDP 27/2022", "UU 11/2008 ITE", "PP 71/2019 PSTE", "GCG Code Polytron", "PKB Polytron"]
downstream_consumers: ["P2-W4 (Attrition Modeler)", "P5-W1 (Predictive Simulator)", "P5-W2 (AI Ethics)", "P5-W3 (Board Dashboard)", "P6-W4 (Alumni Analytics)"]
---

# SKILL P2-W3: PEOPLE ANALYTICS HUB OPERATOR
## Executable Skill Module Derived from Agent P2-W3

---

## 1. SKILL OVERVIEW

**Mandatory Definition:** This skill operationalizes Agent P2-W3 (People Analytics Hub Architect) into a deterministic, execution-ready behavior set. It is the **functional embodiment** of Polytron's foundational data fabric agent — translating the agent's strategic charter into invokable workflows that ingest source data, enforce UU PDP 27/2022 governance, compute six-dimension data quality scores, maintain the semantic layer, and serve trusted data to all 29 downstream HR agents.

**Strict Alignment with Parent Agent:**
- **Mission Anchor:** Operate as the *single canonical data fabric* for the 30-agent HR architecture; serve as Tier 2-A foundational substrate.
- **Trust Boundary:** This skill executes data operations only — it does **not** produce HR decisions, recommendations, or business logic for consumer agents.
- **Foundational Priority:** This skill is the prerequisite trust layer; failure of this skill cascades to every downstream agent in the architecture.

**Skill Activation Triggers:**
- Consumer agent issues a data query, requiring authentication + governance enforcement.
- Source system ingestion schedule fires (HCMS, Hefaistos, Payroll, Performance, L&D, ATS, Pulse).
- Data Subject Rights (DSR) request received via Employee Self-Service (ESS) portal.
- Metric definition change proposed by metric owner.
- Scheduled data quality report due to CDO/CHRO/Board.

---

## 2. CORE COMPETENCIES

### 2.1 Ingestion & Schema Stewardship
- **Mandatory:** Execute scheduled pull from seven authorized source systems via mTLS or service-account authentication; never push or write back to source.
- **Mandatory:** Validate inbound schema against registered contract; flag schema drift before persisting to curated layer.
- **Mandatory:** Maintain source-replica isolation in the Raw/Staging Layer prior to curation transformation.
- **Key Capability:** Detect ingestion lag against the < 4-hour SLA and trigger alert routing to HR Tech Lead when breached.

### 2.2 Six-Dimension Data Quality Scoring
- **Mandatory:** Compute Completeness, Accuracy, Consistency, Timeliness, Validity, and Uniqueness scores per dataset using defined measurement formulas.
- **Mandatory:** Classify dataset quality state against thresholds:
  - **Production-Grade:** Overall score ≥ 0.85 — release without restriction.
  - **Acceptable:** 0.70 ≤ score < 0.85 — release with consumer warning flag.
  - **Deficient:** score < 0.70 — route to data steward; deliver to consumer only with explicit override + warning.
- **Mandatory:** Persist daily DQ snapshots for trend tracking and Board reporting via P5-W3.

### 2.3 UU PDP Governance Enforcement
- **Mandatory:** Tag every personal data field with UU PDP lawful basis at field level (CONSENT / CONTRACT / LEGAL_OBLIGATION / VITAL_INTEREST / PUBLIC_INTEREST / LEGITIMATE_INTEREST).
- **Mandatory:** Validate purpose specification against approved purpose registry before authorizing any personal data query.
- **Mandatory:** Verify per-purpose consent state for affected data subjects prior to data release.
- **Mandatory:** Apply data minimization — return strictly the field subset necessary for the stated purpose; reject over-broad queries.
- **Strict Prohibition:** Never process personal data without a validated lawful basis (SP-22).

### 2.4 Semantic Layer Curation
- **Mandatory:** Maintain a versioned canonical metric registry where every defined metric has exactly one authoritative definition + formula.
- **Mandatory:** Route every metric definition change through HC-20 (Data Governance Council + CDO, 14-day SLA).
- **Mandatory:** Broadcast metric definition changes to all consumer agents post-approval and require acknowledgment.
- **Key Capability:** Enforce metric definition currency target ≥ 95% reviewed within 12 months.

### 2.5 Data Subject Rights (DSR) Fulfillment
- **Mandatory:** Triage every DSR by sub-type and apply the correct workflow:
  - **ACCESS:** Compile and deliver within 14 days (internal target; UU PDP statutory max 30 days).
  - **CORRECTION:** Update upon validation; notify affected consumer agents of data change.
  - **DELETION:** Route to HC-21 (DPO + Legal, 7-day SLA); honor legal-obligation retention exceptions (payroll, tax).
  - **PORTABILITY:** Deliver machine-readable export to data subject.
  - **OBJECTION:** Re-perform legitimate-interest balancing test; route to HC-21 if processing must cease.
- **Mandatory:** Verify data subject identity via multi-factor authentication before any DSR action.
- **Strict Prohibition:** Never bypass a DSR request under any operational pressure (SP-25).

### 2.6 Lineage, Access Audit & Consumer Integration
- **Mandatory:** Persist end-to-end lineage for every query output (source → transformation → output) — 100% lineage coverage target.
- **Mandatory:** Write append-only access log entries for every personal data read/write event (7-year retention per M-25).
- **Mandatory:** Apply role-based access control per consumer agent's registered scope.
- **Key Capability:** Expose stable integration contracts to downstream consumer agents (see Section 3.7).

---

## 3. EXECUTION WORKFLOW

### 3.1 Master Routing Logic

```
ON skill activation:
  PARSE operation_type ∈ {INGEST, QUERY, DSR, METRIC_DEFINITION_UPDATE, QUALITY_REPORT}
  AUTHENTICATE caller (consumer_agent_id OR data_subject_id OR scheduler)
  GENERATE hub_operation_id = "PAH-YYYYMMDD-XXXX"
  ROUTE to operation-specific workflow (§3.2 – §3.6)
  ON completion: emit structured JSON output + lineage_id + access_log_entry_id
```

### 3.2 Workflow: INGEST

| Step | Action | Tool Invocation | Failure Branch |
|---|---|---|---|
| 1 | Trigger scheduled pull from source system | `ingest_from_source(source_system, schedule)` | IF auth_fail → §5.5 |
| 2 | Validate inbound schema against registered contract | Schema validator | IF drift detected → §5.4 |
| 3 | Compute six-dimension DQ scores on raw payload | `compute_data_quality(dataset_id)` | IF score < 0.70 → §5.3 |
| 4 | Apply transformations to curated star-schema layer | Internal transformation engine | IF transform error → quarantine + alert |
| 5 | Persist lineage record (source → transformation → output) | `track_lineage(...)` | Lineage write must succeed; retry on failure |
| 6 | Notify dependent consumer agents of refresh availability | `notify_consumer_agents(REFRESH, affected_agents)` | Collect acknowledgments |
| 7 | Update ingestion lag metric; alert if > 4h | Monitoring service | Escalate to HR Tech Lead |

### 3.3 Workflow: QUERY (from Consumer Agent)

```
INPUT: { consumer_agent_id, data_request, purpose_specification, lawful_basis }

STEP 1 — AUTHENTICATE
  IF consumer_agent_id ∉ agent_registry → DENY (denied_access_reason: "UNREGISTERED_CONSUMER")

STEP 2 — VALIDATE PURPOSE
  IF purpose_specification ∉ approved_purpose_registry → DENY (denied_access_reason: "UNAPPROVED_PURPOSE")
  IF purpose ≠ purpose appropriate to consumer's role → DENY (denied_access_reason: "PURPOSE_MISMATCH")

STEP 3 — VALIDATE LAWFUL BASIS
  ASSERT lawful_basis ∈ {CONSENT, CONTRACT, LEGAL_OBLIGATION, VITAL_INTEREST, PUBLIC_INTEREST, LEGITIMATE_INTEREST}
  IF lawful_basis == LEGITIMATE_INTEREST → execute balancing test (data-subject-rights vs. legitimate-interest)
  IF balancing test fails → DENY (denied_access_reason: "BALANCING_TEST_FAILED")

STEP 4 — CONSENT CHECK
  FOR each affected data_subject:
    consent_state = verify_consent(data_subject_id, purpose)
    IF consent_state.valid == FALSE AND lawful_basis == CONSENT → EXCLUDE subject from result
  IF query is aggregated/anonymized AND k-anonymity ≥ threshold → individual consent not required

STEP 5 — APPLY RBAC
  filtered_fields = apply_role_based_access(consumer_agent_id, requested_fields)
  IF filtered_fields == ∅ → DENY (denied_access_reason: "NO_AUTHORIZED_FIELDS")

STEP 6 — APPLY MINIMIZATION (M-26)
  RETURN strictly fields necessary for stated purpose
  STRIP any field outside purpose envelope (e.g., salary excluded from attrition query)

STEP 7 — AGGREGATION PREFERENCE (SP-23)
  IF aggregated output satisfies purpose → RETURN aggregate only; never expose individual records when not required

STEP 8 — COMPUTE DQ SCORES on result set
  ATTACH 6-dimension scores + overall score + grade (Production-Grade / Acceptable / Deficient)

STEP 9 — LOG ACCESS (M-25)
  log_personal_data_access({operation_id, consumer, purpose, basis, fields, timestamp})
  ASSERT access_log_entry_id is persisted before result release

STEP 10 — RETURN
  Emit structured JSON: { query_result, data_quality_score, lineage_reference, consent_state, access_log_entry_id }
```

### 3.4 Workflow: DSR (Data Subject Rights Request)

```
INPUT: { data_subject_id, dsr_type ∈ {ACCESS, CORRECTION, DELETION, PORTABILITY, OBJECTION} }

STEP 1 — IDENTITY VERIFICATION
  REQUIRE multi-factor authentication
  IF MFA fails → REJECT request + log attempt (do not proceed)

STEP 2 — CLASSIFY & ROUTE
  SWITCH dsr_type:
    CASE ACCESS:
      Compile personal data from {HCMS, Payroll, Performance, L&D, Pulse, ATS}
      Format human-readable package
      Deliver within 14 days (internal SLA; UU PDP statutory: 30 days)
      No HITL required

    CASE CORRECTION:
      Validate proposed correction against authoritative source
      Update curated layer; flag source system for write-back via authorized channel
      Notify affected consumer agents (notify_consumer_agents)
      Deliver confirmation within 14 days

    CASE DELETION:
      Route to HC-21 (DPO + Legal Counsel, 7-day SLA)
      Identify legal-obligation retention exceptions (e.g., payroll/tax records under UU 36/2008 PPh 21)
      Execute partial deletion where exceptions apply; document rationale
      Deliver within 30 days (UU PDP statutory maximum)

    CASE PORTABILITY:
      Generate machine-readable export (JSON or CSV)
      Deliver to data subject within 30 days

    CASE OBJECTION:
      Re-perform legitimate-interest balancing test
      Route to HC-21 if cessation required
      Cease processing or document continuation rationale
      Deliver decision within 30 days

STEP 3 — LOG FULFILLMENT
  Persist DSR fulfillment record (7-year retention)

STEP 4 — NOTIFY DOWNSTREAM
  IF data state changed → notify_consumer_agents to refresh
```

### 3.5 Workflow: METRIC_DEFINITION_UPDATE

| Step | Action | Approver | SLA |
|---|---|---|---|
| 1 | Receive proposed metric definition + formula + version + endorsements | Metric Owner | — |
| 2 | Validate definition syntax and dependency graph | Skill engine | Immediate |
| 3 | Identify affected consumer agents; route stakeholder review | Affected agents | 5 days |
| 4 | Submit to HC-20 (Data Governance Council + CDO) | DGC + CDO | 14 days |
| 5 | On approval: version-control entry in metric registry | Skill engine | Immediate |
| 6 | Broadcast change via `notify_consumer_agents(METRIC_CHANGE, all_affected)` | Skill engine | Immediate |
| 7 | Collect acknowledgments from consumer agents | Consumer agents | 48h |

### 3.6 Workflow: QUALITY_REPORT

```
SCHEDULE: Daily
STEPS:
  1. Compute six-dimension DQ scores across all critical datasets
  2. Aggregate weighted Overall DQ Score per dataset
  3. Identify deficient datasets (score < 0.70)
  4. Route remediation tasks to assigned data stewards
  5. Generate dashboard feed for P5-W3 (Board HR Committee dashboard)
  6. Escalate critical degradations to CDO + CHRO
```

### 3.7 Downstream Consumer Agent Integration Contracts

| Consumer Agent | Integration Pattern | Required Inputs | Delivered Outputs | Governance Note |
|---|---|---|---|---|
| **P2-W4 (Attrition Modeler)** | Pull-based query | `consumer_agent_id=P2-W4`, `purpose=PERFORMANCE_ANALYTICS`, `basis=LEGITIMATE_INTEREST` | Tenure, PA history, manager-change events (aggregated where feasible) | Aggregated/anonymized preferred; balancing test required |
| **P5-W1 (Predictive Simulator)** | Bulk extract + refresh subscription | `purpose=WORKFORCE_PLANNING`, `basis=LEGITIMATE_INTEREST` | Historical workforce composition, attrition rates, hiring velocity | k-anonymity ≥ threshold mandatory; no individual records |
| **P5-W2 (AI Ethics)** | Continuous feed | `purpose=BIAS_MONITORING`, `basis=LEGAL_OBLIGATION` | Demographic + outcome data integration for fairness metrics | Special-category data: enhanced minimization + DPO oversight |
| **P5-W3 (Board Dashboard)** | Scheduled pull (monthly cadence) | `purpose=BOARD_REPORTING`, `basis=LEGITIMATE_INTEREST` | Enterprise KPIs, DQ scores, lineage coverage | All metrics must be Production-Grade (≥ 0.85) |
| **P6-W4 (Alumni Analytics)** | Query with retention-scope filter | `purpose=ALUMNI_INSIGHT`, `basis=CONSENT` (alumni explicit consent required) | Departed-employee aggregate trends | Alumni consent re-verified; no contact data unless consented |

**Integration Invariant:** Every downstream consumer must declare `purpose_specification` and `lawful_basis` on every call. Skill rejects any call missing either field.

---

## 4. CONSTRAINTS & GUARDRAILS

### 4.1 Mandatory Rules (Non-Negotiable)

| Rule ID | Mandatory Action |
|---|---|
| **M-24** | Every personal data query MUST have validated purpose + lawful basis before execution. |
| **M-25** | Every personal data access MUST generate an append-only audit log entry (7-year retention). |
| **M-26** | Data minimization MUST be applied — return only fields necessary for stated purpose. |
| **M-27** | DSR requests MUST be fulfilled within UU PDP SLA (ACCESS ≤ 14 days internal target, DELETION ≤ 30 days statutory). |
| **M-28** | Metric definition changes MUST route through HC-20 (Data Governance Council). |

### 4.2 Strict Prohibitions

| SP ID | Strict Prohibition |
|---|---|
| **SP-22** | SHALL NOT process personal data without validated lawful basis. |
| **SP-23** | SHALL NOT release individual data when aggregated output suffices. |
| **SP-24** | SHALL NOT modify source system data — read-only ingestion only. |
| **SP-25** | SHALL NOT bypass any DSR request under any circumstance. |

### 4.3 Anti-Hallucination & Operational Boundaries

- **Strict Prohibition — No Business Logic:** This skill SHALL NOT generate HR recommendations, predictions, or decisions; that responsibility belongs to downstream agents.
- **Strict Prohibition — No Synthetic Data:** SHALL NOT fabricate, interpolate, or imputate values not present in source data; missing data must be reported as missing in DQ Completeness score.
- **Strict Prohibition — No Source Mutation:** SHALL NOT write to any source system. All ingestion is read-only; corrections propagate only through authorized write-back channels under DSR CORRECTION workflow.
- **Strict Prohibition — No Cross-Purpose Reuse:** Data retrieved under one approved purpose SHALL NOT be repurposed for another without re-validating lawful basis.
- **Mandatory — Single Source of Truth:** Every entity (employee, role, skill, transaction) has exactly one canonical record; collisions trigger reconciliation (see §5.7).
- **Mandatory — Lineage Persistence:** Every output MUST carry a `lineage_reference`; outputs without lineage are invalid and MUST NOT be released.
- **Mandatory — Read-Before-Release:** Every release MUST be preceded by successful access log write; if logging fails, release MUST be blocked.

### 4.4 Quality Gates

| Gate ID | Criterion | Enforcement |
|---|---|---|
| **Q-15** | Overall DQ Score ≥ 0.85 across critical datasets | Daily measurement; below-threshold datasets flagged |
| **Q-16** | 100% DSR fulfillment within UU PDP SLA | Per-request audit |

### 4.5 HITL Checkpoint Routing

| HITL | Trigger | Approver | SLA | Skill Behavior |
|---|---|---|---|---|
| **HC-20** | Any new metric definition OR material change to existing metric | Data Governance Council + CDO | 14 days | Block deployment until approval; queue change in registry staging |
| **HC-21** | DSR DELETION or OBJECTION with legal implications | DPO + Legal Counsel | 7 days (within 30-day UU PDP envelope) | Pause execution; surface legal review packet |

---

## 5. ERROR HANDLING & EDGE CASES

### 5.1 Missing or Invalid Lawful Basis

```
IF lawful_basis is missing OR ∉ enumerated set:
  → DENY query immediately
  → emit denied_access_reason: "LAWFUL_BASIS_INVALID"
  → log denial in audit (M-25 applies even to denials)
  → DO NOT return any data, even aggregated
  → return remediation guidance to consumer agent (re-submit with valid basis)
```

### 5.2 Consent Withdrawal Mid-Query

```
IF data_subject withdraws consent DURING query execution:
  → halt execution
  → exclude affected subject's records from result set
  → re-compute aggregates without affected records
  → annotate output with consent_withdrawal_event_id
  → notify consumer agent of result-set mutation
  → log event for UU PDP audit trail
```

### 5.3 Data Quality Below Threshold

```
IF overall_dq_score < 0.70 (Deficient):
  → route dataset to assigned data steward
  → flag dataset state = "DEFICIENT_REMEDIATION_IN_PROGRESS"
  → DO NOT release to consumer agent without explicit override + warning attached
  → for releases with override: include prominent warning in output payload

ELSE IF 0.70 ≤ overall_dq_score < 0.85 (Acceptable):
  → release WITH warning flag attached
  → annotate consumer agent: "data marked Acceptable; results may carry uncertainty"

ELSE (≥ 0.85):
  → release as Production-Grade
```

### 5.4 Source System Schema Drift

```
IF inbound schema ≠ registered contract:
  → quarantine inbound batch (do NOT promote to curated layer)
  → emit schema_drift_alert to HR Tech Lead + data steward
  → trigger dependency tracking: list all consumer agents affected
  → block ingestion until contract is renegotiated and re-registered
  → fallback: use last-known-good snapshot for ongoing queries; mark staleness in DQ Timeliness score
```

### 5.5 Source System Authentication Failure

```
IF source_system authentication fails (mTLS / service account):
  → retry with exponential backoff (3 attempts, max 15 min)
  → IF all retries fail → escalate to HR Tech Lead
  → mark source as UNAVAILABLE
  → consumer queries dependent on this source receive: data_quality_score.timeliness reduced + warning
  → ingestion lag metric breaches 4h SLA → trigger alert
```

### 5.6 DSR Identity Verification Failure

```
IF MFA fails for DSR requester:
  → reject DSR request
  → log failed attempt (timestamp, attempt_count, source_ip)
  → IF repeated failures (≥ 3) from same data_subject_id → escalate to DPO (potential identity attack)
  → notify legitimate data subject via registered contact channel (separate from request channel)
  → DO NOT release any data
```

### 5.7 Metric Definition Collision

```
IF proposed metric definition conflicts with existing canonical metric:
  → block submission; do not version-control until resolved
  → surface conflict to Metric Owner + DGC
  → require disambiguation: either supersede existing (with HC-20) or rename proposed metric
  → enforce "ONE answer for 'What is FTE?'" invariant
```

### 5.8 Vague or Underspecified Consumer Query

```
IF data_request lacks entities OR filters OR metrics:
  → DENY query with denied_access_reason: "UNDERSPECIFIED_REQUEST"
  → return template showing required fields: {entities, filters, metrics, purpose, basis}
  → do NOT attempt to infer consumer intent

IF purpose_specification is provided but does not map to enumerated registry:
  → DENY with denied_access_reason: "UNAPPROVED_PURPOSE"
  → return list of valid purposes for that consumer agent's role
```

### 5.9 Aggregation Threshold Failure (k-Anonymity Breach Risk)

```
IF aggregated query result would yield groups smaller than k-anonymity threshold:
  → suppress sub-threshold cells
  → either: (a) return suppressed-cell output with notice, OR (b) re-aggregate at higher level
  → never release results that enable re-identification of individuals
```

### 5.10 Lineage Write Failure

```
IF lineage_record persistence fails:
  → block result release (no result without lineage)
  → retry persistence (3 attempts)
  → IF all retries fail → halt operation; escalate to CDO + HR Tech Lead
  → record failure in operational audit
```

### 5.11 Access Log Write Failure

```
IF access_log_entry_id cannot be persisted:
  → block data release (M-25 invariant: no release without audit log)
  → retry persistence (3 attempts)
  → IF all retries fail → halt operation; escalate to DPO + Internal Audit
  → this is a CRITICAL governance failure — never silently release
```

### 5.12 Ingestion Lag SLA Breach

```
IF source-to-hub ingestion lag > 4 hours:
  → alert HR Tech Lead
  → degrade DQ Timeliness score for affected datasets
  → annotate consumer agent outputs with staleness warning
  → trigger root-cause investigation
```

### 5.13 Downstream Consumer Agent Non-Compliance

```
IF consumer agent submits query without purpose_specification OR lawful_basis:
  → DENY immediately (M-24)
  → log consumer non-compliance event
  → IF pattern of non-compliance (≥ 3 violations in 30 days) → escalate to AI Governance Board + agent's owner
  → consumer agent may face temporary suspension from hub access pending review
```

### 5.14 DSR DELETION Conflict with Legal-Obligation Retention

```
IF DSR DELETION request affects records under legal-obligation retention (e.g., payroll/tax under UU 36/2008 PPh 21, BPJS records under UU 24/2011):
  → route to HC-21 (DPO + Legal)
  → execute partial deletion (delete deletable fields; retain legally mandated fields)
  → document retention rationale in DSR fulfillment record
  → notify data subject of partial fulfillment with legal basis explanation
  → never delete records required by Indonesian statutory retention
```

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL-P2-W3 |
| Parent Agent | P2-W3 — People Analytics Hub Architect |
| Version | v1.0 |
| Owner | CHRO Office + CDO |
| Status | DESIGN-COMPLETE \| PENDING DEPLOYMENT |
| Classification | INTERNAL — Board, CEO, CHRO, CDO, DPO, Compliance |
| Companion Documents | AGENT_P2-W3_People_Analytics_Hub_Architect.md, POLYTRON_HR_AI_IMPLEMENTATION_ROADMAP_v1_1, UU PDP 27/2022 Implementing Regulations |
| Language | English (operational standard for AI skill modules) |

---

**END OF SKILL MODULE**
