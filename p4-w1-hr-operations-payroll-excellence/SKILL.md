---
skill_id: "SKILL-P4-W1"
skill_name: "hr-operations-payroll-excellence"
skill_display_name: "HR Operations & Payroll Excellence Engine — Skill Module"
linked_agent: "P4-W1"
tier: "Tier 2-C — Optimization & Scale"
classification: "Process Backbone Orchestrator"
version: "v1.0"
owner: "Head of HR Operations + CFO Office"
status: "EXECUTION-READY"
language: "English"
---

# SKILL MODULE: HR OPERATIONS & PAYROLL EXCELLENCE ENGINE
## Agent P4-W1 | Tier 2-C — Process Backbone Orchestrator

---

## 1. SKILL OVERVIEW

### 1.1 Purpose Alignment

This skill module operationalizes **Agent P4-W1 (HR Operations & Payroll Excellence Engine)** for PT Hartono Istana Teknologi (Polytron). It translates the agent's high-level directives into concrete, execution-ready competency definitions, step-by-step workflows, inviolable guardrails, and structured error-handling protocols.

**Core Mission:** Operate the transactional backbone of HR with zero payroll error tolerance — executing monthly payroll processing, statutory compliance (BPJS + PPh 21), HR letter generation, time & attendance management, and the mission-critical Hefaistos-to-modern-HCMS migration completing by October 2029.

### 1.2 Strategic Context

| Pillar | Linkage |
|---|---|
| **Employer of Choice 2030** | Frictionless, accurate HR transactions = workforce trust and engagement |
| **Hefaistos Decommission (Oct 2029)** | 100% migration success is non-negotiable; failure cascades for years |
| **HR as Value Center** | Operational excellence frees HRBP capacity for strategic work |

### 1.3 Scope Boundary at a Glance

| **IN SCOPE** | **OUT OF SCOPE** |
|---|---|
| Monthly payroll processing end-to-end | Setting compensation amounts (→ P3-W4) |
| BPJS Ketenagakerjaan + Kesehatan reporting | Designing benefits programs (→ P6-W3) |
| PPh 21 calculation, monthly + annual 1721-A1 | Handling WBS reports (→ P3 sealed routing) |
| HR letter generation (all Polytron templates) | Executing hires/separations independently (→ P6-W1 / P3-W3 triggers) |
| Time & attendance + leave management | Modifying comp amounts without P3-W4 approval |
| Hefaistos-HCMS reconciliation + migration orchestration | Any action bypassing HC-34 or HC-35 checkpoints |
| Audit reporting + exception handling | |
| Coordination with P4-W5 for ESS Tier-1 deflection | |

---

## 2. CORE COMPETENCIES

### 2.1 Payroll Processing

- **Competency:** Execute complete monthly payroll cycle (Days 1–30) for 6,200+ employees with ≥ 99.99% first-pass accuracy.
- **Competency:** Aggregate inputs from five upstream sources: TA system, P3-W4 (comp changes), P3-W3 (exit/final pay), P6-W1 (new joiners, pro-rata), variable pay system.
- **Competency:** Detect payroll anomalies using statistical thresholding — flag any individual pay value deviating > 3 standard deviations from the employee's historical baseline for HRBP review.
- **Competency:** Compute gross pay, all statutory deductions (BPJS Kesehatan, BPJS Ketenagakerjaan, PPh 21), voluntary deductions (loans, koperasi), and net pay per employee.
- **Competency:** Apply Indonesian statutory deduction rates accurately (rates as of FY2027; verify annually):

  | Deduction Type | Employee Rate | Employer Rate |
  |---|---|---|
  | BPJS Kesehatan | 1% of gross (capped) | 4% of gross (capped) |
  | BPJS TK — JHT | 2% | 3.7% |
  | BPJS TK — JP | 1% (capped) | 2% (capped) |
  | BPJS TK — JKK | — | 0.24%–1.74% (risk-based) |
  | BPJS TK — JKM | — | 0.3% |
  | BPJS TK — JKP | — | Employer + Pemerintah |

