---
tags: paper
theme: theory-of-change
---

> **Work in progress.** This page is mirrored automatically from `rubicon/docs/principles.md`
> in the Causal Map repository and changes as the design does. The section written for
> whoever changes the code is not published here.

Everything as far as Open questions is for anyone thinking of using Rubicon. The last section is for whoever changes the code.

## Why it exists

**AI is in evaluation and it is staying.** Used well it raises quality on narrative material, more cheaply than anything before. Used badly it produces junk just as fast. On the page the two look alike: both fluent, both quoting a few passages that fit. The difference falls on whoever acts on the report.

**So do not ask an AI a vague question.** It will answer confidently, having decided for itself what you meant.

**Break the question into codable ones.** A codable question is one that two people would answer much the same way from the same material, with every answer leading back to a passage a third person can check. Doing that breaking down is the work.

**Rubicon** does this. It is an experimental wing of the Causal Map code base, with its own page and its own database. Working name. If it goes further it becomes a separate product. Its projects are Causal Map projects, so it can read the project's causal map, and each source's map, alongside the documents.

The reader of an ordinary evaluation report cannot see four things: which passages were counted and which were passed over; what rule set the threshold at "more than half"; whether that rule was written before or after somebody knew how the numbers fell; whether a second coder would have marked the same passages. AI makes that worse, because a model reads a thousand pages overnight and nobody can check its working. It also makes it fixable, because a machine that reads can be made to show every step.

> Rubric and Rubicon share a root, Latin *ruber*, red. A rubric was a heading written in red ochre in the margin of a law book, and the Rubicon was named for the red clay of its bed. Red means take me seriously. Crossing the Rubicon is what this app asks for: fix the rule before you see how the results fall.

## What it does

You state a question and argue out a **workflow** with Ruby, the assistant, before any analysis runs: which sources to read, how to mark them up, how to count what was marked, how to combine the results, how to reach a verdict. Then it runs. What you agreed is the product.

So, five things.

- **The standard is written down and versioned before the run that applies it reads anything.** Pressing Run is the act of agreeing to it.
- **Every claim can be traced back to the words in a document.** Verdict to figures, figure to rows, row to quote, quote to the span in the source.
- **The evaluative method is written out**, usually as a rubric. The machine runs it and a person checks it.
- **A method can be tested before it meets real material**, on synthetic texts with known verdicts, some good and some bad. Optional, and we believe unique to Rubicon.
- **Ruby builds a workflow out of powerful general ideas** rather than picking a named method off a long menu.

Agreeing rubrics before the evidence arrives is sometimes advised in the evaluation literature. Pre-registering them, with a version trail, is not.

Rubicon answers one question at a time. Grouping several into a report is on the roadmap.

## The words we use

Read this before the rest. The terms are the idea, and most of them exist because one of the others does.

**How they fit together.** A *project* holds *sources* and *questions*. For one question you agree a *workflow*, a set of *steps*. Running it makes a *run*, and each step produces a *result*: a *sample*, a *coding*, a *figure*, a *judgement*, a paragraph. Every result records which results it came from, so any claim walks back through *quotes* to the words in a source. When one result answers the question, you *accept* it.

Below, in the order the words turn up in a piece of work. A term in *italics* is defined somewhere else in this list. The rules that go with each term are in the sections after it.

### The material

**Project.** A Causal Map project. Rubicon keeps its own *questions*, *workflows* and *runs* beside it and never writes to the project itself.

**Source.** A document in that project. Rubicon reads these and never changes them. A source is never a *result*.

**Background document.** A *source* that is the standard rather than the evidence: a theory of change, the funder's standards document, terms of reference. You flag it on the source itself in Causal Map, in a custom column, so one library serves every *question* you ask of that project. Never *sampled*, *coded* or counted. There is no button for the flag yet; you type it into the column.

**Sample.** Which *sources* were read, out of which set, chosen how. It is the *result* a `select` or `sample` *step* produces, and every later result carries it.

**Exclusion.** A rule over the source columns that drops *sources* from a *sample*, with a reason attached and a count of what was removed.

**Unit.** What gets counted, and what a *figure* counts across: a person, an organisation, a document. Every threshold needs one, because "more than half of stakeholders" has to know how many there are. Rubicon makes one unit per source. A project whose units are really people, with several interviews to a source, overrides those rows by hand.

