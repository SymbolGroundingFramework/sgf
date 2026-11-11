# The Synapse

### One claim in one place

A representation has an atom when it has a smallest unit that can be wrong on its own. Most knowledge systems never choose one. They store sentences, documents or rows, and the choice of atom is made for them by whatever the source happened to look like. This essay is about choosing it deliberately, and about the storage shape that follows from the choice.

## The atom is not the sentence

The sentence is the unit prose is written in. It is the wrong unit of representation, for a reason that is easy to state and hard to fix: a sentence can hold several claims and only one truth value.

*The valve was closed and the pump started* is false if either clause is false. If the record is false, the record cannot say which clause failed. A correction must rewrite the sentence — possibly changing its punctuation, its conjunction, its emphasis — rather than the claim. The error is real and its location is not.

Go smaller and the pieces assert nothing. *Bob* cannot be false. *The red book* cannot be false. Terms are not claims; no arrangement of terms becomes a claim until a predicate binds them. A record of terms can be complete and say nothing.

Go larger and claims hold each other hostage. *Bob gave Ava a red book* cannot be wrong about the colour without also being wrong about the giving, because the sentence carries one truth value for both.

So the atom is neither the word nor the sentence. It is the unit whose failure can be attributed to it alone. That is the whole of the criterion.

### The grain test

Three questions decide it:

- Can the unit be true or false **by itself**?
- Can it be corrected **without rewriting a larger unit**?
- Does it **name the act** that makes it a claim?

Only one grain passes all three:

| Unit | Wrong on its own? | Correctable alone? | What it lacks |
|---|---|---|---|
| word | no | no | truth, force, participants |
| phrase | no | no | a complete act |
| clause | sometimes | sometimes | one clause can carry two claims |
| sentence | yes, but for too much | no | several claims share one truth value |
| document | yes, but for everything | no | no isolable unit |
| **predication** | **yes** | **yes** | — nothing required for attribution |

The clause is the closest competitor and it fails for a specific reason: it is a *packaging* boundary, not a semantic one. *Maria opened the window and sat down* contains two predications and one clause. To correct "she did not sit down," the clause must be split before either claim can be corrected. The clause was never the unit. It was the unit of punctuation.

The clause also shifts across languages. A language that packs manner into the verb and one that packs it into a satellite draw different clause boundaries for the same claim, and a record built on clauses inherits the difference. A record built on predications does not.

## The shape

A synapse is the storage shape of one predication.

```
              ┌─────────────────────────┐
              │  hub: GIVE (sense)      │
              └─────────────────────────┘
   AGENT ── Ava        RECIPIENT ── Ben        THEME ── book
              ─────────────────────────────
              rim: voice, aspect, mood, tense,
                   number, modality, polarity, force
              ─────────────────────────────
              span: log-2024-03, p.2, chars 41–96
```

Four parts, each answering a different question:

- **The hub** holds the predicate occurrence and its sense.
- **The spokes** hold the participants and the roles they fill.
- **The rim** holds the dimensions that make the act a claim rather than a relation.
- **The span** holds the source location that lets a reviewer check it.

The hub is the *predicate*, not the grammatical subject. This is the single most consequential decision in the shape. *The technician closed the valve* and *The valve was closed by the technician* are two sentences with one predication. A store keyed on the subject creates two records. A store keyed on the predicate creates one.

A subject-centred store also duplicates the frame onto every spoke, and the copies can disagree. The predicate-centred store has one frame and no copies.

The hub requires a *sense*, not a surface string. *Close* as in shut, *close* as in near, and *close* as in finish are three senses and three hubs. A hub without a sense is an ungrounded relation, and the record should refuse it.

## What the shape buys

One claim in one place is not an aesthetic preference. It changes what a correction can name.

At the sentence level, a correction requires a reviewer to read the sentence, decide which clause is wrong, rewrite it, and re-check the surrounding text. At the predication level, a correction changes one field and re-runs the reconciliation.

A record that stores sentences corrects sentences. A record that stores predications corrects claims. The second can audit the correction. The first can audit only the rewrite.

### The two givings

The failure the claim key prevents is worth seeing directly. Five rows:

```
(give, agent,      Ava)
(give, recipient,  Ben)
(give, theme,      book)
(give, recipient,  Cleo)
(give, theme,      pen)
```

Read these rows and you cannot tell whether Ava gave Ben the book and Cleo the pen, or Ava gave Ben the pen and Cleo the book. The rows are identical under both readings. *What did Ava give?* can be answered by aggregating. *What did Ava give Ben?* cannot be answered without guessing.

With a claim key, the rows attach to two hubs, and the readings separate. The key is not metadata around the relation. It is the relation's identity.

## Open verb, closed frame

A verb may be open. The frame must be closed.

A new predicate enters by adding a sense to the lexicon — not by altering a table. That is what lets the record grow without a migration for every new action.

