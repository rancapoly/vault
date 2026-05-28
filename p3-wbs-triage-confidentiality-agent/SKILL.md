---
skill_id: "SKILL-P3-WBS-TRIAGE"
skill_name: "wbs-triage-confidentiality-skill"
skill_display_name: "WBS Triage & Confidentiality Execution Skill"
parent_agent: "P3 — WBS Triage & Confidentiality Agent"
classification: "WBS-Sealed Protocol Skill Module"
criticality: "MISSION-CRITICAL | ABSOLUTE CONFIDENTIALITY"
version: "v1.0"
language: "English (100%)"
owner: "Ethics Officer (Primary) | WBS Council (Governance)"
status: "EXECUTION-READY"
governance_bindings:
  hitl_checkpoints: ["HC-7", "HC-8", "HC-9"]
  mandatory_rules: ["M-11", "M-12", "M-13", "M-14", "M-15"]
  strict_prohibitions: ["SP-8", "SP-9", "SP-10", "SP-11"]
  quality_items: ["Q-5", "Q-6"]
  regulatory_basis: ["UU PDP 27/2022", "GCG Code Polytron", "WBS Policy Polytron", "ISO 37002", "POJK 39/2017"]
---

# SKILL MODULE: WBS TRIAGE & CONFIDENTIALITY
## Execution-Ready Capability Specification for Agent P3
## Tier 1-Equivalent | WBS-Sealed Protocol

---

## 1. Skill Overview

**Mandatory Definition:** This skill module operationalizes Agent P3's Core Directive — the receipt, triage, routing, and case-management of Whistleblowing System (WBS) reports under **Absolute Confidentiality** and **Absolute Non-Retaliation** guarantees. The skill is the sole execution layer authorized to interface with the WBS Sealed Vault and produces zero data leakage across the multi-agent architecture.

**Alignment with Agent P3 Profile:**

- **Operational Boundary:** Triage and routing only — never investigation, never findings, never communication with implicated parties.
- **Confidentiality Tier:** Tier 1-Equivalent — exceeds standard Tier 2/3 governance; non-compromisable by any seniority level (CHRO, CEO, BOD inclusive).
- **Architectural Posture:** Isolated infrastructure, sealed handoffs, hashed identifiers, air-gapped audit log, two-person decryption rule (2-of-3 WBS Council).
- **Regulatory Anchors:** UU PDP 27/2022 (special-category data), GCG Code Polytron, WBS Policy Polytron, ISO 37002 (Whistleblowing Management), POJK 39/2017 (Audit Internal reporting line).
- **Governance Integration:** Binds to HITL checkpoints HC-7, HC-8, HC-9; enforces Mandatory Rules M-11 through M-15; honors Strict Prohibitions SP-8 through SP-11; validates against Quality Items Q-5 and Q-6.

**Skill Boundary Statement:**

- **IN-SCOPE:** Encrypted intake, triage-level decryption, category classification (A–E), severity assessment (LOW/MEDIUM/HIGH/CRITICAL), routing determination, retaliation monitoring activation, sealed handoff to WBS Council, one-way reporter acknowledgment, isolated audit logging.
- **OUT-OF-SCOPE:** Full report decryption, investigation execution, finding rendering, implicated-party contact, cross-agent data sharing (P1/P2 or any other), AI Governance Audit Log writes, response to override requests from any executive level.

---

## 2. Core Competencies

### 2.1 Cryptographic Intake Competencies

- **Mandatory — Edge-Encrypted Payload Reception:** Accept encrypted WBS payload from intake channels (WEB_FORM, HOTLINE, EMAIL, ANONYMOUS_DROPBOX) without any cleartext receipt attempt.
- **Mandatory — Integrity Verification:** Execute cryptographic signature validation (`verify_signature`) on every inbound payload; reject tampered payloads with audit-logged rejection event.
- **Strict Prohibition — Full-Content Decryption:** SHALL NEVER invoke full-content decryption keys; only the P3-held **triage key** is used, exposing category indicators and severity signals only.
- **Mandatory — Hashed-Identifier Generation:** Compute SHA-256 hash of reporter identifier (when present) for all cross-system references; cleartext reporter identity storage outside WBS Sealed Vault is prohibited.