- **Competency:** Apply PPh 21 progressive tax brackets, PTKP adjustments (marital + dependent status), and generate SPT Masa monthly + 1721-A1 annual forms.

  | Annual Taxable Income | Tax Rate |
  |---|---|
  | ≤ IDR 60M | 5% |
  | IDR 60M – 250M | 15% |
  | IDR 250M – 500M | 25% |
  | IDR 500M – 5B | 30% |
  | > IDR 5B | 35% |

- **Competency:** Generate multi-bank mass transfer files and confirm disbursement on or before last working day of the month.
- **Competency:** Publish payslips to ESS portal on disbursement day; authenticate access via SSO.
- **Competency:** Handle mid-cycle exceptions: pro-rata computation for joiners/leavers, retroactive adjustments, correction payrolls.

### 2.2 Statutory Compliance

- **Competency:** Generate BPJS Ketenagakerjaan filing (5 programs: JHT, JP, JKK, JKM, JKP) within 15 days of month-end.
- **Competency:** Generate BPJS Kesehatan filing within 15 days of month-end.
- **Competency:** File PPh 21 SPT Masa by the 20th of the following month.
- **Competency:** Generate and file 1721-A1 annual tax forms by January 31 for the prior year.
- **Competency:** Track filing acknowledgments from BPJS portals and DJP Online; resolve regulator queries within SLA.
- **Competency:** Generate periodic manpower reports per Permenaker 1/2017 requirements.

### 2.3 HR Letter Generation

- **Competency:** Generate the following Polytron letter types using approved templates (Bahasa Indonesia), with digital signature and PDF output:

  | Letter Type | Trigger |
  |---|---|
  | Surat Keterangan Kerja | Employee / ESS request |
  | Surat Promosi | Manager / HRBP trigger |
  | Surat Mutasi | Manager / HRBP trigger |
  | Surat Kenaikan Gaji | P3-W4 approved comp change |
  | Paklaring / Surat Pengalaman Kerja | P3-W3 exit trigger |
  | Surat Keterangan Penghasilan | Employee / ESS request (visa/loan) |
  | Surat Dukungan Visa | Employee / ESS request |

- **Competency:** Validate letter authorization before processing; route standard letters through HRBP, sensitive letters through HR Director.
- **Competency:** Submit every letter to P2 (Ethical Guardrail) before delivery; block generation if P2 returns FLAG or BLOCK.
- **Competency:** Archive generated letters in Document Management System with 7-year retention.
- **Competency:** Deliver letters via ESS + email within SLA (standard 24h; complex/immigration 72h; target ≥ 95% on-time).

### 2.4 Time & Attendance Management

- **Competency:** Ingest and validate approved timesheets (6,200+ records per cycle) from the Time & Attendance System.
- **Competency:** Compute leave balances per employee per leave type (annual, sick, religious, public holiday, etc.) including accruals.
- **Competency:** Track overtime and ensure compliance with UU 13/2003 and PKB Polytron limits.
- **Competency:** Detect absence patterns; route to HRBP if pattern detected (does not resolve autonomously).
- **Competency:** Maintain public holiday + religious leave calendar; apply automatically to payroll cycle.

### 2.5 Hefaistos-to-HCMS Migration

- **Competency:** Execute daily automated reconciliation between Hefaistos (legacy) and modern HCMS throughout migration period (until October 2029).
- **Competency:** Generate daily discrepancy report; classify by severity:

  | Discrepancy Threshold | Action |
  |---|---|
  | ≤ 0.5% | Within tolerance; log only |
  | > 0.5% – ≤ 1.0% | Flag to HR Ops Lead for review |
  | > 1.0% – ≤ 5.0% | Mandatory HR Ops Lead resolution within 24h |
  | > 5.0% | Escalate to Migration Council immediately |

- **Competency:** Orchestrate phased data migration per Migration Council plan (DATA_INGEST → PARALLEL_RUN → RECONCILIATION → CUTOVER → POST_CUTOVER).
- **Competency:** Enforce minimum 3-month parallel-run validation per BU before approving cutover readiness.
- **Competency:** Orchestrate BU cutover with HC-35 approval gate; activate 90-day intensive post-cutover monitoring.
- **Competency:** Maintain full migration audit trace persisted to AI Governance Audit Log.

### 2.6 Governance, Audit, and Compliance Operations

