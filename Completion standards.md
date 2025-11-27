# Delivery readiness & Completion standards  
This document defines the minimum conditions required for work to enter a sprint (Definition of ready) and the criteria that determine when work is considered complete (Definition of Done).  
These standards ensure clarity, reduce rework, and align all teams on how delivery is validated—especially when the final approval belongs to a downstream function or business-facing role.

---

## 1. Purpose

The goal of this guideline is to:

- Prevent work from entering a sprint before it is clear, validated, and feasible  
- Ensure consistent delivery quality  
- Establish a shared understanding of what “Ready” and “Done” mean across Dev, SE, QA, and the Data/Modeling Team  
- Align internal work with the expectation that **“Done is decided by the receiving team, not by Development alone.”**

---

## 2. Definition of Ready (DoR)

An item can only be included in a sprint if **all** conditions below are met.  
If any requirement is missing, the item is deferred.

### 2.1 Requirements clarity
- User story or ticket clearly states the problem or goal  
- Acceptance criteria are explicit, testable, and visible in the ticket  
- Non-functional expectations (performance, data, API behavior, constraints) are defined when relevant  

### 2.2 Technical validation
- Designs, schemas, or field mappings are attached if needed  
- API behavior is understood or confirmed with Solutions Engineering  
- Data requirements validated with the Data/Modeling Team  

### 2.3 Dependency readiness
- External dependencies (API changes, data availability, environment setup) are ready or scheduled  
- No blocking dependencies remain unresolved
  
### 2.4 Documentation availability
- Existing documentation reviewed  
- Any missing documentation identified before entering the sprint  

**If an item fails Ready → it does not enter the sprint.**

---

## 3. Definition of Done (DoD)

Work is not “Done” when Dev finishes coding.  
It is considered Done **only when the receiving function accepts it**, depending on the type of work:

- Business Stakeholder  
- Solutions Engineering  
- Data/Modeling Team  
- QA  

Example: To reflect the operational reality of many teams, the **last development status is “Review” by the receiving function**, and only after acceptance can the item move to “Done”.

### 3.1 Functional completion
- All acceptance criteria pass  
- Expected inputs/outputs behave correctly  
- No regressions introduced  

### 3.2 Cross-Team validation (depending on the work type)

#### Development → Solutions Engineering
- API logic validated  
- Field mappings correct  
- Integrations behave as expected  
- Edge cases handled or documented  

#### Solutions Engineering → Data/Modeling Team  
- Payloads validated  
- Expected schema fields present  
- No mismatches in staging  
- Data flow tested end-to-end  

#### Data/Modeling Team → QA
- Model or data behavior validated  
- No schema or data errors  
- Acceptance criteria confirmed  

#### QA → Business Stakeholder
- Tests completed  
- No critical defects remain  
- Work is ready for presentation or client-facing review  

### 3.3 Final acceptance (Required for Done)

**The receiving team accepts the work and moves it into Done.**  
Examples:

- Business Stakeholder moves the ticket from “Review” → “Done”  
- SE approves integration behavior  
- Data/Modeling Team signs off on schema/data behavior  
- QA validates that the work is fully releasable  

Done means:  
**“Accepted by the owner who validates the outcome, not the owner who produced it.”**

### 3.4 Documentation completed
- Notes, schemas, instructions, or API details updated  
- Any operational changes documented  
- Release notes prepared if needed  

### 3.5 Deployment ready
- Work is deployable without additional changes  
- No manual fixes required after merge  

---

## 4. Why this matters

- Reduces rework caused by unclear requirements  
- Ensures clean and intentional handoffs  
- Makes progress measurable and predictable  
- Aligns all teams around quality and acceptance  
- Reflects the reality that “Done” is outcome-based, not activity-based  

---

## 5. Versioning

**Version:** 1.1  
**Author:** G. Solera  
**Changes:** Updated terminology (Business Stakeholder, Data/Modeling Team)