**Chunk and segment.** A long *source* is cut into equal chunks of at most sixteen thousand characters, one model call each, unless an earlier *step* already narrowed it to passages, when each passage is a call. The whole source is pre-swept into numbered segments and each chunk carries the markers for the ones it holds, so a number means the same thing in every chunk. That numbering is the handle for making a model account for the whole of what it was given rather than stopping at the first good thing.

### The question, and agreeing what to do

**Question.** What you want answered, and the thing every *workflow* is an attempt on. A *project* has many, and every *run* files itself under one, matched on the text, so asking the same thing twice does not make two questions.

**Codable.** Two careful readers would apply the *coding* instruction much the same way, and every row leads back to a *quote* a third person could check. Codability is what *Ruby* refuses a question for, and nothing else is.

- A property of the question and the material together, usually achieved rather than discovered. Most questions arrive uncodable, and making them codable is *Ruby's* job.
- Not the same as objective, factual, measurable or important. A codable question can be trivial, and an excellent question can be uncodable.

**Ruby.** The assistant. She reads the corpus, says what she takes a *question* to mean, argues with the parts that will not work, and proposes a *workflow*. She never decides what counts as good.

**Chat conversation.** An exchange with *Ruby* about a *question*. A question has many and a *workflow* has many, neither owning the other. It is a *run* like any other and carries a status, but what it produces is a workflow or nothing, so that status says whether the conversation ran and never whether the workflow is any good.

**Rewriting a chat turn.** Edit anything you said and the chat carries on from there, dropping the turns below. The result is a fork: a new conversation that reads the earlier turns from the old one and holds none of the later ones. The original is unchanged, and nothing is copied, since the fork stores only the turn it was cut at.

**Project hub.** A list of all the *project's* *questions*, as well as the project's standing *chat conversation* with *Ruby*, attached to no single question and shared by everyone on the project.

**Draft.** A *workflow* *Ruby* has written and you have not yet *run*. Read it, argue with it, change it. Checking that it will run costs nothing, and nothing is spent until you press Run.

### The workflow, and fixing it in advance

**Workflow.** One set of *steps* and the graph joining them. This is the thing you agree, version, date and hand to a commissioner. One *question* may have several, and each may have several *runs*.

- You never number the steps. Each step says what it needs and what it makes, and the order falls out of that. Two lines of work can run side by side and come together later.
- **A name and a version.** The name says which way of answering the *question* this is, and Ruby is asked to say how each one differs from the others. A workflow with no name is refused, and so is a name and version already used for different steps. `foo v2` is a different workflow from `foo v1`; the shared name says the two are attempts at one idea rather than unrelated ideas.
- **Change the steps and it is a new workflow**, at the next version. A *run* fails, Ruby fixes it, and that is `foo v2`. Running the same steps again, or only up to a named step, is the same workflow at another run.
- **A workflow's state** is one of: not run, running, waiting, failed, candidate, accepted, archived. A *question* carries only whether it is open, answered or abandoned, and whether it has been archived. What the *project hub* shows against it, what to do next, is read from its workflows rather than stored: ask it, read what Ruby said, run the *draft*, watch a run, read what came out, or it is answered.

**Step.** One instruction inside a *workflow*. It says which *results* it reads and what it produces, and it is the smallest thing that can succeed or fail on its own. The kinds:

- `select`, `sample` and `select_passages`: three names for one step, saying what may be read next and producing a *sample*. Over documents, over passages, or both.
- `code`: mark up the text, producing a *coding* and its *quotes*.
- `compute`: work out a *figure*.
- `align`: pair two codings of the same text so the agreement can be counted.
- `judge`: apply a *rubric* and reach a *judgement*.
- `note`: write it up.
- `synthesise`: make text to *validate* a method on.

**Fan-out and prong.** A *step* written with `for_each` runs once per item in a list, and each of those runs is a prong. Prongs are built from the same inputs and never receive each other's outputs. Usually a later step gathers them into one table, but it need not: a *workflow* can end in a fan-out, with one *judgement* per partner organisation and nothing combining them.

**Result.** What a *step* produces: a *sample*, a *coding*, a table, a *figure*, a *judgement*, a paragraph. You name the type yourself, in your own words.

- A *source* is never a result. What a sampling step produces is the *sample* it drew; the documents themselves stay Causal Map's.
- A result never changes. Run the step again and the new result sits beside the old one, so the two can be compared.
- Every result knows which results it came from. That chain is its *lineage*.

