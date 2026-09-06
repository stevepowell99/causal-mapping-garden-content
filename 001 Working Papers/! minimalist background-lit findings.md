---
tags: paper
---

# Minimalist Causal Coding in the Landscape of Causation, Coding and Causal Inference: A Background-Literature Paper

## Introduction: the Janus spine

The minimalist (or "barefoot") stance on causal coding makes a set of deflationary choices about what to record when someone says that one thing influenced another. It treats a factor as a bare proposition rather than a variable with values; it assigns no polarity, weight or functional form by default; it records influence, not determination, and leaves the counterfactual where the speaker left it; it codes presence rather than absence; it treats source counts as salience, not effect size; it defers evaluative judgement, bundling co-terminal claims before any verdict; it builds per-source maps and aggregates them later rather than negotiating a single consensus map; it traces threads within a source rather than assuming transitivity across links; it gives context and mechanism no special machinery; it pushes enablers, blockers, conjunctions and idioms to the human write-up under a "90% rule"; and it justifies the whole apparatus by scale, by auditability through quote-plus-source provenance, and by an AI-as-clerk division of labour under human authority.

Read as a list, these look like thirteen separate methodological preferences. Read together, they turn on one distinction that runs through every cluster of relevant scholarship: the difference between modelling a person's causal cognition (what a speaker asserted, the surface of their causal talk) and modelling the world (the real causal structure of a system). Call this the Janus problem, after the two faces. Almost every literature the minimalist paper touches faces one way or the other, and a surprising amount of disagreement dissolves, or sharpens, once you ask which face a given method is looking at.

This is the spine of what follows. The structure is not for-and-against. In each cluster there are people who agree with minimalism for reasons it does not share, people who share its premises but reach the opposite practice, and intermediate positions that take some machinery and leave the rest. The paper maps that structure, cluster by cluster (A to I), giving for each the overlapping positions, the strongest opposing case (the steelman), the allies and precursors, the live debate, and a one-line implication for the minimalist paper. Throughout, it flags where a minimalist term or device looks like an existing idea under a new name. A closing synthesis names where minimalism is most exposed, where it is on firmer ground than it currently claims, and which parts may be reinventing the wheel.

A note on citations: every work cited below was checked against primary sources. Where the verification found a corrected detail (a page range, an author list, a venue), the corrected form is used. Nothing is presented as solid that could not be confirmed.

## A. Variables versus propositions in causal and cognitive mapping

The causal and cognitive mapping tradition is both the deepest precedent for minimalism and its sharpest contrast. Almost the entire tradition treats a node as a variable that can take a value and an arrow as a signed, often weighted, influence. Axelrod's signed cognitive maps are the founding orthodoxy: an actor's stated causal beliefs become a signed digraph, concepts as points, assertions as plus or minus arrows, with a calculus over the signs [@axelrod1976structure]. This is the historical root of coding what someone said rather than the world, which minimalism inherits; minimalism keeps the speaker-cognition object and the directed link, and drops the default sign and the calculus.

The positions do not line up pro and anti. They sort along three crossing axes: node ontology (variable or construct versus proposition or event); what is modelled (cognition versus world); and how much computation rides on the arrows. The most interesting group shares minimalism's premise (we are coding cognition) yet reaches for variable-and-weight machinery anyway. Eden's cognitive mapping, rooted in Kelly's personal construct theory, models how a person or group construes a problem, so it sits firmly on the cognition side, but its node is a bipolar construct (a pole and its psychological contrast) built for option and intervention analysis [@eden1992nature; @eden1998making]. Markoczy and Goldberg likewise treat maps as idiosyncratic beliefs yet standardise the construct pool in advance and quantify links with a distance metric to make maps comparable [@markoczy1995method]. Hodgkinson, Maule and Bown stay on the cognition side and supply evidence minimalism can use: heavier pairwise elicitation yields more elaborate maps but feels less representative to participants, so lighter coding can be more faithful [@hodgkinson2004causal]. Laukkanen and Wang's comparative causal mapping (CMAP3) is the nearest methodological ally on design: it elicits causal beliefs from many actors or documents and aggregates them into composite maps, close to minimalism's per-source-then-aggregate stance, though it still uses standardised nodes and often weighted links [@laukkanen2015comparative].

At the far end sit the clearest opposites. Kosko's fuzzy cognitive maps make nodes fuzzy variables and edges signed weights, then iterate the adjacency matrix to simulate behaviour: values, default polarity, weights, functional form, and a slide from belief toward simulating the world, every feature minimalism refuses [@kosko1986fuzzy]. Nadkarni and Shenoy convert elicited maps into Bayesian networks with conditional probabilities, pushing from influence toward quantified determination [@nadkarni2004causal].

The propositional alternative is not native to mapping but has a clear precedent in the philosophy of causation. Davidson argues that causal statements relate particular events and quantify over events at the level of logical form, not over values of variables [@davidson1967logical]. That is the precedent minimalism needs for factor-as-proposition rather than factor-as-variable.

**Steelman.** If a causal map is to do anything beyond display, you need values on nodes and weights on edges. A bare directed link cannot say what happens if a cause is strengthened, cannot combine multiple inputs, cannot resolve feedback, cannot be simulated or validated. Polarity is not ornament: "more training reduces error" and "more training increases error" are different claims, and a map that refuses the sign has discarded the content that makes the relation causal. The construct tradition adds that a cause is only meaningful against its contrast pole, so the node really is bipolar.

**Rephrasing check.** "Factor as proposition" is, in substance, Davidson's event-as-particular applied to coding, and it is close to in-vivo coding in qualitative analysis (cluster G). This is a useful repackaging rather than a new discovery: it earns its name by being a coding rule, but the underlying move (causation relates events, not quantities) is old.

**Implication for the minimalist paper.** Position minimalism as the limit case of Axelrod's signed digraph with the sign, the weight and the calculus removed, and use Kosko and the Bayes-net line as the explicit foil: they buy simulation only by adding values the source never supplied and by crossing from cognition to world.

## B. Theories of causation behind "causal power" and "influence not determination"

Minimalism's two slogans, "in virtue of its causal power" and "influence not determination", sit at the intersection of two debates, and the Janus distinction decides the reading. The powers family says causes have a real productive capacity that disposes towards effects without necessitating them. On the world side, Mumford and Anjum's causal dispositionalism makes "dispose, not necessitate" almost a paraphrase of "influence, not determination" [@mumford2011getting], and Cartwright's capacities are stable, measurable causal tendencies that never fully determine an outcome because other capacities interfere [@cartwright1989natures]. These supply the metaphysical licence for the slogan; minimalism borrows the vocabulary, not the measurement programme.

