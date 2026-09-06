---
tags: paper
date: 2026-06-23
theme: academic-case-studies
---

> **EES 2026, Lille. Strand S03 Responsiveness. Individual paper.** Steve Powell (Causal Map Ltd) and Fiona Remnant (Bath Social & Development Research).
>
> This is the conference-length version of the argument. The full treatment, with all the coding conventions, is in [[005 Minimalist coding for causal mapping ((minimalist))]]; the opposites and despite extensions are in [[015 Combining opposites, sentiment ((combining-opposites))]] and [[016 Despite-claims ((despite-claims))]].

## People do not speak in variables

To be responsive, evaluation has to listen to stakeholders in their own language: how they describe the worlds they live in, and how they explain what causes what. When we listen at scale, across many interviews, meetings and submissions, we have to record those accounts in some structured form so we can read them back, compare them and aggregate them. The form we choose is not a neutral technical choice. It decides whose logic survives the coding: the stakeholder's, or the analyst's.

People describe concrete happenings. A pump enabled irrigation. A barking dog kept the owner inside. The heat made her tired; another day, the cold made her tired. They almost never say, and rarely mean, that some variable moved along a scale and pushed another variable along its own scale in proportion. Yet that is exactly what most established ways of coding "what causes what" assume.

## The variable-based approach, at its strongest {.banner-info}

It is worth stating the dominant approach in its best form before disagreeing with it, because in its place it works well.

Most systems mapping and causal mapping traditions treat each factor as a **variable**, a thing that can take different values, and each link as an arrow with a **polarity** (more X means more Y, or more X means less Y) and sometimes a **strength** or weight. This is the world of systems dynamics, fuzzy cognitive maps and causal loop diagrams, and of Axelrod's signed cognitive maps of political elites [@axelrodStructureDecisionCognitive1976]. A second family, set-theoretic rather than continuous, codes causes as Boolean conditions and reasons about **necessity and sufficiency**: Charles Ragin's fuzzy sets [@raginMeasurementCalibrationSetTheoretic2008] and Gary Goertz's work on necessary conditions and bipolar concepts [@goertzSocialScienceConcepts2020].

When you can make these commitments honestly, you are rewarded. Signed, weighted links let you reason about feedback loops, run simulations, and talk precisely about counterfactuals. Necessity and sufficiency let you find the bottleneck that no amount of anything else can compensate for. Where respondents really are reasoning in those terms, or where the purpose is to build a model of how the system works rather than to record what people said, this machinery is the right tool, and we use it ourselves.

## Where it overreaches: the mosquito problem {.banner-info}

The trouble starts when we apply that machinery to ordinary-language causal claims as a form of qualitative coding. Take two diary entries:

> 1. I was eating less and felt quite lethargic.
> 2. I started to eat adequately and was feeling more lively.

Coded with variables, both become the same link, `amount eaten -> energy level`, with a positive sign: more eaten, more energy. But we do not know whether the speaker holds a continuous or a yes/no model of "eating", what the opposite of "eating a lot" even is for them, or what function connects the two. To code this way we have to invent all of it. We go well beyond what the speaker meant, and we quietly stop doing qualitative analysis of their account and start doing our own modelling.

The sharpest form of the problem is Michael Scriven's. Scriven defined causation, realistically and generatively, as "the relation between mosquitoes and mosquito bites" [@scrivenEvaluationThesaurus1981]. Now code "mosquitoes cause mosquito bites" with symmetric variables. The formal logic of variables treats the absence of the cause and the absence of the effect as just as informative as their presence, so "mosquitoes cause mosquito bites" comes out **logically equivalent** to "the absence of mosquitoes causes the absence of mosquito bites". In other words: non-mosquitoes cause non-mosquito bites. That is nonsense, and nobody said it. The variable frame imposes a symmetric sample space of presences and absences that the speaker never constructed.

This is not pedantry. For a strand about responsiveness it is the whole point: a coding method that silently rewrites "mosquitoes bite" into a claim about non-mosquitoes is overwriting the stakeholder's meaning with the analyst's apparatus. And it does so while looking rigorous.

| | Variable-based coding | Minimalist coding |
|---|---|---|
| Basic unit | A dimension that varies | A quoted causal claim between bare events or states |
| The link | Signed and maybe weighted relation | Undifferentiated "X influenced Y" |
| Presence and absence | Symmetric, linked by the variable | Asymmetric: absences coded only if asserted |
| What it needs from the text | Scale, polarity, function, counterfactual | The source's own words, plus who said it |
| First question | Is the relationship positive or negative? | What did this person actually claim, and where? |

## The minimalist answer {.banner-info}

