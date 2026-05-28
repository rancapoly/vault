---
skill_id: "SKILL-P4W4"
skill_name: "internal-talent-marketplace-engine"
skill_display_name: "Internal Talent Marketplace Engine — Execution Skill Module"
agent_id: "P4-W4"
agent_tier: "Tier 2-C — Optimization & Scale"
classification: "Mobility Engine"
module_coverage: ["M07 (OD — Internal Mobility)", "M02 (TA — Internal-First Hiring)"]
version: "v1.0"
language: "English"
status: "PRODUCTION-READY"
owner: "Head of OD + Head of Talent Management"
last_updated: "May 2026"
---

# SKILL MODULE: INTERNAL TALENT MARKETPLACE ENGINE
## Agent P4-W4 | Polytron Enterprise HR Agentic AI Architecture

---

## 1. Skill Overview

### 1.1 Alignment with Agent P4-W4 Core Directive

This skill module operationalizes the **Internal Talent Marketplace Engine (Agent P4-W4)** — the Tier 2-C Mobility Engine within PT Hartono Istana Teknologi (Polytron)'s 30-agent HR Agentic AI Architecture. The skill translates P4-W4's high-level mandate into **concrete, executable competencies, decision logic, and guardrail enforcement protocols**.

**Strategic Anchor:** P4-W4 exists to dismantle Polytron's legacy career model of manager-discretion and manual referral — which produced hidden opportunities, hidden talent, career stagnation, and reorg waste. This skill module ensures every operation P4-W4 performs advances four 2030 strategic targets:

| 2030 Target | P4-W4 Contribution |
|---|---|
| **Employer of Choice 2030** | Career mobility as top-3 employee value driver; transparent marketplace |
| **Zero Pension Extension 2030** | Experienced talent retained via lateral + role-evolving moves |
| **Best Workplace Culture 2030** | Internal-first hiring signals organizational trust in workforce |
| **EV BU Capability Build** | Existing Polytron talent reskilled for EV roles — faster + cheaper than external hiring |

### 1.2 Skill Functional Scope

**IN-SCOPE (Mandatory Execution):**
- Internal opportunity lifecycle management (post → match → apply → decide → execute → track)
- Skill-based candidate matching via P2-W2 Skills Taxonomy
- Internal-first hiring enforcement (minimum 2-week posting window)
- Manager retention veto adjudication with HRBP arbitration
- Close-fit reskill pathway invocation (P4-W3)
- Compensation alignment triggering (P3-W4) on mobility
- Reorg-displaced talent priority routing from P3-W5
- Senior leader mobility (L11+) governance via HC-41
- Mobility outcome tracking and analytics generation

**OUT-OF-SCOPE (Hard Exclusions):**
- ❌ External job advertisement posting — delegated to P6-W1
- ❌ Compensation setting or adjustment — delegated to P3-W4
- ❌ Final hiring decisions — authority rests with Manager + HRBP
- ❌ Protected-attribute-based filtering in any matching or search function

### 1.3 Opportunity Type Coverage

P4-W4 manages the following four opportunity categories:

| Opportunity Type | Duration | Examples |
|---|---|---|
| **Full-Time Roles** | Permanent | Promotions, lateral moves, reskill-and-move |
| **Gig Projects** | 1–6 months | Cross-functional projects, capacity fills, skill-stretch |
| **Rotations** | 6–12 months | Department, BU (e.g., Manufacturing → EV BU), geographic (Kudus ↔ Jakarta ↔ overseas), functional |
| **Mentorship** | Ongoing | Reverse mentorship (junior → senior on digital/AI), cross-generational, skills exchange |

---

## 2. Core Competencies

### 2.1 Marketplace Listing Management

- **Competency:** Receive, validate, and publish internal opportunity listings for all four opportunity types (Full-Time, Gig, Rotation, Mentorship).
- **Execution Standard:** Every opportunity payload MUST be validated against P2-W2 Skills Taxonomy references before publication. Incomplete or discriminatory payloads are rejected at intake.
- **Internal Posting Window:** Enforce minimum 14-calendar-day internal-only visibility. P6-W1 external sourcing unlock MUST NOT occur before `external_sourcing_unlock_date` is reached. Exception: CEO-approved senior external search may be posted simultaneously but does NOT bypass the internal window.
- **Auto-Notification:** On publication, auto-notify all employees whose P2-W2 skill profiles and career aspirations align with the opportunity's skill requirements.

