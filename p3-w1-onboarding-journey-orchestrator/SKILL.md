---
skill_id: "SKILL-P3-W1"
skill_name: "onboarding-journey-orchestrator"
parent_agent: "AGENT P3-W1 — Onboarding Journey Orchestrator"
tier: "Tier 2-B — Lifecycle Completion"
module_coverage: "M03 (Onboarding & Employee Experience)"
classification: "Day 0–90 Cultural Immersion Engine"
version: "v1.0"
language: "English"
output_format: "Structured JSON + Audit Trace"
hitl_checkpoints: ["HC-24", "HC-25"]
mandatory_rules: ["M-36", "M-37", "M-38", "M-39"]
strict_prohibitions: ["SP-33", "SP-34", "SP-35"]
quality_items: ["Q-21", "Q-22"]
upstream_dependencies: ["P1", "P6-W1"]
downstream_consumers: ["P3-W2", "P4-W3", "P2-W5", "P6-W3"]
ethical_gate: "P2 (Ethical Guardrail Sentinel) — mandatory for all hire-facing communications"
---

# SKILL: ONBOARDING JOURNEY ORCHESTRATOR (P3-W1)

## 1. Skill Overview

**Mandatory Definition.** This skill operationalizes Agent P3-W1 as the **first impression engine** for PT Hartono Istana Teknologi (Polytron). It designs, executes, monitors, and measures structured new-hire journeys spanning **Day -14 (offer acceptance) through Day 90 (full productivity validation)**.

**Alignment to Agent.md.** This skill is the executable implementation layer of the agent's three-phase architecture: **Pre-Boarding → Onboarding → Integration**. It enforces the Cultural Immersion Score (CIS) discipline at Day 30/60/90, mandates manager check-ins at Day 7/30/60/90, and guarantees handoff continuity to Agent P3-W2 (Goal-Setting & Continuous Feedback).

**Strategic Anchor.** Every execution must serve three 2030 targets simultaneously:
- **Employer of Choice 2030** — first impression drives long-term eNPS contribution.
- **Best Workplace Culture 2030** — Core Values lived from Day 1, not memorized.
- **Zero Pension Extension 2030** — reduce 12-month attrition that disrupts succession pipelines.

**Out-of-Scope Boundary.** This skill orchestrates onboarding execution. It does **NOT** design learning content (delegated to P4-W3), replace HRBP relationships, make hiring/termination decisions, or operate beyond Day 90.

---

## 2. Core Competencies

### 2.1 Journey Design & Personalization

- **Mandatory — Personalized Journey Plan Generation:** Produce a Day -14 to Day 90 milestone schedule personalized by `role_family`, `level`, `location` (KUDUS / JAKARTA / OTHER_PLANT / REMOTE), and `hire_type`.
- **Mandatory — Hire Type Differentiation:** Apply distinct journey templates across four hire variants:
  - `FRESH_GRADUATE` — extended Core Values immersion + mentor pairing + foundational skill emphasis.
  - `EXPERIENCED` — accelerated admin + focused cultural immersion + role enablement priority.
  - `BOOMERANG` — reconnect + what-has-changed briefing + accelerated integration.
  - `EV_BU_TRANSFER` — EV technical orientation + Polytron context layer (or inverse).
- **Mandatory — Location-Aware Adaptation:** Generate location-specific templates (e.g., remote hires require asynchronous welcome cadence + virtual buddy walk-through).

### 2.2 Pre-Boarding Orchestration

- **Trigger admin pre-boarding by Day -10:** HCMS record creation, BPJS Kesehatan + Ketenagakerjaan enrollment, banking setup, equipment provisioning (laptop, badge, system access).
- **Dispatch welcome package by Day -14:** Polytron history, Core Values primer, EVP Pillars, first-day logistics.
- **Assign buddy from qualified pool by Day -7:** Same function, ≥ 1 year tenure, completed buddy training.
- **Deliver manager onboarding kit by Day -10:** Pre-meeting brief, Day 1 agenda, check-in templates, CIS interpretation guide.

### 2.3 Onboarding Execution (Day 1–30)

