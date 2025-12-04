# Incident Review template (Postmortem)
A structured analysis to understand what happened, why it happened, and how to prevent recurrence.  
Designed for cross-functional teams working across software, data, and modeling systems.

---

## 1. Incident Summary
**Incident date:**  
**Impact window:**  
**Severity level:** 
**Affected systems / Products:**  
**Reported by:**  
**Incident commander:**  
**Review date:**  

**Short summary:**  
A 3–5 line executive description of the incident, focusing on impact and symptom, not cause.

---

## 2. Impact assessment
Describe the real impact using factual, quantifiable information when possible.

- **User impact:**  
- **Business impact:**  
- **Internal impact:**  

---

## 3. Timeline of Events

A precise, factual reconstruction of everything that happened.

| Time (local/UTC) | Event | Actor/System |
|------------------|-------|--------------|
| hh:mm | Alert triggered | Monitoring |
| hh:mm | IC assigned | Engineering |
| hh:mm | Temporary fix applied | Backend |
| ... | ... | ... |

Guidelines:
- No interpretations or blame.  
- Only observable facts.  
- Include deploys, merges, ETL runs, model refreshes, config changes, outages, etc.

---

## 4. Containment actions (short-term)
These actions stopped the incident from getting worse.

Examples:
- Disable/rollback feature  
- Stop ETL ingestion  
- Apply temporary data fix  
- Revert configuration  
- Manually correct outputs  
- Restart or redeploy the service  

**Containment Applied:**  
-  
-  
-  

**Effectiveness:**  
Explain how these measures prevented a “snowball effect” or additional impact.

---

## 5. Root Cause Analysis (RCA)

### 5.1 Immediate cause (trigger)
What directly caused the failure.

### 5.2 System weakness ("Why the system allowed this")
Identify structural or procedural gaps that made the incident possible or allowed it to progress:

- Missing validation layers  
- Weak schema/data contracts  
- Incorrect assumptions between teams  
- Lack of automated tests for this scenario  
- Poorly defined handoffs  
- Dependencies not monitored  
- Documentation gaps  
- Monitoring/alerting blind spots  

### 5.3 Detection Gap ("Why it wasn’t caught earlier")
Explain what monitoring/alerting/logging mechanisms failed or were missing:

- No alert for this condition  
- Wrong thresholds  
- Logs insufficient to detect anomaly  
- QA/test coverage missing  
- Acceptance criteria incomplete  
- No integration validation between Dev → Data/Modeling → QA  

---

## 6. Systemic corrective actions (long-term)
Permanent changes required to prevent recurrence.

| ID | Systemic action | Owner | Priority | Due date | Status |
|----|-----------------|-------|----------|----------|--------|
| 1 | Strengthen validation for X | Dev Team | High | YYYY-MM-DD | Open |
| 2 | Add monitoring for Y | Infra/DevOps | High | YYYY-MM-DD | Open |
| 3 | Improve cross-team handoff documentation | PMO / TPM | Medium | YYYY-MM-DD | In Progress |

Guidelines:
- Must address **root cause** or **system weakness** — not just symptoms.  
- Cannot be “communicate better.”  
- Must have a clear owner and timeline.  

---

## 7. Additional observations / Lessons learned
Capture concrete insights about:
- Fragile areas in the architecture  
- Process gaps between teams  
- Repeated patterns or failure modes  
- Missing knowledge, unclear responsibilities  
- Improvements for runbooks, SOPs, or documentation  

Not philosophical — **operational and actionable**.

---

## 8. Verification & closure

This section is completed once all systemic actions are delivered.

- **All systemic actions completed on:**  
- **Verified by:** (Engineering Lead / Data Lead / TPM)  
- **Validated by Business Stakeholder:**  
- **Monitoring period completed:** (Yes/No)  
- **Recurrence observed:** (Yes/No)  

---

## 9. Versioning

**Version:** 1.0  
**Author:** G. Solera  
**Last Updated:** 12/04/2025 
**Notes:** Initial release of the updated, cross-functional postmortem template.

---

