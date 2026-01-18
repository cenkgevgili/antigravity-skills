---
name: antigravity-code-review
description: Reviews code changes according to Antigravity standards. Covers architecture, performance, security, testing, and review communication culture. Use when reviewing PRs or evaluating code quality.
---

# Antigravity Code Review Skill

When reviewing code in Antigravity projects, follow these steps and principles.

---

## Review checklist

### 1. Correctness

- Does the code do exactly what it is supposed to do?
- Are business rules implemented correctly?
- Are error conditions handled explicitly?

---

### 2. Architecture & Clean Code

- Is there any unnecessary duplication (DRY violations)?
- Does each function or class have a single responsibility?
- Are names intention-revealing and unambiguous?
- Are functions small, focused, and readable?
- Is dead or obsolete code removed?

---

### 3. Performance & Scalability

- Are there obvious O(n²) or worse patterns?
- Are database or API calls executed inside loops?
- Are async / I/O operations handled correctly?
- Is pagination or streaming used for large datasets?

---

### 4. Security & Resilience

- Is all user input properly validated and sanitized?
- Are secrets (API keys, tokens, passwords) hard-coded?
- Are errors logged meaningfully rather than swallowed?
- Are authorization checks explicit and enforced?

---

### 5. Testing & Documentation

- Are unit tests added or updated for new behavior?
- Are edge cases covered (nulls, empty lists, invalid input)?
- Do comments explain *why* decisions were made?
- Is documentation updated when architecture changes?

---

## Reviewer skill levels

### Junior Reviewer

- Focuses on readability and basic correctness
- Identifies naming issues and long functions
- Uses `[QUESTION]` and `[NITPICK]` tags

---

### Mid-Level Reviewer

- Identifies SOLID violations and performance risks
- Flags missing edge-case tests
- Uses `[SUGGESTION]` and limited `[BLOCKER]`

---

### Senior Reviewer (Antigravity Standard)

- Evaluates architectural impact and systemic risk
- Identifies technical debt early
- Explains trade-offs clearly
- Writes solution-oriented `[BLOCKER]` comments
- Uses `[KUDOS]` to reinforce good practices

---

## How to provide feedback

- Be specific about what needs to change
- Explain *why*, not just *what*
- Suggest alternatives when possible
- Critique the code, never the person

---

## Reviewer comment tags

- `[BLOCKER]` — Must be fixed before merge
- `[SUGGESTION]` — Recommended improvement
- `[NITPICK]` — Minor, non-blocking issue
- `[QUESTION]` — Clarification only
- `[KUDOS]` — Positive feedback