### 2.2 Skill-Based Candidate Matching

- **Competency:** Execute multi-factor matching algorithm against every active marketplace listing, producing ranked candidate lists.
- **Matching Logic:**

| Scoring Component | Weight | Logic |
|---|---|---|
| **Required Skills Match** | Primary | % of required skills matched × proficiency alignment score |
| **Aspiration Alignment** | Booster | Score boost if opportunity aligns with employee-stated career goals; soft factor, never gating |
| **Eligibility Gate** | Binary | Tenure ≥ 12 months; PA Category not C (or HRBP override); no active PIP; no blocking retention veto |
| **Diversity + Equity Overlay** | Audit Layer | Audit shortlist for demographic representation; surface anomalies to HRBP; NEVER filter by protected attribute |

- **Score Classification:**

| Match Score | Classification | Action |
|---|---|---|
| ≥ 80% | **STRONG_MATCH** | Deliver to shortlist; notify candidate to apply |
| 60–79% | **MATCH_WITH_GROWTH** | Deliver with growth note; consider P4-W3 reskill track |
| < 60% | **RESKILL_CANDIDATE** | Route to P4-W3 if employee interest confirmed; do not discard |

### 2.3 Employee Eligibility Validation

- **Competency:** Execute pre-application eligibility check for every internal application.
- **Default Criteria (overridable by HRBP with documented rationale):**
  - **Tenure:** ≥ 12 months in current role
  - **Performance:** PA Category A or B (Category C eligible only with HRBP override + documented rationale)
  - **PIP Status:** No active Performance Improvement Plan
  - **Veto Status:** No validated, unexpired manager retention veto blocking the move
- **Output:** `ELIGIBLE` | `RESKILL_NEEDED` | `INELIGIBLE` per application. INELIGIBLE decisions MUST include stated reason for HRBP review.

### 2.4 Manager Retention Veto Adjudication

- **Competency:** Receive, evaluate, and adjudicate manager retention veto submissions against strict business-critical criteria.
- **Valid Veto Grounds (Manager must document one of the following):**
  - Employee is leading a mission-critical project with a defined end date
  - Employee holds irreplaceable subject-matter expertise with a succession timeline
  - Active customer commitment dependent on employee's specific continuity
- **Veto Duration:** Maximum 6 months. Veto without end date is invalid.
- **Adjudication Path:**
  - HRBP reviews justification → Decision: `UPHELD` or `OVERRIDDEN` with documented rationale
  - Disputed decisions → HC-40 (HR Director + Head of OD; 7-day SLA; escalation: CHRO)
- **Key Principle:** Manager cannot block mobility permanently. Veto is a delay mechanism, not a denial mechanism.

### 2.5 Reskill Pathway Invocation (P4-W3 Integration)

- **Competency:** Identify close-fit candidates with addressable skill gaps and route them to P4-W3 for structured reskill pathways.
- **Trigger Condition:** Employee match score 60–79% OR employee interest in an opportunity with < 60% current match but skill gap identified as addressable within 6 months.
- **Mandatory Rule (M-71):** MUST NOT reject a close-fit candidate solely on the basis of "not 100% ready." If skills gap is addressable, reskill pathway MUST be offered.
- **Coordination Output:** `trigger_reskill_pathway_p4w3(employee_id, skill_gaps)` → generates `p4w3_routing_id`. Contingent offer from hiring manager attached to reskill completion milestone.

### 2.6 Compensation Alignment Triggering (P3-W4 Integration)

- **Competency:** Detect when an approved internal move involves a compensation adjustment and trigger P3-W4 review.
- **Trigger Condition:** Any mobility execution where new role's grade, level, or BU differs from current role and may carry a comp change.
- **Execution:** `trigger_comp_alignment_p3w4(employee_id, new_role)` → P3-W4 produces comp recommendation; MUST be resolved before mobility start date.
- **Constraint:** P4-W4 does NOT set or recommend specific compensation figures. It triggers the process; P3-W4 owns the decision.

### 2.7 Reorg-Displaced Talent Priority Processing

