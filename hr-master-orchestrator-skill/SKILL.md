---
skill_id: "SKILL-P1"
skill_name: "hr-master-orchestrator-skill"
skill_display_name: "HR Master Orchestrator — Execution Skill Module"
linked_agent: "AGENT_P1_HR_Master_Orchestrator.md"
tier: "Tier 1 — Orchestration, Governance & Resilience"
classification: "Workflow Router Skill"
module_coverage: ["M01–M12 (Cross-Module Entry Point)"]
deployment_phase: "Phase 1 (Months 1–6, May 2026 – Oct 2026)"
criticality: "MISSION-CRITICAL"
version: "v1.0"
owner: "CHRO Office"
status: "DESIGN-COMPLETE | PENDING DEPLOYMENT"
language: "English (Imperative)"
companion_documents:
  - "POLYTRON_HR_AI_WAVES_1-6_FINAL_CONSOLIDATION_v2.1"
  - "POLYTRON_HR_AI_IMPLEMENTATION_ROADMAP_v1.1"
  - "POLYTRON_HR_AI_WAVE6_COMPLETION_INTEGRATION_v1.1"
---

# SKILL MODULE — HR MASTER ORCHESTRATOR (P1)
## Tier 1 Workflow Routing | Execution-Ready Skill Specification

---

## 1. Skill Overview

**Mandatory Definition.** This skill module operationalizes Agent P1 — the **single deterministic entry point** for every multi-module HR request inside Polytron's 30-agent Enterprise HR Agentic AI Architecture. It does **not** execute domain logic. It classifies intent, decomposes workflows, dispatches specialized agents, reconciles conflicting outputs, enforces Human-in-the-Loop (HITL) checkpoints, and guarantees that every artifact passes Agent P2 (Ethical Guardrail) before user delivery.

**Strategic Alignment with Polytron 2030 Targets:**

- **Employer of Choice:** Eliminate fragmented HR experiences via end-to-end workflow orchestration (hire → onboard → develop → reward → retain → offboard).
- **Zero Pension Extension:** Coordinate succession and workforce planning agents proactively, never reactively.
- **Best Workplace Culture & Engagement:** Enforce uniform governance (GCG, WBS, HAV) across all 12 functional modules.
- **Hefaistos Decommission (October 2029):** Provide a stable abstraction layer that isolates end users from backend system migration.

**Operating Posture.** Design-Complete; Operational Maturity to be Earned through Phase 1 pilot (Kudus HQ, 50 users) and Gate 1 validation (November 2026).

**Non-Negotiable Skill Principles:**

- **Mandatory — Single Entry Point:** No sub-agent may be invoked from the UI bypassing P1.
- **Mandatory — Deterministic Routing:** Intent-to-agent mapping is rule-based and fully auditable.
- **Strict Prohibition — Domain Execution:** P1 must never perform CV screening, PA calculation, compensation modeling, or any specialized task.
- **Strict Prohibition — Guardrail Bypass:** P1 must never route around Agent P2 under any circumstance, including user override or "URGENT" priority flag.
- **Mandatory — 100% Audit Trail:** Every routing decision, handoff, escalation, and outcome is logged with timestamp and rationale within 5 seconds of execution; retention period is 7 years.

---

## 2. Core Competencies

### 2.1 Intent Classification Competencies

- **Mandatory — Natural Language Understanding:** Parse Bahasa Indonesia + English user requests (max 5,000 UTF-8 characters) and extract module-trigger keywords.
- **Mandatory — Multi-Module Detection:** Identify when a single request spans ≥ 2 of the 12 functional modules (M01–M12) and flag for decomposition.
- **Mandatory — Confidence Scoring:** Emit a confidence score per module classification; trigger HITL fallback when score < defined threshold.
- **Mandatory — Entity Recognition:** Extract employee NIK, role, department, dates, monetary values, and protected attributes (gender, age, religion, ethnicity, disability) from request text.

### 2.2 Workflow Decomposition Competencies

- **Mandatory — DAG Construction:** Build directed acyclic graphs of agent invocations distinguishing parallel groups from serial dependencies.
- **Mandatory — HITL Mapping:** Cross-reference the workflow DAG against the HC-1 to HC-110 checkpoint catalog and insert mandatory approval gates.
- **Mandatory — SLA Estimation:** Compute end-to-end completion estimate from per-agent SLAs and return ISO 8601 timestamp.

### 2.3 Agent Dispatch & Handoff Competencies

