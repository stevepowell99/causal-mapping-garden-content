---
date: 2025-05-17
---

https://docs.google.com/document/d/1tVKctp5F_p4NNbQzVU7l2ZBpiuGLE1vbUWVMPa849KE/edit?tab=t.0
**

# AI in Text Analysis for Evaluation: Taming the Black Box through Verifiable Micro-Tasks

1. Introduction: The Allure and Peril of AI in Evaluation

Project evaluation, a discipline heavily reliant on the analysis of textual data such as reports and interview transcripts, increasingly turns to Artificial Intelligence (AI) for assistance. The allure is understandable: AI promises efficiency and the potential to unearth insights from vast datasets.1 However, this technological embrace comes with a significant caveat—the "black box" problem. As AI models grow more complex, understanding their internal workings becomes increasingly challenging, posing significant issues for transparency, interpretability, and explainability.3 If evaluators did not possess a clear, transparent workflow from textual data to evaluative judgments before the introduction of AI, relying on opaque AI processes to bridge that gap is a perilous proposition. The potential for AI hallucinations and inherent biases raises further concerns about the validity of purely AI-generated outputs, especially in high-stakes decision-making.4 This article argues that the responsible and effective use of AI in text analysis for project evaluation hinges on a crucial methodological principle: the deconstruction of large, ambiguous evaluative tasks into multiple, smaller, and, critically, intersubjectively verifiable steps. By confining AI to these "tiny black boxes," we limit its evaluative autonomy, enhance transparency 5, and retain human oversight over the ultimate judgments. This approach is vital because the lack of transparency and accountability in AI can lead to significant legal and ethical challenges.7 

2. AI's Strength: Excelling at Specific, Verifiable Micro-Tasks

AI, particularly Natural Language Processing (NLP) and machine learning (ML) models, demonstrates considerable power in processing text.1 However, its true strength in an evaluative context is not in making broad, subjective judgments but in executing specific, well-defined tasks that can be intersubjectively verified. "Intersubjectively verifiable" means that multiple human reviewers, when presented with the same micro-task and data, would largely agree on the outcome, a cornerstone of reliable qualitative analysis.9 The challenge with "big black boxes" is that their complex internal processes often lack the transparency needed for such verification.1 This opacity can obscure how an AI arrives at a conclusion, making it difficult to assess fairness, identify biases, or ensure accountability.5

Consider the contrast:

- Opaque, Non-Verifiable Task (Unsuitable for AI alone): "Is the intervention described in this report efficient and effective?" Such a question invites the AI into a complex evaluative judgment, bypassing the nuanced human expertise core to qualitative social science. The lack of clear, verifiable steps makes it difficult to trust the output or understand its basis.3 Similarly, asking an AI "What are the main themes in this document?" without detailed parameters on what constitutes a "theme" or the analytical framework to be used (e.g., grounded theory, thematic analysis) is to abdicate essential methodological rigor.11 Even a seemingly simple request like "Summarise this document!" grants the AI vast, unchecked discretion.
    
- Clear, Verifiable Micro-Tasks (Suitable for AI assistance):
    

- "Does this paragraph mention water and sanitation?"
    
- "If so, are any recent changes mentioned?"
    
- "If so, do these sound like positive changes according to the interviewee?" Here, a larger analytical goal is broken down. Each step is precise, and its output can be checked. AI can perform such tasks rapidly and consistently across large volumes of text, akin to applying a detailed rubric at scale. This approach ensures that if you can't check the AI's output for a given step, you don't trust it for that step. The focus on intersubjective verifiability at each micro-step is crucial for building trust in the overall analytical process.6
    

The increasing sophistication of AI, including Large Language Models (LLMs), does not negate this principle; rather, it makes adherence to it even more critical.1 While LLMs can generate remarkably human-like text and perform complex operations, their internal reasoning can be opaque.1 Confining them to verifiable micro-tasks mitigates the risks associated with this opacity and allows for more accountable AI integration.4

3. Foundational Methodologies: Deconstruction and Reconstruction as Existing Principles

The deconstruction of analytical tasks into smaller components, followed by the reconstruction of findings, is not a new concept introduced by AI; it is inherent in established qualitative and even classical computational text analysis methodologies.