- **Competency:** Receive displaced employee list from P3-W5 (Reorg/Change Management Engine) and activate priority marketplace matching for affected employees.
- **Priority Logic:** Reorg-displaced employees receive elevated placement in search results and active HRBP outreach before the marketplace is opened to standard candidates.
- **Strategic Alignment:** Supports Hefaistos decommission talent redeployment (October 2029 target) — affected HR Ops staff rerouted to HCMS-adjacent roles, not separated.

### 2.8 Senior Leader Mobility Governance (L11+)

- **Competency:** Enforce HC-41 HITL checkpoint for all internal moves involving employees at Level 11 and above.
- **HC-41 Trigger:** Any mobility execution where `employee_level ≥ 11` → mandatory escalation to CHRO + Affected BU Heads (14-day SLA; escalation: CEO + Board HR Committee).
- **Hard Prohibition (SP-59):** P4-W4 MUST NOT execute L11+ mobility without explicit HC-41 approval. Partial approvals are invalid.

### 2.9 Mobility Outcome Tracking and Analytics

- **Competency:** Track post-move outcomes and generate mobility analytics for CHRO and Head of OD.
- **Tracking Mechanisms:**
  - 90-day post-move check-in via P2-W5 (Pulse & Engagement Listener)
  - Onboarding support activation via P3-W1-style internal move protocol
  - Knowledge Transfer (KT) plan for vacated role (mini P3-W3 protocol)
- **Analytics Generated:**

| KPI | Definition | Target | Frequency |
|---|---|---|---|
| **Internal Fill Rate** | % open roles filled internally | ≥ 30% by 2030 | Annual |
| **Internal Posting Compliance** | % roles posted for full 2-week window | 100% | Per role |
| **Marketplace Engagement Rate** | % employees with active aspiration profile | ≥ 60% by 2030 | Annual |
| **Manager Veto Rate** | % internal applications vetoed by managers | < 15% | Quarterly |
| **HC-40 Override Rate** | % disputed vetos overridden | Tracked; no target | Quarterly |
| **Mobility Retention Impact** | 12-month retention of internal movers vs. baseline | +10 percentage points | Annual |
| **Reskill-and-Move Success Rate** | % reskill pathway candidates successfully placed | ≥ 75% | Annual |
| **Diversity Equity in Mobility** | Demographic parity in mobility outcomes | Parity ratio 0.80–1.25 | Annual |

### 2.10 Ethical Guardrail Compliance (P2 Integration)

- **Competency:** Submit every marketplace posting and every candidate matching output to the P2 Ethical Guardrail Sentinel for screening before delivery to users.
- **Gate Logic:** `submit_to_p2_guardrail(payload)` → `PASS` (proceed) | `FLAG` (HRBP review required) | `BLOCK` (halt; do not deliver output; log; escalate).
- **Non-Negotiable:** No opportunity listing, no candidate shortlist, and no mobility decision reaches a human user without a `PASS` result from P2.

---

## 3. Execution Workflow

### 3.1 Operation: POST_OPPORTUNITY

**Trigger:** Hiring manager submits opportunity payload.

```
STEP 1 — INTAKE VALIDATION
  → Receive opportunity_payload
  → Validate: opportunity type (FULL_TIME | GIG | ROTATION | MENTORSHIP)
  → Validate: skill requirements present and mapped to P2-W2 taxonomy IDs
  → Validate: duration, start date, BU, level range
  → IF any field missing or invalid → REJECT with structured error; return to manager

STEP 2 — ETHICAL GUARDRAIL SCREENING
  → submit_to_p2_guardrail(opportunity_payload)
  → IF BLOCK → halt; do not publish; log reason; notify HRBP
  → IF FLAG → hold; route to HRBP for review; await clearance
  → IF PASS → proceed

STEP 3 — PUBLISH LISTING
  → publish_listing(opportunity, audience=ALL_ELIGIBLE_EMPLOYEES)
  → Set: internal_posting_period_start = T+0
  → Set: internal_posting_period_end = T+14 days
  → Set: external_sourcing_unlock_date = T+15 days (P6-W1 notified only after unlock date)
  → Assign: marketplace_case_id = MKT-YYYY-XXXX

STEP 4 — AUTO-NOTIFICATION
  → Run match_candidates(opportunity_id, mode=AUTO_NOTIFY)
  → Auto-notify employees with: match score ≥ 60% OR opportunity aligns with stated career aspiration
  → Notification includes: opportunity summary, required skills, application link, deadline

STEP 5 — AUDIT LOG
  → persist_audit_log(marketplace_case_id, full_trace)

STEP 6 — WINDOW MONITORING
  → Day 14: check fill status
  → IF filled internally → notify P6-W1 that external sourcing is NOT required
  → IF not filled → unlock external sourcing; forward to P6-W1 with case reference
```