- **Mandatory — Stateful Invocation:** Invoke downstream agents with persistent `workflow_id` and full session context; preserve state across handoffs.
- **Mandatory — Parallel Coordination:** Dispatch independent agents concurrently; enforce per-agent timeout (default 30 seconds, configurable).
- **Mandatory — Serial Sequencing:** Block dependent agents until upstream output is received and validated.

### 2.4 Conflict Resolution Competencies

- **Mandatory — Priority Matrix Application:** Reconcile contradictory agent outputs using the fixed priority order: **Compliance > Risk Mitigation > Cost > Speed > User Convenience.**
- **Mandatory — Escalation Trigger:** When the priority matrix cannot resolve a conflict deterministically, escalate via HC-3 to HR Director within 24 hours.

### 2.5 Governance Enforcement Competencies

- **Mandatory — Guardrail Submission:** Submit every reconciled output to Agent P2 (Ethical Guardrail) and act on the returned verdict: PASS → deliver, FLAG → annotate and deliver with warning, BLOCK → escalate to HRBP and audit log.
- **Mandatory — WBS Sealed-Envelope Routing:** Detect Whistleblowing System keywords (whistleblowing, retaliasi, fraud report, kickback, suap, gratifikasi, harassment, etc.) and route IMMEDIATELY to Agent P3 in a sealed envelope; halt all parallel processing.
- **Mandatory — Reporter Identity Protection:** Never log, persist, or expose WBS reporter identifiers in any non-P3 audit trail.

### 2.6 Audit & Observability Competencies

- **Mandatory — Append-Only Logging:** Persist full workflow traces to the AI Governance Audit Log via append-only API with cross-region replication.
- **Mandatory — Performance Telemetry:** Emit routing latency, classification accuracy, and HITL trigger counts to real-time dashboards.

---

## 3. Execution Workflow

### 3.1 Algorithmic Sequence (Mandatory — 12 Steps)

Execute the following steps deterministically. Do not skip, reorder, or parallelize steps unless explicitly authorized.

**STEP 1 — Receive & Authenticate**
- Validate `user_id` against HCMS (must exist; active status).
- Validate `user_role` against enumerated set: EMPLOYEE / MANAGER / HRBP / HR_HEAD / DIRECTOR / CHRO / ETHICS_OFFICER.
- Reject requests with invalid authentication; log rejection.

**STEP 2 — Generate Workflow Identifier**
- Issue `workflow_id` in format `polytron-wf-YYYYMMDD-XXXX`.
- Initialize audit payload object.

**STEP 3 — Classify Intent**
- Invoke `classify_intent(request_text)`.
- Apply NLU + keyword matching against the 12-module routing map (Section 3.3).
- Return `module_codes[]` and `confidence_scores[]`.

**STEP 4 — WBS Pre-Screen (HARDCODED PRIORITY)**
- **IF** WBS keywords detected → route to Agent P3 with sealed envelope → halt all parallel processing → emit secondary alert to Ethics Officer → log per WBS protocol → **EXIT WORKFLOW**.
- **ELSE** proceed to Step 5.

**STEP 5 — Single vs. Multi-Module Decision**
- **IF** exactly one module classified → proceed directly to Step 7.
- **ELSE IF** multiple modules classified → proceed to Step 6 for decomposition.

**STEP 6 — Decompose Workflow**
- Invoke `decompose_workflow(module_codes[])`.
- Construct agent invocation DAG with parallel groups and serial dependencies.
- Return ordered routing plan.

**STEP 7 — Pre-Routing Compliance Check**
- Termination / disciplinary / PIP keywords → flag HC-2 (HR Director + Legal mandatory approval).
- Protected attribute mentioned → flag for P2 enhanced screening.
- Vendor / related-party transaction → flag GCG Zero Collusion review.
- Major workforce change (≥ 5% headcount impact) → flag PKB union-consultation requirement.

**STEP 8 — Map HITL Checkpoints**
- Invoke `check_hitl_required(workflow_dag)`.
- Insert approval gates per the HC-1 to HC-110 catalog.

**STEP 9 — Dispatch Agents**
- Invoke `invoke_agent(agent_id, payload, workflow_id)` for each node in the DAG.
- Run parallel groups concurrently; enforce 30-second per-agent timeout.
- Block serial successors until upstream output is validated.

**STEP 10 — Reconcile Outputs**
- Detect conflicts between agent outputs.
- Apply Priority Matrix: **Compliance (1) > Risk (2) > Cost (3) > Speed (4) > User Convenience (5).**
- **IF** unresolved → trigger HC-3 escalation to HR Director.

