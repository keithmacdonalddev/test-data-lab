# Test Data Lab public pages coding-agent harness

## Operational baseline

[OPERATIONAL_CONTRACT.md](docs/agent-harness/OPERATIONAL_CONTRACT.md) is the current authority for shared hook wiring, explicit-request Git closeout, core role definitions, and activation limits. The layer inventory below reflects this baseline.


The harness is the set of instructions and tools used while developing this project. It is separate from product behavior.

## Layer map

| Layer | Location and purpose |
| --- | --- |
| Shared workflow | [AGENT_WORKFLOW.md](AGENT_WORKFLOW.md) — common working contract |
| Project instructions | [AGENTS.md](AGENTS.md) — product, safety, command, and verification rules |
| Claude entry | [CLAUDE.md](CLAUDE.md) — explicit imports of the shared workflow and project guide |
| Project routing and tools | [Project profile](docs/agent-harness/PROJECT_PROFILE.md) — scoped documents, skills, hooks, commands, and known gaps |

## Authority and evidence

Higher-priority platform instructions and the current user request come first. Shared workflow and project rules govern authorized work; current source proves actual behavior. Memory, generated output, and historical reports are supporting evidence only.

Read only relevant procedures. The approved shared baseline supplies the three core roles and hooks; additional domain capabilities should follow this project's needs. Verify loaded instructions and tools in a fresh client session before claiming operational parity.

## Maintenance

Keep the two instruction entry points aligned, update the project profile when commands or wiring change, and preserve dated evidence. Do not commit secrets, raw transcripts, or personal account configuration. Validate changed references and the owned diff before reporting completion.


## Shared core specialists

Both clients define the same optional roles; existing domain specialists remain in place.

| Role | Purpose | Declared permission boundary |
| --- | --- | --- |
| `harness-worker` | Bounded implementation and focused checks | Inherits the parent boundary |
| `harness-reviewer` | Independent correctness and regression review | Codex read-only default; Claude Read/Glob/Grep only |
| `harness-security-reviewer` | Independent security, privacy and integrity review | Codex read-only default; Claude Read/Glob/Grep only |

Definitions are in `.codex/agents/` and `.claude/agents/`. The new files pin no model or reasoning effort. Verify effective permissions and model in the loaded client; parent runtime settings can override Codex sandbox defaults. Availability does not require delegation.
