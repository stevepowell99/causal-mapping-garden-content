---
date: 2026-05-29
tags:
  - paper
  - mapcat_methods
---
## Summary: Quality assurance at each step

> In the qualitative space, evaluators have many tools and approaches for reaching robust and rigorous conclusions about causal influences on an outcome of interest, perhaps as the operation of a mechanism. And evaluators are increasingly interested in causal *pathways*: multiple, multi-step, perhaps surprising paths along which influence is passed. How can we reach robust and rigorous conclusions specifically about influences *along* causal *pathways*? This briefing paper claims that *causal mapping* has a long tradition of this kind of thinking. In particular we point to some old and new features within our causal mapping app, Causal Map 4, which can help with this task.

This paper is the quality-assurance (QA) companion to [[901 A workflow for causal coding with and without AI ((ai-coding))|the coding workflow]]. That paper sets out *what you do* at each step. This paper follows the same steps and asks, at each one, how to reach robust and rigorous conclusions. It is built on top of the workflow paper: where that paper describes a tool, we do not describe it again here, we discuss how to use it for QA.

Especially now that AI lets us scale a single project to tens or hundreds of thousands of causal claims, the gap between "we have many claims" and "we have warranted conclusions" is easy to underestimate. Practitioners need practical and transparent ways to get from a claim to a judgement, without overclaiming what the claims can bear.

## From claims to conclusions

Causal mapping, as we practise it, is not a method of causal inference. The fact that twenty people, or twenty thousand, claim that X influences Y does not on its own warrant the conclusion that X really does influence Y. One job of causal mapping is to assemble the claims **so that an evaluator or researcher can make a judgement**. The app does not make that judgement for them. It is a preparatory step which is useful for almost any evaluation approach but especially for theory-based approaches like contribution analysis.

The longer argument for this conservative stance is in our companion [[005 Minimalist coding for causal mapping ((minimalist))|paper]] on minimalist coding and [[011 Our approach clearly distinguishes evidence from facts and does not automatically warrant causal inferences ((evidence-not-facts))|here]]; see also @powellCausalMappingEvaluators2024; @powellDoesOurTheory2023.

The Causal Map app helps at several moments in the quality assurance task.

### A note on "evidence"

We have been criticised for calling the mass of causal claims "evidence": a claim is not really evidence until it has been weighed against something. But Thomas Schwandt disagreed, defining evidence as "information that has a bearing on determining the validity of a claim" -- not as something which is already declared to be valid. We mostly go with Thomas. Moving from coded claims to warranted conclusions is exactly the Rubicon this paper is about. When we use "evidence" loosely, we mean only the body of claims that the evaluator can take into account, not that it has already been judged to be of any particular quality.

We have always assumed that evaluators and researchers using causal mapping and Causal Map will be doing serious quality assurance when crossing the Rubicon from claims to conclusions, but this is the first time that we have tried to address this task in more detail and point out how the Causal Map app can help with quality assurance (QA).

>Sidebar: This is separate from the way causal inference is done specifically in the Qualitative Impact Protocol (QuIP) @copestakeAttributingDevelopmentImpact2019 -- although QuIP projects often use causal mapping, they have a more specialised and specific set of supports for causal inference.

### Solving problems by breaking them down into smaller pieces

Evaluators have primarily addressed the problem of making judgements about causal influences a practical but synthetic problem of making judgements about a *contribution to an outcome*, a judgement which may in fact be about a single causal link or about a pathway or mechanism. So Outcome Harvesting for example often involves making holistic judgements about some kind of path or mechanism from intervention to outcome which is primarily presented as a single problem of "intervention influences outcome?", even though that "mechanism" may have multiple parts. (Of course, mechanisms are fractal.)

From a causal mapping perspective, it gives us a slight headache when evaluators talk about the robustness of evidence for the "causal link" or even "mechanism" from an intervention to an outcome. This holistic perspective, reducing a network of causal pathways to a single link is useful, in fact essential -- it is the last of our steps, but it can gloss over a whole preceding nest of problems within the articulated causal pathways.

In this paper we break that holistic task down across the steps of the workflow.

Causal mapping provides a general, articulated framework to assemble (and then make judgements about) not only individual links (or a single bundle of links) but then about individual links combined into a pathway or network, beginning or ending with any kind of factor, not just outcomes/interventions.

