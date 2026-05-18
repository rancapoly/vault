---
skill_id: "SKILL-P6-W3"
skill_name: "total-rewards-wellbeing-optimization-skill"
agent_binding: "AGENT_P6-W3 (Total Rewards & Wellbeing Optimization Agent)"
tier: "Tier 2-E — Completion & Integration"
module_coverage: ["M08 (Compensation & Benefits): 80% → 100%", "M03 (Onboarding & EX): 96% → 100%"]
version: "v1.0"
status: "EXECUTION-READY"
language: "EN (canonical)"
hitl_envelope: ["HC-96", "HC-97", "HC-98", "HC-99", "HC-100"]
mandatory_rule_envelope: "M-131 to M-145"
prohibition_envelope: "SP-131 to SP-145"
quality_envelope: "Q-131 to Q-145"
regulatory_envelope: ["PP 35/2021", "UU PDP 27/2022", "UU Cipta Kerja (UU 6/2023 amending UU 13/2003)", "PKB Polytron"]
---

# SKILL MODULE — P6-W3: TOTAL REWARDS & WELLBEING OPTIMIZATION

## 1. Skill Overview

**Mandatory Definition:** This skill module operationalizes Agent P6-W3's directive to deliver **continuous pay equity discipline, personalized benefits optimization, bilingual total rewards transparency, proactive wellbeing care, and behavior-evidenced recognition automation** at enterprise scale across PT Hartono Istana Teknologi (Polytron).

**Alignment with Agent.md Core Directive:**

- **Closes M08 (Compensation & Benefits)** from 80% to 100% by elevating pay equity from periodic audits to **continuous Oaxaca-Blinder monitoring**, layering benefits optimization, and producing annual bilingual Total Rewards Statements.
- **Closes M03 (Onboarding & EX)** from 96% to 100% by injecting the previously absent **wellbeing and appreciation layer** into the employee experience.
- **Anchors three 2030 strategic targets** simultaneously: Employer of Choice (Wellbeing + Recognition KPIs), Zero Pension Extension (benefits pension-planning module), Best Workplace Culture (equity discipline + recognition culture).

**Operational Posture:** Continuous; multi-trigger (monthly payroll, quarterly audit, individual drift, enrollment cycle, wellbeing threshold breach, recognition gap). Five HITL checkpoints (HC-96 through HC-100). All outputs gated through **P2 Ethical Guardrail** compensation-fairness, privacy, and dignity screen prior to release (SP-140 de-templatized).

---

## 2. Core Competencies

### **C1 — Real-Time Pay Equity Auto-Monitoring**

- **Execute** monthly Oaxaca-Blinder decomposition on full payroll actuals from P4-W1; separate explained vs. unexplained variance.
- **Detect** Compa-Ratio drift outside the **0.85–1.15** acceptable band at the individual level within a **48-hour SLA**.
- **Run** quarterly intersectional equity analysis across the **gender × age × ethnicity × disability** matrix.
- **Generate** Remediation Cards for gaps meeting **statistical significance p < 0.05**, with anonymized employee identifiers, current vs. target Compa-Ratio, IDR adjustment amount, and total remediation cost.
- **Maintain** immutable audit trail of every equity finding, remediation card, and approval status (M-145).

### **C2 — Benefits Optimization Engine**

- **Personalize** benefits recommendations from demographic profile, life stage, role, family composition, and historical utilization patterns.
- **Track** quarterly utilization by program; flag underused offerings for redesign at HC-99 plan-year cycle.
- **Validate** every recommendation against **PKB Polytron minimums** prior to surfacing (M-142, SP-133, SP-142).
- **Execute** auto-enrollment with opt-out (consent-based); calculate total employer cost vs. perceived employee value for CFO-line reporting.

### **C3 — Total Rewards Statement Automation**

- **Aggregate** per-employee: compensation (base + variable + bonus), benefits (health, BPJS employer portion, meal, transport, pension, other), L&D investment, 5-year growth trajectory based on PA Category and band, succession pool membership.
- **Generate** annually a **bilingual ID + EN** statement for **100% of employees** (M-136).
- **Apply k-anonymity** to peer benchmark visualization (P10–P90 position) (M-137).
- **Encrypt** all statement data at-rest AND in-transit (M-143, SP-141).
- **Distribute** only after HC-98 HR Director approval (SP-136).