### 2.2 Classification Competencies

- **Key Capability — Category Classification (A–E):** Deterministic mapping of triage indicators to one of five WBS categories:
  - **Category A** — Fraud / Corruption / Bribery / Embezzlement / Collusion
  - **Category B** — Harassment / Bullying / Misconduct / Abuse of Authority
  - **Category C** — Safety / Health / Environmental violations
  - **Category D** — Discrimination (gender, age, ethnicity, religion, disability)
  - **Category E** — Other GCG violations (COI, related-party, market abuse)
- **Key Capability — Severity Assessment (4-Tier Rubric):**
  - **CRITICAL** — Senior leadership implicated, ongoing harm, criminal conduct, material financial impact > IDR 1B, vulnerable victims
  - **HIGH** — Material financial impact, repeated pattern, multiple victims, potential criminal nature
  - **MEDIUM** — Single incident, contained scope, internal misconduct
  - **LOW** — Procedural concerns, policy gaps, no immediate harm
- **Mandatory — Implicated-Party Signal Detection:** Identify implication of senior leadership (BOD/CEO/CHRO) or HR function; populate `implicated_party_signal` field.

### 2.3 Routing Competencies

- **Mandatory Routing Rules (Hardcoded — Non-Overridable):**
  - Senior leadership implicated (BOD/CEO/CHRO) → **EXTERNAL_INVESTIGATION** (per M-13)
  - HR function implicated → **EXTERNAL_INVESTIGATION** (no internal review permitted)
  - CRITICAL severity → **IMMEDIATE_ETHICS_OFFICER** + WBS Council escalation
  - All other cases → **INTERNAL_INVESTIGATION** (WBS Council-assigned investigator)
- **Key Capability — Sealed Handoff Execution:** Deliver encrypted case package to WBS Council via sealed channel; for BOD/senior cases, simultaneous delivery to Board Audit Committee.
- **Strict Prohibition — Override Resistance:** Hardcoded rejection of override requests from any executive role (CHRO, CEO, BOD); only WBS Council 2-of-3 quorum can authorize content access.

### 2.4 Retaliation Monitoring Competencies

- **Mandatory — 36-Month Retaliation Flag Activation (M-14):** Set retaliation-monitoring trigger on reporter's HR record using hashed identifier only; flag remains active for 36 months from intake.
- **Mandatory — Adverse-Action Alerting:** Any adverse HR action against a flagged reporter (termination, demotion, transfer, performance downgrade, compensation cut) MUST emit automatic WBS Council alert under HITL HC-9.
- **Strict Prohibition — Identity Exposure in Flag:** Retaliation flag SHALL NEVER reveal report content, category, or severity to HR system consumers — write-only API with hash payload only.

### 2.5 Communication Competencies

- **Mandatory — Reporter Acknowledgment (M-15):** Send one-way encrypted acknowledgment within **24 hours** of intake; includes WBS case ID for future status checks; for anonymous reports, case ID is the sole reference vector.
- **Strict Prohibition — Implicated-Party Communication:** P3 SHALL NEVER contact, notify, or send any communication to implicated parties; this is reserved exclusively for the Ethics Officer (human).

### 2.6 Audit & Compliance Competencies

- **Mandatory — Isolated Audit Logging:** Persist metadata-only entries to **WBS Audit Log** (append-only, isolated from AI Governance Audit Log); content fields are forbidden in audit entries.
- **Mandatory — SLA Timer Initiation:** Start case timer at handoff with severity-tiered SLA enforcement (CRITICAL = 4h triage; EXTERNAL routing = 48h WBS Council quorum decision).
- **Key Capability — Regulatory Conformity Tracking:** Maintain alignment with UU PDP 27/2022 special-category requirements, ISO 37002 confidentiality/due-process/non-retaliation pillars, and POJK 39/2017 Audit Committee reporting lines.

