---
date: 2025-11-09
---
**



## Executive Summary

The integration of Large Language Models (LLMs) into the methodological infrastructure of the social sciences has precipitated a fundamental crisis of epistemology. As researchers increasingly deploy generative AI for tasks ranging from thematic coding to causal mapping, a critical tension has emerged between the scalability of automated analysis and the cultural specificity of human meaning-making. This tension is most acute when applying these technologies—overwhelmingly trained on data from Western, Educated, Industrialized, Rich, and Democratic (WEIRD) societies—to non-WEIRD contexts. The central question facing the field is no longer merely whether AI can code text, but whether it can navigate the complex "positionality" required to interpret qualitative data from diverse cultural frameworks without imposing a hegemonic, Western-centric lens.

This report synthesizes emerging empirical evidence from late 2024 and 2025 regarding the efficacy of "persona" or "positionality" prompts in mitigating this bias. We conduct a rigorous comparative analysis of studies that explicitly test whether instructing an LLM to adopt a specific cultural or regional persona (e.g., "You are an Indian researcher" or "Analyze this from a Japanese cultural perspective") yields results distinct from neutral prompting, and critically, whether these results align with human coders from those backgrounds.

The analysis reveals a complex landscape where the promise of "prompt engineering" as a panacea for cultural bias often falls short of the profound depth of human cultural cognition. While AI agents can simulate surface-level cultural alignment—successfully mimicking survey responses from Saudi Arabia or identifying broad themes in Japanese clinical interviews—they frequently revert to Western norms when tasked with deep interpretive labor. The evidence suggests that current "persona" prompts act more as stylistic filters than as genuine shifts in epistemic standpoint, leading to a phenomenon of "cultural projection" where Western logic is masked in non-Western linguistic markers.

However, promising methodological alternatives are emerging. The shift from "black box" thematic analysis to transparent "causal mapping" pipelines, the development of "radical zero-shot" coding protocols that treat AI as a "clerk" rather than an "architect," and frameworks like AI-empowered Collaborative and Collective Epistemic Reflexivity (i-CCER) offer pathways to harness AI's computational power while centering human oversight. This report argues that achieving valid non-WEIRD analysis requires moving beyond simple persona prompting toward a rigorous structural re-evaluation of the human-AI loop, where positionality is treated not as a prompt parameter, but as a defining constraint of the research design.

## 1. The Hegemony of the Training Set: WEIRD Bias as the Default Ontology

To understand the necessity and performance of non-WEIRD positionality prompts, one must first confront the default ontology of the instruments in use. Large Language Models are not neutral tabula rasas; they are cultural artifacts that encode the values, norms, and inferential patterns of their training data. This section explores the theoretical and statistical foundations of AI bias, establishing why "neutral" prompting is a misnomer in the context of global social science.

### 1.1 The Statistical Dominance of Western Perspectives

Recent scholarship confirms that the training corpora for dominant models (such as the GPT, LLaMA, and Claude families) are heavily skewed toward English-language internet text produced in the Global North. This creates a "WEIRD outlier" effect, where the model's baseline assumptions about causality, morality, and social interaction reflect a specific, globally atypical psychological profile.1

When a researcher inputs a "neutral" prompt—for example, "Identify the main themes in this interview transcript"—the model does not perform a view-from-nowhere analysis. Instead, it defaults to a specific "latent persona": typically that of a helpful, liberal, Western academic or service worker. This default positionality influences every stage of qualitative analysis, from code generation (what is considered a "code") to hierarchy building (which themes are "major" vs. "minor") and interpretation (how ambiguity is resolved).

This bias is not merely a matter of missing vocabulary; it is a matter of epistemic frame. The models are trained on data where individualism, direct communication, and secular rationality are dominant modes of expression. Consequently, when analyzing text from cultures that value collectivism, high-context communication, or spiritual causality, the "neutral" model inevitably misinterprets or marginalizes key concepts unless explicitly constrained or redirected. The danger lies in the subtlety of this erasure: the AI will produce a coherent, plausible-sounding analysis that effectively translates the non-Western data into Western categories, creating an illusion of understanding while obliterating indigenous meaning.2

