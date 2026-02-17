---
title: "Strands Agents SDK (TypeScript)"
position: 2
layout: project
description: "The TypeScript counterpart of the Strands Agents framework — type-safe AI agent development with Zod schemas, streaming, and MCP integration."
links:
  - label: GitHub
    url: https://github.com/strands-agents/sdk-typescript
---

Strands Agents for TypeScript brings the same model-driven agent framework to the Node.js ecosystem. It provides type-safe tool definitions using Zod schemas, real-time response streaming, and flexible conversation management strategies. Built for Node.js 20+, it supports Amazon Bedrock and OpenAI as model providers with an extensible architecture for custom providers.

I was the tech lead for this project — I helped write the initial proposal for the TypeScript SDK and led a team of engineers to design, build, and deliver it for the AWS re:Invent 2025 conference launch. I also bootstrapped the repository using an agentic development system I built, which automated task creation, implementation, and review through GitHub Actions.

Features I shipped directly or through the agent-tasks system:

### Core SDK Foundation

Set up the TypeScript project structure, base model provider interface, AWS Bedrock provider implementation, streaming event aggregation, tool registry, and message/content block type system.

### Multimodal Content

Implemented ImageBlock, VideoBlock, and DocumentBlock content types with support for bytes, S3 locations, URLs, and file IDs across Bedrock and OpenAI providers. Also added GuardContentBlock for guardrail evaluation.

### Event and Hook System

Led a multi-phase initiative to consolidate hook events and stream events into a unified system, adding tool lifecycle events and centralizing hook invocations.

### Testing Infrastructure

Built parameterized integration tests across Bedrock and OpenAI, browser-based testing with Playwright, and comprehensive MCP integration tests covering stdio and HTTP transports.

### Developer Tooling

Built an HTTP request tool, made tool input schemas optional, added a PR review agent triggered by `/strands review`, and generalized model configuration across providers.