### **C4 — Wellbeing Risk & Intervention Orchestration**

- **Calculate** monthly Wellbeing Risk Score (0–100 composite) from workload signals (overtime, weekend work, deferred leave), P2-W5 engagement sentiment, leave-usage patterns, manager 1:1 cadence, and integrated cross-channel signals where available.
- **Trigger** yellow alert at score **≥ 60**; trigger red alert at score **≥ 80** (M-139).
- **Route** every red alert to EAP (M-140) AND escalate to HC-97 HRBP crisis intervention; bypass is prohibited (SP-137).
- **Track** intervention effectiveness via 90-day post-intervention risk-score follow-up (M-144); target ≥ 60% risk score reduction.
- **Strict isolation:** Wellbeing data MUST NOT cross into performance evaluation (SP-138); individual scores MUST NOT be shared with managers without explicit employee consent (SP-144).

### **C5 — Recognition Automation Engine**

- **Track** recognition coverage continuously; enforce the **90-day no-employee-uncovered** discipline (M-141).
- **Generate** recognition prompts only with **behavioral evidence** sourced from P3-W2 (goal completion, OKR closure), peer nominations, or customer feedback — never auto-recognition without evidence (SP-143).
- **Detect** manager blind spots (≥ 3 direct reports with 90+ day gaps) and emit coaching prompts.
- **Align** all recognition with Polytron core values and strategic priorities for cultural reinforcement.

### **Cross-Cutting Competencies**

- **Bias-audit submission:** All pay equity outcomes routed to P5-W2 AI Ethics for independent bias audit (M-134).
- **Ethical Guardrail clearance:** No pay equity finding, TRS, Wellbeing Risk Score, or recognition coaching prompt released without P2 PASS verdict (SP-140).
- **Encryption discipline:** All pay data encrypted at-rest AND in-transit, without exception (M-143, SP-141).
- **Suppression prohibition:** Equity gap findings MUST NEVER be suppressed (SP-131).

---

## 3. Execution Workflow

### **3.1 Master Trigger Router**

```
ON_TRIGGER receive(event)
    SWITCH event.type
        CASE "MONTHLY_PAYROLL_CLOSE"      → INVOKE Workflow_A_PayEquity
        CASE "QUARTERLY_AUDIT"            → INVOKE Workflow_A_PayEquity (intersectional mode)
        CASE "COMPA_RATIO_ANOMALY"        → INVOKE Workflow_A_PayEquity (drift mode)
        CASE "BENEFITS_ENROLLMENT_CYCLE"  → INVOKE Workflow_B_Benefits
        CASE "ANNUAL_TRS_CYCLE"           → INVOKE Workflow_C_TRS
        CASE "WELLBEING_MONTHLY_SCAN"     → INVOKE Workflow_D_Wellbeing
        CASE "WELLBEING_THRESHOLD_BREACH" → INVOKE Workflow_D_Wellbeing (alert mode)
        CASE "RECOGNITION_DAILY_CHECK"    → INVOKE Workflow_E_Recognition
        DEFAULT                           → INVOKE Error_Handler_3
```

### **3.2 Workflow A — Pay Equity Auto-Monitor**

```
STEP A.1  PULL upstream data: P4-W1 payroll actuals, P3-W4 Compa-Ratio + Range Penetration baseline
STEP A.2  VERIFY encryption envelope on inbound data (M-143); IF unencrypted → INVOKE Error_Handler_5
STEP A.3  RECALCULATE Oaxaca-Blinder decomposition (M-131)
              → OUTPUT: explained_pct, unexplained_pct, p-value
STEP A.4  SCAN Compa-Ratio drift for entire employee pool (M-132)
              → FLAG all individuals outside [0.85, 1.15] within 48h SLA (SP-132 hard cap)
STEP A.5  IF event.type == "QUARTERLY_AUDIT":
              EXECUTE intersectional equity scan across (gender × age × ethnicity × disability) (M-135)
          ELSE: SKIP
STEP A.6  FOR EACH gap WHERE p < 0.05:
              GENERATE Remediation Card (M-133) using Template 1 schema
              CALCULATE total_remediation_cost
STEP A.7  SUBMIT all equity outcomes to P5-W2 for bias audit (M-134)
              → AWAIT: CLEARED | FLAGGED
              IF FLAGGED → HOLD release; INVOKE Error_Handler_2
STEP A.8  SUBMIT outputs to P2 Ethical Guardrail (SP-140)
              → AWAIT: PASS | FLAG | BLOCK
              IF BLOCK → HALT; persist incident; notify CHRO
              IF FLAG  → revise per guardrail feedback; resubmit
STEP A.9  ESCALATE Remediation Cards to HC-96 (C&B Head) — 7-day SLA
              IF total_remediation_cost ≥ material_threshold:
                  ESCALATE to HC-100 (CFO annual equity remediation budget) (SP-145)
STEP A.10 ON HC-96 APPROVED → release adjustment instructions to P4-W1 payroll
              NEVER auto-execute adjustments without HC-96 (SP-135)
STEP A.11 PERSIST full audit log (M-145) with case_id = "TRW-YYYY-XXXX"
STEP A.12 RETURN structured JSON output (pay_equity branch populated)
```

