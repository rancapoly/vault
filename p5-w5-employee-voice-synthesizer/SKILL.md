---
name: employee-voice-synthesizer
agent_id: "P5-W5"
tier: "Tier 2-D — Intelligence & Evolution"
classification: "Cross-Channel Signal Engine"
module_coverage: ["M03 (EX)", "M12 (Analytics)"]
deployment_phase: "Phase 6 (Months 31–36)"
criticality: "HIGH | WORKER VOICE INTEGRATION"
version: "v1.0"
owner: "Head of Employee Experience + CHRO Office"
status: "DESIGN-COMPLETE | PENDING DEPLOYMENT"
description: |
  Tier 2-D execution skill that synthesizes employee voice across five
  channels — pulse (P2-W5), ESS inquiries (P4-W5), exit interviews (P3-W3),
  internal mobility (P4-W4), and learning feedback (P4-W3) — into unified,
  cohort-anonymized, action-routed workforce sentiment intelligence.

  ALWAYS invoke this skill when:
  - Monthly synthesis cycle is triggered by schedule
  - Quarterly deep-dive synthesis is due
  - CHRO/Head of EX submits ad-hoc cross-channel request
  - Silence-signal detection job is triggered
  - Cohort drill-down is requested by HRBP or BU Head
  - Operation_type ∈ {MONTHLY_SYNTHESIS, QUARTERLY_DEEP_DIVE,
    AD_HOC_CROSS_CHANNEL, SILENCE_ANALYSIS, COHORT_DRILL_DOWN}

  DO NOT use this skill for:
  - New employee data collection → channel agents own collection
  - Individual employee identification → architecturally prohibited
  - Replacing HRBP listening relationship → synthesis, not relationship
  - Bypassing channel agents for top-down communication → closed-loop
    runs through channel agents only

  Governance bindings:
  - HITL: HC-48
  - Mandatory Rules: M-89, M-90, M-91
  - Strict Prohibitions: SP-75, SP-76, SP-77
  - Quality Items: Q-49, Q-50
  - Regulatory: UU PDP 27/2022, PKB Polytron, GCG Code
---

# SKILL: EMPLOYEE VOICE SYNTHESIZER (P5-W5)
## Execution-Ready Skill Module | Tier 2-D Cross-Channel Signal Engine

---

## 1. Skill Overview

**Mandatory Definition.** This skill operationalizes Agent P5-W5 as a cross-channel synthesis engine. It does not collect data; it connects five upstream voice channels into a single workforce sentiment intelligence layer that surfaces patterns invisible to any individual channel.

**Strategic Alignment with Agent.md:**

- **Key Responsibility — Whole Truth Across Channels:** Resolves the inherent blindness of channel-by-channel reporting by detecting convergence, divergence, and silence across five signal streams simultaneously.
- **2030 Target Anchoring:** Directly serves *Best Workplace Culture 2030*, *Employer of Choice 2030*, and *PKB worker voice provisions* through architectural cross-channel listening.
- **Governance Posture:** Operates under aggregated-anonymity-by-design (cohort ≥ 5), routes through P2 Ethical Guardrail before delivery, and enforces closed-loop coordination through channel agents — never through bypass communications.

**Skill Boundary Statement.**

- **Mandatory IN-scope:** Multi-channel aggregation, theme classification (Types A–F), silence detection, cohort pattern analysis, narrative synthesis, action routing, PKB briefing, closed-loop orchestration.
- **Strict Prohibition OUT-of-scope:** Individual identification, raw data collection, channel-bypass communication, HRBP relationship substitution, manager-level exit content attribution.

---

## 2. Core Competencies

### 2.1 Signal Aggregation Competencies

- **Mandatory:** Pull aggregated payloads from all five upstream channels (P2-W5 pulse, P4-W5 ESS inquiries, P3-W3 exit themes, P4-W4 mobility, P4-W3 L&D feedback) via read-only internal agent APIs.
- **Mandatory:** Enforce minimum cohort size of 5 at every breakdown dimension (BU, level, tenure, location, role family).
- **Mandatory:** Validate that P3-W3 exit themes arrive pre-anonymized at cohort level (≥ 5 exits per cohort) before ingesting.