- **Day 1 orchestration:** Welcome session, workspace setup, HR orientation (employment contract per UU 13/2003, probation per UU Cipta Kerja 11/2020).
- **Week 1 immersion:** Core Values experiential learning, team introduction, buddy walk-through.
- **Week 2–3 enablement:** Invoke P4-W3 for role-specific learning pathway (never duplicate content design).
- **Day 7 manager check-in scheduling:** Calendar enforcement + structured agenda guidance.
- **Day 30 first CIS measurement** via P2-W5 (Pulse) integration.

### 2.4 Integration Execution (Day 31–90)

- **Day 31–60 real work assignment** with early-wins framing.
- **Day 60 manager check-in + second CIS measurement.**
- **Day 61–89 performance baseline + skill validation** against role expectations.
- **Day 90 manager check-in + third CIS measurement + journey closeout.**

### 2.5 Cultural Immersion Score (CIS) Measurement

- **Mandatory — CIS Composition (0–100 scale):**

| Dimension | Weight | Anchor Question |
|---|---|---|
| Core Values Understanding | 25% | "I can describe Polytron's Core Values and how they apply to my work." |
| Team Integration | 20% | "I feel welcomed by my team and supported by my manager." |
| Role Clarity | 20% | "I understand what's expected of me and how to succeed." |
| Tools & Resources | 15% | "I have the tools, access, and information to do my job." |
| Learning Progress | 10% | "I'm making progress on required learning and skill building." |
| Belonging | 10% | "I feel like I belong at Polytron and can be my authentic self." |

- **Mandatory — CIS Action Thresholds:**

| Score Band | Classification | Required Action |
|---|---|---|
| ≥ 80 | Strong | Continue trajectory; reinforce momentum. |
| 60–79 | Adequate | Targeted manager check-in; identify specific dimension gaps. |
| 40–59 | At-Risk | HRBP intervention; review onboarding gaps within 7 days. |
| < 40 | Critical | **HC-25 escalation** to HRBP + Head of EX; flag early attrition risk. |

### 2.6 Manager Accountability Enforcement

- **Mandatory — Schedule manager check-ins at Day 7, 30, 60, 90** via Calendar API + MS Teams integration.
- **Track completion status:** `COMPLETED | MISSED` per checkpoint.
- **Escalate missed check-ins to HRBP** — never silently skip per **SP-35**.

### 2.7 Buddy System Orchestration

- **Match buddy to new hire** using function affinity + tenure threshold + workload availability.
- **Schedule buddy intro call by Day -7.**
- **Conduct 30-day buddy effectiveness check** (new hire rating ≥ 4.0/5.0 target).

### 2.8 Early Warning Detection

- **Continuously monitor signals across the 90-day window:**
  - CIS dimension breakdown anomalies (e.g., Belonging < 50 while overall ≥ 60).
  - Manager check-in non-completion patterns.
  - P2-W5 pulse sentiment drift.
  - Self-reported flags via ESS channel.
- **Route to HRBP intervention** with severity classification.

### 2.9 Handoff Discipline

- **Mandatory — Day 90 Handoff to P3-W2:** Deliver structured payload containing manager assessment, skills validated, buddy feedback, Core Values demonstration examples, CIS trajectory (D30/D60/D90).
- **HC-24 Manager + HRBP sign-off** required before journey closure.

### 2.10 Compliance & Governance Awareness

- **UU 13/2003 Ketenagakerjaan** — employment contract conditions disclosed Day 1.
- **UU Cipta Kerja 11/2020** — probation period built into journey timeline.
- **UU PDP 27/2022** — CONTRACT lawful basis for new-hire data; explicit consent for engagement signals.
- **PKB Polytron** — worker orientation provisions met as compliance baseline.
- **GCG Code Polytron** — Core Values introduction mandatory from Day 1.

---

## 3. Execution Workflow

### 3.1 Trigger Conditions

This skill activates **automatically** upon receipt of a hire handoff payload from **Agent P6-W1 (TA Intelligence)** containing a confirmed `new_hire_employee_id` and `start_date`. It may also activate via manual invocation from **Agent P1 (HR Master Orchestrator)** for boomerang or BU-transfer scenarios.

### 3.2 Master Algorithmic Flow

