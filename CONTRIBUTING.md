# Contributing

Agency Agents OS accepts two kinds of contributions: a new sub-agent inside an existing umbrella repo, or a link to a high-quality external agent repository.

## Adding a sub-agent to an existing umbrella repo

1. Open an issue on the relevant umbrella repo proposing the agent — what it does, who it's for, what APIs it needs.
2. Fork the umbrella repo and add a new folder under `agents/<your-agent-slug>/` with a `SKILL.md` following the template below.
3. Describe required inputs, required connections, and the specific API capabilities the agent depends on — using stable capability names (e.g. `media.generate_video`), not internal provider names.
4. If the required APIs are live, test the workflow end-to-end and include an example transcript.
5. Open a pull request. Include the status label you believe applies (see the [status labels](README.md#status-labels)) and why.

## Proposing a new umbrella repo

Only propose a new umbrella when an existing one doesn't fit and the category has real, distinct search volume (e.g. "AI ads agent" is a different search intent than "AI marketing agent"). Open a discussion on `agency-agents-os` first.

## SKILL.md template

```markdown
---
name: Agent Name
slug: agent-slug
version: 1.0.0
category: category-slug
description: One sentence describing the outcome this agent produces.
status: blueprint
required_connections:
  - muapi
---

# Agent Name

## Mission

## Use this agent when

## Required inputs

## Required connections

## Available Muapi capabilities

## Workflow

## Decision rules

## Approval boundaries

## Output format

## Failure and missing-data behavior

## Example interactions
```

## Curation standards

Every accepted agent must have:

- A clear business outcome.
- Specific input requirements and output format.
- Accurate API references — no unsupported capability claims.
- No secrets, API keys, OAuth client secrets, or private data anywhere in the repo.
- Explicit handling of missing data and failed calls.
- A stated permission level (`read-only`, `draft-only`, `requires-approval-to-publish`, or `autonomous-write`) for any action that reads or writes external data.

## Reporting issues

Open an issue on the relevant repo. For anything security-related, see [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
