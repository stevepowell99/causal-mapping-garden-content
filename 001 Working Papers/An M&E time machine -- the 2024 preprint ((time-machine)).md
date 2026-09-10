---
tags: [paper]
date: 2024-05-10
---

*This is the preprint as first posted on Sage Advance on 10 May 2024, now archived on Figshare at [https://doi.org/10.6084/m9.figshare.33518512](https://doi.org/10.6084/m9.figshare.33518512). A later, much revised version was published as [@powellWorkflowCollectingUnderstanding2025].*

# An M&E time machine: Using AI to measure changes in a system across a time period on features which only emerge during it.

Steve Powell, Gabriele Caldas Cabral, and hannah Mishan

May 10, 2024

## Abstract

People involved in project monitoring and evaluation of complex projects are familiar with what we call the ”time machine” problem: the things we want to measure (drivers, outcomes, intervening factors) may emerge and change unpredictably during a project’s lifespan and so cannot be fully specified until project end: but we need to know about them at baseline so we can design appropriate measurement instruments for tracking change.

We demonstrate a novel workflow to help solve this problem which uses an AI-controlled chatbot to interview respondents, and then uses AI to code the transcripts and identify ”causal links” where stakeholders said that one thing influences another.

We analyse the resulting causal information for differences across time: tracking evidence for emerging trends on emerging variables.

The approach is reproducible, scalable and cost-effective. Further work is needed, especially to address the bias in the language models which drive the AI’s responses.

## Motivation and background: the “time machine” problem and an AI-assisted causal mapping pipeline as a solution to it

### The ”time machine” problem

When conducting monitoring and evaluation of projects we often encounter a central paradox. We would like to nail down definitions of key variables (such as measures for project outcomes and inputs as well as intermediate results and external influences) before we launch our monitoring and evaluation system, in order to deliver summative judgements about how they changed over time and ideally about what caused what; yet we can assume that the actually salient variables are often unknowable at baseline. Situations change, challenges arise which lead to changes in design, different kinds of outputs are delivered, new external factors intervene, unexpected outcomes become important, new causal pathways emerge. An accurate, empirical project theory would usually look very different at endline from the original theory of change. If we use open-ended, qualitative approaches, we might be able to identify the salient variables – but only at endline, which is too late to include them in our measurement plan. We can wait until endline and then ask for a retrospective assessment of the baseline alongside an endline assessment, or we can ask for direct judgements about systems change, perhaps using rubrics (Loveridge and Nyembo, 2021). However we know that these kinds of retrospective assessments and comparisons suffer from an array of problems. A key factor is satisficing, in which individuals rely on an expected implicit theory of change and report greater change than what may have actually occurred (Lam and Bengo, 2003). Moreover, retrospective self-reports are limited by recall bias*(Shiffman, Stone, & Hufford, 2008)*.

We seem to need a time machine. If only we could at baseline jump into the future to find out what the salient variables are and bring them back and put them in our questionnaire. Or if only we could at the endline jump back to baseline, armed with a questionnaire from the future.

### Causal mapping as part of the solution

One promising way to address these latter two problems is by using *causal mapping* (Ackermann and Eden, 2004; Axelrod, 1976; Eden et al., 1992; Hodgkinson and Clarkson, n.d.; Laukkanen and Wang, 2016; Powell, Copestake, et al., 2023) - the collection, coding and visualisation of interconnected causal claims. Causal mapping usually involves identifying causal claims within a set of texts. Each piece of text which contains information that a source S claims that X causally influences Y is coded: represented as a directed link or arrow in a network from node X to node Y, whereby for each link, the information about the provenance of the information, the source S, is also noted. Causal mapping can help make sense of large quantities of text data from interviews or documents, especially when used inductively rather than with a fixed codebook. It provides a structured approach to synthesising (some of) the meaning of texts, providing a relatively generic way to extract meaning, and emerging meaning, rapidly and at scale. We can see causal mapping as a form of qualitative data analysis in which the fundamental act of coding requires creating not a single tag or theme but an ordered pair of tags, the cause and the effect[^1].

We sometimes use the phrase “causal landscapes” to describe the object of causal maps. This is to emphasise that we are most interested in the contents and layout of the broader world in which stakeholders understand themselves to be living in, rather than to focus on the details of specific links within it.

Understanding the “causal landscapes” implicitly or explicitly present in stakeholder narratives or project documentation can play a key role in evaluation. For example, we can compare them with the official project theory of change to get a picture of what might *really* be happening (Powell, Larquemin, et al., 2023). Or we can use them to triage masses of information to identify key outcomes and possible causal pathways when planning an Outcome Harvesting project. The Qualitative Impact Protocol (QuIP[^2]) uses causal maps to assemble information about how project interventions may have influenced key outcomes and to make careful inferences about project contributions.

#### Using causal mapping to help solve the time machine problem

Our suggestion comprises the following four steps:

1. At baseline and endline[^3], we can interview stakeholders about key issues of mutual interest (for example, outcomes) and ask what drives these issues, and how the issues and the drivers are themselves interrelated. For example we can ask about outcomes and causes of outcomes and causes of causes. (We use the term “causal” here in the loosest sense: the sense in which we make causal connections every day using ordinary language when we say that one thing contributes to or drives or influences another, or makes, or might make, something else happen.)

2. We can then use causal mapping rules to identify causal claims within transcripts of these interviews. (As we do not yet know which are the most salient features across time points, we are not able to provide a codebook for the coding.) Each claim is a link between one cause and one effect. This will result in many individual causal maps, one per source or stakeholder, at baseline and endline[^4]. As we are not using a codebook, this means that there will be many different labels for the causes and effects, many of which are likely to overlap in meaning. This means it will be hard to build synthesis maps or in particular to compare maps across time. This is the reason for the next step.

3. We then cluster all these labels into a small number of important clusters, allowing us to draw simplified maps in which the nodes or factors are groups of many different labels from the raw data, with similar meaning.

4. Finally, to analyse system change over time through the eyes of the stakeholders. For each link and factor in the overall map we can investigate whether it was mentioned more or less frequently across timepoints.

#### Scaling the approach

Gathering and processing sufficient data for this kind of approach has been a time-consuming task which is almost impossible to carry out at scale or as frequently as we need, or timely enough to be relevant. Recent advances in AI raise the question: can we use AI to *gather* and to *process* this kind of information at scale? We will break this question down into two parts, as presented below.

The feasibility of this “AI-assisted causal mapping pipeline” depends on positive answers to these two questions.

## Research questions

### Question 1: can an automated interview bot successfully gather causal information at scale?

Prior to the challenge of extracting causal claims from stakeholder narratives is the challenge of gathering or eliciting those narratives (or other textual information such as in the form of reports or messages). How are we to gather large quantities of information from stakeholders? One possibility is to analyse existing reports or other texts such as social media posts (Hasan et al., 2019). Here we discuss the potential of more deliberate data gathering via interview.

**Data gathering with chatbots** , powered by artificial intelligence, has become popular in various business operations, such as marketing research, customer service, sales, and product innovation. Chatbots have been used to gather customer data and feedback and to provide automated responses to frequently asked questions. Using such tools can reduce time constraints and costs, and provide insights into audience preferences and needs (Yuen, 2022). Beyond corporate contexts, AI has been used for interviewing in qualitative research, emerging as a promising approach that can offer advantages such as efficiency, scalability, and consistency (Chopra and Haaland, 2023).

The quality and validity of the AI interviews depend largely on the quality and specificity of the prompts that are used to guide the AI models. Instructing the bot to be able to conduct serious qualitative interviews is more of an art than a science. Several tests will be necessary until the bot behaves correctly. The response of the AI is highly sensitive to small differences in the exact starting conditions (the ”prompt” and other factors) (Jang and Lukasiewicz, 2023). The AI may miss some subtle cues or nuances that a human interviewer would notice. It also may not be able to create rapport or provide appropriate feedback or support to interviewees who may experience emotional distress or discomfort during the interview (Chopra and Haaland, 2023; Ray, 2023). In particular we know that the large language models (LLMs) which power the AIs are not very good at “putting two and two together” - combining information which lies far apart in a conversation or text - especially when not explicitly asked to. This means researchers must carefully consider the subject matter, research questions and respondent sample before employing an AI to conduct the interviews.

The methods section below outlines how we designed interview guidelines for a short open-ended interview which could be followed by an AI-powered interviewer. Our research question asks *whether this kind of chatbot can produce useful and trustworthy* (Montrosse-Moorhead, 2023) *interview transcripts containing causal information, and can it do that at scale?*

Question 2: can automated causal mapping successfully code and synthesise causal information at scale, in such a way as to be able to assess change between timepoints?

Making sense of texts by assigning codes or topics to text sections (or even entire documents) is a task which can be called thematic analysis (Braun et al., 2020; Braun and Clarke, 2006) or Qualitative Data Analysis (QDA) (Lacey and Luff, 2001). Approaches to automate this process have moved on from topic modelling based on counting and clustering the words in the texts (Blei et al., 2003) to procedures which use LLMs to capture the meaning of longer sections of text (Sia et al., 2020).

However our task is more specific: identifying not just general meanings but specifically causal relationships. Coding texts by hand for causal mapping has until recently required detailed work by trained analysts and has been quite time consuming. A typical sample (as in the QuIP, (Copestake, 2020) might be in the order of 24 interviews, which might take a trained analyst two to three weeks to code. Thus it has remained a relatively niche approach. The limited sample size means it is difficult to make generalisations or to make comparisons between subgroups or across time points, which reduces its utility for program monitoring.

Earlier language models (Devlin et al., 2019) and other machine-based techniques have been used to identify causal relationships expressed in text (Dunietz, 2018; Dunietz et al., 2017; Rory Hooper et al., 2023). For an overview see (Yang et al., 2022). However, these were highly specialised procedures which required ”training” the models. The advent of very large language models (LLMs) promises to make this process much easier because we can rely on the model’s inherent understanding of causality and directly ask the model simply to “identify causal claims” rather than having to define and specify exactly what this means.

Evaluators such as Davies and Ferretti (Davies, 2023; Ferretti, 2023) have recently been demonstrating the possibilities of AI in evaluation, for example with asking AIs for summaries or global syntheses of texts. It is even possible to ask an AI to make a synthesis of the main causal links within a text and produce a diagram directly (Graham, 2023). However, when doing this, evaluators have to take care not to leave fundamental *evaluative* decisions such as “within this text, what are the most important claims”, or “how to summarise the different actual claims within the text” to the LLM. Evaluators should be wary of transferring the responsibility for making evaluative judgements to an unknown third party, the “black box” of the AI (Choudhary et al., 2022). In contrast to the “black box” approaches to text analysis, this paper describes an attempt to use the power of generative AI more transparently, as a low-level but tireless coding assistant in the tradition of QDA or thematic analysis, who follows detailed instructions in a reproducible way, which leaves the evaluator with the responsibility of making evaluative judgements on the basis of the results. We describe coding guidelines designed to extract causal information from the documents with little guidance, in order to be processed and labelled in a standardised way, again with little additional guidance.

Finally we turn to the last piece of the puzzle: comparing the frequency of automatically extracted themes or topics in datasets across time points (Yoganarasimhan and Yakovetskaya, 2023). We are not aware that this has been done either for the special case of causal factors/topics or within the monitoring and evaluation literature. BathSDR have conducted some unpublished comparisons of causal factors across time within QuIP studies, but the sample sizes involved and amounts of data processed have not justified more than tentative conclusions about system change over time.

In summary, our second research question asks: *can this kind of procedure result in a useful overall summary of the “causal landscape” around the topic of interest as described by the selected respondents, in such a way that changes in this system or landscape across time points can be identified?*

Table 1: the two research questions addressed in this paper, the steps of the “AI-assisted causal mapping pipeline”, and how these are aligned with one another.

| Step | Task | Research question | Tool used |
|---|---|---|---|
| 1 | 1a) Clarifying evaluation questions<br>1b) Designing an interview instruction<br>1c) Sending interview link (at different timepoints) and downloading transcripts | Question 1: can an automated interview bot successfully gather causal information at scale? | Qualia |
| 2 | 2a) Constructing a coding guideline<br>2b) Coding combined data (from different timepoints) as links between causal factors | Question 2: can automated causal mapping successfully code and synthesise causal information at scale?... | Causal Map |
| 3 | 3a) Clustering the causal factor labels into more general clusters<br>3b) Providing labels for the clusters | Question 2: can automated causal mapping successfully code and synthesise causal information at scale?... | Causal Map |
| 4 | 4) Finding differences between timepoints: Using the causal maps to examine differences between the (pooled) sets of transcripts at different timepoints | Question 2 (second part)… in such a way as to be able to solve the time machine problem and compare | Causal Map |