- Content Analysis, for instance, traditionally requires the deconstruction of text into manageable coding units (e.g., words, phrases, themes) based on predefined rules.9 This unitizing and coding is a form of deconstruction. The subsequent analysis, where frequencies are counted or relationships between codes are examined to draw conclusions, is a process of reconstruction.9 Krippendorff's work emphasizes this systematic reduction and analysis.15
    
- Thematic Analysis, as outlined by Braun & Clarke (2006), involves a systematic process of familiarization, coding (deconstruction of data into initial labels), theme identification, review, definition, and reporting (reconstruction of codes into broader themes and an analytical narrative).16 AI can support the initial coding phase, a relatively discrete deconstructive task. However, the subsequent interpretation and refinement of themes—the more significant reconstructive and evaluative leaps—demand the active role of the human researcher who constructs meaning.11
    
- Grounded Theory also involves meticulous coding and categorization (deconstruction) as theory emerges from data through constant comparison, leading to the development of a core category and a substantive theory (reconstruction).12 AI might assist in managing and suggesting initial codes from large text volumes, but the iterative process of comparison and theory building remains a deeply human, interpretive endeavor.
    
- Algorithmic Text Analysis, even in its earlier forms, often involves a step-by-step reduction (deconstruction) of natural language text into a machine-readable abstraction (e.g., vectors, networks of terms). This is followed by the analysis of shapes, relations, and structures within that abstraction (reconstruction) to identify patterns or insights.20 Computational Text Analysis (CTA) uses techniques like word frequency analysis, topic modeling, and sentiment analysis, which inherently deconstruct text into components (words, topics, sentiment scores) and then allow for broader pattern recognition (reconstruction) across large corpora.21
    

Integrating AI effectively means mapping its capabilities onto these already deconstructed steps within established qualitative workflows or designing new workflows that explicitly incorporate this deconstructive-reconstructive logic. The human evaluator's role becomes one of designing these "tiny black box" tasks, programming or prompting the AI to execute them, verifying their outputs, and then synthesizing these outputs into broader evaluative judgments.

4. A Workflow for Verifiable AI-Assisted Evaluation: Assembling the "Tiny Black Boxes"

To implement this deconstructive approach, evaluators must move from posing broad evaluative questions directly to AI, to designing a workflow of interlinked, verifiable micro-tasks. This involves:

1. Deconstructing the Evaluative Question: Break down overarching evaluation questions into a series of smaller, specific, and intersubjectively verifiable sub-questions. What precise pieces of information are needed? What low-level classifications or identifications can be made?
    
2. Designing AI Micro-Tasks: For each sub-question, define a precise task for the AI. This includes specifying the input text, the exact operation to be performed (e.g., identify keywords, classify sentiment on a specific statement, check for the presence of a predefined concept), and the expected output format. Clear instructions are paramount for reliable results.1
    
3. Data Preparation and AI Application: Prepare data according to the requirements of each micro-task. Apply the AI tool to execute these discrete tasks.
    
4. Verification of Micro-Outputs: Crucially, the outputs of these "tiny black boxes" must be systematically checked by human evaluators, at least on a sample basis, to ensure accuracy and reliability. This aligns with the principle: "If you can’t check it, you can’t trust it." This step is vital for ensuring intersubjective verifiability and accountability.4
    
5. Synthesis and Human-Led Evaluation (Reconstruction): The verified outputs from the individual AI micro-tasks are then aggregated and synthesized by human evaluators. It is at this stage that the broader evaluative judgments are made, informed by the AI-processed information but ultimately guided by human expertise, contextual understanding, and ethical considerations. The structured workflow for NLP analysis proposed by Feuerriegel et al. (2025)—encompassing clear question definition, meticulous data handling, justifiable method selection, transparent analysis, validity assessment, and careful interpretation—provides a valuable framework for managing this process.1
    

This approach, such as highlighting and then aggregating causal links from text data, can provide a structured path from textual data to the brink of evaluative judgment, where human insight then takes precedence.

5. Addressing the "Black Box": Transparency Through Deconstruction

