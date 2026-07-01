# Intake Handoff Template

Use this template when a user-facing intake agent converts plain-language requests into a structured packet for upward submission to the fleet governor.

**Constraint:** The intake agent submits to the governor only. It must not call factory, discovery, mapper, or other meta agents directly.

---

## Packet Overview

**Packet Version:** [e.g. 1.0]  
**Submitting Agent:** [Intake agent name]  
**Target:** Fleet Governor (fixed — never another agent)  
**Date:** [Date]

## Request Summary

**User Request (verbatim or paraphrased):**  
[What the user asked for]

**Classification:**

| Value | Meaning |
|-------|---------|
| `prompt-help` | User needs help crafting a prompt or instruction |
| `process-doc` | User wants process documentation |
| `automation-candidate` | Request may become an automation workflow |
| `agent-candidate` | Request may become a new agent |
| `not-ready` | Insufficient information to proceed |

**Selected classification:** [one value from above]

## Known Context

### Systems Mentioned

| System | Confirmed by user | Notes |
|--------|-------------------|-------|
| [System 1] | Yes / No | [Context] |

### Sources Mentioned

| Source (URL or path) | Confirmed by user | Notes |
|----------------------|-------------------|-------|
| [Source 1] | Yes / No | Preserve URLs character-for-character |

## Risk Flags

Select applicable flags from allowed values only:

- [ ] Scope unclear
- [ ] Customer-facing content possible
- [ ] Cross-system integration required
- [ ] Governance-sensitive change
- [ ] Data sensitivity concerns
- [ ] None identified

## Self-Test Checklist (emission gate)

The packet must not be emitted if any item fails:

| ID | Check | Pass |
|----|-------|------|
| ST-01 | Classification is exactly one allowed value | |
| ST-02 | No fabricated systems or sources | |
| ST-03 | URLs preserved verbatim | |
| ST-04 | Risk flags selected from allowed values | |
| ST-05 | No direct routing to non-governor agents | |
| ST-06 | Unknowns marked explicitly | |
| ST-07 | No customer-facing commitments | |
| ST-08 | Packet is internally consistent | |

## Payload for Governor

```json
{
  "classification": "[value]",
  "userRequest": "[text]",
  "knownSystems": { "confirmed": [], "unconfirmed": [] },
  "knownSources": { "confirmed": [], "unconfirmed": [] },
  "riskFlags": [],
  "selfTestResult": "PASS | BLOCKED",
  "blockingReasons": []
}
```

## Governor Routing (for reference)

After receiving this packet, the governor routes to:

| Work type | Typical target |
|-----------|----------------|
| New agent / major change | Agent Factory |
| Knowledge discovery | Knowledge Discovery agent |
| Knowledge design | Knowledge Mapper agent |
| Documentation / skill authoring | Fleet Documenter |
| Strategic / governance | Self (Governor) |

---

**Template Owner:** [Name or role]  
**Status:** [Draft / Active]