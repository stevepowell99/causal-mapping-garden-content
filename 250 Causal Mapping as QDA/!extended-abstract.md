---
title: "Extended abstract: An orthogonal yes: minimalist causal mapping as an accountable use of AI in qualitative analysis"
subtitle: "Submitted for the special issue *AI-Assisted Qualitative Analysis: Human Reasoning, Accountability, and Ethics*, Text & Talk"
author: "Stephen Powell (Causal Map Ltd). Remove for double-blind review."
date: "2026"
bibliography:
  - ../../../../MyLibrary.bib
  - ../assets/extra-refs.bib
---
## Theoretical and analytical orientation

The debate about generative AI in qualitative analysis is usually drawn as a line between rejecting the technology to protect non-positivist, meaning-based practice [@jowseyWeRejectUse2025] and embracing it to work at scale @frieseBinaryPositionsMaking2026 . We take a position orthogonal to that line. We share the anti-positivist instinct that a research question cannot be completely reduced to a decision procedure an algorithm can execute, and we do not claim that our method is useful on its own for reflexive, Big-Q thematic work in the sense developed by Braun and Clarke [@braunGoodPracticeThematic2023; @braunReportingGuidelinesQualitative2025]. 

The method we use is a minimalist version @powellCausalMappingEvaluators2024 of causal mapping [@axelrodAnalysisCognitiveMaps1976; @edenCognitiveMapping1988; @powellCausalMappingEvaluators2024; @narayananCausalMappingHistorical2005] in which the causal coding is carried out by a large language model (LLM). Causal mapping is not itself a discourse- or interaction-analytic method, but it stays close to the journal's central commitment. Each coded unit is a causal claim a source makes in their own words, along with the verbatim quote and the identity of the source who said it. 

In 2026 it is easy to use an LLM to auto-code codes within a text; but what codebook to use? The for this to be useful and produce meaningful results 

For a large class of applied questions which can be answered by focusing on people's mental models of what causes what, a deliberately generic *causal mapping* approach is surprisingly useful.

The orientation is small-q and exploratory. The unit of analysis is a single causal claim made by a source.  The dataset of such claims is a links table, and that table, rather than a narrative, is the core qualitative product. It has a recognisable relative in Mayring's rule-guided qualitative content analysis [@mayringQualitativeContentAnalysis2000], differing in that its unit is an ordered pair, which is what makes pathway analysis possible.

A bridge to the interpretive tradition runs through the difference between a code and a theme. On Braun and Clarke's own account, a real theme is not a topic summary but a meaning-based interpretive story built around a central organising idea: it could not have been written before the analysis, because it says something in relation to the research question [@braunGoodPracticeThematic2023]. A finding, in other words, is answer-shaped. Causal claims are one species of answer-shaped finding, and causal mapping captures that species at scale while keeping each instance tied to its evidence.

## Connection to the special issue theme

The call asks how computational tools can enter qualitative workflows without compromising interpretive rigour, methodological reflexivity, and accountable links between analytic claims and empirical materials, and it asks specifically about AI-assisted analytic exploration that identifies phenomena for closer inspection rather than as an analytic end product. 



This paper answers with a suggestion which is somewhat orthogonal to that argument: a minimalist form of causal mapping in which the task given to the large language model is a restricted, locally checkable extraction not of ordinary codes but of causal claims. It speaks directly to the issue's themes of the limits of automation, the role of human judgement, and auditability in AI-supported workflows.


## Data and methodology

The methodological argument is illustrated with a corpus of 48 interviews on the experience of loneliness among young adults aged 18 to 24, recruited from four deprived London boroughs in 2019 and available as a de-identified open dataset [@fardghassemiQualitativeOutput2022]. The corpus is analysed in three contrasting ways, which together clarify the position.

First, a causal-mapping pass. Each interview is processed in short chunks. The model is given one instruction: identify each passage where the text says one thing influenced another, and for each record the cause, the effect, and the exact supporting quote. The corpus-level structure is recovered by aggregating the resulting links, around 3,392 quote-grounded causal claims produced in roughly twenty minutes. The analyst then queries the links table with explicit, reversible operations: which factors are most often said to drive an outcome, how pathways differ across subgroups, which claims are contested. This is a qualitative version of the split-apply-combine strategy [@wickhamSplitApplyCombineStrategyData2011]: the model splits, a deterministic pipeline applies, and the human combines. The division of labour is strict. The model is a clerk that proposes quote-backed candidate links; the human is the architect who frames the question, curates the factor vocabulary, designs the pipeline, and writes the interpretation. Evidence that narrow, codebook-anchored extraction is the usable regime for LLM coding [@xiaoSupportingQualitativeAnalysis2023], and a validation study of AI-assisted causal mapping in particular [@powellAIassistedCausalMapping2025], support treating this one step as reliable enough to be worth automating.

