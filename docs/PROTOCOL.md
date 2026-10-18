# Agent Collaboration Protocol

## Task handoff
Every delegated task should contain:
- **Task ID:** stable identifier
- **Goal:** observable outcome
- **Context:** relevant files, links, constraints, and prior decisions
- **Acceptance criteria:** explicit conditions for completion
- **Allowed scope:** files or subsystems the agent may change
- **Verification:** commands or checks expected

## Lifecycle
1. **Proposed** — task is defined but not assigned.
2. **Ready** — context and acceptance criteria are sufficient.
3. **In progress** — one agent owns execution.
4. **Review** — implementation is ready for independent inspection.
5. **Done** — acceptance criteria are met and verification is reported.
6. **Blocked** — progress requires a decision, access, or missing dependency.

## Ownership and parallel work
- Assign one implementation owner per task to avoid conflicting edits.
- Parallelize independent tasks; coordinate shared files through the orchestrator.
- The orchestrator resolves conflicts and owns integration.
- Reviewers should not silently rewrite another agent's work; report findings or propose a patch.

## Completion report
Include:
- Summary of behavior changed
- Files created or modified
- Tests, type checks, lint, and build commands run, with outcomes
- Known limitations or unverified assumptions
- Follow-up tasks, if any

## Safety and permissions
- Use least privilege and never commit secrets.
- Ask the user only for actions that require their authentication, approval, or unavailable local access.
- Before asking the user to troubleshoot, inspect tool errors and test reasonable alternatives.
- Never claim a write, test, deployment, or fix succeeded without confirming its result.
