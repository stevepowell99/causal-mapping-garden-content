<div class="user-guide-callout">
<strong>📄 What you can do here:</strong> Choose which source documents (e.g. interviews or reports) from your current project you want to focus on. You can select one or more sources. Use this to narrow your analysis to specific interviews, reports, or other source materials. 
- The text of the selected source is shown below in the Create Links panel.
- Selecting these sources also fetches only their links and no others, starting off the [Links Pipeline](../links-pipeline/): only the links from the currently selected sources are available for further filtering, and are finally shown in the output tabs.
</div>

### Factor label set (global) {#factor-label-set}

Treat **label sets** like **different versions of the same document**: you keep a **default** “main” version (the usual factor labels on each link) and you can spin up **extra named versions** to experiment—try a different coding scheme, run [AI Recode](../simple-ai-recode/) on a copy, or compare schemes—without changing the main story until you choose to. **Most people** finish by **copying one experimental version back into the default** so the map and tables show that version as the “real” one, while the other versions stay in the project if you need them later.

- **Which version am I using?** The **Label set** button sits under the Sources bar and shows the version you are on. Open it for the list of every version in this project; the one you are using has a tick. Pick another to view and edit **that** version’s labels in the [Links Pipeline](../links-pipeline/), map, links table, and link editor. Switching refreshes those outputs so they match.
- **New experimental version:** choose **Duplicate “<name>”** at the bottom of the menu, give it a name, and confirm. The app fills a new column-pair for **every link** with a copy of the version you were on, then switches you to it. Handy before Recode, so the AI writes into the experiment rather than the default. There is no way to make an empty version, and that is on purpose: a version with no labels shows blank for every link.
- **Delete a version:** the bin icon on its row in the menu. The default has none, because it cannot be deleted. Anything stored only in that version goes with it, and a saved view or bookmark that used it will show nothing.
- **Done experimenting — make it “official”:** choose **Promote to default**, which appears only when you are on a non-default version. That copies the version you are on into the **default** columns for every link. Your other named versions are **not** deleted. What the default held before is not kept anywhere, so duplicate it first if you might want it back.
- **What each version is:** the menu shows the name you gave it with a line beside it saying when it was made, which version it was copied from, what wrote it and how many links it covered. A version made before the app recorded that shows its stored name and nothing else.
- **Renaming** a version is not possible yet, though the name is now stored separately from the columns, so it is a small change rather than a rewrite of every link. Duplicate it under the name you want and delete the old one.
- **Temporary Factor Labels** (old filter in the pipeline): **deprecated** for new work—use this control instead; old bookmarks may still reference the filter.

<!--
Technical (implementers): URL state `factorLabelSet` / `fls`. Non-default labels live in `links.metadata.custom_columns` as `cause{suffix}` / `effect{suffix}`; enriched rows expose `l_cause{suffix}` / `l_effect{suffix}`. Top-level `links.cause` / `links.effect` hold the default pair (may be empty when a link was only coded in a suffix). `DataService.applyFactorLabelSetView` runs at the start of `applyAllPipelineFilters`; alternate sets do not fall back to top-level when suffix columns are empty, and it keeps the default pair on each row as the internal `_causeDefault` / `_effectDefault` (underscored so `getCanonicalLinkColumns` treats them as internal; as plain `cause_default` they were read back as a phantom label set). Output cache keys (`_computePipelineHash`) include the active suffix. `copyFactorLabelSet(project, from, to)` with `to === ''` implements Promote. The domain is three layers: `factor-label-sets.js` holds the rules and imports nothing (so `tests/label-sets.test.mjs` can load it in Node), `factor-label-set-ops.js` composes those rules with DataService's queries into create/delete/promote, and the control is the dropdown only and makes no database call. A set is a PAIR: discovery needs both `cause{suffix}` and `effect{suffix}`, so a stray `cause_notes` custom column is not offered as a set. New names fold case (`suffixForNewSet`) while stored suffixes keep theirs, since the suffix is the column name. Names and provenance live in `projects.metadata.factor_label_sets`, keyed by suffix, written inside `copyFactorLabelSet` so every route that makes a set records one; a set with no entry falls back to its suffix. Bulk label-set writes emit `linksUpdated` from the widget after `suppressLinksUpdatedEvent` batch updates. The UI is a standard Bootstrap dropdown (`factor-label-set-control.js`, menu built in `renderMenu`); `DataService.getActiveFactorLabelSuffix` reads the trigger's `data-suffix`, not the URL, because the URL lags its own save throttle. `default` and `_default` are both reserved in `normalizeFactorLabelSuffix`. Open work on this domain, including the naming manifest that would make renaming cheap: `docs/plans/label-sets-audit`.
-->

### Sources Dropdown {#sources-dropdown}

- 👉🏼 **Sources** (multi-select dropdown): pick one or more sources from the current project (typing searches the list).  
- 👉🏼 **Empty selection**: means “all sources”.
- Selected sources appear as pills; when **two or more** are selected, a **pen-to-square** icon appears to the right of the pill for whichever source is currently open in the Source Text Viewer (not shown when only one source is selected).

**Default behavior when switching projects:**
- When you load a project via the **Project Dropdown** or **Projects Panel**, and nothing else specifies which sources to load, the app auto-selects the **first source** so the Source Text Viewer shows something immediately.
- When loading from a **URL/bookmark**, we do **not** change the sources selection. An empty Sources selection means **all sources** (by design).
- Source loading/viewing behavior is the same for **coded and uncoded** sources (having 0 links must not block selector state, text loading, or source navigation).
<!-->
- Ordering: alphabetically by source title (with any leading "Source " stripped),
  falling back to ID when title is missing. Next/Previous navigation uses the same order.
 
- Opening behavior: if a source is currently selected, opening the dropdown will
   start at the next source after the current one (wrap-around at end). If no
   source is selected (empty dropdown), it starts at the first source.

- The dropdown does not auto-open when sources are updated; it only opens on
   explicit user interaction (click/focus).

-->   

### Source Groups sub-panel{#source-groups-sub-panel}


<div class="user-guide-callout">
<strong><i class="fas fa-layer-group"></i> What this does:</strong> Filter your analysis by participant demographics or document characteristics, using the [custom columns](../custom-columns/) you have defined for your project. For example, show only responses from "women aged 25-35" or interviews from "urban areas." Perfect for comparing how different groups see causal relationships. 
</div>


**Controls**:  
- 👉🏼 **Field** (dropdown): choose which source metadata/custom column to group by (includes built-in fields like title/projectname).  
- 👉🏼 **Value** (multi-select dropdown): choose one or more values (list is filtered by Field).  
- 👉🏼 **Random N** (buttons): load a deterministic random sample of sources from the whole project (e.g. Random 5 / 10 / 20).  
- 👉🏼 **Random N / Group** (buttons): after choosing Field, load up to N deterministic random sources per value of that Field.  
- 👉🏼 **Clear** (button): reset the Source Groups selector.

The sampling buttons make a random selection, but deterministically, so the same sources are chosen again if you click the same button again.

The second, "Value" dropdown is filtered to show only valid values for the selected field. Previous/next buttons cycle through values of the selected group. 

The effect is to retain only links where the selected custom column has the selected values.

This dropdown is  NOT a filter and it does NOT get saved/restored in URL. It is a loader: when we click it, the app automatically loads corresponding sources into the sources selector. These sources then DO form part of the links pipeline and ARE restored from the URL.

There is a similar filter in the [Analysis Filters](../filter-link-tab/).