**Result set.** Everything a *workflow's* *runs* produced, finished or not. A run that broke at its fourth *step* still made three things.

**Validation.** Showing that a *workflow* works at all, by running it over synthetic texts whose *judgements* are known in advance. The `synthesise` *step* that makes those texts is built; nothing yet compares what the workflow awarded against what was expected. Independent of *registration*: a registered workflow may be useless, and a validated one may never be registered.

**Registration.** Fixing the standard before the evidence is read, with a version, a date and a named person. It attaches to the *rubric* rather than to the *workflow* around it, so a workflow that stops short of a *judgement* needs none.

### Running it

**Run.** One execution of a *workflow* or part of one. It records order, *results*, model, duration, cost, and every model call with the prompt as sent and the answer as returned.

- A *step* at a time is the intention: run the *coding*, read it, fix the instruction, run it again, and only then go on to the counting.
- `until` stops at a named step. `continue_from` picks up what an earlier run made, recording the inherited steps as skipped. `rerun` does one named step again. On the command line, `--until <step>` when starting and `resume <run-id> --rerun <step>` afterwards.
- A run that was told to stop records `cancelled` rather than failed.
- `rerun` names one *step* and cannot name a fan-out, whose steps are called `test_link[...]`, one per prong.
- Running twice is repair or a reliability check, so runs are a *workflow's* history rather than things to compare.

**Ledger.** The record of everything that ran: *runs*, *steps*, *results*, *quotes*, model calls and costs. The page and the command line both read it, and it is the only full account of a run there is. Only the cost of each real call is written a second time, to Causal Map's own `ai_logs`.

**Reuse.** Answering a *step* from an earlier identical model call rather than paying for it again. The key is the request as sent, source text included, so an edited *source* cannot inherit an old reading.

### What comes out

**Coding.** A pass over the text that finds passages and records whatever you asked about each one, in columns declared in advance. It is what a `code` *step* produces, and its rows are *quotes*.

- Causal Map has one canonical coding per *project*, because it builds one model of the sources' causal cognitions. Rubicon has no such object. A coding answers the *question* its own instruction asks, so a project holds as many codings as it has questions.
- A coding whose every row was refused by the declared columns is refused, rather than recorded as having found nothing.

**Quote.** A marked passage: the words and their position, checked against the real text and snapped to it where the match is exact, canonical or gapped, and kept as the model wrote it with approximate offsets, labelled as such, where the match is only fuzzy. A quote the machine cannot find in the *source* at all is thrown away rather than stored, because a plausible quotation that appears nowhere is the most dangerous thing an AI can produce. Everything else here exists to stay attached to these.

**Figure.** One value a `compute` *step* produced, a number or a table where it grouped, carrying the *unit* it counted across, the filter it applied and what it took from each unit, all stated rather than implied.

**Rubric.** A table whose rows are the verdicts on offer, each with a shortname, what it stands for, and how to make that judgement. It is how you get from "five out of seven" to "adequate".

- A rubric is not itself a *step*. A `judge` step applies one, reaching a *level* on each *criterion* and then combining them where the rubric says how.
- A shortname alone is not a standard. "Green" says nothing. "Above average for a project of this type" is a claim.
- Where one description fuses several *criteria* and you would rather keep them apart, the column splits into one per criterion. Rubicon takes either.
- The verdicts are whatever you say. Nothing in the app knows which set you will use, or assumes red, amber and green, or three levels.
- Some *workflows* never use one. A *step* may produce a yes, a shortlist, or a short story written to make a typical account palpable, without making a final *evaluative judgement*.

**Criterion, level and band.** One *judgement* may rest on several criteria: salience, strength, frequency, coverage, whatever the *question* needs. The levels are the verdicts a criterion can take, and two criteria in one *rubric* need not share a set of levels: one can be red, amber and green while the next runs 1 to 5. A band is a contiguous run of levels, such as "adequate or better", and it only means anything where the levels are ranked.

**Judgement.** One verdict, produced by a `judge` *step*: what the material earned, why, and which *quotes* it rests on.

- **Where the *rubric* keeps its *criteria* apart, it must say how they combine**, because whether one red outweighs two greens belongs to whoever wrote the standard. A rubric that does not say produces a judgement that reports each criterion and states that nothing combined them.
- Some verdicts are settled by arithmetic over *figures*, others by the AI reading the evidence against the written description. Both are legitimate, they carry different weight, and the judgement records which was which.

