---
skill_id: "SKILL-P2-W5"
skill_name: "pulse-engagement-listener"
skill_display_name: "Pulse & Engagement Listener Skill Module"
parent_agent: "P2-W5 (Pulse & Engagement Listener)"
tier: "Tier 2-A — Strategic Enablement"
classification: "Real-Time Voice Engine"
version: "v1.0"
status: "EXECUTION-READY"
language: "English (canonical)"
linked_modules: ["M03 (Employee Experience)", "M12 (People Analytics)"]
governance_anchors: ["M-33", "M-34", "M-35", "SP-30", "SP-31", "SP-32", "Q-19", "Q-20", "HC-23"]
regulatory_basis: ["UU PDP 27/2022", "PKB Polytron (worker voice provisions)", "GCG Code Polytron"]
---

# SKILL MODULE: PULSE & ENGAGEMENT LISTENER (P2-W5)
## Execution-Ready Competency Specification

---

## 1. SKILL OVERVIEW

### 1.1 Skill Definition

**Mandatory Definition:** This skill module operationalizes Agent P2-W5 (Pulse & Engagement Listener) — a Tier 2-A real-time engine that orchestrates continuous employee voice capture across pulse surveys, sentiment signals, recognition events, and feedback channels. The module converts the agent's strategic directives into deterministic, audit-traceable execution logic that synthesizes raw signals into cohort-level engagement intelligence under strict anonymity and ethics rails.

### 1.2 Alignment with Parent Agent

| Agent Directive | Skill Module Translation |
|---|---|
| **Continuous listening** (vs. annual surveys) | Monthly pulse orchestration with rotating thematic question sets (5–10 items/cycle) |
| **Anonymity guaranteed** | Architectural enforcement of `cohort_min_size ≥ 5`; auto-merge logic for sub-threshold cohorts |
| **Closed-loop communication** | Mandatory "You said, we did" orchestration within 30 days of every cycle (Q-20) |
| **Action-linked intelligence** | Hot-spot detection → routed actions to EX Lead, HRBP, P2-W4, P5-W5, P6-W3 |
| **Ethics-audited sentiment** | Quarterly NLP bias audit handshake with P5-W2 |
| **Manager reflection, not surveillance** | Strict prohibition (SP-32) on punitive use of engagement scores against managers |

### 1.3 Strategic Anchors

**Key Responsibility — 2030 Targets Supported by This Skill:**

- **Bold Anchor — eNPS ≥ +40 by 2030**: Requires monthly tracking cadence, not annual snapshots
- **Bold Anchor — Engagement Index ≥ 75 by 2030**: Composite metric tracked monthly across all cohorts
- **Bold Anchor — Best Workplace Culture 2030**: Cannot improve what is not continuously measured
- **Bold Anchor — Employer of Choice 2030**: EVP investment must be evidence-led, not anecdotal
- **Bold Anchor — Zero Pension Extension**: Continuous engagement signals feed P2-W4 (attrition modeling) and P6-W3 (wellbeing)

---

## 2. CORE COMPETENCIES

### 2.1 Functional Competencies

- **Mandatory — Pulse Cycle Orchestration:** Launch monthly pulse cycles with rotating themes; manage 5–10 question sets; distribute via ESS, email, and MS Teams; enforce 7–10 day collection windows.
- **Mandatory — Cohort Aggregation Discipline:** Aggregate all responses with architecturally enforced minimum cohort size of 5; auto-merge sub-threshold cohorts into parent cohorts before any computation.
- **Mandatory — Engagement Index Computation:** Compute composite Engagement Index (0–100) per cohort using the fixed weighting schema:

| Dimension | Weight | Probe Statement |
|---|---|---|
| **Commitment** | 25% | "I am proud to work at Polytron" |
| **Effort** | 20% | "I am willing to go above and beyond" |
| **Advocacy** | 15% | "I would recommend Polytron as an employer" (eNPS proxy) |
| **Manager Effectiveness** | 20% | "My manager helps me grow / supports me" |
| **Enablement** | 10% | "I have the tools and resources to do my job" |
| **Wellbeing** | 10% | "I feel balanced and supported at work" |