### 1.2 The "Hard-to-Reach" Algorithm and Methodological Exclusion

The consequences of this bias extend into the very methodology of social science. Research into the recruitment and involvement of non-WEIRD populations has highlighted how rigid, Western-centric methods contribute to the exclusion of Global South voices, labeling them "hard to reach".3 When AI analysis tools are applied to data from these populations without adjustment, they risk committing epistemic violence by reinterpreting local narratives through foreign categories.

The concept of "Algorithmic Fidelity"—the degree to which an AI model accurately reflects the sociodemographic subgroups it purports to simulate—is central here.4 If a model has low algorithmic fidelity for non-WEIRD populations, it cannot reliably code their data. Studies examining "force dynamics" in language suggest that while LLMs grasp physical causality across languages, their understanding degrades in abstract social contexts involving emotional forces or culturally specific interpersonal norms.5 This indicates that the "reasoning" capabilities of LLMs are not universally transferable but are tethered to the cultural logic of their training data. Therefore, the use of neutral prompts on non-WEIRD data is functionally equivalent to using a Western coder who lacks cultural competence: the outputs may look structurally sound but will lack validity.

### 1.3 The Mechanics of Alignment and the "Progressive Bias"

A critical, often overlooked factor is the role of Reinforcement Learning from Human Feedback (RLHF) in shaping model positionality. Models are fine-tuned to be helpful, harmless, and honest, based on guidelines developed by Western researchers and labeled largely by workers who are instructed to uphold these specific safety and politeness norms.

This process introduces a "progressive bias" or "alignment tax".7 Empirical comparisons of synthetic survey participants show that AI agents consistently display more positive, progressive, and "financially literate" biases than their human counterparts, particularly in non-WEIRD contexts.7 For example, when simulating a respondent from Saudi Arabia, the AI may express views on gender roles or economic behavior that are significantly more aligned with Western liberal norms than the actual population average. This suggests that the safety alignment process effectively "sanitizes" cultural differences, pulling all simulated personas toward a globalized, liberal mean. For qualitative coding, this is disastrous: it means the AI is predisposed to ignore or "correct" data that conflicts with its safety training, potentially erasing distinct cultural perspectives on controversial or sensitive topics.

## 2. Testing the "Persona Prompt": Empirical Evidence from Cross-Cultural Coding

The primary mitigation strategy employed by computational social scientists has been "persona prompting"—explicitly instructing the model to adopt a specific cultural, professional, or demographic identity (e.g., "Act as an expert anthropologist from India"). Recent empirical work from late 2024 and 2025 has rigorously tested the efficacy of this approach, yielding results that challenge the optimism surrounding prompt engineering.

### 2.1 The "Cultural Alignment" Failure: Wei et al. (2025)

Perhaps the most significant study addressing this precise issue is the work by Wei, Liu, Barany, Ocumpaugh, and Baker (2025) titled "Cultural Alignment and Biases in Qualitative Coding: Comparing GPT and Human Coders".9 This study offers a direct, controlled comparison of human and AI coding across cultural lines, providing a benchmark for the efficacy of positionality prompting.

#### 2.1.1 Experimental Methodology

The researchers designed a study to compare coding decisions made by six trained human researchers from three distinct cultural backgrounds—China, India, and the United States—against decisions produced by GPT-4o. The experimental design was rigorous, controlling for codebook definitions and data sources to isolate the variable of cultural interpretation.

- Data Source: 200 student observations from a U.S. game-based learning environment.
    
- Prompting Conditions:
    

1. Baseline Condition: Neutral prompts asking for coding without specified positionality.
    
2. Culture-Specific Condition: Prompts explicitly instructing the model to adopt a Chinese or Indian cultural perspective when analyzing the data (e.g., "Analyze this data from the perspective of a researcher from China...").
    

- Analysis Metrics: The study measured inter-rater reliability (using Kappa scores) within cultural groups, across cultural groups, and between humans and the model under both prompting conditions.
    

#### 2.1.2 Quantitative Findings: The Persistence of the Western Gaze