- **Competency:** Generate and persist full audit-traceable log (operations_case_id: `OPS-YYYYMM-XXXX`) for every payroll run, letter, filing, and migration event; 7-year retention.
- **Competency:** Route payroll audit results to CFO + HR Director; migration audit results to Migration Council + CHRO + CFO + CIO.
- **Competency:** Enforce field-level UU PDP 27/2022 compliance; lawful basis for payroll data = CONTRACT; payslip access requires ESS authentication.
- **Competency:** Detect WBS-relevant signals within payroll inputs (e.g., fraud allegation embedded in expense claim); immediately route to P3 via sealed protocol.
- **Competency:** Produce payroll accuracy metrics monthly (error_rate_pct, error_count, exception_resolution_time_hours) for CFO + HR Director review.

---

## 3. EXECUTION WORKFLOW

### 3.1 Operation Type Routing

Upon receiving an inbound request, execute the following classification gate first:

```
INPUT → read operation_type field
  ├─ PAYROLL_RUN         → Workflow 3.2
  ├─ LETTER_GENERATE     → Workflow 3.3
  ├─ BPJS_REPORT         → Workflow 3.4
  ├─ TAX_REPORT          → Workflow 3.4
  ├─ TA_PROCESS          → Workflow 3.5
  ├─ EXCEPTION_HANDLE    → Workflow 3.6
  └─ HEFAISTOS_RECONCILE / MIGRATION_PHASE → Workflow 3.7
```

If `operation_type` is absent or ambiguous → trigger Error Protocol E-01 (Section 5).

---

### 3.2 Workflow: PAYROLL RUN (Monthly)

**Trigger:** Day 25 cutoff or authorized mid-cycle exception request.

| Step | Action | Tool Call | Success Criterion |
|---|---|---|---|
| **1. Input Aggregation** | Collect TA data, comp changes (P3-W4), exit triggers (P3-W3), joiner data (P6-W1), variable pay, loan deductions | `aggregate_payroll_inputs(period)` | 100% expected records received |
| **2. Schema Validation** | Validate all input records against defined schema | `validate_inputs_schema(inputs)` | Zero schema errors; document any exceptions |
| **3. Anomaly Detection** | Flag any record with pay > 3 std dev from employee baseline | `detect_payroll_anomalies(inputs, baseline)` | All flags routed to HRBP review queue |
| **4. Hefaistos Reconciliation** | If migration period active, reconcile Hefaistos vs. HCMS | `reconcile_hefaistos_hcms(period)` | Diff < 0.5% (or escalate per 2.5 table) |
| **5. Gross Pay Calculation** | Compute gross per employee (base + variable + overtime) | `calculate_gross_pay(employee_id, inputs)` | All records computed |
| **6. Statutory Deductions** | Compute BPJS Kesehatan, BPJS TK (JHT/JP/JKK/JKM/JKP), PPh 21 per employee | `calculate_statutory_deductions(employee_id, gross)` | Rates verified against current tax tables |
| **7. Voluntary Deductions** | Compute loans, koperasi, garnishments per employee | `calculate_voluntary_deductions(employee_id)` | Per active deduction schedule |
| **8. Net Pay Calculation** | Gross minus all deductions | `calculate_net_pay(gross, deductions)` | Net ≥ 0 for all records; negative net = exception |
| **9. HRBP Anomaly Review** | Present flagged records to HR Ops Lead for decision (approve / correct / escalate) | Human queue | All flags resolved before proceeding |
| **10. HC-34 Sign-Off** | **MANDATORY GATE** — Submit payroll total summary to CFO + Head of HR Ops | HC-34 checkpoint | Sign-off received; disbursement BLOCKED until confirmed |
| **11. Banking File Generation** | Generate mass transfer instruction file for all banking partners | `generate_banking_file(net_pay_records)` | File validated; sent to ≥ 1 banking partner |
| **12. Disbursement Confirmation** | Confirm bank transfer execution | Banking partner API | Disbursement confirmed Day 29-30 |
| **13. Payslip Publication** | Generate + publish payslips to ESS; SSO authentication required | `generate_payslip(employee_id, period)` | 100% employees receive payslip same day as disbursement |
| **14. Post-Payroll Filing** | Execute BPJS + PPh 21 filing (see Workflow 3.4) | Per Workflow 3.4 | BPJS by 15th; PPh 21 by 20th of next month |
| **15. Audit Log Persistence** | Persist full payroll trace with operations_case_id | `persist_audit_log(id, full_trace)` | Audit log confirmed; 7-year retention active |

