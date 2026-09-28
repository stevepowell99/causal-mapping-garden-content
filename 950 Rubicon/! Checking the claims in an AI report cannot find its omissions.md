---
tags: paper
date: 2026-09-28
theme: theory-of-change
---

*For evaluators and applied social researchers who use AI in qualitative analysis, or assess work that does.*

## The problem

An evaluator has twenty interview transcripts. They ask an AI to write up the findings, and the report has sentences such as "Two farmers credit the training for their bigger harvest (F3 and F7)", "Only F12 mentions a government pension" and "Nobody in the northern district mentions drought". To check it, they give the report and the transcripts to a second AI, or to a colleague, and ask for every sentence to be verified.

The checker does what it is asked. It takes each sentence, finds F3 and F7 in the transcripts and confirms that they credit the training. It catches a wrong name or a misquotation. Usually it does not read every transcript for farmers the report left out, so it passes the sentence even though F9 and F15 credit the training too, and it passes "only F12" without checking that three people mention a pension.

In the terms used to evaluate search engines and classifiers, the check measures **precision**: of the things the report says, how many are right. It does not measure **recall**: of the things in the transcripts that belong in the report, how many the report includes. A report can be precise and still leave out half of what it should have counted.

Missed recall comes in two layers. One is people missing from a finding the report does make, which turns counts into undercounts and makes "only" and "nobody" false. The other is findings the report never makes at all. This page is mostly about the first; the second needs a comparison with another reading of the same material.

## Why it matters

A precision-only check rewards reports that commit to little. "Several farmers, including F3 and F7, credit the training" cannot be caught out on recall, because it never said how many. A report that names every farmer who credits the training, and gives the count, can be caught out on every one it misses. The more complete and checkable a report tries to be, the worse it can look.

The checkers we have used also grade an undercount as minor and a wrongly named person as serious, so the recall misses they do find count for less.

An evaluator checking one AI with another is only one version of this. The fault lies in the direction of the check, whoever makes it: any check that starts from the report and looks for support in the transcripts measures precision, whether the checker is a model or a person.

## Making recall measurable

Recall can be measured only by working the other way: start from each transcript and ask which findings that person belongs in. Done for every person, that is explicit coding, with every case placed on every finding.

We call a report built on that an X-ray. Every finding carries a table of who says it, whose account goes against it, who says it only of other people, and who does not speak to it. Every count comes from the table, and "only" and "nobody" become statements about the table that anyone can check.

The table does not guarantee good recall, because whoever places people can still miss one. What it does is make the misses findable. A checker can read a random handful of whole transcripts, place each of those people on every finding without looking at the table, compare the two, and project the rate of misses to the whole set, the way auditors project errors from a sample of invoices.

## One example

From our own work on Rubicon, our AI qualitative-analysis tool. On 15 long interview transcripts, checking every person against every counted claim found 7 of 24 counts wrong in an answer written without coding each person, nearly all too low; a blind review of the same answer found none of the 7. On 18 short transcripts, a blind review of a report with 12 planted errors found all 12, but graded every plain undercount "not substantive" and the wrong inclusions as substantive.

## What the literature calls it

We did not find a single established name for this. Several literatures describe parts of it.