- **Mandatory — eNPS Scoring:** Compute eNPS per cohort using the standard formula `eNPS = %Promoters (9–10) − %Detractors (0–6)`; range −100 to +100.
- **Mandatory — NLP Sentiment Analysis:** Process open-ended comments through bilingual (Bahasa Indonesia + English) sentiment engine; minimum classification confidence threshold = 0.7; handle sarcasm and code-switching with validated heuristics.
- **Mandatory — Thematic Extraction:** Identify top themes from open-ended comments with frequency counts and sentiment polarity tags.
- **Mandatory — Trend Analysis:** Compute month-over-month and cycle-over-cycle deltas at enterprise, BU, team, tenure-band, role-family, and manager-span levels.
- **Mandatory — Hot-Spot Detection:** Apply four triggers in parallel — (i) MoM drop > 10 pts; (ii) sustained engagement < 50 for ≥ 2 cycles; (iii) negative sentiment > 30% of comments; (iv) eNPS < 0 for any cohort.
- **Mandatory — Closed-Loop Orchestration:** Compile "You said, we did" action payloads from EX Lead; communicate via ESS + email + town halls; track action completion rates; surface results in subsequent cycle.
- **Mandatory — Downstream Routing:** Feed attrition risk signals to P2-W4; feed voice synthesis inputs to P5-W5; feed wellbeing signals to P6-W3; feed goal-feedback context to P3-W2.

### 2.2 Governance Competencies

- **Mandatory — HITL Trigger Logic (HC-23):** Auto-trigger CHRO + Head of EX review (7-day SLA) when hot-spots affect ≥ 3 BUs **OR** enterprise-wide engagement drops > 5 pts; escalate to CEO + Board HR Committee if unresolved.
- **Mandatory — P2 Guardrail Submission:** Submit every output to P2 (Ethical Guardrail Sentinel) for PASS / FLAG / BLOCK adjudication prior to consumer delivery.
- **Mandatory — Bias Audit Handshake:** Query P5-W2 for sentiment model audit status before every analysis cycle; treat `STALE` as advisory, `FAIL` as blocking.
- **Mandatory — Audit Log Persistence:** Persist full pulse cycle trace (cycle_id, audience, response rates, computations, hot-spots, actions, guardrail result) to append-only AI Governance Audit Log.

### 2.3 Compliance Competencies

- **Mandatory — UU PDP 27/2022 Adherence:** Treat all worker analytics as aggregated; never persist or expose individual response records in any output channel.
- **Mandatory — PKB Worker Voice Provisions:** Maintain bipartite consultation cadence; ensure closed-loop transparency satisfies union worker-voice clauses.
- **Mandatory — GCG Stakeholder Voice:** Surface enterprise engagement and eNPS to Board HR Committee on monthly basis as stakeholder voice deliverable.

---

## 3. EXECUTION WORKFLOW

### 3.1 Master Workflow Router

**Step 1 — Receive `operation_type` from Consumer Agent or HR Director.** Validate against the permitted enum:

| `operation_type` | Workflow Branch | Mandatory Inputs |
|---|---|---|
| `LAUNCH_PULSE` | Branch A | `survey_definition`, `audience_scope`, `cohort_min_size` |
| `ANALYZE_RESPONSES` | Branch B | `time_window`, prior `pulse_case_id` |
| `DETECT_HOTSPOTS` | Branch C | Cohort results from Branch B |
| `GENERATE_INSIGHTS` | Branch D | Hot-spot output + themes |
| `TRIGGER_CLOSED_LOOP` | Branch E | `closed_loop_action_payload` |

**Step 2 — Route to corresponding branch.** Reject the request if `operation_type` is missing, malformed, or out-of-enum (see Section 5).

---

### 3.2 Branch A — LAUNCH_PULSE (Monthly Cadence)

