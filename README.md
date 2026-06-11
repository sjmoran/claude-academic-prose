# claude-academic-prose

A Claude Code skill for writing academic paper prose that survives editorial triage.

Most paper-writing tools help you *produce* text. This one constrains *how the text is allowed to be written*, on the theory that editors and reviewers judge a paper in under two minutes by two surface signals: whether the prose reads like a careful human academic, and whether the claims can be checked against the evidence quickly. The skill encodes both as hard rules.

## Install

```
/plugin marketplace add sjmoran/claude-academic-prose
/plugin install academic-prose@claude-academic-prose
```

The skill then triggers automatically on any paper-prose request ("tighten the abstract", "write the intro", edits to `.tex` files), and runs a pass/fail pre-submission self-check before any draft is declared done.

## What it enforces

**1. Voice — plain-empirical.** A register distilled from a corpus of published empirical-IR papers: one claim per sentence, flat "We X" declarative abstracts, problem-first openings, deflated definitions ("A topic model is simply a probability distribution over the vocabulary"), intuition stated beside every piece of formalism, limitations raised mid-argument rather than quarantined. Synthetic exemplar sentences ship with the skill.

**2. Anti-screening.** Named constructions that pattern-match to LLM-generated text are banned and rewritten on sight: em-dash chains, rhetorical inversion, the not-X-but-Y pivot, triadic drama ("It unifies. It predicts. It transfers."), aphoristic titles, intensifier adverbs (crucially / notably / remarkably / surprisingly), stacked parenthetical hedges. The test: any sentence that sounds like a keynote slide or ad copy gets rewritten flat.

**3. Evaluability.** Structural rules that make the claim→evidence path walkable in thirty seconds: a numbered claims box closing the introduction, each claim pointing to the section and table that tests it; one protocol per headline number (variants live in ablations; the significance-tested number is always the headline); abstracts ≤160 words with at most one number per claim and zero parentheticals; caveats consolidated into two structural homes rather than interleaved — relocation, never deletion.

**4. Pre-submission self-check.** Eight items, reported pass/fail explicitly before any draft is called finished.

## Example

Before (violates the rules six ways):

> It's not just smoothing — it is a fundamentally different estimator. Crucially, our remarkably simple approach unifies. It predicts. It transfers. We evaluate on two collections and, surprisingly, find improvements of 4.2% MAP (p<0.05, paired t-test, but also 5.1% under a different split…).

After:

> We study a smoothed estimator of the relevance model for retrieval with sparse queries. The estimator interpolates the normalised query distribution with a corpus background model, and we show that it reduces to Dirichlet smoothing under a particular choice of the interpolation weight. We analyse the behaviour of the estimator on the TREC-8 ad-hoc retrieval task. Our experiments show an improvement of 4.2% MAP over the baseline, significant under a paired t-test at the 0.05 level. The main contribution of this work is an empirical characterisation of when smoothed relevance estimates help sparse queries.

## What it deliberately does not do

No citation fetching, math checking, LaTeX hygiene, venue templates, or reviewer simulation — pair it with a mechanics stack for those (e.g. [claude-scholar](https://github.com/yy/claude-scholar)). The skill declares precedence over such tools on anything prose-related: mechanics skills verify and format; this skill owns the words.

## License

MIT