**Evaluative judgement.** A *judgement* that restricts a set of options which are defined and ranked by worth. This is the kind that needs *registration*, and the three conditions are under Worth is declared by a person, below.

**Lineage.** The chain by which every *result* records which results it came from, ending in *quotes* and the words in a *source*. If the walk back breaks anywhere, nothing else about the *run* counts.

**Accepting.** Naming one *result* as the *question's* answer. It points at a result rather than at a *run*, so a table can be accepted as readily as a *judgement*.

**Archiving.** Hiding *runs*, or a whole *question*, when you are finished with them. A *workflow* shows as archived once every run of it is. It never deletes.

## How a piece of work goes

Fully specified means every decision settled before anybody sees the evidence. That is the hardcore end rather than a requirement.

1. State the question, and which part of it this workflow answers.
2. Name the sources.
3. Write the coding instruction.
4. Write the counting rule.
5. Write the rubric.
6. Validate it on synthetic texts.
7. Register it with the commissioner, dated, before the analysis runs.
8. Run it, and report what comes out.

Steps 6 and 7 are independent: a registered workflow may be useless, and a validated one may never be registered.

In practice we iterate. The question turns out not to fit the material, a distinction nobody expected forces new coding columns, a finding rests on one talkative respondent. So every version is dated: change a threshold after seeing the numbers and that shows, change it before and that shows too.

The version trail is half the answer. Holding material back is the other half. Revise on what you have read, then run over documents that played no part in producing the workflow.

We claim no determinism and no full reproducibility. AI coding varies between runs, and machine agreement with human coders is well short of perfect. What survives is **auditability**: a reader who disagrees can find out exactly where.

## Principles

### Worth is declared by a person

Julian King put the objection in October 2025: AI should not be making evaluative judgements about human affairs. Quirkos and SenseMaker refuse AI analysis altogether, and f4analyse will not automate analysis of a whole corpus. We agree.

- Nothing inside a scale makes it evaluative. Green is not better than red because of anything about green, and no amount of looking at the material tells you where adequate begins.
- A descriptive finding has a backstop: count the households wrong and the passages are still there. An evaluative claim has none. A standard set after seeing the numbers can be made to say anything and stay consistent with all of them.
- So your reader's only protection is that the standard came first, from somebody who put their name to it. That is why registration exists.
- **Registration attaches to the standard** rather than to the workflow around it. A workflow that samples, codes and counts and then stops needs none.
- A rubric is versioned and never replaced, and carries who registered it and why, though on the run path both are written by the machine rather than by a person. Freezing a version, and recording whether the freeze came before the run, is designed and not yet built.
- The argument is with tools that ask a model to decide what good looks like and then present the answer as a finding.

**A step is making an evaluative judgement when all three of these hold.** The app does not test the three. It uses the structural proxy, a step of type `judge`, and that is where it requires a rubric.

- It **restricts** a set of options declared in advance, usually to one of them, sometimes to a band such as "adequate or better".
- Each option **says what it takes to earn it**. "Green: every partner described a change they could date and name a cause for" is a standard, because you can argue about whether the material meets it. "Green" on its own is not, because two people reading it would not agree what it means and neither would a model. A coding column whose levels are bare names is refused outright; a rubric that lists its verdicts must say what each stands for, and one that never lists them runs with the meanings reported as missing.
- The options are **graded by worth**. Health, farming and income is classification, because it ranks nothing. A frequency table over speculative, reported and evidenced has options and grading, but it reports the distribution rather than choosing a point on it.

Grading is what makes a band coherent, so `at_least` works on an ordinal and never on a category. The test applies to the answer a step gives, so a workflow is usually descriptive in the middle and evaluative at the end. Structurally: whether it ends in a judge step.

**Transparency is not enough on its own.** There has to be a place to disagree: override the verdict, rewrite the rationale, reject a cited quote, mark a criterion unanswerable. The override would sit beside the machine's verdict so the difference is itself a finding, carry who and when, and be what everything downstream used. None of it is built. Today the only human decision the app records is accepting or withdrawing a whole result.

### Every claim points at a quote