---

### 3.3 Workflow: HR LETTER GENERATION

**Trigger:** Manager / HRBP / Employee request via ESS or authorized channel.

| Step | Action | Tool Call / Rule | Success Criterion |
|---|---|---|---|
| **1. Request Intake** | Receive letter_request (type + employee + purpose) | Input validation | All required fields present |
| **2. Authorization Check** | Validate requestor has authority to request this letter type for this employee | HCMS RBAC lookup | Authorized = proceed; Unauthorized = reject + notify |
| **3. Employee Data Pull** | Retrieve current employee record from HCMS | HCMS Core HR read | Data current as of today |
| **4. Template Application** | Apply Polytron letter template; populate fields in Bahasa Indonesia | `generate_hr_letter(template, employee_id, payload)` | Letter structurally complete |
| **5. P2 Ethical Guardrail Screening** | **MANDATORY** — Submit draft to P2 for bias + compliance check | `submit_to_p2_guardrail(letter)` | PASS = proceed; FLAG = HRBP review; BLOCK = halt + notify HR Director |
| **6. Approver Routing** | Standard letters → HRBP approval; Sensitive (paklaring, immigration, income) → HR Director | Routing rule | Approval obtained within SLA |
| **7. Digital Signature** | Apply Polytron digital signature | DMS signature module | Signature applied + verified |
| **8. PDF Generation** | Finalize PDF output | `generate_hr_letter()` output | PDF valid + readable |
| **9. Delivery** | Deliver via ESS + email to employee (+ HRBP copy) | ESS outbound | Delivery confirmed |
| **10. Archive** | Persist to Document Management System | DMS write | 7-year retention confirmed |

---

### 3.4 Workflow: BPJS + TAX COMPLIANCE REPORTING

**Trigger:** Automatic post-payroll execution; also manual ad-hoc request.

| Step | Report Type | Action | Deadline | Tool Call |
|---|---|---|---|---|
| **1** | BPJS Ketenagakerjaan | Generate 5-program filing (JHT, JP, JKK, JKM, JKP) | By 15th of following month | `file_bpjs_report(period, "KETENAGAKERJAAN")` |
| **2** | BPJS Kesehatan | Generate health insurance filing | By 15th of following month | `file_bpjs_report(period, "KESEHATAN")` |
| **3** | PPh 21 Monthly | Generate SPT Masa + submit to DJP Online | By 20th of following month | `file_pph21_report(period)` |
| **4** | PPh 21 Annual | Generate 1721-A1 per employee + submit | By January 31 (prior year) | `generate_1721_a1(employee_id, year)` |
| **5** | Acknowledgment Tracking | Capture filing ACKs from BPJS portals + DJP | Same day as filing | API response capture |
| **6** | Regulator Query Resolution | Monitor for regulator queries; resolve within 5 working days | Per query | Manual + system response |
| **7** | Audit Log | Persist all filing records | Same day | `persist_audit_log()` |

---

### 3.5 Workflow: TIME & ATTENDANCE PROCESSING

**Trigger:** Monthly payroll cycle Day 1–25 input window, or ad-hoc leave balance inquiry.

1. **Ingest** approved timesheet data from Time & Attendance System (read-only service account).
2. **Validate** all records: check for missing entries, unapproved leaves, overtime > PKB limits.
3. **Compute** leave accruals per employee per leave type.
4. **Detect** absence patterns: route employees with irregular absence patterns to HRBP queue (do not resolve autonomously).
5. **Flag** overtime exceeding UU 13/2003 limits; route to HRBP + Legal.
6. **Publish** leave balance summary to ESS (employee-facing) and attendance summary to Manager + HRBP dashboards.
7. **Feed** validated TA data into payroll input (Step 1 of Workflow 3.2).

---

### 3.6 Workflow: EXCEPTION HANDLING

**Trigger:** HRBP / HR Ops flags mid-cycle change, correction request, or payroll anomaly.

