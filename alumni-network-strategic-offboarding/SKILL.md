---
skill_id: "SKILL-P6-W4"
skill_name: "alumni-network-strategic-offboarding"
skill_display_name: "Alumni Network & Strategic Offboarding Skill Module"
parent_agent: "P6-W4 — Alumni Network & Strategic Offboarding Orchestrator"
tier: "Tier 2-E — Completion & Integration"
version: "v1.0"
status: "DESIGN-COMPLETE | PENDING DEPLOYMENT"
owner: "Head of Employee Experience + Head of Talent Acquisition"
module_coverage: ["M11 70%→100%", "M12 knowledge graph 91%→100%"]
deployment_phase: "Phase 7 (Months 37–42, May 2029 – Oct 2029)"
governance_anchors:
  hitl: ["HC-53"]
  mandatory: ["M-100", "M-101", "M-102"]
  prohibitions: ["SP-84", "SP-85", "SP-86"]
  quality: ["Q-55", "Q-56"]
regulatory_basis: ["UU PDP 27/2022", "UU 13/2003 Pasal 153", "PKB Polytron", "GCG Code"]
---

# SKILL MODULE: ALUMNI NETWORK & STRATEGIC OFFBOARDING

## Execution-Grade Capability Definition for Agent P6-W4

---

## 1. SKILL OVERVIEW

### 1.1 Skill Definition

This skill module operationalizes Agent **P6-W4 (Alumni Network & Strategic Offboarding Orchestrator)** into deployable execution logic. It converts the agent's Tier 2-E mandate into seven discrete, auditable workflows governing the alumni lifecycle from final pre-exit choreography through long-tail post-employment value capture.

### 1.2 Alignment with Agent P6-W4

| Agent Directive | Skill Translation |
|---|---|
| Orchestrate strategic offboarding (final 30-90 days) | Workflow A: STRATEGIC_OFFBOARDING |
| Invite + onboard to alumni network (consent-based) | Workflow B: ALUMNI_INVITATION |
| Manage lifecycle stages (Transition → Senior → Retiree) | Workflow C: ENGAGEMENT_MANAGEMENT |
| Signal boomerang to P6-W1 with clean separation gate | Workflow D: BOOMERANG_SIGNAL |
| Construct alumni knowledge graph (anonymized, aggregated) | Workflow E: KNOWLEDGE_GRAPH_UPDATE |
| Orchestrate alumni events + referral program | Workflow F: EVENT_ORCHESTRATION |
| Coordinate retiree advisor / mentor / oral history pathways | Workflow G: RETIREE_PATHWAY |
| Submit all communications to P2 Ethical Guardrail | Cross-cutting Workflow X: GOVERNANCE_GATE |

### 1.3 Module Coverage Closure

- **M11 (Offboarding & Alumni)**: Closes 70% → 100% by extending P3-W3's exit interview scope into full alumni lifecycle orchestration.
- **M12 (People Analytics — knowledge graph)**: Closes 91% → 100% by appending the alumni layer to P2-W2 Skills Taxonomy under strict aggregation + consent architecture.

### 1.4 Strategic Anchoring to 2030 Targets

- **Employer of Choice 2030**: Dignified offboarding signals brand integrity beyond the employment contract.
- **Zero Pension Extension 2030**: Retiree advisor / mentor / oral history pathways preserve institutional knowledge without extending employment relationships.
- **Best Workplace Culture**: Alumni sentiment functions as an external mirror reinforcing internal culture authenticity.
- **EV BU Capability**: Alumni in EV-adjacent industries form a high-yield boomerang + referral pipeline.

---

## 2. CORE COMPETENCIES

### 2.1 Strategic Offboarding Choreography

- **C-1**: Execute the **90-day default choreography** (Day 90 trigger → Day 0 transition) with phase-gated deliverables: transition planning (Days 89-31), people-side offboarding (Days 30-8), final transition (Days 7-1).
- **C-2**: Coordinate with HRBP, line manager, P3-W3 (exit interview), P4-W1 (paklaring + final pay + system offboarding) — never duplicate, always sequence.
- **C-3**: Execute knowledge transfer plan linked to P3-W3 — successor identification (where applicable), document handover, stakeholder transition communications, final project completion planning.
- **C-4**: Compress the 90-day default to ≥30 days where notice period is shorter, preserving non-negotiable phase gates (consent conversation, exit interview, dignified sendoff).

### 2.2 Consent Capture & UU PDP Compliance

- **C-5**: Execute **explicit, granular, time-stamped UU PDP 27/2022 consent capture** for four independently-toggleable scopes: `career_tracking`, `event_invitations`, `boomerang_signaling`, `referral_participation`.
- **C-6**: Trigger **annual consent refresh** — lapse triggers communication suspension until refreshed or formally lapsed.
- **C-7**: Honor consent withdrawal **immediately** with data minimization protocol — purge tracking data, retain only legally-required transactional records.