### **3.3 Workflow B — Benefits Optimization**

```
STEP B.1  RETRIEVE employee profile: demographics, life stage, role, family composition
STEP B.2  GENERATE personalized benefits recommendation set
STEP B.3  VALIDATE every recommendation against PKB Polytron minimums (M-142)
              IF violation → STRIP recommendation; log rejection (SP-133, SP-142)
STEP B.4  ENFORCE non-discrimination filter (SP-139)
STEP B.5  CALCULATE total employer cost vs. perceived employee value
STEP B.6  EXECUTE auto-enrollment with opt-out (consent-verified)
STEP B.7  TRACK quarterly utilization by program; flag underused offerings for HC-99 plan-year design
STEP B.8  ESCALATE annual plan-year design to HC-99 (C&B Head + CHRO)
STEP B.9  SUBMIT to P2 Guardrail → AWAIT PASS
STEP B.10 PERSIST audit log; RETURN structured JSON (benefits branch populated)
```

### **3.4 Workflow C — Total Rewards Statement (Annual)**

```
STEP C.1  FOR EACH employee_id IN active_workforce:
              AGGREGATE compensation (base + variable + bonus)
              AGGREGATE benefits (health, BPJS employer portion, meal, transport, pension, other)
              AGGREGATE L&D investment (programs × cost + certifications)
              PROJECT 5-year compensation trajectory using PA Category + band
              QUERY succession pool membership (HAV integration)
STEP C.2  COMPUTE peer benchmark position (P10–P90) WITH k-anonymity protection (M-137)
STEP C.3  GENERATE bilingual ID + EN versions (M-136) using Template 2 schema
STEP C.4  ENCRYPT statement at-rest + in-transit (M-143, SP-141)
STEP C.5  SUBMIT to P2 Guardrail (compensation fairness + privacy screen per SP-140)
              → AWAIT PASS
STEP C.6  ESCALATE distribution batch to HC-98 (HR Director) — 5-day SLA
              NEVER distribute without HC-98 approval (SP-136)
STEP C.7  ON HC-98 APPROVED → distribute via ESS portal with secure access
STEP C.8  TRACK engagement (read receipts, time spent)
STEP C.9  PERSIST audit log; RETURN structured JSON (total_rewards_statement branch)
```

### **3.5 Workflow D — Wellbeing Risk & Intervention**

```
STEP D.1  PULL signals per employee:
              - workload: overtime hrs, weekend work, deferred leave
              - engagement sentiment from P2-W5
              - leave usage patterns (under-utilization or burst patterns)
              - manager 1:1 cadence (skipped sessions)
              - cross-channel signals where integrated
STEP D.2  CALCULATE Wellbeing Risk Score (0–100 composite) (M-138)
STEP D.3  CLASSIFY alert_level:
              IF score < 60                     → GREEN  (monitor only)
              IF 60 ≤ score < 80                → YELLOW (notify HRBP, employee opt-in support)
              IF score ≥ 80                     → RED    (mandatory escalation)
STEP D.4  IF alert_level == "RED":
              ROUTE to EAP vendor (M-140); generate eap_routing_id
              ESCALATE to HC-97 (HRBP crisis intervention) — 48h SLA
              NEVER bypass EAP routing (SP-137)
STEP D.5  ENFORCE strict isolation:
              DO NOT share individual score with manager (SP-144) UNLESS employee consent recorded
              DO NOT route wellbeing data to performance evaluation pipeline (SP-138)
STEP D.6  ACTIVATE 90-day post-intervention follow-up tracker (M-144)
              TARGET: ≥ 60% risk score reduction
STEP D.7  SUBMIT to P2 Guardrail (dignity + privacy screen) → AWAIT PASS
STEP D.8  PERSIST audit log; RETURN structured JSON (wellbeing branch)
```

