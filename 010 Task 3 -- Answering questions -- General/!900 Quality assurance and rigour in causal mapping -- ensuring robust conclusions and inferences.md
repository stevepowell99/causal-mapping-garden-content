---
tags:
  - paper
  - mapcat_methods
date: 2026-04-25
---
DEPRECATED DEPRECATED, CONTENTS MOVED

## Summary: Quality Assurance in causal mapping

> In the qualitative space, evaluators have many tools and approaches for reaching robust and rigorous conclusions about causal influences on an outcome of interest, perhaps as the operation of a mechanism. And evaluators are increasingly interested in causal *pathways*: multiple, multi-step, perhaps surprising paths along which influence is passed. How can we reach robust and rigorous conclusions specifically about influences *along* causal *pathways*? This briefing paper claims that *causal mapping* has a long tradition of this kind of thinking. In particular we point to some old and new features within our causal mapping app, Causal Map 4, which can help with this task. 

Especially now that AI lets us scale a single project to tens or hundreds of thousands of causal claims, the gap between "we have many claims" and "we have warranted conclusions" matters more than ever. Practitioners need ways to cross the Rubicon from claim to judgement that are practical, transparent, and modest in their epistemic commitments. 

## Seven moments for quality assurance

1) Managing the codebook
2) Coding individual claims
3) Checking individual claims
4) Moving from claims to bundles
5) From bundles to pathways
6) Judging value and relative contribution
7) Holistic judgements: the whole thing

We will cover them all in more detail in the rest of this paper. Only the last moment is required. Most projects use several, or other overlapping approaches. 

## About causal mapping

Causal mapping is a way of analysing qualitative data, what people say in interviews, focus groups, reports or any written source, when you want to understand what these sources think causes what. An analyst reads through the material and codes each causal claim ("the rains ruined the harvest", "the training raised her confidence") as a *link* from one factor to another. Combining links from multiple sources, and you have a causal map: a network showing which factors people believe influence which others. For a longer introduction, see [[0.10 Causal mapping helps make sense of many causal claims from many sources ((make-sense))|this]] and [[0.03 A causal map consists of multiple links where a link from X to Y means someone believes X influences Y ((causal-map-links))|this]]. 

Causal mapping is like systems mapping, but rather than jumping straight to modelling real causal connections in the world, we first model the multiple *cognitions* or *beliefs* or *claims* made by multiple sources about each link, before (perhaps) making inferences about the world.

### From claims to conclusions 

Causal mapping, as we practise it, is not a method of causal inference. The fact that twenty people, or twenty thousand, claim that X influences Y does not on its own warrant the conclusion that X really does influence Y. One job of causal mapping is to assemble the claims **so that an evaluator or researcher can make a judgement, not to make the judgement for them**. It is a preparatory step which is useful for almost any evaluation approach but especially for theory-based approaches like contribution analysis. 

The longer argument for this conservative stance is in our companion [[005 Minimalist coding for causal mapping ((minimalist))|paper ]]on  minimalist coding and [[011 Our approach clearly distinguishes evidence from facts and does not automatically warrant causal inferences ((evidence-not-facts))|here]]; see also @powellCausalMappingEvaluators2024; @powellDoesOurTheory2023.

The Causal Map app helps at several moments in the quality assurance task. 
### A note on "evidence" 

We have been criticised for calling the mass of causal claims "evidence": a claim is not really evidence until it has been weighed against something. But Thomas Schwandt disagreed, defining evidence as "information that has a bearing on determining the validity of a claim" -- not as something which is already declared to be valid. We will go with Thomas.  

Moving from coded claims to warranted conclusions is exactly the Rubicon this paper is about. When we use "evidence" loosely, we mean only the body of claims that the evaluator can take into account, not that it has already been judged to be of any particular quality. 

We have always assumed that evaluators and researchers using causal mapping and Causal Map will be doing serious quality assurance when crossing the Rubicon from claims to conclusions, but this is the first time that we have tried to address this task in more detail and point out how the Causal Map app can help with quality assurance (QA). 

>Sidebar: This is separate from the way causal inference is done specifically in the Qualitative Impact Protocol (QuIP) @copestakeAttributingDevelopmentImpact2019 -- although QuIP projects often use causal mapping, they have a more specialised and specific set of supports for causal inference.

