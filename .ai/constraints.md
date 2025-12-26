# Constraints (Hard Rules)

These are non-negotiable constraints.
If a request violates any rule below, STOP and ask for clarification.

---

## 1. Behavioral Constraints

- Do NOT change existing behavior unless explicitly instructed.
- Do NOT introduce breaking changes silently.
- If a change alters runtime behavior, CALL IT OUT clearly.
- If uncertain about behavior impact, list assumptions first.

---

## 2. API & Contract Constraints

- Do NOT change public APIs (function signatures, HTTP endpoints, MQTT topics, payload schemas) without explicit approval.
- Do NOT rename exported symbols without justification.
- Backward compatibility is preferred over elegance.

---

## 3. Dependency Constraints

- Do NOT add new dependencies unless:
  - The benefit is clearly stated
  - Alternatives are considered
  - The dependency is actively maintained
- Prefer existing libraries already used in the repo.

---

## 4. Code Change Scope

- Prefer minimal, localized changes.
- Avoid refactoring unrelated code.
- Avoid touching more files than necessary.
- If a large refactor is needed, propose a plan FIRST — do not execute immediately.

---

## 5. Testing & Verification

- Do NOT claim something “works” without a verification method.
- Every change must include at least one of:
  - Test updates
  - A reproducible manual verification command
  - Clear runtime validation steps

---

## 6. Performance & Load Testing (if applicable)

- Do NOT optimize prematurely.
- Do NOT change performance-critical paths without measurements.
- When discussing performance, always specify:
  - Throughput
  - Latency (p95 / p99)
  - Test environment assumptions

---

## 7. Logging & Observability

- Do NOT log secrets, tokens, or PII.
- Prefer structured logs over console prints.
- Any new log must justify:
  - Why it exists
  - Expected debugging value

---

## 8. Security Constraints

- Assume untrusted input by default.
- Avoid insecure defaults.
- Do NOT weaken authentication, authorization, or validation logic.
- If security implications exist, call them out explicitly.

---

## 9. Documentation & Decisions

- If a change affects architecture or long-term behavior:
  - Update `.ai/decisions.log.md`
- Do NOT override documented decisions without recording a new one.

---

## 10. Output Requirements (AI Response Rules)

When responding:
1. State what will change
2. List files affected
3. Highlight risks or edge cases
4. Provide code or config
5. Provide verification steps

If any constraint blocks progress, ASK before proceeding.
