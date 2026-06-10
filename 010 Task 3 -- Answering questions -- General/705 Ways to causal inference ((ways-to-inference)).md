---
date: 2025-10-09
---

There are different ways to set up a table like this. Some of these are more like methods, some are more like frameworks. Some overlap. Most do not exist only or even primarily to conduct causal inference.

## Commonalities

Almost all these meta-models presuppose that causal knowledge can be captured in chunks, and these chunks can be joined together in chains / networks in order to consider indirect effects, ie if X causes Y and Y causes Z, what can we say about the causal effect of X on Z? Everything doesn’t depend on _everything_ else: in a large causal network, to make causal inferences about Z the only causal factors we need to consider are those for which there is a causal chain leading to Z, and the only direct effects on Z are the factors which have arrows directly leading to Z.

“Portability” means that the knowledge that Xs can influence Ys can be applied in multiple contexts, not just on one particular occasion.

Traditionally, more qualitative approaches like QCA are less keen on portability.

Some of the models eg SEM are particularly interested in calculating indirect effects in chains and networks. In others eg QCA the concept of a causal chain is less clear, and there is little portability / generalisibility.

## Table

|   |   |   |   |   |   |
|---|---|---|---|---|---|
||Notes|Prerequisites|Inference|Metaphor||
|Ordinary reasoning||I already know that Xs are likely to cause Ys, and this X happened and Y followed it in just the way you’d expect.<br><br>I don’t exactly have a ready-made theory about X’s and Y’s but I have similar theories about things similar to Xs and Ys and some other knowledge which suggest that the these similar|It is quite likely that X causally influenced Y.|Both the foundation on which all other methods stand and the cement which holds them together||
|Ordinary reasoning:  Modus Operandi||The signatures of all the other possible explanations of Y were absent and the signature of X was present. A signature is evidence of a chain from X to Y or other evidence that X was active.<br><br>Relies on pre-existing causal knowledge<br><br>Argues also that counterfactuals may be irrelevant; the patient might also have died if they hadn’t had the heart attack, but the heart attack was the direct physical cause.|||Scriven|
|Ordinary reasoning: Multiple lines and levels of evidence (MLLE)||||||
|Ordinary reasoning: Causal mapping||Not really a method of causal inference at all, but a way to organise medium or large datasets of pre-existing (possibly conflicting or overlapping) causal claims or inferences made by a set of sources.<br><br>Says nothing about portability because it relies on its sources to decide on what||||
|Successionist||- Many observations that Ys follow Xs|May in practice be used to support but not warrant the conclusion that the Xs caused the Ys. Might be used in evaluation as a hoop test.||Hume|
|Classical Statistical||Not possible||||
|Regression discontinuity||||||
|Counterfactual||Can be used for **disproving** a causal inference: if sometimes Xs appear but Ys do not appear, this X cannot be the cause of this Y.|X caused Y|||
|DAGs / SEM||Level 3:<br><br>A model in which the effect of X on Y is significant<br><br>Substantive theory|||Pearl|
|Configurational; QCA, fQCA||A dataset showing the co-occurrence and non-occurrence of X1, X2, X3 … and Y<br><br>A case in which X1, X2, X3 etc and Y occur/don’t occur in a pattern corresponding to the dataset<br><br>Substantive considerations backing up the dataset<br><br>Possible consolidation of the information into more parsimonious structures.<br><br>Usually not used to establish general causal laws and then make specific causal inferences but only to make causal inferences within a dataset.<br><br>The inference that X1, X2, X3 actually _cause_ Y rather than just being associated with it is not based only on the configuration but has to be provided by other substantive knowledge, so perhaps QCA is not strictly a method of causal inference.|This combination of Xs may have caused Y in this case.|Causal package|Ragin|
|INUS||Special case of the above in which X1, X2, X3 … are necessary parts of a package P which is sufficient for Y, i.e. (X1 & X2 & X3…) is sufficient for Y.|X1 was an INUS-cause of Y (and so was X2 etc)|Causal package||
|Realist||Substantive knowledge that a mechanism M in a context C, when triggered (X) causes Y.<br><br>M and C were present, X was activated, Y happened.|X was a cause of Y|A machine or mechanism||
|Process oriented; Process tracing||||||
|Physical causality||“people’s “operative reasons” for doing what they do are the physical actions.”<br><br>“A design whose purpose is to determine impact will be considered qualitative if it relies on something other than evidence for the counterfactual to make a causal inference. It is qualitative first in the positive sense that it rests on demonstrating a quality-in the present treatment the quality will be a physical connection in the natural world between the proposed cause and effect-and second in the negative sense that it is not quantitative, that is, it does not rely on a treatment variable, or on comparing what is with an estimate of what would otherwise have been.”||Touching|Mohr|
|Dispositional||||||
|Radical systems eg Quinn Patton?||Not possible||||

<!-- xrefs-v1 -->

## Related

- [[010 Causal mapping produces models you can query to answer questions ((query-models))|chapter intro]]
