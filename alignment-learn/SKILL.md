---
name: my-alignment-learn
description: "Analyze a conversation transcript and propose structured updates to the alignment skill. Use when a conversation surfaces insights worth preserving."
argument-hint: "[transcript path or 'learn from this session']"
---

# Alignment Learning Protocol — Template

A learning protocol for extracting insights from high-quality conversations
and proposing structured updates to your alignment document.

---

## How to Use

Invoke this skill with a conversation transcript:

- A file path to an agent transcript (`.jsonl` or text)
- Pasted conversation content
- "Learn from this session" (analyze the current conversation)

---

## Process

### Step 1: Read

Read the full transcript. Skim first for overall shape, then read closely
for moments of insight, disagreement, and principle formation.

### Step 2: Read Current Alignment

Read your current alignment document to understand what's already captured.
Compare, don't duplicate.

### Step 3: Extract — Structured Checklist

Answer each question systematically:

1. **New principles?**
   Did the conversation surface a thinking pattern not yet captured in
   Layer 2? What's the principle? What evidence supports it?

2. **Deepened existing principles?**
   Was an existing principle applied in a new way that reveals deeper
   understanding? Should its description be expanded?

3. **Rejected alternatives?**
   Were ideas proposed and explicitly rejected? What was the reasoning?
   These prevent future re-proposals.

4. **Worldview evolution?**
   Did the conversation expand or refine your understanding of your own
   epistemological foundation?

5. **New interaction patterns?**
   Did the conversation demonstrate a collaboration dynamic worth
   codifying in Layer 3?

6. **New interaction examples?**
   Was there a moment that exemplifies desired AI behavior better than
   current examples in Layer 4?

7. **New theoretical references?**
   Did any insight map to a named theory? Include the full academic
   citation.

8. **Contradictions?**
   Does anything contradict an existing principle? Flag explicitly —
   contradictions are the most valuable signals.

### Step 4: Route Updates by Layer

Different layers change at different rates. Apply the right bar:

| Layer | Change frequency | Bar for update |
|-------|-----------------|----------------|
| **1. Worldview** | Rarely | Only when a fundamental understanding shifts. Requires strong evidence. |
| **2. Principles** | Occasionally | New principles need clear evidence. Refinements are more common than additions. |
| **3. Interaction model** | Moderate | New patterns emerge as you work on different types of problems. |
| **4. Examples** | Most frequent | Better examples should replace weaker ones. Low bar — the best example wins. |

### Step 5: Present Proposal

Format the proposal as follows:

```markdown
## Proposed Updates

### Layer 1 (Worldview)
[No changes / Specific proposed edit with rationale]

### Layer 2 (Principles)
[No changes / New principle with evidence / Refinement with rationale]

### Layer 3 (Interaction Model)
[No changes / New pattern with evidence]

### Layer 4 (Examples)
[No changes / New example replacing Example X, with the conversation
excerpt that demonstrates it]

### Rejected Alternatives to Document
[Ideas proposed and rejected, with reasoning]

### New References
[Academic citations for new theoretical connections]

### Contradictions Found
[Conflicts with existing principles — flag for decision]
```

After presenting, **wait for explicit approval** before making any edits.

---

## Rules

- **Never auto-modify** the alignment document — always present the
  proposal and wait for approval.

- **Preserve existing principles** unless explicitly asked to revise.
  New information refines; it doesn't automatically replace.

- **Flag contradictions prominently** — present them as decisions to
  make, not errors to fix.

- **Maintain academic rigor** — when an insight maps to a theory,
  include the full reference.

- **Be honest about uncertainty** — if unsure whether something is a
  new principle or a situational decision, say so.
