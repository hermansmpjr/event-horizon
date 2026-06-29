# Best Practices

This document captures key best practices for building and governing multi-agent systems using the Event-Horizon IDEA framework.

## 1. Start with Clear Boundaries

One of the most common sources of problems in multi-agent systems is unclear responsibility.

**Best Practice:**
- Define explicit boundaries for every agent using the [Agent Definition Template](templates/agent.md).
- Clearly document what an agent **should** and **should not** do.
- Use [Handoff Contracts](templates/handoff-contract.md) to make expectations between agents explicit.

## 2. Use the Orchestrator Pattern Intentionally

Not every workflow needs a complex orchestrator, but when coordination is required, do it deliberately.

**Best Practice:**
- Use a dedicated orchestrator when work needs to be broken down, routed, or sequenced across multiple agents.
- Keep orchestrators focused on **coordination**, not deep specialist work.
- Define clear routing logic and escalation rules.

## 3. Make Handoffs Explicit

Implicit handoffs are a major source of bugs and inconsistent behavior.

**Best Practice:**
- Always define handoff contracts between agents.
- Specify required inputs, expected outputs, and success criteria.
- Treat handoffs as first-class design artifacts.

## 4. Evaluate Before You Automate

Moving agents into production too early is risky.

**Best Practice:**
- Use structured evaluation (see [Evaluation Criteria Template](templates/evaluation-criteria.md)) before promoting agents.
- Define clear quality, governance, and performance criteria.
- Only promote agents that meet defined thresholds.

## 5. Separate Innovation from Production

Mixing experimental work with production systems creates instability.

**Best Practice:**
- Keep experimental or high-risk work in the **Development Layer**.
- Only move agents to the **Production Layer** after they have been properly evaluated.
- Use the **Meta Layer** to manage standards and patterns, not to run experimental agents.

## 6. Design for Observability

You cannot govern what you cannot see.

**Best Practice:**
- Ensure agents produce traceable outputs (reasoning, sources, decisions).
- Log important handoffs and decisions.
- Make it possible to reconstruct why an agent made a particular decision.

## 7. Iterate Using the IDEA Cycle

Do not treat agent development as a one-time effort.

**Best Practice:**
- Regularly cycle through **Innovate → Develop → Evaluate → Automate**.
- Use feedback from production to drive new innovation.
- Treat your agent fleet as a living system that needs ongoing attention.

## 8. Keep Agents Focused

Overly broad agents tend to be less reliable and harder to govern.

**Best Practice:**
- Prefer narrower, well-scoped specialist agents over large generalist ones.
- Use orchestrators to coordinate multiple focused agents rather than making one agent do everything.

## 9. Document Decisions

Future you (and others) will thank you.

**Best Practice:**
- Document why agents were designed a certain way.
- Record evaluation results and promotion decisions.
- Maintain living documentation alongside your agents.

## 10. Balance Rigor with Pragmatism

Governance and structure are important, but over-engineering can slow you down.

**Best Practice:**
- Apply more rigor to high-stakes or frequently used agents.
- Use lighter processes for low-risk or experimental work.
- Evolve your level of rigor as the system matures.

---

These best practices are derived from real experience building and maintaining multi-agent systems. They are intended to be practical rather than theoretical.