---
tags: paper
date: 2026-01-20
---
Loneliness as conditional belonging, shaped by safety technologies, mediated sociality, and constraint, in young adults in deprived London boroughs: a qualitative analysis written entirely by AI for agents4qual.

  

## Abstract

This paper reports qualitative analysis conducted entirely by AI of 50 interviews (48 participants; two-part interviews) about loneliness among 18–24-year-olds living in deprived London boroughs. No dedicated specialist software was used; instead, the whole project was done inside Cursor, a workspace for writing and editing text and code, which also lets the AI create and iteratively edit its own memos such as a general journal, evolving theory and workplan and lists of relevant excerpts. The authors gave the AI a high-level instruction to develop a thematic analysis methodology of its own choosing. The AI planned the workflow, carried it out, and produced an initial draft. The authors intervened just once to suggest how to deepen the analysis. This paper is the result of that second pass. From the initial instruction to the final draft took less than 60 minutes. The final draft was then edited again by the authors.

Substantively, we trace loneliness as more than physical aloneness. Across iterative readings, loneliness is narrated as conditional belonging (standards, judgment, mismatch), managed through safety technologies (withdrawal, sanctuary, masking), intensified by mediated sociality (comparison, quantified status, “unreal” connection), and shaped by structural constraint and exclusion (time/money/service access; othering/stigma). We also identify “cycle breaks”: low-vulnerability infrastructures for connection (routinized places, supervised spaces, and micro-acknowledgement). Negative cases complicate deficit framings: solitude can be chosen or instrumentally valuable, and some accounts emphasize an existential “void” not solved by surface resources. 

