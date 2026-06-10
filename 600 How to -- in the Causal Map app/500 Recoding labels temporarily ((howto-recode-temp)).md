---
date: 2026-04-28
---

# Recoding labels temporarily

Sometimes you want to improve your factor labels (cause and effect text) without changing the original data. You might want to:

- experiment safely, trying different prompts or AI settings without overwriting what you coded
- iterate, running factor relabelling several times until you're happy
- compare the original and improved labels side by side
- review before committing, only merging into the main labels when you're satisfied

The app supports this with the **Label Set widget** in the toolbar below the Sources bar. Treat label sets like different versions of the same document: one **default** version, plus as many named experimental versions as you want.

## How to use it

1. **Open the Label Set widget** under the Sources bar. Type a new name for your experimental set, for example `v1` or `cleanup`, and confirm. The app fills a new pair of columns (`cause_v1`, `effect_v1`) for every link from what you were just looking at, then switches you to that set.

2. **Edit or recode within the experimental set.** From now on, anything you do (manual edits in the Factors panel or Links table, AI Recode, Answers, search/replace, Bulk Edit) writes to the experimental columns. The default labels stay untouched.

3. **Flip between sets** with the same widget. Pick `default` to see the original labels; pick your experimental set to see the experimental labels. The map and tables refresh to match. Useful for quick before-and-after comparisons.

4. **When you're happy with one experimental set**, open the **⋯** menu in the widget (only visible when a non-default set is selected) and choose **Promote to default**. That copies the current experimental set into the default columns. Your other named versions stay in the project; nothing is lost.

## Summary

Use the Label Set widget to spin up named experimental versions of your labels, work on them without touching the default, switch between versions with one click, and promote the winner to default when you're done.

## See also

- [[905 Different kinds of coding and recoding ((kinds))|Different kinds of coding and recoding]] for the broader picture.
- [[200 Bulk relabelling factors ((howto-bulk-relabel))|Bulk relabelling factors]] for permanent (non-temporary) clean-ups.
- [[300 Translate factor labels ((howto-translate-labels))|Translate factor labels]] for a worked example using a `french` set.
- [[080 Sources Bar ((sourcesHeader))|Sources Bar reference]] for the Label Set widget specification.