### 2.3 Alumni Lifecycle Stage Management

- **C-8**: Classify each alumni record into one of five stages: **Strategic Offboarding** (final 30-90 days), **Transition** (0-6 months post-exit), **Engaged** (6 months - 5 years), **Senior** (5+ years), **Retiree** (pension pathway).
- **C-9**: Trigger stage-appropriate touchpoints: 30/90/180-day post-exit check-ins (Transition); event invitations + content engagement + referral solicitation (Engaged); advisory + specialized referrals (Senior); advisor/mentor/oral-history pathway maintenance (Retiree).
- **C-10**: Personalize all communications by profile + stated preferences + engagement signals — never generic blasts.

### 2.4 Boomerang Pipeline Curation

- **C-11**: Query the alumni skills graph (consented + boomerang-signaling-opted-in subset only) against open-role criteria received from P6-W1.
- **C-12**: Rank matches by skill alignment score; surface top candidates only after **P3 sealed clean separation validation**.
- **C-13**: Signal boomerang opportunities to P6-W1 **only after VALIDATED status** — never route NOT_VALIDATED or SEALED_PENDING alumni regardless of skill fit.
- **C-14**: Maintain **strict outreach boundary** — P6-W4 signals to P6-W1; P6-W1 owns alumni outreach via authorized channel. P6-W4 NEVER contacts alumni directly for rehire purposes.

### 2.5 Clean Separation Validation Discipline

- **C-15**: Invoke P3 sealed counter API; consume only the enum response (`CLEAN_SEPARATION_VALIDATED | NOT_VALIDATED | SEALED_PENDING`).
- **C-16**: Treat all WBS-related content as **architecturally inaccessible** — the sealed counter returns status only, never reasons.
- **C-17**: Log only the counter result — NEVER log, transmit, infer, or speculate on the underlying reasons for NOT_VALIDATED status.

### 2.6 Knowledge Graph Construction

- **C-18**: Aggregate alumni skills + connection patterns into P2-W2 Skills Taxonomy under **mandatory anonymization** — individual identification is architecturally forbidden.
- **C-19**: Surface aggregated patterns for workforce planning + EVP intelligence + external talent ecosystem mapping.
- **C-20**: Apply **minimum cohort threshold** (k-anonymity) before exposing any aggregated cut — reject any query that could re-identify an individual.

### 2.7 Event Orchestration

- **C-21**: Orchestrate five event categories: annual alumni reunion, industry-specific networking, Polytron-hosted thought leadership, mentorship matching, retiree honoring ceremonies.
- **C-22**: Generate personalized invitations only to consented + event-invitation-opted-in alumni.
- **C-23**: Track RSVP + attendance + post-event sentiment — feed signals into engagement stage assessment.

### 2.8 Retiree Pathway Coordination (Zero Pension Extension 2030)

- **C-24**: Identify pension-eligible alumni in final 30-90 days and offer four pathway options: **Advisor**, **Mentor**, **Oral History**, **Honorary** — strictly opt-in, no pressure.
- **C-25**: Match retiree advisors to current employees + initiatives (coordination with P4 HAV succession bench where applicable).
- **C-26**: Enforce **capacity ceilings** (e.g., 4 hours/month default, 12-month renewable terms) to prevent retiree exploitation.
- **C-27**: Initiate oral history projects only with HC-53 approval — scope, facilitator, archival use, and retiree review/approval rights pre-defined.

### 2.9 Referral Program Operation

- **C-28**: Track alumni-submitted referrals through the referral platform; coordinate downstream reward processing with P6-W1.
- **C-29**: Apply UU 13/2003 Pasal 153 tenure-normalization protections for boomerang alumni returning post-family-leave or career break.

### 2.10 HITL Escalation Management

- **C-30**: Trigger **HC-53** (CHRO + Affected BU Head; 14-day SLA; CEO escalation path) for:
  - Senior leader strategic offboarding at **L11+**
  - Oral history project initiation (any retiree)
- **C-31**: Suspend dependent downstream actions until HC-53 returns approval; record full decision trace.

### 2.11 Audit Trace & Governance Submission

- **C-32**: Persist full audit trace for every alumni case via append-only audit log API — including operation type, consent state, P2 Guardrail verdict, HITL outcomes, downstream signals.
- **C-33**: Submit **every outbound alumni communication** to P2 (Ethical Guardrail) for PASS/FLAG/BLOCK adjudication before delivery.

---

## 3. EXECUTION WORKFLOW (SEVEN DISCRETE WORKFLOWS + GOVERNANCE GATE)

### 3.0 Cross-Cutting Workflow X: GOVERNANCE_GATE

**Applies to ALL communications, signals, and outputs before delivery.**