---------

### Solving problems by breaking them down into smaller pieces 

Evaluators have primarily addressed the problem of making judgements about causal influences a practical but synthetic problem of making judgements about a *contribution to an outcome*, a judgement which may in fact be about a single causal link or about a pathway or mechanism. So Outcome Harvesting for example often involves making holistic judgements about some kind of path or mechanism from intervention to outcome which is primarily presented as a single problem of "intervention influences outcome?", even though that "mechanism" may have multiple parts. (Of course, mechanisms are fractal.)

From a causal mapping perspective, it gives us a slight headache when evaluators talk about the robustness of evidence for the "causal link" or even "mechanism" from an intervention to an outcome. This holistic perspective, reducing a network of causal pathways to a single link is useful, in fact essential -- it is the last of our "moments", but it can gloss over a whole preceding nest of problems within the articulated causal pathways. 

In this paper we will try to break down this holistic task into six different moments.

Causal mapping provides a general, articulated framework to assemble (and then make judgements about) not only individual links (or a single bundle of links) but then about individual links combined into a pathway or network, beginning or ending with any kind of factor, not just outcomes/interventions.  

This addresses the formal problem about how causal influences might or might not operate transitively down a causal pathway (if B influences C, and C influences D, does B influence D?). 

But there is another formal (and practical) problem about how/if/whether our assessment of the **quality** of individual claims or bundles of claims can be assembled into an assessment of the **quality** of the evidence for a *pathway*: (if we have a validated claim that B influences C, and a validated claim that C influences D, when/how do we have a validated claim that B influence D?) 

Quantitative approaches sometimes suggest that they warrant moving from data to evaluative conclusions without any "human in the loop". But at least in the qualitative world, an evaluator or evaluation team has to take responsibility for any conclusions drawn from data -- especially, but not only, in the case of causal inference. All sciences help and inspire us to break problems down into smaller, reusable pieces and recombine to get the final answer. That's what this working paper is about. But however we reassemble our conclusion, we can never rely purely on the algorithm. There is a final holistic judgement to be made, even it is just the judgement "We paid for an expensive RCT, I trust those guys, let's just publish whatever they say".

## The seven QA moments
### 1: Managing the codebook

These seven tasks are not really a simple sequence, and in particular this first task may be revisited multiple times, see [[! 100 AI coding overview|Coding Overview]]. You might start from a Zero Codebook, simply free-coding whatever you see, and you might later revise that codebook one or more times; or you might start from a more-or-less fixed codebook. 

Quality Assurance in this "moment" means asking questions like: 
- Are my labels consistent? Right level of granularity? 
- Whose world view do they reflect? 
### 2: Coding individual links

The most important moment for quality assurance is at the time when links are originally coded. 

The two things you most want to maximise are Precision (are the links accurately coded?) and Recall, aka Coverage (did we miss any links?).

[[! 100 AI coding overview]]

### 3: Checking individual links

In spite of all this effort, and whether you have been coding with AI or doing it yourself, there will still be some mistakes.

Raw, individual claims can be quality-checked by looking at the source metadata, the context and the surrounding text and then perhaps qualified with a tag as needed, e.g. as `Doubtful` or `Surprising`.


![[007 Task 2 -- Causal coding -- minimalist style/img/map-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con.jpg]]

In this kind of approach, as opposed to, say, systems mapping, you often get *bundles* of *multiple* links between any one particular cause and one particular effect: [[010 Bundle of Links -- definition]]. The links within each "bundle" represent different claims about the same causal link -- from different sources, or different places within the same source text. 

The first step to quality assurance of a claim is to tag it. The Causal Map app, following other forms of QDA, has always allowed free-form tags at the link level. A tag like `#doubtful`  records a misgiving while coding. Later, you can filter such links in or out. Tags are freeform: you can create `unclear` or `#decisive` or anything you want.


Beyond tags, you can add custom **columns** to your links table. Here are two common columns you could create.