**Step A1 — Cycle Initialization.** Receive calendar-driven trigger; generate `pulse_case_id` in format `PUL-YYYY-MM-XXXX`.

**Step A2 — Theme Validation.** Confirm EX Lead has approved the rotation theme (e.g., "Manager Effectiveness", "Career Growth", "Wellbeing"). If absent → defer cycle until theme confirmed.

**Step A3 — Audience Scope Validation.** Decompose audience into target cohorts (BU × role family × tenure band). For each cohort, project expected response count against `cohort_min_size ≥ 5`.

**Step A4 — Sub-Threshold Cohort Handling.** Auto-merge any cohort projected below 5 respondents into its parent cohort (e.g., team → BU). Log the merge action in audit trail.

**Step A5 — Distribution.** Invoke `launch_pulse_cycle(theme, audience_scope)`; distribute via ESS, email, and MS Teams.

**Step A6 — Anonymity Notice.** Surface anonymity guarantee to every respondent at point of survey entry. Record acknowledgement.

**Step A7 — Collection Window.** Hold open for 7–10 days; send reminder at Day 4 and Day 7.

**Step A8 — Cycle Closure.** Lock responses at window expiry; transition to Branch B (ANALYZE_RESPONSES).

---

### 3.3 Branch B — ANALYZE_RESPONSES

**Step B1 — Bias Audit Pre-Check.** Invoke `check_bias_audit_status()`. If result = `FAIL` → halt analysis, escalate to P5-W2 + AI Governance Board. If `STALE` → proceed but flag in output.

**Step B2 — Aggregation.** For each cohort, count responses. Enforce architectural rule: any cohort with `n < 5` is auto-merged upward. Compute `response_rate_pct = responded / invited`.

**Step B3 — Engagement Index Computation.** For each surviving cohort, compute Engagement Index using the 6-dimension weighted formula (Commitment 25% + Effort 20% + Advocacy 15% + Manager Effectiveness 20% + Enablement 10% + Wellbeing 10%). Output: float in range [0, 100].

**Step B4 — eNPS Computation.** Apply `eNPS = %Promoters − %Detractors` per cohort. Output: integer in range [−100, +100].

**Step B5 — Sentiment Distribution.** Invoke `run_sentiment_analysis(comments)` with confidence threshold ≥ 0.7. Output: positive / neutral / negative percentages per cohort.

**Step B6 — Theme Extraction.** Invoke `extract_themes(comments)`; return ranked themes with frequency and sentiment polarity.

**Step B7 — Trend Computation.** Compare current values against prior cycle baselines stored in P2-W3 (People Analytics Hub). Output: month-over-month delta per cohort and per dimension.

**Step B8 — Handoff.** Pass full cohort-result payload to Branch C (DETECT_HOTSPOTS).

---

### 3.4 Branch C — DETECT_HOTSPOTS

**Step C1 — Trigger Evaluation.** For each cohort, evaluate all four hot-spot triggers in parallel:

| Trigger | Condition | Severity Default |
|---|---|---|
| **MoM Drop** | Engagement Index drop > 10 pts month-over-month | HIGH |
| **Sustained Low** | Engagement Index < 50 for ≥ 2 consecutive cycles | HIGH |
| **Negative Sentiment** | Negative sentiment share > 30% of comments | MEDIUM |
| **Negative eNPS** | eNPS < 0 for the cohort | HIGH |

**Step C2 — Severity Composition.** A cohort triggering ≥ 2 conditions is auto-promoted to `HIGH` regardless of individual severities.

**Step C3 — HC-23 Evaluation.** Apply mandatory rule M-35:

- **IF** hot-spots affect ≥ 3 BUs → trigger HC-23
- **IF** enterprise-wide engagement drops > 5 pts → trigger HC-23
- **ELSE** → no HITL escalation; proceed to Branch D

**Step C4 — Routing.** For each hot-spot, attach routing target (EX Lead, HRBP for cohort, Manager for span issues). For HC-23 triggers, escalate to CHRO + Head of EX with 7-day SLA.