The results were stark and revealing. First, the human data validated the premise that culture shapes coding: human coders achieved high within-culture agreement (indicating distinct, shared interpretive frames within Chinese, Indian, and US groups) but low cross-cultural agreement. This empirically establishes that "ground truth" in qualitative coding is culturally relative.

Critically, GPT-4o failed to bridge this gap. The analysis showed that:

- Persistent Western Alignment: Even when prompted to adopt a Chinese or Indian cultural perspective, the model's coding decisions aligned significantly more closely with the U.S. human coders than with the Chinese or Indian human coders.9 The "persona" prompt failed to shift the model's interpretive center of gravity away from its training data distribution.
    
- Superficial Adaptation: While the model changed its output style or vocabulary in response to the persona prompt, it did not successfully adopt the interpretive lens (the "emic" perspective) of the target culture. The underlying logic remained Western, dressed in the trappings of the target persona.
    

#### 2.1.3 Qualitative Findings: Cultural Projection and Blind Spots

Beyond the statistical failure, the qualitative analysis of the coding discrepancies highlighted four key challenges that define the limits of AI in cross-cultural research 9:

1. Unfamiliar Cultural Phenomenon: The model simply missed cues that were obvious to insiders but opaque to outsiders (and the model).
    
2. Cultural Blind Spots: The model failed to recognize implicit cultural scripts governing behavior in the dataset.
    
3. Choosing the Cultural Lens: When data was ambiguous, the model defaulted to a Western lens rather than the prompted non-Western lens.
    
4. Cultural Projection: This was the most damning finding. The authors identified a phenomenon where the model imposed Western interpretive logic onto the data even while ostensibly operating under a non-Western persona. For instance, it might interpret a behavior as "assertive" (a Western positive value) when a Chinese coder would code it as "disruptive" (violating group harmony). The model projected Western values onto the non-Western persona, creating a "Hallucinated Cultural Perspective."
    

This study suggests that "persona prompting" in qualitative coding is often a mirage. The model's "alignment tax"—its reinforcement learning towards helpful, Western norms—appears to override transient instructions to "be" someone else. For social scientists, this implies that simply adding "You are a Chinese researcher" to a prompt is insufficient to generate valid non-WEIRD analysis.

### 2.2 Descriptive vs. Interpretive Depth: Sakaguchi et al. (2025)

Complementing the findings of Wei et al., Sakaguchi, Sakama, and Watari (2025) conducted a comparative qualitative study titled "Evaluating ChatGPT in Qualitative Thematic Analysis With Human Researchers in the Japanese Clinical Context".14 This study focused on the Japanese healthcare setting, a context rich in high-context communication and distinct cultural norms regarding patient-provider relationships, specifically exploring themes of "sacred moments" in care.

#### 2.2.1 Experimental Methodology

The researchers analyzed transcripts of semi-structured interviews using ChatGPT-4. They compared the AI's output against reflexive thematic analysis performed by experienced human researchers who had conducted the interviews.

- Prompting: The prompt structure mirrored standard qualitative practices, instructing the AI to analyze interviews iteratively to assess data saturation.14
    
- Comparison: The study evaluated the consistency and frequency of extracted themes across two frameworks: Grounded Theory and the Framework Method.
    

#### 2.2.2 Findings: The Depth of the Failure

The study found a dramatic divergence in performance based on the depth and cultural specificity of the theme:

- Descriptive Success: ChatGPT demonstrated high agreement rates (over 80%) with human researchers for identifying explicit, descriptive themes. For example, "building relationships" (86% agreement) and "personal experience of a sacred moment" (73% agreement) were reliably captured.15 These themes rely on explicit lexical markers in the text.
    
- Interpretive Failure: The model performed abysmal on themes requiring deep cultural interpretation or context. Specifically, the theme of "fate" (en)—a deeply resonant cultural concept in Japanese clinical encounters—showed 0% agreement. Similarly, subtle nuances of "dialogue," which involve reading between the lines in high-context Japanese communication, showed only 13% agreement.15
    

#### 2.2.3 Implications for High-Context Cultures