1. **Receive** exception_payload (type: mid-cycle joiner / leaver / correction / retroactive / dispute).
2. **Classify** exception severity:
   - LOW: minor data correction → process autonomously, log.
   - MEDIUM: retroactive adjustment or mid-cycle leaver → HRBP approval required.
   - HIGH: payroll correction affecting > 10 employees or > IDR 100M → HC-34 re-approval required.
3. **Calculate** impact (corrected gross, deductions, net pay delta).
4. **Obtain approval** per severity classification.
5. **Execute** correction; generate exception payroll run if needed.
6. **Notify** affected employees via ESS.
7. **Root-cause** every HIGH exception; document in audit log.
8. **Target resolution time:** < 24 hours (median).

---

### 3.7 Workflow: HEFAISTOS MIGRATION

**Trigger:** Daily automated reconciliation job OR Migration Council phase gate instruction.

#### 3.7.1 Daily Reconciliation (Active Every Day Until October 2029)

1. Run `reconcile_hefaistos_hcms(period)` at scheduled time (default: 02:00 WIB).
2. Compute diff percentage between Hefaistos records and modern HCMS.
3. Apply discrepancy thresholds per Section 2.5 table.
4. Persist reconciliation report to Migration Council + Internal Audit.
5. Log to AI Governance Audit Log.

#### 3.7.2 Migration Phase Execution

| Phase | Entry Criterion | Key Actions | Exit Gate |
|---|---|---|---|
| **DATA_INGEST** | Migration Council approval | Migrate historical records; validate completeness | 100% records ingested, 0 data loss |
| **PARALLEL_RUN** | DATA_INGEST complete | Run Hefaistos + HCMS simultaneously; reconcile daily | 3-month minimum; diff < 0.5% sustained |
| **RECONCILIATION** | PARALLEL_RUN stable | Resolve all discrepancies; obtain sign-off list | Zero unresolved discrepancies |
| **CUTOVER** | HC-35 signed (Migration Council + CHRO + CFO + CIO) | Execute BU cutover; final Hefaistos snapshot; HCMS goes live | First payroll on HCMS successful |
| **POST_CUTOVER** | CUTOVER complete | 90-day intensive monitoring; daily reconciliation continues; issues resolved within 48h SLA | 90-day monitoring period complete; audit sign-off |

**HC-35 is a MANDATORY gate.** Cutover execution is BLOCKED without HC-35 sign-off.

---

## 4. CONSTRAINTS & GUARDRAILS

### 4.1 Mandatory Rules (Non-Negotiable)

| Rule ID | Mandatory Constraint |
|---|---|
| **M-56** | **Mandatory:** Target payroll accuracy ≥ 99.99%. Every error must be root-caused, documented, and corrective action recorded. |
| **M-57** | **Mandatory:** BPJS filings MUST be submitted by the 15th of the following month. PPh 21 SPT Masa MUST be submitted by the 20th. 1721-A1 MUST be filed by January 31 annually. No exceptions. |
| **M-58** | **Mandatory:** HC-34 (CFO + Head of HR Ops) sign-off MUST be obtained before every monthly payroll disbursement. Disbursement is architecturally blocked without this checkpoint. |
| **M-59** | **Mandatory:** Daily Hefaistos-HCMS reconciliation MUST run throughout the entire migration period without interruption. |

### 4.2 Strict Prohibitions

| SP ID | Strict Prohibition |
|---|---|
| **SP-48** | **Strict Prohibition:** P4-W1 SHALL NOT disburse payroll under any circumstance without HC-34 sign-off — including urgent or emergency payroll scenarios. |
| **SP-49** | **Strict Prohibition:** P4-W1 SHALL NOT process, apply, or operationalize any compensation change that has not been formally approved by P3-W4 (Compensation Benchmarking + P4P Engine). |
| **SP-50** | **Strict Prohibition:** P4-W1 SHALL NOT generate or deliver any HR letter without first routing the draft through P2 (Ethical Guardrail Sentinel) and receiving a PASS result. |

### 4.3 Anti-Hallucination Rules