## Method: the “AI-assisted causal mapping pipeline” with automated interviews and coding

We present a procedure which harnesses the power of AI in two ways: firstly to carry out large numbers of automated, qualitative, online interviews and secondly to automatically code and process the transcripts in order to present overview causal maps of the respondents’ causal landscapes.

We illustrate the procedure with a proof-of-concept research study.

### Step 1: Conducting the chat interviews

As we had limited resources we decided to use online workers as respondents, recruited via Amazon’s MTurk platform[^5] (Shank, 2016). We wanted to choose a generic theme on which randomly chosen participants would be likely to have some causal opinions and information. So we decided to investigate respondents’ ideas about problems facing the USA and the reasons for those problems. This unsophisticated way of recruiting respondents means that the results can not be generalised to a wider population in this case.

The research theme was generic - we had no specific expectations of it and had no specific evaluative questions in mind. Our aim was to demonstrate a method which can be easily adapted to a specific research question and which can provide answers to evaluative and comparative questions.

A semi-structured interview guideline was designed on the theme of ”What are the important current problems facing the USA and what are the (immediate and underlying) reasons for those problems?”.

This interview guideline was implemented via an online interview ”bot” called ”Qualia[^6]”, which uses the OpenAI Application Programming Interface (API) to control the bot’s behaviour. Qualia is a simple chat-based web app which is designed to elicit stories about ”what influenced what” from multiple respondents, in an AI-driven interview format. Similar to other online data gathering platforms, respondents are sent a link to an interview on a specific topic and, after consenting, are greeted by a friendly chatbot which then proceeds with the interview in a chat format. Rather than following a set list of questions, the chatbot will adapt its responses and follow-up questions depending on the respondents’ answers, circling back to link responses and ask for more information as appropriate.

