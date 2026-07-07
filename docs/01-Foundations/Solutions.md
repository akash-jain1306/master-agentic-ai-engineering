# Solutions

## Concept Check Notes

1. AI engineering turns model capabilities into reliable product behavior using software architecture, evals, observability, and product constraints.
2. LLM output is probabilistic and context-sensitive, so tests must often check behavior quality rather than exact strings.
3. A chatbot responds conversationally; an agentic system can choose actions, call tools, maintain state, and decide whether to continue.
4. Examples include evaluation, retrieval, logging, latency, cost, security, permissions, UX, deployment, and monitoring.
5. Prompts and evals directly shape production behavior and should be versioned, reviewed, and improved like source code.

## Design Drill Sample Outline

```text
Feature: AI study coach
User input: A topic, deadline, current skill level, and available study time
Model instruction: Create a structured study plan and adapt it after each session
State: Goals, completed sessions, quiz results, weak areas, user preferences
Tools: Calendar lookup, flashcard generator, quiz generator, document search
Stop condition: User confirms plan, session ends, or tool budget is reached
Eval examples:
  - Beginner with two weeks to study recursion
  - Intermediate learner revising vector databases
  - User with only 20 minutes per day
```

