# Project Charter Template  
A lean, structured document for defining purpose, scope, alignment, and execution for technical projects in small, fast-moving teams.

---

## 1. Project overview

**Project Name:**  
**Project Owner:**   
**Teams Involved:** (Dev, SE, Data/ML, QA, DevOps, etc.)  
**Summary:**  
Brief description of the problem, scope, and expected outcome.

---

## 2. Problem Statement

Describe the problem or opportunity driving the project.  
Articulate:  
- What is happening  
- Why it matters  
- How it impacts delivery, clients, or internal workflows  

---

## 3. Objectives & Success criteria

### Objectives  
List 3–5 high-level objectives that define what success means.

### Success Criteria

| Measure | Target | Validation Method |
|---------|--------|-------------------|
| Example: ML schema validation | 0 mismatches | Staging dashboard |
| Example: API integration ready | 100% expected fields | Logs + QA |
| Example: Onboarding milestone delivered | On time | Client environment validation |

---

## 4. Scope definition

### In Scope  
List what the team will deliver (features, integrations, environments, documents).

### Out of Scope  
Clarify exclusions, deferrals, and non-goals.

---

## 5. Requirements summary

Capture essential requirements that shape delivery.

| Requirement | Description | Owner |
|------------|-------------|--------|
| Example: CRM must provide field X | Required for ML model | SE |
| Example: New staging schema | Needed for testing | Data/ML |

---

## 6. Dependencies

| Dependency | Type | Owner | Risk if not ready |
|-----------|------|--------|-------------------|
| API token refresh | API | SE | Blocks testing |
| Model version update | ML | Data Science | Prevents rollout |

---

## 7. Risks & Mitigations

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| Missing CRM fields | Medium | High | Early validation + SE alignment |
| Environment delays | Low | Medium | Buffer + DevOps coordination |

---

## 8. Timeline & Milestones

| Milestone | Target Date | Owner | Status |
|-----------|--------------|--------|--------|
| Kickoff | MM/DD | PM | Planned |
| Requirements Finalized | MM/DD | SE/PM | Planned |
| Development Complete | MM/DD | Dev | Planned |
| ML/Data Validation | MM/DD | DS | Planned |
| Client Delivery | MM/DD | PM | Planned |

---

## 9. Execution approach

Describe the operating model:  
- Sprint structure  
- Review/checkpoint cadence  
- Jira board mapping  
- Handoffs (Dev → SE → ML → QA)  
- Definition of Ready and Done expectations  
- Required documentation updates  

---

## 10. Communication plan

| Group | Communication | Frequency | Owner |
|-------|---------------|-----------|--------|
| Engineering | Status updates | Weekly | PM |
| Leadership | Progress summary | Bi-weekly or by milestone | PM |
| Client (if applicable) | Delivery updates | As needed | PM |

---

## 11. How this charter differs from large organization charters

This template is intentionally lightweight and optimized for small technical teams.  
Large organizations require heavier governance due to scale, compliance, and role specialization.  
Key differences:

- **Documentation depth:** This version excludes regulatory, financial, and procurement details.  
- **Approvals:** Enterprise charters require VP/PMO/Architecture sign-off; here approval is minimal.  
- **Role structure:** Assumes fewer roles, with PM covering analysis, coordination, and delivery.  
- **Scope flexibility:** Designed for iterative refinement rather than fixed early scope.  
- **Governance:** Removes enterprise elements such as budgeting, steering committees, and formal stage gates.  
- **Audience:** Communicates horizontally within a small cross-functional team, not across large departments.

---

## 12. Document Versioning

**Version:** 1.0  
**Author:** G. Solera  