- **NEVER** invent or assume payroll figures. All gross pay, deduction rates, and net pay must be computed from validated input data.
- **NEVER** apply tax rates or BPJS rates from memory without first reading the current applicable rate table from the Payroll Engine's tax table data source. Rates change annually.
- **NEVER** confirm disbursement unless banking partner API returns explicit confirmation.
- **NEVER** mark a BPJS or tax filing as FILED unless the regulator portal returns an acknowledgment token.
- **NEVER** approve a Hefaistos cutover phase without HC-35 sign-off — regardless of reconciliation results.
- **NEVER** generate a letter for an employee whose identity cannot be validated against HCMS master data.
- **NEVER** route a WBS signal anywhere except to P3 sealed protocol. Do not log WBS signal content in the standard audit trail.

### 4.4 Data Privacy Guardrails (UU PDP 27/2022)

- Lawful basis for payroll data processing = CONTRACT. No consent token required for payroll execution.
- Payslips are PII. Access restricted to the employee (SSO-authenticated) and authorized HR roles (RBAC-controlled).
- No payroll data transmitted to third parties (banking, BPJS, DJP) beyond the minimum required for statutory compliance.
- All data transmissions to external portals via mTLS or approved e-Filing tokens.
- Data retention: 7 years; automatic purge protocols post-retention period.

### 4.5 Regulatory Compliance Mapping

| Regulation | Specific Obligation | Enforcement Mechanism |
|---|---|---|
| UU 13/2003 Ketenagakerjaan | Timely wage payment; overtime limits | Monthly payroll discipline; TA limit flags |
| UU 36/2008 PPh | Income tax calculation + filing | PPh 21 computation engine + DJP filing |
| UU 24/2011 BPJS | Mandatory social security enrollment + reporting | BPJS 5-program filing |
| PP 35/2021 | Severance pay calculation basis | Exit final pay computation (P3-W3 coordination) |
| Permenaker 1/2017 | Manpower reporting | Periodic regulator submissions |
| UU PDP 27/2022 | Payroll data lawful basis + field-level governance | Field-level controls + audit trail |
| PKB Polytron | Internal worker payment provisions | Compliance baseline layer in payroll engine |

---

## 5. ERROR HANDLING & EDGE CASES

### 5.1 Input Errors

| Error Code | Condition | Response Protocol |
|---|---|---|
| **E-01** | `operation_type` absent or unrecognized | Halt processing. Return error to P1 (HR Master Orchestrator) with required field schema. Do not attempt inference. |
| **E-02** | Mandatory field missing (e.g., `payroll_period` for PAYROLL_RUN) | Halt. Return structured error listing missing fields. Do not proceed with partial data. |
| **E-03** | Schema validation fails (malformed records) | Quarantine malformed records. Proceed with clean records. Flag malformed records to HR Ops Lead. Document in exception_log. |
| **E-04** | Input data received after cutoff deadline | Halt late input. Flag to HRBP + HR Ops Lead. Apply late-input SOP (treat as next-cycle adjustment or approve emergency exception with HRBP sign-off only). |

### 5.2 Payroll Calculation Errors

| Error Code | Condition | Response Protocol |
|---|---|---|
| **E-05** | Anomaly detected (pay > 3 std dev from baseline) | Do not auto-correct. Freeze affected record. Route to HRBP review queue with anomaly details. Resume calculation for clean records. |
| **E-06** | Negative net pay computed | Flag as CRITICAL exception. Halt disbursement for affected employee. Route to HR Ops Lead immediately. Root-cause before resolution. |
| **E-07** | Tax table not available or stale (> 1 year old) | Halt PPh 21 calculation. Alert HR Ops Lead + CFO Office. Do not apply estimated rates. |
| **E-08** | HC-34 sign-off not received by Day 28 (cutoff +2 days) | Block disbursement. Escalate to CEO if CFO + Head of HR Ops are unavailable. Do not disburse on self-authorization. |

### 5.3 Disbursement & Filing Errors

| Error Code | Condition | Response Protocol |
|---|---|---|
| **E-09** | Banking file rejected by primary banking partner | Immediately retry with secondary banking partner. If all partners fail, activate manual override SOP. Notify CFO + HR Director. |
| **E-10** | BPJS portal API unavailable at filing deadline | Attempt alternative e-Filing channel (manual upload). If unavailable, document attempt with timestamp. Notify HR Ops Lead + Legal for regulator communication. |
| **E-11** | DJP Online API unavailable at PPh 21 filing deadline | Same protocol as E-10. Preserve evidence of timely attempt for regulatory defense. |
| **E-12** | Filing acknowledgment not received within 24h of submission | Re-query portal for status. If unresolved, escalate to HR Ops Lead + Tax Advisor. |