Sakaguchi et al. conclude that while AI can serve as a "second coder" for efficiency in identifying broad, recurring patterns, it lacks the "cultural competence" required for deep hermeneutic inquiry.14 The model could identify that a conversation happened, but not the cultural weight of that conversation. The "neutral" prompt (even when processing Japanese text) failed to capture culturally specific constructs that human Japanese researchers centered. This reinforces the distinction between translation (which LLMs are good at) and interpretation (which requires shared lifeworlds).

### 2.3 Synthetic Participants: Simulating the Non-WEIRD Respondent

While not strictly "coding," the ability of AI to simulate non-WEIRD participants serves as a proxy for its ability to understand and analyze from those perspectives. If an AI cannot accurately simulate a Saudi respondent, it likely cannot accurately interpret data from a Saudi respondent. Shrestha, Krpan, Koaik, and Bin Baz (2025) investigated this in "Beyond WEIRD: Can synthetic survey participants substitute for humans in global policy research?".7

#### 2.3.1 Experimental Methodology

The study compared responses from real human participants in the United States, Saudi Arabia, and the United Arab Emirates (UAE) against "synthetic participants" generated by GPT-4.

- Prompting: The researchers used detailed persona prompts defined by demographic characteristics matching the human sample (e.g., "You are a 30-year-old female living in Riyadh, employed in the public sector...").20
    
- Domains: Sustainability, financial literacy, and female labor force participation.
    

#### 2.3.2 Findings: The "Progressive" Distortion

- Weaker Correlations in Non-WEIRD Contexts: While the AI could mimic human responses reasonably well across all groups, the correlations between human and synthetic responses were significantly weaker for the Saudi and UAE samples compared to the US sample.7 This indicates a degradation of algorithmic fidelity as the cultural distance from the US increases.
    
- The Progressive Bias: The synthetic participants consistently showed "more positive and less negative bias" than their human counterparts. Specifically, the AI-generated "Saudi" participants were more progressive on gender roles and had higher financial literacy scores than the real human sample. This trend was less pronounced in non-WEIRD participants than WEIRD ones, but the bias indicates the model's reluctance to fully embody conservative or traditionalist non-WEIRD worldviews.7
    

This "Progressive Bias" suggests that even when explicitly told to adopt a non-WEIRD persona, the model's underlying safety alignment (which favors inclusivity, equality, and Western liberal values) bleeds through, distorting the simulation. This makes the AI a poor instrument for analyzing data that contains "unaligned" cultural realities, as it may subtly "correct" or misinterpret conservative cultural views as "errors" or "bias."

## 3. Alternative Methodologies: Structure over Persona

Given the demonstrated failure of simple persona prompting to achieve deep cultural validity, researchers are pivoting toward structural interventions. These approaches do not rely on the AI "becoming" a non-WEIRD coder but rather constrain its role within a human-architected system.

### 3.1 The "Radical Zero-Shot" and "Architect" Model: Powell et al. (2025)

In the domain of causal mapping and evaluation, Powell, Cabral, and Mishan (2025) propose a workflow that sidesteps the need for the AI to "understand" culture deeply by restricting its role to low-level extraction.5

#### 3.1.1 The "Clerk vs. Architect" Distinction

This approach, described in their work on "AI-assisted causal mapping," distinguishes between the "Clerk" (the AI) and the "Architect" (the human).5

- The Problem with Interpretation: The authors argue that asking an AI to "interpret themes" invites hallucination and cultural bias because "themes" are abstract and heavily dependent on positionality.
    
- The Solution: Radical Zero-Shot Extraction: Instead, they use "radical zero-shot" prompts that instruct the AI to perform a mechanical, syntactic task: "List every causal claim in the text in the format X causes Y. Do not summarize. Do not interpret. Use the exact words from the text.".5
    

#### 3.1.2 The Workflow

1. AI Interviewer: An AI conducts semi-structured interviews. Notably, in their US-based pilot, 78.5% of respondents accepted the AI's summaries without change, indicating high basic comprehension.5
    
2. Autocoding (The Clerk): The AI extracts causal links (e.g., "Lack of rain -> Crop failure"). It is explicitly forbidden from aggregating or theorizing.
    
