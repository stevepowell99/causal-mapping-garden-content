<div class="user-guide-callout">
<strong>🗺️ What you can do here:</strong> See your causal relationships as an interactive network map. Drag nodes around, click on links to edit them, and use the controls to customize how the map looks. You can even drag one factor onto another to quickly create new links. This is where your data comes to life visually.
</div>

### Map Controls <i class="fas fa-sliders-h"></i> {#map-controls}
- 👉🏼 **Jump to factor** (type-to-search dropdown): quickly find and select factors on the map (supports multiple selections).
- 👉🏼 <i class="fas fa-redo"></i> **Refresh layout** (button): reset the map layout after zooming/moving.
- 👉🏼 <i class="fas fa-camera"></i> **Copy image to clipboard** (button): copy a high-quality map image for reports/slides.
- 👉🏼 <i class="fas fa-clipboard"></i> **Copy legend** (button): copy the map legend text.
- 👉🏼 **Zoom in/out** (controls): zoom the map view.
- 👉🏼 **Double-click** (gesture): zoom in to that point on the background.

### Map Legend <i class="fas fa-list"></i> {#map-legend}
Discrete text legend showing:
- projectname and included sources
- Citation coverage percentage
- Visual encoding explanations (link sizes, colors, numbers)
- Applied filters summary
  - 💡Tip: Click [Copy legend](../map-controls/) to copy this text to clipboard.
  - You can drag the legend box to reposition it on the map.

### Evidence (shortcut to Links Print View) {#map-evidence}
- 👉🏼 **Evidence** (button, bottom-right on the map, opposite the legend): switches to the **Links** tab and opens **[Print View](../quotes-widget/)** for the **same filtered links** you see on the map. It applies a preset—**Group by** Bundle and Source, **sort** by citation count (highest first), **Show details** and **Context** on, **page size** 50—and updates the URL so you can bookmark or share that layout. A toast links to Print View help; a short hint may point to the **Print view** toggle.

<!---

Legend only reports filters that differ from default values. Always ignores text filters with blank fields and path tracing with both fields blank.

Legend format example:
- projectname: foo. Sources included: FX-1, FX-2, FY-3.
- Citation coverage 17%: 135 citations shown out of 786 total for filtered sources
- Link sizes: citation count. Numbers on links: source count. Numbers on factors: source count. Factor sizes: citation count
- Factor colours: outcomeness
- Filters applied: Tracing paths, matching anywhere, 4 steps from `Increased knowledge` (purple borders) to anywhere. Zooming to level 1. Top 10 factors by citation count.

--->

### Map Formatting <i class="fas fa-sliders-h"></i> {#map-formatting-card}

#### Customisable formatting (Things you can tweak)

**Layout and interaction**

- 👉🏼 **Layout** (dropdown): choose how the map is laid out.  
  - Interactive and most other layouts are good while you are conducting your research (fast + supports the [interactive features](../interactive-features/)).  
  - Print/Graphviz is best for static images (reports/journal articles). In Graphviz SVG you can still pan/zoom (mouse wheel, double-click, Shift+double-click).
- 👉🏼 **Groups** (dropdown): layout maps with top-level factors as boxes which group together their "children". Choose how group titles are extracted from factor text: No groups / Level 1 (;) / First colon (:) / Square brackets [] / Round brackets ().
- 👉🏼 **Direction** (radio group): LR, RL, TB, or BT (for Interactive and Print/Graphviz layouts).
- 👉🏼 **Link direction** (dropdown): Normal (directed arrows) vs Undirected (dots at both ends).  
  - In Undirected mode, dots use the same colours as arrowheads (including sentiment colouring). When sentiment is neutral (0), they use **Link Colour**.  
  - Note: when the [Combine Opposites filter](../combine-opposites-filter/) is active, tail/head can still have different colours.

**Factors**

- 👉🏼 **Factor labels** (dropdown): what to show next to each factor (same data as the [Factors Panel](../factors-panel/)).  
  - Citation count (default) / Source count / Sentiment (mean incoming) / None
- 👉🏼 **Factor colours** (dropdown): Outcomeness (default) / Influence / Citation count (total, in, or out) / Source count (total, in, or out) / **Label segment** (full label or the same segment patterns as **Groups**) / None
- 👉🏼 **Factor sizes** (dropdown): Citation count (default) / Source count / None

