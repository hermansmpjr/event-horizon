# Agent Folder Structure

Standard layout for agent documentation in an Event-Horizon fleet repository. One folder per agent; governance policies live in `governance/`, not duplicated per agent.

## Canonical Layout

```
agents/<AgentName>/
  <AgentName>.md                    # Passport / catalog entry (governor-reviewed)
  instructions.md                   # System prompt (verbatim)
  connected-agent-description.md    # Short description for platform UI
  greeting-and-prompts.md           # Greeting and suggested prompts
  <AgentName>-eval-conversations.csv  # Platform eval test import (optional)
  knowledge/                        # Agent-specific knowledge files (.gitkeep if empty)
  skills/                           # Per-agent skills (not repo-wide)
  schemas/                          # JSON schemas for handoff/output contracts (.gitkeep if empty)
```

## File Purposes

| File | Contents |
|------|----------|
| `<AgentName>.md` | Role, scope, boundaries, parent/child relationships, provenance |
| `instructions.md` | Full system prompt as deployed in the platform |
| `connected-agent-description.md` | One-paragraph summary for connected-agent picker |
| `greeting-and-prompts.md` | Default greeting and example user prompts |
| `*-eval-conversations.csv` | Test cases for platform evaluation runs |
| `knowledge/` | Curated reference docs indexed or attached to this agent |
| `skills/` | Skill definitions owned by this agent |
| `schemas/` | Handoff packet, output, or intake schemas |

## Rules

1. **One agent, one folder** — Do not split a single agent across multiple top-level paths.
2. **Skills are per-agent** — Repo-wide `skills/` directories are deprecated; colocate skills with their owner.
3. **Governance is centralized** — Hard rules, model/memory policy, and eval rubrics live in `governance/`. Agents reference them; they do not copy them.
4. **Passport before promotion** — Every promoted agent must have a complete `<AgentName>.md` passport before entering the agent registry.
5. **Mark unknowns** — Fields not confirmed by live platform configuration are marked `Not specified in source` or `Needs validation`.
6. **Optional metadata** — `agent.metadata.yaml` may be maintained by the fleet owner for upload workflows; it is not auto-generated.

## Intake-Ready Agents

Agents that accept user requests and produce upward handoff packets carry additional artifacts:

```
agents/<IntakeAgent>/
  ... (standard layout above)
  acceptance-tests.md               # Pre-promotion test checklist
  schemas/intake-handoff-packet.schema.json
```

See the [Intake Handoff Template](../templates/intake-handoff.md) for packet field definitions.

## Related Documents

- [governance.md](governance.md) — Hard rules and evaluation
- [promotion-workflow.md](promotion-workflow.md) — When folder completeness is required
- [templates/agent.md](../templates/agent.md) — Passport content template