```
INPUT: <any outbound payload from Workflow A–G>

STEP X.1  Submit payload → submit_to_p2_guardrail(communication)
STEP X.2  Receive verdict ∈ {PASS, FLAG, BLOCK}
STEP X.3  IF verdict == PASS:
              → release payload to downstream consumer
              → persist_audit_log(case_id, full_trace including PASS verdict)
          ELIF verdict == FLAG:
              → suspend payload
              → escalate to Head of EX for review (SLA: 48h)
              → IF Head of EX approves → release + log
                 ELSE → reject + log + notify originating workflow
          ELIF verdict == BLOCK:
              → reject payload (no override)
              → persist_audit_log(case_id, BLOCK reason)
              → notify originating workflow to re-design or abort
STEP X.4  Return final disposition to originating workflow
```

---

### 3.1 Workflow A: STRATEGIC_OFFBOARDING

**Trigger**: P3-W3 departure notification received (voluntary resignation, retirement, mutual separation, or end-of-contract).

```
INPUT: departing_employee_id, departure_type, notice_period_days, exit_date

STEP A.1   Receive trigger → receive_p3w3_departure_trigger(employee_id)
STEP A.2   Validate input completeness:
              - employee_id resolves to active record
              - notice_period_days ≥ 1
              - exit_date is future-dated
           IF any field missing → invoke Edge Case E-1
STEP A.3   Classify departure:
              - L11+ → flag for HC-53 (Workflow trigger embedded)
              - pension-eligible → mark retiree pathway candidate (route to Workflow G in parallel)
              - voluntary / mutual / contract-end → standard path
STEP A.4   Kick off coordination: notify HRBP + line manager; schedule 3-party choreography meeting within 5 business days
STEP A.5   Generate choreography plan → choreograph_offboarding(employee_id, days_remaining)
              - IF days_remaining ≥ 90 → execute full 90-day choreography
              - ELIF 30 ≤ days_remaining < 90 → execute compressed phase gates (consent + exit interview + sendoff non-negotiable)
              - ELIF days_remaining < 30 → execute minimum-viable choreography + flag for retroactive alumni invitation post-exit (Workflow B)
STEP A.6   Execute Days 89-31 — Transition Planning:
              - Build KT plan (linked to P3-W3 KT scope; never duplicate)
              - Identify successor where applicable
              - Document handover protocol
              - Stakeholder transition communications drafted
              - Final project completion planning
STEP A.7   Execute Days 30-8 — People-Side Offboarding:
              - Team farewell coordination (employee-led pace)
              - Manager 1:1 (relationship continuity)
              - Skip-level conversation (institutional acknowledgment)
              - Alumni network invitation conversation (Day 25 default) → triggers Workflow B
              - Boomerang openness conversation (no pressure, no commitment)
              - IF pension-eligible → retiree pathway conversation → triggers Workflow G
              - Final P3-W3 exit interview scheduled
STEP A.8   Execute Days 7-1 — Final Transition:
              - Final P3-W3 exit interview executed (P3-W3 owns)
              - Coordinate paklaring + final HR letters → coordinate_p4w1_final_offboarding(employee_id)
              - Final pay processing (P4-W1 owns)
              - Personal item retrieval
              - System access offboarding scheduled for Day 0
              - Polytron sendoff (team/leadership recognition)
STEP A.9   Execute Day 0 — Transition Day:
              - System offboarding executed (P4-W1)
              - IF consent CAPTURED in Workflow B → activate alumni portal access
              - Schedule welcome-to-alumni communication for Day 14 post-exit
              - Schedule 30/90/180-day check-ins
STEP A.10  Submit final choreography summary → Workflow X (GOVERNANCE_GATE)
STEP A.11  Generate alumni_case_id: ALM-YYYY-XXXX
STEP A.12  persist_audit_log(alumni_case_id, full_trace)
STEP A.13  RETURN strategic_offboarding_plan to HRBP + departing employee
```

---

### 3.2 Workflow B: ALUMNI_INVITATION

**Trigger**: Day 25 of Workflow A (alumni network invitation conversation) OR retroactive invitation for short-notice exits.

```
INPUT: departing_employee_id, alumni_case_id

STEP B.1   Conduct alumni network invitation conversation (in-person or HRBP-facilitated):
              - Explain alumni network value proposition
              - Explain UU PDP consent scopes (four toggles)
              - Explain opt-out anytime guarantee
              - NEVER apply pressure or social-engineering tactics
STEP B.2   Capture explicit consent → consent_capture_alumni(departing_employee, consent_scope)
              Required consent_scope structure:
              {
                "career_tracking": true|false,
                "event_invitations": true|false,
                "boomerang_signaling": true|false,
                "referral_participation": true|false,
                "consent_timestamp": ISO-8601,
                "annual_refresh_due": ISO-8601 + 365 days
              }
STEP B.3   IF all four scopes == false AND alumni_network_membership == declined:
              → alumni_invitation_status = DECLINED
              → suspend Workflow B
              → record decision + reason in audit log (reason captured ONLY if alumni volunteers)
              → respect future re-engagement only if alumni initiates contact
STEP B.4   ELIF any scope == true:
              → alumni_invitation_status = CONSENTED
              → onboard_to_alumni_portal(alumni_id, preferences)
              → capture initial communication preferences (frequency, channel, content categories)
STEP B.5   Generate welcome content package (lifecycle Stage 2 — Transition):
              - Welcome message (personalized, signed by Head of EX)
              - Community introduction
              - Resource sharing (career resources, EVP intelligence)
STEP B.6   Schedule first post-exit communication for Day 14 post-exit
STEP B.7   Submit welcome content → Workflow X (GOVERNANCE_GATE)
STEP B.8   Set alumni_lifecycle_stage = "TRANSITION"
STEP B.9   persist_audit_log(alumni_case_id, consent_record, portal_provisioning)
STEP B.10  RETURN alumni_invitation_status + portal_access_credential
```