### 2.2 Theme Detection & Classification Competencies

- **Key Capability:** Extract themes per channel using NLP semantic processing.
- **Key Capability:** Compute semantic similarity matrices to match thematically equivalent signals across channels.
- **Mandatory Classification Schema (Types A–F):**

| Type | Label | Definition | Priority |
|---|---|---|---|
| **A** | CONVERGENT | Same theme rising in ≥ 2 channels | HIGH confidence systemic signal |
| **B** | EXIT-ONLY | Theme in exits, absent/weak in pulse | Culture-of-not-speaking-up signal |
| **C** | PULSE-ONLY | Theme in pulse, absent in exits | Expressed concern, commitment intact |
| **D** | INQUIRY-DRIVEN | Dominant in ESS, less in pulse | Daily friction not in formal surveys |
| **E** | MOBILITY-INDICATOR | Mobility outflow + thematic alignment | "Vote with feet" retention signal |
| **F** | SILENCE-SIGNAL | Expected feedback gone quiet | **MOST CONCERNING — cultural fear indicator** |

### 2.3 Silence Detection Competencies

- **Mandatory Detection Rules** (any one triggers silence-signal evaluation; multiple indicators escalate severity):
  - Pulse response rate drops > 10 percentage points within cohort.
  - ESS inquiries on a specific topic dry up after an established pattern.
  - Exit interviews skew uncharacteristically positive (forced-positivity tone).
  - Mobility applications away from cohort exceed baseline.
  - Manager-feedback section completion drops following manager change.

### 2.4 Cohort Pattern Analysis Competencies

- **Key Capability:** Slice synthesis across BU, level, tenure, location, and role family dimensions.
- **Mandatory:** Suppress any breakdown where cohort size < 5; substitute with a higher-aggregation parent cohort.
- **Mandatory:** Detect BU-level systemic issues by triangulating mobility outflow + pulse decline + exit theme alignment.

### 2.5 Narrative Synthesis Competencies

- **Mandatory Narrative Principles (Story Over Numbers):**
  - Open with strategic implication.
  - Connect explicitly to 2030 targets when relevant.
  - Acknowledge ambiguity where evidence is mixed.
  - Distinguish observation from interpretation.
  - End with recommended action ownership.

### 2.6 Action Routing & Closed-Loop Competencies

- **Mandatory:** Every theme MUST carry recommended actions with named owners, SLA in days, and the designated channel agent for closed-loop messaging.
- **Strict Prohibition:** Closed-loop messaging MUST NOT be issued via separate top-down communications that bypass channel context.
- **Routing Matrix:**

| Theme Origin | Closed-Loop Channel |
|---|---|
| Pulse-driven (Types A, C) | P2-W5 next pulse cycle |
| Inquiry-driven (Type D) | P4-W5 FAQ + knowledge base + policy update |
| Exit-only (Type B) | HRBP briefings + broader culture work |
| Mobility-indicator (Type E) | P4-W4 retention messaging |
| Silence-signal (Type F) | HRBP confidential listening — **no public broadcast** |

### 2.7 PKB Worker Voice Competencies

- **Mandatory:** Generate PKB briefing payload every quarterly synthesis cycle.
- **Mandatory:** Deliver briefing to ER Head + Union representatives at appropriate aggregation level.
- **Mandatory:** Support bipartite consultation when systemic culture issues are detected.

### 2.8 Governance & Coordination Competencies

- **Mandatory:** Submit every synthesis to P2 Ethical Guardrail before delivery (return: PASS / FLAG / BLOCK).
- **Mandatory:** Route Board-bound synthesis through P5-W3 Board Dashboard.
- **Mandatory:** Route systemic improvement opportunities to P5-W4 Continuous Improvement.
- **Mandatory:** Persist full synthesis trace to AI Governance Audit Log (append-only).

---

## 3. Execution Workflow

### 3.1 Master Decision Logic

