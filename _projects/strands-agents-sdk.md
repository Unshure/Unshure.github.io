---
title: "Strands Agents SDK (Python)"
position: 1
layout: project
description: "A model-driven framework for building AI agents in Python — from simple chatbots to complex autonomous workflows — with minimal code."
links:
  - label: GitHub
    url: https://github.com/strands-agents/sdk-python
---

Strands Agents is a Python SDK that takes a model-driven approach to building AI agents. It provides the orchestration layer connecting language models, tools, and user interactions so you can go from idea to working agent in just a few lines of code. The SDK supports multiple model providers including Amazon Bedrock, Anthropic, OpenAI, Google Gemini, and Ollama.

I'm a core contributor to this project with 40+ merged PRs spanning major features, bug fixes, and infrastructure.

### Conversation Manager

Designed the conversation manager interface early in the project to allow flexible context window strategies. Implemented the initial sliding window conversation manager and later helped shepherd a community-contributed summarization manager into the project.

### Development Tenets

Defined the development tenets for the project, establishing the guiding principles for contributors and maintainers.

### Structured Output

Helped introduce and flesh out structured output as a feature, enabling agents to return typed, schema-validated responses.

### Agent State

Created the AgentState class for tracking stateful information outside of model context, laying the groundwork for session persistence.

### Session Persistence

Designed and implemented the session management system for persisting agent state, messages, and conversation history across invocations, with pluggable storage backends for local filesystems and S3.