3. Clustering & Synthesis (The Architect): The human evaluator takes the raw list of thousands of causal links and performs the high-level judgment: deciding what the codes mean, clustering them into themes, and interpreting the "causal landscape".5
    

#### 3.1.3 Implications for Non-WEIRD Contexts

This method is particularly robust for non-WEIRD contexts (referenced in their work on Ghana and Burkina Faso 5) because it prevents the AI from imposing a Western narrative structure on the data. By forcing the AI to stick to "bare causation" and verbatim quotes, the method preserves the original cultural concepts (e.g., "The ancestors were angry -> The rain stopped") without forcing them into a Western scientific framework. The human expert, who possesses the necessary cultural competence, then synthesizes these raw claims. The authors explicitly warn that this method is "not reliable enough for high-stakes single-link adjudication without human checking" and highlight the risk of "hegemonic worldviews" in third-party APIs.5

### 3.2 i-CCER: Distributed Posthuman Reflexivity

A more theoretical contribution comes from the concept of AI-empowered Collaborative and Collective Epistemic Reflexivity (i-CCER).22 This framework challenges the notion that positionality is solely a human attribute or that it can be "prompted" into a machine.

#### 3.2.1 AI as Epistemic Partner, Not Tool

Instead of trying to "prompt away" the AI's bias, i-CCER treats the AI as a distinct epistemic partner with its own (alien, Western-centric) positionality. The methodology involves a recursive dialogue where the research team and the AI "reflect" together.

- Process: Researchers might ask the AI to code data, then ask it to critique its own coding from a specific theoretical standpoint (e.g., "Critique this analysis from a decolonial feminist perspective").
    
- Synthesis: The human team then synthesizes these layers. The goal is not to force the AI to be non-WEIRD, but to use its friction with non-WEIRD data to generate insights. The AI surfaces hidden meanings and synthesizes complex team reflections, but the authors emphasize it "cannot replace ethical, situated, accountable reflexive practice".22
    

### 3.3 Positionality Statements for Robots

The document "Causal Mapping: 97 ideas" includes a provocative section titled "What's your positionality, robot?".5 This reflects a growing consensus that AI tools must be treated as situated actors. Just as human researchers write positionality statements detailing their background and biases, studies using AI for coding must include a "Technical Positionality Statement." This statement should detail:

- The model used (and its known training data bias).
    
- The specific prompts designed to mitigate or acknowledge that bias.
    
- The "game" the AI was told to play (e.g., "We explicitly instructed the AI to prioritize local terminology over standard sociological terms").5
    

## 4. Synthesis: The Mechanics of Failure and the Path Forward

Analyzing the aggregate findings from Wei et al., Sakaguchi et al., and Shrestha et al. allows us to derive second-order insights into why non-WEIRD prompting struggles and how it affects the validity of qualitative inquiry.

### 4.1 The "Alignment Tax" and the Neutering of Culture

A recurring theme is that "alignment" (safety training) serves as a homogenizing force. In Shrestha et al. (2025), the synthetic non-WEIRD participants were more progressive than real humans. This suggests that the RLHF process—which trains models to be inoffensive and align with Western liberal values—acts as a "cultural filter." When a researcher prompts a model to "act like a conservative rural elder in Rajasthan," the model's safety training likely conflicts with the authentic expression of that persona's potential views on gender or hierarchy, resulting in a sanitized, Westernized simulation. This makes the AI a poor instrument for analyzing data that contains "unaligned" cultural realities.

### 4.2 The Illusion of Consensus

Borchers et al. (2025) found that while temperature and persona shape consensus among AI agents, they yield minimal accuracy gains.25 This points to a danger in AI-assisted qualitative coding: artificial consensus. LLMs are designed to generate probable text, which often means converging on the mean. In qualitative research, the "gold" is often in the outliers and divergences—the "thick description" of unique cultural phenomena. A neutral or even persona-prompted AI tends to smooth over these jagged edges, producing a homogenized analysis that looks consistent (high inter-rater reliability) but lacks cultural depth (low validity).

### 4.3 Table 1: Comparative Efficacy of AI Coding Strategies in Non-WEIRD Contexts

  