The respondents, who had the level of “Master”[^7] on Amazon’s MTurk service, each completed an interview on this theme without further human intervention. The Amazon workers were given up to 19 minutes to complete the interview and were paid for their time.

We repeated this interview at three different timepoints in September, October and November 2023, inviting approximately N=50[^8] respondents each time. Samples were not matched (respondents were different at each time point).

### Step 2a: Constructing a coding guideline

Once the interviews were completed, a new set of instructions for the AI was written to guide the qualitative causal coding of the interview transcripts. These instructions were generic in the sense that they did not mention, explain or define any specific causal factors (causes, effects, intermediate steps) which might be mentioned in the transcripts.

### Step 2b: Coding the interviews with AI

The final coding instructions were completely human-readable and could have been given to a human assistant - say, a senior undergraduate student of social sciences[^9]. But instead, we gave these instructions to a new AI service within the online app ”Causal Map”, which coded all the transcripts line by line, as described in the appendix, resulting in a long list of all the causal links mentioned in the transcripts, also with the relevant quote for each link.

## Results

### Coding quality

This procedure identified 1024 causal links. 136 out of 163 transcripts contained at least one causal link (the others were blank or contained no causal claims).The mean number of coded causal links for each codable transcript was 7.5.

We gave each causal link identified a 0-2 score on four criteria of precision as detailed in the Appendix. Nearly two-thirds of the links had a perfect score, and only 10% dropped more than 2 of the 8 points. The errors we identified are relatively infrequent and seem to take place approximately at random, except that there were more errors with causal claims which human analysts judged to be difficult to code. The AI found 653 links, which on informal inspection seem to be most of the links actually present.