A **conviction**^[we prefer this to "confidence" which can be ambiguous ] column records how sure the source sounds about the claim. In practice most claims are unmarked: people just say "X influenced Y" without qualification. A workable three-point scale is weak / neutral / strong, with a few links in the *weak* or *strong* bins, and the bulk in the middle. This is not a coding of the causal strength of the link itself but only a coding of how confident the source sounds.

You could also use a **strength** column which captures cases where a source explicitly says the influence is strong or weak. Our experience says that humans don't often actually mention this in speaking and writing: again, the bulk of claims is likely to be assessed as neutral: no explicit information about strength. But it might be useful to record strength, for example because we might want to filter out claims about weak strength, or examine only the strong ones. 

We suggest caution in interpreting these kinds of scale as ordinal (small, medium, large; or 1, 2, 3). Linguistically, these kinds of columns/attributes rest on the idea that the default claim is unmarked or neutral, which is not the same as "middling". In most cases simply no need to mention or even think about this aspect. **The fact that most people do not mention the strength of a causal link when talking about it does not mean they think the links were of "medium" strength**. It just means it did not occur to them to think about or mention the strength, or that the idea of strength is not even useful or applicable in this case. 

For more background on why we have been reluctant to code strength, at least in the way that systems modellers do it: 
[[0130.2 Our approach is minimalist -- we do not code the strength of a link ((no-link-strength))]]). 

Beyond Conviction and Strength, many other columns/attributes/judgements are possible. The framework is open: you decide what matters in your project for supporting the conclusions you want to make.

The Causal Map app now supports creating custom link columns like this either before coding or even on the fly, in the middle of coding. 

You can also add custom columns for **sources** rather than links, for example distinguishing reliable from unreliable sources, or recording role and position. Because every link belongs to a source, these scores become available for each link, and you can filter accordingly.


### 4: The bundle assessment phase. Moving from claims to bundles

This warrants its own paper; see [[910 Assessing quality or robustness of evidence for a causal link based on a bundle of coterminal causal claims ((assessing))]] for the detail. In outline:


![[007 Task 2 -- Causal coding -- minimalist style/img/map-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con-2.jpg]]

This is a separate stage in which the analyst, looking at the entire batch of causal claims, their context, metadata, and perhaps ground-level judgements from Moment 1, above, judges each bundle of co-terminal claims and does one of two things:
- collapses each bundle into a single link which is rated with one or more overall quality judgements
- decides to either collapse the bundle it into a single, certified "assessed link" or simply discards the entire bundle, leaving only the "assessed links"

This moment can also take advantage of bundle-level summaries of judgements made at the level of individual links, see above. When you look at a bundle of claims for X influences Y, the Causal Map app now summarises the distribution in a sub-panel of the Assessment panel, for example reporting that in most cases conviction was neutral, with a few sources emphasising they were sure. This is helpful both as a backdrop for human judgement and as a filter (e.g. exclude links where the source said they were uncertain). See [[700 Coding with and using link metadata ((link-metadata))]] for the mechanics.

Once coding is finished and any cleaning has been done, you fix on a set of bundles you want to take seriously. These are the bundles that survive your filters, perhaps after zooming to a higher level of the coding hierarchy and restricting to particular sources or subgroups. There might be five or fifty or a hundred such bundles of links. This is the data you are going to base the rest of your analysis on.

You then look at each bundle, with all its underlying quotes and source metadata, and decide whether the body of claims is enough to vouch for a second-level "assessed link" between the two factors. The assessed link is a new type of object in the links database. By default it inherits the citation count and source count of the underlying bundle and can carry additional scores from custom columns. Some bundles will not produce an assessed link at all, because you have judged the evidence too thin. You simply skip the bundle without creating any assessed link. Or you create a link with a custom column "Passed?", with value = "Fail".


![[007 Task 2 -- Causal coding -- minimalist style/img/map-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con-5.jpg]]

*Creating new individual "assessed links" from bundles of links, bundle by bundle, in the Causal Map app*

You can page through the bundles by hand, or you can let the AI do a first pass against a rubric you supply, and then review its work. The app will not let you create assessed links -- either manually or with AI -- until you have written your criteria into a rubric or prompt sub-panel. This is on purpose. 

The rubric might be a five-level scale like the one Jewlya Lynn and colleagues used in their fishing industry retrospective [@HUSeafoodRetrospective], or just yes/no. Or you might want to create multiple dimensions like "confidence" and "degree of triangulation". The decision is yours.