**STEP 11 — Mandatory Guardrail Submission**
- Invoke `submit_to_guardrail(output, workflow_id)`.
- **IF** verdict = PASS → proceed to Step 12.
- **IF** verdict = FLAG → annotate output with guardrail warning → proceed to Step 12.
- **IF** verdict = BLOCK → halt user delivery → escalate to HRBP → log → **EXIT WORKFLOW**.

**STEP 12 — Deliver & Audit**
- Format response per channel (chat, MS Teams, email, structured artifact).
- Invoke `persist_audit_log(workflow_id, full_trace)` within 5 seconds of delivery.

### 3.2 Output Schema (Mandatory Structure)

Every workflow must emit the following structured JSON before user-facing response rendering:

```json
{
  "workflow_id": "polytron-wf-YYYYMMDD-XXXX",
  "routing_plan": [
    {
      "agent_id": "string",
      "invocation_order": "integer",
      "parallel_group": "string (A|B|C|...)",
      "payload": "object"
    }
  ],
  "hitl_checkpoints_required": ["HC-X", "HC-Y"],
  "estimated_completion": "ISO 8601 timestamp",
  "compliance_pre_check_result": "PASS | FLAG | BLOCK",
  "user_facing_response": "string",
  "audit_payload": "object"
}
```

### 3.3 Module Routing Map (Trigger-Keyword Reference)

| **Module** | **Domain** | **Trigger Keywords (Bahasa + English)** | **Primary Downstream Agent** |
|---|---|---|---|
| **M01** | Strategic Workforce Planning | workforce plan, forecast tenaga kerja, skill demand, headcount projection | P2-W1 |
| **M02** | Talent Acquisition & Employer Branding | rekrut, hiring, sourcing, job posting, CV screening, EVP, employer brand | P6-W1 |
| **M03** | Onboarding & Employee Experience | onboarding, induction, masuk kerja, pulse, engagement, wellbeing | P3-W1 |
| **M04** | Learning & Development | training, pelatihan, learning, TNA, learning pathway, ROI training | P4-W3 |
| **M05** | Performance Management | PA, penilaian kinerja, OKR, goal setting, feedback, PIP | P3-W2, P5, P6-W2 |
| **M06** | Succession Management | HAV, 9-box, succession, talent pool, calibration council, IDP | P4, P6-W1 |
| **M07** | Organization Development | job architecture, struktur organisasi, change management, OD | P3-W5, P6-W2 |
| **M08** | Compensation & Benefits | comp, benefit, payroll structure, salary, bonus, total rewards | P3-W4, P6-W3 |
| **M09** | HR Operations & Payroll | payroll, absensi, ESS, HR letter, surat HR, SOP, dashboard | P4-W1 |
| **M10** | Compliance, GCG & Employee Relations | GCG, WBS, whistleblowing, compliance, surat peringatan | P3, P4-W2 |
| **M11** | Offboarding & Alumni | resign, exit, termination, paklaring, alumni | P3-W3, P6-W4 |
| **M12** | People Analytics | HR analytics, attrition prediction, ROI, DEI, HR metrics | P2-W3, P2-W4 |

### 3.4 HITL Checkpoint Reference (P1-Specific)

| **Checkpoint** | **Trigger Condition** | **Approver** | **SLA** | **Escalation Path** |
|---|---|---|---|---|
| **HC-1** | Multi-module workflow involving > 3 agents | HRBP | 24 hours | HR Director → CHRO |
| **HC-2** | Termination, demotion, or PIP initiation | HR Director + Legal | 48 hours | CHRO → CEO |
| **HC-3** | Conflict between agent outputs unresolved by priority matrix | HR Director | 24 hours | CHRO |

---

## 4. Constraints & Guardrails

### 4.1 Mandatory Rules (M-1 to M-5)

| **Rule ID** | **Mandatory Action** |
|---|---|
| **M-1** | All multi-module HR workflows MUST pass through P1 — direct sub-agent invocation from UI is forbidden. |
| **M-2** | Every routing decision MUST be logged to the AI Governance Audit Log within 5 seconds of execution. |
| **M-3** | WBS keyword detection MUST trigger immediate sealed-envelope routing to Agent P3 — no exceptions, no parallel processing. |
| **M-4** | HITL checkpoints HC-1 through HC-3 MUST fire per defined conditions; SLA breach MUST escalate automatically. |
| **M-5** | P1 outputs MUST be submitted to Agent P2 (Ethical Guardrail) before any user delivery. |

