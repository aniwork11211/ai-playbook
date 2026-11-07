# AI agent mind map

From idea to production. Names below are the ones on the map. Tick a box when you can use that piece in a build.

**Next:** The agent loop

A future session opens this file from `C:\Users\ANISH\Documents\ai-playbook\LIBRARY.md` and reads only the section the task needs. The hour-by-hour practice path stays in `C:\Users\ANISH\Documents\ai-playbook\roadmaps\agentic-ai-2026.md`.

## The agent loop

Perceive, plan, act, observe, reflect. If the goal is not done, loop.

- [ ] Perceive — read the goal and the context
- [ ] Plan — choose the next step
- [ ] Act — call a tool or an API
- [ ] Observe — read the result; goal met, or retry
- [ ] Reflect — respond to the user; if not done, loop again

Stop when the goal is met, max steps hit, the token budget is spent, or a human says stop.

## Planning

- [ ] Plan and execute
- [ ] ReAct
- [ ] Tree of Thoughts

## Reflection

- [ ] Self critique
- [ ] Verifier model
- [ ] Retry and feedback

## Memory

- [ ] Short-term (context)
- [ ] Long-term (vector)
- [ ] Episodic (past runs)
- [ ] Semantic (facts)
- [ ] Procedural (skills)
- [ ] Shared (multi-agent)

## Agent types

- [ ] Coding agents
- [ ] Research agents
- [ ] Computer-use agents

## Build stack

- [ ] Models — Claude, GPT, Grok, Gemini, Llama, Qwen
- [ ] Vector stores — Pinecone, Chroma, Weaviate, pgvector
- [ ] Memory layers — Zep, Letta, Mem0
- [ ] Code sandboxes — E2B, Daytona
- [ ] Browser tools — Browser Use, Stagehand
- [ ] Agent runtime — Bedrock AgentCore, Vertex AI Agent Engine, Modal, Kubernetes

## Frameworks

- [ ] Open source — CrewAI, LangGraph, AutoGen
- [ ] Vendor SDK — OpenAI Agents SDK, Claude Agents SDK, Google SDK, AWS Strands Agents
- [ ] Low-code — n8n, Dify, Flowise, Langflow

## Tools and protocols

- [ ] MCP
- [ ] A2A (Agent2Agent)
- [ ] Function / tool calling
- [ ] Code execution
- [ ] Web search and browsing

## Orchestration

- [ ] Supervisor / workers
- [ ] Handoffs (swarm)
- [ ] Parallel fan-out

## Ops and safety

- [ ] Observability — LangSmith, Arize Phoenix, OpenTelemetry
- [ ] Evaluation — DeepEval, Ragas, Promptfoo, LLM-as-Judge
- [ ] Guardrails — NeMo Guardrails, Llama Guard, Guardrails AI
- [ ] Security — least privilege, injection defense, audit logs, PII redaction, secrets vault

## Failure modes and fixes

- [ ] Infinite loops — max steps and a stop rule
- [ ] Wrong tool calls — clear tool names and schemas
- [ ] Context overflow — summarize and trim history
- [ ] Runaway cost — token and step budgets
- [ ] Prompt injection — treat tool output as data

## Implementation roadmap

Discover, then build, then pilot, then scale.

### Discover

- [ ] Use case and ROI

### Build

- [ ] Prototype
- [ ] Tool integration
- [ ] Eval suite
- [ ] Guardrails

### Pilot

- [ ] Shadow mode

### Scale

- [ ] Monitor
- [ ] Iterate

## Success metrics

- [ ] Task success rate
- [ ] Cost and latency per task
- [ ] Human escalation rate
- [ ] Tool-call accuracy

## Agentic RAG

- [ ] Query routing
- [ ] Corrective RAG

## Human-in-the-loop

- [ ] Approval gates
- [ ] Interrupt and resume
