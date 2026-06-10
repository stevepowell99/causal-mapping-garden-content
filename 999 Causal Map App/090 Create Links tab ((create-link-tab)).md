Qualitative causal mapping involves taking passages of text, e.g. from interviews or documents, and identifying sections which make causal claims. We highlight each of these sections and specify a causal factor at each end of each link (for example Lost job or Went hungry). This means creating a new factor or reusing an existing one. Usually we create these factors inductively as we code, and revise and review and consolidate them as part of the process, as with any other kind of qualitative content analysis. 


To code a causal link,

- With your mouse, highlight a piece of text within the statement which makes a causal claim. Your selection must remain within one statement and must not cross into another statement.
- Watch how that passage is copied for you into the "Quote" window. (Usually, you don't need to think about this window: you can edit the text if you really need to but it **has to remain an exact quote of one part of the text**.)
- Start to type the name of the influence factors at the**start** of the link(s) which you are going to make, in the first drop-down menu.
- If there is an existing factor which matches what you want, you can select it.
- Otherwise, you will create a new factor with the contents of what you have typed; finish what you have typed with a comma or a tab character if you want to continue to select or create another factor.
- If you want to create more than one link, you can select or create additional factors in the same box (as shown in the video below).
- When you have finished, press Enter.
- Repeat the process in the other box to specify the factors at the**end** of the link (or ends of the links).
- Press the green Save button which is now active.
- The link is created in the Map window.
- When you have finished coding one source, click the right arrow in the **Source text** header to code the next source.

### Source Text Viewer {#text-viewer-content}

<div class="user-guide-callout">
<strong>✨ What you can do here:</strong> Read your source documents and create causal links by highlighting text. When you highlight a passage that claims or implies that one thing influences or causes another, a popup lets you identify the cause and effect. 

This is where you do the core work of mapping out causal relationships from your source material, a process which we call *coding*</strong>
</div>

The text viewer shows full text from one source at a time. The **Source text** header contains source ID, source info toggle, source Prev/Next, highlight navigation, and Help. When you select several sources, it initially shows the first in the selection; with **two or more** selected, a **pen-to-square** icon on a pill in the Sources dropdown marks which source is on screen. You can:
- Highlight sections to identify causal claims. Highlighting opens the causal link editor.
- Examine and edit existing highlights by clicking on them.

#### Full text search (selected sources) {#full-text-search}

Below the **Sources** bar, **Full text search…** opens a small panel. Type **at least three characters** to search **source text** in the current scope (same rule as the Sources dropdown: **no selection = all sources** in project order; **more than one** source selected = only those; **exactly one** selected still searches **all** project sources for this tool—only the strict multi-select narrows the list). Matches are highlighted in the viewer in a **separate colour** from causal link highlights; they do **not** change the links table or filters.

Use **First / Previous / Next / Last** to jump between hits. The counter shows **hits** and how many **sources** actually contain a match (out of how many are in scope). When the next hit is in another source, the viewer **loads that source** without changing what is selected in the Sources dropdown (so **empty = all** stays empty). **×** clears the query and closes the panel; **clicking Full text search… again** while the panel is open does the same.

Inside the header, there is an info ℹ️ icon which toggles open/shut a panel beneath it which shows the values of the custom columns for the current source e.g. gender etc. 


<!--

ignore the help search highlighting, that is a different system, leave it alone. 
with the rest:
Highlight positions are stored once per link in start/end offsets links.text_start_offset / links.text_end_offset.

For AI highlighting, the model receives text from the Sources table (including line breaks). Returned `selected_text` may differ in how it represents line breaks. We locate canonical start and end offsets in the original text using a single method:
- Case-insensitive literal match first
- If no exact match, fuzzy match via a fuzzy-search library
- No additional strategies
The resulting start and end are absolute positions in the original, unchanged source text.

Then, to do the actual highlighting in textviewer, don't iterate but calculate in advance the positions of all the starts and ends of all the spans including spans which mark overlapping sections, BEFORE allowing for the fact that the actual html will ultimately also include br linebreaks and look like: <br>"some text"<br><br> etc. 
Then, produce the actual html with all the correct spans, <br>, etc. 

MANUAL HIGHLIGHTING:
Behaves the same. The `selected_text` contains no HTML. We first try exact match, then a single fuzzy match to determine and store start/end positions.  

-->

#### Navigation Controls {#navigation-controls}

Navigate sources (buttons in the **Source text** header):
- <i class="fas fa-chevron-left"></i> **Previous source**
- <i class="fas fa-chevron-right"></i> **Next source**

Navigate highlights within the current source:
- <i class="fas fa-fast-backward"></i> **First highlight in source**
- <i class="fas fa-step-backward"></i> **Previous highlight**
- <i class="fas fa-step-forward"></i> **Next highlight**
- <i class="fas fa-fast-forward"></i> **Last highlight in source** (useful if you haven't finished coding the whole text yet and want to see the last highlight)


Source selection is controlled by the Sources dropdown. When several sources are selected, the viewer starts on the first; with **two or more** selected, a **pen-to-square** icon on a pill shows which source is open (hidden when only one source is selected).

- **Multiple sources selected:** Main Previous/Next pages between the selected sources and only changes which source is displayed in the text viewer. It does **not** change the actual selected-sources set.
- **Exactly one source selected:** Main Previous/Next pages through **all project sources** (project order). In this mode it **does** change the selected source, so both source selection and text viewer content update together.
- **No source selected (empty = all):** Main Previous/Next picks and then pages in project order like the one-source case, so selection changes as you page.
- These navigation rules apply equally when selected sources currently have zero links.

#### Dealing with long documents in the source text viewer {#long-documents-text-viewer}

For documents longer than ~30-40 pages, the text viewer automatically splits content into manageable chunks for better performance.
- 👉🏼 **Next chunk** (button at end of chunk): appears at the end of each chunk (except the last).



### Visual Highlighting {#visual-highlighting}
Each section of coded text, each causal claim, is shown with a highlight. 

For overlapping or identical highlights with multiple links, overlaps are shown with varying color opacity. Clicking on multiple highlights shows a link selector for each section.
- Multiple highlights shown with varying color opacity
- Click on overlapping highlights to select specific links

### Link Editor screen {#causal-overlay}

<!--aka ("Causal Overlay") -->
Opens when you highlight text or click on existing links.

**Fields:**
- 👉🏼 **Project** (read-only): current project name.
- 👉🏼 **Source** (text): source document id for this link; editable and prefilled when you code from the text viewer. Save requires a non-empty value; if you change it from what it was when the overlay opened, the app asks you to confirm.
- 👉🏼 **Cause selector** (multi-select dropdown + free text): choose one or more causes (project-wide list, sorted by frequency).
- 👉🏼 **Effect selector** (multi-select dropdown + free text): choose one or more effects (same project-wide list). After you select Causes, the Effect dropdown boosts the most common effects of those causes to the top.
- 👉🏼 **Quote** (text area): editable evidence text; supports ellipses like `Actual quote [this text is ignored] quote continues...`.
- 👉🏼 **Chain** (toggle): if on, saving keeps the editor open and uses the previous Effect as the next Cause.
- 👉🏼 **Plain coding** (toggle): if on, saves a self-loop (Cause = Effect) tagged `#plain_coding` so it counts as “theme present” rather than a causal claim. Plain codings can be hidden with the [Exclude self-loops](../exclude-self-loops-filter/) filter.
- 👉🏼 **Tags** (multi-select input): add tags like `#hypothetical` or `check`.
- 👉🏼 **Favourites** (3 toggle buttons): heart / exclamation / star.
- 👉🏼 **Custom fields** (collapsed panel): choose a small subset of link custom columns to edit in-place for this overlay. You can also type a new field name here to create it for the project. The selection is remembered per project; untouched custom columns are preserved.

**Actions:**
- 👉🏼 **Save** (button): create/update link(s).
- 👉🏼 **Delete** (button): remove an existing link.
- 👉🏼 **Cancel** (button): close without saving.

**Update behavior:**
- If you save with exactly one Cause and one Effect, the editor updates the existing link row in place.
- If you save with multiple Causes and/or Effects, the editor applies causes × effects and recreates rows for that cross-product.


Links in Causal Map only have one cause and one effect. You can add multiple causes and/or effects to the boxes, and the system createsall combinations when saving. So if you put `unemployment` and `violence` in the Cause box, and `stress` and `worry` in the Effect box, the system will create four links.

<!---
The favorites buttons are stored in the metadata column and appear in the links table for searching and sorting.

TECH NOTE (Effect suggestion re-ordering):
- Implemented in `webapp/js/causal-overlay.js`.
- When Cause selectize changes, we re-order Effect options by observed cause→effect frequency from the project’s links.
- Uses `DataService.getProjectLinks(projectName)` so it benefits from the in-memory cache (no DB temp tables).
- Auto-disabled for large projects to avoid slowing the overlay (search-only mode, or very large link/label counts).

TECH NOTE (Source id field, `#overlay-source-id`):
- Editable in `webapp/index.html` (not readonly). Baseline when the overlay opened is stored as `_overlaySourceIdAtOpen` (normalized trim); set when opening a new highlight, when editing an existing link, and after a chained save prepares the next link (`_captureOverlaySourceIdBaseline()`); cleared in `hideOverlay()`.
- On Save: trimmed source id must be non-empty. If it differs from `_overlaySourceIdAtOpen`, `confirmModal` (from `ui-utils.js`) asks to confirm changing the id; a blank baseline is labeled `(empty)` in the message.
- New links and updates pass this trimmed id into `createLinksFromCausesEffects`; **Go to source** prefers the trimmed input, then the existing link’s `source_id`.
- **Update existing link:** `updateExistingEntry` snapshots `this.currentEntry` into a local `entry` *before* `await DataService.deleteLinksByIds(...)`, then uses `entry` for `text_start_offset`, `text_end_offset`, and selected-text fallback — after the await, `this.currentEntry` may already be null if other handlers ran.
--->

### About the factor label dropdown menus

By creating links, you also create the names of your factors.

In Causal Map, a factor*is*its label. Once you create a label, there is nothing else to add.

Factor names which contain semicolons **`;`** get special treatment as they separate the different parts of [🔖 Hierarchical factors](xx) .

After beginning to create links between factors, already-coded factors will appear in the dropdown menus in the to and from factor boxes. For added convenience. The most frequently coded factors will appear at the top of this list


### #doubtful? #hypothetical? Adding link tags

#### Link tags

Link tags are available as a special kind of memo when coding a link: you can use them to provide any kind of additional information.

There is no need to actually use a hash `#` at the start of a link tag, though you can if you want. Just use any unique single word which is easy to search and filter on, like #nutrition or nutrition# or nutrition–.

As usual in Causal Map, you can apply one or more tags, and you can either select existing tags or create new ones on the fly.

Later, you can filter the map (see  [✨ Transforms Filters: Include or exclude tags](%E2%9C%A8%20Transforms%20Filters%20Include%20or%20exclude%20hashtags%2052c71ae58ea74c628a790142f9b728f8.md)) to show only links containing or beginning or ending with specific hashtags (or parts of hashtags), and also for links which do*not*contain specific hashtags or parts of hashtags.

You can also use tags to narrow down your searches in [🔗 The Manage Links tab](%F0%9F%94%97%20The%20Manage%20Links%20tab%2070835b4b20664837870680b7151d4c6e.md).

You can display [tags on your map](../%EF%B8%8F%E2%83%A3%20Link%20tags%2050a789cc60ad4b1e9cad10b81c68e2a1.md/).

Conceptually, there are two kinds of tag.

#### Ordinary link tags

You can use any tag which does not begin with a `?` to record any other information about the link, e.g.:

- respondent doesn't like this connection
- respondent feels good about the outcome
- for you, the analyst, e.g.
    - respondent is answering a different question
    - to tag links you want to come back and review.

#### Weak tags

Weak tags are a special kind of tag. They are*caveats*. If you use weak tags, you should make sure that by default your maps do not include any link with a weak tag.

This is just a convention, it makes no difference to the Causal Map app. 

They begin with `?` and are used to mark any link which you are not sure is always valid across the global context for the whole global map, for example:

- **the causal connection** is only valid for a specific context, e.g.
    - the respondent says this is only true for their village, not for other villages e.g. `?village X`
    - a link is only projected for the future e.g. `?future`
- you are unsure about **the claim about the causal connection**
    - a link is only a hypothesis e.g. `?hypothetical`
    - you as the analyst are not confident in the claim e.g. `?doubtful`
    - the source themselves are not sure e.g. `?source seems unsure`
    - to add other qualifying information e.g. `?probably hearsay`
    - to mark the fact that a connection is **weak or non-existent**, e.g.
        - Respondent makes a substantive claim that X does *not* influence Y, e.g. `?zero influence`
        - Respondent makes a substantive claim that X only insignificantly influences Y, e.g. `?weak`