---
name: academic-prose
description: Rules for writing, revising, or reviewing academic paper prose — abstracts, introductions, results sections, captions, rebuttals, and camera-ready edits. Use whenever the task involves LaTeX manuscripts, .tex files, journal or conference submissions, or whenever the user asks to write, edit, polish, restructure, or check any section of a paper, even if they only say "write the intro", "tighten the abstract", or "fix this paragraph". Also use before declaring any paper draft finished, to run the pre-submission self-check.
---

# Academic Prose

Four rule sets, applied in this order whenever paper prose is written or edited:
1. **Voice** — plain-empirical register (§1).
2. **No hype** — strip constructions that put rhetoric ahead of substance (§2).
3. **No self-sabotage** — keep every fact and limitation, but never word the work down more than the evidence requires (§2b).
4. **Evaluability** — structure the paper so claims can be checked against evidence in seconds (§3).

Then run the **pre-submission self-check** (§4) before declaring any draft done. These rules apply to every paper, every venue, every section. If an instruction in the conversation conflicts with a rule here, flag the conflict rather than silently overriding.

Rationale (one line): the first judgement of a paper rests on whether the prose is clear and plain and whether the claims can be checked against the evidence quickly. These rules keep the writing from getting in the way of the work.

## 1. Voice — plain-empirical

Plain, confident, economical academic prose: one claim per sentence, subject–verb–object, moderate sentence length (15–30 words), no rhetorical staging. Formal machinery is always accompanied by a plain-language reading. Synthetic exemplars in `voice-exemplars.md` in this skill directory.

- **Abstract:** a flat sequence of "We X" declaratives — "We study… We propose… We prove that… We demonstrate… Our experiments show…" — closing with the contribution stated plainly: "The main contribution of this work is a tractable formal method for estimating topic models without relevance judgements."
- **Person:** "we" throughout, even when sole-authored.
- **Problem-first openings:** brief cited history of the area, then the gap in one sentence ("The primary obstacle to estimating such models is the absence of labelled examples at query time."), then the explicit motivation ("The desire to estimate this quantity directly is the primary motivation behind the present paper.").
- **Signposting:** "The remainder of this paper is structured as follows."; sections open "In this section we describe…"; back-references "As we pointed out in section 1.2".
- **Definitions deflated and immediate:** "A topic model is simply a probability distribution over the vocabulary." Introduce notation, then immediately gloss it: "We can think of this distribution as a summary of how the topic tends to be discussed."
- **Connective stock:** "Note that", "Recall that", "Suppose", "It is easy to see that", "It turns out that", "It is important to realise that", "It is worthwhile to point out that", "Intuitively, …", "In a nutshell, …".
- **Intuition beside formalism:** every formal step gets a prose reading; proofs and reductions are summarised in plain words before or after the symbols.
- **Results register:** "We observe that…" with plain numbers ("an improvement of 5%"); the significance procedure named in the text ("Significance was determined by a paired sign test at the 0.05 level."); restrained enthusiasm sparingly and always tied to evidence.
- **Limitations stated mid-argument, not buried:** "Note that this assumption may be problematic in practice, since the training sample is itself part of the collection."
- **Measured corrections** only when they earn their place: "At first glance it appears that adding weights makes the search harder, since we have introduced more degrees of freedom. In reality the weights make the problem tractable, since the relaxed space admits gradient methods." These remain subject to §2 — no staged reversals for drama.
- **Related work** engages each cited approach concretely in 2–4 sentences; parallel credit constructions are characteristic: "To the first line of work we owe the underlying model of relevance; to the second we credit the estimation machinery we build upon."
- **Spelling:** pick one variant (British or American) per the venue or the author's preference, and hold it with zero mixing.
- **Punctuation:** commas carry the sentences; em-dashes essentially absent; parentheses only for short glosses; footnotes rare.
- **Conclusions:** "In this paper we studied… We presented… We then showed…", closing with "questions that warrant further exploration".

Do not: pad sentences with qualifiers; chain subordinate clauses; use bold/italic for emphasis in running prose; adopt journalistic or marketing register; stack rhetorical questions.

## 2. No-hype rules (mandatory)

Banned constructions — rewrite on sight, in drafts and in any text being edited:

