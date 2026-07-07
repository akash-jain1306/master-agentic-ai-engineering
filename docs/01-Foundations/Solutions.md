# Solutions

These are reference answers. Your wording can differ if the reasoning is sound.

## Concept Check Notes

1. ChatGPT created a platform shift because it combined broad foundation-model capability with instruction following, conversational access, useful behavior, and developer APIs. Earlier systems were powerful but usually narrower, harder to access, or less general as software interfaces.
2. An LLM application uses a model as part of a product. A copilot assists a human who remains in control. An agent uses a loop to choose actions, call tools, observe results, and continue toward a goal.
3. An LLM alone does not provide private data access, durable memory, permissions, tool execution, evals, observability, deployment, or product UX.
4. Context is working memory because it is the information currently visible to the model during generation.
5. Tools let the model affect external systems: search, calculate, run code, query databases, open files, create tickets, or send messages.
6. Memory lets the system store useful information across time and reintroduce it later.
7. An evaluation harness measures behavior across examples so teams can detect regressions and improve quality.
8. Full autonomy is often unsafe because real systems involve money, privacy, legal risk, customer trust, and irreversible actions. Human approval reduces blast radius.

## Misconception Notes

### "Agents are just prompts."

Prompts are instructions. Agents also require state, tools, control flow, permissions, observations, stop conditions, and traces.

### "RAG solves hallucination."

RAG can reduce unsupported answers by providing relevant context, but retrieval can fail. The system still needs citations, verification, evals, and fallback behavior.

### "Bigger models are always better."

Bigger models may be more capable, but they can be slower, more expensive, and still wrong. Task design, retrieval quality, tools, and evals often matter more.

### "A framework is required to build agents."

A basic agent loop can be implemented with ordinary code. Frameworks help manage complexity, state, orchestration, and integrations.

### "If the model is good enough, we do not need evals."

Models change, prompts change, data changes, and user behavior changes. Evals are how teams preserve quality over time.

## Mini Project Solution Outline

A strong submission should:

- Compare products by architecture layer, not marketing category.
- Clearly mark assumptions.
- Explain context sources such as files, chat history, repository state, uploaded documents, issue text, or web results.
- Describe tools as capabilities with permissions, not vague magic.
- Include risks such as stale context, incorrect tool use, hallucinated citations, unsafe file edits, privacy exposure, and over-trust.
- Include metrics such as answer acceptance, edit acceptance, task success, latency, cost, tool failure rate, user corrections, and regression eval scores.