The result of this Bundle Assessment process is a parallel map. The unassessed claims remain in the database, but a switch in the app lets you view only the assessed links (or only the unassessed links, but not both). A typical project might go from 1000 raw claims to 500 filtered claims in 30 bundles to 25 assessed links. In the Causal Map app, you can use the new "Map Custom Columns" filter to apply custom formatting to your links in the final maps, by source count, citation count, or any custom score (degree of triangulation, for example).

The simpler, assessed map gives you a cleaner basis for argument than the raw claims.

### 5: Pathways and the transitivity trap

This moment involves judging often indirect (sets of) multi-step pathways e.g. from an intervention to an outcome. This is a central part of evaluation and social research and of course a massive theme in the quantitative sciences, but qualitative evaluation approaches have not had quite so much to say about it. Causal mapping provides researchers with a useful set of formal tools for transitive causal thinking. But how in particular do we validate claims for transitivity of causation? 

![[007 Task 2 -- Causal coding -- minimalist style/img/map-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con-3.jpg]]




Even when each link, or each assessed link, is now well grounded, your work is not finished. 

Often you will need to draw conclusions not just about single influences of B on C but about a whole overlapping network of mostly indirect links from B1 and B2 to C via E, F, G and so on. 

Two causal mapping ideas help, as implemented in the Causal Map app.

First, [[300 Path tracing and source tracing ((path-tracing-filter))|Path tracing]] selects the links that lie on some pathway from your chosen start factor to your chosen end factor, within a set number of steps. It excludes all links which are not on such a path, to make it easier to examine the evidence for whatever conclusion you want to draw.

However, from "A influenced B" and "B influenced C" you cannot in general conclude "A influenced C", because the contexts in which each step holds may not overlap. This is [[The transitivity trap ((transitivity-trap))]], the single most important challenge for any approach that uses directed network diagrams. So Causal Map provides Source Tracing as the stricter version of Path Tracing: it finds only sources which have any pathways all the way from A to C and keeps only those pathways, and then combines all such pathways into one map. This is the conservative move when you want to avoid stitching fragments of different stories together. Every link is then part of at least one complete story told by at least one source from A to C. A new button in the app opens the links panel arranged in such a way that you can review all the evidence, source by source, and judge whether each respondent's account is internally coherent.


![[007 Task 2 -- Causal coding -- minimalist style/img/map-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con-4.jpg]]
*Setting up Source Tracing from Increased Knowledge to Food Consumption Quantity, and examining the corresponding narratives.*

 
![[007 Task 2 -- Causal coding -- minimalist style/img/map-source-tracing-example-map.jpg]]
*The corresponding map, in this case tweaked to show source IDs and source counts for easy verification.*

If you have already run a bundle assessment, there is a choice to make: source-trace on the assessed links or on the unassessed ones? With the assessed links you get clean source and citation counts but no direct view of the quotes. With the unassessed links you get the quotes but a busier map. In practice you may want both, in different views.

### 6: Judging value and relative contribution

![[007 Task 2 -- Causal coding -- minimalist style/img/screenshot-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con.jpg]]
Judging value and relative contribution and comparing with alternative explanations are central (overlapping but distinct) questions in evaluation which have been really extensively covered, not least by John Mayne [-@mayneAssessingRelativeImportance2019] for that reason we won't deal with them much here, but QuIP has a lot to say about value, and see @powellTheoriesChangeMaking2019. Watch this space. 


See also [[118 Counting and comparing influences ((counting-influences))]] for an approach to comparing influences on an outcome using path/source tracing. For example here we construct a map tracing all the single-source narratives from two factors of interest (farm production and Increased Knowledge) to two outcomes of interest (Increased income and Improved health) ...

![[010 Task 3 -- Answering questions -- General/img/map-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con.jpg]]

... and here we use the From x To Path Matrix to count the number of sources with complete narratives from the "From" factors to the "To" factors:
![[010 Task 3 -- Answering questions -- General/img/map-900-quality-assurance-and-rigour-in-causal-mapping-ensuring-robust-con-2.jpg]]


### 7: Holistic judgements