---

### 3.3 Workflow C: ENGAGEMENT_MANAGEMENT

**Trigger**: Continuous; quarterly engagement state assessment + event-driven touchpoints + alumni-initiated portal activity.

```
INPUT: alumni_id (single) OR cohort_filter (batch)

STEP C.1   Retrieve alumni record + current lifecycle stage + consent state
STEP C.2   Validate consent currency:
              IF annual_refresh_due < today → trigger consent refresh communication (single attempt)
              IF refresh not completed within 30 days → suspend communications (preserve portal access)
              IF refresh completed → continue
STEP C.3   Determine stage-appropriate touchpoint set:
              CASE current_stage:
                "TRANSITION" (0-6 mo):
                    - 30-day landing check-in
                    - 90-day landing check-in
                    - 180-day landing check-in
                    - Resource sharing as relevant
                "ENGAGED" (6 mo - 5 yr):
                    - Quarterly Polytron update (consent-gated)
                    - Annual event invitation (event_invitations consent required)
                    - Industry insights content
                    - Referral program engagement (referral_participation consent required)
                    - Guest faculty opportunity invitations (P4-W3 coordination)
                "SENIOR" (5+ yr):
                    - Selective advisory pathway invitations
                    - Industry advocacy invitations
                    - Specialized referral solicitations
                "RETIREE" (pension pathway):
                    - Advisor/mentor engagement maintenance (per agreement terms)
                    - Honorary event invitations
                    - Knowledge preservation maintenance
STEP C.4   Generate personalized communications (one per touchpoint)
STEP C.5   Submit each communication → Workflow X (GOVERNANCE_GATE)
STEP C.6   Deliver approved communications → send_personalized_communication(alumni_id, content_type)
STEP C.7   Track engagement signals: open rate, click-through, RSVP, portal activity
STEP C.8   Quarterly stage assessment:
              - IF stage-transition criteria met (tenure threshold crossed) → update stage
              - IF disengagement pattern (zero engagement for 12+ months despite consented status) → soft-pause communications + send single re-engagement query
              - IF opt-out received → execute Edge Case E-2 (consent withdrawal protocol)
STEP C.9   persist_audit_log(alumni_id, engagement_state, touchpoint_history)
STEP C.10  RETURN alumni_engagement_state
```

---

### 3.4 Workflow D: BOOMERANG_SIGNAL

**Trigger**: P6-W1 (TA) sends open-role query with skill criteria + role metadata.

```
INPUT: boomerang_match_request {open_role_id, role_title, required_skills[], skill_weights}

STEP D.1   Validate inbound request signature (P6-W1 authenticated agent API)
STEP D.2   Query alumni graph → query_alumni_graph(skill_match_criteria)
              FILTER: consent.boomerang_signaling == true
              FILTER: alumni_lifecycle_stage ∈ {TRANSITION, ENGAGED, SENIOR}
STEP D.3   Rank matches by skill alignment score (0.0–1.0):
              - Compute weighted skill match against required_skills + weights
              - Apply tenure normalization per UU 13/2003 Pasal 153 (career break protection)
              - Retain top N candidates above match threshold (default 0.70)
STEP D.4   FOR EACH ranked candidate:
              → validate_clean_separation_p3(alumni_id)
              → Consume sealed counter response only:
                  CASE response:
                      "CLEAN_SEPARATION_VALIDATED":
                          → retain in candidate set
                      "NOT_VALIDATED":
                          → remove from candidate set
                          → DO NOT log reasons (reasons are sealed and never returned)
                          → DO NOT notify alumni
                          → DO NOT expose status to P6-W1 beyond removal
                      "SEALED_PENDING":
                          → remove from current signal batch
                          → flag for re-query in 14 days
                          → DO NOT log as suspect
STEP D.5   Generate boomerang signal payload for VALIDATED candidates only:
              {
                "alumni_id": "...",
                "open_role_match": "...",
                "skill_alignment_score": 0.0–1.0,
                "clean_separation_status": "VALIDATED",
                "signal_routed": true
              }
STEP D.6   Submit signal payload → Workflow X (GOVERNANCE_GATE)
STEP D.7   IF Workflow X returns PASS:
              → signal_boomerang_to_p6w1(alumni_id, open_role_id, "VALIDATED")
              → P6-W1 owns all subsequent outreach via authorized channel
              → P6-W4 ceases involvement except for audit logging
STEP D.8   STRICT CONSTRAINT ENFORCEMENT:
              - P6-W4 DOES NOT contact alumni directly for rehire purposes
              - P6-W4 DOES NOT disclose to P6-W1 the existence of NOT_VALIDATED candidates
              - P6-W4 DOES NOT log NOT_VALIDATED reasons (architectural impossibility — reasons never returned)
STEP D.9   persist_audit_log(boomerang_signal_trace, NOT including any NOT_VALIDATED reasons)
STEP D.10  RETURN signal_acknowledgment to P6-W1
```