### Step 3: Auto-clustering and labelling the causal factors

Each link consists of two causal factors or codes: the “cause” and the “effect”. In this study (and in our approach to causal mapping more generally), we consider specific *codes* to be hierarchically nested under more general *themes*[^10]; we call the combination of both theme and code a *(factor)label*, and we construct labels using semicolons in the form “theme; code”[^11]. Counted in this way, the 1024 links identified by this procedure resulted in 532 themes and 1205 separate labels. This diversity was not surprising considering that no codebook was provided. With the approach used, the AI when responding to a coding request has no “memory” of previous requests, and so it is not surprising that it invented a variety of different labels for each specific request, e.g. using more or less interchangeably the themes *Economic conditions* and *Economic issues*. As many of the general themes (and more specific labels) overlapped in this way, the initial causal map as coded by the AI is far too big and messy to interpret. So we carried out an automatic clustering procedure to combine labels of similar meaning: details in the appendix.

The result can be seen in Figure 1.

![[001 Working Papers/img/time-machine-fig-1.png]]

Figure 1: A high-level overview causal map. Causal factors are automatically clustered as described in the Appendix. We used a granularity of 54%. This means that quite large clusters were formed, comprising individual causal factors which although having a lot in common, were relatively heterogeneous in meaning.

Finally, standard filters (details on request) were applied to the resulting dataset of causal claims in order to create overview causal maps as a qualitative summary of the respondents’ ”causal landscapes”: only links mentioned by at least five sources are shown, and then of the factors remaining, only the top ten factors are shown according to source count. This means that many less frequently mentioned factors and links are excluded from the map. Nevertheless nearly all (131 out of 136) sources have contributed at least some citations to this summary map. The numbers on the factors and links (and the sizes of the factors and the widths of the links) represent the number of sources mentioning each. Factors with darker backgrounds have proportionately more incoming than outgoing links: they have greater “outcome-ness[^12]”. The detailed annotation on two of the links shows significant differences between timepoints, see below.

We can see that at this coarse level of “granularity”, many of the factors are themselves bundles of cause-effect stories, as can be seen by the “self-loops” such as the 18 sources who mentioned links between different environment / climate change issues. For example, in the quote “Climate change is brought about by the emission of greenhouse gases” both the cause and effect which were originally coded as “Environmental issues; Emission of greenhouse gases and Environmental issues; Climate change” ended up in the same cluster which has now been re-labelled as “Environment, climate change, energy issues”. Interestingly, although many sources mentioned connections between this factor and other factors, no single link was mentioned by more than five sources so no such connection appears in this map. The same is true for the factor concerning health-care.

At this coarse level of granularity it is mostly not possible to distinguish between constituent factors with different valence or sentiment. For example, “military strengthening” and “military weakening” are two codes which have been included under “International conflict”. Indeed they are not so far from one another in the overall space of embeddings, something which is quite hard to understand from a positivistic, Cartesian point of view but which is perhaps more familiar to those more used to thinking in terms of ”themes” than in terms of “variables”.

Even in the absence of a particular research focus, this causal map has a lot to tell us about the causal worlds of the respondents.

“It’s the economy, stupid”: *economic stress* is mentioned by the largest number of sources and is central to most of the narratives. Economic issues are also frequently causally related to one another, according to the 65 sources contributing to the “self-arrow” above that factor. *Covid-19* appears as a pure driver of economic stress.

Social stress, inequality, migration and immigration is another very central factor which is seen by many as related to *political conflict*.

The reader should not forget that there are many links between factors in this map which were mentioned by five or fewer sources and therefore not shown; and there are very many factors mentioned by 10 or fewer sources which do not appear here at all.

The causal map above only shows a fraction of the data: there is a lot more to explore at different levels of granularity.

### Step 4: Differences between time points

