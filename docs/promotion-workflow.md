# Promotion Workflow

This document describes how agents and agent workflows move through the Event-Horizon system — from initial creation to production use.

The goal of the promotion workflow is to ensure that only well-designed, properly evaluated agents reach production, while still allowing for reasonable speed of development.

## Overview

Promotion follows the **IDEA** cycle and is closely tied to the three-layer architecture:

- **Innovate** → Happens in the **Meta Layer**
- **Develop** → Happens in the **Development Layer**
- **Evaluate** → Happens primarily in the **Development Layer** (with Meta oversight)
- **Automate** → Happens when moving into the **Production Layer**

## Promotion Stages

### Stage 1: Innovation & Initial Development

**Location:** Meta Layer + Development Layer

**Activities:**
- New agent ideas are created or existing patterns are adapted.
- Initial agent definitions are written using the [Agent Definition Template](templates/agent.md).
- Basic prompts and logic are developed.
- Early testing is performed in the development environment.

**Exit Criteria:**
- Agent has a clear purpose and defined boundaries.
- Initial version of the agent definition exists.
- Basic functionality has been demonstrated in development.

### Stage 2: Structured Development & Testing

**Location:** Development Layer

**Activities:**
- The agent is developed more fully.
- Handoff contracts are defined (using the [Handoff Contract Template](templates/handoff-contract.md)).
- Integration with orchestrators or other agents is tested.
- Edge cases and failure modes are explored.

**Exit Criteria:**
- Agent behaves reliably in common scenarios.
- Handoff contracts with related agents are defined.
- Initial documentation is in place.

### Stage 3: Formal Evaluation

**Location:** Development Layer + Meta Layer

**Activities:**
- The agent is evaluated using the [Evaluation Criteria Template](templates/evaluation-criteria.md).
- Quality, governance, performance, and risk are assessed.
- Feedback is gathered from relevant stakeholders (if applicable).
- A formal go/no-go decision is made.

**Possible Outcomes:**
- **Promote** — Agent meets criteria and can move to production.
- **Promote with Conditions** — Minor issues must be addressed.
- **Iterate** — Significant issues found; return to development.
- **Redesign** — Fundamental problems; major rework required.

**Exit Criteria:**
- Evaluation has been completed and documented.
- All critical issues have been resolved (or accepted with mitigation).
- Approval has been granted (by owner or governance process).

### Stage 4: Promotion to Production

**Location:** Production Layer

**Activities:**
- The agent is deployed to the production environment.
- Monitoring and logging are enabled.
- Operational documentation is finalized.
- The agent is added to the active fleet registry (if applicable).

**Post-Promotion Activities:**
- Monitor performance and quality over time.
- Collect feedback and issues.
- Plan periodic re-evaluation (especially for high-impact agents).

## Promotion Principles

### 1. Evidence Over Speed
Never promote an agent just because it “mostly works.” Require evidence that it meets defined standards.

### 2. Clear Ownership
Every agent should have a clear owner responsible for its quality and ongoing maintenance.

### 3. Reversible Decisions
Treat promotion as a reversible decision. It should be possible to roll back or demote an agent if serious issues are discovered.

### 4. Proportionate Rigor
Apply stricter evaluation to high-impact or high-risk agents. Lower-risk agents can follow a lighter process.

### 5. Continuous Improvement
Promotion is not the end. Use production feedback to drive improvements through the IDEA cycle.

## Promotion Checklist (Summary)

Before promoting an agent to production, ensure the following:

- [ ] Agent definition is complete and up to date
- [ ] Handoff contracts are defined and agreed upon
- [ ] Evaluation has been performed and documented
- [ ] Critical issues have been addressed
- [ ] Monitoring and logging are in place
- [ ] Documentation is sufficient for operations
- [ ] Owner is identified and accepts responsibility

## Roles in the Promotion Process

| Role                    | Responsibilities                                      |
|-------------------------|-------------------------------------------------------|
| **Agent Owner**         | Primary responsibility for quality and maintenance    |
| **Developer**           | Builds and iterates on the agent                      |
| **Evaluator / Reviewer**| Conducts formal evaluation before promotion           |
| **Governance / Meta**   | Defines standards and approves high-impact promotions |

---

This workflow is designed to balance **speed of development** with **responsible governance**.