---
date: 2026-04-28
---

This page walks you through manually coding the practice project that every new user gets, called `example-short-uncoded`. The aim is to take you from "I just signed up" to "I have a small map I made myself", in around twenty minutes. If you'd rather have the AI code it for you, see the AI coding walk-through (separate page); if you want to know why we code the way we do, see [[0.001 Task 2 -- Introduction ((task2-intro))|Task 2 introduction]].

## Watch first

<iframe width="100%" height="420" src="https://www.youtube.com/embed/vf96cvLB7qQ?list=PLSCKdSxlLlfGfcab5njcT57xzU0hOURc-" title="Manual coding in cm4: first steps" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

A short video tour is often quicker than reading. The video above ("Manual coding in cm4: first steps") covers the same workflow as the rest of this page. The full playlist of [Causal Map 4 tutorial videos](https://www.youtube.com/playlist?list=PLSCKdSxlLlfGfcab5njcT57xzU0hOURc-) covers everything else. The written walk-through below uses the first interview in `example-short-uncoded`, where Mark talks about his day-to-day feelings.

## Open the example project

When you sign up, the app creates a personal copy of a practice project for you. 

1. In the **Project Dropdown** at top left, choose `example-short-uncoded-[your-username]`.
2. The Sources bar will fill with two short interview extracts.
3. In the Sources bar, click source `1`.

The text of source 1 (Mark's interview) appears in the **Source Text Viewer**. The right-hand side shows an empty Map panel. That's your starting point.

## Read before you code

Read the whole of source 1 once, without coding anything. You're looking for places where Mark says or implies that one thing influences another, even loosely. Notice how often a single sentence contains a chain (A made B happen, which then led to C). That's normal in real speech, and it's why a single quote often becomes two or three separate links.

While you read, ignore everything that isn't a causal claim, including descriptions of facts, opinions about whether something is good or bad, and questions from the interviewer. Causal mapping codes only **bare causation**: someone saying or implying X influences Y. The reasons for this minimalist stance are in [[010 Our approach is minimalist -- we code only bare causation ((minimalist-bare-causation))|why we code only bare causation]].

## Code your first link

A clear causal claim from Mark, about what calms him down at the end of a long day:

> a bit of quiet time. After they're in bed. Just to like, mess around with something. My old soldering iron. Or trying to fix that radio. Something hands-on... That calms me down.

The quiet hands-on time causes him to feel calm. Code it like this:

1. With your mouse, **highlight** the passage in the Source Text Viewer, from "a bit of quiet time" to "That calms me down". Stay within one statement; don't drag across paragraph breaks.
2. The **Link Editor** opens. Your highlight appears in the Quote box at the bottom; you don't normally need to touch it.
3. In the **Cause** box, type a short label, `quiet hands-on time`. Press Enter to commit.
4. In the **Effect** box, type `feels calm`. Press Enter.
5. Press **Save**.

A new link appears in the Map panel on the right. The phrase you highlighted is now coloured in the source text. Click it again at any time to reopen the link for editing.

That's the whole loop: highlight, name cause, name effect, save. Everything else is variation on this.

For the full reference on the editor (chain mode, plain coding, multi-cause and multi-effect, custom fields), see [[090 Create Links tab ((create-link-tab))|Create Links tab]].

## Naming factors well

Factor labels do most of the work in causal mapping. A few principles:

- **Reuse existing labels** when you can. After you've coded a few links, the dropdowns will start suggesting labels you've already used; pick from the list rather than re-typing, so the same idea ends up under one name.
- **Be specific, not abstract.** `Increased household income` works better than `Economic improvement`. See [[610 Factor labels -- do not over-generalise ((labels-no-overgeneralise))|don't over-generalise]].
- **Make the direction implicit.** Labels like `Lost job`, `Sold cow`, `More food` already point in a direction; the link itself just says "this caused that". This is what we mean by [[580 Factor labels -- semi-quantitative formulations can help ((labels-semi-quant))|semi-quantitative labels]].
- **Don't worry about consistency on the first pass.** You'll tidy labels up later, in bulk, using search/replace and bulk relabel; that's a separate page.

The wider craft of writing factor labels is covered in [[220 Factor labels -- a creative challenge ((labels-creative))|factor labels: a creative challenge]].

## Several causes, several effects

Often a single quote supports more than one link. The Link Editor handles this without forcing you to repeat yourself.

Type two or more causes into the Cause box (separated by Enter), and likewise for effects. When you press Save, the app creates one link for every cause-effect combination. Two causes and two effects means four links, sharing the same quote.

Mark gives a clear example when he describes coming home to chaos:

> Sarah's late back, I've had a long day on-site, and you walk in and it's like... toys everywhere. Half-eaten cereal. Laundry mountain. And the kids are immediately like, "Dad, I'm hungry!" or "Dad, my show!"... That's when I just get... so frustrated.

Several causes, one effect. Highlight the passage and:

- in **Cause**, type `house mess`, then `Sarah late home`, then `kids demanding attention` (Enter between each)
- in **Effect**, type `feels frustrated`
- press **Save**.

The app creates three links, one for each cause, all sharing the same quote and the same effect. Use this when the speaker names several drivers, or several outcomes, in one breath. Don't use it as a shortcut for unrelated claims; if two causal statements are really separate, code them separately.

A bit further on, Mark tells you what happens next:

> And then I snap. Just say something sharp. To the kids. Or to Sarah, if she's just walked in. And then, instantly, it's like, "Why did I say that?" That guilt.

That's a chain: frustrated leads to snapping, snapping leads to guilt. Code it as two links sharing the same quote: `feels frustrated` to `snaps at family`, then `snaps at family` to `feels guilty`. (If you turn on **Chain mode** in the Link Editor, the Effect of the link you just saved becomes the Cause of the next one, which saves a bit of typing.)

For more on chain mode, multi-cause/effect, and using the Links tab to review your work, see the next video in the playlist:

<iframe width="100%" height="420" src="https://www.youtube.com/embed/2wZEsiq4gpA?list=PLSCKdSxlLlfGfcab5njcT57xzU0hOURc-" title="Manual coding in cm4: advanced tricks and Links tab" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Adding metadata as you go

Most of the time you can ignore the rest of the editor and come back to it later. Three small things are worth knowing about now:

- **Tags.** Quick free-text labels, useful for "come back and review this", "respondent unsure", "future hypothesis", and similar. Tags starting with `?` mark caveats (`?hypothetical`, `?doubtful`); see the tag conventions in the [[090 Create Links tab ((create-link-tab))|Create Links tab]] reference.
- **Sentiment.** A simple `+1`, `0`, `-1` per link, used when a claim is about an increase, no change, or a decrease in the effect. Mark's `quiet hands-on time` to `feels calm` is positive; `house mess` to `feels frustrated` is negative. Details in [[720 Link metadata -- Sentiment ((metadata-sentiment))|sentiment metadata]].
- **Custom fields.** Project-specific structured fields, for example `mechanism` or `confidence`. You don't need these on day one; if you do, see [[410 Adding and using custom columns for your links ((howto-custom-columns))|adding custom columns]].

You can also add metadata in bulk later, in the Links panel, so don't slow yourself down adding it as you code.

## Hierarchy and tags inside labels

Two label conventions become useful as the project grows. They're worth noting now even if you don't use them on the first pass.

- A label containing a semicolon is treated as **hierarchical**: `Family life; Quiet time` is read as "Quiet time under Family life". This lets you zoom out to a coarser map without losing detail. See [[590 Hierarchical coding ((zoom-filter))|hierarchical coding]].
- You can also embed metadata in the label itself, for example `feels calm #positive` or `feels guilty (Outcome)`. Useful when you don't yet want a full custom column. See [[300 Factor label tags -- coding factor metadata within its label ((label-tags))|tags inside factor labels]].

If you're not sure, code flat first. You can convert flat labels to hierarchical ones in bulk later (see the bulk relabel page when it's written).

## Move through the sources

When you've coded everything in source 1 that looks worth coding, click the right arrow in the Source Text header to move to source 2. The map will start to grow as the same labels appear across multiple sources. That's where causal mapping starts to pay off: the same factor named by several speakers gets a thicker presence on the map.

## Look at your map

Switch your attention to the **Map panel** on the right.

- Click any edge to see the underlying quote.
- Click any factor to focus on links that touch it.
- The **Map Formatting** controls let you change colour, width, and labels (we have a separate how-to on map formatting).

If the map looks crowded after just a few sources, that's expected. The Filter Links panel exists exactly to manage that, starting with a top-N frequency filter. The full picture of which filters do most of the work is in [[000 Tasks 2 & 3 --  Extensions -- Introduction ((extensions))|the extensions chapter]].

On a larger real project, **factor-frequency** and **link-frequency** filters are the usual first step. The anonymised `example-original` tutorial project shows the idea at scale — e.g. bookmark [#266](https://app.causalmap.app/?bookmark=266) (map) and [#1124](https://app.causalmap.app/?bookmark=1124) (link-frequency style):

![Factor-frequency style map — example-original (bookmark #266)](img/bookmarks-example-original/screenshot-top-factors-map.png)

![Link-frequency style view — example-original (bookmark #1124)](img/bookmarks-example-original/screenshot-link-frequency-top-links.png)

## Tidy up afterwards, not during

Resist the urge to consolidate labels as you code. It slows you down and you'll often regret early decisions once you see the whole project. Code messy, tidy in bulk:

- Use search/replace in the Factors and Links tabs to rename labels project-wide.
- Use Bulk Relabel in the Factors panel to merge or split labels.
- Use the temporary cause/effect columns if you want to experiment without overwriting the originals: see [[500 Recoding labels temporarily ((howto-recode-temp))|recoding labels temporarily]].

The full decision tree for cleaning up labels (and where AI-assisted recoding fits) is in [[905 Different kinds of coding and recoding ((kinds))|different kinds of coding and recoding]].

## When you're done

Save a bookmark of your map (Bookmarks button, top right) so you can come back to this exact view. From there, the natural next steps are:

- explore the Filter Links panel to ask questions of your map
- read [[905 Different kinds of coding and recoding ((kinds))|different kinds of coding and recoding]] to see what the AI can take off your hands
- and, when you outgrow the example project, read about [[000 Task 1 -- Introduction ((task1-intro))|gathering your own data]].
- browse [[050 Example views (example-original) ((howto-example-original-views))|saved example views]] from the public `example-original` project for inspiration.

<!--
Internal reference only: tidied transcripts of the embedded videos. Hidden from the published page.

## Transcript: video 6, "Manual coding in cm4: first steps"

**0:01** Right. So we've uploaded some source texts into the app and now we want to code them. That means identifying causal claims and highlighting them. Here it says "my personal health and hygiene was not of the best because we didn't have good practice of hygiene." So I'm going to highlight that, and here the quote appears: that text which I selected, which is the evidence for the causal claim. And I put here something like `poor personal hygiene`.

**0:32** That text hasn't been used before, so I'm going to create it as a new factor label. If there had been the same or a similar text before, it would have appeared as a suggested factor label which I could have selected; but here there isn't one.

**0:47** So the effect: we'll just say `for personal health`, which again is new. So I just click to select it. There's other things I can do here, but that's basically it. So I click Save, and that will create the causal link. And you'll see then that the text is highlighted here, and over here, the link has been created on the map.

## Transcript: video 7, "Manual coding in cm4: advanced tricks and Links tab"

**0:01** Let's do one that's a bit more advanced. You can see here we've created a causal link. It's also possible to edit that link, either by clicking on the link itself or by clicking on the highlight; same thing.

**0:23** If I want to edit the link, I might, for example, change the factor label. It actually says `poor personal hygiene and health`, which doesn't really make sense, but that's what the person said. So I can edit the labels like that.

**0:39** Or maybe I think this is really interesting and I want to come back to it. So I'm going to mark it with this exclamation mark, "remember to come back to it later". It'll be easy then to find in the table of links. Or I can create a tag like `doubtful`, which does something like the same thing. You can create your own tags as you go along, because you maybe want to exclude or include this particular kind of link later.

**1:06** It's also possible to say I'm very interested in the sentiment of this claim, that this is a bad effect, so I'm going to put that as something with a negative sentiment rather than a positive sentiment. A lot of people don't use this, but it's usable. We use it a lot in the AI coding. And when I save, it saves the link, making the update I just made.

**1:28** Sometimes you have not only more than one causal claim, but overlapping causal claims. So arguably somebody could say that this whole paragraph is an argument about improved overall health and hygiene because of organisation X. So we can say `improved health` because of the intervention of organisation X. Let's say that the whole paragraph kind of sums that up.

**2:15** I'm going to save that here. You see that not only can you see the original claim, but you can see this much broader claim highlighted with a whole paragraph. If you now click on part of this because you want to edit it, in the right situation it gives you the correct claim to edit. Click on this one and it gives me the whole piece of text. Click here, it gives me just that specific piece of text. Sometimes if they're really overlapping, it'll give me a choice which link I want to edit.

**2:55** All of this editing, which you can do here, can also be done from the map, as we've seen, and you can do it from the Links table too. Over in the Links table you've got the same links. You notice also that there are tags here which you can look for. We can edit the links by clicking Edit, and the same dialogue appears.
-->
                                                                                                                                                                                                                                                                                                                                                                                        