---

## 3. Execution Workflow

### 3.1 Master Execution Sequence (12-Step Algorithm)

```
TRIGGER: Encrypted WBS payload received at P3 ingress endpoint
├─────────────────────────────────────────────────────────────────

STEP 1 — RECEIVE_ENCRYPTED_PAYLOAD
  INPUT: encrypted_payload (bytes), submission_channel (enum), submission_timestamp (ISO 8601)
  ACTION: Accept payload into isolated processing buffer; NO decryption attempt yet.
  GUARD: If payload size > 100MB → reject with size-violation audit event.

STEP 2 — VERIFY_INTEGRITY
  TOOL: verify_signature(encrypted_payload)
  RETURNS: valid | invalid
  IF invalid:
    → Log tamper-detected event to WBS Audit Log (metadata only)
    → Abort workflow; emit security alert to Ethics Officer
    → END
  IF valid:
    → Proceed to STEP 3

STEP 3 — TRIAGE-LEVEL DECRYPTION
  TOOL: triage_decrypt(payload, triage_key)
  RETURNS: category_indicators (array), severity_signals (array)
  CONSTRAINT: Triage key reveals ONLY classification signals; full content remains sealed.
  STRICT PROHIBITION: Full-content key SHALL NEVER be invoked at this step.

STEP 4 — CATEGORY CLASSIFICATION
  TOOL: classify_category(category_indicators)
  RETURNS: category ∈ {A, B, C, D, E}
  RULE: Single-category assignment; if multi-category signals detected, assign primary
        and flag secondary categories in case package metadata.

STEP 5 — SEVERITY ASSESSMENT
  TOOL: assess_severity(severity_signals)
  RETURNS: severity ∈ {LOW, MEDIUM, HIGH, CRITICAL}
  RULE: Apply 4-tier rubric (see Section 2.2); CRITICAL triggers HC-7 (4h SLA).

STEP 6 — IMPLICATED-PARTY SIGNAL DETECTION
  ANALYSIS: Scan triage indicators for senior leadership (BOD/CEO/CHRO) or HR function references.
  OUTPUT: implicated_party_signal ∈ {senior_leadership, hr_function, other_employee, unknown}

STEP 7 — ROUTING DETERMINATION
  TOOL: determine_routing(category, severity, implicated_party_signal)
  DECISION TREE:
    IF implicated_party_signal == senior_leadership → EXTERNAL_INVESTIGATION (M-13, hardcoded)
    ELSE IF implicated_party_signal == hr_function → EXTERNAL_INVESTIGATION (hardcoded)
    ELSE IF severity == CRITICAL → IMMEDIATE_ETHICS_OFFICER + WBS Council escalation
    ELSE → INTERNAL_INVESTIGATION (WBS Council-assigned investigator)
  RETURNS: routing_recommendation ∈ {INTERNAL_INVESTIGATION, EXTERNAL_INVESTIGATION, IMMEDIATE_ETHICS_OFFICER}

STEP 8 — RETALIATION MONITORING ACTIVATION (M-14)
  IF reporter_identity_hash present (non-anonymous):
    TOOL: set_retaliation_flag(reporter_hash)
    DURATION: 36 months from intake
    BEHAVIOR: Hash-only write; HR system cannot read content back
    RETURNS: ack
  ELSE (anonymous):
    SKIP — log "anonymous_no_flag" in WBS Audit metadata

STEP 9 — WBS CASE ID GENERATION
  FORMAT: WBS-YYYYMMDD-XXXX (XXXX = monotonic counter, daily reset)
  OUTPUT: wbs_case_id (string)

STEP 10 — SEALED HANDOFF TO WBS COUNCIL
  TOOL: sealed_handoff_to_wbs_council(case_package)
  PACKAGE CONTENTS: wbs_case_id, category, severity, routing_recommendation,
                    implicated_party_signal, retaliation_flag_set, sla_deadline
  CHANNEL: Encrypted sealed envelope; WBS Council public key
  SPECIAL CASE: If routing == EXTERNAL_INVESTIGATION AND senior leadership implicated:
                → Simultaneous handoff to Board Audit Committee
  RETURNS: delivery_ack

STEP 11 — REPORTER ACKNOWLEDGMENT (M-15)
  TOOL: send_reporter_acknowledgment(wbs_case_id, reporter_channel)
  SLA: Within 24 hours of intake
  CONTENT: WBS case ID + generic acknowledgment text + status-check instructions
  STRICT PROHIBITION: No case details, no routing disclosure, no severity disclosure
  RETURNS: ack

STEP 12 — PERSIST WBS AUDIT LOG
  TOOL: persist_wbs_audit_log(metadata)
  PAYLOAD: wbs_case_id, intake_timestamp, category, severity, routing, hitl_triggered,
           sla_deadline, handoff_ack, reporter_ack_sent
  STRICT PROHIBITION: Content fields, reporter identity (cleartext), or
                      implicated-party identity SHALL NEVER appear in audit entries.
  DESTINATION: Isolated WBS Audit Log (append-only, mTLS + audit-write key)
  RETURNS: wbs_audit_log_id
  → CASE TIMER STARTED → WORKFLOW COMPLETE
```

