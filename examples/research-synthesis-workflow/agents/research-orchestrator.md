# Research Orchestrator

> Stub agent definition. Fill out using [../../../templates/orchestrator.md](../../../templates/orchestrator.md).

**Type:** Runtime Orchestrator  
**Layer:** Development

## Role

Coordinates research tasks across Web Research and Document Research agents. Does not perform research itself.

## Specialist Agents

| Agent | Handoff contract |
|-------|------------------|
| Web Research Agent | [web-to-synthesis.md](../handoff-contracts/web-to-synthesis.md) |
| Document Research Agent | [doc-to-synthesis.md](../handoff-contracts/doc-to-synthesis.md) |
| Synthesis Agent | [research-to-synthesis.md](../handoff-contracts/research-to-synthesis.md) |

**Status:** Draft