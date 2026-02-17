---
title: "Agent SOPs"
position: 4
layout: project
description: "Natural language workflows that guide AI agents through complex, multi-step tasks with consistency and reliability."
links:
  - label: GitHub
    url: https://github.com/strands-agents/agent-sop
---

Agent SOPs (Standard Operating Procedures) are markdown-based instruction sets that transform complex processes into reusable, shareable workflows for AI agents. Using parameterized inputs and RFC 2119 constraint keywords (MUST, SHOULD, MAY), they provide structured guidance that works across different AI systems and teams.

The framework ships with built-in workflows for codebase summarization, prompt-driven development, task generation, TDD-based code assistance, and automated evaluation. It supports multiple deployment modes — as MCP server prompts, Cursor IDE commands, or Anthropic Skills with progressive context disclosure.

My contributions to this project focused on build tooling, release infrastructure, and documentation:

- **Build and test infrastructure** — Set up hatch with testing, linting, and formatting scripts, and updated the release workflow to run tests before publishing to PyPI.
- **Release pipeline fixes** — Fixed packaging issues (missing `utils` in the wheel) and added proper permissions to the PyPI publish workflow.
- **CLI documentation** — Updated the README to clarify how to target MCP prompts across different CLI tools like Claude Code.