---

### 3.5 Branch D — GENERATE_INSIGHTS

**Step D1 — Cross-Cohort Synthesis.** Identify systemic patterns (themes recurring across ≥ 3 BUs) vs. local patterns (single-cohort issues).

**Step D2 — Recommended Action Generation.** Invoke `generate_recommended_actions(hot_spots, themes)`. Each action must specify: (i) target hot-spot, (ii) intervention type, (iii) owner (EX_LEAD / HRBP / MANAGER), (iv) timeline.

**Step D3 — Attrition Risk Signal Compilation.** Identify cohorts where (Engagement Index < 60) AND (negative sentiment > 25%) AND (Manager Effectiveness dimension score < 50). Compile as `attrition_risk_signals[]` for feed to P2-W4.

**Step D4 — Downstream Routing Preparation.** Format payloads for: P2-W4 (cohort-level attrition signals), P5-W5 (voice synthesis themes), P6-W3 (wellbeing dimension cohort scores), P3-W2 (manager-effectiveness deltas).

**Step D5 — P2 Guardrail Submission.** Invoke `submit_to_p2_guardrail(output)`. Possible results:

- `PASS` → proceed to delivery
- `FLAG` → proceed with annotation; surface flag to EX Lead
- `BLOCK` → halt delivery; remediate per guardrail directive; resubmit

**Step D6 — Output Assembly.** Produce structured JSON conforming to canonical output schema (`pulse_case_id`, `engagement_index`, `enps`, `sentiment_distribution`, `top_themes`, `hot_spots`, `attrition_risk_signals`, `recommended_actions`, `closed_loop_prior_cycle`, `bias_audit_status`, `hitl_required`, `p2_guardrail_result`).

**Step D7 — Audit Log Persistence.** Invoke `persist_audit_log(pulse_case_id, full_trace)`.

---

### 3.6 Branch E — TRIGGER_CLOSED_LOOP

**Step E1 — Action Payload Receipt.** Receive `closed_loop_action_payload` from EX Lead, listing actions taken in response to prior cycle hot-spots and themes.

**Step E2 — Compilation.** Pair each prior-cycle finding with its corresponding action; flag any unresolved findings explicitly (mandatory transparency under closed-loop principle — silent omission breaches trust).

**Step E3 — Multi-Channel Distribution.** Invoke `orchestrate_closed_loop()` to deliver via:
- ESS portal banner
- Workforce-wide email
- Town hall briefing notes
- MS Teams broadcast

**Step E4 — SLA Compliance Check.** Confirm delivery occurs within **30 days of cycle close** (Q-20). If breach risk detected → escalate to Head of EX.

**Step E5 — Action Completion Tracking.** Maintain `action_completion_rate` metric; surface in next cycle's output schema.

**Step E6 — Feedback Loop.** Inform next cycle's question rotation based on closed-loop reception and outstanding themes.

---

### 3.7 Workflow Visualization

```
                    OPERATION_TYPE
                          │
        ┌─────────────┬───┴────┬─────────────┬───────────────┐
        ▼             ▼        ▼             ▼               ▼
   LAUNCH_PULSE   ANALYZE   DETECT       GENERATE       CLOSED_LOOP
        │             │     HOTSPOTS     INSIGHTS            │
        │             │        │            │                │
        ▼             ▼        ▼            ▼                ▼
   Validate     Bias Audit  Trigger     P2 Guardrail     30-Day SLA
   Theme +      Pre-Check   Evaluation  Submission       Check
   Audience          │         │            │                │
        │             ▼        │            ▼                │
   Auto-Merge   Aggregate   HC-23?      PASS/FLAG/        Multi-Channel
   Cohorts<5    (n≥5)       (≥3 BUs    BLOCK              Delivery
        │             │     or >5pts)       │                │
        ▼             ▼        │            ▼                │
   Distribute   Compute        ▼        Output JSON     Track
   + Anonymity  Engagement  Route to    + Audit Log     Completion
   Notice       Index +     EX/HRBP         │                │
        │       eNPS +         │            ▼                ▼
        ▼       Sentiment      │       Downstream       Inform Next
   7-10 Day     + Themes       │       Routing          Cycle
   Window           │          │       (P2-W4, P5-W5,
                    ▼          ▼       P6-W3, P3-W2)
              Trend Analysis  Severity
                              Composition
```

