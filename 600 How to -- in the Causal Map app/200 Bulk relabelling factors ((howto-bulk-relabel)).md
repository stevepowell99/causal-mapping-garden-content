---
date: 2026-04-28
---

Sooner or later, every project ends up with a pile of slightly different factor labels for the same idea: `feels frustrated`, `feeling frustrated`, `frustration`, `gets frustrated`. This page covers the four ways to clean that up in bulk, when to reach for which, and how to use the same tools to convert flat labels into hierarchical ones.

The page assumes you've already coded something. If you haven't, start with [[100 Manually code your first project ((howto-manual-code))|manually code your first project]].

## Watch first

<iframe width="100%" height="420" src="https://www.youtube.com/embed/zuQfFoqvBNA?list=PLSCKdSxlLlfGfcab5njcT57xzU0hOURc-" title="Factors table: Search and Replace" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="100%" height="420" src="https://www.youtube.com/embed/a-LK4va6ca4?list=PLSCKdSxlLlfGfcab5njcT57xzU0hOURc-" title="Factors table: Bulk edit" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

The two videos cover the two manual routes (search/replace and Bulk Edit). For the AI-assisted routes, see [[905 Different kinds of coding and recoding ((kinds))|different kinds of coding and recoding]] and the soft recode page.

## The four routes

Four ways to relabel factors, in rough order from "most precise" to "most aggressive":

- **Search/replace** in the Factors table. Find a substring, preview the change, tick the rows you actually want changed, hit Replace. Best for "fix one mistake everywhere".
- **Bulk Edit** in the Factors table. Switch the table body for a multi-cursor text editor and edit many labels at once. Best for "tidy up dozens of variants in one sitting".
- **AI-assisted Recode** (Links recoding or Factors recoding). Send labels to the AI with an instruction (e.g. "merge anything about anger or frustration into `feels frustrated`"), apply to all currently filtered rows. Best for "I've got hundreds of labels and I want a smaller, cleaner codebook".
- **Soft Recode** (magnetic labels). The cheapest option: define a small set of target labels and the app pulls similar labels towards them by embedding similarity, on the fly, without changing your underlying data. Best for "I want to see what a tidied version would look like, without committing".

The decision tree across all of these is in [[905 Different kinds of coding and recoding ((kinds))|different kinds of coding and recoding]]. This page focuses on the first two (manual) routes; the AI ones get their own page.

## Search/replace in the Factors table

This is the workhorse. Open the **Factors panel** and look near the top of the table for the search box. Type a substring; the table filters to matching rows and a Replace box appears next to it. Type the new text in the Replace box; the table updates to show a preview of what each label would become.

Tick the rows you actually want changed (or tick the header checkbox to select all visible matches), then press **Replace**. The Cause and Effect labels in those links are updated everywhere they appear.

A few things worth knowing:

- The search is **case sensitive**. `Calm` won't match `calm`. If you've coded inconsistently, search for each variant in turn.
- It only changes labels in **the currently selected links**. If you've filtered or restricted the source set, factors that only appear outside that selection won't be touched.
- If the matches don't fit on one page of the table, either treat each page separately or bump the **Page Size** selector at the bottom.
- An empty Replace box deletes the search text from each label, which is useful for stripping prefixes (`Improved health` → `health` by replacing `Improved ` with empty).

The full reference is in [[140 Factors Panel ((factors-panel))|the Factors panel page]].

The same search/replace also exists on the **Links table** (see [[150 Links Panel ((links-panel))|Links panel]]). Use the Links table when you want to find a substring in the **Quote** column or in custom link fields, not just in cause/effect labels.

## Bulk Edit: edit dozens of labels at once

Search/replace handles "fix this one variant"; Bulk Edit handles "fix everything I can see in front of me". Toggle **Bulk Edit** at the top of the Factors table. The table body becomes a multi-cursor text editor (Ace), one factor label per line, in the same order as the table. The header stays put for sorting and filtering.

What this gets you:

- **Multi-cursor**: Alt+click to add cursors anywhere; Ctrl+Shift+L to select every occurrence of the currently selected text. Very fast for "add `Feelings; ` to the start of these eight labels".
- **Find next**: Ctrl+Alt+Right adds the next occurrence of the selection to the cursor set; Ctrl+Alt+Left goes back.
- **Side info**: the right-hand column shows source and citation counts, plus the list of sources, for the label your cursor is on.

Two practical tricks:

- **Merge several factors into one**: just overwrite the rows you want to merge with the same target label. When you save, every link pointing at any of those old labels will point at the new one instead. There's no separate "merge" step.
- **Sort first, then edit**: sort by citation count to put the heavy hitters at the top, or sort alphabetically to bring near-duplicates next to each other. The bulk editor refreshes when you sort, so do all your sorting before you start typing.

Three things to watch for:

- **Pagination**: the editor shows the current page only (default 10 rows). For large clean-ups, increase the page size first.
- **Recoded labels are read-only** (shown with a yellow background). They've been generated by an AI recode and the app protects them from accidental edits. Edit the original cause/effect columns instead, or clear the recoded values first.
- **Label-transforming filters**: if you have Soft Recode, Zoom, Collapse, or Combine Opposites running in the filter pipeline, the Factors table is showing transformed labels, but Bulk Edit saves by exact label text match. Turn those filters off before bulk editing, or you'll be confused when nothing changes.

**Soft Recode** is a good example of a temporary label transform.

## Worked example: tidy up Mark's project

Suppose you've coded both interviews in `example-short-uncoded` and your Factors table looks something like this (made-up, but realistic for a small manual coding session that crossed a few sittings):

- `quiet hands-on time`
- `Quiet hands-on time`
- `feels calm`
- `Feels Calm`
- `calmer`
- `feels frustrated`
- `feeling frustrated`
- `gets frustrated`
- `house mess`
- `mess at home`
- `kids demanding attention`
- `kids demanding`

Three small clean-ups:

**Fix the capitalisation drift.** Search for `Feels Calm`, replace with `feels calm`, hit Replace. Same for `Quiet hands-on time` → `quiet hands-on time`. Two presses, done.

**Merge the `frustrated` family.** Switch on Bulk Edit, sort by label so the three frustration variants are adjacent, overwrite all three rows with `feels frustrated`, Save. Three labels become one; all the links repoint automatically.

**Decide what to do with `mess at home` vs `house mess`.** This is a judgement call. Either pick one (search/replace), or recognise that they actually capture slightly different things (general clutter vs the specific moment) and leave them alone. Bulk relabelling is not a licence to flatten distinctions you wanted to keep.

After all that, the map gets noticeably simpler without losing any evidence: the same quotes are still attached to the same links, just with cleaner labels.

## Converting flat labels into hierarchical ones

This is the same tooling, used differently. Suppose all of Mark's emotion labels are flat: `feels calm`, `feels frustrated`, `feels guilty`. You want them under one parent so you can zoom out to a single `Feelings` node.

Two ways:

- **Search/replace**: search for `feels `, replace with `Feelings; `. Tick all three rows, Replace. Now you have `Feelings; calm`, `Feelings; frustrated`, `Feelings; guilty`. Zoom to level 1 in the map shows them all as one node.
- **Bulk Edit**: switch on Bulk Edit, select the three rows, use multi-cursor (Ctrl+Shift+L on the word `feels`) to add the `Feelings; ` prefix in one keystroke pattern. Slightly faster if you're already in the editor.

You can convert the other direction too (drop the prefix to flatten), and you can build deeper hierarchies the same way (`Feelings; negative; frustrated`). The semicolon convention and what it licenses is in [[590 Hierarchical coding ((zoom-filter))|hierarchical coding]].

## When to recode into temporary columns instead

Anything in this page is **destructive**: once you replace `feels frustrated` with `Feelings; frustrated`, the original is gone (the links table no longer has it). For most clean-ups that's fine; you wanted the change.

If you want to **try a relabelling without committing**, do it into a temporary cause/effect column instead. Set a Label set with a suffix (e.g. `_v2`), recode into that, and use the temporary labels in your maps and tables. You can throw the temporary set away if it doesn't work out. Details in [[500 Recoding labels temporarily ((howto-recode-temp))|recoding labels temporarily]].

## Other places you can do this

The Factors panel is the obvious place, but you can also:

- **Edit a single label in the Map**: click the factor, edit. Useful for a one-off rename.
- **Edit in the Link Editor**: open any link that uses the label, retype the cause or effect. The change applies to that link only unless you choose otherwise.
- **Edit in the Links table**: search/replace works in the Cause and Effect columns there too, and you can also search the Quote column, which the Factors table can't do.

When in doubt, do the rename in the Factors panel: it's the most predictable, and the preview shows you exactly what's about to change before you commit.

## See also

- [[050 Example views (example-original) ((howto-example-original-views))|Example views]] for saved bookmarks illustrating filters and recoding.
- [[905 Different kinds of coding and recoding ((kinds))|Different kinds of coding and recoding]] for the wider decision tree, including AI-assisted routes.
- [[500 Recoding labels temporarily ((howto-recode-temp))|Recoding labels temporarily]] when you'd rather experiment without overwriting.

<!--
Internal reference only: tidied transcripts of the embedded videos. Hidden from the published page.

## Transcript: video 15, "Factors table: Search and Replace"

**0:03** Hi. In this little video we're going to look at the Factors table in the Causal Map app. The Factors table, like the Links table and the other tables, responds to whatever filters you've got set in your filter column. So in this case you can see that we're focused on `farm production` and links coming into and out of it. The Factors table will respond to that and show just those same factors as you could see on the map. If you switch that filter off, the display changes, and you see there are now 277 different factors in this list.

**0:50** They're ordered in this table according to citation count, with the most often cited factors at the top. But you can change that. All of these tables you can sort and filter just the way you want. In fact, 15 sources mentioned all of these factors, 14 sources mentioned these, and so on. You can see the citation count and the source count aren't the same: quite often you'll get a factor mentioned by not so many sources, but those sources mentioned that factor a lot. That's why we have two different counts.

