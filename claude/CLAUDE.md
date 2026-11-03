# Claude Code — shared instruction entry

@${CODEX_HOME_DIR}/AGENTS.md

## Local adapter
- The imported AGENTS.md is the single common contract. Relative guide/review paths resolve from ${CODEX_HOME_DIR}, not the current project.
- Load only the needed skills and references. Native personal skills are under ~/.claude/skills; shared links reuse the installed Codex/agent skill sources.
- Keep the main's configured permissions and existing models, hooks, accounts, and settings. This document does not change runtime permission profiles.
- Use the existing dedicated code-reviewer/ui-reviewer roles only when the common review conditions apply. Their tool restrictions remain in force; a model/effort declaration is not proof of delivery or actual read-only execution.
- code-reviewer retains Read/Grep/Glob only, without Bash/MCP/edit/additional-agent access. The existing scripts/run_code_review.py collector remains a separate, previously unverified execution path until an actual authorized review establishes support, authentication, routing, and permission evidence.
- A reviewer with omitClaudeMd must obtain needed common conditions from the supplied brief and referenced contract, rather than assuming this entry was automatically loaded.
- No model call, login, permission downgrade, or reviewer demonstration is required merely to apply these instruction files.