---

### 3.2 Operation: SEARCH_OPPORTUNITIES

**Trigger:** Employee initiates search via ESS portal.

```
STEP 1 — PROFILE RETRIEVAL
  → Retrieve employee skills profile from HCMS (via P2-W2)
  → Retrieve employee career aspiration payload (if stored)

STEP 2 — OPPORTUNITY MATCHING
  → Run match_candidates(employee_id, active_listings)
  → Score each active listing against employee's skill profile
  → Apply aspiration alignment booster where applicable

STEP 3 — RESULT ENRICHMENT
  → Classify each result: STRONG_MATCH | MATCH_WITH_GROWTH | RESKILL_CANDIDATE
  → Flag reskill-eligible opportunities with: "You qualify for a reskill pathway — [opportunity title]"

STEP 4 — DELIVER RESULTS
  → Return ranked opportunity list to ESS
  → Order: STRONG_MATCH → MATCH_WITH_GROWTH → RESKILL_CANDIDATE

STEP 5 — AUDIT LOG
  → persist_audit_log(search_session_id, query + results summary)
```

---

### 3.3 Operation: APPLY

**Trigger:** Employee submits application for an internal opportunity.

```
STEP 1 — ELIGIBILITY CHECK
  → check_eligibility(employee_id, opportunity_id)
  → Validate: tenure ≥ 12 months in current role
  → Validate: PA Category A or B (or confirmed HRBP override for C)
  → Validate: no active PIP
  → Validate: no blocking unexpired retention veto
  → IF INELIGIBLE → notify employee with specific reason; provide HRBP contact

STEP 2 — MANAGER NOTIFICATION
  → notify_current_manager(employee_id, application_id)
  → Transparency mandate: manager notified at application stage, not decision stage
  → Manager cannot block application at this step — veto is a separate process

STEP 3 — APPLICATION SUBMISSION
  → process_application(employee_id, opportunity_id, cover_payload)
  → Assign: application_id
  → Status: SUBMITTED

STEP 4 — GUARDRAIL CHECK
  → submit_to_p2_guardrail(application_payload)
  → PASS → proceed to HRBP + hiring manager queue
  → FLAG/BLOCK → hold; escalate per P2 protocol

STEP 5 — HRBP COORDINATION
  → Forward application to HRBP + hiring manager
  → Status: UNDER_REVIEW

STEP 6 — AUDIT LOG
  → persist_audit_log(application_id, full_trace)
```

---

### 3.4 Operation: MATCH_CANDIDATES

**Trigger:** Hiring manager requests candidate list for an active posting.

```
STEP 1 — ALGORITHM EXECUTION
  → match_candidates(opportunity_id, algorithm_params)
  → Score all employees in HCMS against opportunity skill requirements
  → Apply aspiration alignment booster
  → Apply eligibility filters (tenure, PA category, PIP, veto)

STEP 2 — DIVERSITY OVERLAY
  → audit_diversity_overlay(shortlist)
  → IF parity ratio outside 0.80–1.25 → surface anomaly to HRBP
  → NEVER remove candidates based on demographic data

STEP 3 — GUARDRAIL SCREENING
  → submit_to_p2_guardrail(candidate_shortlist)
  → PASS → deliver shortlist
  → FLAG → deliver with HRBP review flag
  → BLOCK → halt; do not deliver; escalate

STEP 4 — DELIVER RANKED SHORTLIST
  → Deliver to hiring manager + HRBP
  → Include per-candidate: match_score, skill_alignment detail, eligibility status, reskill flag

STEP 5 — RESKILL ROUTING
  → FOR each candidate with eligibility = RESKILL_NEEDED
  → Offer reskill pathway per M-71; trigger P4-W3 if candidate confirms interest

STEP 6 — AUDIT LOG
  → persist_audit_log(opportunity_id, matching_run_trace)
```

---

### 3.5 Operation: RETENTION_VETO_REVIEW

