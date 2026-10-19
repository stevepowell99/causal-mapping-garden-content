---
tags: paper
theme: theory-of-change
---

*For evaluators who use AI on interviews, reports and other text, and for the people who commission them.*

**Reconstructible reporting** means handing over, with your report, the data and enough detail for someone else to rebuild your analysis and run it again. In particular, any frontier AI should be able to do it out of the box without further information or instructions.

We think it should be easy for evaluators to show that they used AI in ways somebody else can check. Rubicon reports in this format, but you do not need Rubicon to report reconstructibly. We have published the format so that anyone can use it: [version 0.3](https://app.causalmap.app/rubicon/spec/0.3/).

## Why

"Read these forty interviews and tell me whether the programme worked" leaves everything to the model. "Mark every passage where a respondent describes an increase in income; count how many interviews contain at least one; judge that count against this rubric" leaves it much less. Breaking a fuzzy request into simpler ones makes the work auditable, can help clarify what we even meant, and puts every judgement against an explicit rubric. We call the set of steps a **workflow**.

Explicit steps also make absences visible: a step that finds nothing has to show what it searched and how much it read, and a proportion has to state its base, including the texts that said nothing.

## The bundle

With your report, hand over a **bundle**: the sources; the workflow as a text file, with every setting it ran with, including which AI model did each step; what every step produced, such as each coding table with its quotations, each codebook and each count with the documents behind it; the rubrics; every call made to a model; and how to read all of it. Machine-readable, so that a competent reader with time, or an AI in minutes, can rebuild the workflow and run it again without needing any particular software.

## The format

Our format builds every workflow from six general pieces:

- **sample** chooses documents;
- **code** marks passages and records what each says, in whatever columns the question needs;
- **group** finds the themes behind open codes and writes them up as a codebook, each theme with what counts and what does not;
- **tabulate** counts, done by software rather than by a model, and always out of a stated base that includes the documents that said nothing;
- **judge** applies the evaluator's rubric to the counts and passages;
- **write** gives the answer, in which every number comes from a count and every claim cites the passages it rests on.

Each piece has a few settings with defaults, and a run writes down every setting it used. The format is published, now at [version 0.3](https://app.causalmap.app/rubicon/spec/0.3/). A published version never changes; a correction becomes a new version beside it. Use it, fork it or ignore it. Nobody needs to agree on *one* format: a bundle that carries its own description can be read without knowing the format in advance.

## What a rerun proves

No-one expects a rerun with AI to always give exactly the same results. Sometimes a step that forks on a threshold like "more than half" diverges because the count lands near that 50% line. What we claim is that the process can be rebuilt, run again, giving findings in the same ballpark which can be compared: in the terms of [Goodman, Fanelli and Ioannidis (2016)](https://doi.org/10.1126/scitranslmed.aaf5027), *methods* reproducibility in a form that runs. *Results* reproducibility is "nice to have". The smaller and more explicit the steps, particularly early on, the better the chance that a rerun produces the same results.

## What the format does not do

It says nothing about how to *design* the workflow. In Rubicon that happens in dialogue with the assistant, but there is no algorithm for the right way to answer an evaluation question. Some clients want the workflow fixed early; others are happy for you to experiment. The format only asks that, once you have run it, you can hand over how it was done.

Our format is all about processing texts and narratives. But the same idea could work for workflows which include statistical analysis too.

## Existing reporting standards

Evaluation has the CHESS checklist ([Montrosse-Moorhead and Griffith, 2017](https://doi.org/10.1177/1098214017699275)); qualitative research has COREQ and SRQR. They say how to report what you did. This adds one thing: report it in a form that runs. Our survey: [[007 Is there already a standard qq ((rubicon-standards))|Is there already a standard?]]

------

## More ideas

### What makes a question well defined

One that two people with graduate-level social science skills would answer much the same way from the same material. In the problem-solving literature a problem is ill-defined when its statement leaves parts open (Reitman, 1964), and well and ill defined are the ends of a continuum ([Simon, 1973](https://doi.org/10.1016/0004-3702%2873%2990011-8)). Most evaluators mix and adapt methods to the case in hand ([Aston and Apgar, 2022](https://doi.org/10.19088/IDS.2022.068); [Apgar and others, 2024](https://doi.org/10.1177/13563890241232405)). A format like this does not stop that. It only asks that the mix be written down.

### Pre-registering the workflow, or not, or half-way

A workflow can be registered in advance with a commissioner, with a version, a date and a named person. Register nothing and you can still hand over a workflow somebody else can read *and run*. Register the sampling and the coding and you have committed to the descriptive half. Register the rubric too and you have said what counts as good before you know what the material says. (Some people love this, some people hate it.) Iterating is still allowed: every workflow version is dated and never rewritten, and every run records which version was in force, so a reader can see whether a threshold was moved before or after the results arrived.

A workflow written up afterwards, describing only the arrangement you settled on after experimenting, is still a workflow somebody else can read, check and rerun.

### Rubrics somebody can apply

A rubric turns a count or a set of passages into a verdict: is this good, or good enough. Each level needs a description detailed enough that somebody could hold it against real material and say whether the material meets it; a level that only gestures at what it wants leaves the reasoning to be rebuilt case by case. Where several criteria bear on one judgement, the rubric says how they combine rather than leaving that to whoever reads the table. The format does not supply thresholds such as "overwhelming means eight out of ten". Setting them is the evaluator's job, and the format only makes the setting visible. And sometimes nobody wants criteria settled in advance, because the material may be richer than the question anticipated, so a workflow can stop at a table or a piece of prose without reaching a verdict.

### Room for participation and reflection

In many approaches, Outcome Harvesting among them, participation and the analyst's own reflection are the most important part rather than an add-on. A format like this can mark a phase of a workflow as outside any algorithm: the work pauses while people meet or think, then continues with what they decided, or starts again. So one workflow can be participatory where it needs to be and rule-bound and checkable elsewhere, and the reader can see which parts are which.

### Why not just an appendix of prompts?

An appendix can be read. It cannot be run. Reading somebody's prompts tells you what they meant to do. It never tells you what the run did, and a prompt only makes sense in the conversation around it. Three common faults survive a careful reading of any appendix, because each is a property of the results rather than of the plan: a quotation that appears nowhere in the source; a proportion whose base leaves out the documents that said nothing; a threshold set after the numbers arrived. And a commissioner receiving forty evaluations a year will not read forty folders of prompts, while a machine can check forty bundles against a published format.

### Validating the workflow

- Generate two sets of synthetic documents, one that should score well and one that should score badly, and run the workflow over both before the real material.
- Develop the workflow on a subset and run the settled version over the rest.
- Run one instruction twice over the same ten sources to see the run-to-run variation, and two wordings to see how sensitive the instruction is.

See also: [[000 Reconstructible reporting -- keeping evaluators the pilots ((rubicon))]]; [[005 Rubicon principles ((rubicon-principles))]].

*This page was drafted with the assistance of Claude, an AI model from Anthropic; the arguments and judgements are our own.*