- **Em-dash chains.** At most one em-dash per paragraph, appositive definitions only. Never nest a clause inside an em-dash pair.
- **Rhetorical inversion.** "A strong annotator, we find, needs no training" → "We find that a strong annotator needs no training." Subject, verb, object.
- **The pivot.** "It is not X — it is Y", "not because X but because Y", "X is not the contribution; we use it to Z". State what is true; do not stage a reversal.
- **Triadic drama.** "It unifies. It predicts. It transfers." — three parallel short sentences or three bolded paragraph leads read as keynote rhetoric. Use an ordinary signposted enumeration.
- **Aphoristic titles and slogan openers.** No "The X Is the Y" titles; no abstract whose first sentence is a slogan. Titles name the method, the problem, and ideally the result, plainly.
- **Intensifier adverbs.** Crucially, importantly, notably, strikingly, remarkably, surprisingly — delete; the evidence carries the point.
- **Stacked parenthetical hedges.** One parenthetical caveat per sentence at most; move the rest to their own sentences or a footnote.
- **"Load-bearing" and structural/engineering metaphors.** Never call a term, assumption, result, or sentence "load-bearing" — it is a recognised LLM tell. The same goes for "the linchpin", "the cornerstone", "does the heavy lifting", "carries the weight", "the backbone of the argument". Say plainly what the thing does: "the marginal denominator is the **principal** correction" / "removing the corpus costs 11 F1, so the corpus **produces** the result", not "the corpus is load-bearing".
- **Blow-by-blow experiment history.** Do not narrate the experimental journey or re-argue a design decision in the results prose: "The earlier reading rested on one number…", "We separate the two by holding X fixed and varying Y…", "in case the programme form rather than the task limits the gain", "one factor changes per arm, so a gain localises the limit". State the result; the method belongs once in the setup/metrics section or a single lean clause, and the rationale for *why* an experiment was run is almost never needed. Symptoms: a results paragraph that opens by recapping the previous section's reading before giving its own; the same caveat restated two or three ways; a mechanism re-explained in the prose when it already sits in the table caption or the threats section. Cut to: the finding, its number, one scope clause. Keep each limitation in exactly one place (§3: caveats one hop away, never interleaved) — over-hedging that re-discloses a §7 caveat inside §5 is the same defect as overclaiming.

Prefer the venue's boring register over memorability. The goal is careful, plain academic prose. Read-aloud test: any sentence that sounds like a keynote slide, a tweet, or ad copy gets rewritten flat.

## 2b. No-self-sabotage rules (mandatory)

No-hype (§2) forbids overselling; this rule forbids the opposite and equally common error, **underselling**. Both serve accuracy. Honesty is non-negotiable: keep every number, CI, p-value, negative result, and limitation — never delete a disclosure. The rule governs only *wording*: state each fact in the most neutral, least self-damaging phrasing the evidence allows, so a reviewer's first impression is not handed a quotable confession. The failure mode is a paper that is *true but framed to lose*.

Rewrite on sight:

- **Self-deprecating verbs for neutral findings.** A result that is lower is "lower" / "does not improve" / "matches" / "is within noise" — not "fails", "worst", "useless", "merely", "no better than", "degrades". Reserve failure language for actual failures. "R3 is worst" → "R3 is lowest"; "the compression fails" → "the compression does not recover the corpus's accuracy".
- **Negative/null results are designed findings, not admissions.** If the paper predicted a null and confirmed it, state the confirmation ("the composition effect is within noise"), not a shortfall ("composition never helps"). A confirmed negative prediction is evidence *for* the framework, so frame it that way.
- **Scope every concession to where it holds.** If a baseline leads only in one regime, bind the concession to that regime in the same clause ("in that regime, with ample per-class data, the head reaches higher accuracy"). Never a bare "the head is more accurate" that a reviewer can quote as a general admission.
- **One delimitation, after the positive claim** (mirrors §3). At most one "we do not claim X" in the whole paper. Convert every other self-limiting "we do not / cannot / only / merely / do not surpass" into a neutral scope statement that keeps the fact: "we do not surpass end-to-end heads" → "end-to-end heads remain the accuracy ceiling, which a training-free method does not target".
- **Do not hedge a tested result.** A number whose CI excludes zero is a result; do not also label it "exploratory" / "indicative" / "appears to". Keep the precise caveat once (e.g. "fragile to a multiple-comparison correction") and drop the bare adjective.
- **Guard the high-read positions.** The abstract, the contribution sentence, and the conclusion form the first and last impression. Lead with the defensible win, then the scoped caveat; never open or close on a limitation stated more starkly than the evidence requires. Order matters: "exceeds RAM++ by 7 mAP and is far better calibrated; on MS-COCO a nearest-neighbour baseline reaches the same accuracy" beats "its 7 mAP margin is matched by a nearest-neighbour baseline".

Read-aloud test (mirror of §2): any sentence a hostile reviewer could quote verbatim to justify rejection, that a neutral rephrasing would defuse **without changing a single fact**, gets rephrased. If the rephrasing would require softening a number or dropping a disclosure, stop — keep the honest version.

## 3. Evaluability rules (mandatory)

Write for a reviewer who reads the abstract, skims the intro for claims, jumps to the headline table, and tries to verify one claim end-to-end in five minutes. If any step needs a footnote, a split reconciliation, or decoding a flourish, the check fails. Honesty delivered inline reads as noise; honesty delivered in structure reads as rigour.