Finally, you want to draw a conclusion. You have done some or all of the other steps, checked the individual causal claims, assessed the robustness of co-terminal link bundles, traced paths of influence, compared influences and alternative explanations, and finally you want to at least eyeball all the evidence again and draw a valid conclusion. But "all the evidence" might be a massive corpus. In Causal Map, you can set up all the filters to present the evidence for your conclusion, and you are presented with just a map, but behind the map are still maybe hundreds of causal claims with their associated quotes and context. Does the overall claim still make sense? Can we be sure that the links in all the pathways all belong to the same context?

In Causal Map, the AI vignette feature helps with this, drafting a commentary on a chosen view that helps support inference by drawing on the underlying paths, links, quotes and source metadata, and answering specific quality questions, perhaps according to rubrics you provide.


Vignettes can be created with the specific task of answering quality assurance questions like: is each link really part of a coherent complete and consistent story from source factor (e.g., Intervention) to target factor (e.g., Outcome)?


![[007 Task 2 -- Causal coding -- minimalist style/img/map-automated-vignette-tasked-with-checking-pathway-coherence.jpg]]

*An automated Vignette for the same map, tasked with examining whether the evidence for each pathway is coherent.* 


A common use is to ask for a commentary on the pathways from an intervention to a chosen outcome from the perspective of individual sources, discussing how coherent each source's story is. But you can use a Vignette to re-examine the evidence behind any output.  

The AI is doing nothing more than a careful reader could do given the same inputs, and the patience to examine the quotes behind each link. Some users use this as a starting point and then edit the vignette. 

## What the app does not do

At no point does the Causal Map app move on its own from claims to facts. Causal mapping as we see it is still, on its own, not a method of causal inference but more of a way to *identify and organise the evidence* in order for the evaluator or researcher to make causal inferences, especially when assisting established methods like Contribution Analysis or QuIP. Still, in the past we have perhaps not done enough to say how exactly to do this or to make it easier to do. This post hopes to redress that. 

The warranting is always the evaluator's. We provide structures (tags, columns, the assessed-link switch, source tracing, vignettes) that make warranting easier, more transparent, and more auditable. We do not provide an engine that turns "twenty people said so" into "therefore it is so".

The opposite design, in which an algorithm rules on causal truth from coded text, would either smuggle in strong assumptions about variables and functional forms (which we argue against in [[0130.2 Our approach is minimalist -- we do not code the strength of a link ((no-link-strength))]] and at length in our minimalist coding paper) or conflate evidence volume with effect size, which Causal Map has always been at pains to avoid. As we put it elsewhere, "a coded link is first and foremost 'there is evidence that a source claims X influenced Y', not a system model with weights or effect sizes" [@powellCausalMappingEvaluators2024].

## A typical workflow

A causal mapping project that uses these features looks roughly like this. You code a corpus, in vivo, manually or with AI, and end up with several hundred or several thousand raw claims, each with a quote and a source. You tag occasional claims as doubtful, code conviction where it stands out, and code source reliability in the source metadata. You filter to a maximal set of bundles that matter for your evaluation question, probably omitting links which you are not sure of, perhaps zooming to a level of abstraction at which your factors are useful. You run the bundle assessment phase, by hand or with AI assistance plus review, against a rubric you have written down. You arrive at a much smaller set of assessed links, each of which you are willing to vouch for. You trace pathways, source by source where it matters, between interventions and outcomes. You may ask for vignettes that help you check that the conclusions you want to draw from the map is valid.

None of this is causal inference in a statistical sense. It is a disciplined way to assemble evidence, weigh it transparently, and reach conclusions that you can defend. 


This all works, we use it every day in our consultancy work at Causal Map Ltd., but it is still also evolving every day, so if you are interested in going on this journey with us, do get in touch.

For the practical first step in this workflow, see [[100 Manually code your first project ((howto-manual-code))|Manually code your first project]].

>Footnote: The same QA problematic and logic applies even when the links are not strictly causal: in social network analysis or other map-based work, you may still want to go from a mass of raw claims to a smaller set of checked or verified links, even though the links are about relationships rather than causation. Causal Map can do this too, and the mechanics described below work in the same way, though our main focus here is specifically on *causal* links.
