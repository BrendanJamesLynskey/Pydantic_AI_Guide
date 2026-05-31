# Pydantic AI — A Visual Deep Dive

An interactive, single-page visual guide to **Pydantic AI** — the type-safe agent framework from the team behind Pydantic. Covers the full surface, from the first `agent.run_sync()` to durable execution, MCP, observability and evals.

**[View the Live Guide](https://brendanjameslynskey.github.io/Pydantic_AI_Guide/)**

## What's Covered

The guide walks through 15 sections covering Pydantic AI end to end:

- **Overview** — What Pydantic AI is, why the Pydantic team built it, and the "FastAPI feeling for GenAI" pitch
- **Agent Anatomy** — The five things an `Agent` binds together: model, instructions, dependency type, output type, tools — and why the generics matter
- **Defining & Running** — `run` / `run_sync` / `run_stream` / `iter`, the result object, and usage tracking
- **Type-Safe Outputs** — `output_type` with Pydantic models, unions, output functions and `@agent.output_validator`; native vs tool-based structured output
- **Tools & Function Calling** — `@agent.tool` vs `@agent.tool_plain`, docstring-derived JSON schemas, `RunContext`, and tool-level `ModelRetry`
- **Dependency Injection** — Typed `deps_type`, dynamic instructions, and why DI makes agents testable
- **Validation & Self-Correction** — The reflection loop: how validation errors and `ModelRetry` are fed back to the model, and the retry budget
- **Streaming** — Streaming text deltas *and* progressively-validated structured output
- **Models & Providers** — The `'provider:model'` string, the supported-provider matrix, and `FallbackModel` for resilience
- **Messages & History** — Multi-turn conversations, serialising the message log, and history processors
- **Pydantic Graph** — `pydantic-graph` for complex, type-hinted state-machine workflows
- **Durable Execution & MCP** — Temporal / DBOS / Prefect / Restate, MCP client toolsets, human-in-the-loop approval, AG-UI & A2A
- **Observability & Evals** — Logfire + OpenTelemetry tracing, `pydantic-evals`, and offline testing with `TestModel` / `FunctionModel`
- **When to Choose It** — Head-to-head comparison with LangGraph, CrewAI and the OpenAI Agents SDK
- **Live Demo** — Animated execution traces showing the agent loop, a validation retry, and a tool `ModelRetry`

## Features

- Single-file HTML — zero dependencies, zero build step
- Dark theme with animated Canvas hero (network graph)
- Sticky sidebar navigation with scroll-aware active state
- Syntax-highlighted, accurate code examples reflecting the Pydantic AI 1.x API (May 2026)
- Interactive trace viewer demonstrating the self-correction loop
- Fully responsive layout for mobile and desktop
- Designed for GitHub Pages deployment

## Deployment

Push to a GitHub repository with GitHub Pages enabled on the `main` branch. The `index.html` file serves directly — no build process required.

## Built With

Pure HTML, CSS, and vanilla JavaScript. No frameworks, no bundlers, no external dependencies.

## Related Guides

- [Agentic Frameworks Guide](https://brendanjameslynskey.github.io/Agentic_Frameworks_Guide/) — The framework landscape (LangGraph, CrewAI, AutoGen, OpenAI Agents SDK) in which Pydantic AI sits
- [How LLM Agents Work](https://brendanjameslynskey.github.io/LLM_Agents_guide/) — Visual deep dive into the internals of LLM-powered agents
- [Introduction to LangGraph](https://github.com/BrendanJamesLynskey/Introduction_to_LangGraph) — Graph-based agent orchestration with runnable examples