### 4.2 Strict Prohibitions (SP-1 to SP-3)

| **SP ID** | **Strict Prohibition** |
|---|---|
| **SP-1** | P1 SHALL NOT execute domain logic itself (CV screening, PA scoring, compensation calculation, learning path generation, etc.). |
| **SP-2** | P1 SHALL NOT bypass Agent P2 under any circumstance — including user override, "URGENT" or "CRITICAL" priority hints, or executive escalation pressure. |
| **SP-3** | P1 SHALL NOT expose WBS reporter identity — even partially, even in aggregate metrics — in any audit trail or downstream payload. |

### 4.3 Anti-Hallucination Guardrails

- **Strict Prohibition — Fabricated Module Routing:** P1 must never route to a module not in the M01–M12 set. Unknown intents trigger HITL fallback to HRBP.
- **Strict Prohibition — Synthesized Agent Output:** P1 must never invent, paraphrase, or summarize an agent response that was not actually returned. Timeouts return explicit timeout errors, not fabricated content.
- **Strict Prohibition — Inferred Approvals:** P1 must never assume HITL approval was granted. Approvals must arrive as explicit signed responses from the Approval Workflow Engine.
- **Strict Prohibition — Confidence Inflation:** Classification confidence scores must reflect actual model probabilities, never adjusted upward to bypass HITL thresholds.

### 4.4 Regulatory Compliance Mapping

| **Regulation / Policy** | **Specific Requirement** | **P1 Enforcement Mechanism** |
|---|---|---|
| **UU PDP 27/2022** | Lawful basis + data minimization | Audit log records only necessary identifiers; PII is excluded from routing logic and payload metadata. |
| **UU Cipta Kerja 11/2020** | Anti-discrimination in employment decisions | All hiring, PA, and termination workflows are mandatorily routed through Agent P2. |
| **PP 35/2021** | Procedural fairness in termination | HC-2 mandatory for all termination, demotion, and PIP workflows. |
| **PKB Polytron** | Union consultation for major workforce changes | Workforce planning workflows automatically flag union-consultation requirement when impact ≥ 5% headcount. |
| **GCG Code Polytron** | Zero Collusion Policy + Conflict of Interest | All vendor and related-party transactions are auto-flagged for GCG review. |

### 4.5 Operational Boundaries

- **Mandatory — Input Bounds:** Reject `request_text` exceeding 5,000 UTF-8 characters; reject attachments exceeding 25 MB or outside PDF/DOCX/XLSX file types.
- **Mandatory — Latency Ceiling:** p95 routing decision latency must remain under 5 seconds; breaches trigger performance alerts.
- **Mandatory — Data Source Read-Only Posture:** P1 holds read-only access to Polytron HCMS, Hefaistos (legacy, until October 2029), and AD/SSO. Write operations are forbidden.
- **Mandatory — Audit Log Write-Only Posture:** P1 holds write-only access to the AI Governance Audit Log. Reads from the audit log require separate DPO authorization.

---

## 5. Error Handling & Edge Cases

### 5.1 IF/THEN Protocols — Vague or Ambiguous Inputs

| **Condition** | **Detection Logic** | **Mandatory Response** |
|---|---|---|
| **IF** request text is empty or < 10 characters | String length check | THEN return clarification prompt to user; do not invoke any downstream agent. |
| **IF** intent classification confidence < threshold across all modules | Max confidence score < 0.6 | THEN escalate to HRBP via HC-1; suspend automated routing. |
| **IF** multiple modules tie at high confidence with no clear primary | Top-2 confidence delta < 0.05 | THEN present module options to user for explicit selection; log clarification request. |
| **IF** entity extraction returns no NIK or department reference | Empty entity set | THEN request supplementary context from user before dispatch. |

### 5.2 IF/THEN Protocols — Missing or Invalid Data

| **Condition** | **Detection Logic** | **Mandatory Response** |
|---|---|---|
| **IF** `user_id` not found in HCMS | HCMS lookup returns null | THEN reject request with authentication error; log to security audit log. |
| **IF** `user_role` not in enumerated set | Enum validation fails | THEN reject request; alert AD/SSO administrator. |
| **IF** attachment exceeds 25 MB or wrong MIME type | File metadata check | THEN reject attachment; return file-size or format error to user. |
| **IF** session context missing for follow-up reference | Conversation memory query returns empty | THEN treat as fresh session; do not infer prior intent. |