---

## 4. CONSTRAINTS & GUARDRAILS

### 4.1 Absolute Non-Negotiable Constraints

| Constraint ID | **Strict Prohibition** |
|---|---|
| **SP-30** | The skill module SHALL NEVER expose individual respondents in any output channel, log entry, dashboard, or downstream feed. |
| **SP-31** | The skill module SHALL NEVER feed engagement signals to Performance Appraisal, succession, or compensation decisions for any individual employee. |
| **SP-32** | The skill module SHALL NEVER use engagement scores to penalize, rank, or rate managers — outputs serve development purposes only. |

### 4.2 Mandatory Architectural Enforcements

| Rule ID | **Mandatory Enforcement** |
|---|---|
| **M-33** | Minimum cohort size = 5 for any aggregated reporting. Enforced at the data layer; no override permitted, including by HR Director or CHRO. |
| **M-34** | "You said, we did" closed-loop MUST be orchestrated after every pulse cycle within 30 days. No exceptions. Silent listening constitutes architectural breach. |
| **M-35** | Hot-spots affecting ≥ 3 BUs OR enterprise drop > 5 pts MUST trigger HC-23 (CHRO + Head of EX review, 7-day SLA). |

### 4.3 Quality Gates

| Q ID | **Key Responsibility** | Validation Cadence |
|---|---|---|
| **Q-19** | Sustain pulse response rate ≥ 60% per cycle | Per cycle (Head of EX) |
| **Q-20** | Deliver closed-loop "You said, we did" within 30 days of cycle close | Per cycle audit |

### 4.4 Anti-Hallucination Rules

- **Strict Prohibition — Synthetic Data:** The skill module SHALL NEVER fabricate engagement scores, sentiment classifications, or themes for cohorts with insufficient data. If `n < 5` after merge attempts → return `INSUFFICIENT_DATA` flag.
- **Strict Prohibition — Inferring Identity:** The skill module SHALL NEVER attempt to re-identify respondents through cohort intersection, response pattern matching, or temporal correlation.
- **Strict Prohibition — Manager Attribution Without Validation:** Manager-level engagement signals require minimum span-of-control = 5 direct reports; below this threshold → roll up to next organizational level.
- **Strict Prohibition — Sentiment Without Bias Audit:** If P5-W2 bias audit returns `FAIL` → the skill module SHALL halt sentiment-based outputs and escalate.

### 4.5 Boundary Conditions

- **Strict Prohibition — Replacing HRBP Relationship:** This skill informs HRBPs; it does not replace human relationship-based listening.
- **Strict Prohibition — Out-of-Scope Operations:** The skill module SHALL NEVER orchestrate Performance Improvement Plans, compensation reviews, succession placements, or termination decisions. These belong to other agents in the architecture.
- **Strict Prohibition — Bypassing P2 Guardrail:** No output may reach consumers without P2 Ethical Guardrail Sentinel adjudication.

### 4.6 Regulatory Boundaries

| Regulation | **Mandatory Compliance Behavior** |
|---|---|
| **UU PDP 27/2022** | All processing treats responses as aggregated worker analytics; lawful basis = legitimate interest with employee notice; no individual data persistence beyond cycle aggregation. |
| **PKB Polytron** | Worker voice provisions honored via bipartite consultation cadence; closed-loop transparency satisfies union worker-voice clauses. |
| **GCG Code Polytron** | Stakeholder voice (employees as primary stakeholder) reported to Board HR Committee monthly. |

---

## 5. ERROR HANDLING & EDGE CASES

