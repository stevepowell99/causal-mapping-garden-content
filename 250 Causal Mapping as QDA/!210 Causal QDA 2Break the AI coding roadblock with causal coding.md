---
date: 2025-04-09
---

> **SOURCE NOTE (consolidation):** This is a draft/fragment. The flagship QDA-facing paper is now: [[040 Causal mapping as causal QDA ((causal-qda))]].  
> Companion methods notes: [[900 Magnetisation ((magnetisation))]]; [[900 A simple measure of the goodness of fit of a causal theory to a text corpus ((goodness-of-fit))]].

# Break the AI coding roadblock with causal coding.

# The fundamental problem of using generative AI to make sense of texts: too much black box, or too much work

In my the first and second posts, I argued:

- A lot of evaluation work involves some kind of text analysis.
- Evaluators, like (qualitative) social scientists in general, need to get ready for what AI means for text analysis.
- It’s great to use AI to break up complex, vague tasks into many smaller steps which can be intersubjectively verified (and which you could have done yourself if you had the time):
    - DO Document your methodology so that you can explain step by step how you reached your conclusions in a way which anyone can check.
    - BUT if you didn’t have a clear workflow from data to judgements *before* AI, DON’T lean on the black box of the AI to cover that up.
- We have to continue to take responsibility for our work.

In this post we’ll extend this argument with one big DO and one big DON’T.

### **DO try causal mapping….**

| **Do** | **Don't** |
| --- | --- |
|  | ***DON’T***   |
|  |  |
|  |  |

# xx

We often see evaluators and other researchers using AI for tasks like "list the main themes in this document" or even "list the main themes in this collection of documents".
To be clear: we've all done it. there are times when it can be a useful time-saver. 
But the trouble with that is 
- it's massively sensitive to what one means by a theme. What

*do you*

mean by "theme"? 
- you can improve your prompt massively simply by narrowing the universe: 
- "Identify the main kinds of relationship issues mentioned"
- The natural conclusion of this narrowing-down is reducing the generation problem to a categorisation problem. Categorisation is probably taking things too far, because you lose the advantage of any kind of identification of unexpected things. 
Wouldn't it be great if you could just have a generic instruction like "make sense of this document already. Just tell me what's going on, but not only as a summary, but also as a report which is to some extent representative of the different contributions from different sources or sections,

*and*

in such a way that it's somehow intersubjectively verifiable ?!?!
There

*is*

such an instruction: it's called causal mapping. 
The chances of two independent coders achieving somewhat similar results are much bigger with this reformulation. This is anecdotal, I don't have a reference for it. 
There are two issues - chunk size and intersubjective verifiability.
Ensemble agreement is the second-loop version of intersubjective verifiability.
Rick D is going to love Workflows

So there's been a lot of talk about using large language models and evaluation and specifically in coding and processing texts here at causal map limited we've been working very hard on just that. And we see fantastic potential. We're already using it and now first projects however, I wanted to draw attention to a really big distinction which I think is important. 