The "black box" nature of many advanced AI models, where the internal logic is not fully transparent 1, is a significant concern. However, by deconstructing tasks into verifiable "tiny black boxes," we shift the locus of transparency. Instead of needing to understand how the AI performs a complex, overarching evaluative judgment (which may be impossible), we focus on understanding what specific, limited task it is performing and verifying that its output for this micro-task is correct. This focus on verifiable micro-tasks helps in building trust and ensuring accountability, even when the overarching AI system is complex.4

This does not eliminate all challenges. Algorithmic bias can still infiltrate even narrowly defined tasks if the training data or the micro-task's design is flawed.5 Data quality remains paramount.1 However, identifying and mitigating bias in a "tiny black box" is a more manageable problem than addressing diffuse bias in an AI tasked with holistic evaluation. Privacy and data security also remain critical considerations when AI processes any textual data.5

The core argument is that by limiting AI's role to well-defined, intersubjectively verifiable sub-components of the evaluation, we reduce the risks associated with its opacity and prevent the AI from making unsupervised, high-level evaluative judgments. The evaluative freedom is curtailed, and human accountability is maintained.

6. Conclusion: AI as a Tool, Not an Oracle, in Evaluation

AI offers powerful assistance for text analysis in project evaluation. However, its effective and ethical use demands a shift away from treating it as an autonomous decision-maker for complex evaluative questions. The key lies in methodological discipline: breaking down large, opaque analytical challenges into a series of smaller, intersubjectively verifiable "tiny black boxes." This deconstruction, followed by a human-led reconstruction of findings, mirrors established principles in both classical and computational text analysis.

This approach allows evaluators to leverage AI's speed and scale for specific, well-defined operations while retaining human control over the design of the analytical process, the verification of intermediate steps, and the ultimate evaluative judgments. It transforms the AI from a potential "black box" oracle into a more transparent and accountable tool.7 Future developments should focus on AI tools and platforms that explicitly support this deconstruction, verification, and reassembly workflow, empowering evaluators to harness AI's capabilities without ceding their critical evaluative responsibilities. This ensures that evaluation methods and qualitative research expertise guide the application of AI, rather than being bypassed by it.

7. References

1

#### Works cited

