# Test Data Lab public pages — agent instructions

## Shared workflow and project routing

Git closeout is explicit-request only: commit and push when the user asks, using existing authorization without repeated confirmation. Project branch, PR, DCO and upstream restrictions still apply. Both tools have optional `harness-worker`, `harness-reviewer`, and `harness-security-reviewer` roles; see [the operational contract](docs/agent-harness/OPERATIONAL_CONTRACT.md).

Read [AGENT_WORKFLOW.md](AGENT_WORKFLOW.md) at task start. It defines the common Codex/Claude working contract. Use [the project profile](docs/agent-harness/PROJECT_PROFILE.md) for task-specific instructions, commands, safeguards, and actual harness availability. Detailed project safety and release rules below remain in force.


This repository contains `index.html`, `privacy.html`, and `eula.html`. It is a static public site, separate from the `qbo` application checkout.

- Read `AGENT_WORKFLOW.md` before work and `docs/agent-harness/PROJECT_PROFILE.md` when choosing checks or changing the harness.
- Preserve the existing HTML/CSS structure unless the user requests a redesign. Keep local links and narrow-screen readability working.
- Do not change substantive legal or privacy commitments as incidental copy cleanup. Research current authoritative sources if a requested legal-content change requires them.
- Use the approved shared development hooks and core roles. Do not add app dependencies, secrets, QBO access, or additional specialists merely for structural symmetry.
- Preserve concurrent changes. Commit, push, and publish only when requested; verify the current branch and upstream first.
- For agent-document edits, validate references and the diff. For page edits, verify links and rendered desktop/narrow layouts. There is no npm test or build script here.

See `AGENT_HARNESS.md` for the coding-agent layer map.