**Links**

- 👉🏼 **Link labels** (dropdown): what to show on each link.  
  - Citation count (default) / Source count / Sentiment / Label by Group / Unique Sources / All Sources / Unique Tags / Unique Tags (Tally) / All Tags / None
- 👉🏼 **Link widths** (dropdown): Citation count (default) / Source count / None
- 👉🏼 **Link label font size** (control): change link label font sizes.
- 👉🏼 **Arrowhead size** (control): scale arrowhead size (Interactive + Print/Graphviz). Default 100% keeps current appearance.
- 👉🏼 **Link colour** (colour picker): sets the default link line colour (Interactive + Print/Graphviz). When sentiment is neutral (0), this colour is also used for arrowheads and node borders.
- 👉🏼 **Links highlight** (dropdown): optional extra "halo" highlighting without changing the base colour scheme.  
  - Off (default)  
  - Reverse (backwards/same-rank in current layout direction)  
  - Significant (when Label by Group shows ⬆/⬇)  
  - Feedback loop (2 / ≤3 / ≤4 factors)  
  - Feedback loop + reverse (combine the above)

**Other**

- 👉🏼 **Show self-loops** (toggle, default on): show/hide A→A links on the map.



<!---

**Factor Count Display (#factor-count-type):**
Control to display count at end of each factor label in brackets. If set to citation count (default), label becomes "foo label (nn)" showing nn citations for this factor.

**Link Label Options (#link-label-type):**
- Citation count (default)
- Source count
- Sentiment: Mean sentiment for the bundle (-1 to +1)
- Label by Group: Uses field and display mode from Label by Group
- Unique Sources: List unique source IDs in alphabetical order 
- All Sources: List ALL source IDs in order eg M1 M1 M2 M3 M4 M4 M4 etc
- Unique Tags: List unique link tags in alphabetical order eg #hypothetical suspicious
- Unique Tags (Tally): List unique link tags with per-bundle counts eg #hypothetical (3) suspicious (1)
- All Tags: List ALL link tags in order eg #hypothetical #hypothetical suspicious

**Factor Color Options:**
Colors factor backgrounds:
- outcomeness (default, current formatter)
- source count
- citation count
- none

**Self-loops Display:**
Toggle next to #link-label-type "Show self-loops" controls whether to show self-loops from foo to foo.  Default TRUE.

--->


#### Fixed visual appearance (things you can't tweak) {#visual-appearance}

Some parts of the map’s appearance are automatic (i.e. they are not controlled by the Map Formatting widgets above):

**Leading emoji (Print / Graphviz only):**
- If a factor label starts with an emoji, the **Print (Graphviz)** SVG post-process moves that emoji to a larger symbol offset near the top of the node and removes it from the inline label text (trivial matches like lone digits are left inline). **Interactive** layout keeps the full label, including any leading emoji, in the normal label position.

**Link geometry (bundling):**
- Links are bundled and drawn as curved edges for readability.

**Automatic colouring overlays:**
- Arrowhead colours reflect mean **sentiment** for that link bundle (neutral uses your chosen **Link colour**).
- When the [Combine Opposites filter](../combine-opposites-filter/) is active, arrowhead colours instead reflect **flipped share** (tail=cause, head=effect).

**Automatic highlighting:**
- Factors that match filters like [Factor Label](../factor-label-filter/) or [Path Tracing](../path-tracing-filter/) show dashed coloured borders.
- Factor border colour reflects mean incoming edge sentiment (but when Combine Opposites is active: average flipped share, blue→red).

<!---

**Link Appearance:**
- Arrowheads colored by mean sentiment of bundled edges
- Color scale: muted blue (+1) → grey (0) → muted red (-1)
- Bezier curved edges with bundling for clarity

**Node Appearance:**
- Size scaled by node degree (with min/max bounds)
- Border color reflects mean incoming edge sentiment (but when Combine Opposites is active: average flipped share, blue→red)
- Missing sentiment values treated as zero for calculations
- Factor background colour varies from white to mid-pale green according to "outcomeness" (in-degree/degree)
- If factors are matched by labels filter or path tracing filter, borders are dashed with special colour

--->



### Interactive Features {#interactive-features}

These work for all layouts except Print/Graphviz layout (which is mostly for static export, but does support clicking nodes/links now).

- **Drag factors** to temporarily reposition them
- **Drag factor to factor** to create new links
- **Shift+drag** for box selection of multiple factors (opens edit modal)
- **Ctrl+drag** for box selection of multiple factors (direct selection, no modal)
- **Click a link** to edit.
- **Click a factor** to edit; shift-click or ctrl-click to add to selection without opening modal.

#### Editing and deleting (multiple) factors
- Select factor(s) by clicking a factor, shift-click or ctrl-click to add more, or shift+drag/ctrl+drag a box around multiple factors, then:
  - Move selected factors together
  - Delete matching factors everywhere or in current view only
  - Rename matching factors everywhere or in current view only

**What does "everywhere or in current view only" mean?**
- **everywhere**: all links containing factors with exactly the selected labels will be deleted
- **in current view only**: all links containing factors with exactly the selected labels (and matching the current filters, i.e. those you can see in the current map) will be deleted


💡Tip: By control-clicking or shift-clicking multiple factors you can easily rename several at once, e.g. you can merge multiple factors as a single factor.


### Grid layout

**What this is for:** Sometimes you want factors to appear in a rough **grid**—like “this cause is clearly to the left of that one”—instead of leaving the layout algorithm to guess. You do that by putting a small **coordinate tag** in the factor label (anywhere in the text). The app reads the tag to place the box, and (by default) hides the tag so respondents don’t see a string of numbers.

This is especially useful when:
- your factors fit logically into some kind of positional story like a theory of change and you want to keep them there
- you are showing many different versions of a larger map (e.g. districts within a country) and you want them to be more easily comparable.

**How to write a tag:** Use two whole numbers: a **column along the main flow** of the map and a **row** across the flow. For example `(2,1)` or `(2.1)` in the label means “second step along the story, first slot across.” You can use square brackets instead of parentheses, and you can leave one side blank if you only care about one direction—for example `(3,)` fixes the step along the flow but not the slot across.

**In Map Formatting**

- **Grid layout** — Turn this **off** if you want to ignore tags and let the map place everything as usual. It only appears when at least one factor in your current links actually has a tag. Default is **on**.
- **Strip grid tags** — Turn this **off** if you want to **see** the `(…)` or `[…]` text on the map. Default is **on** (tags still affect layout when **Grid layout** is on, but the numbers are hidden on the label). These two switches work independently.

**Interactive map** (the usual live map): tagged factors snap to a grid; anything without a tag is still laid out automatically, but is kept **near** the grid so the picture stays readable.

**Print / Graphviz** (static SVG): the app can’t pin exact pixel positions like the live map, but it still respects **left‑to‑right order of the first number** along the direction you chose, and does its best to respect the second number **within** each step. If you only give a second number and not the first, Print layout can’t place that factor on the “step” axis—use both numbers when you care about order.

**Heads-up:** The grid helpers only apply to the **default interactive** layout and to **Print**. If you switch the live map to layouts like **Cola**, **Circle**, or **CiSE**, coordinate tags are **not** used for placement.

<!---

**Grid layout — technical reference (implementation)**

Tag syntax (anywhere in label): full `(N.M)` or `(N,M)`; partial / bracket `(N,)`, `(,M)`, `[N,M]`, `[N,]`, `[,M]`. Convention: first number = rank direction (main flow), second = perpendicular.

Controls: `#enable-grid-layout` gates Dagre preset + DOT rank hints; disabled when `updateGridLayoutToggleState` finds no `extractGridCoordinates` on any link cause/effect. `#strip-grid-tags` strips display only (see `stripGridTags` / DOT label loop); independent of grid layout toggle.

Interactive: grid preset `applyForcedGridLayoutPreset` + post-`layoutstop` axis re-apply, repulsion, bounds, gravity — **only when `layout-select` is `dagre`**, not cola/circle/cise. Both coords → `node.lock()` + `positions` for dagre; one axis → `axisConstraints` re-applied after layout. Grid bounds in units: min rank−1..max+1, min perp−1..max+1 (defaults when one axis missing in data).

Print/DOT: Graphviz has no arbitrary x/y; when grid on and `hasGridRankTagNodes` (finite first coordinate / `coords.x`), `generateDotString` adds invisible rank anchors, `rank=same`, chained `constraint=true` invis edges for rank order; within-rank ordering via `constraint=false` invis edges; skip helper edges that duplicate real edges. Y-only tags `(,M)` do not join rank chain. Strip from DOT labels only if strip checkbox on.

Layout direction mapping (first = rank, second = perp): LR — first→x left-right, second→y top; RL — first→x flip; TB — first→y top-bottom, second→x; BT — first→y flip, second→x. See `applyForcedGridLayoutPreset` branches.

--->

<!---

**Graph Layout:**
- Left-to-right orientation using Cytoscape
- Clickable links open editor or chooser modal
- Visual feedback during selection
- Edge handles for drag-and-drop link creation

**Link Interactions:**
- Clicking on link opens modal with selector to choose specific link to edit
- Causal overlay for editing (from map and links table) has button to open sources panel and textviewer, scrolling to relevant highlight

**Factor Interactions:**
- Factor click opens modal with options:
- Delete factor everywhere (all projects)
  - Delete factor in current filters only
- Rename factor everywhere (all projects)  
- Rename factor in current filters only
- Shift + drag to select multiple factors, then move by clicking and dragging one selected factor
- Box selection: Hold Shift and drag to select multiple nodes, opens same modal as single node selection
- Box selection: Hold Ctrl and drag to select multiple nodes directly without opening modal

**Creation Mode:**
- Drag-and-drop one factor towards another creates new links (using cytoscape "edge handles")
- Causal overlay opens with prefilled cause and effect boxes
- Editable selected_text field prefilled with "manual"
- Toggle between creation mode and normal mode

--->


### Vignettes <i class="fas fa-pen"></i> {#vignette-card}

<div class="user-guide-callout">
<strong>📝 What you can do here:</strong> Generate AI-powered narrative summaries of your causal maps. Choose between a **whole-map** summary that covers the relationships in your current filtered view, or a **typical-source** story that focuses on one representative respondent. Useful for reports, annexes, and explaining your analysis in plain language.
</div>

#### For practitioners (getting started)

**What are vignettes and why use them?**  
Vignettes turn your coded causal map into readable prose. After you have links (and usually quotes on those links), the AI can draft a narrative that names themes, tensions, and patterns in your material. You stay in control: you choose the prompt (tone, audience, structure), and you can edit the text afterwards. They are a fast way to move from “many links on a map” to “something I can paste into a report or share with stakeholders”—not a substitute for your judgement, but a structured first draft.

**Whole-map vignette**  
Use this when you want a bird’s-eye story of **everything that is currently in the map** (respecting your filters and source selection). The app sends a compact summary of factors and bundled links (with sentiment), **evidence snippets** (quotes and source IDs from highlighted bundles where available), and up to **30 “typical” sources** scored by how much they represent common bundles—each with bundles, link-level quotes, and a small **metadata preview** (title, filename, and simple custom fields). If you want the narrative to emphasise particular edges, set **Map Formatting → Links highlight** to **Significant** or **Feedback loop** first; that snapshot is included so the model can focus there. **AI region** (where Gemini runs) follows **Project Details → AI region**, not a separate control on this card.

**Typical-source vignette**  
Use this when you want a **single-respondent case study**: the app picks the most “representative” source for the **current** map view (using link counts and coverage of bundles, with a bias so very long documents do not always win). It sends that source’s **full text** plus its links with quotes and sentiment, so the model can write as if telling **one** story. Do not ask it to generalise across the whole project in this mode—the prompt and data are scoped to that one source.

**How to use (UI):**
1. Open the **Vignettes** card on the Map side panel and expand it if needed.
2. Choose **model** (and optional **thinking** controls if your model supports them). **Region** for AI is set per project under **Edit project** (AI region), not on this card.
3. (Optional) Leave **Enable checking (second AI pass)** on so a checker can review the draft; notes appear in a collapsed panel when relevant.
4. Edit the **Whole-map prompt** and/or **Typical-source prompt** (prompt history: dropdown and prev/next; see [tips on using prompt history](../tips-prompts/)).
5. Click **Write Whole-map Vignette** or **Write Typical-source Vignette** (two separate buttons).

**Tip (optional): tell the AI which links matter most (whole-map mode):**
- Go to **Map Formatting → Links highlight** and choose **Significant** or **Feedback loop**.
- When you run the **whole-map** vignette, the app includes a small snapshot of those highlighted edges so the model can focus on them.
- If **Links highlight** is **Off** (or **Reverse** only, with no edges flagged), or nothing qualifies, **no extra highlight list is sent**.

**What each mode sends (summary):**

- **Whole map:** Aggregated nodes/edges for the current view, optional **links highlight** snapshot, **bundle evidence** (quotes/source IDs sampled from top bundles so large projects stay within limits), and up to **30 typical sources** with bundles, per-link quotes, and compact source metadata—not the entire raw links table.
- **Typical source:** One chosen source’s **full text**, its links with quotes and sentiment, simple node frequencies, and optional links-highlight context for that source.

**Output format:** Markdown (headers, bold, lists, blockquotes, code blocks). You can copy from the result area.

**Bookmarking & restore:**
- Each run saves a **bookmark** for the current view (description: `Vignette (whole|typical): <your prompt>`) and appends a link at the bottom of the vignette output.
- The bookmark footer includes the **model name** used.
- Vignette-related settings are stored in **URL state** where applicable (model, thinking, checking, prompts); project **AI region** lives in project metadata.

<!---

**Technical Implementation:**

**Whole Map Payload:**
- Node frequencies and average effect sentiment
- Bundled edges with frequencies and average sentiment
- Optional **linksHighlight** snapshot from Map Formatting (Significant / Feedback loop) when applicable
- **bundleEvidence**: top bundles by link count with sampled per-link evidence (quote from `selected_text`, `source_id`, sentiment, optional original labels); sampling when the linkset is very large
- **typicalSources**: up to 30 sources scored by bundle coverage + frequency; each entry has `title`, `filename`, `source_custom_preview` (primitive custom fields only), and `bundles` → `links` with quotes; up to 5 links per bundle per source (random sample if more)
- Context is JSON-embedded in the prompt via `PromptSanitizer.wrapPromptWithContext` (sanitizer depth must allow nested `{ payloadType, data }`).

**Typical Source Payload:**
- Selection normalizes link count by text length (per 1000 characters) to avoid bias towards longer sources
- Selection includes a 50% weight based on the proportion of bundles the source covers
- Includes the full source text (content from sources)
- Includes individual links with quotes (`selected_text`) and sentiment plus node frequencies; optional **linksHighlight** for that source

**UI Components:**
- Model dropdown (saved per-project to localStorage)
- AI **region** is **not** on this card; Vertex region follows `projects.metadata.ai_region` (Project Details → AI region)
- Two buttons: **Write Whole-map Vignette** / **Write Typical-source Vignette**; prompt history via `prompts` table (DB-backed)
- Thinking budget / level (for supported models)
- Status indicator during generation

**Default Prompts:**
- Whole map: "This is parts of stories told by several respondents. write a) a local-newspaper style heading (markdown h2) summarising the stories, then a three-sentence summary in simple, straightforward language illustrated with key quotes, and then a one-paragraph more technical summary like in a social science blog, also illustrated with quotes. Note the sentiment field gives the sentiment of the effect of the causal link, from -1 to +1. Note the node labels may not be quite appropriate especially in terms of sentiment / valence so don't get too misled by them."

- Typical source: "This is a typical respondent telling their story. The full source text is provided, and the link quotes are verbatim extracts from that text. write a) a local-newspaper style heading (markdown h2) summarising the story, then a three-sentence summary in simple, straightforward language illustrated with key quotes, and then a one-paragraph more technical summary like in a social science blog, also illustrated with quotes. Note the sentiment field gives the sentiment of the effect of the causal link, from -1 to +1. Note the node labels may not be quite appropriate especially in terms of sentiment / valence so you should definitely mention them if you can but don't worry if they don't fit, find other words instead."

**Markdown Rendering:**
- Custom converter handles callouts (`>`), lists, headers, code blocks, bold/italic
- Callouts styled with left border and background (same font size as body text)
- Lists properly wrapped in `<ul>`/`<ol>` tags
- HTML escaping uses placeholder system to protect generated tags

--->