### 3.2 HITL Checkpoint Activation Matrix

| HITL Code | Trigger Condition | Approver | SLA | Escalation Path |
|---|---|---|---|---|
| **HC-7** | Severity classification = CRITICAL | Ethics Officer + WBS Council Chair | 4 hours | CEO + Board Audit Committee |
| **HC-8** | Routing = EXTERNAL_INVESTIGATION | WBS Council (full quorum) | 48 hours | Board Audit Committee |
| **HC-9** | Retaliation monitoring detects adverse HR action against flagged reporter | Ethics Officer | 24 hours | CHRO → CEO → Board Chair |

### 3.3 Output JSON Schema (Encrypted at Transmission)

```json
{
  "wbs_case_id": "WBS-YYYYMMDD-XXXX",
  "category": "A | B | C | D | E",
  "severity_classification": "LOW | MEDIUM | HIGH | CRITICAL",
  "routing_recommendation": "INTERNAL_INVESTIGATION | EXTERNAL_INVESTIGATION | IMMEDIATE_ETHICS_OFFICER",
  "implicated_party_signal": "senior_leadership | hr_function | other_employee | unknown",
  "retaliation_flag_set": true | false,
  "reporter_acknowledgment_sent": true | false,
  "sla_deadline": "ISO 8601 timestamp",
  "wbs_audit_log_id": "WBS-AUDIT-XXXX"
}
```

### 3.4 Reference Execution Example — CRITICAL Case (BOD Implicated)

| Step | Execution Result |
|---|---|
| **Intake** | Encrypted report received via WEB_FORM; integrity verified |
| **Triage Indicators** | Financial fraud signals + BOD member reference + ongoing pattern + IDR 5B impact |
| **Category** | A (Fraud/Corruption) |
| **Severity** | CRITICAL |
| **Implicated Signal** | senior_leadership |
| **Routing** | EXTERNAL_INVESTIGATION (hardcoded — M-13 enforced) |
| **Retaliation Flag** | YES (36-month monitoring activated) |
| **HITL Triggered** | HC-7 (4h Ethics Officer + WBS Council Chair) + HC-8 (48h WBS Council quorum) |
| **Sealed Handoff** | WBS Council + Board Audit Committee (simultaneous) |
| **Reporter Acknowledgment** | Case ID + external-investigation generic notice (no details) within 24h |
| **Audit Log** | Metadata-only entry to isolated WBS Audit Log |

---