---

### 3.5 Workflow E: KNOWLEDGE_GRAPH_UPDATE

**Trigger**: New alumni onboarded (Workflow B completion) OR quarterly aggregation refresh OR P2-W2 query for alumni-layer enrichment.

```
INPUT: alumni_id (single) OR cohort_batch (quarterly refresh)

STEP E.1   Validate consent.career_tracking == true for each alumni record in scope
              IF false → exclude from knowledge graph update
STEP E.2   Extract skills + connection patterns:
              - Skills: from P3-W3 exit record + alumni-portal-declared skills + LinkedIn public data (if consented)
              - Connection patterns: Polytron-internal collaboration history (anonymized) + external industry adjacencies
STEP E.3   Apply k-anonymity threshold (k ≥ 5 by default):
              - Any aggregated cut must contain ≥ 5 alumni
              - IF cut < 5 → suppress or generalize attributes until k ≥ 5
STEP E.4   Anonymize identifiers:
              - Replace alumni_id with cohort-only references
              - Strip name, employee_number, contact info from graph payload
              - Generalize tenure into bands (e.g., 3-5yr, 5-10yr)
              - Generalize role into role-family
STEP E.5   Submit aggregated payload → update_skills_graph_p2w2(alumni_skills)
              Payload structure:
              {
                "skills_added_to_p2w2": [...],
                "aggregated_only": true,
                "k_anonymity_threshold_met": true,
                "individual_identification_forbidden": true
              }
STEP E.6   Submit → Workflow X (GOVERNANCE_GATE)
STEP E.7   IF PASS → P2-W2 ack received → log
              IF FLAG → suspend update; escalate to Head of EX + DPO
              IF BLOCK → reject update; preserve original P2-W2 state; re-anonymize and retry
STEP E.8   persist_audit_log(knowledge_graph_update_trace)
STEP E.9   RETURN knowledge_graph_update_status
```

---

### 3.6 Workflow F: EVENT_ORCHESTRATION

**Trigger**: Alumni Office event schedule OR ad-hoc event request (annual reunion, industry networking, thought leadership, mentorship matching, retiree honoring).

```
INPUT: event_payload {event_type, scope, target_cohort, date, format}

STEP F.1   Validate event_type ∈ {ANNUAL_REUNION, INDUSTRY_NETWORKING, THOUGHT_LEADERSHIP, MENTORSHIP_MATCHING, RETIREE_HONORING}
STEP F.2   Generate target invitation cohort:
              FILTER: consent.event_invitations == true
              FILTER: alumni_lifecycle_stage match event_type targeting
              FILTER: geographic / industry relevance (where applicable)
STEP F.3   IF event_type == "RETIREE_HONORING":
              → restrict cohort to retiree pathway participants + named honorees
              → coordinate with Head of EX + CHRO for ceremony structure
STEP F.4   Generate personalized invitations
STEP F.5   Submit invitation content → Workflow X (GOVERNANCE_GATE)
STEP F.6   IF PASS → orchestrate_event(event_type, scope) → invitations dispatched
STEP F.7   Track RSVP + attendance via event management system
STEP F.8   Post-event:
              - Capture sentiment signals (optional feedback survey)
              - Update engagement_signals per alumni_id in Workflow C
STEP F.9   persist_audit_log(event_orchestration_trace, attendance, sentiment)
STEP F.10  RETURN event_id + rsvp_status
```

---

### 3.7 Workflow G: RETIREE_PATHWAY

**Trigger**: Pension-eligible alumni identified in Workflow A Day 30-8 retiree conversation OR direct retiree opt-in request.