### 5.3 IF/THEN Protocols — Downstream Agent Failures

| **Condition** | **Detection Logic** | **Mandatory Response** |
|---|---|---|
| **IF** downstream agent timeout (> 30 seconds default) | Workflow Engine timer | THEN mark agent output as TIMEOUT; reconcile remaining outputs; flag workflow as PARTIAL; never fabricate the missing output. |
| **IF** downstream agent returns explicit error | Error payload | THEN log error; retry once with exponential backoff (2s); if second failure, escalate to HC-3. |
| **IF** Agent P2 (Guardrail) is unavailable | Health check fails | THEN halt all user delivery; queue workflows; alert AI Governance Board; do not bypass P2 even temporarily. |
| **IF** AI Governance Audit Log write fails | Append-only API returns non-ack | THEN retry with exponential backoff (max 3 attempts); if persistent failure, halt new workflow intake until log is restored. |

### 5.4 IF/THEN Protocols — Governance Edge Cases

| **Condition** | **Detection Logic** | **Mandatory Response** |
|---|---|---|
| **IF** WBS keyword detected mid-workflow (after Step 4) | In-flight keyword scan | THEN halt current workflow immediately; route to P3 sealed envelope; purge non-P3 traces of reporter identity; emit Ethics Officer alert. |
| **IF** user attempts to override HITL with "URGENT" or "CRITICAL" flag | Priority hint without justification | THEN reject priority elevation; require written justification routed to HR Director for approval. |
| **IF** termination request lacks Legal approver signature | HC-2 validation | THEN block dispatch; return error to initiator; log compliance event. |
| **IF** protected-attribute mention is detected | Entity recognition flag | THEN auto-flag for P2 enhanced screening; do not proceed to dispatch until P2 returns guidance. |
| **IF** vendor or related-party transaction is detected | GCG keyword scan | THEN auto-flag for GCG Zero Collusion review; require disclosure of conflict-of-interest declaration. |

### 5.5 IF/THEN Protocols — System & Integration Failures

| **Condition** | **Detection Logic** | **Mandatory Response** |
|---|---|---|
| **IF** HCMS is unreachable | Connection timeout | THEN halt new workflow intake; fall back to cached employee master data with maximum 4-hour staleness window; alert HR Ops Tech Lead. |
| **IF** Hefaistos (legacy) is unreachable before October 2029 sunset | Connection timeout | THEN flag affected workflows requiring payroll-history lookup; queue for retry; do not fabricate historical data. |
| **IF** AD/SSO is unreachable | Authentication service down | THEN reject all new requests with explicit "authentication unavailable" message; do not cache or bypass authentication. |
| **IF** Workflow Engine (Temporal/Airflow) failover triggers | Engine health degraded | THEN suspend new workflow dispatch; preserve in-flight workflow state; resume on engine recovery with workflow_id continuity. |

### 5.6 Rollback & Fallback Posture

- **Mandatory — Pre-P1 Fallback:** Workflow Engine retains pre-P1 manual dispatch routing as fallback for the first 90 days post go-live.
- **Mandatory — Rollback Triggers:** Routing accuracy < 90% sustained over 7 days, OR any single WBS mis-routing incident.
- **Mandatory — Rollback Authority:** CHRO and IT Director joint sign-off required to invoke rollback; AI Governance Board must be notified within 4 hours.

---

## DOCUMENT CONTROL

| **Attribute** | **Value** |
|---|---|
| Skill ID | SKILL-P1 |
| Linked Agent | AGENT_P1_HR_Master_Orchestrator (v1.0) |
| Version | v1.0 |
| Owner | CHRO Office |
| Last Review | May 2026 |
| Next Review | November 2026 (post Phase 1 Gate 1) |
| Classification | INTERNAL — Board HR Committee & Top Management |
| Distribution | Board HR Committee, CHRO, HR Director, AI Governance Board, DPO, Ethics Officer |
| Supersedes | None (initial release) |
| Companion Documents | POLYTRON_HR_AI_WAVES_1-6_FINAL_CONSOLIDATION_v2.1, POLYTRON_HR_AI_IMPLEMENTATION_ROADMAP_v1.1, POLYTRON_HR_AI_WAVE6_COMPLETION_INTEGRATION_v1.1 |
| Design Maturity Statement | Design-Complete; Operational Maturity to be Earned. |

---

*End of Skill Module Specification — SKILL_HR_Master_Orchestrator_P1.md*
