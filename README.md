# Duet — Personal Alignment

**Teaching AI how to think *with* you — not just *for* you.**

---

Most alignment research operates at the species level — safety, harmlessness,
helpfulness. Some operates at the organization level — brand voice, tool
policies, workflow rules.

This project operates at a third level: **personal alignment** — teaching AI
your worldview, your reasoning patterns, and how to collaborate with you as a
long-term intellectual partner.

This is not personalization ("the user prefers concise answers"). This is
alignment in the deeper sense: teaching AI what makes an argument convincing
to you, when to push back on your assumptions, and how to build on your
thinking instead of just responding to it.

## Why This Exists

The best human collaborations aren't built on instructions. They're built on
shared ways of seeing. A great research partner doesn't follow directions —
they understand *how you think*, challenge your blind spots, and contribute
from a shared intellectual foundation.

Current AI systems can't do this. Not because they lack capability, but
because no one has tried to teach them. System prompts tell AI *what to do*.
This project teaches AI *how to think alongside a specific person*.

## Architecture

The alignment document is structured in four layers. Each layer changes at a
different rate — deeper layers provide stability, surface layers provide
adaptability:

| Layer | Contains | Changes |
|-------|----------|---------|
| **1. Worldview** | Epistemological foundation — how you understand problems and construct arguments | Rarely |
| **2. Principles** | Core thinking patterns — first principles, theory-grounded reasoning, recursive self-application | Occasionally |
| **3. Interaction Model** | Collaboration dynamics — co-creation over delegation, slow thinking, productive disagreement | Moderately |
| **4. Examples** | Behavioral anchors — correct/wrong pairs that define boundaries, not just targets | Frequently |

This is [pace layering](https://jods.mitpress.mit.edu/pub/issue3-brand/release/2)
(Brand, 1999) applied to human-AI alignment. The structure holds coherent
while the content evolves through use.

### The Learning Loop

Every substantive conversation is an opportunity to refine the alignment.
The companion skill (`alignment-learn`) analyzes what happened, extracts
findings against a structured checklist, routes each to the appropriate
layer — and changes nothing without human approval.

Over time, your alignment document accumulates the residue of every
meaningful collaboration — not as a log, but as distilled principles and
sharpened examples.

## Key Ideas

Three ideas in this project that may be useful beyond this specific
implementation:

### Mentorship over Programming

As models grow more capable, procedural instructions ("check these 4 items,
then do X") become increasingly suboptimal. Principles ("here's how to think
about this class of problem") scale with capability — they let the AI apply
judgment rather than follow scripts.

The litmus test: *does the instruction leave room for judgment, or does it
prescribe the action?* "Comparison → table" is a rule disguised as a
principle. "What form would make the right answer visually obvious?" is a
genuine principle — it teaches the thinking, not the output.

### Recursive Self-Application

The design philosophy must apply to the design process itself. If the product
teaches principle-based thinking, the instructions should be principles, not
procedures. If the product rejects arbitrary constraints, the development
process should too.

This prevents a common trap: building a principled product through an
unprincipled process.

### Rejected Alternatives Are Knowledge

Document what was considered and rejected, and why. This prevents circular
re-proposals across sessions and preserves institutional memory. A rejected
idea with a clear rationale is more valuable than an accepted idea without
explanation.

## Intellectual Lineage

The worldview layer draws from the Carnegie Mellon School of Design
tradition — design understood as a **liberal art** for a technological
culture, not a 5-step innovation process.

This tradition treats design as rhetorical: constructing arguments about how
things *ought to be*, not descriptions of how they are. Every design decision
is an argument — it should be defensible and grounded in theory.

Key references:
- Buchanan, R. (1992). "Wicked Problems in Design Thinking." *Design Issues*, 8(2), 5–21.
- Buchanan, R. (2001). "Design Research and the New Learning." *Design Issues*, 17(4), 3–23.
- Rittel, H. & Webber, M. (1973). "Dilemmas in a General Theory of Planning." *Policy Sciences*, 4(2), 155–169.
- Brand, S. (1999). *The Clock of the Long Now*. Basic Books.

## Getting Started

### 1. Fork or clone this repo

```bash
git clone https://github.com/woody-design/duet-personal-alignment.git my-alignment
cd my-alignment
```

### 2. Fill in the alignment template

Edit `alignment/SKILL.md` — the template guides you through each layer
with questions to help you articulate your worldview, principles, interaction
preferences, and behavioral examples.

Start with whatever you know. The document will evolve through use — that's
the design.

### 3. Set up the learning skill

Edit `alignment-learn/SKILL.md` — customize the extraction checklist to
match the categories that matter to your thinking.

### 4. Install as agent skills

Both skills are discovered under `~/.codex/skills/`. Symlink from your repo:

```bash
ln -s /path/to/my-alignment/alignment       ~/.codex/skills/my-alignment
ln -s /path/to/my-alignment/alignment-learn  ~/.codex/skills/my-alignment-learn
```

Compatible with any AI coding agent that supports skills — including
[Claude Code](https://docs.anthropic.com/en/docs/claude-code),
[Cursor](https://cursor.sh), [Codex](https://openai.com/index/codex/),
and other agents using `~/.codex/skills/`.

### 5. Use and evolve

**Enter deep collaboration mode** at the start of a session:

```
@my-alignment [topic or question]
```

**Capture learnings** when a conversation surfaces insights worth preserving:

```
@my-alignment-learn learn from this session
```

The learning skill generates a layered proposal and waits for explicit
approval before changing anything.

## License

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) — use freely,
give credit, share improvements under the same terms.

---

*By [Woody Li](https://github.com/woody-design) — designer & AI cocreator.*