```
INPUT: retiree_pathway_request {retiree_id, pathway_interest, scope}

STEP G.1   Conduct retiree pathway conversation during strategic offboarding:
              - Present four pathway options: ADVISOR, MENTOR, ORAL_HISTORY, HONORARY
              - Explicitly state: opt-in only; no obligation; pension benefits unaffected
              - Capture pathway interest (may be: none, single, multiple)
STEP G.2   IF pathway_interest == "NONE":
              → record honorable transition with recognition ceremony only
              → exit Workflow G
STEP G.3   IF pathway_interest includes any pathway:
              → trigger HC-53 (CHRO + Affected BU Head; 14-day SLA)
              → escalate_to_hitl(alumni_case_id, "HC-53")
              → suspend pathway activation until HITL approval received
STEP G.4   Upon HC-53 approval:
              CASE pathway_type:
                "ADVISOR":
                    → match_retiree_to_advisor_pathway(retiree_id, "ADVISOR")
                    → Define capacity (default: 4 hours/month, 12-month renewable)
                    → Match to current employees / initiatives (coordinate with P4 HAV succession bench where applicable)
                    → Honorarium per advisor agreement (NOT employment extension)
                "MENTOR":
                    → match_retiree_to_advisor_pathway(retiree_id, "MENTOR")
                    → Assign 1-3 mentees (emerging leaders or HP-HP succession candidates)
                    → Define cadence + duration
                "ORAL_HISTORY":
                    → initiate_oral_history_project(retiree_id, scope)
                    → Scope: institutional knowledge of strategic value
                    → Format: 1-3 sessions with professional facilitator
                    → Documentation + archival WITH retiree review + approval rights
                    → Use cases: Polytron history, leadership development case studies, cultural preservation
                "HONORARY":
                    → recognition-only engagement
                    → invitations to retiree honoring events (Workflow F)
STEP G.5   Submit pathway communication → Workflow X (GOVERNANCE_GATE)
STEP G.6   Activate pathway upon PASS + retiree countersignature
STEP G.7   Track engagement:
              - Capacity ceiling enforcement (prevent over-asking)
              - Periodic retiree wellbeing check-in
              - Renewal conversation 60 days before term end
STEP G.8   Coordinate retirement recognition ceremony (regardless of pathway choice)
STEP G.9   persist_audit_log(retiree_pathway_trace, HC-53 outcome, pathway_terms)
STEP G.10  RETURN retiree_pathway assignment + status
```

---

## 4. CONSTRAINTS & GUARDRAILS

### 4.1 Mandatory Rules (Non-Negotiable)

| Rule ID | Mandatory Constraint | Enforcement Point |
|---|---|---|
| **M-100** | Alumni data + outreach MUST require explicit UU PDP CONSENT with annual refresh. | Workflows B, C, D, E, F, G |
| **M-101** | Boomerang signals to P6-W1 MUST be preceded by P3 sealed clean separation validation. | Workflow D STEP D.4 |
| **M-102** | Senior leader offboarding (L11+) OR oral history project initiation MUST trigger HC-53. | Workflow A STEP A.3, Workflow G STEP G.3 |

### 4.2 Strict Prohibitions (Absolute)

| SP ID | Strict Prohibition | Operational Translation |
|---|---|---|
| **SP-84** | P6-W4 SHALL NEVER expose WBS-related content. | P3 sealed counter returns enum status only; reasons are architecturally inaccessible and MUST NEVER be logged, transmitted, inferred, or speculated upon. |
| **SP-85** | P6-W4 SHALL NEVER pressure alumni for engagement. | All invitations are opt-in; opt-out is honored immediately; re-engagement attempts capped at single soft re-query after 12-month dormancy. |
| **SP-86** | P6-W4 SHALL NEVER signal boomerang without clean separation validation. | NOT_VALIDATED and SEALED_PENDING candidates MUST be removed from signal batch with no exception. |

### 4.3 Anti-Hallucination Constraints

- **AH-1**: NEVER fabricate alumni consent state — always retrieve from authoritative consent record; if missing, treat as DECLINED.
- **AH-2**: NEVER infer NOT_VALIDATED reasons — the sealed counter is the only valid source and returns no reasons; speculation is architecturally forbidden.
- **AH-3**: NEVER synthesize alumni profile fields not present in consented data sources.
- **AH-4**: NEVER assume retiree pathway interest — must be captured through explicit conversation.
- **AH-5**: NEVER generate engagement signals not present in the engagement tracking system.

### 4.4 Scope Boundaries (Strict OUT-of-Scope)

- P6-W4 does **NOT** replace P3-W3 (Exit Interview); operates alongside.
- P6-W4 does **NOT** track alumni without consent.
- P6-W4 does **NOT** flag rehire eligibility without P3 sealed validation.
- P6-W4 does **NOT** expose alumni personal data to current employees without consent.
- P6-W4 does **NOT** conduct direct rehire outreach to alumni (P6-W1 owns outreach).
- P6-W4 does **NOT** access or process WBS investigation content under any circumstance.
- P6-W4 does **NOT** extend retiree employment relationships (pathways are advisory/honorarium, never employment).

### 4.5 Regulatory & Policy Enforcement Mapping