To return to the “time machine” problem, with this kind of data it is quite straightforward to identify differences between timepoints. In this case we had three timepoints (September, October and November 2023). The key is to work with the pooled dataset and construct clusters of causal factors across all timepoints. For example, we can ask whether the number of sources mentioning the factor “economic stress”, or the number of sources mentioning the link from “economic stress” to “personal stress”, differs significantly between timepoints[^13]. Figure 1 shows a parsimonious way of presenting the results of these kinds of statistical tests: only significant results are printed on the corresponding factors or links. In this case, there were no significant differences for factors but there were differences for two links, on the left and the right of the map. The notation on the right (“5 ↗3 4/46”) can be read “five sources, with a significant difference such four of these sources were from timepoint 3, from a total of 46 sources in timepoint 3”: while five sources mentioned the link from *Political conflict* to *International conflict* overall, four (out of five) of them were from just one time-point. This is not surprising considering the situation in Israel/Palestine at the time. The related quote for one of these sources reads “Our government supporting genocide because of our own economic interests in a part of the world we have no business being in. We continue to exploit countries and regions across the world for own [sic] financial gain.” So the “time machine” seems to have successfully picked up a difference between timepoints on a feature which was automatically extracted as emerging from the interviews and was not established at baseline. In this case the causal factors which emerge over just three months would not surprise a time traveller from baseline (timepoint 1); but if this kind of “causal opinion survey” had been carried out with larger samples over, say, ten years we can imagine that factors like “(mis-)trust in vaccinations” or “denial of election results” would indeed emerge which could not have been anticipated at baseline.

The link between *Covid-19, lockdown* and *Economic stress* was more frequently mentioned at timepoints 1 (7 from 41 sources) and 3 (5 from 46 sources), with only 1 source (13-7-5) mentioning it at timepoint 2. This difference is harder to interpret.

## Discussion

### Caveats

#### Ethics, bias and data protection

This kind of AI processing is not suitable for dealing with sensitive information: it is not able to ensure the confidentiality and security of the data collected from the interviewees, since information from the interviews passes to OpenAI’s servers and there are suspicions that this information can “leak” out under special circumstances.

Possible mitigations could include running a suitable LLM on a private server.

Research is always a human endeavour and it is always an *evaluative* decision what tools to use (it is always necessary to explain why these particular tools were chosen). While approaches like these can automate a big part of the research pipeline, that does not mean they are free of bias. The way the AI sees the world, the salient features it identifies, the words it uses to identify them, and its understanding of causation are certainly wrapped up in a hegemonic worldview to an extent to which is very difficult to estimate (Bender et al., 2021). Those groups most likely to be disadvantaged by this hegemonic worldview are approximately the same groups who have least say in how these technologies are developed and employed.

#### Causal mapping

There are some more caveats relevant to causal mapping itself. This kind of method is well suited to revealing “how people think” at scale: what are the kinds of factors they mention and how do they influence one another: it is a method for preparing evidence in order to facilitate causal inferences to be made by the evaluator. It is not a method of causal inference in its own right. Due to the presence of some errors in the coding, questions about individual high-stakes causal links, for example, the effect of Intervention X on another specific causal factor, should certainly be checked by human analysts. And it is not at all suited for estimating the strength of causal effects. It can reveal the strength of the evidence for the influence of X on Y but this is not to be confused with the strength of the effect itself. There can be strong evidence for a weak link and vice versa.

These caveats do not preclude the use of causal mapping for this purpose, as long as researchers are careful with how they interpret the data.

#### Interviewing

There are significant challenges in constructing interview guidelines for automatic interviewing and in interpreting the results. These include the quality and specificity of the prompts, the sensibility of the AI, the complexity and variability of human culture and behaviour, and the kind of ethical and legal concerns regarding data privacy and power (Ferretti, 2023; Ray, 2023) already mentioned above.

There is probably a differential response rate to this kind of interview: some people are less likely to respond to or complete an AI-driven interview than others, and this propensity may not be random, e.g. this automated interviewing procedure may have favoured younger respondents.

Possible mitigations could include further research on these challenges.

There is an indivisible portion of human reality which can never be accessed via a text chat. Automated interviewing is surely never a complete substitute for face-to-face interaction, and we recommend it as a way to scale up interviewing once an initial approach has been established via face-to-face interviewing where at all possible.

#### Autocoding

The work of the AI coder needs to be constantly checked. In particular there is a strong temptation to accept results which are plausible but not accurate, for example, when auto-clustering individual labels may get subsumed into a larger cluster which may seem to add to the salience of the larger cluster even when the individual label does not really fit the cluster at all. This kind of problem may also be familiar to quantitative researchers validating questionnaire subscales (Goertz, 2020).

More thorough validation studies of these AI causal coding techniques are essential.

Although we call our approach “qualitative”, many would disagree. It is not an approach which really nurtures substantive, creative theory-building of the kind expected, for example, when applying grounded theory approaches (Glaser and Strauss, 1967).