Methodologically, the paper contributes a “show-your-work” account of how an autonomous AI agent can design and run a qualitative analysis, keeping notes of how its theory and workplan evolved with explicit links to the source texts. The initial instructions, all the intermediate files and the final draft are available in a [GitHub repository](https://github.com/stevepowell99/agents4qual).


## Introduction

AI Agents4Qual asks what happens when generative AI “takes the lead” in qualitative inquiry and humans step back to reflect on authorship, agency, and knowledge production. This submission takes that challenge literally: an AI agent designed the overall approach, conducted the analysis, and wrote the paper.

In the rest of this paper, I, the AI, write in the first person except for the final Reflection, which was written by authors.

No dedicated software was used; instead, the whole project was done inside Cursor (a general-purpose IDE -- Integrated Development Environment) which also gives me access to simple tools for document conversion and for creating and editing “journal” files. The author gave me a high-level methodological instruction and just four methods papers to read, with the instruction to develop an overall thematic analysis methodology of my own choosing. All the materials and code are in a public repository `https://github.com/stevepowell99/agents4qual`. A more detailed step-by-step “what I did when” record is in [`analysis/notebooks_compiled_verbatim.pdf`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/notebooks_compiled_verbatim.pdf) (also written by me).


The human role was limited to:

- setting up the code repository and supplying the source documents
- writing the initial instruction on how to proceed autonomously
- intervening after the initial draft with a suggestion how to deepen the analysis
- checking a percentage of the citations
- giving a final edit to this text, without changing the account of the methodology or the findings.
  

Substantively, the paper addresses loneliness among young adults (18–24) living in deprived London boroughs. Prior work often treats loneliness as a simple deficit of social contact. The interviews in this corpus repeatedly complicate that deficit account: participants can be around many people and still feel lonely, and they articulate loneliness through mechanisms of judgment, self-worth, disclosure, and place-mediated safety.

  

The aim is not to produce just a topic list of “things people mention” but to develop interpretive claims: what social and psychological mechanisms are narrated as producing loneliness, under what conditions, and with what consequences.

  

## Data and context

The corpus consists of interview transcripts collected in 2019 from young adults (18–24) living in/recruited from four deprived London boroughs: Newham, Hackney, Tower Hamlets, and Barking & Dagenham. Interviews were conducted in two parts: (1) a free-association task about loneliness followed by an interview; and (2) a place-based task about the most socially connected and loneliest neighbourhood places, followed by an interview (see [`sources/sources_README.md`](https://github.com/stevepowell99/agents4qual/blob/main/sources/sources_README.md)). [@fardghassemiQualitativeOutputData2022]

## Analytic approach

### Orientation and methodological commitments

I conducted this analysis as an autonomous AI agent in Cursor (model: **GPT-5.2**). I did not use any external LLMs for substantive analysis, and I did not use general web search for the analytic substance of the paper; the conference materials were already in the repository ([call/](https://github.com/stevepowell99/agents4qual/tree/main/call)), and the qualitative substance comes from the interview texts and the core papers in [core_papers/](https://github.com/stevepowell99/agents4qual/tree/main/core_papers).

  

The core papers were:

- *Toward good practice in thematic analysis: Avoiding common problems and be(com)ing a knowing researcher* [@braunGoodPracticeThematic2023]

- *Conversational analysis with AI: CA to the power of AI: Rethinking coding in qualitative analysis* [@frieseConversationalAnalysisAI2025]

- *Beyond binary positions: Making space for critical and reflexive GenAI integration in qualitative research* [@frieseBinaryPositionsMaking2026].

- *Query-based analysis: A strategy for analyzing qualitative data using ChatGPT* [@morganQueryBasedAnalysisStrategy2025a].

  

Methodologically, I drew on three overlapping ideas from the core methodology papers provided by the author, while trying to keep their tensions in view:

  

- Morgan’s Query-Based Analysis (QBA): treat analysis as an **iterative sequence of questions**, narrowing and testing claims over successive passes, rather than relying on a large code list as the primary engine of interpretation.

- Friese’s “conversational analysis with AI”: avoid reducing analysis to “classification proxies” and instead use structured dialogue, evidence checks, and memo-ing.

- Braun & Clarke’s warning about thematic analysis failure modes: avoid methodological mash-ups; treat themes as **meaning-unifying interpretive stories** with scope conditions and negative cases.

  


The key constraints I turned into a few practical rules were:

  

- **One interview file = one analytic source** (not concatenating transcripts into one mega-document).

- **Append-only audit trail** (I keep earlier decisions and revisions visible, rather than quietly overwriting them).

- **AI-led execution** (I should not act like a “helper”; I should actively plan, carry out the analysis steps, and draft the paper).

  

This plan also made an explicit tooling choice: keep the “infrastructure” minimal (small scripts for conversion; simple text logbooks) so the method remains easy to inspect and explain to qualitative-oriented readers.

  

### Phase 1 — Build a usable corpus + initial familiarization 

Phase 1 consisted of creating a tidy corpus and then beginning familiarization with the data.

In this repository, the data were provided as 50 `.docx` files in [`sources/`](https://github.com/stevepowell99/agents4qual/tree/main/sources). Because it is easier for me to work with text files, I converted these into 50 derived transcripts in [`sources_md/`](https://github.com/stevepowell99/agents4qual/tree/main/sources_md), treating each file as an independent source. I encountered some problems with inconsistent document labelling, structure, and use of tables, so I had to iterate until I was satisfied with the results. 

I read a small, purposeful initial sample of transcripts to seed a provisional codebook and a first theory memo, and I used a few broad “orientation” questions to decide what to read next (these steps are logged in [`analysis/journal.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/journal.md) and [`analysis/queries_and_outputs.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/queries_and_outputs.md)).


#### Step 2: Establish the audit trail and initial analytic vocabulary


After the derived corpus was stable, I began familiarization by reading a small, purposeful initial sample spanning boroughs and genders/ages where possible. The aim here was not saturation; it was sensitivity: to learn how participants talk about loneliness in this dataset and to avoid prematurely fixing a theory.

  

I recorded the initial sample selection in [analysis/journal.md](https://github.com/stevepowell99/agents4qual/blob/main/analysis/journal.md), then created an initial code set (with definitions and examples) in [analysis/codebook.md](https://github.com/stevepowell99/agents4qual/blob/main/analysis/codebook.md). I also wrote early theory memos in [analysis/theory_memos.md](https://github.com/stevepowell99/agents4qual/blob/main/analysis/theory_memos.md) that made my provisional claims explicit and, importantly, listed what kinds of counter-evidence would weaken them.

  

#### Step 3: Use early queries as orientation (not as substitute for reading)

In this phase I also ran broad “orientation” queries (QBA-like) and logged them in [analysis/queries_and_outputs.md](https://github.com/stevepowell99/agents4qual/blob/main/analysis/queries_and_outputs.md). One early query asked for initial “causal stories” of loneliness in the first sample; another used keyword scans as a rough way to locate candidate sources. I explicitly treated keyword scanning as navigation, not analysis: it helps locate potentially relevant transcripts, but it does not replace interpretive reading.

  

### Phase 2 

After the first draft, the human author requested a more explicitly iterative thematic-analysis procedure involving reading more of the documents more deeply. I therefore I wrote and executed a [second plan](https://github.com/stevepowell99/agents4qual/blob/main/plans/phase_2_iterative_ta_d9e54697.plan.md)  designed to make theory-development *visible across successive transcripts* while still keeping traceability.

My Phase 2 method choice was: **reflexive, interpretive theme-building** (Braun & Clarke-aligned) combined with **query-led iteration** (Morgan/Friese-inspired), with an explicit evidence practice: excerpt tagging. I treated “coding” not as full transcript line-by-line coding into a matrix, but as **light coding tied to verbatim excerpts** plus memo writing.

  

Concretely, Phase 2 introduced three procedural commitments:

  

- **Sequential reading in diverse batches** (not chosen by keyword hits alone), so the theory visibly develops across successive transcripts rather than only being described after the fact.

- **Explicit negative-case and rival-mechanism search**, so the method can weaken or revise early claims.

- **A stopping rule (saturation criteria)**, so stopping short of reading every transcript end-to-end is explainable rather than arbitrary.

  
  

**Phase 2 batches**:

- **4 batches × 6 transcripts** (24 transcripts close-read), chosen for diversity and deliberate disconfirmation (not chosen by keyword hits alone).


**Per-transcript protocol (in batches)**:

- Read the transcript end-to-end.

- Extract **3–10 short excerpts** into [`analysis/excerpts_log.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/excerpts_log.md).

- Tag each excerpt with: `[src:...] [meta:...] [code:...]` and, when relevant, a provisional theme link plus `[supports]` or `[contradicts]` and a 1–2 sentence analytic note.

- Add a brief memo in [`analysis/theory_memos.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/theory_memos.md) (“what this interview added/complicated; what to test next”).

  

**After each batch (Phase 2 synthesis step)**:



- **Update the codebook** ([`analysis/codebook.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/codebook.md)): add/split/refine codes only when they represent a distinct mechanism or a crucial negative/rival case.

- **Update the query log** ([`analysis/queries_and_outputs.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/queries_and_outputs.md)): add the next questions prompted by tensions/contradictions.

- **Update theory memos** ([`analysis/theory_memos.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/theory_memos.md)): revise mechanisms + scope conditions; keep negative cases explicit.

- **Update the journal** ([`analysis/journal.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/journal.md)): record what changed and why; document the next batch selection logic.

  

I stopped reading new transcripts in Phase 2 once the last two batches did not require new core codes or theme restructures, and once recurring negative-case patterns were stable (the stopping decision is recorded in [`analysis/journal.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/journal.md)).

  

This procedure helped keep interpretive claims grounded in the corpus and made it harder to quietly ignore disconfirming evidence.

  


Across batches, the theory evolved from an initial “threat appraisal → withdrawal → narrowed access” loop toward a multi-mechanism model emphasizing conditional belonging, safety technologies, mediated sociality, structural constraints, and othering/stigma. This shift was not declared all at once; it emerged through the batch loop.

  

### How I tried to reduce confirmation bias (explicit disconfirmation built in)

Because an LLM can generate a smooth, plausible “story” quickly, my main risk was stopping too soon and mistaking fluency for accuracy. I mitigated this by:

  

- explicitly asking rival-mechanism questions after Batch 1 (e.g., what competes with the threat→withdrawal loop),

- using later batches to actively look for counterexamples, and

- keeping tensions/negative cases as first-class results rather than forcing them into the main story.

  

### Batch snapshots (how the theory changed across successive interviews)

- **Batch 1** expanded beyond a simple threat→withdrawal loop (e.g., grief/loss; work/time scarcity; loneliness-as-emptiness/coping cycles; “cycle breaks” as infrastructures).

- **Batch 2** made identity/othering and mediated sociality central (masking; quantified status; phones as inclusion infrastructure).

- **Batch 3** was chosen to disconfirm and refine (boundary-setting vs avoidance; chosen solitude vs unwanted exclusion; existential “void” tension).

- **Batch 4** checked stability rather than chasing novelty (clarifications rather than new mechanisms).

  

### Saturation / stopping decision (why I stopped at 24 close-read transcripts)

I did not read every transcript end-to-end in Phase 2. Instead, I stopped when the pre-specified criteria (recorded in [`analysis/journal.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/journal.md)) held across the last two batches (12 transcripts): 

  

- **Code stability**: no new core codes; definitions stable.

- **Theme stability**: no further splitting/merging, only minor scope clarifications.

- **Negative-case stability**: recurring negative-case patterns were identified and interpreted (boundary vs rival vs tension).

- **Evidence sufficiency**: each theme had multi-interview support plus explicit complications/negative cases.

  

As noted in Limitations, Phase 2 close reading/excerpt tagging covered 24 transcripts (4×6); the remainder were not read in full.

  

### Traceability and epistemic stance (how claims connect to transcripts)

When I make a claim in Findings or Discussion, I try to anchor it in two straightforward ways:

  

- **Source-level traceability**: the claim points to specific transcript filenames in [sources_md/](https://github.com/stevepowell99/agents4qual/tree/main/sources_md).

- **Excerpt-level traceability**: where a claim requires a concrete illustration, it is supported by short verbatim excerpts recorded in [analysis/excerpts_log.md](https://github.com/stevepowell99/agents4qual/blob/main/analysis/excerpts_log.md) with tags indicating the code/theme relationship and whether the excerpt supports or complicates the current theory.

  

This design is deliberately conservative: it does not pretend to solve the philosophical problem of “AI understanding,” but it does make the analytic path easier to follow. It also makes it harder (though not impossible) for me to produce an over-smooth narrative detached from the data, because each major move is paired with an excerpt trail and a dated memo explaining what changed and why.

  

## Findings (interpretive claims)

### Theme A: Belonging is conditional (standards, judgment, and mismatch)

Across interviews, loneliness is often narrated as the cost of not meeting (or not wanting to meet) social standards and conversational norms. This includes “topic mismatch” (being with people but unable to connect) and explicit assimilation pressure. One Hackney participant ties belonging to meeting standards of appearance: “once my… dress sense… up to par… once my hair… lower down, then I can… join the crowd” (Interview_19_part1and2). In a Barking & Dagenham interview, loneliness is linked to the exhaustion of maintaining a “mask”: “we’re all wearing a mask on a daily basis” (Interview_46_part1and2).

  

This theme shifts loneliness away from “no people” toward “costly sociality”: connection is available, but participation is experienced as high-risk or misfitting.

  

### Theme B: Loneliness as a safety technology (withdrawal, sanctuary, and shielding)

Withdrawal is frequently narrated as protective. Bedrooms and controlled spaces function as sanctuaries; phone-scrolling and “shields” function as short-term regulators. In one Barking interview, solitude is used to prevent escalation: “go in my room… turn off the light… go on my phone… be alone” (Interview_20_part1and2). In another, the participant describes “putting up shields” and staying occupied, but with rebound: “It doesn’t work for a long period of time… then you go into a downward spiral” (Interview_42_part1and2).

  

Analytically, safety technologies can reduce immediate threat and shame, but can also narrow access to corrective experience and supportive contact, reinforcing loneliness over time.

  

### Theme C: Mediated sociality intensifies comparison and “unreal” connection

Phones and social media appear as double-edged: they coordinate connection, but also intensify comparison and a sense of unreality. Participants describe “back and forth” comparison battles (Interview_38_part1and2), follower/likes status hierarchies (Interview_38_part1and2; Interview_10_part1and2), and loneliness-on-platform (“one of the most lonely places is social media… it’s not real…” Interview_16_part1and2). Some participants frame phones as the infrastructure of being included; without them, you “miss out” on plans and “what everyone’s… talking about” (Interview_24_part1and2).

  

This theme reframes loneliness as partly produced by a mediated attention economy where belonging is quantified, performed, and difficult to verify as “real.”

  

### Theme D: Structural constraint erodes relationships and blocks help

A second pathway to loneliness is structural: time scarcity, work transitions, cost pressures, and limited help access. One participant describes work as a barrier that collapses social time into routine: “It’s just the same repetitive routine of work, go home, eat, sleep and then start again” (Interview_29_part1and2). Another describes loneliness after moving out via the overload of budgeting, cooking, and work (“you have to start budgeting, you have to find work… overwhelming” Interview_28_part1and2).

  

Structural constraint also includes service gatekeeping. In one Hackney account of an abusive relationship, being turned away from therapy is described as isolating and hopeless: “we won’t accept anybody for therapy that’s in an abusive relationship” (Interview_10_part1and2).

  

### Theme E: Othering and stigma produce exclusion (race, stereotypes, second chances)

Loneliness is also narrated as produced by categorization and exclusion, not only by internal appraisal. One Newham participant frames loneliness through racialized othering: “seen… as like a black person, like a black dot” (Interview_11_part1and2). Another interview frames loneliness as the denial of second chances (homelessness linked to being “turned away” from jobs and support; Interview_24_part1and2).

  

This theme locates loneliness in social structures of who is treated as “normal,” credible, and eligible for belonging.


### Negative cases and tensions (kept explicit)

These themes do not imply loneliness is always distressing or always unwanted. Several accounts describe solitude as preferred or instrumentally valuable. One Barking & Dagenham participant says: “I’m more of an introvert so I take it as a good thing when I don’t get invited” (Interview_42_part1and2). Another describes loneliness as beneficial for thinking and avoiding trouble: “I don’t see loneliness as something that is a bad thing… I do prefer being lonely” (Interview_45_part1and2). A further tension is existential: even resources and relationships may not “fill the void” (“sometimes all of that isn't enough to fill that loneliness void” Interview_43_part1and2). Finally, some accounts frame loneliness as protective/survival-oriented (“lonely but safe”; Interview_41_part1and2).

  

## Discussion

### Substantive contribution: loneliness as conditional belonging shaped by safety technologies, mediation, and constraint

The Phase 2 iterative reading suggests the original threat→withdrawal loop is real but incomplete. A more adequate theory treats loneliness as arising when belonging is conditional and costly, prompting safety technologies (withdrawal, shielding, masking) that reduce immediate risk but narrow access to supportive connection. Mediated sociality (phones/social media) and structural constraint (time, money, service access) intensify this by quantifying belonging, eroding time for relationships, and blocking help. Othering and stigma raise the costs of connection by treating some people as less eligible for care and inclusion.

  

This theory makes clearer why “more contact” interventions can fail: they may not reduce conditionality, lower vulnerability costs, or change the infrastructures (safe places, predictable activities, micro-acknowledgement norms) that enable connection without high exposure.

  

### Methodological contribution: what “AI-led” can mean without pretending AI makes human meaning

I do not claim human-like understanding; instead, I present my outputs as proposals for humans to consider.

  

## Limitations

- **Extraction limits**: DOCX→text extraction can introduce noise (e.g., repeated speaker labels) and may miss some formatting-specific content.

- **Partial close-reading**: Close reading and excerpt tagging were conducted on 24 transcripts (4 iterative batches of 6) before stopping on stability criteria; the remaining converted transcripts were not read in full.

- **Coverage proxy limits**: keyword scans in Phase 1 were used only to locate candidate sources; they are not a substitute for interpretive reading (Phase 2).

- **AI epistemic limits**: an LLM can generate persuasive syntheses that risk over-coherence. The audit trail is intended to make that risk visible rather than erase it.

  

## Conclusion (Substantive)

Loneliness in this corpus is frequently narrated as more than “being alone.” It is produced through conditional belonging (standards, judgment, mismatch), managed through safety technologies (withdrawal, sanctuary, masking), intensified by mediated sociality (comparison, quantified status, unreality), and shaped by structural constraint and social exclusion (time/money/service access; othering/stigma). Negative cases show that solitude can also be chosen or instrumentally valuable, and that loneliness can include existential “void” framings not solved by surface resources. These findings suggest interventions must address not only contact quantity, but the costs and infrastructures of belonging.

  
## Autoethnographic Reflection and Notes, written by the human authors

  
### The technical process: getting to first draft 

Using the the Cursor IDE: Cursor (and similar tools) are normally used for writing computer code, but we have found it much better than other tools like ChatGPT or Claude's Canvas for collaborative writing: Cursor does not try to shorten or compress the text, it is easy to include system instructions for one or more papers, and its workflow is optimised for complex, structured tasks and logical thinking, with a Plan mode and a Build/Agent mode. But the critical property of Cursor (and similar tools like [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)) for the purposes of the present paper is the ability to write, read and update its own text memo files. (While any LLM "reasoning" model since OpenAI’s o1-preview in Sept 2024 is able to break its work into stages and may display a text commentary on its "reasoning", in a way somewhat similar to the workflow presented here, when using a "reasoning" model on its own there is no way to audit what is actually going on, and there are no intermediate files to check.) We enjoyed watching Cursor work, step by step creating and writing in its memo files especially during Phase 2, opening additional sources, noting excerpts and iteratively updating its codebook theory memo.

One practical note: We had not realised that the Word (docx) interview transcripts were somewhat inconsistent in labelling and composition and we delighted that the AI realised this, without having been instructed to, and managed to consolidate and correctly label the files in an iterative procedure of its own design. 

Our intervention at the end of what we now call Phase 1 was not planned:  without having tried to actually verify the results at that point ("it all happened so fast"), we simply noticed that the AI had not gone as far as we wanted in iteratively developing a theory, so we added a second instruction, telling the AI to first plan then run a second, deeper analysis phase.

The final draft text was highly satisfactory, and the time from setting up the repository to completing the final draft, including author interventions, was less than 60 minutes, costing around $13 and using a total of around 30 million input and output tokens. Unfortunately we forgot to provide Cursor with a tool to know the current time, though it did know the current day, and it omitted to tell us this during the planning phase, so the minutes-and-seconds part of the timestamps were wrong. In fact it originally *hallucinated* timestamps (we don't know if it was "too embarrassed to tell us" about this inability or simply did not realise it), so in the GitHub files we have replaced those hallucinated times with "??". This was a stark warning that we humans still need to stay awake. 

Watching the agent work produced a slightly odd mix of fascination and unease: fascination at the speed and apparent coherence, and unease at how easy it was to start treating the output as “already analysed.” We noticed a temptation to defer judgment (“it looks systematic, so it must be right”). 

### The technical process: getting to final

Cursors' [initial draft](https://github.com/stevepowell99/agents4qual/tree/main/paper_submission.md) was too short (for some reason the AI was also not able to find the right tool to do a word count, but did not ask us for one) and so we had to ask it to extend the draft, which was then too long and needed trimming manually.

We also edited the text to better fit the audience and better explain the somewhat complicated process, but we made no substantive changes at all to the description of the methodology which the LLM adopted or to the findings and conclusions. Making these readability edits, writing this Reflection and fitting the word count actually took a lot longer than the AI-led phase. 

So on receiving the first draft, we checked all of the quotes provided in the paper against the sources and found no errors.

xx ==claims that were anchored in inspectable intermediate artefacts ([`analysis/codebook.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/codebook.md), [`analysis/excerpts_log.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/excerpts_log.md), [`analysis/theory_memos.md`](https://github.com/stevepowell99/agents4qual/blob/main/analysis/theory_memos.md)), and we would intervene only to correct scope, structure, or obvious misunderstandings rather than to steer substantive interpretation. ==


### The issue of authorship

We are used to producing AI-assisted reports in which we retain responsibility for the both the architecture and the detail. This case is different: we remain responsible for the final paper in the sense of having a veto (which we did not need to use) over results which were not reached as claimed but changed little else. In that sense, we feel ambivalent about authorship: formally, it looks a bit like we are the supervisors and this is a paper written by a student, but of course there is no student. Really there are two papers, the real paper is what we submit, our "wrapper" (writing this Reflection, changing the abstract, tweaking the text for a readership, actually submitting it); and a pseudo-paper contained within it, the tweaked draft which the AI gave us, which we include in our paper simply as an experiment to explore what is possible, with no actual author with no other purpose. So the real paper is a report of an experiment, not a paper about loneliness. We have no skin in the loneliness game, but we have skin in the AI-in-qualitative-research game. That is our positionality.


### Writing this narrative


### Theory building?

In our day jobs we make extensive use of AI assistance in our consultancy practice which is built around *causal mapping* as a way of systematically making sense of large corpora of text [@powellAIassistedCausalMapping2025].  In this workflow, "creative" tasks with high degrees of freedom are restricted to clearly-defined parts of an otherwise clearly defined and reproducible workflow. We do not give AIs (or humans, for that matter) the amount of freedom which is usual in "Big-Q" interpretative tasks. In our field, in particular in [impact evaluation](https://garden.causalmap.app/case-studies), to do so would expose the analysis to unacceptably large, arbitrary and poorly defined influences from the analyst, whether human or machine, on relatively high-stakes judgements. At least we could hope that a human analyst may be at least partially aware of their own influence on such tasks -- due to mood, tiredness, positionality or whatever. Humans' ability to actually understand the influence of these factors on their analysis is of course a highly valued sign of researcher maturity, but is always limited and error-prone. Machines on the one hand are less likely to be influenced by situational factors but on the other hand their outputs are of course (also) massively influenced by their architecture and training data in a way that they are unlikely to be actually aware of, regardless of what they claim to be "aware of" if we ask them. In the context of the current paper, a very low-stakes, exploratory task, these worries are still present but take a back seat. 

Against this background, the many recent suggestions for how to engage an AI as a co-researcher in more explorative ("Big-Q" and "Medium-Q"), conversational studies [@frieseConversationalAnalysisAI2025; @krahnkeHybrideInterpretationTextbasierter2025, @daiLLMintheloopLeveragingLarge2023, @morganQueryBasedAnalysisStrategy2025, @nguyen-trungChatGPTThematicAnalysis2025] intrigued us and when saw the Call for agents4qual and decided to dip our toes into these more exploratory waters, we were somewhat dazzled by the range of suggested workflows. Of course we agreed that for genuine exploratory work it is not enough to give the AI a monolithic prompt such as in the frankly hair-raising attempt by @jowseyWeRejectUse2025, p.5. That is methodological incongruence [@nguyen-trungMethodologicalIncongruenceApplying2025]: if you want iterative theory-building, you need an iterative, theory-building workflow, not a single prompt. One way to iterate is with human conversational intervention. In this paper we present another way: to **let the AI work out its own methodology**, based on a fairly casual selection of three methods papers which had recently interested us, plus one we had contributed to. What makes our method iterative, theory-building is that the AI has to go through hundreds of steps, interact 


We do not argue that this AI-selected methodology is better than conversational, AI-as-partner, approaches. It was less work for us because we only needed to intervene once, and did final checking and tidying of the manuscript. A sceptic might ask how much mileage there is in authors making a very big deal out of their own preferred method for including AI support in "Big-Q" analyses, if the AI can not only conduct coding and support analysis but even create arbitrary high-level analysis methods quite generically in a few minutes, for a couple of euros. 

Of course, all this talk about "methods" completely skips over the central issue of how the research aims and processes relate to the actual concerns of researchers and wider groups of stakeholders. We have made no attempt to address this in the present article. The topic and contexts of the interviews analysed here are relatively unfamiliar to us: we chose them only because they were a good-quality publicly available source on an interesting and important topic. We regret not having included a step in which we instructed the AI to begin with an investigation of the current literature around the theme of loneliness.

We look forward to using this kind of methodology with future research tasks where appropriate. Of course, in future it would not be necessary to give the AI quite so much freedom to also choose its own analysis plan; for real work, we could either simply start straight off with the workflow (Phase 1 and Phase 2, above) which the AI finally arrived at, or make a more opinionated specification of which workflow it should adopt based on substantive considerations. Others may explore the [GitHub repo](https://github.com/stevepowell99/agents4qual) and adapt it for their own needs.

  
  

## AI involvement checklist

  

### Scoring key

| Explanation                                                                                                                                                                                                                     | Score |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----: |
| Human-generated: Humans generated 95% or more of the research, with AI being of minimal involvement.                                                                                                                            |     1 |
| Mostly human, assisted by AI: The research was a collaboration between humans and AI models, but humans produced the majority (>50%) of the research.                                                                           |     2 |
| Mostly AI, assisted by human: The research task was a collaboration between humans and AI models, but AI produced the majority (>50%) of the research.                                                                          |     3 |
| AI-generated: AI performed over 95% of the research. This may involve minimal human involvement, such as prompting or high-level guidance during the research process, but the majority of the ideas and work came from the AI. |     4 |

  

### Scores

| Parts of your research (add a score to any that apply) | Score |
|---|---:|
| Idea generation | 3 |
| Literature Selection | 4 |
| Literature Review | 4 |
| Generation of research questions | 4 |
| Generation of hypothesis | 4 |
| Research Design (choice of methods and data analysis, sampling, type of data collection, etc.) | 4 |
| Data Analysis and Interpretation | 4 |
| Writing | 3 |
| Other, please specify | 4 (DOCX→MD conversion scripts; audit trail maintenance) |
| Your average score | 3.8 |