This addresses the formal problem about how causal influences might or might not operate transitively down a causal pathway (if B influences C, and C influences D, does B influence D?).

But there is another formal (and practical) problem about how/if/whether our assessment of the **quality** of individual claims or bundles of claims can be assembled into an assessment of the **quality** of the evidence for a *pathway*: (if we have a validated claim that B influences C, and a validated claim that C influences D, when/how do we have a validated claim that B influence D?)

Quantitative approaches sometimes suggest that they warrant moving from data to evaluative conclusions without any "human in the loop". But at least in the qualitative world, an evaluator or evaluation team has to take responsibility for any conclusions drawn from data -- especially, but not only, in the case of causal inference. All sciences help and inspire us to break problems down into smaller, reusable pieces and recombine to get the final answer. That's what this working paper is about. But however we reassemble our conclusion, we can never rely purely on the algorithm. There is a final holistic judgement to be made, even if it is just the judgement "We paid for an expensive RCT, I trust those guys, let's just publish whatever they say".

## Quality assurance at each step

The steps are not really a simple sequence, and several may be revisited. Only the last is required. Most projects use several, or other overlapping approaches. Steps 1 and 2 of the workflow, planning and data gathering, carry their own quality questions; here we pick up at the codebook.

### QA at Step 3: managing the codebook

