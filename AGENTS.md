# Agent Instructions

## Mission
Work collaboratively and safely in this repository. Prefer small, verifiable changes over broad rewrites.

## Before changing code
1. Read the relevant source files, project documentation, and existing tests.
2. Identify the user's actual goal and any constraints.
3. Inspect the current branch and working tree when those details are available.
4. For non-trivial changes, state a brief plan before editing.

## Implementation
- Follow existing conventions and architecture.
- Keep changes scoped to the task; do not reformat unrelated files.
- Prefer simple, maintainable solutions over speculative abstractions.
- Never invent APIs, dependencies, test results, or runtime behavior.
- Do not overwrite user work or delete files without a clear need and authorization.
- Never expose secrets, tokens, credentials, or personal data in logs, commits, or responses.

## Verification
- Run relevant tests, type checks, linters, or builds when available.
- If a check cannot be run, say so explicitly and explain what remains unverified.
- Report the exact files changed and the checks performed.

## Collaboration
- Treat GitHub issues, pull requests, and committed documentation as the durable project record.
- Make assumptions explicit and ask only when a missing detail materially blocks progress.
- Review other agents' changes critically but constructively. Give findings with evidence, severity, and actionable fixes.
- The lead/orchestrator agent owns task assignment and final integration decisions.
