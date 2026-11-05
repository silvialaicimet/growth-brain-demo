---
name: legal-check
description: Apply when checking marketing copy, website text, sign-up flows, consent wording, AI assistant conversations or agency proposals against consumer and energy regulation before they go public. Also apply when someone asks "is this compliant", "what does the law say about", or "what do we need from Legal".
---

# Legal check

This skill flags regulatory risk and prepares questions for counsel. It is **not legal advice and never a legal sign-off**. The legal owner signs off.

## Sources (load only what the task needs)
Reference files live in `${CLAUDE_PLUGIN_ROOT}/skills/legal-check/references/`. In this demo there is one placeholder that shows the format: each file covers one body of rules, states its status (official text, translation, AI-extracted, reviewed by counsel) and gives every rule a row ID.

**Precedence.** A briefing reviewed by the legal team outranks AI-extracted files. Where two rows conflict, follow the reviewed one and name both row IDs in the finding.

## How to check
1. **Identify what is being checked and its domain:** marketing, sign-up, billing, customer contact, AI assistant channel, or cross-cutting.
2. **List the touchpoints** in the item: each screen, message, decision, data field, automated step and hand-over.
3. **Match each touchpoint to rules** in the reference files. Always test these, because they recur:
   - Is the customer told they are dealing with an AI?
   - Is there a significant automated decision? If so: a valid legal ground, a human review route, and an explanation of the logic.
   - Can the customer reach a person at any point?
   - Distance contract: pre-contract information, confirmation, withdrawal period.
   - Vulnerable customers: identification, protections, information duties.
   - Marketing and comparisons: price claims, no misleading omissions, no dark patterns, no pre-ticked consents.
4. **Rate each finding:**
   - **Blocker:** a rule stated clearly in a source, and the item breaks it.
   - **High:** likely breach or missing control on a significant decision or right.
   - **Medium:** missing information, wording or record that is probably needed.
   - **Check:** unclear, needs counsel.
5. **Cite precisely:** reference-file row ID, law and article. If a point is not in the references, say "not in loaded sources" instead of answering from memory.

## Output
Findings table: Severity, Item and touchpoint, Rule (ID, law, article), What is wrong or missing, Suggested fix, Question for counsel. Then three short lists: what looks fine, questions for counsel, and sources not covered.

## Rules
- Never invent an article, deadline, fine or quote.
- A finding based only on an AI-drafted source is at most "High" and always gets a question for counsel.
- Flag every reference whose recheck date has passed.
- No em dashes. Plain English.
