# Glossary

This glossary defines key terms used throughout the Event-Horizon IDEA framework.

## Agent
A specialized AI system designed to perform a specific set of tasks or responsibilities within a larger workflow.

## Orchestrator
An agent whose primary role is to coordinate other agents. It receives work, breaks it down, routes tasks to appropriate specialist agents, manages state, and ensures governance rules are followed.

## Specialist Agent
An agent focused on a narrow, well-defined domain or task (as opposed to an orchestrator). Examples include research agents, summarization agents, or data extraction agents.

## Handoff
The transfer of work from one agent to another. A well-defined handoff includes clear inputs, expected outputs, and success criteria.

## Handoff Contract
A formal agreement between two agents that defines what information must be passed, what output is expected, and under what conditions the handoff is considered successful.

## IDEA Cycle
The core operating framework of Event-Horizon:
- **I**nnovate – Explore and create new capabilities
- **D**evelop – Build and test in a controlled environment
- **E**valuate – Assess quality, risk, and readiness
- **A**utomate – Promote to production and operationalize

## Meta Layer
The architectural layer responsible for governance, standards, strategy, and the creation of reusable patterns and templates.

## Development Layer
The architectural layer where agents are built, tested, iterated, and formally evaluated before promotion.

## Production Layer
The architectural layer where evaluated and approved agents run in live environments.

## Evidence-Based Output
An output from an agent that includes not just the result, but also supporting reasoning, sources, or justification.

## Governance
The set of rules, processes, and standards that ensure agents behave reliably, stay within boundaries, and produce auditable results.

## Promotion
The process of moving an agent (or workflow) from the Development Layer to the Production Layer after it has passed evaluation.

## Evaluation Criteria
A defined set of standards used to assess whether an agent is ready for promotion. This typically includes quality, governance, performance, and risk dimensions.

## Governor
The top-level strategic orchestrator in a meta-layer fleet. Holds promotion authority, interprets hard rules, and retains long-horizon fleet evolution work.

## Peer Agent
A connected agent at the same level under a governor, without a parent-child hierarchy between peers. Verified in the live runtime graph, not inferred from exports.

## Connected Child
An agent linked to a parent via the platform's connected-agent mechanism. Operates under connected-child framing rules — never addresses end users directly.

## Internal Skill
A skill topic or tool component attached to a parent agent, not a separate connected agent in the runtime graph. Returns structured result blocks for parent integration.

## Handoff Packet
A structured routing artifact with required fields (`SelectedAgent`, `Confidence`, `Reason`, `RequiredInputsMissing`, `InputsReceived`, `ExecutionConstraints`, `RequestedDeliverable`, `PayloadForChildAgent`, `ExpectedReturnContract`). See [templates/handoff-contract.md](templates/handoff-contract.md).

## ChildResult
A structured status block returned by an internal skill to its parent, including result status, confidence, source scope confirmation, blocking issues, and export-safety flags.

## Needs validation
A canonical label for values, relationships, or capabilities not confirmed by authoritative sources. Never treat as firm fact.

## documentationId
A stamped identifier for governance artifacts following the pattern `DOC-AGENT-*`, `DOC-SKILL-*`, or `DOC-GOV-*` with version and date.

## Agent Registry
A canonical record of fleet agent identities, environment context, eval test sets, and verified topology. See [templates/agent-registry.md](templates/agent-registry.md).

## Correct Abstention
When an agent properly refuses out-of-scope work, invents nothing, and routes appropriately. In governance-adjusted evaluation, this is a pass — not a failure.

## Methodology Overlay
An additive governance layer that applies stricter rules to agents in a specific methodology (e.g., challenge-before-build). Never weakens fleet hard rules.