- Any narrative or verdict about the material must lead back to the quotes it rests on. The system refuses to store a note or a judgement that cites none, and it gets there by requiring the coding to be a declared input of the step making the claim, so a claim cannot drift away from its evidence. A table is not held to this.
- This is the likeliest way a tool like this fails, and it fails without showing: two steps from the source the prose still reads well and the numbers still look precise, while nothing connects either to a document. Note it's easy for an AI tool to reach a conclusion and then search the text for quotes to back that up. Rubicon does not fall into that trap.
- **Some findings are about the method rather than the material:** was contrary evidence looked for, was the sample drawn in a way that supports the claim. No quotation can evidence the absence of a search, so those cite the run record instead, and the judgement says which kind each verdict was.
- A criterion should be one kind or the other, and nothing refuses one that is both. "Was anything found that cuts against the hypothesis, and how was it handled?" is two questions, and asked as one it makes a model rate the method by reading the evidence.
- A band should stand for one state of affairs, and this one is on you: nothing reads a band's description. Where the worst band covers both "contrary evidence was found and it is damaging" and "nobody looked", the reader cannot tell which happened.

Anything that can legitimately find nothing must show that it at least looked. A check that passed because it matched nothing, a search pointed at the wrong place, a step that read half of what it was given: all three look exactly like a good result. So the machinery reports what it did as well as what it found: passages dropped because the quote could not be located, how much of each document was examined, how many model calls and what they cost.

**A negative finding is the hardest case.** No quotation can evidence an absence, so demanding one pushes "nobody described a two-way benefit" into citing something irrelevant. A negative finding cites the search: what was looked for, where, and how much was read.

### Build the thing, and not only the verdict

A verdict is one word standing for eight links, three hundred passages and nineteen documents, and tracing back through it does not rebuild what was compressed. So where you would expect a graph, a table of outcomes or a cross-tab to be in front of you, the workflow builds it and declares it as a result, which usually costs nothing because it was a step on the way anyway. Such a workflow can stop there: a table can be accepted as the answer as readily as a verdict. The mirror fault costs more, so a question that wants a number should not pay for a graph nobody asked for.

### Say what you are comparing against

A programme did well: compared with what? Seven answers, and they are not interchangeable.

- **A denominator.** Eleven of the fourteen partners. Needs a unit and a stated base.
- **An alternative.** Which of two readings the material better supports. No denominator at all.
- **A written standard.** A rubric agreed in advance. The only one that works when there is nothing to compare with.
- **A comparison case.** The programme before it started, a similar one elsewhere, a site that got no support. Rests on the cases being alike in the ways that matter.
- **What was expected.** The theory of change, the target, the plan. Cheap, and it measures delivery rather than worth.
- **What would have happened anyway.** Usually the hardest. Approachable through causal mapping and other generative accounts of causation, which treat people as causality detectors whose judgements carry counterfactual implications.
- **The evidence itself.** Sometimes the finding is that nothing here is well enough evidenced for any of the above.

Most confusion in evaluation reporting comes from sliding between them: counting how many people said something, then writing as though that settled whether it was any good. Two obligations follow.

- **Search both sides equally.** Look harder for X than for Y and "more evidence for X" is an artefact of how hard you looked, and the risk is invisible in the output. Searching both sides in one pass over the same text is a convention rather than something the app enforces. What the app does is check, where two codings are compared, that they had the same opportunity: same sources, same settings, comparable segment coverage, and no shared reused answers. It reports the disparity on the comparison and refuses nothing.
- **A proportion states its base, and the base includes the documents that gave nothing.** Build a denominator from the passages already coded and a document that said nothing disappears, so "of the sources that gave me something" reads as "of the sources". On a sparse question, which unintended harm usually is, that inflates the headline figure where it matters most.

### What it refuses, and what stays soft

