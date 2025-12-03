# Incident Management & Root Cause Analysis workflow  
A lightweight but robust operational process to identify, respond to and prevent technical incidents.  

---

## 1. Purpose

This workflow defines how the team detects incidents, responds to them, investigates the underlying causes, and prevents recurrence.

Goals:
- Minimize impact on customers and business stakeholders  
- Restore service quickly and safely  
- Understand what truly caused the issue (not just symptoms)  
- Drive meaningful corrective and preventive actions

---

## 2. Definitions

**Incident:**  
Any unplanned event that disrupts system functionality, data integrity, or customer experience.

**Severity (SEV) Levels:**  
High-level classification for routing and escalation.  

**Incident Commander (IC):**  
The single point of coordination responsible for communication and directing the response.

**Root Cause Analysis (RCA):**  
A structured investigation to identify the chain of causes (technical + operational) behind an incident.

---

## 3. Incident lifecycle overview
Detection → Triage → Response → Stabilization → Root Cause Analysis → Action Items → Verification

Each phase has clear owners and required outputs.

---

## 4. Phase 1: Detection

Incidents may be detected through:

- Monitoring and alerts  
- Data quality checks  
- Errors observed by engineering  
- Reports from customer-facing teams  
- Automated ML model validation

**Output:**  
A new incident is logged in the tracking system with timestamp, initial severity, and description.

---

## 5. Phase 2: Triage

Determine:

- **Severity** (impact, scope, urgency)  
- **Whether to escalate** to on-call or leadership  
- **Who becomes Incident Commander**

Triage must happen within minutes for high-severity incidents.

**Output:**  
Severity level confirmed + IC assigned + first communication sent.

---

## 6. Phase 3: Response

The Incident Commander coordinates:

- Assigning technical owners  
- Establishing a slack/teams channel  
- Validating the issue  
- Gathering logs, metrics, and recent deployments  
- Applying a mitigation or rollback  
- Communicating updates to business stakeholders

**Guiding principles:**

- Focus on stabilization, not solving root cause  
- Communicate early and often  
- Avoid parallel conflicting fixes

**Output:**  
Service stabilized or degraded impact contained.

---

## 7. Phase 4: Stabilization & containment
After detection and initial response, the priority is containment: preventing further impact, data corruption, or cascading failures.

### 7.1 Containment measures (short-term)
These actions do **not** fix the root cause. They only stop active damage or service degradation.

Examples:
- Disable the failing feature
- Roll back the deployment
- Pause ETL / ingestion
- Revert configuration
- Apply manual correction to data for short-term continuity

**Output:**  
System is no longer deteriorating and impact is contained.

---

## 8. Phase 5: Root Cause Analysis (RCA)

Performed after stabilization.

### 8.1 RCA Steps

1. **Reconstruct the factual timeline**  
   No interpretations, no blame — only verifiable events.

2. **Immediate Cause (Trigger)**  
   The direct failure that produced the incident.

3. **System Weakness Analysis ("Why the system allowed this")**  
   Identify which gaps in the system made the incident *possible*:
   - Missing validation layers  
   - Incorrect or undocumented assumptions  
   - Lack of integration checks  
   - Weak data contracts  
   - Insufficient monitoring or alert thresholds  
   - Poorly defined handoffs between teams  

   This step explains **not just what broke**, but **why our systems did not stop it earlier**.

4. **Contributing factors**  
   Environmental, process, or organizational elements that increased impact.

5. **Detection Gap Analysis**  
   Why it escaped:
   - No alert for this condition  
   - Wrong alert thresholds  
   - Logs incomplete  
   - QA coverage missing  
   - Acceptance criteria unclear  
   - Monitoring for downstream systems missing  

6. **Define Preventive Actions (Systemic)**  
   Based on the system weaknesses identified.

---

## 9. Phase 6: Corrective Actions

Corrective actions are divided in two categories:

### 9.1 Containment Actions (short-term)
Already executed during the incident.  
Document them for traceability.

### 9.2 Systemic Actions (long-term)
Permanent changes that eliminate the failure mode.

Examples:
- Add automated input validation  
- Strengthen data schema contracts  
- Add pre-deployment validation steps  
- Improve cross-team handoff documentation  
- Expand test coverage for the failure mode  
- Modify dashboards/alerts  
- Update model assumptions or versioning  
- Introduce runbooks or checklists  

**Key rule:**  
Systemic actions must address *why the system allowed the incident*, not just the trigger.

**Output:**  
Action tracker with owners, deadlines, and priority.

---

## 10. Phase 7: Verification

Verification ensures the incident is **truly** resolved long-term.

Verification includes:

- All actions completed  
- No recurrence observed  
- Monitoring confirms stability  
- Business Stakeholder validates outcome  
- Lessons documented and shared  

**Output:**  
Incident formally closed.

---

## 11. Governance & Cadence

- **Weekly / bi-weekly review:** open incidents + action items  
- **Monthly review:** patterns, repeated failures, systemic gaps  
- **Quarterly review:** improvements to process, SEV definitions, and documentation

---

## 12. Versioning

**Version:** 1.0  
**Author:** G. Solera  
**Last Updated:** 12/03/2025  
**Notes:** Initial release of incident management + RCA workflow.

---