Second, for contrast, a fully autonomous AI thematic pass on the same data, in which an agent was given the transcripts and a high-level instruction and developed and applied a thematic method on its own, producing a readable account of four "mechanism stories". This is neither our position nor the dialogic one: there was no real conversation, and the machine ran the whole interpretation itself, which makes it, oddly, the most positivist of the three. On checking, some of its quotations were not verbatim, one was attributed to the wrong interview, and some of its claims about its own process overstated what had been done. These are exactly the errors that handing interpretation wholesale to a model makes hard to catch.

Third, by reference, the human-AI dialogue that conversational frameworks prescribe [@frieseConversationalAnalysisAI2025; @morganQueryBasedAnalysisStrategy2025; @nguyen-trungNarrativeIntegratedThematicAnalysis2026], in which the analyst keeps interpretation by staying in the exchange. The comparison shows that in both the dialogic and the autonomous cases the quote must be requested and then verified after the fact, whereas in causal mapping the quote is the unit of coding, present on every link by construction.

## Main claims in relation to the literature

1. The choice between rejecting and embracing AI is a false one for questions about what people say causes what. A one-way pipeline, narrow extraction, then deterministic transforms, then human synthesis, is more accountable than a conversation precisely because it is not a conversation.

2. The position withstands the strongest objections in the current literature. To the methodological-incongruence and skeuomorphism argument [@nguyentrungMethodologicalIncongruence2025], we answer that our links table is not a memory crutch imposed on the model, which is stateless across chunks, but an audit artefact for humans and readers; holding the analysis "in the model's head" is the move that reinstates the black box. To the empirical bias finding that LLM coding errors are systematically non-random [@ashwinUsingLargeLanguage2025; @weiCulturalAlignmentBiases2025], we answer that our workflow relocates bias into an explicit, shareable prompt and makes each unit checkable against its quote, and that the bias literature's own remedy, a narrow model trained on human-coded samples, points toward checkable coding rather than holistic synthesis. To the post-coding claim that the future is dialogic [@frieseConversationalAnalysisAI2025; @morganQueryBasedAnalysisStrategy2025], we answer that the dialogic paradigm puts the analytic state where it cannot be reproduced, and that even its proponents concede there is no guaranteed way to detect AI bias or to prevent fabricated quotes [@morganQueryBasedAnalysisStrategy2025]. To the deflationary objection that the labour has merely moved into prompt-fiddling, we answer that the concentration of judgement at a few explicit, shareable moments is the gain.

3. The anti-positivist rejection and our position are orthogonal rather than opposed. The reject letter scopes its refusal to Big-Q reflexive work and concedes that rule-governed techniques such as content analysis can be automated [@jowseyWeRejectUse2025]; our narrow extraction falls on the automatable side of its own line. This extends, rather than contradicts, calls to move beyond binary acceptance and rejection [@frieseBinaryPositionsMaking2026; @depaoliWhyShouldReject2026].

## AI-use declaration

- **Type.** Commercial large language models, used at the extraction step only; specific model versions are reported because behaviour changes across versions.
- **Role.** The model proposes candidate causal links from short text chunks, each paired with a verbatim quote. It does not summarise across documents, choose the codebook, write the report, or make any claim about the world.
- **Analytic accountability.** Every link is traceable to a specific quote and source; every step beyond extraction is deterministic and human-authored; the extraction prompt functions as a shareable codebook; the links table can be inspected line by line.
- **Legal and ethical accountability.** The illustrative corpus is a published, de-identified open dataset used under its own consent and licensing terms, so no new personal data was processed for this paper. For sensitive material in applied use, training on input is disabled where the provider allows it, and consent, confidentiality and removal of identifying information are handled at the chunking stage before any text reaches the model.

The full paper develops the argument and the worked comparison in detail, with practical guidance on the workflow and a full account of its limits.