- **"Read the documents and tell me whether the project was effective."** Answered in one pass, that produces the thing this app exists to replace: a confident verdict, no stated standard, and no way for anyone to disagree with it in particular.
- **"Is this a good project?"** is four questions in one coat: good for whom, compared with what, against whose standard, and how much of that this material can answer.
- The test is codability. Nothing is refused for being about tone or feelings or anything else that sounds soft.
- **Refusing is rarer than it sounds.** "What percentage of the budget went on training?" is codable where a report states the figure and unanswerable where none does, which is a fact about the corpus. The answer is usually a workflow that goes and looks. If nobody wrote the figure down, that is the finding, with the search behind it.
- **Some questions are codable in parts and not as a whole.** "What share of the fellows who wanted a policy meeting got one?" is two codings and a ratio. A single pass would be arithmetic done in a model's head.
- **A question whose answer is in a spreadsheet is refused, and that is the point.** Hours between landfall and the first cash payment, cost per person reached: those live in a payments system with no words behind them. Everything here rests on a number being followable back to the words somebody said, and mixing the two makes every number only as traceable as the weakest. The workflow says which part of the question it answers, and you bring the other figures in when you write.
- **A number spoken in a document is in scope.** "We reached about four hundred children", said by a school director, has words behind it, a speaker and a position in a source. A coding step declares a numeric column and the counting does arithmetic on those.
- **A judgement may refuse the question.** Where the material shows the question rests on something that did not happen, or compares two things the sources cannot compare fairly, the judge says so instead of awarding a band, and cites what that rests on. Awarding a band is worse, because the band gets quoted and the doubt does not. One criterion challenging the question sinks the overall verdict rather than being outvoted.

Named methods stay available and stay out of the code.

- Outcome harvesting, contribution analysis, process tracing, realist evaluation: Ruby knows them and offers one when a question suits it. That knowledge is writing, and it reaches no code path.
- The app is built from general blocks: choose sources, narrow to relevant passages, code text, group and count, compare, apply a rubric, write it up. A named method is a recipe written in those.
- Two reasons. A tool built round a fixed list is wrong the first time somebody wants something slightly different, which is most of the time. And a method encoded in software is a method nobody can argue with.
- Where a method wants a dial that is useful more widely, build the dial. Outcome harvesting needs the unit to be a person rather than a document, and so does anything else about actors. The test is whether it serves several methods.

## Ruby, the assistant

- **Ruby is the way into the app** rather than a tool beside it. You state your question in your own words, argue about it, and out comes a workflow you have agreed to.
- **She learns what the app accepts by being refused.** Refusals are written to teach.
- **She is a methods coach rather than an order-taker.** A question can be perfectly codable and a poor use of the material: it rests on two speakers out of seventy, or it counts how many said something where the interesting thing is what they said. She says what she would ask instead, then writes the workflow for what you actually asked. The evaluation is yours rather than hers.
- **She argues and you decide.** What she does not do is settle what counts as good.
- **What gets agreed is the workflow** rather than the conversation.

## The screen

A conversation on one side and a canvas on the other. 

- **A workflow is one scrolling document.** Unrun, it is the steps. Run, each result sits in the block of the step that made it. Lineage is the point of the app.
- **A margin map runs beside it**, one viewport tall and sticky, its nodes the steps and results and its edges the parentage. Click a node to scroll to its block; read a block and its node lights.
- **Click a node and it opens in a lightbox:** a coding step's wording and the quotes it found, a judging step's rubric and verdict. A quote opens the source around it.
- **You can walk back from any claim.** A result says which results it came from, a figure opens the rows behind it, and clicking a quote opens its source with the words highlighted.
- Rubicon is its own page in Causal Map. It shares the login with Causal Map and reads the project's documents, and past those two things it is not a tab in an existing app.

## Where this sits in the literature

- Scriven's logic of evaluation separates description, "What's so?", from valuing, "So what?", then reaches a verdict through criteria of merit, standards of merit and a synthesis into overall worth (Scriven 1980, 1991; Fournier 1995).
- Davidson puts it as a test: an evaluation must ask not only "What were the results?" but "How good were the results?" Her worked failure is an executive summary of counts and percentages with no verdict in it (Davidson 2014).
- Gargani and King's second principle says the same about worth: "an evaluator cannot ascertain the value of an impact solely by studying it because value is not located within it". The philosophy stays open, and Putnam's argument against the fact and value dichotomy is the standing objection.
- Davidson already advises drafting rubrics before the evidence is gathered, as advice rather than as a dated record. Pre-registration proper has reached evaluation aimed at outcomes and analysis plans, which is the descriptive half (Nosek et al. 2018; Peck and Litwok 2024).
- What we have not found stated is the step after that: treating the advice as a registration with a version trail, a date and a named person, and holding it meaningful for the standard *because* the standard cannot be recovered from the evidence afterwards. Not finding it is one search rather than a proof.

## Open questions

An item leaves when it is decided: built and durable it graduates into the principles above, abandoned it goes without ceremony.

