# Repository Instructions

## GitLab Operations

- Use `glab` for all GitLab interactions: merge requests, reviews, comments, pipelines, and
  GitLab API metadata. Do not use `gh`, browser automation, or raw GitLab HTTP requests unless
  the user explicitly asks for that route.
- Confirm `glab auth status` before a GitLab write. If authentication is unavailable, report the
  blocker rather than falling back to interactive web/OAuth login.
- Never expose or place GitLab tokens in Git, source files, command arguments, or output.