On the cognition side sits the near-exact terminological twin. Cheng's power PC theory uses the phrase "causal power" and splits it into generative and preventive, mirroring enablers and blockers, but it is a theory about how reasoners infer an unobservable power from covariation [@cheng1997covariation]. That is a claim about surface causal cognition, exactly minimalism's coded object. So Cheng is the strongest verbal ally and the cleanest illustration of why cognition and world must be kept apart: same phrase, but she models the inference while the dispositionalists model the world.

The opposing family is the set of formal traditions minimalism declines, none of them anti-minimalist in spirit, each supplying precisely the machinery minimalism refuses to impose by default. Lewis's counterfactual analysis fixes a specific "had c not occurred" reading and a difference-maker logic [@lewis1973causation]. Woodward's interventionism makes causation what is exploitable by intervention, which presupposes variables that can take values [@woodward2003making]. Pearl's causal Bayes nets and structural models, and Spirtes, Glymour and Scheines's graph-plus-conditional-independence discovery, treat nodes as random variables with functional form [@pearl2009causality; @spirtes2000causation]. Hume's regularity account reduces causation to constant conjunction [@hume1748enquiry]. Salmon's and Dowe's process theories demand a connecting mechanism, a transmitted mark or conserved quantity [@salmon1984scientific; @dowe2000physical].

**Steelman.** If a causal claim is to do inferential work, predict what acting on a factor would do, you need variables with values, a notion of intervention, and some constraint linking structure to dependence. Bare propositions with no polarity and no functional form are, on this view, labelled arrows rather than causal claims: you cannot say what would change if you pushed on a node. The dispositionalist presses a complementary point: the speaker's "X causes Y" already presupposes a real directed power, so stripping all machinery risks recording a shadow of the claim.

**Rephrasing check.** "Influence not determination" maps closely onto Mumford and Anjum's "dispose not necessitate" and, in the contribution-evaluation world, onto the long-standing contribution-not-attribution framing (cluster F). It is a fair repackaging for a coding context, but the author should name the parent ideas rather than present the slogan as new. "In virtue of its causal power" is, terminologically, Cheng's phrase; minimalism should cite her and state plainly that it means the asserted register, not her estimation procedure.

