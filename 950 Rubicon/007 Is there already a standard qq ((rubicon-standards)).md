---
tags: paper
date: 2026-09-07
theme: theory-of-change
---

# Is there already a standard for this?

Before publishing [[003 An open format for reconstructible reporting ((open-format))|an open format for reconstructible reporting]], we looked for an existing open standard for specifying a qualitative text-processing workflow in evaluation. This page lists what we found, so that anyone who thinks one already exists can check our search.

We did not find one, or even a draft of one. Several standards have one of the properties such a standard would need. We did not find any that has two.

> **Work in progress.** We made this survey in September 2026 and last checked it on 15 September 2026. We have not done a literature review. Below we say what we looked at and what we could not verify.

## Three properties a standard would need

A useful standard would need all three of these.

- **Be executable.** Software runs the analysis from the specification itself, so nobody has to fill in a description afterwards.
- **Trace each claim to a quotation.** Each assertion in a report is linked to the span of source text that supports it.
- **Fix the rules before reading.** The evaluator registers the decision rule, including any threshold or rubric, with a date and a version, before anyone reads the material.

We found each property in some existing standard. The W3C Web Annotation Data Model, a Recommendation since February 2017, deals with anchoring. It identifies a passage by the words it contains as well as by its character offsets, so the reference still works after someone edits the document. Canada's Algorithmic Impact Assessment is a computable decision rule; its weights and thresholds are encoded in the questionnaire. Workflow languages such as the Common Workflow Language and packaging standards such as RO-Crate describe a run and its provenance in machine-readable form.

Each of these does one job. Web Annotation has nothing on what questions to ask of a text. The Algorithmic Impact Assessment applies its rule to free-text answers without any evidence attached to them, and the workflow standards record which files a run read and wrote but not which passage supports which assertion. We did not find a standard that combines them.

## What the evaluation profession publishes

What the profession publishes falls into three groups. We did not find such a standard in any of them.