|   |   |   |   |   |
|---|---|---|---|---|
|Strategy|Mechanism|Empirical Outcome (Non-WEIRD)|Risks|Key Studies|
|Neutral Prompting|"Analyze themes in this text."|Low Validity. Misses implicit cultural context; interprets ambiguity through Western lens.|Hegemonic imposition; erasure of local meaning.|Sakaguchi et al. (2025); Wei et al. (2025)|
|Persona Prompting|"Act as a [Culture] researcher."|Low/Moderate Validity. Adjusts vocabulary but not interpretive frame. High similarity to US coders persists.|"Cultural Projection"; False confidence; Stereotyping.|Wei et al. (2025); Shrestha et al. (2025)|
|Clerk / Extraction|"List causal links verbatim. Do not interpret."|Moderate/High Utility. Preserves original terms; shifts interpretation to humans.|Requires heavy human labor for synthesis; does not automate meaning.|Powell et al. (2025); Causal Map|
|Reflexive Partner|"Critique this code from a decolonial lens."|High Potential. Uses bias as data; facilitates human reflexivity.|High cognitive load; requires advanced prompt engineering.|i-CCER 22|

## 5. Recommendations for Professional Practice

For social scientists working with non-WEIRD data, the evidence supports the following protocols:

1. Abandon the "Magic Wand" Persona Prompt: Do not rely on "Act as [Culture]..." prompts to solve validity issues. Assume the model is a Western coder and treat its outputs with the same scrutiny you would apply to a research assistant unfamiliar with the local context.
    
2. Operationalize the "Clerk" Model: Follow the Powell et al. (2025) approach for extraction. Use AI to extract structured data (citations, causal links, entities) where the definition of the object is syntactic rather than semantic. Leave the naming of themes and the inference of meaning to human experts or local stakeholders.
    
3. Validate with "Emic" Experts: As shown in Wei et al. (2025), statistical agreement with the model is meaningless if the model aligns with the wrong cultural group. AI coding of non-WEIRD data must be validated against human coders from that specific culture, not just against the principal investigator.
    
4. Adopt Radical Transparency: Methodological sections must go beyond listing prompts. They must disclose the "Technical Positionality": which model was used, its known biases, and specifically how disagreements between AI and human cultural interpretations were resolved.
    
5. Utilize "Despite" Coding: Use coding conventions that capture tension and failure (e.g., "X happened despite Y") to prevent the AI from smoothing over cultural contradictions or resistance narratives.5
    

## 6. Conclusion

The integration of AI into social science offers scale, but at the cost of specificity. The studies reviewed in this report—particularly the comparative work of Wei et al. and the validation studies by Powell and Sakaguchi—demonstrate that non-WEIRD positionality prompts are currently insufficient to overcome the deep-seated Western bias of Large Language Models.

The AI "persona" is a mask, not a mind. When that mask slips—as it inevitably does during complex interpretive tasks—the underlying WEIRD logic reasserts itself, potentially distorting the lived realities of non-Western populations. Therefore, the most rigorous path forward is not better prompting, but better process: architectures of collaboration that keep human cultural expertise as the "architect" of meaning, while relegating AI to the role of a powerful, but culturally illiterate, clerk. The future of equitable social science with AI lies not in teaching the machine to be "us," but in rigorously understanding precisely how it is not.

#### Works cited