**Claims.** End the introduction with a numbered claims list (C1, C2, …), each pointing to the section and table that tests it. Every results subsection opens by naming its claim in one plain sentence with its supporting table. A claim with no dedicated table or figure is not a claim — give it one or demote it to discussion. State the contribution affirmatively, once; at most one "we do not claim X" delimitation in the whole paper, in the introduction, after the positive statement.

**One protocol per headline number.** Each benchmark in the headline table gets exactly one protocol — one split, one config, one selection procedure, the one the significance test uses. Variants live in ablation tables. No footnote may be needed to compare two cells of the same table; if one is, restructure the table. Non-comparable studies are firewalled in their own subsection with the difference stated in the table title. The significance-tested number is always the headline, never the "best" number.

**Abstract.** ≤160 words. Problem (one sentence), method in plain terms (one–two sentences), the claims as flat declaratives with at most one headline number each, one sentence on the conceptual contribution. Zero parentheticals, CIs, split sizes, or inline hedges — those live in the body. First sentence is a direct declarative ("We show that...", "This paper studies..."). Sentences over ~35 words get split.

**Caveats consolidated, never interleaved.** Qualifications, selection details, and protocol notes go in exactly two places: a short "Protocol" paragraph opening each experiments subsection, or the reproducibility appendix, with pointers. Results sentences state the result; the qualification lives one hop away. Preserve every disclosure — relocation, never deletion.

**Register in results.** One claim per sentence; maximum one parenthetical per paragraph. "Removing the corpus costs 11 F1 (Table 7)" beats "The corpus, not the parameters, is the model." Thesis-style section titles are acceptable, but the first sentence beneath each states the claim plainly with its table. Table captions ≤3 sentences, descriptive only. Teaser figures carry mechanism, not marketing — no "beats X" callouts.

**Numbers are immutable and traceable.** Every reported number traces to one protocol (ideally one registry entry or script). Never report two versions of "the" result for a benchmark in the main text. If a structural edit seems to require touching a number, stop and re-derive which protocol it belongs to — and ask before changing anything.

## 4. Pre-submission self-check (run before declaring any draft done)

1. Enumerate the claims and verify each against its evidence using only the claims box — each must be locatable and checkable in ≤30 seconds.
2. Each headline table: interpretable from its caption alone, single stated protocol, no footnote needed to compare its cells.
3. Read the abstract aloud; any sentence needing a breath mid-way gets split.
4. Count "we do not claim": more than one instance → delete down to one.
5. Search results sections for parentheses: each is deletable or evidence the sentence does two jobs.
6. Confirm the headline number is the significance-tested one and every variant is in an ablation table.
7. Banned-construction check — TWO stages, both mandatory:
   a. Mechanical: grep for em-dashes ("---", and "--" outside number ranges), intensifier adverbs, banned spellings, and the LLM-tell metaphors ("load.?bearing", "linchpin", "cornerstone", "heavy lifting", "the backbone of"); count and justify every remaining instance — these phrases are banned (§2), so the justified count is zero.
   b. Semantic: greps CANNOT detect inversions, pivots, keynote/aphoristic sentences, marketing register, or anthropomorphic drama. These require reading every sentence, every \section/\subsection/\paragraph heading, every caption, and every figure label (including TikZ text nodes). Run this as a dedicated fresh-context audit — a subagent given the full source and the §2 ban list, instructed to return line-numbered violations with flat rewrites, explicitly told to sweep headings and captions — then apply the fixes. NEVER report this item as PASS on the strength of stage (a) alone.
   Calibration note: a grep-only pass once reported PASS on a manuscript whose reader then found two violations within minutes of opening the PDF; the subsequent full semantic audit of the "clean" file surfaced 33 further must-fix items, six of them in headings and captions. Watch especially for: "what X buys" clefts, "the right tool was X; for Y it is Z" frames, "not X; it Y" pivots, sports/economic metaphors (wins, buys, clears, payoff, the load), structural/engineering metaphors (load-bearing, linchpin, cornerstone, heavy lifting, backbone of the argument), one-line slide sentences used as paragraph closers, fronted-participle openers ("Written this way, ...", "Recognised as X, ..."), and blow-by-blow experiment narration ("The earlier reading rested on…", "We separate the two by…", "in case X rather than Y limits…", the same caveat restated two or three ways, a mechanism re-explained in prose when it already sits in a caption or the threats section).