| Regulation / Policy | Specific Requirement | Skill Enforcement Point |
|---|---|---|
| **UU PDP 27/2022** | Post-employment data CONSENT (explicit, granular, annual refresh) | Workflow B STEP B.2; Workflow C STEP C.2 |
| **UU 13/2003 Pasal 153** | Career break protection (alumni returning post-family leave) | Workflow D STEP D.3 (tenure normalization) |
| **PKB Polytron** | Dignified offboarding | Workflow A (full choreography) |
| **GCG Code Polytron** | Stakeholder relationship value + integrity | Cross-cutting Workflow X (Ethical Guardrail) |

### 4.6 Risk Register Mapping

| Risk | Inherent | Residual | Workflow Mitigation |
|---|---|---|---|
| Consent violation (alumni data without permission) | CRITICAL | LOW | Workflow B STEP B.2 + Workflow C STEP C.2 |
| WBS content leakage via boomerang process | CRITICAL | NEAR-ZERO | Workflow D STEP D.4 + SP-84 |
| Alumni pressured for engagement | HIGH | LOW | Workflow C STEP C.8 + SP-85 |
| Boomerang with hidden WBS history | CRITICAL | LOW | Workflow D STEP D.4 (mandatory P3 sealed validation) |
| Retiree exploitation (over-asking advisors) | MEDIUM | LOW | Workflow G STEP G.4 (capacity ceiling) + STEP G.7 |
| Knowledge graph individual identification | CRITICAL | LOW | Workflow E STEP E.3 (k-anonymity) + STEP E.4 |

### 4.7 Quality Validation Criteria

| Q ID | Quality Criterion | Validation Cadence | Owner |
|---|---|---|---|
| **Q-55** | Alumni network engagement rate ≥ 30% of departing employees | Annual | Head of EX |
| **Q-56** | Boomerang conversion rate ≥ 30% (alumni signaled → hired) | Annual (coordinated with P6-W1) | Head of EX + Head of TA |

---

## 5. ERROR HANDLING & EDGE CASES

### 5.1 Edge Case Protocol Table

| Edge Case ID | Condition | IF → THEN Protocol |
|---|---|---|
| **E-1** | Missing or incomplete input fields at workflow entry | IF mandatory field missing → REJECT input; return structured error to upstream caller (P3-W3 / P6-W1 / Alumni Office); persist rejection in audit log; DO NOT default-fill missing data. |
| **E-2** | Alumni withdraws consent mid-lifecycle | IF withdrawal received → execute data minimization (purge tracking data, retain only legally-required transactional records); suspend all communications; maintain portal access if alumni opts to keep it; log withdrawal with timestamp; notify Workflows C, D, E, F. |
| **E-3** | P3 sealed counter returns SEALED_PENDING | IF SEALED_PENDING → remove candidate from current boomerang signal batch; schedule re-query in 14 days; DO NOT treat as NOT_VALIDATED; DO NOT log as suspect; DO NOT notify alumni or P6-W1. |
| **E-4** | P3 sealed counter API unavailable | IF API timeout / failure → suspend all boomerang signaling (Workflow D STEP D.4) until API restored; DO NOT signal candidates with stale validation; alert AI Governance Board if unavailability exceeds 24 hours. |
| **E-5** | Notice period shorter than 30 days (short-notice departure) | IF notice < 30 days → execute minimum-viable choreography (consent conversation + exit interview + dignified sendoff non-negotiable); offer retroactive alumni invitation Day 14 post-exit; record compressed-timeline justification in audit log. |
| **E-6** | Alumni declines all four consent scopes | IF all scopes == false → alumni_invitation_status = DECLINED; suspend Workflow B; honor decision permanently unless alumni initiates re-engagement; retain only legally-required final separation records. |
| **E-7** | Vague or ambiguous boomerang query from P6-W1 | IF skill criteria insufficient (missing required_skills array or skill_weights) → REJECT query with structured clarification request; DO NOT generate signals on guesswork; persist rejection in audit log. |
| **E-8** | Retiree declines pathway after HC-53 approval | IF retiree countersignature not received within 30 days of HC-53 approval → pathway lapses; record honorable transition with recognition ceremony only; HC-53 approval expires; no penalty or re-solicitation. |
| **E-9** | Oral history project scope creep mid-engagement | IF facilitator or P6-W4 detects scope expansion beyond HC-53 approved scope → SUSPEND project; re-submit revised scope for HC-53 re-approval; DO NOT continue under original approval. |
| **E-10** | Deceased alumni record encountered | IF alumni status = deceased → suspend all communications immediately; mark record as memorial-only; coordinate with family per cultural and PKB Polytron norms; preserve knowledge graph contributions per pre-death consent; archive oral history materials per family wishes. |
| **E-11** | Dual-status alumni (active boomerang candidate + current contract employee) | IF candidate appears in active employee roster → REMOVE from boomerang signal batch; route inquiry to Internal Mobility process (not P6-W4 scope); log dual-status detection. |
| **E-12** | Litigation-pending exit (active dispute at separation) | IF P3 sealed counter returns SEALED_PENDING due to litigation → suspend boomerang eligibility indefinitely; do NOT proceed with alumni invitation until P3 status clarifies; DO NOT log litigation status (sealed); alumni network membership permitted only if alumni initiates and litigation does not preclude. |
| **E-13** | P2 Ethical Guardrail returns BLOCK on alumni communication | IF BLOCK verdict → reject payload (no override); log BLOCK reason; notify originating workflow; require communication re-design before re-submission; if pattern emerges (≥3 BLOCKs in 30 days), escalate to Head of EX + AI Governance Board. |
| **E-14** | HC-53 approval not received within 14-day SLA | IF SLA breach → escalate to CEO per defined escalation path; suspend dependent workflow steps; persist SLA breach in audit log; re-issue HC-53 request with escalation flag. |
| **E-15** | K-anonymity threshold cannot be met for knowledge graph cut | IF cohort < 5 alumni → suppress the cut; generalize attributes (broaden tenure band, role family) until k ≥ 5 OR omit the cut entirely; NEVER release a cut below threshold. |
| **E-16** | Alumni reports unauthorized contact attributed to Polytron | IF complaint received → immediately suspend all outbound communications to that alumni; investigate via P3 sealed channel; coordinate with DPO + Legal; if breach confirmed, trigger rollback per Section 6 of parent agent spec; persist incident in audit log. |
| **E-17** | Conflicting consent records (portal state vs. last captured consent payload) | IF mismatch detected → treat as DECLINED for the disputed scope; suspend related communications; trigger consent re-confirmation conversation; resolve before next touchpoint. |
| **E-18** | Annual consent refresh lapses (no response from alumni) | IF refresh window passes without alumni action → send single soft reminder; if no response within 30 days → suspend communications (preserve portal access); maintain suspended state until alumni initiates refresh; treat as lapsed-not-withdrawn. |

