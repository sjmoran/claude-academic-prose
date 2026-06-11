# Plain-empirical voice — synthetic exemplars

The register was distilled from a corpus of published empirical-IR papers. All sentences below are synthetic, written in that register. They illustrate the rhythm; do not copy them verbatim into papers.

## Abstract rhythm (complete example)

> "We study the problem of estimating topic models from very short queries. We propose a weighted estimator that interpolates document models according to their likelihood of relevance. We prove that selecting the optimal subset of documents is computationally infeasible, and we describe a gradient procedure that avoids the search entirely. We demonstrate the estimator on two retrieval collections. Our experiments show that the weighted estimator outperforms a strong unweighted baseline. The main contribution of this work is a tractable formal method for estimating topic models without relevance judgements."

## Problem-first gap statement

> "The primary obstacle to estimating such models is the absence of labelled examples at query time. In a typical retrieval setting we are given a query, a large collection of documents, and no indication of which documents are relevant."

## Explicit motivation in one sentence

> "The desire to estimate this quantity directly is the primary motivation behind the present paper."

## Deflated definition, then gloss

> "A topic model is simply a probability distribution over the vocabulary. We can think of this distribution as a summary of how the topic tends to be discussed."

## Intuition beside formalism

> "Intuitively, the difficulty is that the number of candidate subsets grows exponentially with the size of the collection."

> "In a nutshell, the decision problem asks whether the target distribution can be assembled exactly from members of the collection."

## Measured correction (load-bearing only)

> "At first glance it appears that adding weights makes the search harder, since we have introduced more degrees of freedom. In reality the weights make the problem tractable, since the relaxed space admits gradient methods."

## Parallel credit in related work

> "To the first line of work we owe the underlying model of relevance; to the second we credit the estimation machinery we build upon."

## Results register

> "We observe that the weighted estimator outperforms the baseline at all levels of recall. Significance was determined by a paired sign test at the 0.05 level."

> "The weighted estimator yields an average precision of 0.741, an improvement of 6%."

> "We find these results encouraging, since they show the estimator is stable across collections."

## Honest limitation mid-argument

> "Note that this assumption may be problematic in practice, since the training sample is itself part of the collection. We hope that stopping the procedure after a small number of iterations avoids the degenerate solution."

> "It is worthwhile to point out that we were not able to establish the converse."

## Signposting

> "The remainder of this paper is structured as follows. In section 2 we define the estimation problem formally and derive a lower bound on its solutions."

> "As we pointed out in section 1.2, the quality of the estimate depends strongly on the subset of documents used to form it."

## Conclusion rhythm

> "In this paper we studied weighted estimators of topic models. We presented a proof that subset selection is infeasible, and we then showed that a relaxed weighted formulation admits an efficient gradient procedure. In the course of this work we encountered several questions that warrant further exploration."
