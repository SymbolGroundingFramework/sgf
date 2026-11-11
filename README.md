# Symbol Grounding Framework

**An architecture for representing claims so machines can store them, check them, project them into graphs and tables, and govern what may be done with them.**

The unit is the **predication**, not the sentence and not the triple. The sentence holds several claims and one truth value, so a false sentence cannot tell you which claim failed. A triple has no room for the act that made it a claim. A predication is the smallest unit whose failure can be attributed to it alone — and that single choice determines what a correction can name, all the way up.

Its storage shape is the **synapse**:

```
        ┌──────────────────────────┐
        │  hub: predicate + sense  │
        └──────────────────────────┘
  spokes ── participants, one of fifteen closed roles
        ─────────────────────────────
  rim    ── eight closed dimensions: voice, aspect, mood,
            tense, number, modality, polarity, force
        ─────────────────────────────
  span   ── the source location that lets a reviewer check it
```

One claim in one place, with the address of the evidence attached.

---

## What is in this repository

| | |
|---|---|
| **[THE SYNAPSE](books/SYNAPSE.pdf)** | Volume 1 of the SGF book series. 614 pages, 68 chapters, 13 parts, 11 appendices. *A Predication-Centric Architecture for Knowledge Graphs, Ontology, and Accountable AI.* |
| **[The Synapse — an extraction](THE_SYNAPSE.md)** | ~1,700 words from chapters 6–8. Start here if you want the core idea in five minutes. |
| **[This Architecture Is Yours](THIS_ARCHITECTURE_IS_YOURS.md)** | What is public domain, what is licensed, and why. |

## Status

This is a **specification-first project**. The book is the reference; implementations follow it rather than the reverse.

- **Architecture and specification** — complete, in the book.
- **Reference implementation** — in progress. Not yet in this repository.
- **Earlier material** — the previous five-volume series and the first code are archived at tag `v0-final`. They described an earlier architecture and are superseded.

## Licensing

The architecture — concepts, grammars, protocols and designs — is dedicated to the public domain. Reference code is Apache 2.0. The books and prose remain the author's.

---

*James Lee Stäkelum*
