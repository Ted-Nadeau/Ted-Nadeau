# Ted Nadeau

Platform architect with 25 years building enterprise software, now focused on ambient AI and personal knowledge systems.

I'm drawn to problems where machines and humans reason *together* —
systems that extend human judgment rather than replace it.

---

## What I'm exploring

### Machine Augmented Reasoning (MAR)

The most interesting near-term AI work is not automation — it's *augmentation*.
The design principle: AI proposes, human decides.
Candidates, not actions. Reviewable artifacts, not autonomous side effects.

LLMs are stochastic — they generate plausible outputs, not provably correct ones.
The natural complement is **formal reasoning**:
[SMT (Satisfiability Modulo Theories)](https://en.wikipedia.org/wiki/Satisfiability_modulo_theories)
solvers — [z3](https://github.com/Z3Prover/z3), [cvc5](https://cvc5.github.io/),
[pySMT](https://github.com/pysmt/pysmt) — are deterministic and complete.
Given a set of constraints, they either find a satisfying assignment or prove none exists.
Where an LLM approximates, a solver *verifies*.

This suggests a layered architecture:
the stochastic layer (LLM) generates candidates,
the constraint layer (SMT / [Amazon Bedrock Guardrails](https://aws.amazon.com/bedrock/guardrails/)) validates them,
and the human layer decides.
Formal methods catch logical inconsistencies that humans miss;
humans catch contextual and ethical failures that formal systems can't express.
Neither replaces the other.

### Graph Neural Networks (GNNs) & Large Relational Models (LRMs)

Learning on structured relational data — knowledge graphs, conversation graphs,
entity networks that evolve over time.
Particularly interested in GNNs as the representation layer for personal memory:
how do you model what you know, who you know, and how ideas connect
across years of conversations?
The knowledge graph is the long game beneath the transcript.

LLMs emerged when transformer architectures were scaled on language.
The analog for relational data is coming:
**Large Relational Models (LRMs)** — foundation models trained at scale on graph-structured
and relational data, capable of emergent relational reasoning the way LLMs exhibit emergent
language reasoning.
GNNs ([PyG](https://pyg.org/), [DGL](https://www.dgl.ai/)) are the architectural primitive;
relational deep learning ([RelBench](https://relbench.stanford.edu/)) and graph foundation models
are early signals of what scale will unlock.
Where LLMs answer *what does this mean*, LRMs will answer *how does this connect*.

### Vibe-Coding Best Practices

AI-assisted development is a genuinely new discipline and most practitioners are still
treating it like autocomplete on steroids.
I've built an opinionated workflow around session orientation, agent memory,
human-in-the-loop review, and document-driven context that makes AI coding tools
reliably useful rather than occasionally impressive.
Working toward making this teachable and shareable.

---

## Current work

### RecordEverything *(coming public)*

A continuous personal memory system.
Passive ambient audio capture → chunked ASR transcription →
listener-driven candidate extraction (tasks, commitments, questions, assertions, decisions) →
searchable, chat-able timeline grounded in source audio.

Local-first. Human-review-gated. Raw audio is immutable ground truth.
Derived artifacts are versioned and traceable back to source timestamps.

*Explores: MAR in practice · listener pipeline architecture ·
conversation microstructure extraction · knowledge graph construction from speech*

---

## Demo projects & experiments

*Small focused experiments — GNN applications, MAR primitives, vibe-coding tooling.*
*Indexing here as they ship.*

<!-- When ready, uncomment and add:
- [project-name](https://github.com/Ted-Nadeau/project-name) — one-line description
-->

---

## Writing & thinking

<!-- Add when you have a blog, newsletter, or notable writing:
- [Post title](url) — brief note on why it matters
-->

*Notes on MAR, GNNs, and AI-assisted development — coming.*

---

## Find me

[LinkedIn](https://linkedin.com/in/tednadeau) &nbsp;·&nbsp;
[Email](mailto:trnadeau@gmail.com)