1. (PDF) How much of a pluralist is ChatGPT? A comparative study of value pluralism in generative AI chatbots - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/publication/393680123_How_much_of_a_pluralist_is_ChatGPT_A_comparative_study_of_value_pluralism_in_generative_AI_chatbots](https://www.researchgate.net/publication/393680123_How_much_of_a_pluralist_is_ChatGPT_A_comparative_study_of_value_pluralism_in_generative_AI_chatbots)
    
2. Discipline and Label: A WEIRD Genealogy and Social Theory of Data Annotation - arXiv, accessed on January 22, 2026, [https://arxiv.org/html/2402.06811v1](https://arxiv.org/html/2402.06811v1)
    
3. Who Gets Heard? Calling Out the "Hard-to-Reach" Myth for Non-WEIRD Populations' Recruitment and Involvement in Research - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/publication/391241012_Who_Gets_Heard_Calling_Out_the_Hard-to-Reach_Myth_for_Non-WEIRD_Populations'_Recruitment_and_Involvement_in_Research](https://www.researchgate.net/publication/391241012_Who_Gets_Heard_Calling_Out_the_Hard-to-Reach_Myth_for_Non-WEIRD_Populations'_Recruitment_and_Involvement_in_Research)
    
4. Emulating Public Opinion: A Proof-of-Concept of AI-Generated Synthetic Survey Responses for the Chilean Case - arXiv, accessed on January 22, 2026, [https://arxiv.org/pdf/2509.09871](https://arxiv.org/pdf/2509.09871)
    
5. site.pdf
    
6. A tutorial for integrating generative AI in mixed methods data analysis - University of Pretoria, accessed on January 22, 2026, [https://repository.up.ac.za/bitstreams/f46b73d6-8209-4a55-9952-7c231f9a09e6/download](https://repository.up.ac.za/bitstreams/f46b73d6-8209-4a55-9952-7c231f9a09e6/download)
    
7. (PDF) Beyond WEIRD: Can synthetic survey participants substitute for humans in global policy research? - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/publication/388818114_Beyond_WEIRD_Can_synthetic_survey_participants_substitute_for_humans_in_global_policy_research](https://www.researchgate.net/publication/388818114_Beyond_WEIRD_Can_synthetic_survey_participants_substitute_for_humans_in_global_policy_research)
    
8. (PDF) Building a methodological profile for communication's study of the passive generation of information - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/publication/398317679_Building_a_methodological_profile_for_communication's_study_of_the_passive_generation_of_information](https://www.researchgate.net/publication/398317679_Building_a_methodological_profile_for_communication's_study_of_the_passive_generation_of_information)
    
9. Cultural Alignment and Biases in Qualitative Coding: Comparing GPT and Human Coders, accessed on January 22, 2026, [https://www.researchgate.net/publication/397476558_Cultural_Alignment_and_Biases_in_Qualitative_Coding_Comparing_GPT_and_Human_Coders](https://www.researchgate.net/publication/397476558_Cultural_Alignment_and_Biases_in_Qualitative_Coding_Comparing_GPT_and_Human_Coders)
    
10. Zhanlan Wei (0009-0002-3931-6398) - ORCID, accessed on January 22, 2026, [https://orcid.org/0009-0002-3931-6398](https://orcid.org/0009-0002-3931-6398)
    
11. Andres Felipe Zambrano's publications - SciProfiles, accessed on January 22, 2026, [https://sciprofiles.com/user/publications/1269355](https://sciprofiles.com/user/publications/1269355)
    
12. Jaclyn L. Ocumpaugh's research works | University of Pennsylvania and other places, accessed on January 22, 2026, [https://www.researchgate.net/scientific-contributions/Jaclyn-L-Ocumpaugh-2159233011](https://www.researchgate.net/scientific-contributions/Jaclyn-L-Ocumpaugh-2159233011)
    
13. Amanda BARANY | Research Assistant | PhD | Drexel University, Philadelphia | DU | Educational Leadership and Learning Technologies | Research profile - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/profile/Amanda-Barany](https://www.researchgate.net/profile/Amanda-Barany)
    
14. Evaluating ChatGPT in Qualitative Thematic Analysis With Human Researchers in the Japanese Clinical Context and Its Cultural Interpretation Challenges, accessed on January 22, 2026, [https://www.jmir.org/2025/1/e71521](https://www.jmir.org/2025/1/e71521)
    
15. Evaluating ChatGPT in Qualitative Thematic Analysis With Human Researchers in the Japanese Clinical Context and Its Cultural Interpretation Challenges - NIH, accessed on January 22, 2026, [https://pmc.ncbi.nlm.nih.gov/articles/PMC12062757/](https://pmc.ncbi.nlm.nih.gov/articles/PMC12062757/)
    
16. Evaluating ChatGPT in Qualitative Thematic Analysis With Human Researchers in the Japanese Clinical Context and Its Cultural Interpretation Challenges: Comparative Qualitative Study - PubMed, accessed on January 22, 2026, [https://pubmed.ncbi.nlm.nih.gov/40273439/](https://pubmed.ncbi.nlm.nih.gov/40273439/)
    
17. Evaluating ChatGPT in Qualitative Thematic Analysis With Human Researchers in the Japanese Clinical Context and Its Cultural Interpretation Challenges: Comparative Qualitative Study | Request PDF - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/publication/391116901_Evaluating_ChatGPT_in_Qualitative_Thematic_Analysis_With_Human_Researchers_in_the_Japanese_Clinical_Context_and_Its_Cultural_Interpretation_Challenges_Comparative_Qualitative_Study](https://www.researchgate.net/publication/391116901_Evaluating_ChatGPT_in_Qualitative_Thematic_Analysis_With_Human_Researchers_in_the_Japanese_Clinical_Context_and_Its_Cultural_Interpretation_Challenges_Comparative_Qualitative_Study)
    
18. Beyond WEIRD: Can synthetic survey participants substitute for humans in global policy research?, accessed on January 22, 2026, [https://eprints.lse.ac.uk/127300/1/shrestha-et-al-2025-beyond-weird-can-synthetic-survey-participants-substitute-for-humans-in-global-policy-research.pdf](https://eprints.lse.ac.uk/127300/1/shrestha-et-al-2025-beyond-weird-can-synthetic-survey-participants-substitute-for-humans-in-global-policy-research.pdf)
    
19. Generative AI in service research: promise or peril? - Taylor & Francis, accessed on January 22, 2026, [https://www.tandfonline.com/doi/pdf/10.1080/02642069.2025.2525893](https://www.tandfonline.com/doi/pdf/10.1080/02642069.2025.2525893)
    
20. Generative AI to augment behavioral research—evidence from the Middle East - PwC Strategy, accessed on January 22, 2026, [https://www.strategyand.pwc.com/m1/en/ideation-center/ic-research/2025/gen-ai-behavioral-research/gen-ai-behavioral-research.pdf](https://www.strategyand.pwc.com/m1/en/ideation-center/ic-research/2025/gen-ai-behavioral-research/gen-ai-behavioral-research.pdf)
    
21. The Emergence of Hyper-Consumerism in UAE Society: A Socio-Cultural Perspective, accessed on January 22, 2026, [https://www.researchgate.net/publication/327128423_The_Emergence_of_Hyper-Consumerism_in_UAE_Society_A_Socio-Cultural_Perspective](https://www.researchgate.net/publication/327128423_The_Emergence_of_Hyper-Consumerism_in_UAE_Society_A_Socio-Cultural_Perspective)
    
22. Exploring undiscovered country: AI-empowered collective and collaborative epistemic reflexivity (i-CCER) - RMIT Research Repository., accessed on January 22, 2026, [https://research-repository.rmit.edu.au/ndownloader/files/60363914/1](https://research-repository.rmit.edu.au/ndownloader/files/60363914/1)
    
23. Full article: Exploring undiscovered country: AI-empowered collective and collaborative epistemic reflexivity (i-CCER) - Taylor & Francis, accessed on January 22, 2026, [https://www.tandfonline.com/doi/full/10.1080/0267257X.2025.2566931](https://www.tandfonline.com/doi/full/10.1080/0267257X.2025.2566931)
    
24. The price of positionality: assessing the benefits and burdens of self‐identification in research methods - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/publication/362272023_The_price_of_positionality_assessing_the_benefits_and_burdens_of_self-identification_in_research_methods](https://www.researchgate.net/publication/362272023_The_price_of_positionality_assessing_the_benefits_and_burdens_of_self-identification_in_research_methods)
    
25. Conrad BORCHERS | PhD Student | Master of Science | Carnegie Mellon University, Pittsburgh | CMU | Human-Computer Interaction Institute | Research profile - ResearchGate, accessed on January 22, 2026, [https://www.researchgate.net/profile/Conrad-Borchers](https://www.researchgate.net/profile/Conrad-Borchers)
    

**