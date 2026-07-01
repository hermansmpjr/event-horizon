# Handoff Contract Template

Use this template to define clear expectations when work moves between agents.

---

## Handoff Overview

**From Agent:** [Name of the sending agent]  
**To Agent:** [Name of the receiving agent]  
**Contract Version:** [e.g. 1.0]  
**Last Updated:** [Date]

## Purpose of This Handoff

**Why does this handoff exist?**  
[Brief description of the reason for this connection between agents]

## Handoff Packet Fields

All routing handoffs must include these fields:

| Field | Required | Format | Description |
|-------|----------|--------|-------------|
| `SelectedAgent` | Yes | string | Target child agent or role |
| `Confidence` | Yes | High / Medium / Low | Routing confidence |
| `Reason` | Yes | string | Why this routing was chosen |
| `RequiredInputsMissing` | Yes | list | Gaps that block work (empty list OK, never omit) |
| `InputsReceived` | Yes | object | What was provided |
| `ExecutionConstraints` | Yes | string | No guessing; preserve source discipline |
| `RequestedDeliverable` | Yes | string | Expected artifact |
| `PayloadForChildAgent` | Yes | object | Structured input data |
| `ExpectedReturnContract` | Yes | string | What must come back |
| `SuggestedNextRoute` | No | string | Optional downstream routing |
| `Mode` | No | enum | fast / deep / export / debug / selftest |

## Routing Rules

- Parent owns final synthesis
- Children do not address end users
- Only authorized export paths produce customer-facing output
- One child per request unless phased work is explicitly requested
- Tool/MCP evidence must be source-classified before recommendations

## Input Requirements

**Additional context beyond the packet:**

| Field | Required | Format / Type | Description |
|-------|----------|---------------|-------------|
| [Field 1] | Yes/No | [e.g. string, JSON] | [What this field contains] |

**Minimum Required Context:**
- [What context or previous outputs must be included]

## Output Expectations

**What the receiving agent must produce:**

| Output                  | Format                  | Description                                      | Required Elements                     |
|-------------------------|-------------------------|--------------------------------------------------|---------------------------------------|
| [Primary Output]        | [e.g. JSON, Markdown]   | [Main deliverable]                               | [Reasoning, confidence, references]   |
| [Secondary Output]      | [e.g. status, log]      | [Additional information]                         | [Optional or required]                |

## Success Criteria

**How do we know the handoff was successful?**

- [Criterion 1]
- [Criterion 2]
- [Criterion 3]

**Failure / Escalation Conditions:**
- [When should the receiving agent escalate or reject the handoff?]

## Responsibility Boundaries

**Sending Agent is Responsible For:**
- [What the sender must ensure before handing off]

**Receiving Agent is Responsible For:**
- [What the receiver must do after receiving the work]

**Shared / Joint Responsibilities:**
- [Any areas where responsibility is shared]

## Communication & Logging

**Required Logging:**
- [What information should be logged during this handoff]

**Status Updates:**
- [How should status be communicated back to the sender or orchestrator?]

## Notes & Rationale

**Why this contract was designed this way:**
- [Design reasoning]

**Known Limitations:**
- [Any known weaknesses or areas for improvement]

**Related Contracts:**
- [Links to other handoff contracts that connect to this one]

---

**Contract Owner:** [Name or role]  
**Reviewers:** [Names]  
**Status:** [Draft / Active / Deprecated]