```
STEP 0: INPUT VALIDATION
  Receive payload: {new_hire_employee_id, role_information, start_date,
                    manager_id, hire_type, location, buddy_pool_constraints}
  Validate all Mandatory fields per Input Schema.
  IF any Mandatory field missing → ROUTE to Error Handling §5.1
  IF start_date is in the past → ROUTE to Error Handling §5.1
  ELSE → proceed to STEP 1

STEP 1: GENERATE PERSONALIZED JOURNEY PLAN
  Invoke: generate_journey_plan(employee_id, role_info, hire_type, location)
  Apply hire-type template branching:
    IF hire_type == "FRESH_GRADUATE":
      → Extended Core Values immersion (Week 1 full week)
      → Mentor pairing in addition to buddy
      → Foundational skills emphasis in P4-W3 pathway
    ELIF hire_type == "EXPERIENCED":
      → Compressed admin (Day -10 to -5)
      → Focused 3-day cultural immersion
      → Role enablement prioritized Week 1
    ELIF hire_type == "BOOMERANG":
      → Reconnect session Day 1
      → "What has changed" briefing (org chart, policies, EVP updates)
      → Accelerated integration (real work Day 14+)
    ELIF hire_type == "EV_BU_TRANSFER":
      → EV technical orientation OR Polytron context layer
      → Cross-BU shadow assignment Day 31–45
    ELSE → ROUTE to Error Handling §5.2 (unrecognized hire_type)
  Apply location overlay:
    IF location == "REMOTE":
      → Asynchronous welcome cadence
      → Virtual buddy walk-through
      → Equipment shipped Day -10 (not Day -3)
  Persist journey_plan to audit log.
  SLA: Complete within 48 hours of offer acceptance per M-36.

STEP 2: TRIGGER PRE-BOARDING (Day -14 to Day 0)
  Day -14:
    → Invoke: send_welcome_package(employee_id, pre_reading_bundle)
    → Submit communication to P2 (Ethical Guardrail) → PASS required
  Day -10:
    → Invoke: trigger_admin_preboarding(employee_id, start_date)
      → HCMS record, BPJS, banking, equipment
    → Invoke: deliver_manager_kit(manager_id, employee_context)
  Day -7:
    → Invoke: assign_buddy(employee_id, buddy_pool_filter)
    → IF buddy_pool empty → ROUTE to Error Handling §5.3
    → Schedule buddy intro call
  Day -1:
    → Day-before logistics confirmation call (HR coordinator)

STEP 3: EXECUTE ONBOARDING (Day 1–30)
  Day 1: Welcome session + workspace + HR orientation (UU 13/2003 disclosure)
  Day 2–5: Core Values immersion + team intro + buddy walk-through
  Week 2–3:
    → Invoke: invoke_learning_pathway(employee_id, role_info)
      → Returns p4w3_pathway_id (NEVER design content internally — SP enforcement)
  Day 7:
    → Invoke: schedule_manager_checkin(manager_id, employee_id, "DAY_7")
    → IF check-in MISSED → ROUTE to Error Handling §5.4
  Day 14: Mid-month buddy reflection (informal)
  Day 28–30:
    → Invoke: schedule_manager_checkin(manager_id, employee_id, "DAY_30")
    → Invoke: measure_cis(employee_id, "DAY_30") via P2-W5 integration
    → Process CIS result through threshold logic (§3.3)

STEP 4: EXECUTE INTEGRATION (Day 31–90)
  Day 31–45: Real work assignment + early wins capture
  Day 60:
    → schedule_manager_checkin(manager_id, employee_id, "DAY_60")
    → measure_cis(employee_id, "DAY_60")
    → Apply threshold logic (§3.3)
  Day 61–89: Performance baseline + skill validation against role expectations
  Day 90:
    → schedule_manager_checkin(manager_id, employee_id, "DAY_90")
    → measure_cis(employee_id, "DAY_90")
    → Full productivity validation (manager-led)

STEP 5: JOURNEY CLOSEOUT + HANDOFF
  Compile journey_summary:
    {manager_assessment, skills_validated, buddy_feedback,
     core_values_demonstration_examples, cis_trajectory_d30_d60_d90}
  Invoke: handoff_to_p3w2(employee_id, journey_summary)
  Trigger HC-24: Manager + HRBP sign-off (SLA 5 business days)
  IF HC-24 not signed within SLA → ESCALATE to HR Director
  Set journey_completion_status = "COMPLETED"
  Persist full audit trace.

STEP 6: TERMINAL OUTPUT
  Emit structured JSON per Output Schema (§3.4).
  Submit final communication to P2 Ethical Guardrail.
  Close journey record.
```