- **Ethics and quality principles.** The Program Evaluation Standards, the American Evaluation Association's Guiding Principles, the OECD DAC quality standards, the UNEG norms. These are prose guidance for judgement and do not describe any analysis procedure. The first guidance on AI is of this kind too. The UK Evaluation Society's [AI in evaluation: good practice guidelines for practitioners](https://evaluation.org.uk/new-ai-guidance-launched-for-evaluators/) (November 2025) sets out four principles: transparency and competence, human control, risk management, quality assurance. The Society asks for disclosure proportionate to the risk and gives sample wording for a report: "This evaluation used artificial intelligence tools to support [specific functions]. All AI-generated outputs were verified through [specific verification methods]." For peer review it asks for "detailed documentation enabling methodological scrutiny, including specific tools used, verification approaches, quality assurance measures". The evaluator decides what that documentation contains and in what form. Montrosse-Moorhead's criteria domains for assessing AI use in evaluation are a framework for judging that use, and do not include a form for recording it [@montrosse-moorheadEvaluationCriteriaArtificial2023]. We have heard that the JCSEE, the AEA and the EES are considering AI in their own standards, but we have not seen anything published.
- **Reporting checklists.** COREQ, SRQR, ENTREQ, RAMESES, PRISMA, and for evaluation itself CHESS, the checklist of evaluation-specific standards, which lists the minimum a written evaluation report must contain before anyone can judge its quality ([Montrosse-Moorhead and Griffith, 2017](https://doi.org/10.1177/1098214017699275)). These standardise what you must say you did.
- **Data formats and inference engines.** REFI-QDA for coded data, the QCA packages, Bayesian process-tracing tools. All are machine-readable. Each of them begins after the step where text becomes data.

Each method formalises every step except the one applied to the words themselves. Qualitative comparative analysis formalises Boolean minimisation and then describes calibration as an interpretative act. Formal process tracing provides a vocabulary for classifying evidence once the inference is made, but does not give any procedure for assigning a passage to a class [@ricksProcessTracingResearchDesigns2018]. Outcome Harvesting specifies six steps; who substantiates an outcome, and how many people to ask, depend on the credibility the intended use requires [@wilson-grauOutcomeHarvestingPrinciples2018]. The Most Significant Change guide says that selection criteria should emerge through discussion instead of being decided in advance. It offers five incompatible ways of deciding, does not name a default, and does not require anyone to record which one was used [@daviesMostSignificantChange2005].

The profession has considered the question and decided against formalising this step. The Magenta Book's own guide to quality in qualitative evaluation says its framework was "devised to aid informed judgement, not mechanistic rule-following", and adds that "in qualitative research, there are no 'validated' instruments or standardised methods". Its last appraisal question, on auditability, is "How adequately has the research process been documented?", and the indicators under it are written in prose. Most evaluators in fact practise bricolage (mixing and adapting methods to the case in hand). The authors cited here defend the practice [@astonArtCraftBricolage2022; @apgarRethinkingRigourEmbrace2024].

An open format for reconstructible reporting therefore has to work with judgement in the analysis. It can record where each judgement was made, and on what material.

## REFI-QDA, the one standard for qualitative data

Qualitative analysis does have one interchange standard. REFI-QDA, published in 2019 under an MIT licence, lets users move a coded project between ATLAS.ti, MAXQDA, NVivo, Dedoose, Quirkos and other packages, and independent developers have built tools around it. A REFI-QDA file contains the documents, the codebook, the coded segments and their character offsets.

That is the result of an analysis. How the analyst reached it is not part of the format: the words *audit*, *provenance*, *workflow* and *history* do not appear anywhere in the sixty pages of the specification. Each coding is stamped with who made it and when, but the format does not provide any way to show that a coding was ever revised. The codebook is not versioned at all.

The specification defines a user as "A person who has worked on a project." There is no agent type, so a model that codes a corpus can appear in a REFI-QDA file only if someone enters it as a person. The authors are candid about their scope: round-tripping "may not work without data loss", and "the focus in developing the standard was only on exchange".

## What comes closest

Two efforts outside evaluation come closer than anything within it.

The **Reproducible Open Coding Kit** is the only standard we found that was designed to record the process of coding as well as its data [@petersReproducibleOpenCoding2026]. The coder writes codes, utterance identifiers and a codebook into the source file using plain-text conventions, so both a person and a machine can read the whole analysis. Because the files are plain text under version control, the coding history can be reconstructed. It is a small academic project without support from any commercial software. In our view the approach is right.

The **joint position statement on AI in evidence synthesis**, issued on 10 November 2025 by Cochrane, the Campbell Collaboration, JBI and the Collaboration for Environmental Evidence, is the closest any body has come to publishing a testable rule [@flemyngPositionStatementArtificial2025]. It requires that "Authors should declare when they have used AI if it makes or suggests judgements". It lists the judgement tasks it means: eligibility, risk of bias, data extraction, synthesis, certainty assessment. We have not found any tool that implements it.

## Two measurements

One study replicated 37 annotation tasks from 21 published social science studies, across 18 models and 13 million labels. Even with the best models, it found incorrect conclusions for about 31% of hypotheses, and its authors showed that "with just a handful of prompt paraphrases, virtually anything can be presented as statistically significant" [@baumannLargeLanguageModel2025]. Current standards do not require anybody to write down the configuration choices that produce this variation.

A second study looked at what researchers report. Of 75 studies that used large language models in qualitative research between 2020 and 2025, 75% reported no parameter settings at all; 13 gave a temperature and 4 gave a top_p value. Agreement between model and human coders ranged from 36% to 99% [@kempnyUseMethodologicalReporting2026]. The reports do not contain the information a reader would need to tell which studies are at the good end of that range.

The problem is older than the technology. The case for making qualitative claims traceable to the passages behind them was made well before language models [@moravcsikTransparencyRevolutionQualitative2014]. Authors are now arguing that the technology can strengthen the commitments of qualitative inquiry instead of threatening them [@wiseWhyAINot2026]. What is new is that a model reading the text can be made to show its working, so there is less excuse for not showing it.

## Two gaps

The first gap is the combination. Anchoring, computable decision rules and run provenance each have a standard of their own. We did not find anything that puts the three together.

The second gap is in evaluation itself. The only registered reporting guideline for qualitative work with language models is an extension of COREQ. Its protocol was published in September 2025 with a target of December that year, and on 15 September 2026 the EQUATOR Network still listed it as under development. It is a prose checklist and covers neither traceability nor pre-registration. It is also aimed at health research, so an executable specification for evaluation would not overlap with it.

The [[003 An open format for reconstructible reporting ((open-format))|open format for reconstructible reporting]] is our attempt to fill the second gap. We designed it so that the first could be filled as well. Rubicon is one implementation of the format: see [rubicon.causalmap.app](https://rubicon.causalmap.app) for what it does and [[005 Principles for reconstructible analysis in the age of AI ((principles))|the principles page]] for the principles behind it.

## What we checked, and what we could not

We searched the evaluation profession's standards bodies and method manuals, the qualitative data and annotation formats, the workflow and provenance standards, the reporting-guideline family indexed by EQUATOR, and the AI transparency and audit instruments including the EU AI Act, the ISO/IEC 42000 series and the national algorithm registers.

We took each quotation from the REFI-QDA specification, the Magenta Book guide, the UK Evaluation Society guidance, the Cochrane and partners position statement, and the two studies cited for figures from the original document, never from a summary. Where this page says that something does not exist, it means our search did not find it.

We dropped one claim. The Dutch national algorithm register is the best-specified public register we saw, with a published schema and bulk export. Reports say that in a large majority of its entries the impact-assessment field is left empty, but we could not reach the data to check the proportion, so we do not give a figure. We would have used it to make a simple point. Publishing a schema does not by itself get a field filled in; people complete a standard only when they have a reason to.

*This page was drafted with the assistance of Claude, an AI model from Anthropic; the arguments and judgements are our own.*
