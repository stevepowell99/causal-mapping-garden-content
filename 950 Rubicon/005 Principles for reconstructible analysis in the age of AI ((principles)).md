---
tags: paper
theme: theory-of-change
---

*For evaluators who use AI to analyse interviews, reports and other text, and for the people who commission their work.*

These are the principles we work to when AI does some or all of an analysis of text. We developed them while building [[000 Pilots, not passengers -- reconstructible reporting in evaluation ((rubicon))|Rubicon]], but they apply whichever tool or model is used, and most of them apply to analysis done entirely by people. The [[003 An open format for reconstructible reporting ((open-format))|open format]] is one way of meeting them.

> **Work in progress.** Comments welcome.

### The model does the work; the record makes it trustworthy

Frontier models improve faster than any purpose-built tool can keep up with, so we do not try to out-analyse them. What a tool or a procedure can add is a record of the work that somebody else can read, check and run again. An evaluator cannot put their name to "the model says it did this", however good the model is, because a model describing its own work is still only describing it.

We treat two kinds of addition differently.

- Help with the analysis, such as guidance on building a codebook or on breaking down a question, is temporary. We measure each piece against the bare model, and again when a new model comes out, and drop it once the bare model does as well without it.
- Checks stay. Counting by code instead of by the model, finding every quotation in its source document, a second reading by somebody who did not see the first, and a record from which the work can be rerun: a stronger model does not make any of these unnecessary, any more than competent accountants make audits unnecessary.

### Worth is declared by a person

The AI does not decide what counts as good. A person sets the standard, in advance and under their own name, and the AI applies it to the material and shows how. Julian King made the objection in October 2025 that AI should not be making evaluative judgements about human affairs, and the evidence-synthesis bodies draw the line in the same place, where a model makes or suggests a judgement [@flemyngPositionStatementArtificial2025]. We agree.

Nothing in the material tells you where "adequate" begins, and a standard chosen after seeing the numbers can be fitted to any of them. So an AI assistant can show where a threshold has to go, but the evaluator supplies the threshold.

A standard is usable only if each level says what it takes to reach it, in enough detail for somebody to hold it against real material. "Green: every partner described a change they could date and name a cause for" is a standard. "Green" on its own is a label.

People also need a way to disagree with a verdict: to override it, rewrite the reasoning, reject a quotation or mark a criterion as unanswerable. The override is recorded beside the original verdict, with who made it and when, and everything downstream uses it.

### Every claim points at a quote

Every claim in an answer should lead back to the passages it rests on, and every number should be a count that somebody can check [@moravcsikTransparencyRevolutionQualitative2014]. When this goes wrong, nobody can see that it has: two steps away from the sources the prose still reads well and the numbers still look precise.

An AI can easily reach a conclusion first and then look for quotations to support it. So a report should say whether the passages were coded before the answer was written or cited for an answer already written. Citing afterwards shows that every quotation is real and every count is right. It does not show that the passages cited are all the documents hold.

Some findings are about the method, such as whether anybody looked for contrary evidence, and these point at the record of the work.

### Say what you did not read

Every number is stated out of what was read, and the base includes the documents that said nothing. A base made only from the documents that mentioned something makes a rare finding, such as unintended harm, look commoner than it is. "28 of the 718 achievements coded mention the embassy, and those 718 came from 40 of the 142 documents" tells the reader that 28 is a floor for the whole corpus.

After a partial reading, an absence is an absence in the search: "No passage on childcare in any of the thirty-seven interviews read", never "Nobody mentioned childcare". A claim that something was never mentioned needs the search behind it: what was looked for, in which documents, and how much of each was read.

### Say what you are comparing against

"The programme did well" invites the question: compared with what? The answers are not interchangeable. It might be a share of the cases, a competing explanation, a rubric agreed in advance, a comparison case, the targets in the theory of change, or what would have happened anyway. Sometimes the finding is that nothing is well enough evidenced to say. Counting how many people said something does not tell you whether it was any good.

Look for evidence against a claim as hard as for evidence for it. Where a codebook or a threshold is developed by reading the material, develop it on part of the material, or on similar material from elsewhere, and apply the settled version to the rest.

### Break down questions that cannot be checked as asked

"Read the documents and tell me whether the project was effective" produces a confident verdict without a stated standard or anything specific to disagree with. "Summarise these documents" has the same problem on a smaller scale. Questions like these need breaking into steps somebody else could repeat, each with its own standard. "Is this a good project?" is four questions: good for whom, compared with what, against whose standard, and how much of that this material can answer.

No question is too soft to ask because it concerns tone or feelings. What matters is whether it is well defined.

### Leave statistics to statistics

An analysis of text cannot produce effect sizes, difference-in-differences estimates, power calculations or regressions, and a version improvised from counts would be wrong in a way no reader could see. The useful answer says what analysis is needed, that somebody with the data and a statistics package has to do it, and what the text can contribute, which is usually what people said about the change and why. A difference between small groups in a table is not a finding however large it looks, and a small difference does not show that the groups are alike.

### Write for a reader who was not there

The report goes to people who took no part in planning the analysis. Its definitions, its standard and each of its steps are written in their terms, without internal labels or anything that depends on the conversation in which the analysis was planned.

[Rubicon for Claude](https://rubicon.causalmap.app/plugin) and the Rubicon app both work to these principles.

*This page was drafted with the assistance of Claude, an AI model from Anthropic; the arguments and judgements are our own.*