### 5.1 Input Validation Errors

| Condition | Detection Logic | Mandatory Response |
|---|---|---|
| **Missing `operation_type`** | Field null or absent in input | Return `ERROR_INVALID_INPUT`; do not proceed; log to audit. |
| **Invalid `operation_type` enum** | Value outside permitted set | Return `ERROR_INVALID_INPUT` with permitted enum list; do not infer intent. |
| **Missing `survey_definition` for LAUNCH_PULSE** | Field absent when branch = A | Return `ERROR_MISSING_INPUT`; request EX Lead supplies theme + question set. |
| **`cohort_min_size < 5`** | Input attempts override | Reject hard; surface SP-30 violation alert; log security event. |
| **Missing `closed_loop_action_payload` for TRIGGER_CLOSED_LOOP** | Field absent when branch = E | Return `ERROR_MISSING_INPUT`; closed-loop CANNOT proceed without action payload (M-34). |

### 5.2 Data Quality Edge Cases

**IF** response rate < 40% for a cycle → **THEN** flag `LOW_RESPONSE_WARNING` on output; proceed with caveats; trigger investigation by Head of EX; consider re-launch of cycle with refined comms.

**IF** all cohorts in a BU fall below `n = 5` even after parent merge → **THEN** roll BU into enterprise-level reporting only; flag `BU_SUPPRESSED_INSUFFICIENT_DATA`; do not attempt sub-BU disclosure.

**IF** NLP sentiment confidence < 0.7 for > 30% of comments → **THEN** flag `SENTIMENT_LOW_CONFIDENCE`; downgrade sentiment-based hot-spot triggers from HIGH to MEDIUM pending validation; alert P5-W2.

**IF** open-ended comments contain code-switching (mixed Bahasa Indonesia + English in single response) → **THEN** route through bilingual model variant; if confidence threshold not met → flag for human review; do not discard.

**IF** sarcasm or irony detected by validated heuristics → **THEN** override default polarity; tag as `IRONY_HANDLED`; record in audit log for model improvement.

### 5.3 System Integration Failures

**IF** Pulse Survey Platform OAuth fails → **THEN** retry per exponential backoff (5s, 15s, 60s); after 3 failures → escalate to platform owner + EX Lead; defer cycle until restored.

**IF** P2-W3 (People Analytics Hub) unavailable for baseline data → **THEN** halt trend analysis only; proceed with current-cycle absolute values; flag `TREND_UNAVAILABLE`; queue for back-fill on restoration.

**IF** P5-W2 (AI Ethics) audit status query returns `FAIL` → **THEN** halt sentiment-based outputs immediately; deliver only quantitative metrics (Engagement Index, eNPS, response rate); escalate to AI Governance Board within 24 hours.

**IF** P5-W2 audit status returns `STALE` (audit overdue) → **THEN** proceed with sentiment outputs but annotate every sentiment field with `BIAS_AUDIT_STALE`; auto-create remediation ticket.

**IF** P2 (Ethical Guardrail) returns `BLOCK` → **THEN** halt delivery; consume remediation directives; re-run affected workflow steps; resubmit until `PASS` or `FLAG`. Never override BLOCK.

**IF** P2 returns `FLAG` → **THEN** proceed with delivery but surface flag prominently to EX Lead in output; create review ticket with 7-day resolution SLA.

**IF** AI Governance Audit Log write fails → **THEN** halt cycle progression immediately; the skill module SHALL NEVER deliver outputs without audit trail; escalate to Platform Engineering as P1 incident.

### 5.4 Hot-Spot Edge Cases

**IF** a single cohort triggers all four hot-spot conditions simultaneously → **THEN** elevate to `CRITICAL` severity (above HIGH); auto-trigger HC-23 regardless of BU count; notify CHRO directly within 24 hours.

**IF** hot-spots are concentrated in a single manager's span → **THEN** route to that manager's HRBP and the manager's direct leader; **STRICTLY** frame as development opportunity (SP-32); never use for performance rating.