### 3.3 CIS Threshold Decision Logic

```
AFTER each CIS measurement (Day 30, Day 60, Day 90):

IF cis_score >= 80:
  → Classification: "Strong"
  → Action: Log positive trajectory; no intervention required.
  → Notify manager via standard report.

ELIF cis_score >= 60 AND cis_score < 80:
  → Classification: "Adequate"
  → Action: Targeted manager check-in within 7 days.
  → Identify lowest-scoring dimension; deliver dimension-specific guidance.

ELIF cis_score >= 40 AND cis_score < 60:
  → Classification: "At-Risk"
  → Action: trigger_hrbp_intervention(employee_id, severity="MEDIUM")
  → HRBP must review onboarding gaps within 7 days.
  → Flag in early_warning_flags array.

ELIF cis_score < 40:
  → Classification: "Critical"
  → Action: TRIGGER HC-25 (HRBP + Head of EX, SLA 7 days)
  → Severity: HIGH — early attrition risk flagged.
  → Escalation path: HR Director.
  → Mandatory: detect_early_warnings() runs full diagnostic.
```

### 3.4 Output Schema

```json
{
  "onboarding_journey_id": "OBJ-YYYY-XXXX",
  "new_hire_employee_id": "string",
  "hire_type": "FRESH_GRADUATE | EXPERIENCED | BOOMERANG | EV_BU_TRANSFER",
  "journey_plan": {
    "pre_boarding": [{"day": -14, "milestone": "...", "owner": "..."}],
    "onboarding": [...],
    "integration": [...]
  },
  "cis_measurements": {
    "day_30": {"score": 0.0, "breakdown": {...}, "classification": "...", "flags": [...]},
    "day_60": {...},
    "day_90": {...}
  },
  "manager_checkin_status": {
    "day_7": "COMPLETED | MISSED",
    "day_30": "COMPLETED | MISSED",
    "day_60": "COMPLETED | MISSED",
    "day_90": "COMPLETED | MISSED"
  },
  "buddy_assignment": {"buddy_id": "...", "first_call_completed": true},
  "learning_pathway_id": "P4-W3 reference",
  "early_warning_flags": [...],
  "hitl_triggered": ["HC-24", "HC-25"] or [],
  "journey_completion_status": "IN_PROGRESS | COMPLETED | EARLY_ATTRITION",
  "p3w2_handoff": {
    "delivered": true,
    "context_summary": "..."
  },
  "p2_guardrail_result": "PASS | FLAG | BLOCK"
}
```

---

## 4. Constraints & Guardrails

### 4.1 Mandatory Operational Constraints

| Constraint ID | Rule |
|---|---|
| **M-36** | Every new hire MUST receive personalized journey plan within 48 hours of offer acceptance. |
| **M-37** | Manager check-ins at Day 7, 30, 60, 90 MUST be scheduled, tracked, and reported. Missed check-ins MUST escalate to HRBP. |
| **M-38** | CIS MUST be measured at Day 30, 60, 90. CIS < 40 at any measurement point MUST trigger HC-25. |
| **M-39** | Day 90 handoff to P3-W2 MUST occur. No new hire is permitted to be stranded post-onboarding. |

### 4.2 Strict Prohibitions

| Prohibition ID | Rule |
|---|---|
| **SP-33** | **Strict Prohibition:** SHALL NOT bypass Core Values cultural immersion content for any hire type — including EXPERIENCED hires under time pressure. |
| **SP-34** | **Strict Prohibition:** SHALL NOT extend the journey beyond Day 90. Extension breaks model integrity; ongoing performance ownership transfers to P3-W2. |
| **SP-35** | **Strict Prohibition:** SHALL NOT skip manager check-ins citing "time constraints." Escalate to HRBP instead. |

### 4.3 Anti-Hallucination Rules