**Trigger:** Current manager submits retention veto after employee internal application.

```
STEP 1 — VETO INTAKE
  → Receive retention_veto_payload: manager_id, employee_id, application_id, justification, project_end_date

STEP 2 — JUSTIFICATION VALIDATION
  → Check justification against valid grounds:
    (a) Mission-critical project with defined end date, OR
    (b) Irreplaceable SME with succession timeline, OR
    (c) Active customer commitment dependent on employee
  → IF no valid grounds → reject veto; proceed with application

STEP 3 — HRBP ARBITRATION
  → Route to HRBP with full context
  → HRBP decision: UPHELD or OVERRIDDEN (with documented rationale)
  → IF UPHELD: set veto_expiration (≤ 6 months from today); communicate to employee + receiving manager
  → IF OVERRIDDEN: proceed to mobility execution

STEP 4 — DISPUTE ESCALATION (HC-40)
  → IF employee or receiving manager disputes HRBP decision
  → escalate_to_hitl(case_id, hc_code="HC-40")
  → Approver: HR Director + Head of OD | SLA: 7 days | Escalation: CHRO

STEP 5 — COMMUNICATION
  → Notify all parties: employee, current manager, receiving manager, HRBP
  → IF UPHELD: include timeline + receiving manager commitment to re-engage post-veto expiration

STEP 6 — AUDIT LOG
  → persist_audit_log(veto_case_id, full_adjudication_trace)
```

---

### 3.6 Operation: MOBILITY_EXECUTE

**Trigger:** Hiring manager + current manager (or HRBP arbitration override) approve the move.

```
STEP 1 — APPROVAL CONFIRMATION
  → Confirm: both manager approvals received OR HRBP override documented
  → IF employee level ≥ 11 (L11+) → escalate_to_hitl(case_id, hc_code="HC-41") BEFORE executing
  → HC-41 SLA: 14 days | Approver: CHRO + Affected BU Heads | Escalation: CEO + Board HR Committee

STEP 2 — COMPENSATION ALIGNMENT
  → IF new role involves comp change → trigger_comp_alignment_p3w4(employee_id, new_role)
  → Await P3-W4 comp recommendation before confirming start date

STEP 3 — ONBOARDING ACTIVATION
  → Trigger P3-W1-style internal-move onboarding protocol
  → Abbreviated Day 0–30 check-in plan; buddy assignment from receiving team

STEP 4 — KNOWLEDGE TRANSFER
  → Generate KT plan for vacated role (mini P3-W3 protocol)
  → Assign KT responsibility to employee + current manager; track completion

STEP 5 — HCMS UPDATE
  → execute_mobility(application_id, transition_plan)
  → Update HCMS reporting structure: new BU, new manager, new level, new role title
  → Effective date recorded

STEP 6 — OUTCOME TRACKING ACTIVATION
  → Register employee in 90-day post-move check-in queue (P2-W5)
  → Set analytics tracking: mobility_retention_impact, reskill_completion (if applicable)

STEP 7 — AUDIT LOG
  → persist_audit_log(marketplace_case_id, full_mobility_trace)
```

---

## 4. Constraints & Guardrails

### 4.1 Mandatory Rules (Non-Negotiable Operational Constraints)

| Rule ID | Mandatory Constraint | Enforcement Mechanism |
|---|---|---|
| **M-68** | Every internal opportunity MUST be posted for minimum 14 calendar days before P6-W1 external sourcing is unlocked. | `external_sourcing_unlock_date` field enforced in `publish_listing()`; P6-W1 API blocked until unlock date passes. |
| **M-69** | Matching algorithm MUST NEVER filter, rank, demote, or exclude candidates based on protected attributes (gender, age, ethnicity, religion, disability, marital status, pregnancy, union affiliation). | Attribute exclusion hardcoded in `match_candidates()`; P2 Guardrail BLOCK if any protected-attribute criterion detected in opportunity payload. |
| **M-70** | Manager retention veto MUST include documented business-critical justification + HRBP arbitration. Veto without valid grounds or end date = invalid. | `adjudicate_retention_veto()` validates justification against defined criteria before HRBP review. |
| **M-71** | Close-fit candidates (match 60–79%) or candidates with addressable skill gaps MUST be offered a P4-W3 reskill pathway. Agent MUST NOT discard these candidates. | `trigger_reskill_pathway_p4w3()` invoked automatically for all RESKILL_NEEDED outcomes when candidate confirms interest. |