8. Spot-check spelling is consistent with the chosen variant throughout — no mixing.
9. Self-sabotage sweep (§2b): scan for self-deprecating verbs on neutral findings ("fails", "worst", "useless", "merely", "degrades"), bare hedges on tested results ("exploratory", "indicative", "appears to"), and unscoped concessions to baselines; reframe each neutrally while keeping every number and disclosure. Re-read the abstract, contribution sentence, and conclusion specifically for limitations stated more starkly than the evidence requires. In the same pass, flag blow-by-blow experiment history (§2): results prose that recaps *why* or *how* an experiment was run, restates one finding two or three ways, or re-discloses a caveat already consolidated in the threats section; cut each to the finding, its number, and one scope clause, and keep every limitation in exactly one place. Best run as the same fresh-context audit as 7b. Confirm no fact, number, or disclosure was removed.
10. Compiled-output sanity (open the built PDF, not just the source — a clean source can still render wrong). Two recurring faults:
    a. **Malformed heading numbers.** Scan headings for spurious deep numbers such as "14.0.0.1 Open problems." This is a numbered run-in `\paragraph` heading: the class is numbering to paragraph depth. IEEEtran journal/compsoc defaults to `\setcounter{secnumdepth}{4}`, which numbers `\paragraph`; when `\paragraph{}` is used for unnumbered run-in headings, set `\setcounter{secnumdepth}{3}`. (Detect by eye, or grep the PDF text for `\b[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+ [A-Z]`.)
    b. **Floats overflowing or magnified.** Check every table/figure against the margins. A `\resizebox{\textwidth}{!}{...}` around a *tabular* renders at a huge font once the float becomes full-width (`table*`), because `\textwidth` is then the whole page, not the column — drop the resizebox so the tabular renders at its natural size. Likewise, in two-column classes `width=0.4\textwidth` subfloats and wide tabulars overflow a single column; promote genuinely wide floats to `figure*`/`table*` (identical in single-column classes, full-width in two-column). The fixes belong to `latex-cleanup`; this item only mandates that the *rendered* output be eyeballed, since these never show up in a source-only read.

Report the outcome of this checklist to the user explicitly — pass/fail per item — before calling the draft finished.

## 5. Pre-submission experiment-code audit (papers with empirical claims)

Before any empirical paper is called submission-ready, run an **adversarial bug audit of the experiment/evaluation code and its shared library** — in addition to the multi-reviewer simulation (`paper-reviewer-panel`), not instead of it. The two catch different failures: the reviewer panel reads the *manuscript* and judges claims and framing; it never sees the code. This audit reads the *code* that produced every headline number.

Why it is mandatory and separate: **a result registry (numbers traced to the command that produced them) proves *reproducibility*, not *correctness*.** A bug in an eval script produces a wrong number, the registry faithfully records that wrong number, and a registry checker passes. "Every number traces to a command" is not "every number is correct."

Run it as an adversarial fan-out (one skeptic per headline-claim script + the shared metric/estimator/data modules, each tasked to *find a result-invalidating bug*), then a second pass that tries to *refute* each finding (default to false-positive unless the code confirms it). Hunt specifically for the bug classes that survive a registry and a manuscript review but sink a claim:

- **Test/corpus leakage** — a test/query item (or duplicate) sitting in the corpus/KV memory or in the co-occurrence/prior construction; the same split used to both select and evaluate.
- **Test-set fitting** — temperature, threshold, kernel/β, top-k, or fusion weights chosen on test rather than validation; a "val" split that is actually test.
- **Metric errors** — wrong averaging (micro vs per-class), off-by-one top-k, mAP on the wrong axis/sort, wrong P/R/F1 or ECE denominator, ties resolved so as to flatter.
- **Baseline handicap** — the comparator given fewer dials, the wrong operating point, or a harder split than the proposed method.
- **Aggregation** — seeds/bootstraps averaged or counted wrong; CI on the wrong resampling unit; permutation/sign-flip test mis-specified.
- **Denominator/normalisation scope** — a correction summed over a set that includes the query itself or test items, or applied inconsistently between method and baseline.
- **Silent filtering** — dropping hard examples, empty-label rows, or classes in a way that inflates the score.

Deliverable: a severity-ranked report with `file:line` and the fix for each confirmed bug, an explicit list of uncertain items needing human eyes, and a stated coverage list (which scripts/claims were and were **not** audited). Report pass/fail to the user before calling the paper submission-ready; a clean audit is reported as clean, plainly.

## One-line summary

Write plainly and economically (one claim per sentence, intuition beside formalism), strip every construction that puts rhetoric ahead of substance, word each result neither above nor below what the evidence shows, report findings without narrating the experimental journey or re-arguing why each experiment was run, state each claim once and plainly, test it under one protocol in one table readable from its caption, keep every qualification one structured hop away — and make the claim→evidence path walkable in thirty seconds.

## Precedence over other skills

These voice, no-hype, and evaluability rules take precedence over any other writing, style, or paper-related skill. If another skill's instructions conflict, follow this skill and note the conflict. Mechanics skills (citation checking, math verification, LaTeX cleanup, venue templates, reviewer simulation) handle verification, formatting, and review structure only; whenever any of them would touch prose, tone, register, or abstract content, this skill governs.
