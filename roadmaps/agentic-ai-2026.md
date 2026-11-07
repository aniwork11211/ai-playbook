# Agentic AI path

Personal study path, reorganized from the 2026 masterclass carousel (@decode_leox). This file is the working copy. The slides are the source, not the thing to reopen.

**Current position:** not started  
**Next action:** topic 1, LLM and API fundamentals  
**Rule for any model:** read this file only. Do the next unchecked item. Then tick it. Do not reload the slide set.

## How this data is stored

The carousel used four different layouts for one path. Each fact is kept here in the layout you will act on.

| Slide type | Kept as | Why |
| --- | --- | --- |
| Cover, about, contents | This header and the phase list | Orientation, read once |
| Lesson pages and code samples | One line per topic, plus the hour budget | You type the code yourself when you reach that topic |
| Checkpoints | Tick boxes | The gate before the next phase |
| Project cards | The project table | The work that proves the topic |
| Learning roadmap | The ordered topic list | The sequence and the time |

Section 19, the cheat sheet, was not in the screenshots. Add it here when you have it. The cover says 16 projects. Nine project cards were visible. Do not invent the missing seven.

## Phases

Prerequisite: basic Python helps. No AI background required.

| Phase | Hours | You are practicing | Done when |
| --- | --- | --- | --- |
| Beginner | 0–70 | LLM APIs, prompting, tool use | The beginner checkpoint is ticked and one beginner project runs |
| Intermediate | 70–190 | Agent loops, memory, knowledge, MCP | The intermediate checkpoint is ticked and one intermediate project runs |
| Advanced | 190–380 | Multi-agent, safety, observability, scale | The advanced checkpoint is ticked and one project has traces, a budget, and an approval gate |

Finish one project in a phase, then move on. Skip a topic you can already do, and leave its box ticked so the next session can see that.

## Study order

Hours are estimates for focused study. Follow this order.

### Beginner · 0–70 h

- [ ] **1. LLM and API fundamentals** (25 h) — token, context window, stop reason, streaming, cost
- [ ] **2. Prompting and structured output** (20 h) — role, stop rules, tool descriptions, JSON, validate before trust
- [ ] **3. Tool use basics** (25 h) — schema, dispatch, return the result, return errors as text

Milestone: an assistant that calls real tools.

- [ ] Explain the difference between a chatbot, a workflow, and an agent
- [ ] Call an LLM API and read its stop reason
- [ ] Define a tool, run it, and return the result to the model

### Intermediate · 70–190 h

- [ ] **4. Agent loop and patterns** (30 h) — loop with a step cap and a token budget; chaining, routing, parallel workers, evaluator
- [ ] **5. Memory and context** (25 h) — short-term messages, working notes, long-term store; trim old turns; keep a tool call and its result together
- [ ] **6. RAG and knowledge tools** (25 h) — retrieval is a tool; cite sources; say when nothing useful was found
- [ ] **7. MCP and integrations** (20 h) — one server, many clients; treat third-party servers as untrusted
- [ ] **8. Evaluation basics** (20 h) — task suite from real requests; score tool choice, not only the final text

Milestone: a tested agent with memory and an MCP server.

- [ ] Write an agent loop with a step budget
- [ ] Manage context with trimming, notes, and memory
- [ ] Expose tools through an MCP server and evaluate the agent

### Advanced · 190–380 h

- [ ] **9. Multi-agent systems** (35 h) — add agents only when subtasks are independent or need different tools
- [ ] **10. Planning and long tasks** (30 h) — checkable steps, pause and resume, idempotent steps, human approval
- [ ] **11. Safety and guardrails** (35 h) — untrusted text, least privilege, approval for irreversible actions, spend caps
- [ ] **12. Observability and debugging** (25 h) — log every step, replay a failed run, classify the failure
- [ ] **13. Deployment and cost** (35 h) — API plus a queue, timeouts, cache, cost per task
- [ ] **14. Frameworks and portfolio** (30 h) — learn the raw loop first; 3–5 projects with traces, evals, and a written failure

Milestone: a safe, observable agent service.

- [ ] Decide when multiple agents are worth the cost
- [ ] Gate risky tools with permissions and human approval
- [ ] Trace, replay, and budget every agent run

## Projects

Build these in order inside the phase. One project is enough to leave the phase. The others stay available.

| # | Phase | Project | Concepts | Difficulty | Outcome | Status |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Beginner | Tool-calling calculator bot | Tool schema, dispatch, results | Easy | Bot that computes via tools | [ ] |
| 2 | Beginner | Info lookup assistant | API tool, error handling | Easy | Answers using live data | [ ] |
| 3 | Beginner | Task extractor | Structured output, validation | Easy | Text turned into validated tasks | [ ] |
| 4 | Beginner | File helper agent | Read-only tools, confirmation | Easy–medium | Safe file search and summary | [ ] |
| 5 | Beginner | Daily planner agent | Multiple tools, loop, limits | Easy–medium | Plan built from calendar data | [ ] |
| 6 | Intermediate | Research assistant | Search tool, citations, loop | Medium | Cited briefs on a topic | [ ] |
| 7 | Intermediate | Support agent with RAG | Retrieval tool, order lookup | Medium | Grounded customer answers | [ ] |
| 8 | Intermediate | Agent with long-term memory | Memory store, summarization | Medium | Assistant that remembers preferences | [ ] |
| 9 | Intermediate | MCP server for your data | MCP tools and resources | Medium | Reusable tool server | [ ] |

Seven further project cards were not in the screenshots. When you have them, add them under Advanced in this table. Do not guess their titles.

## What a future session should do

When ANISH says "continue the agentic path" or "next topic":

1. Find the first unchecked topic or checkpoint above.
2. Teach or build only that item. ANISH types the code. Do not paste a finished project.
3. Tick the box in this file when ANISH can do the checkpoint line.
4. If they ask for a project, take the first unchecked row in the table for the current phase.

Open another playbook file only when the topic needs it:

- MCP work: `C:\Users\ANISH\.claude\skills\mcp-builder\SKILL.md`
- RAG work: `C:\Users\ANISH\.claude\skills\rag-techniques\SKILL.md`
- Which model should help: `C:\Users\ANISH\Documents\ai-playbook\model-routing.md`

## Practice rules

- Type every example. A pasted solution does not count.
- Tick the phase checkpoint before the next phase.
- Keep one project per phase as the proof. Extra projects are optional.
- A loop needs a maximum step count and a token budget.
- Return tool errors as text. Validate arguments before the tool runs.
- Memory can store wrong facts. It must be viewable and deletable.