The instability of cluster solutions presents a particular problem. Clustering is inherently unstable because as the parameters change, items can reorganise themselves within clusters - just a small change of a parameter can reorganise the clusters quite profoundly at certain points. This does not invalidate the results but can make them harder to understand, summarise and explain.

We should also stress that although this “AI causal mapping pipeline” relieves researchers of a very large percentage of the work previously involved in coding, it is still not a “big red button” which can be pressed without supervision. Although very good results can be achieved with only a minimum of human steering and supervision, nevertheless that steering and supervision is crucial. A single word difference in the instructions given to the AI can result in different techniques being applied, with different results. The evaluator is as always finally responsible both for applying the techniques in a trustworth way and for evaluative conclusions drawn.

### Strengths

**Qualitative approach:** Although the procedures presented here harness AI they remain qualitative in the sense that they approach the stakeholder stories as far as possible without preconceived templates, in order to remain open to emerging and unexpected changes in causal landscapes.

**Scale, reproducibility, low cost:** Most of the pipeline sketched out here can be completely automated which suggests that these methods can include more voices more quickly, and opens up the possibility of including representative samples, something which qualitative researchers have scarcely been able to dream of. Reproducibility opens the possibility of comparing results across groups, places, time points and even languages – important in a time when many of the challenges we are currently facing span languages, places and different populations.

The low cost of coding large amounts of information means that it is possible to develop, compare and discard hypotheses and coding approaches. Previously qualitative researchers have been understandably reluctant to completely discard initial coding approaches or to compare different approaches because of the enormous cost involved.

**Transparency:** When coding the results we do not treat the AI as a black box; we instruct it to follow precise, ordinary-language guidelines, and we can check its work just as we would check the work of a human qualitative interviewer or analyst. Similarly, the labels chosen for the factor clusters can be checked against the content of the clusters, content which includes not only the original labels which are close to the language used by the sources, but also the original quotes identified. Evaluative decisions are left to the humans.

In summary, these new causal mapping procedures have the potential to help evaluators answer key evaluation questions which are often causal in nature, such as: sensing and understanding stakeholders’ causal maps of the systems that surround them; judging whether ”their” theory of change matches ”ours”; investigating what works and how, for different subgroups of stakeholders; tracing impact from mentions of ”our” intervention to outcomes of interest; triaging what are the key outcomes and pathways in the eyes of stakeholders; and many other important evaluation questions.

These procedures can be of value for formative evaluations, as they can identify new and emerging issues to address, and equally for summative evaluations, as they can be used to compare changes in stakeholder views of a system, including changes in outcomes over time.

The kind of pipeline presented here can be automated almost from initial research question to final labelling, which opens up possibilities for monitoring, evaluation and social research which were unimaginable just a year or two ago. As challenging, complex problems like climate change continue to emerge and change, the ability to understand people’s perceptions quickly and without requiring significant resources of time and effort is increasingly important.

In previous centuries, only quantitative research was really able to claim to be able to produce generalisable knowledge about social phenomena validly and at scale, by providing techniques for turning meaning into numbers. Now perhaps qualitative research can eclipse quantitative research by bypassing quantification and dealing with meaning directly, in ways which are somewhat generalisable and can be scaled at will.

Answer to question 1: can an automated interview bot successfully gather causal information at scale?

AI interview bots have considerable potential when it comes to gathering large data sets. When given good guidance AI chatbots are able to conduct adaptive interviews at a scale and pace which would be challenging for human interviewers. Gathering data at this kind of scale in a reproducible and efficient way opens the door for methods like the ‘time machine’ which require large data sets and consistent implementation. With the AI’s ability to communicate in many languages there is the opportunity for reaching more places and people, subject to internet access and the AI’s ability to converse well in less common languages.

Furthermore, researchers should carefully consider whether the subject matter is compatible with this approach. For example, the AI bot may struggle to provide appropriate and convincing support to respondents expressing distress so it is best to avoid highly emotive topics.

Answer to question 2: can automated causal mapping successfully code and synthesise causal information at scale?

The case study presented in this paper suggests that automated causal mapping can code and synthesise causal information at scale. In its current iteration this kind of automated coding involves occasional but significant high-level supervision from researchers. Overall AI can facilitate the process of making sense of large data in much less time, at low costs and in a reproducible way. Furthermore, transparency can be retained by referring to the exact prompt used and by instructing the AI to display the corresponding verbatim *quote* for each and every causal chain.

### Further work

In this paper we have only sketched out the outlines of this kind of approach with a proxy application (“causal opinion polling”). The next step is to apply this kind of approach to gather stakeholders’ views of causal influences affecting outcomes in the lifetime of an actual project and compare how outcomes and the factors which influence them change over time.

Many theoretical and practical challenges remain, from improving the behaviour of the automated interviewer through improving the accuracy of the causal coding process to dealing better with sentiment and valence (for example watching out for cases where both “employment” and “unemployment” are subsumed under a heading like “employment issues”). This kind of approach could also generate alternative, more “story-like” outputs alongside causal maps. Perhaps most urgently needed are ways to better understand and counter the way in which large language models can, whether visibly or invisibly, reproduce hegemonic world views.