But if each verb brought its own roles, two claims with different verbs would be incomparable, and comparison is what the record exists to support. So the frame closes in exchange for the verb staying open.

**Fifteen roles.** Each protects a distinction, and the loss column names what disappears if the role folds:

| Role | The job it protects | What is lost if it folds |
|---|---|---|
| AGENT | the intentional initiator | the wind becomes a chooser |
| PATIENT | what undergoes change | a damage claim loses its victim |
| THEME | what is moved, located, possessed | located and broken things collapse |
| EXPERIENCER | who perceives, feels, knows | giving and seeing become one relation |
| RECIPIENT | who receives the transferred thing | the addressee disappears into the beneficiary |
| BENEFICIARY | for whose benefit the act happens | addressee and beneficiary become one claim |
| TIME | when the act occurs | a deadline becomes a date |
| LOCATION | where the act occurs | a path loses direction |
| SOURCE | where a path starts | *from Paris* must be recovered from a preposition |
| DESTINATION | where a path ends | *to Paris* must be recovered from a preposition |
| MANNER | how the act is done | a method becomes a tool |
| INSTRUMENT | with what the act is done | a tool becomes a method |
| CAUSE | the non-choosing trigger | weather becomes an actor |
| REASON | the stated aim | a justification becomes a cause |
| ATTRIBUTE | a property used as a participant | measures and classifications go unrepresented |

**Eight dimensions.** The rim describes the act rather than its participants, and every value set is closed:

| Dimension | Values |
|---|---|
| voice | active, passive, middle |
| aspect | perfective, imperfective, habitual, progressive |
| mood | indicative, subjunctive, imperative, conditional |
| tense | past, present, future, none |
| number | singular, plural, mass |
| modality | actual, possible, necessary, permitted, obligatory |
| polarity | positive, negative |
| force | assertion, definition, directive, commitment, question, hypothesis, attribution, evaluation, fiction |

The dimensions are not tags. A tag is optional metadata; a dimension is a value the claim *must* have. A parse without polarity is not a claim with missing metadata. It is a claim that cannot be evaluated.

### Where the fifteen come from

They do not come from a theory, and it is worth saying so plainly, because readers who know the literature will ask.

Fillmore's case grammar, Gruber and Jackendoff's thematic relations, Davidson and Parsons on events, Dowty's proto-roles — the lineage supplies the *shape*: roles attach to an event or state, and the verb's sense determines which roles are permitted. It does not supply the *number*. No attempt in that history produced a universal inventory of fifteen.

The roster is an engineering set, chosen for comparability, and it is versioned so a later edition can say which fifteen it means. The number is a governance decision, not a discovery.

That has two consequences. A role assignment is a claim about this record's frame, not about universal grammar, and it can be wrong in the ordinary way. And a comparison between two systems is a comparison of rosters, not of languages — two systems can share a roster and disagree about a sentence, and the disagreement is the useful signal.

### The fold test

A request for a sixteenth role is settled by folding. Fold the proposed role into the nearest existing one. If the fold loses a distinction that a question depends on, the role is real. If the fold loses nothing, the role is a sense.

A team building a consent registry wants `CONSENT`. It folds into AGENT for the consenting party and THEME for the consented act. The fold loses the distinction between the consent and the act — but that distinction belongs to a *separate claim*, not to a sixteenth role. So the repair is a new predicate, not a new spoke.

## What the frame cannot hold

The dimensions qualify one act. Some meaning does not.

*Not*, *every*, *must* and *before* relate to more than one act, or bind a variable across acts. These are **operators**, and they need a scope.

Negation is the clearest case. *The valve was not closed because the pump started* has two readings: the valve was not closed, and the pump start is why; or the valve was closed, but not because the pump started. The words are identical. The scope of *not* differs. A `polarity=negative` on the valve claim can represent the first reading and cannot represent the second.

Quantification behaves the same way. *Every student read a book* can mean one book for all students or a book for each. The record needs a variable and a scope, not a single role filler.

So operators are stored as rows — type, operand, scope, warrant — annotated onto a claim or a group. Polarity records the sign. The operator records what the sign applies to. Collapsing them loses the second reading.

The record does not resolve every ambiguity. Where the source does not determine scope, it stores a candidate with a gap, and the gap is a first-class row. The alternative is a silent choice, and a silent choice is the failure the operator layer exists to prevent.

## What this does not claim

The frame is closed so that the vocabulary can stay open. A closed set does not make a comparison *true*. It makes the comparison *possible*, which is the property a record needs before it can argue about truth.

And the atom is independent of the storage technology. A predication can be a row in a relational table, a node in a graph, a document in a store. The storage choice affects performance and projection. It does not affect what counts as one claim.

The atom is a predication. The synapse is its encoding.

---

*Extracted from **THE SYNAPSE**, Volume 1 of the Symbol Grounding Framework Book Series — chapters 6, 7 and 8. The full argument, with projections into property graphs, RDF, and the conformance ladder, is in the book.*