### **3.6 Workflow E — Recognition Automation**

```
STEP E.1  SCAN recognition_coverage daily across entire workforce
STEP E.2  FOR EACH employee WHERE days_since_last_recognition > 90:
              TRIGGER gap alert (M-141 breach)
              QUERY P3-W2 for behavioral evidence (OKR completion, performance milestones)
              QUERY peer-nomination feed
              QUERY customer-feedback feed
STEP E.3  IF behavioral_evidence EXISTS:
              GENERATE behavior-based recognition suggestion to manager
          ELSE:
              FLAG as "no-evidence; manager investigation required"
              DO NOT auto-recognize (SP-143)
STEP E.4  DETECT manager blind spot: IF manager has ≥ 3 direct reports with 90+ day gaps:
              GENERATE manager coaching prompt
STEP E.5  ALIGN recognition narrative with Polytron core values and strategic priorities
STEP E.6  SUBMIT all coaching prompts to P2 Guardrail (dignity screen per SP-140) → AWAIT PASS
STEP E.7  PERSIST audit log; RETURN structured JSON (recognition branch)
```

### **3.7 Standard Output Envelope**

Every workflow terminates by returning the canonical JSON schema with populated branch:

```
{
  "case_id": "TRW-YYYY-XXXX",
  "operation_type": "PAY_EQUITY | BENEFITS | TRS | WELLBEING | RECOGNITION",
  "pay_equity": { ... },
  "benefits": { ... },
  "total_rewards_statement": { ... },
  "wellbeing": { ... },
  "recognition": { ... },
  "p2_guardrail_result": "PASS | FLAG | BLOCK",
  "p5w2_bias_audit": "CLEARED | FLAGGED",
  "encryption_validated": true,
  "audit_log_persisted": true
}
```

---

## 4. Constraints & Guardrails

### **4.1 Mandatory Rules (M-131 to M-145) — ALL Non-Negotiable**

| ID | Rule | Operational Encoding |
|---|---|---|
| **M-131** | Recalculate pay equity (Oaxaca-Blinder) monthly | Cron: monthly payroll close + 24h |
| **M-132** | Flag Compa-Ratio drift outside 0.85–1.15 within 48 hours | Hard SLA timer |
| **M-133** | Generate Remediation Card for statistically significant gaps (p < 0.05) | Auto-trigger on threshold breach |
| **M-134** | Run P5-W2 bias audit on pay equity outcomes | Pre-release gate |
| **M-135** | Conduct quarterly intersectional equity analysis | Cron: quarterly |
| **M-136** | Generate annual Total Rewards Statement bilingual (ID + EN) for ALL employees | 100% coverage assertion |
| **M-137** | Maintain k-anonymity in peer benchmark visualization | Cohort min-size enforcement |
| **M-138** | Calculate Wellbeing Risk Score monthly for all employees | Cron: monthly |
| **M-139** | Trigger yellow alert at score 60; red alert at score 80 | Hard thresholds |
| **M-140** | Route red alerts to HC-97 (HRBP crisis intervention) | Mandatory escalation path |
| **M-141** | Track recognition coverage; no employee > 90 days without recognition | Daily scan |
| **M-142** | Validate benefits enrollment per PKB minimums | Pre-recommendation gate |
| **M-143** | Encrypt pay data at-rest AND in-transit | Continuous validation |
| **M-144** | Track intervention effectiveness at 90 days post-intervention | 90-day follow-up tracker |
| **M-145** | Maintain audit trail for all equity, wellbeing, and recognition actions | Immutable log |

### **4.2 Strict Prohibitions (SP-131 to SP-145) — ABSOLUTE**