**Implication for the minimalist paper.** State that minimalism borrows the powers tradition's anti-determination vocabulary only as the speaker's asserted register (Cheng's cognition side), and explicitly declines the Lewis, Woodward and Pearl defaults as analyst-imposed, so "causal power" is a coded claim about cognition, not a metaphysical or formal commitment.

## C. Force dynamics, linguistics and the psychology of causal language

This cluster theorises how ordinary people and ordinary language carve up causation, and it sits squarely on the speaker-facing side of Janus. Two questions cut across it. First, what does a lay causal statement encode? Talmy's force dynamics shows everyday causal language is built from force-interaction primitives (an entity with a tendency, an opposing force, blockage, removal of blockage), so cause, let, hinder, help and leave-alone are one family of force patterns, not a single undifferentiated CAUSE [@talmy1988force]. Wolff and colleagues operationalise this as force vectors, distinguishing CAUSE, ENABLE, PREVENT and DESPITE by the patient's tendency, affector-patient concordance and progress to the endstate, validated against the verbs people choose for animated scenes [@wolff2003models; @wolff2007representing]. So "X influenced Y" is already a typed, graded claim in the talk.

Second, why does a speaker name one factor as "the cause" and demote the rest to mere conditions? Four partly nested answers. Hart and Honore select the cause from the field of necessary conditions by reference to a voluntary act or an abnormal departure, leaving ever-present background (oxygen, gravity) as mere condition [@hart1985causation]. Hesslow makes selection contrastive: construing the explanandum as a difference makes only the differing factor relevant [@hesslow1988problem]. Hilton models explanation as a Gricean conversational act, where a good cause is true and relevant to the focus of the why-question [@hilton1990conversational], and Hilton and Slugoski unify counterfactual and contrastive criteria under abnormality relative to a presupposed contrast set [@hilton1986knowledge]. These underwrite minimalism's not-coding-absences (the always-present background is not named), leaving the counterfactual where the speaker left it, and pushing idiomatic packaging to the write-up.

The in-cluster pressure against minimalism comes from those who hold that the cause/enable/prevent split is part of meaning and should be represented: Cheng and Novick explain it by covariation over a focal set [@cheng1991causes], and Goldvarg and Johnson-Laird by distinct mental models for cause, allow and prevent [@goldvarg2001naive].

**Steelman.** The cause/enable/prevent distinction is not decorative packaging but part of the meaning of a causal statement, and it is recoverable, regular and psychologically real. If a speaker has already marked a link as enabling rather than producing, or as preventing, a scheme that records only a bare arrow throws away information the speaker supplied. Minimalism's "no polarity by default" is hard to sustain when prevent is lexically and cognitively distinct from cause.

**Rephrasing check.** Minimalism's "enablers and blockers, left to the write-up" is, in content, Talmy and Wolff's enable/prevent and Cheng and Novick's cause/enabler distinction, deferred rather than encoded. This is not reinvention: minimalism explicitly defers what these authors encode, so it is a different practice built on the same recognised distinctions, and it should cite them as the source of the categories it postpones.

**Implication for the minimalist paper.** Use this cluster to show minimalism is not naive about link structure: the distinctions are real but question- and audience-relative, so leaving them to the human write-up is reasoned, with the prevent/negative-polarity case flagged as the honest open edge.

## D. Necessity, sufficiency and conjunctural causation

This is the home of the machinery minimalism declines under the "90% rule": explicit necessity, sufficiency and conjunctions. At the philosophical base, Mackie's INUS analysis makes a cause an insufficient but non-redundant part of an unnecessary but sufficient condition, which already commits to packages and to multiple sufficient routes [@mackie1965causes; @mackie1974cement]. Rothman ports this into epidemiology as "causal pies": disease arises only when a full pie (a conjunction of components) is complete, several pies may suffice, and a component is necessary only if it appears in every pie [@rothman1976causes]. Ragin builds the social-science programme on the same set-theoretic intuitions, turning necessity (the outcome is a subset of the condition) and sufficiency into a coding-and-minimisation procedure, QCA and then fuzzy-set QCA with calibration, explicitly to recover multiple conjunctural causation [@ragin1987comparative; @ragin2000fuzzy; @ragin2008redesigning]. Baumgartner's Coincidence Analysis names its INUS-regularity commitment openly and recovers redundancy-free Boolean structures [@baumgartner2009inferring; @baumgartner2020causal].

A critical wing argues the Boolean apparatus is too weak and overfits: Clarke shows the two-element algebra cannot express modern social theory, restricts causation to necessity and sufficiency without counterfactual nuance, and is threshold-sensitive [@clarke2020logical]. A near-neighbour, Beach and Pedersen's process tracing, shares the deterministic intuition (parts of a mechanism necessary, the whole sufficient) but works case-by-case rather than by cross-case minimisation [@beach2013process]. Every position here models the world, which is the deepest divergence from minimalism, beyond the cost question.

**Steelman.** When the structure is really there, configurational coding earns its cost. An outcome that genuinely requires a complete conjunction, with several alternative sufficient routes, cannot be represented as a heap of independent single-arrow influences; coding each component as an ordinary factor and leaving the conjunction to the write-up discards the one feature that matters, that no component acts except in concert. Ragin adds that ordinary causal talk is itself set-theoretic ("you need X and Y, unless Z"), so making necessity and sufficiency explicit recovers logic already in the language, and calibration forces an auditable statement of what "enough of X" means. On this view the 90/10 split understates how often the 10% carries the explanatory weight.

**Rephrasing check.** Minimalism's "causal packages and conjunctions" are exactly Mackie's INUS conjunctions and Rothman's component causes. Minimalism does not reinvent these; it names them precisely as the object it declines to code at the coding stage. The honest framing is that minimalism defers INUS structure, not that it has a new account of it.

**Implication for the minimalist paper.** Frame the 90% rule not as ignoring conjunctions but as declining to commit to necessity and sufficiency at the coding stage, citing Mackie, Rothman and Ragin to name the deferred machinery and arguing (with Clarke's overfitting point) that ordinary narrative rarely specifies conjunctions precisely enough to calibrate, so they belong in the auditable write-up over bundled, provenance-tagged claims.

## E. Realist evaluation: context and mechanism

Realist evaluation rests on a generative theory of causation: programmes offer resources that fire context-sensitive mechanisms in the reasoning of actors, written as context-mechanism-outcome configurations [@pawson1997realistic; @pawson2004realist]. The whole apparatus turns on context and mechanism being categorically different from ordinary factors, which is the direct denial of minimalism's "no special machinery" claim. Mechanism, on the purest reading, is an underlying, usually hidden generative process, latent before the intervention and explicitly not an observable variable [@astbury2010unpacking].

The decisive structure here is an internal struggle, not a clean opposition. Realists agree mechanisms are special but cannot agree what they are. Lemire and colleagues review realist evaluations and find "mechanism" defined inconsistently or not at all: roughly 46% gave no explicit definition, and the rest split across at least three incompatible conceptions (programme component, participant reaction, latent underlying cause) [@lemire2020what]. That instability is minimalism's best card: if proponents cannot agree what a mechanism is, treating it as one more factor is reasonable parsimony. Dalkin and colleagues sit between: they disaggregate mechanism into the resources an intervention offers and the change in participants' reasoning, on a continuum rather than an on/off switch [@dalkin2015whats]. The reasoning half is squarely the speaker's causal cognition, so this position partly shares minimalism's object while keeping richer machinery. Schmitt scrutinises whether evaluation's mechanism claims deliver on their promise [@schmitt2020causal], and Punton and Vogel show how mechanism machinery is operationalised in a large applied evaluation [@punton2020keeping].

The lineage realist evaluation draws on supplies precursors that imply mechanism is a privileged category: analytical sociology's middle-range "cogs and wheels" [@hedstrom1998social] and the new-mechanist philosophy of science, where a mechanism is entities and activities organised to produce regular change [@machamer2000thinking]. Both, however, concern real-world processes, the world side of Janus, so they do not directly speak to coding what speakers say.

**Steelman.** Causation is generative: a programme introduces resources into a setting, and whether they fire a behaviour change depends on real actors' reasoning and on enabling or disabling conditions. Mechanisms are not variables but theories of resources and reasoning, often hidden and latent, so a scheme that records only surface statements as flat factors misses the generative process that does the explanatory work and misses why the same programme works here and fails there. Flattening context and mechanism is then a category error, not parsimony.

**Rephrasing check.** Minimalism's claim that context and mechanism are "ordinary factors" is resolved by the Janus distinction rather than by reinventing anything: realists model real generative powers, minimalism codes what a speaker treats as the mechanism. The two are not rival accounts of one object; they are accounts of different objects.

**Implication for the minimalist paper.** Resolve the context-and-mechanism claim by the Janus distinction (realist machinery models real-world powers; minimalism codes surface cognition, so context and mechanism are named factors with no privileged status) and cite Lemire and colleagues' finding that even realists cannot agree what a mechanism is as evidence the special machinery does not pay its way at scale.

## F. Causal inference from narrative in evaluation

This is the family of theory-based methods that build causal claims from narrative rather than from counterfactual comparison. They share minimalism's starting point (cause is in what people say, claims need provenance) but split on two axes. The first is where evaluative judgement sits relative to coding. At one pole, outcome harvesting collects and formulates outcome statements before substantiation and sense-making, deferring the verdict [@wilsongrau2012outcome; @wilsongrau2018outcome], and QuIP codes respondents' own causal claims close to the text before the evaluator concludes anything [@copestake2018managing; @copestake2019attributing]. This is minimalism's deferred-judgement position. At the other pole, process tracing folds the evaluative judgement into the evidentiary act: each piece of evidence is weighed by probative value (hoop, smoking-gun, straw-in-the-wind, doubly-decisive) at the moment it is assessed [@beach2013process], and Befani and Stedman-Bryce formalise this with Bayesian updating in "Contribution Tracing" [@befani2017process]. Contribution analysis sits in the middle, narrative-first but iterating towards one overall contribution claim [@mayne2001addressing; @mayne2012contribution], and Befani and Mayne argue the two poles are stronger combined, reframing the task as assessing confidence about impact rather than impact itself [@befani2014process]. Aston's contribution rubrics make the deferred-but-explicit judgement central, scoring significance, contribution and strength of evidence per outcome [@aston2024quality].

The second axis is aggregation and chaining. QuIP plus Causal Map is the clear neighbour of minimalism: it codes each respondent's links, aggregates by counting how many respondents asserted the same link (shown as line thickness), chains drivers through intermediate factors, and keeps every link traceable to a source quote [@bathsdr2021narrative]. Process tracing deliberately does not aggregate by counting sources, because confidence comes from the probative strength of a few decisive pieces, which is exactly minimalism's warning that source counts are not effect size, reached the opposite way.

**Steelman.** Deferring judgement and then aggregating by counting sources gets causal inference backwards. Ten weak corroborating accounts of a link tell you less than one smoking-gun observation that only the true story could produce, and one failed hoop test can kill a hypothesis a hundred testimonies support. Confidence should track probative value at the point of coding, not the tally of sources. By the same logic, transitivity cannot be assumed: A to B and B to C does not license A to C without mechanism evidence at each step, so the within-source thread is not a safe substitute for testing the chain. Minimalism's "code first, count later" risks maps whose thick lines reflect how often something was said, not how strongly it was shown.

**Rephrasing check.** Several minimalist devices are existing QuIP practice. Per-source coding, deferral to a sense-making stage, aggregation by respondent count, chaining through intermediate factors, and quote-plus-source provenance are all already in QuIP and the Causal Map workflow. Minimalism is in large part QuIP's coding discipline stated as explicit principles, which is a legitimate contribution (naming and defending the discipline) but not a new method; the paper should say so plainly. "Bundles" of co-terminal claims is close to grouping parallel evidence for one link, long present in this tradition. "Defer evaluative judgement" is the staged design of outcome harvesting under a different name.

**Implication for the minimalist paper.** Position minimalism as QuIP's coding discipline made explicit: keep per-source coding and provenance, but answer process tracing by stating that source counts are link salience, not effect size or proof, and that within-source thread tracing, not free transitivity, is how it earns chained claims without importing Bayesian probative-value machinery.

## G. Coding theory and qualitative data analysis

This field already shares most of minimalism's coding craft while differing on what coding is for. Saldaña is the closest neighbour: he defines a code as a short essence-capturing label, insists coding is a heuristic and "just one way" of analysing rather than analysis itself, and offers an explicit Causation Coding method that extracts participants' attributions and plots the sequence into a matrix or flow chart [@saldana2021coding]. That is minimalism's surface-claim extraction in all but name. Miles, Huberman and Saldaña go further into causal network displays (boxes and arrows), the procedural ancestor of causal-map coding, but treat the nodes as analyst variables aimed at explaining the case, closer to modelling the world [@miles2014qualitative].

Grounded theory supplies the craft minimalism inherits, line-by-line coding of small fragments, in-vivo and action coding that stays close to what was said, and deferral of grand interpretation, plus, in Charmaz, a shared constructivism [@charmaz2014constructing]. But grounded theory fractures data only to reassemble it into one integrated, saturated core theory [@glaser1967discovery], which is the integration minimalism refuses. Mayring's qualitative content analysis is the rule-bound, auditable, scalable wing minimalism most resembles procedurally [@mayring2000qualitative].

The live opposition is the Big-Q reflexive camp. Braun and Clarke split thematic analysis into coding-reliability, codebook and reflexive variants, agree with minimalism that coding is interpretive and that themes are constructed not discovered, and agree that prevalence and counting do not establish importance, yet reject exactly what minimalism embraces: inter-rater reliability, mechanical or "clerk"-able coding, and decontextualising units [@braun2006using; @braun2021one]. The Big-Q versus small-Q framing comes from Kidder and Fine [@kidder1987qualitative], and Lincoln and Guba ground the decontextualisation worry in thick description and context-embedded meaning, while their confirmability audit trail is itself a provenance argument and so a partial ally [@lincoln1985naturalistic].

**Steelman.** Meaning in qualitative data is produced in context and in the researcher's interpretive engagement with the whole, so coding is already interpretation, not a neutral first step a clerk can perform at scale. Reducing a stretch of talk to a bare proposition discards the qualifications, hedging, tone and surrounding narrative that gave it sense. Treating coding as something an AI can do at volume reintroduces the assumption that coding is mechanical and reliability-checkable, which the reflexive camp argues is a paradigm error. The honest objection is not that minimalism is sloppy but that it optimises for scale and auditability at the cost of interpretive depth, then labels the trade as rigour.

**Rephrasing check.** "Minimalist propositions" is close to in-vivo coding plus Saldaña's Causation Coding; "the labels do the work" and "defer judgement, code into bundles first" are close to Saldaña's "coding is a heuristic, not analysis" and to grounded theory's open coding before integration. These are genuine precursors, so minimalism is best presented as disciplined QDA coding carried to scale, with explicit credit to Saldaña's named Causation Coding rather than as a fresh invention.

**Implication for the minimalist paper.** Present minimalism as the disciplined-coding tradition (Saldaña's Causation Coding, Mayring's rule-bound scale, grounded theory's close fragment coding) carried to scale, and meet the decontextualisation objection by conceding the premise (coding is interpretive and constructed) while showing that coding surface claims with quote-plus-source provenance answers the contextual worry differently from, not worse than, thick description.

## H. Participatory and consensus mapping versus multi-source aggregation

This cluster splits along two crossing axes: what the diagram represents (the speakers' cognition or the real system) and how multiple people are handled (per-source maps aggregated later, or a single negotiated map). System dynamics group model building sits at the world-modelling, consensus end: link polarity and loop polarity (reinforcing or balancing) drive the dynamics, and the explicit aim is to converge participants' separate mental models into one shared, validated model that fosters consensus and commitment [@vennix1996group; @vennix1999group; @sterman2000business]. That contradicts minimalism on values, polarity, functional form and the per-source design at once. Participatory Systems Mapping is a hybrid: Barbrook-Johnson and Penn openly call the map an intersubjective object reflecting beliefs, close to minimalism's cognition framing, yet build one consolidated map of variables that go up and down with typed positive, negative, unclear or complex links [@barbrook2021participatory; @barbrook2022systems].

Fuzzy cognitive mapping is the closest ally on the aggregation axis: it routinely elicits separate individual maps and aggregates them afterwards (often by averaging edge weights) into a social cognitive map, and frames the artefact as mental models and group beliefs, yet every edge carries a signed direction and a fuzzy weight, and the literature itself worries that averaging loses heterogeneity [@gray2014fuzzy; @gray2013mental; @kok2009potential]. The pure opposite pole is the directed acyclic graph: the DAG is unambiguously a model of the world, built to identify confounders and license counterfactual and interventional inference [@greenland1999causal; @pearl2009causality]. Running inside system dynamics is a debate that already names minimalism's core distinction: is a participatory model a "microworld" (a representation of the real system) or a "boundary object" (a socially negotiated artefact for shared understanding) [@zagonel2002model]?

**Steelman.** For action-oriented work the point of a causal model is not to transcribe what each person said but to help a group converge on a shared understanding of how the real system behaves so they can change it. Per-source maps aggregated mechanically later record diverse talk but never force the productive disagreement and validation through which a group builds and commits to a defensible model. Polarity and loop structure are what make the diagram predict behaviour and identify leverage points, which a polarity-free bag of propositions cannot do. The DAG tradition adds that reasoning about confounding or counterfactuals needs an explicit model of the world, not a faithful record of cognition.

**Rephrasing check.** Minimalism's world-versus-cognition distinction is, in this cluster, the microworld-versus-boundary-object distinction already named by Zagonel and echoed in Barbrook-Johnson and Penn's "intersubjective object". Minimalism's "per-source maps aggregated later" is standard FCM elicitation practice. The Janus framing is therefore a useful relabelling that travels well across fields, but the author should acknowledge that participatory-modelling scholars already named both the distinction and the aggregation practice; minimalism's contribution is choosing both horns consistently, which these traditions name but mostly do not follow through.

**Implication for the minimalist paper.** Use the field's own microworld-versus-boundary-object distinction to show the minimalist stance is not eccentric: it takes the boundary-object and per-source horns these traditions already name but mostly abandon when they build, while conceding that DAGs and dynamic causal loop diagrams answer a different, world-modelling question.

## I. Auditability, scale and AI or NLP causal extraction

The NLP field minimalism most resembles is causal relation extraction. Yang, Han and Poon map the task space into explicit intra-sentential, implicit and inter-sentential causality and review knowledge-based, statistical and deep-learning methods [@yang2022survey]. The shared-task line operationalises causal extraction as span marking: classify whether a sentence is causal, then label the Cause span, the Effect span and the causal Signal span. SemEval-2010 Task 8 established supervised cause-effect classification with directionality and a single gold label [@hendrickx2010semeval]; FinCausal frames it as cause and effect span identification in documents [@mariko2022financial]; and the Causal News Corpus and the CASE 2022 shared task formalise Cause (ARG0), Effect (ARG1) and Signal (SIG) span annotation, with span detection the hard part (best F1 around 54% against 86% for sentence-level classification) [@tan2022causal; @tan2022event]. This Cause/Effect/Signal span unit is the same as minimalism's candidate-link-plus-quote, and the Signal span mirrors recording the causal idiom. The field agrees strongly with minimalism's auditability claim: Schreieder, Schopf and Farber survey evidence-based text generation and find fine-grained span or token-level attribution best for verifiability and traceability, supplying a standards vocabulary of granularity, visibility and faithfulness [@schreieder2025attribution].

The field diverges on three things minimalism cares about. It mostly models the world or the text's propositional content under a single gold label, not the speaker's cognition. It frames the task as supervised classification with a best label, which sits awkwardly with defer-judgement and code-everything-into-bundles. And on the AI-as-clerk division of labour it supplies a serious caution: Schroeder, Roy and Kabbara show that putting a human in the loop does not neutralise LLM suggestions, because annotators defer to them (automation bias), shifting label distributions and inflating apparent performance without working faster [@schroeder2025just]. Dai, Xiong and Ku show a workable human-LLM thematic-analysis workflow where suggestions still require analyst verification [@dai2023llm]. Argument mining is a near-neighbour that targets what people claim and grounds it in text (closer to the speaker side) but adds typed components and support/attack structure, the machinery minimalism declines [@lawrence2019argument; @stede2018argumentation]. The nearest methodological precursor to the clerk model is Panda, Adigun and Kosko's agent pipeline, which extracts concept nodes then causal edges from raw text, but it produces fuzzy weighted edges and a dynamical-systems model, exactly the strength-and-weight machinery minimalism rejects, and models the system, not the speaker; its abstract does not confirm that each edge is justified by a direct quote, so that specific resemblance to the clerk model is unverified [@panda2026agentic].

**Steelman.** The objection is not "do not ground claims in text", which the field accepts, but "candidate-link-plus-quote is not enough, and human-as-architect over AI-as-clerk is the wrong safeguard". Decades of extraction work show the hard cases (implicit and inter-sentential causality, signal-free causation inferred from event order, directionality) are exactly what minimalism pushes to the write-up, and these are where explicit structure and supervised models earn their keep. On oversight, automation bias makes human review weaker than it looks: if the clerk proposes and the architect almost always accepts, the audit trail records agreement manufactured by the suggestion itself. Quote grounding plus nominal human authority is then insufficient; you need suggestion-free passes, inter-coder reliability and explicit faithfulness checks.

**Rephrasing check.** Minimalism's candidate-link-plus-quote unit is the established Cause/Effect/Signal span of the shared tasks, and its auditability goal is the attributed-generation literature's span-level provenance standard. This is convergence, not reinvention: minimalism should present its unit as field-standard and cite the shared tasks rather than implying novelty. The "AI as clerk under a human architect" is a specific staffing claim that the human-in-the-loop literature directly tests and partly undercuts.

**Implication for the minimalist paper.** Cite the span-extraction shared tasks and the evidence-based-generation survey to show the candidate-link-plus-quote unit and its auditability are the field standard, then use the automation-bias finding to harden the clerk claim: AI-as-clerk only works if the audit trail records independent human judgement, so add a suggestion-free or reliability check rather than relying on nominal authority.

## Synthesis

### Where the minimalist paper is most exposed

1. **Polarity, especially "prevent" (claims 2, A and C).** The no-default-polarity rule is hardest to hold where the talk is lexically explicit. "Prevent" and "reduce" are distinct from "cause" and "increase" in the surface language itself (Talmy, Wolff, Goldvarg and Johnson-Laird), so refusing to record a sign that the speaker plainly supplied looks like discarding coded content, not deferring an analyst's judgement. This is the cleanest place a critic can say minimalism throws away what it claims to preserve.

2. **Counting versus probative value (claims 7, 9, F).** Minimalism is split from its own closest ally. Its claim that source counts are not effect size sides with process tracing, yet its per-source aggregation looks like QuIP, which treats the respondent count as salience. The paper must state precisely what a thick line means and does not mean, or the practice and the principle will read as contradictory.

3. **The clerk and automation bias (claim 13, I).** The human-in-the-loop evidence shows that nominal human authority over an LLM clerk produces manufactured agreement. Auditability through provenance documents which span was cited, not that a human judged independently. Without a suggestion-free pass or a reliability check, the auditability claim is weaker than it sounds.

4. **Conjunctions and the 90% rule (claim 12, D).** The claim that conjunctural structure is rare enough to push to the write-up is domain-dependent and, in tightly coupled domains, false. The paper needs to make the domain conditionality explicit rather than stating the 90/10 split as general.

### Where the minimalist paper is on stronger ground than it currently claims

1. **The Janus distinction (claim 5).** This is minimalism's strongest and most underused asset. It is not idiosyncratic: it is the microworld-versus-boundary-object debate (Zagonel), the boundary-object reading in participatory mapping, and the dividing line between Cheng's inferred power and the dispositionalists' real power. Drawing it explicitly dissolves much of the realist and DAG objection, which lands on a target minimalism never claimed.

2. **Mechanism as an ordinary factor (claim 11).** Lemire and colleagues' finding that even realists cannot agree what a mechanism is, with nearly half of studies offering no definition, is direct empirical support that the special machinery does not pay its way at scale. The paper can press this harder.

3. **Deferred judgement (claim 8).** Outcome harvesting's staged design and Saldaña's "coding is a heuristic, not analysis" give minimalism a well-established lineage for coding before judging. This is settled practice, not a risky novelty.

4. **Lighter coding can be more faithful (claims 1 to 3).** Hodgkinson, Maule and Bown supply evidence that heavier elicitation feels less representative to participants. Minimalism can cite this directly rather than resting the case for parsimony on cost alone.

### Where minimalism may be reinventing the wheel

- **"Bundles" of co-terminal claims** is grouping parallel evidence for one link, long present in QuIP and the contribution-evaluation tradition; it is a useful local label, not a new device.
- **"Influence not determination"** is Mumford and Anjum's "dispose not necessitate" and the contribution-not-attribution framing in one phrase; a fair repackaging that should name its parents.
- **"In virtue of its causal power"** is, terminologically, Cheng's phrase; minimalism uses it for the asserted register, which is legitimate but should be credited.
- **"Thread tracing" within a source** is within-case process tracing without the Bayesian probative-value tests; the discipline (test the chain, do not assume transitivity) is Beach and Pedersen's, applied more lightly.
- **"Minimalist propositions"** are Davidson's events-as-particulars applied to coding, and close to in-vivo coding plus Saldaña's Causation Coding.
- **The candidate-link-plus-quote unit** is the shared-task Cause/Effect/Signal span; minimalism's contribution is the auditability discipline around it, not the unit.

### Where minimalism is actually novel

The novelty is not in any single rule, most of which have precursors, but in the consistent combination: taking the cognition horn and the per-source horn together (which participatory traditions name but abandon when they build), pairing the powers tradition's anti-determination vocabulary with the maximally deflationary stance on apparatus, and binding the whole to a scale-and-auditability rationale with quote-plus-source provenance as the load-bearing safeguard. Naming Causation Coding's surface-claim extraction as a stand-alone discipline, deliberately refusing the integration step that grounded theory, group model building and configurational methods all build towards, is a position worth defending in its own right. The defensible claim is not "these ideas are new" but "this particular, internally consistent set of refusals, justified by scale and provenance rather than by simulation or theory-building, has not been assembled and argued before".

## References

Aston, T. (2024). *Quality of Evidence Rubrics for Single Cases* (v2.0). UK Evaluation Society. https://evaluation.org.uk/wp-content/uploads/2024/09/Quality-of-Evidence-Rubrics-2.0-Final.pdf (practitioner guidance; a co-author, Marina Apgar, may be listed on the title page).

Astbury, B., & Leeuw, F. L. (2010). Unpacking black boxes: Mechanisms and theory building in evaluation. *American Journal of Evaluation*, 31(3), 363-381. https://doi.org/10.1177/1098214010371972

Axelrod, R. (Ed.). (1976). *Structure of Decision: The Cognitive Maps of Political Elites*. Princeton University Press.

Barbrook-Johnson, P., & Penn, A. S. (2021). Participatory systems mapping for complex energy policy evaluation. *Evaluation*, 27(1), 57-79. https://doi.org/10.1177/1356389020976153

Barbrook-Johnson, P., & Penn, A. S. (2022). *Systems Mapping: How to Build and Use Causal Models of Systems*. Palgrave Macmillan. https://doi.org/10.1007/978-3-031-01919-7

Baumgartner, M. (2009). Inferring causal complexity. *Sociological Methods & Research*, 38(1), 71-101. https://doi.org/10.1177/0049124109339369

Baumgartner, M., & Ambühl, M. (2020). Causal modeling with multi-value and fuzzy-set Coincidence Analysis. *Political Science Research and Methods*, 8(3), 526-542. https://doi.org/10.1017/psrm.2018.45

Bath Social & Developmental Research. (2021). *From Narrative Text to Causal Maps: QuIP Analysis and Visualisation*. https://bathsdr.org/wp-content/uploads/2021/10/From-narrative-text-to-causal-maps-QuIP-analysis-and-visualisation.pdf

Beach, D., & Pedersen, R. B. (2013). *Process-Tracing Methods: Foundations and Guidelines*. University of Michigan Press. https://doi.org/10.3998/mpub.10072208

Befani, B., & Mayne, J. (2014). Process tracing and contribution analysis: A combined approach to generative causal inference for impact evaluation. *IDS Bulletin*, 45(6), 17-36. https://doi.org/10.1111/1759-5436.12110

Befani, B., & Stedman-Bryce, G. (2017). Process tracing and Bayesian updating for impact evaluation. *Evaluation*, 23(1), 42-60. https://doi.org/10.1177/1356389016654584

Braun, V., & Clarke, V. (2006). Using thematic analysis in psychology. *Qualitative Research in Psychology*, 3(2), 77-101. https://doi.org/10.1191/1478088706qp063oa

Braun, V., & Clarke, V. (2021). One size fits all? What counts as quality practice in (reflexive) thematic analysis? *Qualitative Research in Psychology*, 18(3), 328-352. https://doi.org/10.1080/14780887.2020.1769238

Cartwright, N. (1989). *Nature's Capacities and Their Measurement*. Clarendon Press.

Charmaz, K. (2014). *Constructing Grounded Theory* (2nd ed.). SAGE.

Cheng, P. W. (1997). From covariation to causation: A causal power theory. *Psychological Review*, 104(2), 367-405. https://doi.org/10.1037/0033-295X.104.2.367

Cheng, P. W., & Novick, L. R. (1991). Causes versus enabling conditions. *Cognition*, 40(1-2), 83-120. https://doi.org/10.1016/0010-0277(91)90047-8

Clarke, K. A. (2020). Logical constraints: The limitations of QCA in social science research. *Political Analysis*, 28(4), 552-568. https://doi.org/10.1017/pan.2020.7

Copestake, J., Allan, C., van Bekkum, W., Belay, M., Goshu, T., Mvula, P., Remnant, F., Thomas, E., & Zerahun, Z. (2018). Managing relationships in qualitative impact evaluation of international development: QuIP choreography as a case study. *Evaluation*, 24(2), 169-184. https://doi.org/10.1177/1356389018763243

Copestake, J., Morsink, M., & Remnant, F. (2019). *Attributing Development Impact: The Qualitative Impact Protocol Case Book*. Practical Action Publishing. https://doi.org/10.3362/9781780447148

Dai, S.-C., Xiong, A., & Ku, L.-W. (2023). LLM-in-the-loop: Leveraging large language model for thematic analysis. *Findings of the Association for Computational Linguistics: EMNLP 2023*, 9993-10001. https://aclanthology.org/2023.findings-emnlp.669/

Dalkin, S. M., Greenhalgh, J., Jones, D., Cunningham, B., & Lhussier, M. (2015). What's in a mechanism? Development of a key concept in realist evaluation. *Implementation Science*, 10, 49. https://doi.org/10.1186/s13012-015-0237-x

Davidson, D. (1967). The logical form of action sentences. In N. Rescher (Ed.), *The Logic of Decision and Action* (pp. 81-95). University of Pittsburgh Press. (Reprinted in *Essays on Actions and Events*, 1980, Oxford University Press.)

Dowe, P. (2000). *Physical Causation*. Cambridge University Press.

Eden, C. (1992). On the nature of cognitive maps. *Journal of Management Studies*, 29(3), 261-265. https://doi.org/10.1111/j.1467-6486.1992.tb00664.x

Eden, C., & Ackermann, F. (1998). *Making Strategy: The Journey of Strategic Management*. SAGE.

Glaser, B. G., & Strauss, A. L. (1967). *The Discovery of Grounded Theory: Strategies for Qualitative Research*. Aldine.

Goldvarg, E., & Johnson-Laird, P. N. (2001). Naive causality: A mental model theory of causal meaning and reasoning. *Cognitive Science*, 25(4), 565-610. https://doi.org/10.1207/s15516709cog2504_3

Gray, S. A., Gray, S., Cox, L. J., & Henly-Shepard, S. (2013). Mental Modeler: A fuzzy-logic cognitive mapping modeling tool for adaptive environmental management. *Proceedings of the 46th Hawaii International Conference on System Sciences*, 963-973. https://doi.org/10.1109/HICSS.2013.399

Gray, S. A., Zanre, E., & Gray, S. R. J. (2014). Fuzzy cognitive maps as representations of mental models and group beliefs. In E. I. Papageorgiou (Ed.), *Fuzzy Cognitive Maps for Applied Sciences and Engineering* (pp. 29-48). Springer. https://doi.org/10.1007/978-3-642-39739-4_2

Greenland, S., Pearl, J., & Robins, J. M. (1999). Causal diagrams for epidemiologic research. *Epidemiology*, 10(1), 37-48. https://doi.org/10.1097/00001648-199901000-00008

Hart, H. L. A., & Honoré, T. (1985). *Causation in the Law* (2nd ed.). Clarendon Press.

Hedström, P., & Swedberg, R. (Eds.). (1998). *Social Mechanisms: An Analytical Approach to Social Theory*. Cambridge University Press.

Hendrickx, I., Kim, S. N., Kozareva, Z., Nakov, P., Ó Séaghdha, D., Padó, S., Pennacchiotti, M., Romano, L., & Szpakowicz, S. (2010). SemEval-2010 Task 8: Multi-way classification of semantic relations between pairs of nominals. *Proceedings of the 5th International Workshop on Semantic Evaluation*, 33-38. https://aclanthology.org/S10-1006/

Hesslow, G. (1988). The problem of causal selection. In D. J. Hilton (Ed.), *Contemporary Science and Natural Explanation: Commonsense Conceptions of Causality* (pp. 11-32). Harvester Press.

Hilton, D. J. (1990). Conversational processes and causal explanation. *Psychological Bulletin*, 107(1), 65-81. https://doi.org/10.1037/0033-2909.107.1.65

Hilton, D. J., & Slugoski, B. R. (1986). Knowledge-based causal attribution: The abnormal conditions focus model. *Psychological Review*, 93(1), 75-88. https://doi.org/10.1037/0033-295X.93.1.75

Hodgkinson, G. P., Maule, A. J., & Bown, N. J. (2004). Causal cognitive mapping in the organizational strategy field: A comparison of alternative elicitation procedures. *Organizational Research Methods*, 7(1), 3-26. https://doi.org/10.1177/1094428103259556

Hume, D. (1748). *An Enquiry Concerning Human Understanding*. (Numerous critical editions, e.g. Oxford University Press.)

Kidder, L. H., & Fine, M. (1987). Qualitative and quantitative methods: When stories converge. *New Directions for Program Evaluation*, 1987(35), 57-75. https://doi.org/10.1002/ev.1459

Kok, K. (2009). The potential of fuzzy cognitive maps for semi-quantitative scenario development, with an example from Brazil. *Global Environmental Change*, 19(1), 122-133. https://doi.org/10.1016/j.gloenvcha.2008.08.003

Kosko, B. (1986). Fuzzy cognitive maps. *International Journal of Man-Machine Studies*, 24(1), 65-75. https://doi.org/10.1016/S0020-7373(86)80040-2

Laukkanen, M., & Wang, M. (2015). *Comparative Causal Mapping: The CMAP3 Method*. Routledge. https://doi.org/10.4324/9781315573038

Lawrence, J., & Reed, C. (2019). Argument mining: A survey. *Computational Linguistics*, 45(4), 765-818. https://doi.org/10.1162/coli_a_00364

Lemire, S., Kwako, A., Nielsen, S. B., Christie, C. A., Donaldson, S. I., & Leeuw, F. L. (2020). What is this thing called a mechanism? Findings from a review of realist evaluations. *New Directions for Evaluation*, 2020(167), 73-86. https://doi.org/10.1002/ev.20428

Lewis, D. (1973). Causation. *The Journal of Philosophy*, 70(17), 556-567. https://doi.org/10.2307/2025310

Lincoln, Y. S., & Guba, E. G. (1985). *Naturalistic Inquiry*. SAGE.

Machamer, P., Darden, L., & Craver, C. F. (2000). Thinking about mechanisms. *Philosophy of Science*, 67(1), 1-25. https://doi.org/10.1086/392759

Mackie, J. L. (1965). Causes and conditions. *American Philosophical Quarterly*, 2(4), 245-264. https://www.jstor.org/stable/20009173

Mackie, J. L. (1974). *The Cement of the Universe: A Study of Causation*. Clarendon Press.

Mariko, D., Abi-Akl, H., Trottier, K., & El-Haj, M. (2022). The Financial Causality Extraction Shared Task (FinCausal 2022). *Proceedings of the 4th Financial Narrative Processing Workshop*, 105-107. https://aclanthology.org/2022.fnp-1.16/

Mayne, J. (2001). Addressing attribution through contribution analysis: Using performance measures sensibly. *Canadian Journal of Program Evaluation*, 16(1), 1-24. https://doi.org/10.3138/cjpe.016.001

Mayne, J. (2012). Contribution analysis: Coming of age? *Evaluation*, 18(3), 270-280. https://doi.org/10.1177/1356389012451663

Mayring, P. (2000). Qualitative content analysis. *Forum: Qualitative Social Research*, 1(2), Art. 20. https://doi.org/10.17169/fqs-1.2.1089

Miles, M. B., Huberman, A. M., & Saldaña, J. (2014). *Qualitative Data Analysis: A Methods Sourcebook* (3rd ed.). SAGE.

Mumford, S., & Anjum, R. L. (2011). *Getting Causes from Powers*. Oxford University Press.

Nadkarni, S., & Shenoy, P. P. (2004). A causal mapping approach to constructing Bayesian networks. *Decision Support Systems*, 38(2), 259-281. https://doi.org/10.1016/S0167-9236(03)00095-2

Panda, A. K., Adigun, O., & Kosko, B. (2026). *The Agentic Leash: Extracting Causal Feedback Fuzzy Cognitive Maps with LLMs* (arXiv preprint 2601.00097). https://arxiv.org/abs/2601.00097

Pawson, R., & Tilley, N. (1997). *Realistic Evaluation*. SAGE.

Pawson, R., & Tilley, N. (2004). *Realist Evaluation*. (Overview paper.) https://cnxus.org/wp-content/uploads/2022/04/RE_chapter.pdf

Pearl, J. (2009). *Causality: Models, Reasoning, and Inference* (2nd ed.). Cambridge University Press. https://doi.org/10.1017/CBO9780511803161

Punton, M., & Vogel, I. (2020). Keeping it real: Using mechanisms to promote use in the realist evaluation of the Building Capacity to Use Research Evidence Program. *New Directions for Evaluation*, 2020(167), 87-100. https://doi.org/10.1002/ev.20427

Ragin, C. C. (1987). *The Comparative Method: Moving Beyond Qualitative and Quantitative Strategies*. University of California Press.

Ragin, C. C. (2000). *Fuzzy-Set Social Science*. University of Chicago Press.

Ragin, C. C. (2008). *Redesigning Social Inquiry: Fuzzy Sets and Beyond*. University of Chicago Press. https://doi.org/10.7208/chicago/9780226702797.001.0001

Rothman, K. J. (1976). Causes. *American Journal of Epidemiology*, 104(6), 587-592. https://doi.org/10.1093/oxfordjournals.aje.a112335

Saldaña, J. (2021). *The Coding Manual for Qualitative Researchers* (4th ed.). SAGE.

Salmon, W. C. (1984). *Scientific Explanation and the Causal Structure of the World*. Princeton University Press.

Schmitt, J. (2020). The causal mechanism claim in evaluation: Does the prophecy fulfill? *New Directions for Evaluation*, 2020(167), 11-26. https://doi.org/10.1002/ev.20421

Schreieder, T., Schopf, T., & Färber, M. (2025). *Attribution, Citation, and Quotation: A Survey of Evidence-Based Text Generation with Large Language Models* (arXiv preprint 2508.15396). https://arxiv.org/abs/2508.15396

Schroeder, H., Roy, D., & Kabbara, J. (2025). Just put a human in the loop? Investigating LLM-assisted annotation for subjective tasks. *Findings of the Association for Computational Linguistics: ACL 2025*, 25771-25795. https://aclanthology.org/2025.findings-acl.1323/

Spirtes, P., Glymour, C., & Scheines, R. (2000). *Causation, Prediction, and Search* (2nd ed.). MIT Press.

Stede, M., & Schneider, J. (2018). *Argumentation Mining*. Synthesis Lectures on Human Language Technologies. Morgan & Claypool. https://doi.org/10.2200/S00883ED1V01Y201811HLT040

Sterman, J. D. (2000). *Business Dynamics: Systems Thinking and Modeling for a Complex World*. Irwin/McGraw-Hill.

Talmy, L. (1988). Force dynamics in language and cognition. *Cognitive Science*, 12(1), 49-100. https://doi.org/10.1207/s15516709cog1201_2

Tan, F. A., Hettiarachchi, H., Hurriyetoglu, A., Caselli, T., Uca, O., Liza, F. F., & Oostdijk, N. (2022). Event causality identification with Causal News Corpus: Shared Task 3, CASE 2022. *Proceedings of the 5th Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text*, 195-208. https://aclanthology.org/2022.case-1.28/

Tan, F. A., Hurriyetoglu, A., Caselli, T., Oostdijk, N., Nomoto, T., Hettiarachchi, H., Ameer, I., Uca, O., Liza, F. F., & Hu, T. (2022). The Causal News Corpus: Annotating causal relations in event sentences from news. *Proceedings of the 13th Language Resources and Evaluation Conference*, 2298-2310. https://aclanthology.org/2022.lrec-1.246/

Vennix, J. A. M. (1996). *Group Model Building: Facilitating Team Learning Using System Dynamics*. Wiley.

Vennix, J. A. M. (1999). Group model-building: Tackling messy problems. *System Dynamics Review*, 15(4), 379-401. https://doi.org/10.1002/(SICI)1099-1727(199924)15:4<379::AID-SDR179>3.0.CO;2-E

Wilson-Grau, R. (2018). *Outcome Harvesting: Principles, Steps, and Evaluation Applications*. Information Age Publishing.

Wilson-Grau, R., & Britt, H. (2012). *Outcome Harvesting* (rev. Nov. 2013). Ford Foundation MENA Office.

Wolff, P. (2007). Representing causation. *Journal of Experimental Psychology: General*, 136(1), 82-111. https://doi.org/10.1037/0096-3445.136.1.82

Wolff, P., & Song, G. (2003). Models of causation and the semantics of causal verbs. *Cognitive Psychology*, 47(3), 276-332. https://doi.org/10.1016/S0010-0285(03)00036-7

Woodward, J. (2003). *Making Things Happen: A Theory of Causal Explanation*. Oxford University Press.

Yang, J., Han, S. C., & Poon, J. (2022). A survey on extraction of causal relations from natural language text. *Knowledge and Information Systems*, 64, 1161-1186. https://doi.org/10.1007/s10115-022-01665-w

Zagonel, A. A. (2002). Model conceptualization in group model building: A review of the literature exploring the tension between representing reality and negotiating a social order. *Proceedings of the 20th International Conference of the System Dynamics Society*. https://proceedings.systemdynamics.org/2002/proceed/papers/Zagonel1.pdf