**Precision without recall.** FActScore, which scores a long AI answer claim by claim, "considers precision but not recall, e.g., a model that abstains from answering too often or generates text with fewer facts may have a higher FActScore" ([Min et al. 2023](https://arxiv.org/abs/2305.14251), section 3.1). Wei et al.'s F1@K adds recall, measured against a preferred number of supported facts ([2024](https://arxiv.org/abs/2403.18802)), which rewards quantity rather than completeness against the source. In summarisation research omission is an error type of its own; Zou et al. built a dataset of omission labels because none was available ([2023](https://aclanthology.org/2023.acl-long.798/)).

**Omission blindness in AI judges.** Zheng et al.'s study of models used as judges examined position, verbosity and self-enhancement bias ([2023](https://arxiv.org/abs/2306.05685)); omission is not among them. A recent preprint names it. Fox et al. call it omission blindness: eight judge designs reading clinical notes against the transcript told a flawed note from its correct twin at 0.79 to 0.94 for added or altered content and 0.50 to 0.63 for omissions, where 0.5 is a coin flip ([2026](https://arxiv.org/abs/2608.31016)). Restructuring the task partly recovered detection, and the restructured task runs from the source: "list the facts the transcript establishes, then check the note for each". AbsenceBench found the same weakness in language models generally ([Fu et al. 2025](https://arxiv.org/abs/2506.11440)). A second model may also share the first model's blind spots: Goel et al. found mistakes growing more similar as models become more capable, "pointing to risks from correlated failures" ([2025](https://arxiv.org/abs/2502.04313)).

**Auditing: the direction of the test.** Auditors separate the claim that recorded items are real (the existence or occurrence assertion) from the claim that everything that should be recorded is (the completeness assertion) ([PCAOB AS 1105](https://pcaobus.org/oversight/standards/auditing-standards/details/AS1105), para .11). They are tested in opposite directions: for completeness, "the procedure should start from the underlying documents and check to the entries in the relevant ledger to ensure none have been missed" ([ACCA](https://www.accaglobal.com/gb/en/student/exam-support-resources/fundamentals-exams-study-resources/f8/technical-articles/assertions.html)). Checking from the record back to the evidence is often called vouching; checking from the evidence forward to the record is tracing ([Vero 2025](https://trullion.com/blog/guide-to-audit-tracing-and-vouching/)). A claim-by-claim review vouches. Where full tracing costs too much, auditors sample and "project the misstatement results of the sample to the items from which the sample was selected" ([PCAOB AS 2315](https://pcaobus.org/oversight/standards/auditing-standards/details/AS2315), para .26). One limit: an invoice is either in the ledger or not, while deciding that someone "said X" is itself coding.

**Why checkers let undercounts go.** Klayman and Ha's positive test strategy is the tendency to test cases expected to have the property in question ([1987](https://pages.ucsd.edu/~mckenzie/KlaymanHaPsychReview1987.pdf)). When the hypothesised set sits inside the true set, as when a report names F3 and F7 and F9 also qualifies, people using only positive tests "can never discover that their rule is incorrect" (p. 214). A tester "may simply be more concerned that all chosen cases are true than that all true cases are chosen" (p. 216). Their subjects were testing their own hypotheses, which a checker is not. Behind this sits the feature-positive effect: adults learn a discrimination more easily when the presence of a feature marks the answer than when its absence does, which the authors take as evidence of "the difficulty organisms experience in using 'nonoccurrence' as a cue" ([Newman, Wolff and Hearst 1980](https://doi.org/10.1037/0278-7393.6.5.630)). Two terms fit less well. Satisfaction of search, missing a second abnormality once one is found ([Adamo et al. 2021](https://doi.org/10.1186/s41235-021-00318-w)), assumes a search for further cases that a checker is never asked to make. Omission bias, judging harmful omissions less bad than harmful commissions ([Spranca, Minsk and Baron 1991](https://doi.org/10.1016/0022-1031%2891%2990011-T)), concerns people's actions.

**Qualitative method and information retrieval.** Negative case analysis, one of Lincoln and Guba's techniques for credibility, is "the constant reworking of hypotheses in light of disconfirming evidence" ([Phillips et al. 2014](https://doi.org/10.1186/s12913-014-0559-4), tabulating Lincoln and Guba): the analyst's discipline of reading beyond the claim. Information retrieval meets the counting problem head on: missed items are absent from the results, so recall is estimated "by assessing a random sample of documents", including documents the search did not return ([Webber 2012](https://arxiv.org/abs/1202.2880)).

## Sources

- Adamo, S. H., Gereke, B. J., Shomstein, S. and Schmidt, J. (2021). [From "satisfaction of search" to "subsequent search misses": a review of multiple-target search errors across radiology and cognitive science](https://doi.org/10.1186/s41235-021-00318-w). *Cognitive Research: Principles and Implications*, 6.
- ACCA. [The audit of assertions](https://www.accaglobal.com/gb/en/student/exam-support-resources/fundamentals-exams-study-resources/f8/technical-articles/assertions.html). Technical article for ACCA students.
- Fox, S., Markham, L., Lail, R. and Karotsieris, M. (2026). [LLM judges verify presence, not absence: omission blindness in AI clinical notes and what recovers it](https://arxiv.org/abs/2608.31016). arXiv preprint 2608.31016.
- Fu, H. Y., Shrivastava, A., Moore, J., West, P., Tan, C. and Holtzman, A. (2025). [AbsenceBench: language models can't tell what's missing](https://arxiv.org/abs/2506.11440). arXiv 2506.11440.
- Goel, S. et al. (2025). [Great models think alike and this undermines AI oversight](https://arxiv.org/abs/2502.04313). arXiv 2502.04313.
- Klayman, J. and Ha, Y.-W. (1987). [Confirmation, disconfirmation, and information in hypothesis testing](https://pages.ucsd.edu/~mckenzie/KlaymanHaPsychReview1987.pdf). *Psychological Review*, 94(2), 211–228.
- Min, S. et al. (2023). [FActScore: fine-grained atomic evaluation of factual precision in long form text generation](https://arxiv.org/abs/2305.14251). EMNLP 2023.
- Newman, J., Wolff, W. T. and Hearst, E. (1980). [The feature-positive effect in adult human subjects](https://doi.org/10.1037/0278-7393.6.5.630). *Journal of Experimental Psychology: Human Learning and Memory*, 6(5), 630–650.
- PCAOB. [AS 1105: Audit Evidence](https://pcaobus.org/oversight/standards/auditing-standards/details/AS1105).
- PCAOB. [AS 2315: Audit Sampling](https://pcaobus.org/oversight/standards/auditing-standards/details/AS2315).
- Phillips, C. B., Dwan, K., Hepworth, J., Pearce, C. and Hall, S. (2014). [Using qualitative mixed methods to study small health care organizations while maximising trustworthiness and authenticity](https://doi.org/10.1186/s12913-014-0559-4). *BMC Health Services Research*, 14.
- Spranca, M., Minsk, E. and Baron, J. (1991). [Omission and commission in judgment and choice](https://doi.org/10.1016/0022-1031%2891%2990011-T). *Journal of Experimental Social Psychology*, 27, 76–105.
- Vero, Y. (2025). [Audit tracing and vouching: a complete guide](https://trullion.com/blog/guide-to-audit-tracing-and-vouching/). Trullion blog.
- Webber, W. (2012). [Approximate recall confidence intervals](https://arxiv.org/abs/1202.2880). arXiv 1202.2880; later in *ACM Transactions on Information Systems*.
- Wei, J. et al. (2024). [Long-form factuality in large language models](https://arxiv.org/abs/2403.18802). arXiv 2403.18802.
- Zheng, L. et al. (2023). [Judging LLM-as-a-judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685). NeurIPS 2023 Datasets and Benchmarks Track.
- Zou, Y., Song, K., Tan, X., Fu, Z., Zhang, Q., Li, D. and Gui, T. (2023). [Towards understanding omission in dialogue summarization](https://aclanthology.org/2023.acl-long.798/). *Proceedings of ACL 2023*, 14268–14286.
