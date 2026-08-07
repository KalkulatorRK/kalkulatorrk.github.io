# Agent Skills (selected)

Synced from [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) (MIT).

Shared checklists: `/references/` at the repository root.

## Installed (13)

| Skill | Why |
|-------|-----|
| `using-agent-skills` | Meta-routing to the right workflow |
| `interview-me` | Clarify underspecified asks |
| `source-driven-development` | Ground answers in official docs/standards |
| `debugging-and-error-recovery` | Incidents, VPS/Hermes, broken builds |
| `context-engineering` | MCP, packing context, session quality |
| `planning-and-task-breakdown` | Multi-step work into atomic tasks |
| `incremental-implementation` | Thin vertical slices + verify |
| `test-driven-development` | Red-green-refactor when changing behavior |
| `code-review-and-quality` | Pre-merge five-axis review |
| `git-workflow-and-versioning` | Atomic commits, branches |
| `doubt-driven-development` | Adversarial check on high-stakes decisions |
| `frontend-ui-engineering` | HTML/UI work on this site |
| `security-and-hardening` | Auth, secrets, hardening |

Routing rule: `.cursor/rules/agent-skills.mdc`.

## Refresh from upstream

```bash
git clone --depth 1 https://github.com/addyosmani/agent-skills.git /tmp/agent-skills-src
# example: refresh one skill
cp -a /tmp/agent-skills-src/skills/test-driven-development/. .cursor/skills/test-driven-development/
cp -a /tmp/agent-skills-src/references/. ./references/
```
