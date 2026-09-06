---
tags: paper
date: 2026-06-23
theme: academic-case-studies
---

> **Short companion** to [[! EES2026 bites paper|Non-mosquitoes do not cause non-mosquito bites]] (EES 2026, Lille, Strand S03 Responsiveness). The full conventions are in [[005 Minimalist coding for causal mapping ((minimalist))]], [[015 Combining opposites, sentiment ((combining-opposites))]] and [[016 Despite-claims ((despite-claims))]].

# People do not speak in variables

To be responsive, evaluation has to hear stakeholders in their own language, including how they explain what causes what. When we listen at scale, we record those accounts in some structured form, and that form decides whose logic survives: the stakeholder's or the analyst's.

People describe concrete happenings. A pump enabled irrigation. The heat made her tired; another day the cold made her tired. They rarely mean that one variable moved along a scale and pushed another along its own scale in proportion. Yet most ways of coding "what causes what" assume exactly that.

# The mosquito problem

Code a causal claim with variables and you commit to a scale, a polarity and a function the speaker never gave you. The symmetry baked into variables then produces an absurdity. Michael Scriven defined cause, realistically, as "the relation between mosquitoes and mosquito bites" [@scrivenEvaluationThesaurus1981]. Treat that with symmetric variables and "mosquitoes cause mosquito bites" comes out equivalent to "the absence of mosquitoes causes the absence of mosquito bites": non-mosquitoes cause non-mosquito bites. Nobody said it. The variable frame imposes a sample space of presences and absences the speaker never built, and so overwrites the stakeholder's meaning while looking rigorous.

# Code less, not more

Minimalist coding records one cause label, one effect label, the verbatim quote and the source id. No polarity, no weight, no variable, no forced counterfactual. We code the claim before judging whether it is true, because first we want to know what the person thinks [@copestakeAttributingDevelopmentImpact2019]. The asymmetry that broke the variable approach is now a feature: we code an absence only when the speaker asserts one.

Because the task is simple, it scales, and AI can do most of it as a low-level clerk while people keep the judgement [@powellAIassistedCausalMapping2025a; @powellCausalMappingEvaluators2024]. That is the democratic payoff: more voices in evaluative reasoning without thinning each one to a pre-set variable. Counts then mean breadth of evidence in a corpus, not effect size in the world.

# Keeping the difference when you need opposites

Sometimes we do want to line up presences and absences, employment and unemployment, heat and cold. Mark the opposite with `~` (`Employment` and `~Employment`), then apply a combine-opposites transform that rewrites `~Y` to `Y` for aggregation while recording, per link end, whether it was flipped. Nothing is lost: "mosquitoes cause mosquito bites" and "the absence of mosquitoes causes the absence of mosquito bites" aggregate under the same labels yet stay visibly distinct claims. For countervailing claims like "the river failed to improve despite the drainage project," a separate `-despite->` link type keeps a failed causal power visible instead of dropping it or reversing its meaning.

# The point for evaluation

Evaluators are asked to listen to ever larger and more diverse publics. The methods that absorb those voices must not quietly rewrite them, and the mosquito case shows how far variable coding can drift. Minimalist coding, extended only where the data demands it by conventions that preserve the difference between a claim and its opposite, stays close to what people said, keeps provenance anyone can check, and is clear that counts mean breadth, not strength. It needs no hidden vocabulary of necessity, sufficiency, polarity and weights, only labels that hold their meaning and the discipline to add nothing the speaker did not.

See also [@remnantQualitativeCausalMapping2025].