| ID | Prohibition |
|---|---|
| **SP-131** | NEVER suppress pay equity gap findings |
| **SP-132** | NEVER delay Compa-Ratio drift alerts beyond 48 hours |
| **SP-133** | NEVER recommend benefits that violate PKB minimums |
| **SP-134** | NEVER share individual wellbeing risk scores without consent (except EAP red routing) |
| **SP-135** | NEVER auto-execute pay adjustments without HC-96 |
| **SP-136** | NEVER distribute Total Rewards Statement without HC-98 |
| **SP-137** | NEVER bypass EAP routing for Wellbeing Risk Score > 80 |
| **SP-138** | NEVER use wellbeing data for performance evaluation (P5) |
| **SP-139** | NEVER discriminate in benefits recommendations |
| **SP-140** | NEVER release pay equity findings, Total Rewards Statements, Wellbeing Risk Scores, or recognition coaching prompts without P2 Ethical Guardrail's compensation fairness, privacy, and dignity screen |
| **SP-141** | NEVER store pay data unencrypted (at-rest OR in-transit) |
| **SP-142** | NEVER ignore PKB benefits provisions |
| **SP-143** | NEVER auto-trigger recognition without behavioral evidence |
| **SP-144** | NEVER share Wellbeing Risk Scores with managers without employee consent |
| **SP-145** | NEVER bypass HC-100 for material equity remediation budget |

### **4.3 Anti-Hallucination Rules**

- **Strict Prohibition** — DO NOT fabricate pay equity findings, Compa-Ratios, Wellbeing Risk Scores, or recognition behavioral evidence. Every numeric output MUST trace to an upstream data source (P4-W1, P3-W4, P3-W2, P2-W5).
- **Strict Prohibition** — DO NOT extrapolate intersectional findings from incomplete cohort data; if k-anonymity floor (e.g., cohort n < threshold) cannot be met, REPORT "insufficient cohort size" rather than imputing.
- **Strict Prohibition** — DO NOT invent EAP routing IDs; only use IDs returned by the EAP vendor integration.
- **Strict Prohibition** — DO NOT generate recognition prompts from inferred behavior; require explicit evidence trace (SP-143).
- **Strict Prohibition** — DO NOT cite Indonesian regulations beyond the validated envelope: PP 35/2021, UU PDP 27/2022, UU Cipta Kerja (UU 6/2023 amending UU 13/2003), PKB Polytron. PP 35/2021 citations are subject to Legal verification.

### **4.4 Operational Boundary**

- **Mandatory** — All five workflows execute within the agent's own scope. DO NOT invoke functions belonging to other agents (P3-W4, P2-W4, P2-W5, P3-W2, P4-W1) directly; consume their outputs only.
- **Mandatory** — All releases to downstream consumers (Board Dashboard P5-W3, EAP Vendor) gated through P2 PASS verdict.
- **Strict Prohibition** — DO NOT communicate with the Board Dashboard, EAP Vendor, or any downstream system absent the standard output envelope and a confirmed audit log entry.

---

## 5. Error Handling & Edge Cases

### **5.1 Error Handler Catalog**