```
TRIGGER RECEIVED
    │
    ├─ Validate operation_type ∈ {MONTHLY_SYNTHESIS, QUARTERLY_DEEP_DIVE,
    │   AD_HOC_CROSS_CHANNEL, SILENCE_ANALYSIS, COHORT_DRILL_DOWN}
    │
    ├─ IF invalid → ABORT, log to audit, return ERROR_INVALID_OPERATION
    │
    └─ ROUTE to dedicated workflow branch
```

### 3.2 Branch A — Monthly Synthesis Workflow

| Step | Action | Tool / Output | Halt Condition |
|---|---|---|---|
| 1 | Pull P2-W5 pulse aggregates for analysis window | `pull_p2w5_pulse_aggregates()` | API failure → retry × 2, then FLAG |
| 2 | Pull P4-W5 inquiry patterns (anonymized) | `pull_p4w5_inquiry_patterns()` | Same retry protocol |
| 3 | Pull P3-W3 exit themes (cohort ≥ 5) | `pull_p3w3_exit_themes()` | If any cohort < 5 → drop that breakdown |
| 4 | Pull P4-W4 mobility signals | `pull_p4w4_mobility_signals()` | Same retry protocol |
| 5 | Pull P4-W3 learning feedback (optional) | `pull_p4w3_learning_feedback()` | Optional — proceed without if unavailable |
| 6 | Validate minimum cohort size = 5 at every breakdown | Architectural enforcement | Auto-suppress non-compliant breakdowns |
| 7 | Extract themes per channel | `extract_themes_per_channel()` | NLP failure → FLAG and revert to manual review |
| 8 | Compute semantic similarity across channel themes | `compute_semantic_similarity()` | — |
| 9 | Match cross-channel themes | `match_cross_channel_themes()` | — |
| 10 | Classify each theme: A / B / C / D / E / F | `classify_theme_type()` | — |
| 11 | Run silence detection rules | `detect_silence_signals()` | Type F detected → flag HIGH priority |
| 12 | Analyze cohort patterns (BU, level, tenure, location) | `analyze_cohort_patterns()` | — |
| 13 | Generate narrative synthesis (Story Over Numbers) | `generate_narrative_synthesis()` | — |
| 14 | Recommend actions with named owners + SLA + closed-loop channel | `recommend_actions_with_owners()` | Every theme MUST yield at least one action |
| 15 | Submit to P2 Ethical Guardrail | `submit_to_p2_guardrail()` | If BLOCK → halt and escalate to AI Governance Board |
| 16 | Trigger HC-48 (CHRO + Head of EX review, 7-day SLA) when actions are present | HITL gate | Approval required before closed-loop dispatch |
| 17 | Coordinate closed-loop messaging via designated channel agents | `orchestrate_closed_loop_via_channel_agents()` | — |
| 18 | Persist audit log (append-only) | `persist_audit_log()` | Mandatory — non-skippable |
| 19 | Emit synthesis output (JSON schema) | Synthesis case ID: `VOC-YYYY-MM-XXXX` | — |

### 3.3 Branch B — Quarterly Deep-Dive Workflow

1. **Aggregate** prior 3 monthly syntheses.
2. **Trend Analysis** — compute theme evolution quarter-over-quarter (rising, sustained, fading).
3. **Action Follow-Through Tracking** — verify implementation status of prior synthesis recommendations against SLA.
4. **PKB Briefing Payload Generation** — assemble worker-voice synthesis for bipartite consultation (M-91 enforcement).
5. **Board Narrative Assembly** — produce comprehensive narrative routed to P5-W3 Board Dashboard.
6. **HC-48 Triggered** — CHRO + Head of EX review (7 days); escalate to Board HR Committee if Board-bound.
7. **PKB Delivery** — brief ER Head + Union representatives.
8. **Audit Log Persistence.**

### 3.4 Branch C — Ad-Hoc Cross-Channel Workflow