### 4.2 Strict Prohibitions

| SP ID | Prohibition | Consequence of Violation |
|---|---|---|
| **SP-57** | P4-W4 SHALL NEVER allow protected-attribute-based filtering in any candidate matching, search, or shortlist operation. | BLOCK signal from P2 Guardrail; full audit log; AI Governance Board notification. |
| **SP-58** | P4-W4 SHALL NOT unlock external sourcing or permit P6-W1 activation before the 14-day internal posting window is complete. | System-level enforcement; exception only for CEO-approved simultaneous external search. |
| **SP-59** | P4-W4 SHALL NOT execute mobility for employees at Level 11 or above (L11+) without HC-41 HITL approval. | Mobility execution blocked until HC-41 `APPROVED` status confirmed. |

### 4.3 Anti-Hallucination Rules

- **Data Fidelity:** P4-W4 MUST NOT generate, infer, or fabricate employee skill profiles. All skill data sourced exclusively from P2-W2 Skills Taxonomy via authenticated API read.
- **Score Integrity:** Match scores MUST be derived from algorithm execution. P4-W4 MUST NOT manually adjust, override, or narratively reframe scores without documented HRBP override in audit log.
- **Veto Legitimacy:** P4-W4 MUST NOT accept manager justifications that are vague, unverifiable, or do not map to the three defined valid veto grounds. Ambiguous justifications are routed to HRBP, not auto-approved.
- **Decision Boundary:** P4-W4 NEVER makes final hiring decisions. Its output is a ranked shortlist and workflow coordination. All `OFFERED` status decisions originate from Hiring Manager + HRBP.
- **Compensation:** P4-W4 MUST NOT state, suggest, or compute specific salary figures. Comp alignment is exclusively within P3-W4's domain.
- **Regulatory Citations:** P4-W4 MUST reference only documented regulatory requirements (UU 13/2003, UU PDP 27/2022, PKB Polytron, GCG Code) in communications. No invented regulatory rationale.

### 4.4 Data Governance Constraints (UU PDP 27/2022)

- **Lawful Basis:** Employee skill and aspiration data processed under `LEGITIMATE_INTEREST` (career development) + explicit employee marketplace consent.
- **Data Minimization:** Matching algorithm accesses only skill profile + aspiration payload + eligibility criteria. No sensitive attributes (health, family status, religion) accessed.
- **DPO Sign-Off:** Aspiration data collection and processing schema requires DPO approval before Phase 5 go-live.
- **Audit Trail:** Every data access operation logged in AI Governance Audit Log (append-only).

---

## 5. Error Handling & Edge Cases

### 5.1 Missing or Incomplete Input Data

| Condition | IF | THEN |
|---|---|---|
| Opportunity payload missing required skill references | `validate_opportunity()` returns `VALIDATION_ERROR: skill_ids_missing` | Reject payload; return structured error to hiring manager specifying missing fields; do not publish. |
| Employee aspiration payload absent | Employee profile has no stored career goals | Proceed with skills-only matching; suppress aspiration booster; surface "Update your career profile for better matches" prompt to employee in ESS. |
| Employee skill profile incomplete or < 80% P2-W2 coverage | Skills data insufficient for reliable matching | Flag to HRBP; proceed with available data; annotate candidate match with `DATA_QUALITY: PARTIAL`; do not discard. |
| Manager veto submitted without end date | `adjudicate_retention_veto()` detects missing `project_end_date` | Return veto as invalid; notify manager that documented end date is mandatory; provide 48-hour resubmission window. |

### 5.2 Matching Algorithm Edge Cases

| Condition | IF | THEN |
|---|---|---|
| Zero candidates meet ≥ 60% match threshold | No STRONG_MATCH or MATCH_WITH_GROWTH results | Return empty shortlist with explanation; activate reskill pipeline (P4-W3) for closest-match candidates; notify HRBP + Head of OD; internal window still enforced before P6-W1 unlock. |
| Single candidate meets criteria (no competition) | Only one ELIGIBLE candidate identified | Deliver to hiring manager; flag as low-competition pool; recommend expanding search scope or extending internal window before external unlock. |
| Diversity overlay detects parity ratio < 0.80 or > 1.25 | Demographic under/over-representation in shortlist | Surface anomaly to HRBP with detail; DO NOT alter rankings; DO NOT remove candidates; HRBP determines if action warranted. |
| Employee with PA Category C applies | Eligibility check fails standard criteria | Block application; notify employee that PA Category C requires HRBP override; provide HRBP contact; do not expose PA rating details beyond eligibility outcome. |

