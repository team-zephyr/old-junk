<!-- org-agent-standards:begin version=1.0.2 -->
# Repository guidance

## Working rules

- Establish observable success criteria before editing.
- For bugs, reproduce the failure or identify the failing test first.
- Read the implementation, its callers, and relevant tests before changing it.
- Follow existing architecture and patterns unless the task explicitly changes them.
- Keep the diff limited to the requested outcome; avoid adjacent refactors.
- Do not add production dependencies, change public contracts, or create migrations without identifying the impact.
- Run the smallest relevant verification during iteration, followed by the required final checks.
- Report exact commands and results. Never claim a check passed if it was not run.
- For UI changes, inspect the rendered result and provide before/after evidence.

## Merge requests

- Use the standard sections: Why, What changed, Review focus, Validation evidence, Risk and delivery, and Impact assessment.
- Disclose Claude, Codex, or other agent assistance.
- Identify anything not verified instead of implying completion.
- Do not open, approve, or merge an MR unless the user or workflow authorizes it.
<!-- org-agent-standards:end -->

<!-- project-agent-guidance:begin -->
# Repository Instructions

## GitLab Operations

- Use `glab` for all GitLab interactions: merge requests, reviews, comments, pipelines, and
  GitLab API metadata. Do not use `gh`, browser automation, or raw GitLab HTTP requests unless
  the user explicitly asks for that route.
- Confirm `glab auth status` before a GitLab write. If authentication is unavailable, report the
  blocker rather than falling back to interactive web/OAuth login.
- Never expose or place GitLab tokens in Git, source files, command arguments, or output.

## Repository facts

- Purpose: TODO(REQUIRED)
- Languages and runtime versions: TODO(REQUIRED)
- Frameworks: TODO(REQUIRED)
- Package manager: TODO(REQUIRED)
- Deployment target: TODO(REQUIRED)
- Primary entry points: TODO(REQUIRED)
- Source directories: TODO(REQUIRED)
- Test directories: TODO(REQUIRED)
- Generated or vendored directories: TODO(REQUIRED)
- Load-bearing or security-sensitive areas: TODO(REQUIRED)

## Commands

- Install: `TODO(REQUIRED)`
- Run locally: `TODO(REQUIRED)`
- Build: `TODO(REQUIRED)`
- Test one file or case: `TODO(REQUIRED)`
- Test affected component: `TODO(REQUIRED)`
- Full test suite: `TODO(REQUIRED)`
- Lint: `TODO(REQUIRED)`
- Typecheck: `TODO(REQUIRED)`
- Format: `TODO(REQUIRED)`

Use `N/A — <reason>` for commands that genuinely do not apply. Do not invent commands.

## Architecture and boundaries

- Component ownership: TODO(REQUIRED)
- Allowed dependency direction: TODO(REQUIRED)
- Forbidden dependency direction: TODO(REQUIRED)
- Public compatibility requirements: TODO(REQUIRED)
- Data ownership or tenancy rules: TODO(REQUIRED)

## Repository-specific hazards

- Never modify: TODO(REQUIRED)
- Changes requiring owner or security review: TODO(REQUIRED)
- Common but incorrect implementation: TODO(REQUIRED)
- Known debugging or test-suite traps: TODO(REQUIRED)
<!-- project-agent-guidance:end -->