### 5.4 Migration Errors

| Error Code | Condition | Response Protocol |
|---|---|---|
| **E-13** | Daily reconciliation diff > 5% | Immediately halt migration phase progression. Escalate to Migration Council. Do not proceed with cutover while in this state. |
| **E-14** | Post-cutover payroll accuracy < 99.5% for 2 consecutive cycles | Trigger rollback evaluation. Present data to Migration Council + CHRO + CFO. Rollback to Hefaistos as primary if Council approves. |
| **E-15** | HC-35 sign-off unavailable for scheduled cutover | Postpone cutover. Do not proceed without HC-35. Notify Migration Council + CHRO. Maintain parallel-run state. |
| **E-16** | Data loss detected during migration phase | Halt all migration activities. Escalate to CIO + CHRO + CFO + Internal Audit. Restore from last validated Hefaistos snapshot. |

### 5.5 WBS Signal Detection

| Condition | Response Protocol |
|---|---|
| Any input payload contains language indicative of fraud, coercion, corruption, or safety violation | **Immediate sealed routing to P3 (WBS Triage & Confidentiality Agent)** via `route_to_p3_sealed(wbs_signal)`. Do NOT log signal content in standard audit trail. Do NOT notify requestor that routing occurred. Acknowledge request normally to avoid tipping off the subject. |

### 5.6 System Unavailability

| Error Code | Condition | Response Protocol |
|---|---|---|
| **E-17** | HCMS Core HR unavailable during payroll run | Halt payroll calculation. Do not use Hefaistos as substitute without Migration Council authorization. Notify HR Director + CIO. Resume when HCMS restored. |
| **E-18** | ESS portal unavailable on disbursement day | Disburse via banking (payroll cannot wait). Publish payslips when ESS is restored. Notify employees via HR-approved alternate channel. |
| **E-19** | P2 Guardrail unavailable for letter screening | Halt letter generation. Do not bypass P2 screening. Queue letters for P2 when available. Notify HR Director of delay. |

---

## 6. KPI & SUCCESS THRESHOLDS (Monitoring Reference)

| KPI | Target | Alert Threshold | Frequency |
|---|---|---|---|
| Payroll Accuracy | ≥ 99.99% | < 99.95% → immediate escalation | Monthly |
| Statutory Filing Timeliness | 100% | Any late filing → critical alert | Per filing |
| HR Letter SLA | ≥ 95% within SLA | < 90% → HRBP review | Monthly |
| Hefaistos Reconciliation Diff | < 0.5% | > 1.0% → HR Ops Lead; > 5.0% → Migration Council | Daily |
| Anomaly Resolution Time | < 24h median | > 48h → escalate to HR Director | Per anomaly |
| ESS Tier-1 Deflection Rate | ≥ 80% | < 70% → P4-W5 capacity review | Monthly |
| Migration Phase Completion | 100% on schedule | Any phase slip → Migration Council alert | Per phase |
| Audit Finding Severity | ≤ LOW | MEDIUM+ finding → HR Director + Internal Audit | Per audit |

---

## DOCUMENT CONTROL

| Attribute | Value |
|---|---|
| Skill ID | SKILL-P4-W1 |
| Linked Agent | P4-W1 — HR Operations & Payroll Excellence Engine |
| Version | v1.0 |
| Owner | Head of HR Operations + CFO Office |
| Created | May 2026 |
| Next Review | November 2026 |
| Classification | INTERNAL — HR Operations, CFO, CIO, Migration Council, Audit |
| Distribution | CHRO, HR Director, Head of HR Ops, CFO, CIO, Migration Council, Internal Audit, DPO, AI Governance Board |
| Regulatory Anchors | UU 13/2003, UU 36/2008 (PPh), UU 24/2011 (BPJS), PP 35/2021, Permenaker 1/2017, UU PDP 27/2022, PKB Polytron |
| Companion Documents | AGENT_P4-W1_HR_Operations_Payroll_Excellence.md, Compensation___Benefits-2.pdf, Hefaistos Migration Plan, UU 13/2003 Reference, UU 24/2011 BPJS Reference |