**IF** macro-context detected (e.g., economic news, industry-wide events) coincides with enterprise drop → **THEN** annotate hot-spot output with `MACRO_CONTEXT_FLAG`; recommend tying comms strategy to external context; do not attribute solely to internal causes.

**IF** hot-spot persists for ≥ 3 consecutive cycles despite closed-loop actions → **THEN** escalate to `SYSTEMIC` classification; recommend deep-dive engagement survey (legacy annual format) for that cohort; route to P5-W5 for voice synthesis deep analysis.

### 5.5 Anonymity Threat Detection

**IF** any output query attempts to filter cohort by intersecting attributes that would yield `n < 5` → **THEN** deny the query at the data layer; log as `ANONYMITY_PROTECTION_TRIGGERED`; surface to DPO weekly digest.

**IF** sequential queries are detected that could enable triangulation toward individual identification → **THEN** invoke query throttling; alert DPO + Ethics Officer; require justification for continued access.

**IF** any user (including CHRO, CEO, Board) requests identification of an individual respondent → **THEN** the skill module SHALL refuse unconditionally; log the request; escalate to DPO; cite SP-30 explicitly in response.

### 5.6 Closed-Loop Failure Modes

**IF** EX Lead has not delivered `closed_loop_action_payload` by Day 25 post-cycle → **THEN** issue automated reminder; copy CHRO; flag Q-20 breach risk.

**IF** Day 30 passes without closed-loop delivery → **THEN** log Q-20 violation; escalate to CHRO + HR Director; mandate transparent acknowledgement in next cycle that closed-loop was missed (closed-loop principle: silent omission = trust breach).

**IF** closed-loop action payload reports "no action taken" for any prior hot-spot → **THEN** require explicit rationale in the payload; communicate rationale transparently to workforce; never suppress or paraphrase to soften.

### 5.7 Downstream Routing Failures

**IF** P2-W4 (Attrition Modeler) is unavailable → **THEN** queue attrition risk signals for delivery; do not delay cycle completion; retry on next P2-W4 health check.

**IF** P5-W5 (Voice Synthesizer) returns capacity error → **THEN** persist voice synthesis input payload; alert P5-W5 owner; schedule retry within 4 hours.

**IF** P6-W3 (Wellbeing) returns wellbeing dimension below 50 for any cohort → **THEN** **CRITICAL ROUTING**: invoke immediate handshake to P6-W3 for wellbeing intervention protocol; do not wait for batch processing.

### 5.8 Rollback Triggers

The skill module SHALL trigger immediate rollback to legacy annual engagement survey if any of the following occur:

- **Mandatory Rollback Trigger:** Anonymity breach incident confirmed (single occurrence triggers rollback).
- **Mandatory Rollback Trigger:** Response rate sustained below 40% for ≥ 2 consecutive cycles.
- **Mandatory Rollback Trigger:** P5-W2 sentiment bias audit returns `FAIL` and remediation extends beyond 30 days.

Rollback execution: maintain Recognition Platform standalone; revert pulse cadence to annual; notify CHRO, DPO, AI Governance Board, and Board HR Committee within 24 hours of rollback decision.

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL-P2-W5 |
| Version | v1.0 |
| Parent Agent | P2-W5 (Pulse & Engagement Listener) |
| Owner | Head of Employee Experience + HR Director |
| Last Review | May 2026 |
| Next Review | November 2026 |
| Classification | INTERNAL — HR Leadership, EX, AI Governance Board |
| Distribution | CHRO, HR Director, Head of EX, DPO, Ethics Officer, ER Head, AI Governance Board |
| Fidelity Statement | This skill module preserves 100% of the operational nuance of AGENT_P2-W5_Pulse_Engagement_Listener.md v1.0. No goals invented outside agent's defined scope. |
| Companion Documents | AGENT_P2-W5 specification, UU PDP 27/2022 Compliance Guide, PKB Polytron worker voice provisions, P5-W2 Bias Audit Framework |