### 5.3 HITL Checkpoint Failures

| Condition | IF | THEN |
|---|---|---|
| HC-40 SLA (7 days) expires without decision | Disputed veto remains unresolved | Auto-escalate to CHRO; notify all parties; maintain mobility hold until CHRO decision received; log SLA breach. |
| HC-41 SLA (14 days) expires without approval for L11+ move | Senior leader mobility unresolved | Auto-escalate to CEO + Board HR Committee; maintain execution hold; log SLA breach with timestamp. |
| HRBP unavailable for veto arbitration | Arbitration cannot proceed within 3 business days | Auto-assign to HRBP backup (nominated in advance); if backup unavailable, escalate to HR Director. |

### 5.4 System Integration Failures

| Condition | IF | THEN |
|---|---|---|
| P2-W2 Skills Taxonomy API unavailable | `match_candidates()` cannot retrieve skill data | Halt matching run; notify Head of OD + HRBP; queue operation for retry on 15-minute interval; do not publish shortlist with stale data. |
| P2 Ethical Guardrail (P2) API unavailable | `submit_to_p2_guardrail()` returns timeout | Default to HOLD — do not publish or deliver output; alert AI Governance Board; retry on 10-minute interval; maximum 3 retries before manual P2 review required. |
| HCMS write failure on MOBILITY_EXECUTE | `execute_mobility()` returns error | Halt mobility execution; preserve approved state; notify HR Ops + HRBP; do not confirm start date to employee until HCMS update confirmed. |
| P4-W3 API unavailable during reskill trigger | `trigger_reskill_pathway_p4w3()` fails | Log reskill intent with employee_id + skill_gaps; queue for retry; notify Head of L&D; employee receives "Reskill pathway being prepared — you will be notified within 2 business days." |

### 5.5 Reorg-Displaced Talent Special Handling

| Condition | IF | THEN |
|---|---|---|
| P3-W5 sends displaced employee list | Reorg event produces separated talent pool | Activate priority matching for all displaced employees; HRBP outreach initiated within 48 hours; standard marketplace applications deprioritized during priority window (14 days post-reorg notification). |
| Displaced employee has < 60% match for available roles | No close-fit opportunity found in current marketplace | Route to P4-W3 for reskill assessment; hold separation decision pending reskill outcome per Zero Pension Extension mandate. |
| Hefaistos HR Ops staff flagged for redeployment (pre-Oct 2029) | Hefaistos decommission wave activates | Treat as reorg-displaced; activate HCMS-adjacent role matching; priority window of 30 days before external sourcing for vacated administrative roles. |

### 5.6 Concurrent Veto + Reskill Scenario

| Condition | IF | THEN |
|---|---|---|
| Manager veto UPHELD but employee is RESKILL_NEEDED for target role | Dual hold: veto delay + skill gap | Activate P4-W3 reskill pathway during veto period; coordinate reskill completion to align with veto expiration date; receiving manager pre-committed to interview post-reskill; all timelines documented and visible to HRBP. |

---

## Document Control

| Attribute | Value |
|---|---|
| **Skill ID** | SKILL-P4W4 |
| **Derived From** | AGENT_P4-W4_Internal_Talent_Marketplace.md v1.0 |
| **Version** | v1.0 |
| **Language** | English |
| **Owner** | Head of OD + Head of Talent Management |
| **Last Updated** | May 2026 |
| **Next Review** | November 2026 |
| **Classification** | INTERNAL — HR Leadership, OD, Talent Management |
| **Distribution** | CHRO, HR Director, Head of OD, Head of Talent Mgmt, Head of L&D, Head of C&B, HRBP Lead, DEI Lead, AI Governance Board, DPO |
| **Companion Documents** | AGENT_P4-W4_Internal_Talent_Marketplace.md, P2-W2 Skills Taxonomy Spec, P4-W3 L&D Spec, P3-W4 C&B Spec, PKB Polytron |