See [[901 A workflow for causal coding with and without AI ((ai-coding))#step-3-manage-the-codebook|Step 3]] for the mechanics.

This step may be revisited multiple times. You might start from a Zero Codebook, simply free-coding whatever you see, and you might later revise that codebook one or more times; or you might start from a more-or-less fixed codebook.

Quality Assurance in this step means asking questions like:
- Are my labels consistent? Right level of granularity?
- Whose world view do they reflect?

### QA at Step 4: coding individual links

See [[901 A workflow for causal coding with and without AI ((ai-coding))#step-4-code-the-claims|Step 4]] for the mechanics.

The most important moment for quality assurance is at the time when links are originally coded.

The two things you most want to maximise are Precision (are the links accurately coded?) and Recall, aka Coverage (did we miss any links?). The whole apparatus of coding-style choice, chunk and sample strategy, instruction-writing, and iterations in Step 4 is in the service of these two metrics. The main QA discipline here is the iterative one: test your instruction on a small, varied sample, work out specifically what is causing any problems with accuracy or coverage, tweak, and try again.

A second non-negotiable QA discipline is insisting on a verbatim quote for each and every link. Without it you are no longer showing your working, and as evaluators you cannot really justify the conclusions you draw.

### QA at Step 5: checking individual links

See [[901 A workflow for causal coding with and without AI ((ai-coding))#step-5-check-and-enrich-individual-links|Step 5]] for the mechanics.

In spite of all this effort, and whether you have been coding with AI or doing it yourself, there will still be some mistakes.

The first move is to tag a doubtful or surprising claim, so you can later filter such links in or out. Beyond tags, the **conviction** and **strength** columns let you record, respectively, how sure the source sounds and whether they explicitly call the influence strong or weak.

Two cautions matter for QA here. First, do not read these scales as ordinal (small/medium/large; 1/2/3). They rest on the idea that the default claim is unmarked or neutral, which is not the same as "middling". **The fact that most people do not mention the strength of a causal link when talking about it does not mean they think the links were of "medium" strength.** It just means it did not occur to them to think about or mention the strength, or that the idea of strength is not even useful or applicable in this case. Second, a conviction score is a coding of how confident the *source* sounds, not a coding of the causal strength of the link itself. Keeping that distinction clear is part of not overclaiming what the evidence says.

Source-level columns (for example distinguishing reliable from unreliable sources) feed the same QA purpose: because every link belongs to a source, source reliability becomes available for each link and can be filtered on.

#### Source-level checks

It can also be useful to view the links just from one source to see if they make sense and are consistent. This can involve checking the individual bundles of links between individual pairs of factors -- are they consistent? See the next step. 


### QA at Step 6: the bundle assessment

See [[901 A workflow for causal coding with and without AI ((ai-coding))#step-6-from-claims-to-bundles|Step 6]] for the mechanics. This step warrants its own paper; see [[910 Assessing quality or robustness of evidence for a causal link based on a bundle of coterminal causal claims ((assessing))]] for the detail.

This is the core QA move, and you should do it whether or not you use the app's formal feature for it. Look at each bundle, the claims about one link, with their context, metadata and the link-level judgements from Step 5, and weigh whether the evidence is enough to vouch for the connection. You can leave it there, having weighed the bundles by eye. Or you can record the verdict by collapsing the bundle into a single "assessed link": the underlying claims are not deleted, and a switch shows either the assessed links or the unassessed bundles, never both. Some bundles will earn no assessed link, because the evidence is too thin.

If you formalise it this way, two features keep it auditable rather than arbitrary. First, bundle-level summaries of the link-level judgements from Step 5 (for example, "in most cases conviction was neutral, with a few sources emphasising they were sure") give the human judgement a backdrop and a filter. Second, the app will not let you create assessed links, manually or with AI, until you have written your criteria into a rubric or prompt sub-panel. This is on purpose: the criteria for crossing this part of the Rubicon have to be written down. The rubric might be a five-level scale like the one Jewlya Lynn and colleagues used in their fishing industry retrospective [@HUSeafoodRetrospective], or just yes/no, or several dimensions like "confidence" and "degree of triangulation".

Either way, formal or by eye, the move is from a mass of raw claims to a smaller set you are willing to vouch for: a much cleaner basis for argument. A typical project might go from 1000 raw claims to 30 bundles to 25 assessed links.

Rubrics (at this step but also in steps 7, 8 and 9) can include these three criteria (@astonQualityEvidenceRubrics2023):

- Plausibility (does evidence make a convincing case for the model's contribution, accounting for alternative explanations?);     
- Uniqueness (does evidence point specifically to this model's practices rather than factors that would have produced similar outcomes regardless?); and     
- Triangulation (are claims supported by multiple independent sources, including grantee perspectives?).
    



### QA at Step 7: pathways and the transitivity trap

See [[901 A workflow for causal coding with and without AI ((ai-coding))#step-7-from-bundles-to-pathways|Step 7]] for the mechanics.

Even when each link, or each assessed link, is now well grounded, your work is not finished. The question of this step is how to validate claims for the *transitivity* of causation: how do we get from grounded single links to a grounded multi-step pathway?

From "A influenced B" and "B influenced C" you cannot in general conclude "A influenced C", because the contexts in which each step holds may not overlap. This is [[The transitivity trap ((transitivity-trap))]], the single most important challenge for any approach that uses directed network diagrams. The canonical failure mode is: source 1 says `A -> B`, source 2 says `B -> C`, and we mistakenly conclude that anyone told a coherent story `A -> B -> C`.

Path tracing alone does not protect you from this: it shows every link on a route between your two factors, across all sources, and is easy to misread as a story someone actually told. Source Tracing is the conservative QA move. It keeps only sources that have pathways all the way from A to C, so every link on the map is part of at least one complete story told by at least one source. The app then lets you review the evidence source by source and judge whether each respondent's account is internally coherent. This is also where the **quality**-of-pathway question gets its practical answer: a pathway is only as well warranted as the within-source narratives that support it end to end.

If you have already run a bundle assessment, there is a QA trade-off in the choice to source-trace on the assessed links (clean source and citation counts, but no direct view of the quotes) or on the unassessed ones (the quotes, but a busier map). In practice you may want both, in different views.

### QA at Step 8: value, relative contribution and alternative explanations

See [[901 A workflow for causal coding with and without AI ((ai-coding))#step-8-judge-value-and-relative-contribution|Step 8]] for the mechanics.

Judging value and relative contribution, and comparing with alternative explanations, are central (overlapping but distinct) questions in evaluation which have been really extensively covered, not least by John Mayne [-@mayneAssessingRelativeImportance2019]; for that reason we won't deal with them much here, but QuIP has a lot to say about value, and see @powellTheoriesChangeMaking2019. From a QA point of view, the discipline is to compare the influence you care about against rival explanations on the same map, rather than examining it in isolation. See [[118 Counting and comparing influences ((counting-influences))]] for an approach using path/source tracing.

### QA at Step 9: holistic judgement

See [[901 A workflow for causal coding with and without AI ((ai-coding))#step-9-holistic-judgement|Step 9]] for the mechanics.

Finally, you want to draw a conclusion. You have done some or all of the other steps, checked the individual causal claims, assessed the robustness of co-terminal link bundles, traced paths of influence, compared influences and alternative explanations, and finally you want to at least eyeball all the evidence again and draw a valid conclusion. But "all the evidence" might be a massive corpus. Behind a single map there are still maybe hundreds of causal claims with their associated quotes and context. Does the overall claim still make sense? Can we be sure that the links in all the pathways all belong to the same context?

The AI vignette feature can be tasked with exactly these quality questions, for example: is each link really part of a coherent, complete and consistent story from source factor (e.g. Intervention) to target factor (e.g. Outcome)? A common use is a commentary on the pathways from an intervention to a chosen outcome from the perspective of individual sources, discussing how coherent each source's story is. The AI is doing nothing more than a careful reader could do given the same inputs, and the patience to examine the quotes behind each link, so treat its draft as a starting point for your own judgement and edit it.

## What the app does not do

At no point does the Causal Map app move on its own from claims to facts. Causal mapping as we see it is still, on its own, not a method of causal inference but more of a way to *identify and organise the evidence* in order for the evaluator or researcher to make causal inferences, especially when assisting established methods like Contribution Analysis or QuIP. Still, in the past we have perhaps not done enough to say how exactly to do this or to make it easier to do. This paper hopes to redress that.

The warranting is always the evaluator's. We provide structures (tags, columns, the assessed-link switch, source tracing, vignettes) that make warranting easier, more transparent, and more auditable. We do not provide an engine that turns "twenty people said so" into "therefore it is so".

The opposite design, in which an algorithm rules on causal truth from coded text, would either smuggle in strong assumptions about variables and functional forms (which we argue against in [[0130.2 Our approach is minimalist -- we do not code the strength of a link ((no-link-strength))]] and at length in our minimalist coding paper) or conflate evidence volume with effect size, which Causal Map has always been at pains to avoid. As we put it elsewhere, "a coded link is first and foremost 'there is evidence that a source claims X influenced Y', not a system model with weights or effect sizes" [@powellCausalMappingEvaluators2024].

### How this relates to other strength-of-evidence methods

The bundle and pathway judgements above are our practical contribution to a question the wider causal pathways field takes seriously: how do you assess the strength of evidence behind a causal claim [@apgarHowWeDefine2025]? Some methods build the test in. Process tracing weighs each link with hoop and smoking-gun tests [@befaniProcessTracingBayesian2017; @collierUnderstandingProcessTracing2011]; contribution analysis builds and tests a contribution story [@mayneMakingCausalClaims2012]. Where a method has no such test built in, a written rubric does the same job, agreed in advance of the evidence, as in the CLARISSA programme's quality-of-evidence rubrics [@marinaapgarPARTICIPATORYAPPROACHEXPLORING2024] and Jewlya Lynn's seafood retrospective [@HUSeafoodRetrospective]. The rubric in Step 6 is exactly this device. None of these removes the final evaluative judgement; they make it transparent and auditable.

## None of this is causal inference

None of this is causal inference in a statistical sense. It is a disciplined way to assemble evidence, weigh it transparently, and reach conclusions that you can defend.

This all works, we use it every day in our consultancy work at Causal Map Ltd., but it is still also evolving every day, so if you are interested in going on this journey with us, do get in touch.

>Footnote: The same QA problematic and logic applies even when the links are not strictly causal: in social network analysis or other map-based work, you may still want to go from a mass of raw claims to a smaller set of checked or verified links, even though the links are about relationships rather than causation. Causal Map can do this too, and the mechanics described in the workflow paper work in the same way, though our main focus here is specifically on *causal* links.

<!-- xrefs-v1 -->

## Related

- [[901 A workflow for causal coding with and without AI ((ai-coding))]]: the workflow this paper assures
- [[910 Assessing quality or robustness of evidence for a causal link based on a bundle of coterminal causal claims ((assessing))]]: detail on the bundle assessment step
- [[005 Minimalist coding for causal mapping ((minimalist))]]: the coding stance
- [[011 Our approach clearly distinguishes evidence from facts and does not automatically warrant causal inferences ((evidence-not-facts))]]
- [[The transitivity trap ((transitivity-trap))]]
- [[700 The most controversial feature of causal maps is transitivity ((transitivity))]]
- [[050 Just add rigour Three do’s and don’ts ((add-rigour))]]