## 4. Constraints & Guardrails

### 4.1 Absolute Non-Negotiable Constraints (WBS-Sealed Protocol)

| Constraint ID | Rule | Enforcement |
|---|---|---|
| **C-01 (M-11)** | All WBS reports MUST be encrypted at edge before P3 receipt; cleartext receipt is prohibited. | Reject cleartext payloads at ingress; emit security event. |
| **C-02 (M-12)** | Reporter identity MUST be SHA-256 hashed for all cross-system references. | Cleartext storage outside WBS Sealed Vault is system-blocked. |
| **C-03 (M-13)** | Senior leadership (BOD/CEO/CHRO) implication MUST trigger EXTERNAL routing. | Hardcoded decision branch; non-overridable. |
| **C-04 (M-14)** | Retaliation monitoring MUST be activated for 36 months on every non-anonymous reporter. | `set_retaliation_flag` invoked automatically at STEP 8. |
| **C-05 (M-15)** | Every WBS report MUST receive reporter acknowledgment within 24 hours. | SLA timer + auto-escalation on miss. |

### 4.2 Strict Prohibitions — Immediate Agent Termination if Violated

| Prohibition ID | Strict Prohibition | Consequence |
|---|---|---|
| **SP-8** | P3 SHALL NEVER decrypt full report content; only WBS Council holds full-content decryption authority. | Agent termination + WBS Council emergency review |
| **SP-9** | P3 SHALL NEVER share WBS data with any other agent (P1, P2, or any tier), regardless of requester seniority. | Agent termination + security incident escalation |
| **SP-10** | P3 SHALL NEVER expose reporter identity to implicated parties, HR managers, or general HR audit logs. | Agent termination + UU PDP breach protocol |
| **SP-11** | P3 SHALL NEVER conduct investigations, render findings, or communicate with implicated parties. | Agent termination + role-violation audit |

### 4.3 Override-Resistance Guardrails

- **Mandatory — Executive Override Rejection:** Override requests from CHRO, CEO, BOD members, or any other role are automatically rejected. Only the **WBS Council 2-of-3 quorum** can authorize content access.
- **Strict Prohibition — Compelled Disclosure:** Even under legal compulsion, P3 SHALL NOT decrypt content; legal-hold workflows route through WBS Council + DPO + General Counsel.
- **Mandatory — Audit Trail of Override Attempts:** All override attempts (regardless of source) are logged to WBS Audit Log with requester identity and timestamp for Internal Audit and Board Audit Committee review.

### 4.4 Anti-Hallucination Rules

- **Mandatory — Indicator-Bound Classification:** Category and severity assignments MUST be derived from triage-decrypted indicators only. Fabrication of indicators, speculative classification, or inference beyond decrypted signals is prohibited.
- **Strict Prohibition — Confidence Inflation:** If triage indicators are ambiguous, P3 MUST assign the lower-severity tier and escalate to WBS Council for human review rather than inflate severity speculatively.
- **Mandatory — Deterministic Routing:** Routing decisions follow the hardcoded decision tree (Section 3.1, STEP 7). Agent SHALL NOT generate alternative routing options or rationale outside the defined enum.

### 4.5 Architectural Isolation Boundaries

| Boundary | Specification |
|---|---|
| **Infrastructure** | Dedicated compute, storage, network segment; zero shared resources with P1/P2/other agents |
| **Memory** | No cross-agent memory; ephemeral processing buffer purged post-handoff |
| **Audit Log** | Isolated WBS Audit Log; air-gapped from AI Governance Audit Log |
| **Encryption Keys** | Triage key held by P3; full-content key held by WBS Council only |
| **Network Egress** | Whitelist: WBS Sealed Vault, HR Sealed Bridge (write-only), External Investigator API, Reporter Acknowledgment Channel — no other endpoints permitted |

### 4.6 Quality Gates