We've got a dimension between on the one hand transparent responsible, reproducible approaches founded in social science and the other end of the spectrum approaches where responsibility is shifted from the evaluator to the AI. And while to be sure that maybe use cases for the latter kind of approach I'd like to set out here reasons why we prefer the former. The kind of approach I want to warn about is where it's possible today. And it's going to get it's possible today in its rudiments and it's going to get a lot more accessible and powerful quite quickly. And that approach is essentially that is most extreme to say to the AI. Here's a load of documentation from a project. You tell me if the project is efficient, effective, sustainable and so forth in other words submitting a long text This is an extreme case, but the basic idea is submitting a long text and asking for a blackbox judgement about what themes are present in particular out causal map limited were well aware it would be possible to it is possible to say to an AI, please read this long document and draw a causal map saying what do you think are the main causal drivers and outcomes and intermediate links and just print it out? As a map? And the job's done but that's exactly the sort of approach we are warning against. Because you have no way of knowing how the model has reached that conclusion. To be sure, it's possible to say to a model Yes and also show your working or print out some quotes or examples to backup your findings. But it's very important to realise that this is pretty spurious because AI at the current state of development has no more insight into its inner workings than does a human being or probably less so. And so while it can competently bullshit about what steps somebody might have taken to reach that conclusion doesn't mean it's actually the steps that it did take. So basically, you have no way of knowing how the AI came up with a particular finding our conclusion using this approach and it's a massive abrogation of responsibility for an evaluator to sign off this kind of output without further analysis, now at the safer end of the spectrum what we recommend is using AI merely to speed up manual coding and make it more reliable and reproducible. So we believe not in submitting a text to a blackbox and asking it to tell a story about how one might have come up with such a conclusion. But to do it the old school way of First of all, highlighting individual sections of text showing how ensuring that coding is done according to explicit rules set by the evaluator and then aggregating and combining those codings and the sort of way that in our field. Causal mapping has been carried out for 50 years or more. As an aside we believe that even before we get into the AI possibilities, causal mapping is a really good way to summarise the implicit programme theory or causal theory expressed within a document obviously, there is more to a document than simply the causal claims it makes, but nevertheless, causal claims are pretty central and the procedure for identifying, extracting and aggregating those claims aka causal mapping are pretty straightforward. Relatively straightforward and give you a massive leg up. In the effort to make meaningful and useful summaries of sets of documents, in particular causal mapping is dedicated to or is particularly good at. Making summaries about sets of from sets of documents, such as semi structured interviews with comparable respondents rather than only the special case of making one summary of just one document so what we do when we use AI to help code a set of documents is we tell it to explicitly identify explicit causal claims within the documents following rules we give it and in each case, it's possible to look at the actual quote it identifies and check if it really is evidence for the causal claim. It's been a lot of work to develop the right set of prompts but in any given case the set of prompts needed for coding. a given set of transcripts will be around about half a page of standard prompts. Which will be pretty much the same across use cases and another half a page or so of prompt which is specific to the use case and which is itself 90% derived in an automated way that these prompts are just plain English. Given the original documents to be processed on these prompts, it would be perfectly possible to set a bunch of postgrads to work following the instructions to do the coding and just the way we asked the AI to do it. There is no black box and no magic and you can follow every step of the argumentation in order to aggregate synthesise and simplify the causal maps which result we can use the many more or less standard causal mapping procedures which have been developed over the years and in particular our open source set of causal mapping functions. So an interested outsider can follow the chain of argument right away from the original text to the final conclusion without ever having to simply trust the AI or abrogate responsibility and that's the biggest issue that's at stake here. Because. At the moment at least, we don't want to have anything to do with we really want to steer clear of a situation where we simply feed data or documentation into a machine and it comes up with its own conclusions in an untransparent way. Because as evaluators we simply cannot sign off on these conclusions. If we don't know where they've come from. That's why we stick to using AI to simply speed up the process which is fully described for the manual case

## Caveats

This circle model of evaluator responsibility is very transactional and doesn’t really fit well with highly participatory models. Sorry for that. 

At Causal Map Ltd, we’ve found that [highlighting and then aggregating causal links](https://www.causalmap.app/resources/causal-mapping-for-evaluators/) is a great and relatively generic path from text data to the brink of evaluative judgement. We’re also working on ways to make workflows accessible. See how we currently use AI in Causal Map [here](https://www.causalmap.app/ai/).

This post is based on my recent contribution to the [NLP-CoP](https://merltech.org/nlp-cop/) Ethics & Governance Working Group, along with colleagues [Niamh Barry](https://www.linkedin.com/in/niamh-barry-mel/), [Elizabeth Long](https://www.linkedin.com/in/elizabethannelong/) and [Grace Lyn Higdon](https://www.linkedin.com/in/gracelynhigdon/). In the next couple of weeks we’ll xxyxxyxyxyx.

*This post was originally published by Steve Powell on LinkedIn and has been republished here. See the original article here*

### German, the language of evaluation

Two untranslatable words essential for evaluation:

(1) Nachvollziehbar. “the way you explained what you did and why you did it was great, I could follow and the hows and the whys, it was very nachvollziehbar, your explanation had great Nachvollziehbarkeit.”  

(2) Konsensfaehig. Likely to garner or attract or achieve consensus, or amenable to having consensus achieved for it. Note the even more exciting heightened version *am konsensfaehigsten:* most likely to garner consensus.