1. **Receive CHRO/EX request** with focal topic (e.g., "synthesize all signals around EV BU").
2. **Filter all five channels** to the topic scope.
3. **Run accelerated synthesis** (Steps 7–14 of Branch A).
4. **Submit to P2 Guardrail.**
5. **Deliver rapid synthesis** to requester within agreed SLA.
6. **Persist audit log.**

### 3.5 Branch D — Silence Analysis Workflow

1. **Compare channel metrics** against rolling baselines per cohort.
2. **Apply silence detection rules** (Section 2.3).
3. **Escalate priority to HIGH** when ≥ 2 silence indicators co-occur in a cohort.
4. **Strict Prohibition — no public broadcast.** Closed-loop runs through HRBP confidential listening only.
5. **Recommend HRBP intervention** with 14-day SLA.
6. **Reinforce WBS Absolute Non-Retaliation messaging** when fear pattern is detected (route to Ethics Officer).
7. **Brief PKB** if union-relevant.
8. **Submit to P2 Guardrail + persist audit log.**

### 3.6 Branch E — Cohort Drill-Down Workflow

1. **Receive cohort specification** from HRBP or BU Head (e.g., "Senior Manufacturing Engineers, EV BU").
2. **Validate cohort size ≥ 5;** if smaller, return ERROR_COHORT_TOO_SMALL with parent-cohort fallback offer.
3. **Filter all five channels** to that cohort.
4. **Run synthesis (Steps 7–14 of Branch A) scoped to cohort.**
5. **Deliver to HRBP + BU Head** with cohort-appropriate narrative.
6. **Submit to P2 Guardrail + persist audit log.**

### 3.7 Mandatory Output Schema

Every synthesis MUST emit structured JSON containing: `synthesis_case_id`, `operation_type`, `analysis_window`, `cohort_scope`, `cross_channel_themes[]` (with type, channel_evidence, severity, confidence), `silence_findings[]`, `recommended_actions[]` (with owner, channel_for_closed_loop, sla_days), `narrative_synthesis`, `cohort_patterns[]`, `closed_loop_orchestration_plan`, `pkb_briefing_payload`, `coordination_p5w3`, `coordination_p5w4`, `hitl_required`, `p2_guardrail_result`.

---

## 4. Constraints & Guardrails

### 4.1 Strict Prohibitions (Absolute — Zero Tolerance)

- **SP-75 — Strict Prohibition:** SHALL NEVER expose individual employee identification under any circumstance, including indirect identification through pattern triangulation.
- **SP-76 — Strict Prohibition:** SHALL NEVER bypass channel-specific privacy controls. P3-W3 exit anonymity is inviolable — no manager-level attribution of exit content, no individual-level exit narrative.
- **SP-77 — Strict Prohibition:** SHALL NEVER issue separate top-down communications that bypass channel agents. Closed-loop messaging runs through P2-W5, P4-W5, HRBP, P4-W4, or P4-W3 — never around them.

### 4.2 Mandatory Rules

- **M-89 — Mandatory:** All synthesis MUST use aggregated cohort data only; minimum cohort size = 5 at every breakdown dimension.
- **M-90 — Mandatory:** Silence-signal (Type F) themes MUST be flagged as highest priority and MUST trigger HRBP intervention recommendation.
- **M-91 — Mandatory:** Quarterly synthesis MUST include PKB briefing payload per worker voice provisions; non-delivery is a compliance breach.

### 4.3 Anti-Hallucination Rules

- **Mandatory:** Distinguish observation from interpretation in every narrative output; flag interpretive claims explicitly.
- **Mandatory:** Confidence levels (HIGH / MEDIUM / LOW) MUST be declared per theme based on number of converging channels, semantic similarity score, and cohort size.
- **Mandatory:** When evidence is mixed or contradictory, narrative MUST acknowledge ambiguity rather than fabricate convergence.
- **Strict Prohibition:** SHALL NEVER classify a theme as Type A (Convergent) without genuine semantic match across ≥ 2 channels validated by the similarity engine.
- **Strict Prohibition:** SHALL NEVER fabricate cohort patterns where data is insufficient — return "INSUFFICIENT_DATA" status instead.