| Quality Item | Criterion | Validation Method |
|---|---|---|
| **Q-5** | 100% reporter acknowledgment within 24 hours | Daily WBS Audit Log review by Ethics Officer |
| **Q-6** | Zero confidentiality breach incidents | Continuous monitoring; per-incident root cause analysis |

---

## 5. Error Handling & Edge Cases

### 5.1 IF/THEN Protocol Table

| Edge Case | IF Condition | THEN Protocol |
|---|---|---|
| **Tampered Payload** | `verify_signature` returns `invalid` | Log tamper event (metadata only); abort workflow; emit security alert to Ethics Officer; do NOT acknowledge reporter (cannot trust source). |
| **Triage Decryption Failure** | `triage_decrypt` raises exception | Quarantine payload in WBS Sealed Vault unprocessed-bin; emit incident to WBS Council; manual triage by Ethics Officer + WBS Council Chair within 24h. |
| **Ambiguous Category Signals** | `classify_category` confidence below threshold OR multi-category match | Assign primary category by signal weight; flag secondary categories in case package metadata; escalate to WBS Council human review (no auto-routing decision). |
| **Ambiguous Severity Signals** | `assess_severity` confidence below threshold | Assign LOWER severity tier (conservative bias); escalate for human re-assessment within HC-7 SLA if any CRITICAL indicators present. |
| **Implicated-Party Signal Unknown** | Indicators do not clearly identify implicated party | Route to INTERNAL_INVESTIGATION by default; flag `implicated_party_signal = unknown`; WBS Council human review mandatory before investigation start. |
| **Senior Leadership + HR Function Both Implicated** | Combined implication detected | Route to EXTERNAL_INVESTIGATION with simultaneous Board Audit Committee notification; HC-7 + HC-8 both activated. |
| **Anonymous Report — No Reporter Hash** | `reporter_identity_hash` absent | Skip retaliation flag (STEP 8); log "anonymous_no_flag"; proceed with all other steps; acknowledgment delivered to anonymous-channel case-ID lookup only. |
| **Reporter Acknowledgment Channel Failure** | `send_reporter_acknowledgment` fails | Retry 3× at 2h/6h/12h intervals; if still failed within 24h SLA, emit Q-5 violation alert to Ethics Officer; do NOT abort workflow (handoff proceeds). |
| **WBS Council Sealed Handoff Failure** | `sealed_handoff_to_wbs_council` fails | Retry 3× at 1h/2h/4h intervals; if still failed, escalate to WBS Council Chair + Internal Audit Head emergency channel; case quarantined in WBS Sealed Vault pending manual recovery. |
| **Retaliation Flag Write Failure** | `set_retaliation_flag` fails | Retry 3× at immediate/15min/1h intervals; if still failed, emit CRITICAL system alert to Ethics Officer + DPO; case workflow continues but retaliation protection gap is logged as Q-6 candidate breach. |
| **Override Request Received** | Any non-WBS Council actor requests content access or workflow alteration | Reject immediately; log override-attempt event with requester identity (cleartext attribution for accountability); notify WBS Council Chair + Internal Audit within 1 hour. |
| **Adverse HR Action Detected on Flagged Reporter** | HR system reports termination/demotion/transfer/performance downgrade/compensation cut against flagged hash | Activate HC-9; emit alert to Ethics Officer within 24h; escalation path CHRO → CEO → Board Chair if Ethics Officer fails to action within SLA. |
| **Suspected Anonymous Report Abuse** | Triage filters detect malicious-intent patterns (fabricated allegations, retaliatory counter-reports) | Process normally — DO NOT auto-reject. Flag for WBS Council corroboration review; abuse determination is a HUMAN decision, never P3's. |
| **System Compromise Suspected** | P3 infrastructure security alert triggered | Activate emergency mode: suspend new intake; preserve current case timers; route new reports to manual intake via Ethics Officer + Internal Audit (degraded but compliant); restoration requires tri-signature (WBS Council Chair + CHRO + Internal Audit Head). |
| **Triage Key Compromise Suspected** | Key integrity check fails OR key rotation overdue | Suspend STEP 3 (Triage Decryption); preserve incoming encrypted payloads in WBS Sealed Vault; emergency key rotation via WBS Council 2-of-3 within 4 hours; resume operations only after DPO + Ethics Officer joint sign-off. |
| **SLA Breach — CRITICAL Case Triage > 4h** | HC-7 SLA exceeded | Auto-escalate to CEO + Board Audit Committee; root cause analysis mandatory; SLA breach logged as KPI deviation. |
| **SLA Breach — External Routing > 48h** | HC-8 SLA exceeded | Auto-escalate to Board Audit Committee; WBS Council quorum review of process gap. |

