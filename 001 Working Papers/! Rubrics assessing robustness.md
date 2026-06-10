---
tags:
  - paper
date: 2026-04-20
---

# Phase 1: Testing AI Recall and Precision (The Coding Phase)

- **The Goal:** Test the hypothesis that adding extra custom columns to the initial coding prompt increases the AI's reasoning burden, thereby reducing its **recall** (how many true links it finds) and/or **precision** (how accurate those links are).
- **The Variables:** sentiment is heavily baked into LLM training, making it a poor variable for testing cognitive load. Instead, I will test the two link-level custom columns explicitly mentioned in the Causal Map quality assurance guidance: **Certainty (Conviction)** and **Strength**.
    - _Certainty (Conviction):_ Records how sure the source sounds about the claim (e.g., using a weak / neutral / strong scale).
    - _Strength:_ Records if the source explicitly states whether the causal influence itself is strong or weak.
- **The Process:** You will run the AI-assisted coding in two variations:
    - _Control Prompt:_ A basic prompt extracting just the causal claims.
    Approved 
    #### Prompt
		Later I will give you interviews, including Focus Group Discussions, about an international development project that works to enhance climate resilience and sustainable livelihoods through the protection and regeneration of Boswellia papyrifera forests and improved participation in the frankincense value chain.
		
		***Your task:***
		Try to understand the overall causal network in these texts: what is causing what, and how are they interrelated? Then give me a standard table with columns, Cause, Effect, Quote and Sentiment.
		Identify places where someone says that something causes or leads to or influences another thing, and identify how these kinds of claims fit together into causal chains or networks.
		Each row is one causal link mentioned in the text. List the Cause and Effect and give an EXACT, VERBATIM Quote backing up the causal link. Find common elements which appear as cause and/or effect multiple times, forming chains and other patterns that tell bigger stories, not just isolated pairs of links.
		Only report relationships which are really causal. Do not report hypothetical links or stories about the future or what someone would like to be true. Only report relationships which are a clear causal influence of one clearly identifiable thing or event on another.
		
		Labelling rules:
		1. The Cause and Effect labels should not themselves contain causal ideas like 'due to...' or 'because of...' Delete or correct or add links if necessary.
		2. Make sure to write clear, concrete and specific labels for the Cause and Effect, using the language in the text, that say what actually happened -- but rephrase anything that the ordinary reader would not understand in a more general way if necessary.
		3. Make sure the Cause and Effect are distinct; the Cause should not mention the Effect, and vice-versa.
		4. Use a special coding style of labelling: General Label; Specific Detail. 
		 - Include Actors/Locations: Try to always add the general actor responsible for the factor/causal claim in the Specific Detail part of the label using its full name or official abbreviation. For example: donor, Tree Aid, organisation X, community, youth, women etc. 
		However, remember to create clear, understandable labels, and never just add an actor as the entire label. 
		To ensure all causal factor labels are consistent for analysis, you must standardise any label that refers to a specific organisation, country, person, or place. But, do not include the specific proper noun in the main part of the label. Instead, use a generic descriptor for the actor/entity. Then, add the specific name after a semicolon (;) at the end.
		The required format is: [Generic Descriptor/Label]; [Specific Detail]
		For example: Increased income; selling more, or Increased income; making more money, etc.

		5. DO NOT give your opinion or draw conclusions, just print all of the causal claims within the texts.
		6. Bear in mind the meaning of these words and use them in the labels:
		- For 'TreeAid', 'Tree Aid', 'TA', 'EC0', and similar, write 'EC0 project'
		- For 'Frankincense', ‘Incense’, 'Itan', ‘Aduris’, ‘Duris’, ‘Adurs’, ‘Meker’ and similar, write ‘Frankincense’
		- For ‘PFM’, ‘PFMC’, ‘Participatory Forest Management Group’, ‘ forest protection committee’ and similar, write ‘PFM’
		- For ‘FSS’, ‘Fuel Saving Stoves’, ‘Fuel saving group’, and similar, write ‘FSS'
		- For ‘VTE’,  ‘Village Tree Enterprise’ and similar, write ‘VTE’
		- Mingaf is an ousing blade needed to tap the Boswellia tree to produce frankincense
		7. Some causal claims might mention other organisations working in the area, make sure to name every actor involved in the causal chain in the label.
		
		  **Quote**
		- The quote **must be a verbatim excerpt** from the text.
		- **Do NOT modify or translate it.**
		- **Do NOT break sentences apart or reassemble them differently.**
		- Do not provide links without a quote in this format.
		
		**Sentiment:**
		In the Sentiment column, give a number to rate the sentiment of the effect of the causal link.
		- 1 = Positive effect
		- 0 = Neutral or unclear effect
		- -1 = Negative effect
		
		- Consider the context and speaker's perspective when determining sentiment: what did the effect, outcome or result of this causal link mean to the speaker?
		- Use 0 for Effects that are purely descriptive, have no clear positive/negative connotation, or when sentiment is ambiguous.
		
		  **General**
		- The same piece of text or quote can be the basis for multiple but different links or chains.
		- Do not use bullet points or quote marks when printing out your answer, and do not prefix your answers with 'Cause: ' or 'Effect: '
		- Remember that one cause can have several effects, one effect can have several causes.
		- Make sure you do print out each and every causal chain, even if similar chains or links are repeated in different parts of the text. Your job is not to summarise but to provide every detail. If the text repeats the same or similar causal information several times, provide a separate chain each and every time.
		- These interviews were recorded in Amharic and translated into English, so some parts of the interviews might not be as clear. So make an effort to understand all of the causal claims mentioned in the text and report them; DO NOT skip any links. However, make sure all of the links have clear evidence in the text; DO NOT infer or invent anything. 
		- Your causal network should not be mostly fragments, individual links on their own. You need to try hard to make a coherent story out of all these fragments.
		- All of the verbatim quotes must be from the statements, do not make up any quotes.
		- Do not invent or assume causes or efects. The evidence for the causal chain must be in the text.
		- Make your labels as clear as possible for someone who never read the text
		- I love it when you find longer chains
		- Pay attention to the direction of each link to print them correctly.
		- Those are your instructions.
		
		=====
		Good, but your causal network is mostly fragments, individual links on their own. You need to try much harder to make a coherent story out of all these fragments. So give me the same links table again with the same columns and the same quotes, but find a set of factors (cause or effect labels) which express the same idea and rewrite them with a common label expressing that common idea. Repeat with other sets of similar labels until you have a much more connected causal network. But don't make stuff up, your relabelling must be true enough to the original meanings. And don't forget to also include links which in spite of your efforts are not part of a larger story. Don't forget the sentiment column!

    - _Complex Prompt:_ A prompt asking the AI to extract causal claims _and_ simultaneously evaluate the text to populate the Certainty and Strength columns.