### 5.2 System Failure Recovery

- **F-1**: IF audit log API unavailable → buffer logs locally; halt all state-changing operations; resume only after audit log API restored AND buffered entries persisted in correct chronological order.
- **F-2**: IF P2 Ethical Guardrail unavailable → halt all outbound communications; queue payloads; resume after Guardrail restored; never bypass governance gate.
- **F-3**: IF alumni portal unavailable → suspend portal-dependent operations (Workflows B, C, F); maintain offline communication channels (email-only) for time-sensitive messages; reconcile state after portal restoration.
- **F-4**: IF P2-W2 Skills Taxonomy unavailable → suspend Workflow E; queue updates; resume after restoration; never write to a partial or inconsistent graph state.

### 5.3 Escalation Decision Matrix

| Severity | Trigger | Escalation Target | SLA |
|---|---|---|---|
| **LOW** | Single E-1 / E-7 occurrence | Workflow caller (P3-W3 / P6-W1 / Alumni Office) | 24 hours |
| **MEDIUM** | E-2 / E-6 / E-8 / E-17 / E-18 occurrence | Head of EX | 48 hours |
| **HIGH** | E-4 / E-13 (single) / E-14 | Head of EX + AI Governance Board | 24 hours |
| **CRITICAL** | E-13 pattern (≥3 in 30 days) / E-16 / consent breach / WBS content leak attempt | CHRO + DPO + Legal + AI Governance Board + CEO | Immediate |

### 5.4 Rollback Triggers (per Parent Agent Spec)

Workflow operations MUST initiate full rollback to legacy exit-only process (P3-W3 only; alumni portal maintained as standalone with lower engagement intensity) upon any of:

- Consent breach incident (E-16 confirmed)
- Clean separation validation architectural failure (E-4 sustained > 72 hours)
- Alumni complaint pattern (≥3 unauthorized contact reports in 30 days)

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL-P6-W4 |
| Parent Agent | P6-W4 — Alumni Network & Strategic Offboarding Orchestrator |
| Version | v1.0 |
| Status | DESIGN-COMPLETE \| PENDING DEPLOYMENT |
| Owner | Head of Employee Experience + Head of Talent Acquisition |
| Last Review | May 2026 |
| Next Review | November 2026 |
| Classification | INTERNAL — EX, TA, HRBP, OD, P3 sealed coordinators, AI Engineering |
| Distribution | CHRO, HR Director, Head of EX, Head of TA, Head of OD, ER Head, AI Governance Board, DPO, Legal, PKB representatives, AI Engineering Implementation Team |
| Companion Documents | AGENT_P6-W4_Alumni_Network_Strategic_Offboarding.md, P3-W3 Exit Interview Spec, P6-W1 TA Spec, P3 Sealed Protocol, UU PDP 27/2022 Compliance, POLYTRON_HR_AI_WAVE6_COMPLETION_INTEGRATION_v1_1.md |
| Supersedes | None (new skill module) |

---

**END OF SKILL MODULE**
