# Agent Definition Template

Use this template to define specialist agents in a clear and consistent way.

---

## Agent Name

**Name:** [Short, descriptive name of the agent]  
**Version:** [e.g. 1.0]

## Role & Responsibility

**One-sentence description:**  
[What is this agent’s primary job?]

**Detailed Responsibilities:**
- [Responsibility 1]
- [Responsibility 2]
- [Responsibility 3]

**Out of Scope:**
- [What this agent should *not* do]

## Inputs

**Expected Inputs:**
- [Input type 1] — [Description and format]
- [Input type 2] — [Description and format]

**Required Context:**
- [Any previous agent outputs or knowledge this agent needs]

## Outputs

**Expected Outputs:**
- [Output type 1] — [Format and structure]
- [Output type 2] — [Format and structure]

**Required Elements in Output:**
- [e.g. Reasoning / Justification]
- [e.g. Confidence level]
- [e.g. References to source material]

## Tools & Capabilities

**Available Tools:**
- [Tool 1] — [Purpose]
- [Tool 2] — [Purpose]

**Model Recommendations:**
- Preferred model(s): [e.g. Grok 4.1 Fast, or specific model]
- When to use lighter/faster models: [Guidance]

## Knowledge Sources

**Approved Knowledge Sources:**
- [Source 1]
- [Source 2]

**Knowledge Usage Rules:**
- [Any restrictions or guidelines on how knowledge should be used]

## Handoff Contracts

**Can receive work from:**
- [Agent / Orchestrator names]

**Can hand off work to:**
- [Agent names]

**Handoff Requirements:**
- What must be included when handing work to this agent?
- What must this agent include when handing work to another agent?

## Evaluation Criteria

**Quality Criteria:**
- [Criterion 1]
- [Criterion 2]

**Governance Criteria:**
- [e.g. Must produce evidence-based outputs]
- [e.g. Must respect defined boundaries]

**Success Indicators:**
- [How do we know this agent is performing well?]

## Constraints & Boundaries

**Hard Constraints:**
- [Things this agent must never do]

**Soft Boundaries:**
- [Areas where the agent should be cautious or escalate]

## System Prompt Guidance

**Core Instructions to Include:**
- [Key behavioral instructions]
- [Tone and style guidance]
- [How to handle ambiguity or missing information]

> **Note:** The actual system prompt should be stored separately (e.g. in the agent’s configuration) and kept in sync with this definition.

## Notes & Rationale

**Design Decisions:**
- [Why was this agent designed this way?]

**Open Questions / Future Improvements:**
- [Any known limitations or areas for future work]

---

**Agent Owner:** [Name or role]  
**Last Updated:** [Date]  
**Status:** [Draft / In Review / Active]