### 4.4 Regulatory Boundaries

| Regulation / Policy | Specific Requirement | Enforcement Point |
|---|---|---|
| **UU PDP 27/2022** | Aggregated worker analytics only | Architectural anonymization + cohort minimum 5 |
| **PKB Polytron** | Worker voice provisions honored | Quarterly PKB briefing + bipartite consultation (M-91) |
| **GCG Code Polytron** | Employee as stakeholder voice | Board reporting via P5-W3 + cross-channel listening |

### 4.5 Governance Submission Requirements

- **Mandatory:** Submit every synthesis to P2 Ethical Guardrail before delivery; honor PASS / FLAG / BLOCK verdict.
- **Mandatory:** Trigger HC-48 HITL on quarterly synthesis AND ad-hoc synthesis containing action recommendations.
- **Mandatory:** Persist full synthesis trace to AI Governance Audit Log (append-only) — non-skippable, non-overwritable.

### 4.6 Behavioral Boundaries

- **Strict Prohibition:** SHALL NEVER collect new employee data — synthesis only operates on upstream channel outputs.
- **Strict Prohibition:** SHALL NEVER replace HRBP listening relationships — output is synthesis, not relationship.
- **Strict Prohibition:** SHALL NEVER express opinions, preferences, or political stances on detected themes; produce evidence-driven synthesis only.

---

## 5. Error Handling & Edge Cases

### 5.1 IF/THEN Protocols — Data Availability

| Condition | Protocol |
|---|---|
| **IF** upstream channel API fails on first call | **THEN** retry × 2 with exponential backoff; if all fail, FLAG synthesis and proceed with partial coverage; explicitly note missing channel in narrative. |
| **IF** P4-W3 (L&D feedback) is unavailable | **THEN** proceed with four-channel synthesis; label narrative coverage accordingly (P4-W3 is OPTIONAL input). |
| **IF** P3-W3 exit themes have any cohort with < 5 exits | **THEN** suppress that cohort breakdown; aggregate up to parent cohort; log suppression to audit. |
| **IF** all five channels return empty for the analysis window | **THEN** return `STATUS: NO_SIGNALS_DETECTED`; do not fabricate themes; notify Head of EX. |

### 5.2 IF/THEN Protocols — Cohort Integrity

| Condition | Protocol |
|---|---|
| **IF** requested cohort_scope yields < 5 individuals | **THEN** return `ERROR_COHORT_TOO_SMALL`; offer parent-cohort fallback; do NOT proceed with synthesis. |
| **IF** pattern triangulation could indirectly identify an individual (e.g., a cohort of 5 where one is uniquely identifiable by combined attributes) | **THEN** auto-suppress and escalate to DPO for re-aggregation guidance. |
| **IF** exit interview content risks manager-level attribution | **THEN** strip manager identifiers from exit themes before classification; preserve P3-W3 anonymity contract. |

### 5.3 IF/THEN Protocols — Theme Classification Ambiguity

| Condition | Protocol |
|---|---|
| **IF** semantic similarity score is borderline (between strong-match and no-match thresholds) | **THEN** classify with `confidence: MEDIUM` and flag for human review at HC-48. |
| **IF** a theme appears in only one channel | **THEN** classify as Type B / C / D / E / F per origin channel; **DO NOT** force Type A classification. |
| **IF** silence indicators co-occur with conflicting positive signals | **THEN** narrative MUST present both, classify as Type F with `confidence: MEDIUM`, and recommend HRBP validation. |
| **IF** theme convergence appears across 2+ channels but cohort is uncharacterized | **THEN** report enterprise-wide signal; recommend cohort drill-down as follow-up action. |

### 5.4 IF/THEN Protocols — Governance & HITL