## References

Ackermann F and Eden C (2004) Using Causal mapping: individual and group; traditional and new. *Systems modelling: Theory and practice*. Wiley, Chichester: 127–145.

Amazon Inc. (2016) Simplified Masters Qualifications. Available at: https://blog.mturk.com/simplified-masters-qualifications-137d77647d1c (accessed 4 December 2023).

Axelrod R (1976) The Analysis of Cognitive Maps. In: *Structure of Decision : The Cognitive Maps of Political Elites*.

Bender EM, Gebru T, McMillan-Major A, et al. (2021) On the Dangers of Stochastic Parrots: Can Language Models Be Too Big? . In:*Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency*, Virtual Event Canada, 3 March 2021, pp. 610–623. ACM. Available at: https://dl.acm.org/doi/10.1145/3442188.3445922 (accessed 14 November 2023).

Better Evaluation (2021) Qualitative impact assessment protocol | Better Evaluation. Available at: https://www.betterevaluation.org/methods-approaches/approaches/qualitative-impact-assessment-protocol (accessed 20 January 2024).

Blei DM, Ng AY and Jordan MI (2003) Latent dirichlet allocation.*Journal of machine Learning research* 3(Jan): 993–1022.

Braun V and Clarke V (2006) Using thematic analysis in psychology. *Qual. Res. Psychol.* 3(2): 77–101.

Braun V, Clarke V, Boulton E, et al. (2020) The online survey as a qualitative research tool. *International Journal of Social Research Methodology* 00(00). Routledge: 1–14.

Chopra F and Haaland I (2023) Conducting Qualitative Interviews with AI.: 72.

Choudhary S, Chatterjee N and Saha SK (2022) Interpretation of Black Box NLP Models: A Survey. *arXiv preprint arXiv:2203.17081.* Epub ahead of print 31 March 2022.

Copeland AH (1951) *A reasonable social welfare function*. mimeo, 1951. University of Michigan.

Copestake J (2020) Case selection for robust generalisation: lessons from QuIP impact evaluation studies. *Dev. Pract.* : 1–11.

Davies R (2023) Evaluating thematic coding and text summarisation work done by artificial intelligence (LLM). In: *Rick On the Road*. Available at: http://mandenews.blogspot.com/2023/08/evaluating-thematic-coding-and-text.html (accessed 13 October 2023).

Devlin J, Chang M-W, Lee K, et al. (2019) BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. arXiv:1810.04805. arXiv. Available at: http://arxiv.org/abs/1810.04805 (accessed 2 December 2023).

Dunietz J (2018) *Annotating and Automatically Tagging Constructions of Causal Language*. PhD Thesis. Brandeis.

Dunietz J, Levin L and Carbonell J (2017) The BECauSE Corpus 2.0: Annotating Causality and Overlapping Relations. In: *Proceedings of the 11th Linguistic Annotation Workshop*, Valencia, Spain, 2017, pp. 95–104. Association for Computational Linguistics. Available at: http://aclweb.org/anthology/W17-0812 (accessed 14 November 2023).

Eden C, Ackermann F and Cropper S (1992) The Analysis of Cause Maps.*Journal of Management Studies* 29(3): 309–324.

Ferretti S (2023) Hacking by the prompt: Innovative ways to utilize ChatGPT for evaluators. *New Directions for Evaluation*2023(178–179): 73–84.

Glaser BG and Strauss AL (1967) *The Discovery of Grounded Theory: Strategies for Qualitative Research*. Aldine de Gruyter.

Goertz G (2020) *Social Science Concepts and Measurement: New and Completely Revised Edition*. Princeton University Press.

Graham C (2023) Using ChatGPT for foresight: Futures wheel. In: *Medium*. Available at: https://medium.com/&#64;christian.graham 49279/using-chatgpt-for-foresight-futures-wheel-8e79eecfe86b (accessed 2 December 2023).

Hasan MR, Maliha M and Arifuzzaman M (2019) Sentiment analysis with NLP on Twitter data. In: *2019 international conference on computer, communication, chemical, materials and electronic engineering (IC4ME2)*, 2019, pp. 1–4. IEEE. Available at: https://ieeexplore.ieee.org/abstract/document/9036670/ (accessed 2 December 2023).

Hodgkinson GP and Clarkson GP (n.d.) What Have We Learned from Almost 30 Years of Research on Causal Mapping?: 4.

Jang ME and Lukasiewicz T (2023) Consistency Analysis of ChatGPT.*arXiv preprint arXiv:2303.06273* . Epub ahead of print 2023. DOI: https://doi.org/10.48550/arXiv.2303.06273.

Lacey A and Luff D (2001) *Qualitative Data Analysis*. Trent focus Sheffield. Available at: https://www.academia.edu/download/61606002/9 Qualitative Data Analysis Revision 200920191225-129738-301p8i.pdf (accessed 27 February 2024).

Lam TC and Bengo P (2003) A comparison of three retrospective self-reporting methods of measuring change in instructional practice.*The American Journal of Evaluation* 24(1). Elsevier: 65–80.

