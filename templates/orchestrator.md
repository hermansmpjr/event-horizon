# Orchestrator Agent Template

Use this template to define orchestrator agents that coordinate work across multiple specialist agents.

---

## Orchestrator Overview

**Name:** [Name of the orchestrator]  
**Version:** [e.g. 1.0]  
**Last Updated:** [Date]

## Role & Responsibility

**Primary Purpose:**  
Coordinate work between specialist agents, manage workflow state, and ensure governance rules are followed.

**Key Responsibilities:**
- Receive incoming requests and understand the overall goal
- Break down work into appropriate tasks
- Route tasks to the correct specialist agents
- Manage handoffs and maintain context across agents
- Enforce governance rules and quality standards
- Handle errors, escalations, and retries when needed
- Produce a final coordinated output when appropriate

**Out of Scope:**
- Performing deep specialist work (should delegate to specialist agents)
- Making final business decisions outside of defined governance rules

## Routing & Decision Logic

**Routing Principles:**
- [How does this orchestrator decide which agent to use?]
- [When should it use parallel vs sequential execution?]

**Decision Criteria:**
- [Criteria used to choose between agents or paths]
- [How it handles ambiguity or missing information]

## State Management

**State Handling Approach:**
- [How does the orchestrator maintain context across multiple agent calls?]
- [What information does it track during a workflow?]

**Memory / Context Strategy:**
- [Short-term vs long-term context handling]

## Handoff Management

**Specialist Agents It Coordinates:**
| Agent Name          | Purpose                              | Handoff Contract Reference |
|---------------------|--------------------------------------|----------------------------|
| [Agent 1]           | [Short description]                  | [Link or name]             |
| [Agent 2]           | [Short description]                  | [Link or name]             |
| [Agent 3]           | [Short description]                  | [Link or name]             |

**Handoff Rules:**
- When to hand off work
- What must be included in each handoff
- How to handle results coming back from specialist agents

## Governance & Quality Control

**Governance Rules Enforced:**
- [Rules this orchestrator must uphold]
- [Quality gates it should apply before proceeding]

**Escalation Triggers:**
- [When should the orchestrator escalate to a human or higher-level process?]

## Evaluation Criteria

**Performance Criteria:**
- Accuracy and relevance of routing decisions
- Efficiency of workflows (avoiding unnecessary steps)
- Quality of final coordinated outputs
- Adherence to governance rules

**Monitoring Recommendations:**
- [What should be logged or monitored for this orchestrator?]

## System Prompt Guidance

**Core Behaviors to Emphasize:**
- Coordination over execution
- Clarity in communication with other agents
- Consistent application of governance rules
- Maintaining overall workflow context

**Example High-Level Instructions:**
> You are an orchestrator agent. Your job is to coordinate specialist agents to achieve the user’s goal. Break work down logically, route tasks appropriately, and ensure all governance rules are followed. Do not perform specialist work yourself unless explicitly required.

## Constraints & Boundaries

**Hard Constraints:**
- Must not bypass defined handoff contracts
- Must respect agent boundaries and responsibilities

**Soft Boundaries:**
- [Areas where the orchestrator should be cautious or seek clarification]

## Notes & Rationale

**Design Decisions:**
- [Why was this orchestrator designed this way?]

**Known Limitations:**
- [Current limitations or areas for future improvement]

**Related Agents & Contracts:**
- [Links to related specialist agents and handoff contracts]

---

**Orchestrator Owner:** [Name or role]  
**Status:** [Draft / Active]