**1:36** We also have what we call citation-count-in (also known as in-degree), which is the number of times this factor was mentioned as the effect of something (the arrows coming into it). And here it's the opposite, the out-degree: the number of times a link leaves this factor. So in this case you can see that `improved health` is mentioned very often as the effect and not so often as the cause. We also have a special metric called outcomeness: how much like an outcome is it? It's very high here because it's mostly mentioned as the effect.

**2:22** There's other interesting columns here too. You can move the columns around, sort by them, and most importantly you can filter the factor labels. So you're saying I'm only interested in something to do with farming. Here are all the factors where the word `farm` is mentioned anywhere. And as usual you can choose how many factors to see at a time; if you've got only 10, you'll be clicking through to subsequent pages.

**3:08** There's a few other special features. There's the breakdown box, which lets us break out the columns by different groups within the sources, for example young and old, or gender, or village. There's another little video about that.

**3:24** There's also Search and Replace, which is quite important. Supposing I want to search for any factors which mention `xx`, because somebody somewhere has put an `xx` in here which shouldn't be there. I want to get rid of all the xxs and replace them with, for example, nothing. If I put the search text as `xx` and the replace text as nothing, you can see it gives a preview of what it's going to look like afterwards. This is a very simple example; you can imagine it's pretty powerful. Remembering of course that this is also conditional on any filters you might have, so you can apply filters to get just those factors that you want to apply a search and replace to.

**4:23** Now, I'm going to do the beginner's mistake, which is to press Replace. That won't work because there's no rows selected; I need to select some rows with the checkboxes first. The reason for the checkboxes is you might say "I want to make this change for some of the labels but not all of them". In this case I want all of them, so I select all, press Replace, it asks me to confirm, and the xxs are removed from the labels for those three factors. If we try to search for `xx` again, there aren't any. It seems quite simple but it's quite powerful.

**5:25** There's also an even more powerful thing called Bulk Edit, which we'll look at in a different video.

**5:33** Finally, I forgot to mention: these checkboxes can be used for other things too. You can select multiple factors and then delete them, or merge them. Irrespective of the checkboxes, you can also download an Excel sheet or take a screenshot of just what you can see. You can also press the Edit button to directly change the label, if you've got a typo or a different idea.

## Transcript: video 16, "Factors table: Bulk edit"

**0:02** Hi. If you've done a lot of causal coding, especially manually, you might find you've got a complicated list of different factor labels and maybe you're happy with some of them and not so happy with others. In this case, this is a copy of our favourite file `example original`, and you can see there's lots of different labels in it.

**0:36** We need to do some kind of high-level restructuring, perhaps using hierarchical labels (semicolons to distinguish higher and lower-level concepts). Or maybe we just need to systematically clean up: perhaps we've done it collaboratively and one coder has used American spelling and another UK spelling. The problem is you need to do a kind of bulk refactoring of the factor labels.

**1:08** There's another video that shows how you can use the search/replace box, which is pretty powerful. But sometimes you just want to see all of your labels and go through the whole lot and tidy them up, do a massive spring clean.

**1:28** There's a very small button here on the Factors table which doesn't look like much, but what it does is it shows you a view of the same information as the Factors table: there's 10 factors here just the same as there were 10 factors before, but you just see the labels and you can edit them directly. Which is pretty amazing.

**1:52** But you've got to remember that it responds just exactly to whatever table-like settings you've got. So if you're viewing 10 at a time you'll see the first 10, then the next 10, and so on. Or you can just change the page size. In this case there's about 300 factor labels, so if you switch it to 1000 you can see all of the labels at once. It's very important to understand that any changes you make only apply to the factors you can see in front of you on the screen. Otherwise these labels respond just the same way as the table does. So if I sort by factor label alphabetically, they're alphabetically organised.

**2:49** And you might think, "Aha, this is useful because I might have a nice system going in my top-level labels here but I'm not sure about what's going on down here, and I might want to change some things, reorganise the levels of the hierarchy." That's what I can do with this editor.

**3:11** Very simply, I could change `bank D` to `bank X`, for example. So I change using this text editor just what I want, I save changes, and that label will be changed. It says "you're about to rename one factor, two links mention this factor, changing `bank D` to `bank X`". I can say yes or cancel.

**3:45** There's a lot more you can do because it's a sophisticated text editor. You can do things like multiple cursors. So if I press Ctrl and the down arrow, you see how I can select multiple things at once. I can say instead of `agricultural production`, I might change this to `farm production` by using these multiple cursors. There's a blue box here giving you a lot of detail about the different shortcuts for using this powerful text editor.

**4:22** A different thing you can do (let me press Ctrl+Z to undo): supposing I think "what else is there to do with agriculture around here?" I select a piece of text, then Ctrl+Alt+right-arrow, and you see it's selecting all the different instances where `agriculture` or `agricultural` have been mentioned. That's multiple cursors, so I can start to type. It's not going to quite work in this case because 