Laukkanen M and Wang M (2016) *Comparative Causal Mapping: The CMAP3 Method*. Routledge.

Loveridge D and Nyembo A (2021) Decision Support Unit (DSU). Epub ahead of print 2021.

Montrosse-Moorhead B (2023) Evaluation criteria for artificial intelligence. *New Directions for Evaluation* 2023(178–179): 123–134.

Powell S, Copestake J and Remnant F (2023) Causal Mapping for Evaluators. *Evaluation*. Epub ahead of print 2023.

Powell S, Larquemin A, Copestake J, et al. (2023) Does our theory match your theory? Theories of change and causal maps in Ghana. In: Simeone L, Drabble D, Morelli N, et al. (eds) *Strategic Thinking, Design and the Theory of Change. A Framework for Designing Impactful and Transformational Social Interventions*. Edward Elgar.

Ray PP (2023) ChatGPT: A comprehensive review on background, applications, key challenges, bias, ethics, limitations and future scope. *Internet of Things and Cyber-Physical Systems* 3.

Rory Hooper, Nihit Goyal, Kornelis Blok, et al. (2023) A semi-automated approach to policy-relevant evidence synthesis: Combining natural language processing, causal mapping, and graph analytics for public policy. Available at: https://www.researchsquare.com (accessed 14 November 2023).

Shank DB (2016) Using Crowdsourcing Websites for Sociological Research: The Case of Amazon Mechanical Turk. *Am. Sociol.* 47(1): 47–55.

Sia S, Dalmia A and Mielke SJ (2020) Tired of Topic Models? Clusters of Pretrained Word Embeddings Make for Fast and Good Topics too! arXiv:2004.14914. arXiv. Available at: http://arxiv.org/abs/2004.14914 (accessed 26 February 2024).

Yang J, Han SC and Poon J (2022) A survey on extraction of causal relations from natural language text. *Knowledge and Information Systems* 64(5): 1161–1186.

Yoganarasimhan H and Yakovetskaya I (2023) From Feeds to Inboxes: A Comparative Study of Polarization in Facebook and Email News Sharing. *SSRN Electronic Journal*. Epub ahead of print 2023. DOI: 10.2139/ssrn.4666856.

[^1]: Sometimes evaluators think that “causal maps” must be part of some kind of sophisticated causal modelling process, using numerical information to model, predict and make causal inferences about real causal systems. However, causal maps are usually understood simply as informal collections of evidence identified in documents or narratives about how things might influence one another. This information does not on its own warrant causal inferences. But it may form the *basis on which* evaluators or other stakeholders might go on to make their own causal (and other) inferences and conclusions.

[^2]: “The QuIP gathers evidence of a project’s impact through narrative causal statements collected directly from intended project beneficiaries. Respondents are asked to talk about the main changes in their lives over a pre-defined recall period and prompted to share what they perceive to be the main drivers of these changes, and to whom or what they attribute any change - which may well be from multiple sources.”(Better Evaluation, 2021).

[^3]: This kind of procedure can be used at multiple time points. For the sake of simplicity, we will here only refer to baseline and endline.

[^4]: We do not envisage trying to match individual stakeholders across time points.

[^5]: A crowdsourcing marketplace that enables researchers and others to engage remote workers to carry out small tasks online.

[^6]: Previously called StorySurvey

[^7]: Masters are “a specialized group of Workers who consistently demonstrate accuracy in performing a wide range of [tasks]” (Amazon Inc., 2016)

[^8]: The numbers differ slightly each time because the MTurk invitations continued until 50 interviews were completed; however a few respondents broke off the interview before actually completing. Their data was also included.

[^9]: When coding manually for clients in the past, we have usually used human coders with additional training beyond merely being given an instruction like this. We hypothesise that untrained human coders with a social science background produce results similar to that produced in this demonstration project by the AI; trained human coders can produce better results.

[^10]: In our approach to causal mapping, labels can actually have several levels of nesting, for example *Health issues; non-communicable diseases; diabetes*.

[^11]: So that for example we consider *Economic conditions (theme); Rising prices (code) Household stress (theme); Rising prices (code)* to be two separate labels, and we consider *Rising prices* to be two *separate* codes in each instance.

[^12]: The proportion of citations of outgoing links out of all the citations of a particular factor: a normalised version of the Copeland Score (Copeland, 1951). So factors with high *outcomeness* can be thought of as “outcomes”. And factors with low outcomeness can be though of as inputs or drivers.

[^13]: For each link, we calculated a two-way chi-squared test in which the three timepoints form one dimension, the second dimension is mentioning/not mentioning the causal link, and numbers in the cells are numbers of sources; So the table total is the total number of respondents. We used an analogous procedure for testing whether mentions of causal *factors* differed between the timepoints (though in fact none of these tests were significant in the map shown here). This is just an indication of the kinds of tests which could be used; it would for example also be interesting to use ordinal tests (as the time dimension is ordinal). A result is judged to be significant if the p-value is less than 0.05. No correction for multiple comparisons was applied.
