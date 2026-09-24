# Test Data Lab public pages agent profile

## Current operational setup

Both clients now have the same three optional core roles and shared SessionStart, UserPromptSubmit and PreToolUse handlers. Git closeout requires an explicit request. See [OPERATIONAL_CONTRACT.md](OPERATIONAL_CONTRACT.md) for the actual coverage and remaining trust/session limits. Project safeguards below remain in force.


Inspected: 2026-09-07. This is the project-specific companion to [the shared workflow](../../AGENT_WORKFLOW.md) and [the harness map](../../AGENT_HARNESS.md). Current source and configuration must be checked before treating a dated inventory as live behavior.

## Purpose

Static public information, privacy, and EULA pages. The application and live-company integrations are in the separate qbo checkout.

## Read only what the task needs

Paths in the following tables are relative to the repository root. Wildcards mean select the relevant existing file; they are not automatically loaded imports.

| Work | Read |
| --- | --- |
| Page structure | index.html; privacy.html; eula.html |
| Agent workflow | AGENT_WORKFLOW.md; AGENT_HARNESS.md |

Codex must explicitly read applicable `.agents/rules/` or scoped `CLAUDE.md` documents listed above; these names do not provide native Codex instruction discovery. Claude loads its own matching rules. A workflow in `.claude/skills/` can be read as a procedure by Codex when relevant, but that does not register a Codex skill or grant its tool permissions.

## Commands and evidence

Verify the current manifest or build configuration before running a command. Placeholders identify a choice to make from the current source. Commands separated by `/` are alternatives, not a single shell command.

| Command | Purpose and boundary |
| --- | --- |
| `git diff --check` | Documentation/whitespace check |
| `git status --short --branch --untracked-files=all` | Check ownership and current branch |

For documentation changes, inspect references, instruction consistency, supported command names, and the owned diff. App builds and live services are not required merely because agent Markdown changed.

## Project safeguards

- Keep the site identity, product claims, privacy statements, and legal wording accurate to the authorized request. Do not silently change substantive legal terms during style or harness work.
- Do not add a database, Node toolchain, provider integration, or QBO credentials merely to match the other apps.
- Check local page links and render changed pages at desktop and narrow width when visible content changes. Publication requires its own authorization.

## Current configuration inventory

Inspected 2026-09-07. This table records files and wiring; trust and actual execution are separate.

| Layer | Contents |
| --- | --- |
| `.agents/skills/` | Not present; read relevant project procedures explicitly |
| `.agents/rules/` | Not present; read relevant project procedures explicitly |
| `.claude/skills/` | Not present; read relevant project procedures explicitly |
| `.claude/rules/` | Not present; read relevant project procedures explicitly |
| `.claude/agents/` | `harness-reviewer.md`, `harness-security-reviewer.md`, `harness-worker.md` |
| `.codex/agents/` | `harness-reviewer.toml`, `harness-security-reviewer.toml`, `harness-worker.toml` |
| Codex shared hooks | `.codex/hooks.json`: SessionStart, UserPromptSubmit, PreToolUse |
| Claude shared hooks | `.claude/settings.json`: SessionStart, UserPromptSubmit, PreToolUse |

## Activation and verification limits

Installed Codex 0.153.4 currently disables this project configuration because the checkout is not trusted. Open the checkout in Codex, review its project trust prompt, then inspect `/hooks` and approve the shared hooks if desired. The verification did not change trust records.

Shared scripts and configuration are checked locally. A fresh Claude session and a Codex specialist invocation were not run in this checkout; their effective permissions and model behavior remain unverified.

Run `node --test scripts/agent-harness/workflow.test.cjs` and `node scripts/agent-harness/verify.cjs` after harness changes. Existing domain specialists, personal permissions, app safeguards and concurrent work remain separate from the shared baseline.

## Session acceptance and maintenance

Start a fresh session in this checkout and ask the agent to identify its root instructions, shared workflow, project safeguards, and the smallest relevant check without editing or starting services. Claude users can inspect `/context` or `/memory`; Codex users should inspect loaded instructions and available skills in their client. Verify hook trust and effective specialist settings separately when a task depends on them. Do not claim this session test passed from file inspection alone.

Update this profile when commands, source layout, risks, or actual harness wiring change. Keep historical evidence dated, personal settings local, and sibling checkouts independent.
