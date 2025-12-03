# AI Prompt Library for Software Engineers

A curated collection of high-quality prompt strategies for coding, debugging, architectural design, and software engineering workflows.

This repository contains battle-tested prompt patterns for using AI coding assistants (ChatGPT, Claude, GitHub Copilot Chat, etc.) effectively. These prompts help you:

- Get higher-quality answers
- Clarify requirements
- Reduce hallucinations
- Maintain consistent output
- Generate production-ready code
- Improve design, testing, CI/CD, documentation, and security

---

## 📌 Table of Contents

- [Overview](#overview)
- [Core Prompt Strategies](#core-prompt-strategies)
  - [Q&A Guided Discovery](#1-qa--guided-requirement-discovery)
  - [Pros & Cons Trade-off](#2-pros--cons--design-trade-off-analysis)
  - [Stepwise Execution](#3-stepwise-execution-with-keyword-next)
  - [Role-Play Personas](#4-role-play--expert-persona)
  - [Minimal Reproducible Example](#5-minimal-reproducible-example-mre)
  - [Debugging](#6-debugging-checklist)
  - [Code Review](#7-code-review)
  - [Refactoring](#8-refactor-with-beforeafter)
  - [Testing & CI](#9-testing--ci-generation)
  - [API Design](#10-api-design)
  - [Security](#11-security-checklist)
  - [Performance Optimization](#12-performance-optimization)
  - [Commit/PR Generation](#13-commit--pr-messaging)
  - [Pair Programming](#14-pair-programming-mode)
  - [Format/Style Control](#15-output-format-control)
- [Common Scenarios & Copy-Paste Prompts](#common-scenarios--copy-paste-prompts)

---

## Overview

This repository provides AI prompt templates specifically tailored for software engineering tasks.

The prompts follow these principles:

- Clear role instructions
- Explicit output format rules
- Controlled verbosity
- Step-by-step execution with checkpoints
- Visibility of assumptions
- Code with file structure and tests
- Reproducibility and correctness

> Use these prompts in any AI coding tool.

---

## Core Prompt Strategies

Below are the major prompt types with examples and use cases.

### 1. Q&A — Guided Requirement Discovery

Use when the problem is unclear or you want the AI to ask clarifying questions first.

**Prompt Template:**

```
Ask me up to 10 prioritized clarifying questions before producing any solution.
For each question include:

- Type (yes/no, multiple-choice, or short answer)
- Why the question matters
- Acceptable answers
  Wait for my responses before generating code.
```

**Use Cases:**

- Designing new features
- Setting up new services
- Choosing frameworks, libraries, hosting strategies

---

### 2. Pros & Cons — Design Trade-off Analysis

Use for architecture decisions.

**Prompt Template:**

```
Compare the following options: [Option A], [Option B], [Option C].

For each option include:

1. Summary (1–2 lines)
2. Pros
3. Cons
4. Complexity (Low/Medium/High)
5. Risks & mitigations
6. Best use-cases
   Finally, give a recommendation with justification.
```

**Use Cases:**

- REST vs GraphQL vs gRPC
- Monolith vs Microservices
- SQL vs NoSQL
- React vs Vue vs Svelte

---

### 3. Stepwise Execution with Keyword “next”

Use to prevent the AI from jumping ahead.

**Prompt Template:**

```
Break the solution into numbered steps.
After each step, STOP and wait until I say “next” before continuing.
For each step include:

- Goal
- Expected output
- Commands or code that will be produced
```

---

### 4. Role Play — Expert Persona

Use to specify tone, reasoning style, and expected artifacts.

**Prompt Template:**

```
Act as a Senior Software Engineer with 10+ years experience in [technology].

When answering:
- Provide a short rationale
- Provide production-ready code
- Include tests
- Include a short README section
- Provide a one-line commit message
```

---

### 5. Minimal Reproducible Example (MRE)

Use when debugging.

**Prompt Template:**

```
Create a minimal, runnable example demonstrating this bug: [describe issue].
Include:

- File tree
- Source files
- Commands to run
- Sample input & expected output
```

---

### 6. Debugging Checklist

**Prompt Template:**

```
Given the issue: [short summary]
Provide a prioritized debugging checklist with:

- Commands to run
- What to inspect
- Signs of each root cause
- Fix + verification steps
```

---

### 7. Code Review

**Prompt Template:**

```
Perform a code review. Provide:
1. Summary of the code
2. High-priority issues (bugs/security)
3. Medium/low-priority improvements
4. Suggested changes (unified diff)
5. Tests to add
```

---

### 8. Refactor with Before/After

**Prompt Template:**

```
Refactor the code below. Provide:

- BEFORE summary
- AFTER version (full)
- List of changes
- Complexity/comparison
- When NOT to refactor it this way
```

---

### 9. Testing & CI Generation

**Prompt Template:**

```
Generate tests for this code using [test framework].
Include:

- Unit tests
- Edge case matrix
- Integration tests (if relevant)
- GitHub Actions / GitLab CI workflow to run tests
```

---

### 10. API Design

**Prompt Template:**

```
Design REST API endpoints for: [feature].

For each endpoint include:

- Method + URL
- Request example (JSON)
- Response example (JSON)
- Status codes
- Auth
- Error objects
Provide:
- cURL examples
- OpenAPI spec (if requested)
```

---

### 11. Security Checklist

**Prompt Template:**

```
Perform a security review for this system: [description].
List threats with:

- Severity
- Exploit path
- Short-term mitigation
- Long-term recommendations
```

---

### 12. Performance Optimization

**Prompt Template:**

```
Provide a performance tuning plan for: [component].

Include:

- Metrics to measure
- Benchmarks to run
- Profiling tools/commands
- Expected bottlenecks
- 3 optimizations with estimated impact
```

---

### 13. Commit & PR Messaging

**Prompt Template:**

```
Based on this diff:
[Paste diff]

Return:

- One-line commit message
- Commit body (why + impact)
- PR description with checklist
- Changelog entry
```

---

### 14. Pair Programming Mode

**Prompt Template:**

```
Act as my pair programmer.
When I say "implement X":
- Output ONLY code blocks
- Include file paths
When I say "explain":
- Provide a short explanation
```

---

## Common Scenarios & Copy-Paste Prompts

Below are ready-made prompts for real-world situations.

---

### 🚀 Scenario 1: Create a new project from scratch

```
Help me scaffold a new project using [tech stack].
Ask me 6–8 clarifying questions first.
Then provide:
- File structure
- Setup commands
- Base code
- Tests
- README
```

---

### 🧪 Scenario 2: Convert code into production-ready version

```
Take the code below and convert it into a production-ready version, including:
- Input validation
- Error handling
- Logging
- Separation of concerns
- Tests
- Documentation
```

---

### 🐞 Scenario 3: Debugging a crash / error message

```
Here is the error: [paste].
Create a root-cause analysis with:
- What the error likely means
- How to reproduce
- Step-by-step debugging Checklist
- Fix + verification
```

---

### 📦 Scenario 4: Migrate from X to Y

```
Generate a migration plan from [framework X] to [framework Y] including:
- File changes
- API differences
- Risks
- Timeline
- After-migration cleanup
```

---

### 📐 Scenario 5: Architectural decision

```
Act as a senior architect.
Compare these architecture patterns: [list].
Provide pros/cons, risks, complexity, and best recommendation.
```

---

### 🔒 Scenario 6: Security hardening

```
Perform a security audit for my service: [description].
List vulnerabilities, risks, and patch instructions.
```

---

### 🌐 Scenario 7: Generate API documentation

```
Generate full API documentation for the following endpoints.
Include:
- Parameters
- Schemas
- Error formats
- Examples
- OpenAPI 3.1 YAML
```

---

### 🧹 Scenario 8: Clean up messy code

```
Refactor this messy code into clean, readable, testable functions.
Maintain the same behavior.
Show Before → After.
```

---

### 📊 Scenario 9: Add logging, monitoring, metrics

```
Add structured logging, metrics, and recommended observability patterns to this code.
Include which libraries and dashboards to use.
```

---

### 🤝 Scenario 10: Guide a junior developer

```
Explain this concept to a junior developer using simple language, examples, diagrams, and analogies.
```
