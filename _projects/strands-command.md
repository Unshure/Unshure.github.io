---
title: "Strands Command"
position: 3
layout: project
description: "An agentic execution system that responds to /strands commands in GitHub issues and PRs to automate repository workflows."
links:
  - label: GitHub
    url: https://github.com/strands-agents/devtools/tree/main/strands-command
---

Strands Command is an agentic execution system that brings AI-powered automation directly into GitHub workflows. When users leave `/strands` commands in issue or PR comments, the system triggers specialized agents to perform tasks like implementing features, refining requirements, or generating release notes.

The system operates through a multi-stage GitHub Actions workflow with security built in — read and write operations are isolated in separate jobs, and AWS credentials are temporary and time-limited through OIDC authentication.

I created this project by extracting the GitHub agents from the TypeScript SDK into a standalone, reusable repository for the broader Strands organization. My contributions include:

- **Reusable action architecture** — Simplified the workflow into three composable GitHub Actions (parse-input, agent-runner, finalize) that any repo can adopt without repo-specific setup.
- **Artifact-based data passing** — Replaced output plumbing between workflow steps with artifact uploads, keeping orchestrating workflows simpler.
- **Reviewer SOP** — Added a code review SOP and updated the release notes SOP for consistency across repos.
- **Auth action** — Built a shared authentication action for reuse across the Strands GitHub organization.
- **Conditional finalize step** — Added conditional execution logic so the finalize step handles edge cases cleanly.