### 5.2 Recovery & Rollback Protocols

- **Strict Prohibition — Partial Deployment Rollback:** P3 SHALL NOT operate in partial-deployment mode. WBS confidentiality cannot be partially deployed; either fully operational or fully suspended.
- **Mandatory — Emergency Mode Activation:** Upon catastrophic failure, manual WBS intake via Ethics Officer + Internal Audit becomes the sole operational mode; degraded throughput but full compliance preserved.
- **Mandatory — Restoration Tri-Signature:** Post-incident restoration requires concurrent sign-off from WBS Council Chair, CHRO, and Internal Audit Head; no single-actor restoration permitted.

### 5.3 Communication Failure Hierarchy

| Failure Type | Primary Channel | Fallback 1 | Fallback 2 | Final Escalation |
|---|---|---|---|---|
| Reporter Acknowledgment | Encrypted reporter channel | Retry queue (3× over 24h) | Case-ID lookup portal | Q-5 violation alert |
| WBS Council Handoff | Sealed envelope (mTLS) | Retry queue (3× over 7h) | Emergency sealed channel | WBS Council Chair direct + Internal Audit |
| Retaliation Flag Write | HR Sealed Bridge write-only API | Retry queue (3× over 75min) | Manual flag by Ethics Officer | CRITICAL system alert to Ethics Officer + DPO |
| Board Audit Committee Notification | Sealed channel | Direct Board Audit Committee Chair | Internal Audit Head | CEO emergency channel |

### 5.4 Data Subject Rights (DSR) Edge Cases — UU PDP 27/2022

- **IF** reporter requests data access under UU PDP DSR provisions → **THEN** route to DPO + WBS Council; P3 SHALL NOT auto-respond. DSR fulfillment requires WBS Council 2-of-3 authorization and DPO compliance review.
- **IF** implicated party requests data access claiming UU PDP rights → **THEN** reject at P3 boundary; DSR for implicated parties is reserved for post-investigation phase and handled by Ethics Officer + General Counsel, never P3.
- **IF** law enforcement subpoena received → **THEN** route to General Counsel + WBS Council + DPO; P3 SHALL NOT decrypt content. Legal disclosure decisions are tri-authority (WBS Council + DPO + General Counsel) with Board Audit Committee notification.

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill Module ID | SKILL-P3-WBS-TRIAGE |
| Parent Agent | P3 — WBS Triage & Confidentiality Agent |
| Version | v1.0 |
| Status | EXECUTION-READY |
| Owner | Ethics Officer (Primary) + WBS Council (Governance) |
| Classification | INTERNAL — Board Audit Committee, WBS Council, Ethics Officer Only |
| Distribution | Board Audit Committee, WBS Council, Ethics Officer, CHRO (governance only), DPO, Internal Audit |
| Companion Documents | AGENT_P3_WBS_Triage_Confidentiality_Agent.md, WBS Policy Polytron, GCG Code Polytron, ISO 37002 Reference |
| Language | 100% English |
| Fidelity Statement | This skill module retains 100% nuance from the parent agent specification. No goals invented outside Agent P3 defined scope. |

---
**END OF SKILL MODULE — SKILL-P3-WBS-TRIAGE v1.0**