1. business.columbia.edu, accessed on May 7, 2025, [https://business.columbia.edu/sites/default/files-efs/citation_file_upload/s44159-024-00392-z.pdf](https://business.columbia.edu/sites/default/files-efs/citation_file_upload/s44159-024-00392-z.pdf)
    
2. Natural Language Processing and Social ... - JMIR Mental Health, accessed on May 7, 2025, [https://mental.jmir.org/2025/1/e67192](https://mental.jmir.org/2025/1/e67192)
    
3. Context Is King: Large Language Models' Interpretability in ... - MDPI, accessed on May 7, 2025, [https://www.mdpi.com/2076-3417/15/3/1192](https://www.mdpi.com/2076-3417/15/3/1192)
    
4. Generative AI in Knowledge Work: Design Implications for Data Navigation and Decision-Making - arXiv, accessed on May 7, 2025, [https://arxiv.org/html/2503.18419v1](https://arxiv.org/html/2503.18419v1)
    
5. (PDF) AI Ethics: Integrating Transparency, Fairness, and Privacy in ..., accessed on May 7, 2025, [https://www.researchgate.net/publication/388803359_AI_Ethics_Integrating_Transparency_Fairness_and_Privacy_in_AI_Development](https://www.researchgate.net/publication/388803359_AI_Ethics_Integrating_Transparency_Fairness_and_Privacy_in_AI_Development)
    
6. www.arxiv.org, accessed on May 7, 2025, [https://www.arxiv.org/pdf/2501.13320](https://www.arxiv.org/pdf/2501.13320)
    
7. www.arxiv.org, accessed on May 7, 2025, [https://www.arxiv.org/pdf/2502.15838](https://www.arxiv.org/pdf/2502.15838)
    
8. Ethical Artificial Intelligence in Nursing Workforce Management and ..., accessed on May 7, 2025, [https://pmc.ncbi.nlm.nih.gov/articles/PMC11999746/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11999746/)
    
9. Content Analysis Method and Examples | Columbia Public Health, accessed on May 7, 2025, [https://www.publichealth.columbia.edu/research/population-health-methods/content-analysis](https://www.publichealth.columbia.edu/research/population-health-methods/content-analysis)
    
10. Thematic Research: How To Use in Qualitative Research - Qualtrics, accessed on May 7, 2025, [https://www.qualtrics.com/experience-management/research/thematic-analysis-in-qualitative-research/](https://www.qualtrics.com/experience-management/research/thematic-analysis-in-qualitative-research/)
    
11. Braun, V. and Clarke, V. (2006) Using thematic analysis in psychol ..., accessed on May 7, 2025, [https://psychology.ukzn.ac.za/?mdocs-file=1176](https://psychology.ukzn.ac.za/?mdocs-file=1176)
    
12. Grounded theory methodology - has it become a movement? - PMC, accessed on May 7, 2025, [https://pmc.ncbi.nlm.nih.gov/articles/PMC3376761/](https://pmc.ncbi.nlm.nih.gov/articles/PMC3376761/)
    
13. Generative AI in Qualitative Research: A Systematic Review (2022 ..., accessed on May 7, 2025, [https://www.researchgate.net/publication/383561165_Generative_AI_in_Qualitative_Research_A_Systematic_Review_2022-2024](https://www.researchgate.net/publication/383561165_Generative_AI_in_Qualitative_Research_A_Systematic_Review_2022-2024)
    
14. Understanding Content Analysis in Qualitative Research (Examples included) - Looppanel, accessed on May 7, 2025, [https://www.looppanel.com/blog/content-analysis-in-qualitative-research-example](https://www.looppanel.com/blog/content-analysis-in-qualitative-research-example)
    
15. (PDF) Review of Content analysis: An introduction to its methodology - ResearchGate, accessed on May 7, 2025, [https://www.researchgate.net/publication/362833185_Review_of_Content_analysis_An_introduction_to_its_methodology](https://www.researchgate.net/publication/362833185_Review_of_Content_analysis_An_introduction_to_its_methodology)
    
16. (PDF) Using thematic analysis in psychology - ResearchGate, accessed on May 7, 2025, [https://www.researchgate.net/publication/235356393_Using_thematic_analysis_in_psychology](https://www.researchgate.net/publication/235356393_Using_thematic_analysis_in_psychology)
    
17. Inductive Thematic Analysis vs. Deductive Thematic Analysis in ..., accessed on May 7, 2025, [https://delvetool.com/blog/inductive-deductive-thematic-analysis](https://delvetool.com/blog/inductive-deductive-thematic-analysis)
    
18. afgr.scholasticahq.com, accessed on May 7, 2025, [https://afgr.scholasticahq.com/article/22173-grounded-theory-description-divergences-and-application#:~:text=The%20crux%20of%20Glaser%20%26%20Strauss,coding%20and%20analysing%20data%20concurrently.](https://afgr.scholasticahq.com/article/22173-grounded-theory-description-divergences-and-application#:~:text=The%20crux%20of%20Glaser%20%26%20Strauss,coding%20and%20analysing%20data%20concurrently.)
    
19. Grounded theory research: A design framework for novice researchers - PMC - PubMed Central, accessed on May 7, 2025, [https://pmc.ncbi.nlm.nih.gov/articles/PMC6318722/](https://pmc.ncbi.nlm.nih.gov/articles/PMC6318722/)
    
20. Algorithmic Analysis of Medieval Arabic Biographical Collections ..., accessed on May 7, 2025, [https://www.journals.uchicago.edu/doi/full/10.1086/693970](https://www.journals.uchicago.edu/doi/full/10.1086/693970)
    
21. Language, Power, and Computation: Algorithmic Text Analysis ..., accessed on May 7, 2025, [https://www.coa.edu/live/profiles/4594-language-power-and-computation-algorithmic-text](https://www.coa.edu/live/profiles/4594-language-power-and-computation-algorithmic-text)
    
22. accessed on January 1, 1970, [https://www.researchgate.net/publication/227978808_Three_Approaches_to_Qualitative_Content_Analysis](https://www.researchgate.net/publication/227978808_Three_Approaches_to_Qualitative_Content_Analysis)
    

**