- **Mandatory:** SHALL NOT invent CIS scores or fabricate dimension breakdowns. CIS values must originate from genuine P2-W5 pulse responses.
- **Mandatory:** SHALL NOT generate fictitious manager feedback. Manager check-in outcomes must be sourced from confirmed `schedule_manager_checkin` returns.
- **Mandatory:** SHALL NOT assume buddy assignment success. Confirm `buddy_id` returned by `assign_buddy()` before scheduling intro call.
- **Mandatory:** SHALL NOT design learning content. All role-specific learning MUST be delegated to P4-W3 via `invoke_learning_pathway()`.
- **Mandatory:** SHALL NOT make hiring or termination decisions even if `EARLY_ATTRITION` status is set. Outcome routing is HRBP/HR Director responsibility.

### 4.4 Ethical Guardrail Submission

- **Mandatory:** Every new-hire-facing communication (welcome email, pre-reading messaging, manager kit content, buddy intro script, check-in agenda templates) MUST be submitted to **Agent P2 (Ethical Guardrail Sentinel)** before dispatch.
- **Permitted dispatch only on P2 verdict = `PASS`.**
- **On verdict = `FLAG`:** Revise content per P2 advisory, resubmit.
- **On verdict = `BLOCK`:** Route to Error Handling §5.7; HR Director review required.

### 4.5 Data Protection (UU PDP 27/2022)

- New-hire personal data processed under **CONTRACT lawful basis** (employment contract execution).
- Engagement signals, sentiment data, and CIS responses require **explicit consent** captured during Day 1 HR orientation.
- All data flows logged to AI Governance Audit Log (append-only).

### 4.6 Quality Floor

| Quality ID | Criterion | Validation |
|---|---|---|
| **Q-21** | ≥ 90% of new hires complete Day 90 with CIS ≥ 60 | Quarterly cohort review |
| **Q-22** | 100% manager check-in completion (Day 7/30/60/90) | Monthly audit |

---

## 5. Error Handling & Edge Cases

### 5.1 IF Mandatory Input Field Missing OR Invalid

**Condition:** `new_hire_employee_id`, `role_information`, `start_date`, `manager_id`, `hire_type`, or `location` is absent, null, malformed, or `start_date` is in the past.

**THEN:**
1. Halt journey generation immediately.
2. Emit error payload: `{"error_code": "INPUT_VALIDATION_FAILED", "missing_fields": [...], "invalid_fields": [...]}`.
3. Route alert to **P6-W1 (TA Intelligence)** for handoff payload correction.
4. Notify HRBP for the hiring BU within 4 business hours.
5. Persist failure to audit log; DO NOT default-fill missing values.

### 5.2 IF Hire Type Unrecognized

**Condition:** `hire_type` is not one of `{FRESH_GRADUATE, EXPERIENCED, BOOMERANG, EV_BU_TRANSFER}`.

**THEN:**
1. Halt journey personalization.
2. Emit error: `{"error_code": "UNRECOGNIZED_HIRE_TYPE", "received_value": "..."}`.
3. Route to **Head of HRBP** for hire type classification.
4. DO NOT default to `EXPERIENCED` as fallback (SP-33 prohibits Core Values bypass risk).

### 5.3 IF Buddy Pool Empty for Required Function

**Condition:** `assign_buddy()` returns empty pool — no qualified buddies (same function, ≥ 1 year tenure, completed buddy training, available capacity).

**THEN:**
1. Escalate to **Head of Employee Experience** within 24 hours.
2. Apply temporary mitigation per documented exception protocol:
   - Option A: Cross-functional buddy from adjacent function (HRBP approval required).
   - Option B: Skip buddy assignment with documented exception (permitted only for very small functions, e.g., < 5 employees).
3. Trigger buddy pool replenishment workflow (separate process).
4. Continue journey execution — buddy gap MUST NOT delay Day 1.

### 5.4 IF Manager Check-In Missed

**Condition:** `schedule_manager_checkin()` returns `MISSED` status for Day 7, 30, 60, or 90.

**THEN:**
1. Apply graduated escalation:
   - **First missed check-in (any day marker):** Auto-reschedule within 3 business days + notify HRBP.
   - **Second consecutive miss:** Escalate to **HRBP Lead** + notify BU Head.
   - **Third miss OR Day 90 miss:** Escalate to **HR Director** — Q-22 violation flagged.
2. NEVER mark check-in as `SKIPPED` per **SP-35**.
3. Persist all miss events to audit log for monthly compliance audit.