The alternative we have used across thousands of stakeholder interviews, developed with Bath SDR through QuIP practice and formalised in the [Causal Map app](https://app.causalmap.app), is to code less, not more.

A coded link is one cause label, one effect label, the verbatim quote, and the source id. Nothing else: no polarity, no weight, no variable, no assumed function, no forced counterfactual. The second diary entry becomes simply:

> I started to eat adequately `->` feeling more lively (source: diary 2; quote: "I started to eat adequately and was feeling more lively")

We code the claim before judging whether it is true, because first we want to know what the person thinks [@copestakeAttributingDevelopmentImpact2019]. The asymmetry that broke the variable approach is here a feature: we do not code absences unless the speaker asserts one ("because of the barking dog, the owner did not come out"). If one family blames social media for arguments and another blames homework, we do not read the first as denying that homework matters.

This stance is unsophisticated by design, and that is what lets it scale. The coding task is easy enough that generative AI can do most of it as a low-level clerk while leaving human judgement for the few decisions that matter [@powellAIassistedCausalMapping2025a; @powellWorkflowCollectingUnderstanding2025; @powellCausalMappingEvaluators2024]. The democratic payoff is direct: minimalist coding makes it feasible to bring far larger and more diverse publics into evaluative reasoning without thinning each voice down to a pre-defined variable. One caution travels with it: counts of coded links measure the **breadth of evidence in a corpus**, how many people said something, not the size of an effect in the world.

## But sometimes you do need opposites {.banner-info}

Minimalism is not the end of the story, and the full version of this paper says where it runs out. Sometimes we really do want to line up presences and absences, heat and cold, poverty and wealth, employment and unemployment, so that evidence for one pole can be read alongside the other. The question is how to do that without sliding back into variables and re-importing the mosquito problem.

Our answer is a label convention plus an explicit transform that preserves the difference. Mark a factor's opposite with a `~` prefix: `Employment` and `~Employment`. We say "opposite" rather than "plus or minus" on purpose, because which pole is "good" depends on context (`Smoking` versus `~Smoking`). A **combine-opposites** transform then rewrites every `~Y` to the canonical `Y` so the evidence aggregates under one label, but records, for each end of each link, whether it was flipped.

That last move is the whole trick. Because flip status stays attached to the evidence, nothing is lost and the original claim can always be reconstructed. "Mosquitoes cause mosquito bites" and "the absence of mosquitoes causes the absence of mosquito bites" aggregate under the same factor labels yet remain visibly **distinct** claims, distinguished by their flip flags rather than collapsed into one symmetric arrow. We get the convenience the variable people wanted, and we keep the asymmetry the mosquito example demands.

A worked health example makes this concrete. Coded as-is, two stories use separate poles: `smoking` leads to `~being fit`, while `running` leads to `being fit`. As plain labels the app cannot see that the two are related.

![[map-278ec2b569edd2dbcda3a448a7f4742e-md5.jpg]]
*Opposites coded as-is: `~being fit` and `being fit` sit as unrelated labels, so half the evidence is invisible to a search for "being fit".*

Combining opposites rewrites `~being fit` onto `being fit` and colours each flipped link end pink, so the two senses aggregate without merging. An inference that was hidden now becomes available: running, as a healthy habit, may make visits to the doctor less likely.

![[map-53401812ec144ec48107a45a72ac9f62-image-8.jpg]]
*After combining: a pink end marks a link flipped from `~`. No information is lost, and the original map can always be read back.*

A related but separate axis is **sentiment**. Oppositeness and sentiment overlap oddly and are only semi-orthogonal: `~Smoking` is the opposite of `Smoking`, but which pole counts as good is a context-dependent valence question, not an oppositeness one. Tagging each claim's effect as +1, 0 or -1 becomes especially useful with AI-assisted coding, because embeddings cluster `employment` and `unemployment` together and ignore the `~`, and a sentiment pass recaptures the negative meaning that clustering drops. The full conventions, including opposites inside hierarchical labels and sentiment, are in [[015 Combining opposites, sentiment ((combining-opposites))]].

## And sometimes you need "despite" {.banner-info}

A harder case the abstract promised: "the river levels failed to improve despite the drainage project." A "despite" clause does two things at once. It says the drainage project was meant to work against the outcome, and it says the outcome happened anyway. Code only the main claim (`Heavy rains -> River levels rose`) and you lose the attempted mitigation. Code the despite clause as an ordinary link (`Drainage project -> River levels rose`) and you flip its meaning into its opposite.

So we treat "despite" as its own **link type**, not a new meaning for the arrow: `Drainage project -despite-> River levels rose`, read as "this was presented as a countervailing power against the outcome, in virtue of its power to work against it, but the outcome occurred anyway." These links can be shown in a distinct style, filtered on their own, counted separately, and contrasted with cases where the same factor was said to succeed. It is a small, conservative addition that keeps a failed causal power visible instead of dropping it or misreading it. Details in [[016 Despite-claims ((despite-claims))]].

## Why this matters for vibrant democracies {.banner-info}

Evaluators are now asked to listen to larger and more diverse publics than before, across more interviews, meetings, submissions and digital texts than any analyst can read closely. If wider participation is to mean anything in evaluation, the methods that absorb all those voices must not quietly overwrite them. Variable-based coding, applied to ordinary language, does overwrite them, and the mosquito case shows how absurd the result can get.

Minimalist coding, extended only where the data demands it by opposites and despite conventions that preserve rather than erase the difference between a claim and its opposite, is a more responsive default. It stays close to what people said, keeps provenance so anyone can check it, scales with AI assistance, and is clear that counts mean breadth of evidence rather than effect size. None of that requires a hidden vocabulary of necessity, sufficiency, polarity and weights. It requires labels that hold their meaning long enough to be useful, and the discipline to add nothing the speaker did not.

See also [@powellCausalMappingEvaluators2024; @remnantQualitativeCausalMapping2025].