- **The Metric:** compare the recall and precision between the two variations to see if the extra effort of evaluating Certainty and Strength degraded the AI's core extraction performance.

# Phase 2: Bundle Assessment (The Rubrics Phase)

- **The Goal:** This is the "second moment" of quality assurance, where you cross the gap from evaluating individual claims to evaluating the robustness of the evidence as a whole.
- **The Process:** After the AI has finished the initial coding in Phase 1, you group the individual causal claims into bundles (sets of links starting at the same cause and finishing at the same effect).
- **Applying the Rubrics:** This is where your rubrics (**Uniqueness, Triangulation, and Factuality**) actually belong. Using the app's assessment panel, you will look at the entire bundle, along with all its underlying quotes and source metadata, and judge its overall quality against your rubrics. Based on this rubric score, you will decide whether the bundle's evidence is robust enough to be collapsed into a single, verified "assessed link"






Draft

Use tree aid? 
choose a map and work on the bundles only on that map

Choose a dataset (maybe example-file or lonely in London to compare between: 
- our standard AI-coding approach (steve suggested mermaid, but I'm not really used to it, so I might go with our normal approach with sentiment and type columns) 
- using rubrics approach (come up with one after reading the articles) adding like 3 more columns 

1. Experiment/Phase 1: Check how much the links coverage decreases with adding new columns/coding tasks i.e rubrics 

Phase 2: Robustness/Certainness: how much certain about the causal claim is the respondent? 

My question: do I also assess the links after raw coding or only check the links coverage with the new columns?

look at the aggregate numbers on each bundle --> like citation and source count and average sentiment 