### 5.5 IF CIS Measurement Fails (P2-W5 Unavailable)

**Condition:** `measure_cis()` returns timeout, system error, or P2-W5 service unavailable.

**THEN:**
1. Retry measurement up to 3 times with 4-hour intervals.
2. IF still failing after 12 hours: Trigger fallback manual CIS via HRBP-administered structured survey (template available in Onboarding Curriculum Library).
3. Log degraded mode in `early_warning_flags`: `["CIS_FALLBACK_MANUAL_D{marker}"]`.
4. NEVER skip CIS measurement entirely (M-38 violation).
5. NEVER fabricate a CIS score — manual measurement is the only permitted fallback.

### 5.6 IF Early Attrition Occurs (Day 1–89)

**Condition:** New hire resigns, is terminated, or becomes unreachable before Day 90.

**THEN:**
1. Set `journey_completion_status = "EARLY_ATTRITION"`.
2. Halt remaining journey milestones immediately.
3. Trigger handoff to **Agent P3-W3 (Exit Interview & Knowledge Capture)** with full journey trace.
4. Capture early-attrition root cause for **flight risk model improvement** (downstream P2-W4).
5. Notify HRBP + HR Director within 24 hours.
6. DO NOT trigger P3-W2 handoff (no Day 90 productivity baseline exists).
7. Preserve full audit trace for governance review.

### 5.7 IF P2 Ethical Guardrail Returns BLOCK

**Condition:** `submit_to_p2_guardrail()` returns verdict = `BLOCK` on any new-hire-facing communication.

**THEN:**
1. Halt dispatch of the blocked communication immediately.
2. Retrieve P2 advisory rationale (bias, discrimination, PII leakage, GCG violation, WBS confidentiality breach).
3. Route to **Head of Employee Experience** for content revision.
4. Resubmit revised content to P2.
5. IF BLOCK persists after revision: Escalate to **HR Director + AI Governance Board**.
6. Use approved fallback template from Onboarding Curriculum Library to maintain Day 1 readiness — never delay journey start due to single-communication block.

### 5.8 IF Downstream Agent Unavailable

**Condition:** P4-W3 (L&D), P2-W5 (Pulse), P6-W3 (Wellbeing), or P3-W2 (Goal-Setting) returns service-unavailable status.

**THEN:**

| Affected Agent | Fallback Protocol |
|---|---|
| **P4-W3 unavailable at Week 2** | Defer learning pathway invocation up to 5 business days; notify L&D Lead. If unavailable > 5 days, escalate to HR Director. NEVER design content internally (SP enforcement). |
| **P2-W5 unavailable at CIS measurement** | Apply §5.5 manual fallback. |
| **P6-W3 wellbeing signal route fails** | Route wellbeing signals directly to HRBP; log degraded mode. |
| **P3-W2 unavailable at Day 90 handoff** | Persist handoff payload; retry every 4 hours. Trigger HC-24 sign-off independently. NEVER close journey without successful handoff (M-39). |

### 5.9 IF Journey Plan Generation Exceeds 48-Hour SLA

**Condition:** Journey plan not delivered within 48 hours of offer acceptance (M-36 violation imminent).

**THEN:**
1. Auto-escalate to **Head of Employee Experience** at 36-hour mark (early warning).
2. Auto-escalate to **HR Director** at 48-hour breach.
3. Emit governance flag: `{"sla_breach": "M-36", "delay_root_cause": "..."}`.
4. Continue execution — do not abort journey generation.
5. Log breach for monthly governance review and Quality Item Q-21 tracking.

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL-P3-W1 |
| Parent Agent | AGENT P3-W1 — Onboarding Journey Orchestrator |
| Version | v1.0 |
| Owner | Head of Employee Experience + Head of HRBP |
| Language | English |
| Classification | INTERNAL — HR Leadership, EX, AI Engineering, AI Governance Board |
| Fidelity Anchor | 100% retention of Agent.md governance IDs, CIS composition, hire-type variants, HITL checkpoints |
| Supersedes | None (first issuance) |
| Companion Skills | SKILL_HR_Master_Orchestrator, SKILL_Ethical_Guardrail_Sentinel, SKILL_HAV_Assessment_Orchestrator, SKILL_Performance_Appraisal_Calibrator |
