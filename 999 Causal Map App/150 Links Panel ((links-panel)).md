Ideas Garden: [Links Panel](https://garden.causalmap.app/bundles)

<div class="user-guide-callout">
<strong>🔗 What you can do here:</strong> View and manage all your causal links in a spreadsheet-like table. You can sort, filter, and edit individual links, view the quotes like a printed page, or export your data to Excel. Each row shows one causal relationship with its source quote and any additional details you've added. Great for detailed review and bulk editing of your causal map data.
</div>

### Links Table {#links-table}

**Links Table Features:**
- Standard column filters, sorting <i class="fas fa-sort text-muted"></i>, and pagination
- Sentiment column with numeric values (-1 to 1) and blue/white/red conditional formatting (blue = higher, red = lower, white = mid-range relative to the current view)
- **Citation Count** – total number of links in each bundle (cause >> effect pair), with muted green → white conditional formatting (darker green = more links in that bundle relative to the current view)
- **Source Count** – number of different sources contributing links to each bundle, with the same muted green → white conditional formatting
- **AI run** – short id of the `ai_runs` row for links created by [AI coding](../responses-panel/) (hover for full UUID); empty for manual links or older imports
- Checkbox selection for bulk operations
- Edit functionality opens causal overlay for link modification
- Action button to open coding in the Sources pane and scroll to the corresponding highlight <!-- opens textViewer -->
- <i class="fas fa-times"></i> Clear Table Filters option
  - 💡Tip: For label changes, prefer [Factors Search/replace](../factors-search-replace/) when working on labels across bundles.

**Link Editing:**
- Single link click opens editor popup
- Multiple link selection opens chooser interface
- Consistent with coding panel behavior
- **AI run id after manual save:** the link editor uses a split update path:
  - **1 cause × 1 effect:** updates that existing row in place (keeps row id; `ai_run_id` remains unless changed elsewhere).
  - **multi cause/effect (cross-product):** deletes the original row and inserts new rows; those new rows do not carry the original `ai_run_id`.
  The original AI call is still traceable in **Responses**.

#### Link Custom Columns {#link-custom-columns}

Alongside **tags** and **sentiment**, each link can now carry its own named custom fields. Use these when you want more structured information on each causal claim, for example `confidence`, `policy_area`, `mechanism`, `evidence_strength`, `time_horizon`, or a numeric score.

This is also the main place to add QDA-style memos while you code. Create one or more memo columns, for example `link_memo`, `evidence_note`, `interpretive_note`, or `coder_reflection`, and use them to record why you coded a link in a particular way, doubts about the evidence, or analytic notes you want to revisit later.

- Create/remove column names in **Manage Link Table Columns**.
- Show/hide Links table columns in the same modal (checkbox list), or from the header **⋮** menu.
- Create new fields directly from the **Link Editor** custom-fields picker.
- Edit values in the **Link Editor** or directly in the **Links Table**; this works the same way as editing [source custom columns](../custom-columns/), but on link rows instead of source rows.
- Use them elsewhere in the app, for example in the [Everything filter](../everything-filter/), links-table grouping/breakdowns, the [Link Editor screen](../causal-overlay/), and map display via the [Map Custom Columns filter](../map-custom-columns-filter/).

### Links Utilities {#links-controls-row2}

- Download as Excel
- Take a screenshot and copy it to clipboard
- Clear any filters at the top of the table columns
- Bulk delete any selected rows in the table

### Row Grouping and Print View {#links-controls-row1}

- **Group by selector** - Choose one or more columns to group rows by values. This applies both the the links table and Print View.

**Useful Columns:**
- **Bundle** - Shows "cause >> effect" pairs
- **Original Bundle** - If you have used filters which transform the links, like Zoom or Soft Recode, use this to also view the original causes and effects

#### Bulk Tags editor

Toggle **Bulk Tags** to switch the Links table into a line‑by‑line editor for **unique link tags** (one tag per line), sorted alphabetically.

- The list contains **all tags** found in the **current filtered links** (the pipeline output: current Project + Sources selection + Analysis Filters). It does **not** use Links table header filters or pagination.
- While Bulk Tags is on, the Links table (including header filters and pagination controls) is hidden.
- You **cannot** add/remove/reorder lines.
- Edit a line to **rename** that tag; make a line **blank** to **remove** that tag.
- Clicking **Save Changes** applies the rename/remove across **all currently filtered links**.
- Tag matching is **case‑insensitive exact match** (after trimming).


#### Print View <i class="fas fa-quote"></i> {#quotes-widget}

The purpose Print View is to make it easy to explore and read actual quotes from the currently filtered links. What it does is show, instead of the contents of the Tabulator table, a printed version of the same information, leaving the table headers and filters in place. The toggle switches between table contents view and print view. 

This view prints out the quotes from each row in the table, grouped by the Group By columns formatted as nested headings, and we suppress repeated headings until they change. 

We also reveal two more toggles: 

- Show Details: Print the values of all the extra columns such as tags and any [Custom Columns](../custom-columns/)
- Context: for each quote we add an additional three sentences at each side, highlighting the actual quotes. 
- **PDF**: prints the **full** list (not just the current on-screen page) in a new tab. Use **Print** → **Save as PDF**. The export uses slightly **smaller** body type. Each **group** from **Group by** is a separate table so the **group title repeats at the top of each printed sheet** when one group spans many pages. The new tab’s **title** (and the usual default **Save as PDF** name in **Chrome** / **Edge**) is `CausalMap-Links-<project>-<YYYY-MM-DD-HHmm>`. In **Chrome 131+** and current **Edge**, the **bottom page margin** lists the **current project name**, **date/time**, `Causal Map | causalmap.app`, and **page _i_ / _n_**. If the system print dialog also adds its own header/footer, turn that off there to avoid duplicates.

You can manually sort the texts using to the sorting widgets in the tabulator headers, as far as allowed by the nested headers.

### Search/replace {#links-search-replace}


This works exactly the same as [search/replace in the factors table](../factors-search-replace/), except that it works on the Cause label and/or the Effect label.

Near the top is a row containing a search box. If you type something into it, 
- a replace box and a Replace button also appear. 
- the table is filtered to show only matching rows.

The search is **case sensitive**.

You can then alter what you see in the Replace box:
- in the label columns in the table, you see a preview of what the affected rows text so the would look like; 
- if you delete all the replace text so it is empty, the preview shows the effect of deleting the search text from each label. 

Then when you are satisfied, check all the checkboxes where you want to update the labels as shown. If you want, select all rows using the checkbox at the top of the column. Note, if there are more hits than fit on this page of your table, you'll want to either treat each page separately or increase the page size with the Page Size selector. 

Finally, hit the Replace button to actually update the labels as shown in the rows you selected. As you'd expect, this search/replace only affects the factors for the currently selected links: for example if you have only selected the first three sources, this update will not affect the links in the other sources.


 <!--
Below the grouping controls row is a row containing a search textinput and a replace textinput and a Replace btn. 
Every time search field is updated, update the replace field to match. But obviously then allow manual changes to the replace field.

This works exactly the same as search/replace in the factors table, so we can maybe wrap and reuse that code, EXCEPT if search is non-empty, first filter the table to show only rows matching the search text in **Cause OR Effect** column, then do a fake preview search-replace on those two columns in the table just before display (don't really replace text yet). (If replace is empty, preview deleting the search text from each label.) 

Then when user hits Replace, only the checkbox-selected rows (across all pages) are processed; unselected rows are ignored. A confirmation modal shows the total number of replacements, then the replacements are applied in the Cause and Effect fields to_label/from_label in DB , then the view refreshes -- using linksUpdated -->.

<!---

not yet working ### Statistical Significance Testing for Links {#links-statistical-significance}
The links table includes the same chi-squared significance testing as the [factors table](../statistical-significance-testing/) but operates on **link bundles** (cause >> effect pairs) instead of individual factors.

**Key differences:**
- **Unit of analysis**: Link bundles instead of factors
- **Bundling**: Links grouped by "cause >> effect" pairs using current filtered labels
- **Example bundle**: All links from "Economic Support" → "Education Access" become one bundle


extra columns: bundle, source count and citation count. Bundle is just the concatenation cause >> effect. source count and links count are number of unique sources / links in the bundle. 

**NOT IMPLEMENTED Summarising features:**

First we add:
- `group by rows` selectize (not multi-select) with default "No grouping". this is populated with all table columns which have fewer than 10 levels. 
- "group by columns" selectize (not multi-select) with default "No grouping". this is populated with all table columns which have fewer than 10 levels. 
- aggregation dropdown with just the values "count unique" (default) and "count".

As usual, the col names in these selectors are populated with the columns of the current links table.

When such a grouper is selected:
- remove action buttons and checkbox and source count and citation count columns

If col grouper is active, show the levels of that colum as columns. if row grouper is None, that really means the default, hidden linkID is providing the rows. If row grouper is active, i.e. not None, the rows show the levels of the row grouper.  
when either grouper is active, cells show the result of the selected aggregation function. 

**Statistical Testing Implementation:**

**Key Differences from Factors Table:**
- **Unit of analysis**: Link bundles instead of factors
- **Bundling**: Links are automatically grouped by "cause >> effect" pairs using current filtered labels
- **Breakdown controls**: Located next to "Breakdown by" selectize instead of factors controls
- **URL state keys**: `linksBreakdown`, `linksCountType`, `linksSigThreshold` (vs factor equivalents)

**How Bundling Works:**
Links are grouped into bundles using **current filtered labels** (after soft recode, etc.), so bundles reflect processed data rather than raw labels. Each bundle represents all links sharing the same cause >> effect relationship.

**Example bundle**: All links from "Economic Support" → "Education Access" become one bundle for statistical analysis, regardless of slight variations in original coding.

For complete methodology, visual indicators, and interpretation guidance, see the [Statistical Significance Testing](../statistical-significance-testing/) section above - all concepts apply identically to link bundles. 

--->


### Assessing link evidence quality {#assessing-link-evidence-quality}

Use this when you want one assessed summary row per causal bundle (`cause >> effect`) while keeping all original unassessed citation rows unchanged.

The **Assessment** control sits **below the Project bar**, to the **right** of the Label Set widget. The button label is just **Assessed** or **Unassessed**. Click it to toggle modes; its tooltip explains the two modes. **Assessed** is only available once the project has at least one assessed row.

**Bundle assessment UI** lives on the Links pane, sub-tab **Assess links** (next to Create links / Filter links). Open that sub-tab to edit bundle-level assessed rows when the global mode is **Unassessed**; in **Assessed** mode the editor is read-only and the app switches you away from **Assess links** if needed.

Because assessed rows can use link custom fields, you can add a narrative judgement field as well as, or instead of, a simple score. For example: `Solid evidence overall, but more sketchy testimony from younger respondents`.

The card’s header **×** sets **Unassessed**, switches to the **Filter links** sub-tab, and briefly highlights the Assessment control.

Ideas Garden: [Assessing quality or robustness of evidence for a causal link](https://garden.causalmap.app/assessing)

#### Main controls

1. 👉🏼 **(Assessed / Unassessed)** (below Project bar): click to toggle between assessed and unassessed links.
2. 👉🏼 **(`Assess links`)** (Links sub-tab): opens the bundle assessment card (when the global mode allows editing).
3. 👉🏼 **(`×`)** (Card header): switches to **Unassessed**, opens **Filter links**, and briefly highlights the Assessment control.
4. 👉🏼 **(`Bundle selector`)** (Dropdown): chooses which bundle to edit.
5. 👉🏼 **(`◀` / `▶`)** (Buttons): move to previous/next bundle.
6. 👉🏼 **(`Help`)** (Button): opens this section in the help drawer.
7. 👉🏼 **(`Tags`)** (Input): sets bundle-level assessed tags.
8. 👉🏼 **(`Sentiment`)** (Buttons + number input): sets assessed sentiment (`-1`, `0`, `1`, or custom numeric value).
9. 👉🏼 **(`Favorites`)** (Buttons): toggles heart / exclamation / star on the assessed row.
10. 👉🏼 **(`Add`)** (Button): adds a visible custom field to the assessed-row editor.
11. 👉🏼 **(`×` on custom field row)** (Button): hides that field from the editor (does not delete saved values).

#### AI-assisted bundle assessment

1. 👉🏼 **(`Run scope`)** (Dropdown): run on `Current bundle` or `All filtered bundles`.
2. 👉🏼 **(`Evidence fields`)** (Dropdown): use `All row fields` or a selected subset.
3. 👉🏼 **(`Evidence fields list`)** (Multi-select): picks fields passed to AI when using selected mode.
4. 👉🏼 **(`Prompt history` controls)** (Buttons + dropdown): reuse previous prompts.
5. 👉🏼 **(`Save assessed link`)** (Button): runs AI and writes results to the bundle’s assessed row.
6. 👉🏼 **(`Status text`)**: shows progress and completion counts (saved / skipped / failed).

When you save an assessed link, CausalMap stores the prompt text used for that assessment on the assessed row so you can see what instruction produced it.

<!--
#### Technical note (assessed mode + pipeline)
- The global assessed switch is implemented as `assessedLinksMode` in the filter pipeline (`unassessed` or `assessed`).
- Canonical output (`currentFilteredLinks`) is always partitioned by that mode at the end of `applyAllPipelineFilters`, so outputs never mix assessed and unassessed rows.
- Assessment editing still needs bundle context from both sides. The pipeline therefore keeps an in-memory companion set (`currentAssessmentLookupLinks`) from pre-partition links in the same run.
- The Links assessment card uses that companion set for lookup/update of existing assessed rows while the visible outputs can remain unassessed-only.
- Legacy per-filter `assessed` widgets are compatibility-only and do not control final canonical membership.
- URL/bookmark state persists this as top-level `assessedLinksMode` (not as a normal filter row).

#### Technical note (Assessment toolbar UI — where it lives and how it wires)

Dev: keep this aligned with `index.html`, `app.js` boot, `table-manager.js`, `dom-utils.js`, `ui-reveal-schema.js`.

- **DOM**: The toolbar is **not** inside the Links button bar. It is in `index.html` under the Project bar in one row with the factor label set: **Label Set first (left), Assessment second (right, `ms-auto` on `#links-assessment-toolbar-wrap`)** — `#links-assessment-toolbar-wrap`, `#links-assessment-mode-trigger`. Help/MapCat: `ui-reveal-schema.js` entry `links_assessment_mode` → `anchorId: 'links-assessment-toolbar-wrap'`.
- **Toggle behaviour**: The trigger is the whole control; there is no popover. Clicks switch `assessedLinksMode` between `assessed` and `unassessed`, while the tooltip carries the short explanation.
- **TableManager**: `TableManager._ensureLinksAssessmentControlsWiring()` attaches the trigger click handler. Inline label text is synced via `_refreshLinksAssessedModeControls()` / `_linksAssessmentModeInlineLabel()` (**Assessed** / **Unassessed**). The **Assess links** sub-tab (left pane, Links) hosts `#links-assessment-panel` in `#links-assessment-tab-mount`; bundle editing is shown only when that sub-tab is active (and the global mode is not **Assessed**, which is read-only).
- **Boot (important)**: Wiring must run **once at app boot** in `app.js` (right after `initFactorLabelSetControl()`), not only from `addLinksControls()`. Reason: `addLinksControls()` is scoped to the Links table and can return early if `#links-button-bar` is not ready or may not run until the Links table is built — users on Sources would otherwise get a dead button. `addLinksControls()` still calls `_ensureLinksAssessmentControlsWiring()` for idempotency (`data-assessment-toolbar-wired` on the wrap prevents double listeners).

#### Functions behind this card

- `renderLinksAssessmentPanel()` builds the card UI and keeps it synced with the selected bundle.
- `runAiBundleAssessmentFromCard()` runs AI over one/all bundles and prepares column assignments.
- `DataService.saveAssessedLinkForBundle(...)` creates/updates exactly the assessed row for each bundle.

TECH NOTE (assessed links prompt traceability):
- Assessed-row saves persist:
  - `links.ai_run_id` when an AI run is active
  - `links.metadata.assessment_prompt` (full prompt text)
- We intentionally do NOT mix prompt IDs into `links.ai_run_id`; that column is reserved for `ai_runs.id`.
-->