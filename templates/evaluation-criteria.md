# Evaluation Criteria Template

Use this template to define how agents, workflows, or agent fleets should be evaluated before being promoted or considered production-ready.

---

## Evaluation Overview

**Item Being Evaluated:** [Agent name / Workflow / Fleet component]  
**Evaluation Version:** [e.g. 1.0]  
**Date:** [Date]  
**Evaluator(s):** [Name or role]

## Evaluation Objectives

**What are we trying to assess?**
- [Objective 1]
- [Objective 2]
- [Objective 3]

## Evaluation Dimensions

Use the categories below to structure your evaluation.

### 1. Output Quality

| Criterion                    | Description                                      | Target / Threshold          | Status (Pass / Fail / N/A) | Notes |
|-----------------------------|--------------------------------------------------|-----------------------------|----------------------------|-------|
| Accuracy                    | Correctness of outputs                           | [Define target]             |                            |       |
| Completeness                | All required information is present              | [Define target]             |                            |       |
| Consistency                 | Outputs are stable across similar inputs         | [Define target]             |                            |       |
| Clarity & Structure         | Outputs follow expected format and are readable  | [Define target]             |                            |       |

### 2. Reasoning & Evidence

| Criterion                    | Description                                      | Target / Threshold          | Status | Notes |
|-----------------------------|--------------------------------------------------|-----------------------------|--------|-------|
| Evidence-based outputs      | Outputs include supporting reasoning or sources  | Required                    |        |       |
| Handling of ambiguity       | Clearly identifies and handles unclear inputs    | [Define target]             |        |       |
| Confidence calibration      | Confidence levels are reasonable and justified   | [Define target]             |        |       |

### 3. Governance & Compliance

| Criterion                    | Description                                      | Target / Threshold          | Status | Notes |
|-----------------------------|--------------------------------------------------|-----------------------------|--------|-------|
| Adherence to boundaries     | Agent stays within defined scope                 | Required                    |        |       |
| Handoff contract compliance | Follows defined handoff rules                    | Required                    |        |       |
| Auditability                | Sufficient logging and traceability              | Required                    |        |       |
| Data handling               | Respects data sensitivity and usage rules        | [Define target]             |        |       |

### 4. Performance & Efficiency

| Criterion                    | Description                                      | Target / Threshold          | Status | Notes |
|-----------------------------|--------------------------------------------------|-----------------------------|--------|-------|
| Latency                     | Response time is acceptable                      | [Define target]             |        |       |
| Cost efficiency             | Token usage and model costs are reasonable       | [Define target]             |        |       |
| Reliability                 | Consistent performance over time                 | [Define target]             |        |       |

### 5. User / Stakeholder Experience

| Criterion                    | Description                                      | Target / Threshold          | Status | Notes |
|-----------------------------|--------------------------------------------------|-----------------------------|--------|-------|
| Usability of outputs        | Outputs are actionable and easy to consume       | [Define target]             |        |       |
| Error handling              | Graceful handling of failures and edge cases     | [Define target]             |        |       |

## Overall Assessment

**Summary of Findings:**
[High-level summary of evaluation results]

**Strengths:**
- [Strength 1]
- [Strength 2]

**Areas for Improvement:**
- [Area 1]
- [Area 2]

**Risks Identified:**
- [Risk 1]
- [Risk 2]

## Recommendation

**Overall Recommendation:**
- [ ] **Promote to Production**
- [ ] **Promote with Conditions**
- [ ] **Return for Further Development**
- [ ] **Redesign Required**

**Conditions / Next Steps (if applicable):**
- [Action item 1]
- [Action item 2]

**Re-evaluation Required?**
- [ ] Yes — [When / What should be re-evaluated]
- [ ] No

---

**Evaluator Signature / Approval:** ___________________________  
**Date:** [Date]