---
date: 2026-07-10
---

The [[questions-introduction|individual questions catalogue]] describes what a skilled analyst asks of a causal map and how they answer it: which filters, in what order, counting by sources or citations, with which caveats. A slide creation function (SCF) is that recipe written down as code, so the app can apply it for you. The 1-click report in the Causal Map app runs a catalogue of SCFs to draft a first set of report views.

## What an SCF is

Each SCF answers one question from the catalogue and has three parts:

- **An applicability test.** The SCF reads some basic facts about the project and decides whether its question is worth asking here. The sentiment discrepancy view only appears when sentiment is coded and sources disagree about at least one factor; the group comparison only appears when there is a metadata field with a handful of values covering enough of the data; the zoomed view only appears when labels use the `;` hierarchy convention. A question that does not apply produces no slide.
- **A parameterisation.** The SCF sets its own thresholds and choices from the data, the way an analyst would: thin the link bundles only when there are enough to clutter the map, pick the path-tracing endpoints from the factors with the highest and lowest [[tables-fields|outcomeness]], choose the grouping field with the best coverage.
- **A fixed filter recipe.** The output is an ordered stack of the app's own filters, the same ones you would apply by hand ([[combining-questions|combining questions]]). Nothing is invented: every slide can be explained by pointing at its filters, and reproduced by loading its bookmark.

## What the AI does and does not do

The deterministic part, which views to offer and how to parameterise them, is plain code. AI is used in three narrow places, each of which can fail without breaking the report:

- **Review.** After the slides are built, a model reads each slide's title, description and most-cited links, discards slides that say nothing, and writes a short commentary for the rest.
- **Narrative.** Each surviving map gets a vignette: a narrative description with verbatim quotes, through the same vignette channel you can run by hand. The report closes with a [[vignettes|typical source's own story]].
- **Selection** (planned): given the researcher's stated aim, choose and order a subset of the catalogue rather than showing everything applicable.

The AI never authors filters. It only chooses from things that already exist: slides, factor names, field names.

## Why the commentary is worded the way it is

The commentary and narratives follow the reasoning rules of this chapter. They report evidence rather than fact: "12 sources said X influenced Y", never "X drives Y". Counts are treated as salience of mention, never effect size. And the [[transitivity-trap|transitivity trap]] is respected in the tracing views: the drivers-to-outcomes slide uses [[source-tracing|source tracing]], so any pathway it narrates was told end to end by at least one source; if nobody told a whole story, there is no slide, rather than a stitched chain nobody claimed.

## Where it is going

The report reads its aim from the project description. The next step is an intake conversation that asks "what do you want to find out?", asks follow-ups until the answer is usable, and saves it there, so both the coding and the report are steered by the same stated aim.
