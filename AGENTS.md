# AGENTS.md

This repository uses the SNMB workflow as the operating protocol for all future sessions.

Before doing any substantive work, read these files in order:

1. `.codex/workflow/workflow-state.md`
2. `.codex/workflow/project-protocol.md`
3. The latest relevant artifact referenced from `workflow-state.md`

Rules:

- `workflow-state.md` is the source of truth for current step and recovery.
- `project-protocol.md` is the highest-priority workflow protocol for this project.
- Do not report a step complete while placeholders, `TBD`, or missing artifacts remain.
- Preserve the agent roster in `.codex/agents/` and use it as the project-specific subagent baseline.
- All workflow and project documentation must be written in Vietnamese with proper diacritics by default, unless the user explicitly requests another language.

If context is compacted, recover by reading `.codex/workflow/workflow-state.md`, verifying the latest artifacts exist, and resuming from the recorded step instead of restarting the workflow.