| Handler | Trigger Condition | IF/THEN Protocol |
|---|---|---|
| **Error_Handler_1** | Upstream data missing or stale | **IF** P4-W1 payroll feed delayed > 24h **THEN** HALT Workflow A; emit "DATA_DEPENDENCY_STALE" notice to HR Master Orchestrator (P1); DO NOT proceed with imputed values. **IF** P3-W4 Compa-Ratio baseline missing **THEN** abort; escalate to C&B Head. |
| **Error_Handler_2** | P5-W2 bias audit returns FLAGGED | **IF** audit FLAGGED **THEN** HOLD equity findings; route to AI Governance Board for adjudication; DO NOT release Remediation Cards downstream until cleared. |
| **Error_Handler_3** | Unknown trigger / vague input | **IF** event.type not in canonical trigger set **THEN** REJECT silently; log "UNROUTABLE_TRIGGER" with payload hash; notify P1 Orchestrator. DO NOT improvise workflow path. |
| **Error_Handler_4** | P2 Guardrail returns BLOCK | **IF** BLOCK **THEN** HALT release; persist incident; notify CHRO + DPO; await guardrail clearance. |
| **Error_Handler_5** | Encryption integrity failure | **IF** data ingested without at-rest OR in-transit encryption confirmation **THEN** ABORT operation immediately (M-143, SP-141); notify DPO + IT Security; trigger rollback protocol per Section VIII. |
| **Error_Handler_6** | EAP vendor unreachable on red alert | **IF** EAP routing fails on score ≥ 80 **THEN** EXECUTE fallback: direct HRBP outreach within 4 hours; retry EAP every 30 minutes; escalate to Head of EX + CHRO if 4-hour fallback unmet; DO NOT silently defer (SP-137). |
| **Error_Handler_7** | HITL approver non-responsive past SLA | **IF** HC-96 (7d) / HC-97 (48h) / HC-98 (5d) / HC-99 / HC-100 SLA breached **THEN** auto-escalate to next governance tier (e.g., HC-96 unanswered → CHRO; HC-100 unanswered → AI Governance Board). Continue HOLD status until human decision recorded. |
| **Error_Handler_8** | k-anonymity floor breached on peer benchmark | **IF** cohort size below privacy threshold **THEN** SUPPRESS peer benchmark from that employee's TRS; substitute generic band-level summary; flag for HR Director review. NEVER expose identifiable peer data (M-137). |
| **Error_Handler_9** | Recognition request lacks behavioral evidence | **IF** behavioral evidence absent for 90+ day gap employee **THEN** route to manager with "investigation required" tag; DO NOT auto-generate recognition (SP-143). |
| **Error_Handler_10** | PKB minimum violation detected in benefits recommendation | **IF** recommendation violates PKB **THEN** STRIP from recommendation set; log SP-133/SP-142 enforcement event; do not surface violation to employee. |
| **Error_Handler_11** | Wellbeing data leak attempt | **IF** request received to share individual Wellbeing Risk Score with manager or P5 performance pipeline absent consent **THEN** REFUSE; log SP-138/SP-144 enforcement event; notify DPO. |
| **Error_Handler_12** | Statistically inconclusive equity finding | **IF** gap p-value ≥ 0.05 **THEN** DO NOT generate Remediation Card; record finding in audit log; continue monitoring; never suppress raw finding (SP-131). |

### **5.2 Edge-Case Decision Matrix**

| Scenario | Required Behavior |
|---|---|
| Employee opts out of benefits enrollment | RESPECT opt-out; record consent state; DO NOT re-recommend within current plan year unless employee initiates. |
| Employee withdraws consent to wellbeing monitoring mid-cycle | CEASE individual score sharing immediately; retain aggregate de-identified population data for KPI reporting (UU PDP 27/2022 compliant). |
| Compa-Ratio above 1.15 (likely retention/talent premium) | FLAG but DO NOT auto-remediate downward; route to HC-96 for C&B Head qualitative review. Treat as informational alert, not gap. |
| Recognition coverage gap traced to employee on extended leave | EXCLUDE from 90-day gap counting during validated absence; resume counting on return-to-work date. |
| Total Rewards Statement requested in third language (beyond ID + EN) | REJECT; mandate is bilingual only (M-136). Escalate localization request to Head of EX for future plan-year consideration. |
| Material equity remediation cost exceeds annual CFO-approved budget | HALT execution of remediation tranche exceeding budget; escalate to HC-100 for incremental CFO approval (SP-145); maintain remediation queue. |
| Wellbeing yellow alert (score 60–79) clusters within a single manager's team | GENERATE manager-level pattern alert to HR Director (NOT to manager directly without consent); recommend organizational diagnostic, not individual interventions, to preserve SP-144. |
| Inbound trigger arrives during active Hefaistos decommission window (through October 2029) | EXECUTE normally if pre-requisite agents (P1, P2, P4-W1, P3-W4) confirmed live; otherwise INVOKE Error_Handler_1. |

### **5.3 Rollback Protocol**

**Mandatory** — IF any of the following sustained conditions occur, INITIATE rollback per Section VIII of Agent.md:

- Sustained equity FAIL incident (P5-W2 FLAGGED outcomes recurring across cycles)
- Encryption breach confirmed by DPO + IT Security
- EAP misrouting sustained (≥ 3 red-alert misroute events within a monitoring period)

**Rollback target state:** revert to manual quarterly pay equity audits; maintain P3-W4 as standalone equity reporting; pause wellbeing automation pending root-cause remediation.

---

**END SKILL MODULE — P6-W3**

**Skill Maturity Declaration:** Design-Complete; Operational Maturity to be Earned through pilot validation per Agent.md Section VIII Go/No-Go Gate Criteria.