- **Validating a workflow on synthetic contrasting texts.** The `synthesise` step is built, with its refusals: it will not generate from the rubric alone, it will not take a set with no decoys unless you say why, it demands an expected verdict on every document, it will not default the generating model, and it namespaces what it makes as `syn:` so it cannot be mistaken for a real source. What is missing is the last step, the one that compares the verdicts awarded against the verdicts expected and reports the separation as a figure. Design in `rubicon/validate a workflow on synthetic contrasting texts xkTODO xpSTEVE.md`.
    - The texts cannot come from the rubric alone, because a text written to satisfy a rubric uses the rubric's own vocabulary and the judge then finds the words planted for it. Generate from the theory of change and the programme documents, from real transcripts, and from scenarios invented first and banded afterwards by a person.
    - The set needs decoys. A strong account written well and a weak one written badly are easy, and any method scoring nothing but enthusiasm sails through that pair. So the set also holds a warm, admiring document describing nothing anybody did differently, and a grudging, badly written one describing real change in detail.
    - Form: a `synthesise` step, then the ordinary workflow run over what it produced, never a path of its own. Generated documents stored as assets, discrimination reported as a figure rather than as a pass, and generated by a different model from the one that judges.
- **Near-miss reuse.** Identical reuse is settled by hashing the request. What an evaluator meets is a theory of change very like one this project already holds, where rebuilding costs an hour and ten dollars. Two things would make it safe, neither automatic: the difference stated in terms somebody can judge, which links differ and which clause changed, rather than as a similarity score; and the reuse agreed rather than assumed.
- **Building a theory of change, rather than checking one.** Checking is tractable, since each link is a proposition and asking the material what supports it is close to what the app does now. Building is harder: the object is assembled from hundreds of fragments and no fragment contains it, so the categories cannot all be declared in advance and a source read late can change what an earlier passage meant. Causal Map does this well, so the question is what an auditable version looks like when the structure emerges rather than arriving.
- **Running a step at a time from the page.** The engine has `until`, `continue_from` and `rerun`, and the command line reaches them. The page posts a draft and gets back the whole workflow, so the way this app is meant to be used is the way nobody using it can work. The per-step blocks of the single pane are where the control will hang. One naming trap waits there: `runs.status` already uses `partial` for a run whose steps failed, so the workflow-level word has to be a different one.
- **Whether the sample belongs to the workflow or to the run.** Run over twelve sources, then over all fifty-three: intuitively the same workflow twice. The engine disagrees, because the sample lives in a step's `spec` and one id-and-version pair cannot cover two different specs. Unsettled, and the pane needs a run picker whichever way it goes.
- **Forking a workflow from a step**, discarding everything downstream. That makes a new workflow. Not built.
- **A place to disagree.** Overriding a verdict, rewriting a rationale, rejecting a cited quote, recorded beside the machine's version and carried downstream. The principle is above and the surface does not exist.
- **Composite markup.** Assembling one object from evidence scattered across passages, sources and speakers, with every part keeping its own trail. A realist configuration is context in one passage, reasoning in another, an outcome in a third. Today those come together inside a model's rationale, which reads well and cannot be queried. Wanted by more of the work than any other open item.
- **Comparison against what was expected.** A workflow can compare two codings and compute a proportion. It cannot yet read a written expectation and ask the material whether it happened, which would report which links nobody mentioned, something an evaluator cannot get any other way.
- **The draft-to-run link.** A run stores a copy of the workflow it ran rather than the id it came from, so the ledger cannot say which proposal an attempt came from. One column would close it.
- **Project home shows raw column names**, fifteen lines of `s_#Name of province` and the rest, where the reader should see the name a person would use.
- **Flagging a background document has no button.** You type the value into a custom column on the source.
- **Arranging the canvas by asking.** "Show me the quotes, longest first", "put the two codings side by side". Ruby proposes workflows and has no tool that touches the canvas, so today the page shows what it shows. Not built.

Not settled at all:

- Making the unit a person or an organisation rather than a document, when who they are is only discovered during the coding.
- Expressing a base that is not a set of documents, such as "the forty partner organisations", when only twelve appear in the material.
- Pausing a workflow for people to do something in the world, then picking up where it left off.
- Merging results that turn out to describe the same thing, keeping the trail back to every passage that contributed.
- Naming.
