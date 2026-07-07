# Foundations

AI engineering is the discipline of turning model capabilities into reliable software systems. The model is important, but it is only one component. A useful AI product also needs input handling, prompt or instruction design, tool access, retrieval, memory, evaluation, observability, security, cost control, and a user experience that handles uncertainty honestly.

## From Software Engineering to AI Engineering

Traditional software usually behaves deterministically: the same code and same input produce the same output. AI systems often behave probabilistically: the same input may produce different acceptable outputs, and correctness can depend on context, user intent, and downstream consequences.

That changes how you build:

- You test behavior with examples, fixtures, metrics, and human review.
- You design for graceful failure instead of assuming perfect output.
- You log inputs, outputs, tool calls, latency, and costs.
- You treat prompts, schemas, retrieval data, and evals as production assets.

## The AI Feature Lifecycle

Most AI features move through these stages:

1. Define the user outcome.
2. Choose the model and system boundaries.
3. Design prompts, schemas, and tool contracts.
4. Build a thin prototype.
5. Create evaluation cases.
6. Add guardrails, retries, and fallbacks.
7. Instrument traces, cost, and latency.
8. Ship gradually.
9. Monitor real failures.
10. Improve through eval-driven iteration.

## Agentic Systems

An agentic system is software that can use a model to decide what to do next. Most useful agents are not magical autonomous beings. They are controlled systems with loops, state, tools, permissions, stop conditions, and observability.

A basic agent loop looks like this:

```text
observe -> reason -> act -> observe result -> continue or stop
```

The engineering challenge is not making the loop exist. The challenge is making it bounded, useful, debuggable, and safe.

## Common Failure Modes

- The model gives plausible but false answers.
- The model ignores an instruction under pressure from user input.
- Tool arguments are malformed or unsafe.
- Retrieval returns irrelevant context.
- The system has no way to tell whether an answer is good.
- Costs or latency grow without visibility.
- The product trusts model output in places that require verification.

## Core Principle

Treat AI output as a component of a larger system, not as the system itself.