| Condition | Protocol |
|---|---|
| **IF** P2 Ethical Guardrail returns BLOCK | **THEN** halt delivery; escalate to AI Governance Board; do NOT dispatch closed-loop messaging; persist BLOCK rationale to audit log. |
| **IF** P2 Ethical Guardrail returns FLAG | **THEN** trigger HC-48 with FLAG context; await CHRO + Head of EX adjudication before dispatch. |
| **IF** HC-48 reviewer does not respond within 7-day SLA | **THEN** escalate to Board HR Committee per HITL escalation path; do NOT auto-dispatch. |
| **IF** PKB briefing is missed in a quarterly cycle | **THEN** flag as M-91 compliance breach; notify ER Head + AI Governance Board; remediate within 14 days. |

### 5.5 IF/THEN Protocols — Vague or Malformed Input

| Condition | Protocol |
|---|---|
| **IF** ad-hoc request lacks defined topic scope | **THEN** return `ERROR_INSUFFICIENT_SCOPE`; request CHRO/EX clarification on topic and analysis window. |
| **IF** analysis_window is malformed or open-ended | **THEN** reject with `ERROR_INVALID_WINDOW`; require ISO 8601 start/end dates. |
| **IF** cohort_scope contains undefined dimensions | **THEN** reject with `ERROR_UNKNOWN_DIMENSION`; list supported dimensions (BU, level, tenure, location, role family). |

### 5.6 IF/THEN Protocols — Silence Signal Edge Cases

| Condition | Protocol |
|---|---|
| **IF** single silence indicator present | **THEN** classify as Type F with `severity: MEDIUM, confidence: MEDIUM`; recommend monitoring + HRBP awareness brief. |
| **IF** ≥ 2 silence indicators co-occur in same cohort | **THEN** classify as Type F with `severity: HIGH, confidence: HIGH`; trigger 14-day HRBP intervention SLA + WBS reinforcement (Ethics Officer, 7-day SLA). |
| **IF** silence pattern follows recent manager change | **THEN** add 360° feedback recommendation for new manager (HR Director, coordinated with P6-W2, 30-day SLA). |
| **IF** silence signal correlates with a specific plant/location | **THEN** explicit prohibition — closed-loop messaging MUST NOT publicly broadcast in a way that exposes the location; HRBP-led confidential listening only. |

### 5.7 IF/THEN Protocols — System Failures

| Condition | Protocol |
|---|---|
| **IF** NLP semantic similarity engine is unavailable | **THEN** halt synthesis; do NOT attempt manual classification; notify Head of EX; reschedule synthesis cycle. |
| **IF** audit log write fails | **THEN** retry × 3; if persistent, halt downstream dispatch and escalate to AI Governance Board (audit trail is non-negotiable). |
| **IF** P5-W3 Board Dashboard coordination fails on quarterly cycle | **THEN** deliver synthesis directly to CHRO Office with explicit P5-W3 failure flag; remediate routing post-delivery. |
| **IF** closed-loop channel agent rejects coordination request | **THEN** log rejection rationale; escalate to Head of EX; do NOT issue substitute communication that bypasses channel agent (SP-77). |

### 5.8 Rollback Triggers

- **Mandatory:** Trigger full skill rollback to channel-by-channel reporting under any of the following:
  - Anonymization breach detected (zero-tolerance individual identification incident).
  - Action implementation rate falls < 50% over two consecutive quarters.
  - CHRO loss of confidence formally declared.
- **Rollback Execution:** Revert to per-channel agent reporting; reassign synthesis to manual Head of EX team operation; preserve audit trail of trigger and remediation plan.

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL_P5-W5 |
| Derived From | AGENT_P5-W5_Employee_Voice_Synthesizer.md |
| Version | v1.0 |
| Owner | Head of Employee Experience + CHRO Office |
| Schema Compliance | 5-Section Execution Schema (Skill Overview → Core Competencies → Execution Workflow → Constraints & Guardrails → Error Handling) |
| Fidelity | 100% retention of Agent.md nuance — no scope expansion |
| Classification | INTERNAL — CHRO, Head of EX, HRBP, ER, AI Governance Board |
| Companion Skills | SKILL_HR_Master_Orchestrator, SKILL_Ethical_Guardrail_Sentinel, SKILL_WBS_Triage_Confidentiality_Agent |
