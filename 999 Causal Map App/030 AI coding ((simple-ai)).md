The **AI Coding panel** provides a streamlined AI coding workflow inside the normal left pane. It keeps the app structure familiar while reducing clutter.

<div class="user-guide-callout">
<strong>Quick start:</strong> If you have roughly 5–100 pages of text, you can usually **just run everything** and get decent results. Press **One-click coding** and confirm the short set-up modal, then let it run. You can then go back and adjust the coding (edit links, tweak prompts, re-run specific steps) if you want. For longer texts or high-stakes coding, work incrementally: use the **source limit** in Auto-code (1, 5, 20%, 50%, 100%) and the **Links limit** in Recode to process a sample first, check quality, then scale up.
</div>

AI is switched on and off in the [Account panel](../account-panel/) with the **"AI options switched on and active"** switch. If you choose an AI workflow when you sign up, it is turned on for you; otherwise you can turn it on there at any time. When AI is on, the **AI Coding panel** appears inline at the top of the **Create links** tab, ready to use.

AI usage consumes **credits** (see [Responses Panel](../responses-panel/)); credits renew monthly and do not roll over. Costs depend on model and workflow, but very roughly you might autocode around 30 pages for about 1 credit.

Users with dedicated AI plans receive a larger batch of AI credits each month; other users receive 10 free AI credits per month (the free credits do not stack with paid plans). 

### The AI Workflow

The AI Coding panel sits at the top of the **Create links** tab, above the source text viewer. The Sources bar, the right-hand output tabs, and the **Create links** / **Filter links** / **Assess links** tabs all stay where they are; the panel does not take over the screen.

The panel is broken down into five straightforward sections (filtering is a separate step, see below):

1. **One-click coding**: Pipeline runner with a **set-up** modal first. Press **One-click coding** to choose **level of effort** (Flash vs Pro for the AI model slots), **Skip coded**, **Filter on finish**, and (if the project has links) whether to delete **every** link in the project or **only** links on the sources in scope, then confirm **Run**.
   - Pre-steps: clears Filter Links and turns the filter pipeline **on** before the modal.
   - **Scope**: One-click respects the Sources bar (empty bar = all sources, otherwise your current selection) and the sources % radio, exactly like the Auto-code button (no separate "code all sources" toggle). The modal states how many sources Auto-code will run on, including the % sample and when **Skip coded** removes already-coded sources (and **Run** is disabled if nothing is left).
   - **Auto-code prompt**: One-click coding uses the current Auto-code panel prompt and settings. The prompt is shown in the set-up modal before you run.
   - **Single source** in scope: only **Auto-code** runs (Revise codebook and Recode are skipped so labels are not merged across several AI passes). **Filter on finish** defaults off in that path but you can turn it on.
   - **Several sources** in scope: **Auto-code**, then **Revise codebook**, then **Recode**.
   - **Recode target suffix**: Choose blank (simpler — synthesised labels go straight into cause/effect) or e.g. _recoded (keeps raw labels, writes synthesised to temp columns so you can compare).
   - Per-step **Run** buttons still work on their own; the modal suppresses the extra confirms for the sequenced run after you confirm **Run**.
2. **Background**: Give the AI project context before coding. A status tick indicates whether enough background text is set.
3. **Auto-code**: This is where the AI reads your documents and extracts causal links. 
   - You can choose to process a small sample first (e.g., `1` or `5` sources) to test your prompt, or process `100%` of them.
   - The "Skip coded" switch ensures you don't waste time and money re-processing documents that already have links.
   - Default model is **Qwen Flash**.
4. **Revise codebook**: Once you have some causal links, the AI can review them and suggest a cleaner, more consistent list of factor labels (a "codebook"). The header tick shows whether the Recode codebook area currently contains suggestions.
   - Includes a **Target clusters** slider; see [Target clusters](../simple-ai-target-clusters/).
   - Optional **Use automatic pre-clustering** switch (default OFF).
   - When pre-clustering is OFF, the AI tries to find the clusters directly from the factor list using the standard Revise codebook prompt. This prompt supports macro replacement: use `[number]` (or `[cluster_count]`) and the **effective** target cluster count is injected at run time (same as the slider logic below).
   - When pre-clustering is ON, the app first groups factor labels semantically using embeddings, then sends those clustered groups to the AI with a separate labelling prompt plus a **Representatives per cluster** slider (`8` to `20`, default `8`).
   - Pre-clustering is more systematic than asking the AI to find all clusters "in its head" from a long raw list. It reduces the black-box / WEIRD-data risk a bit, and may make it easier to preserve more unusual or divergent concepts instead of collapsing them into whatever the model finds most typical.
   - Default model is **Gemini 3 Flash Preview**.
5. **Recode**: Apply the AI's suggested, cleaned-up labels back to your existing causal links. Paste the codebook (from Revise codebook or your own), add a recode instruction, and run.
   - In **AI factors** mode the AI returns index mappings (row → codebook item) rather than full label text, reducing tokens and improving reliability; in **AI links** mode it returns a recoded cause and effect for each link.
   - **AI factors** and **AI links** each have their **own recode-instruction box, default and history** (separate prompt channels), and only the box for the selected mode is shown. AI factors default: *"For each raw label give me the number of the best-matching codebook item by meaning. Use 0 when no codebook item fits. Never invent labels."* AI links default: *"Recode each link to the codebook: pick the best-matching label for its cause and for its effect, using the link quote for context."* <!--- factors channel rag_ai_simple_factor_recode (#ai-simple-factor-recode-prompt); links channel rag_ai_simple_links_recode (#ai-simple-links-recode-prompt). Kept separate so the two prompts and histories never collide. -->
   - **Skip recoded**: When on, only processes links that have at least one unrecoded label (cause or effect). Use this when recoding again to focus on remaining work.
   - **Links limit** (1, 5, 20%, 50%, 100%): When not 100%, a random sample of links is recoded. Non-sampled links keep their existing recoded values (or stay blank on first run).
   - The header progress bar is segmented: grey = empty recoded fields, orange = recoded equals original cause/effect, green = recoded non-empty and different.
   - Default model is **Qwen Flash**.
After coding, **filtering** happens in the adjacent **Filter links** tab (the normal Filter Links pipeline). When **Filter on finish** is **on** in the One-click set-up, completing the run applies these analysis filters to the pipeline: **Factor Frequency** (top `12`, counted by **citations**) → **Link Frequency** (top `30`, counted by **citations**). The global [Label set](../factor-label-set/) controls which `cause`/`effect` columns Recode writes to (no separate “recode suffix” in this panel).

### One-click coding (AI) {#simple-ai-runner}
- Sequencer for the AI pipeline, with one **set-up** modal (see step 1 under [The AI Workflow](../simple-ai/)).
- **Run** starts **Auto-code**; with **more than one** source in scope it continues with **Revise codebook** then **Recode**, stopping on the first non-successful stage. With **exactly one** source in scope, it **stops after Auto-code**.
- One-click uses the same panel prompts/settings as the separate step buttons, while skipping the extra per-step run confirmations after you confirm the one-click set-up modal.
- Optional link deletion is configured **in the modal** (project-wide vs scoped to sources in scope), not only a single “delete everything” confirm.
- **Recode target**: Use the global [Label set](../factor-label-set/) below the Sources bar. Create a new suffix there first if you want Recode to fill `cause_suffix` / `effect_suffix` instead of only the default columns.

### Background (AI) {#simple-ai-background}
- Sets shared project context used by AI coding prompts.
- The status tick indicates whether enough background text is present.

### Auto-code (AI) {#simple-ai-auto-code}
- Runs AI coding across selected/all sources using your prompt and model.
- **Layout (top → bottom):** **Model**, **Skip coded**, **Add source prompt**, and **source limit** row; then the **Prompt sections** editor; then **Advanced** (chunk size, concurrency, temperature, thinking, etc.).
- Use source limit + skip coded options to test quickly and avoid rework.
- **Add source prompt** (switch): when ON, each source’s optional *Source Prompt* (edit above the source text when viewing a source) is prepended to your main Auto-code prompt for that source. Saved per project in the browser. Use when sources need different context; skip when one background prompt in **Background** is enough.
- **Status line** under the settings shows progress, per-chunk detail, and stop — same behaviour as the former “Code with AI” card.
- **Prompt sections**: use **Add section** / **Remove** in the UI to split one saved prompt into reproducible iterations. Internally this is still stored as one prompt with `====` separator lines. Later sections see prior user/assistant turns. Only the last iteration’s result is written to links; all iterations appear in Responses. This is best for workflows where coding is genuinely better in stages, such as first building the network, then adding columns like Time or Certainty, then running a checking pass.
- **Rerun from here**: each prompt section has a small rerun button. Use it to continue a stable multi-section prompt without paying again for earlier successful stages, not as an open-ended chat workflow for coding maps. Section 1 reruns normally. Later sections reuse the latest successful earlier iteration history only when the earlier source text, prompt sections, chunk bounds, and Holistic setting are unchanged; otherwise the run fails loudly. You can add new sections under a successful run and rerun from the first new section.
- **Holistic first pass**: when enabled, only the first iteration asks the model for a Mermaid causal network with quote-backed edge labels. The server parses that Mermaid into the standard links JSON format before passing it to later iterations or saving final links. If the Mermaid cannot be parsed into links, the run fails loudly.
- **Confirm** before a run shows model, chunking, word count, and cost estimate. **Stop** cancels after current chunk tasks finish.
- Timeouts scale by model and iteration count (cap ~540s total). **Concurrency** (1–5) is in Advanced; raise for speed, lower if you see 429/timeouts.
- [Tips on using the prompt history](../tips-prompts/) (same chrome as other prompt fields).
- Default model is **Qwen Flash**.

#### Holistic first pass (Auto-code) {#simple-ai-auto-code-holistic}
- **What it does**: keeps Auto-code on the normal single `process_chunk` route, but changes iteration 1 so it asks for a connected Mermaid causal network before converting that network to standard links JSON in code.
- **When to use it**: helpful when asking directly for a links table gives fragmented networks and you want the first pass to reason about the whole causal story.
- **Switch**:
  - **ON** = iteration 1 uses Mermaid instructions, then server-side parsing converts the result to links JSON.
  - **OFF** = all sections use the standard links JSON instructions.
- **Extra columns**: if your prompt asks for extra columns such as sentiment or mood, the Mermaid edge labels must include them as safe `key=value` fields. The parser writes those fields into the resulting links.

### Revise codebook (AI) {#simple-ai-revise-codebook}
- Suggests a cleaner consolidated codebook from existing links.
- Use this after you have enough coded links for a representative sample.
- Header tick indicates whether the Recode codebook area currently has content.
- **Target clusters**: see [Target clusters](../simple-ai-target-clusters/).
- Optional **Use automatic pre-clustering** switch (default OFF).
- With pre-clustering OFF, the AI clusters the factor list directly from the Revise codebook prompt. That prompt supports `[number]` / `[cluster_count]`.
- With pre-clustering ON, embeddings are used first to group labels semantically, then the AI only has to label those grouped clusters. This is a bit more systematic, less dependent on the AI doing all clustering internally as a black box, and may help preserve unusual or divergent concepts.
- Pre-clustering also adds a **Representatives per cluster** slider (8-20, default 8) and uses a separate labelling prompt.
- Default model is **Gemini 3 Flash Preview**.

#### Target clusters (Revise codebook) {#simple-ai-target-clusters}
- The **Target clusters** control is a slider with **50 positions**. The **far left** is **Default**; moving right sets an explicit target of **2** through **50** clusters (one step per cluster count).
- **Default** (far left): the app derives a target count \(K\) from the number of **unique factor labels** \(n\) in the **current filtered pipeline** (same scope as Revise codebook): \(K = \min(\lfloor n/3 \rfloor, 25)\) — at most **25**, or roughly **one label in three** as clusters, whichever is smaller.
- **Explicit** positions (not Default): the requested \(K\) is the number shown by the slider (**2**–**50**). If \(K\) is **greater than** \(n\), the run uses **\(n\)** instead (you cannot have more clusters than distinct labels); the app may show a short notice when that cap applies.
- Pre-clustering, embedding clustering, and `[number]` / `[cluster_count]` in prompts all use this **effective** \(K\).

### Recode (AI) {#simple-ai-recode}
- Applies your codebook back onto existing links, turning raw factor labels into cleaner synthesised ones.
- The **Recoding** radio buttons map onto the kinds of recoding (see [Different kinds of coding and recoding](https://garden.causalmap.app/kinds/)). Overall the four run in order of **increasing cost and increasing quality**, left to right: Magnetic, then AI factors, then AI links, then Hard. Pick the cheapest one that is good enough for your data.
  - **Magnetic** (soft recoding): embedding similarity to codebook lines, the same magnet machinery as the pipeline's soft-recode path, with a similarity threshold. No AI call, and only as good as the embedding space.
  - **AI factors** (factors recoding): the model relabels each unique factor label to its best-matching codebook line. You can bring other factor columns into play (citation count, source count) when you write the instruction.
  - **AI links** (links recoding): the model relabels each link from its cause, effect and the actual quote, so it decides with much more context, almost like recoding from scratch. This is the default.
  - **Hard** (hard recoding): re-codes the source text from scratch against the codebook rather than relabelling existing links. Pick the sources (**Coded sources**, the ones already coded, or **All sources**), confirm, and it re-runs AI coding with the codebook as a closed list (the default instruction forbids inventing labels; your own instruction may relax that), replacing those sources' links. It uses the Auto-code model and chunk settings.
  - The names refer to the mapping method, not "soft recoding" in the filter sense.
- **Watch the batch size**: with a large set of links and long quotes, a recode run is split into multiple calls, and each call can settle on slightly different labels. If you want a small fixed set of top-level labels, develop them first with Answers mode or the Cluster part of the Soft Recode filter, then recode against that codebook. <!--- AI factors reuses scoreFactorsBatchForRelabel (label to label rename map); AI links reuses scoreLinksBatchForColumns with canonicalColumns ['cause','effect'] and the codebook in the query, writing each link's cause/effect directly, both into the active label set. Hard reuses aiManager.processSelectedSources with sourceIdsOverride + bypassSourcesLimit + disableSkipCoded and a promptOverride that appends the codebook; channel rag_ai_simple_hard_recode (#ai-simple-hard-recode-prompt). -->
- **Recode target**: the global [Label set](../factor-label-set/). The default set writes the standard cause/effect labels; a named set writes that set's own cause and effect columns instead, leaving the default pair untouched.
- Supports sampled recoding and skip-recoded behavior (skip-recoded only applies when using a non-default label set).
- Header bar shows recode coverage mix across all cause/effect recoded fields.
- Default model is **Qwen Flash**.

### Filter links (AI) {#simple-ai-filter-links}
- This is the same Filter Links workflow, run from the adjacent **Filter links** tab (not embedded in the AI Coding panel).
- Use it to refine/select links before reviewing outputs on the right.
- When **One-click coding** finishes with **Filter on finish** enabled, the app applies top-12 factor frequency (citations), then top-30 link frequency (citations) (no longer injects the deprecated Temporary Factor Labels filter).

### Advanced Settings
Each section header is clickable and opens/collapses its settings panel. Section headers also include contextual **Help** buttons. The advanced sections are inline (not flyouts), and only one section is expanded at a time.

Inside advanced panels you can:
- Edit the exact **Prompt** the AI uses.
- View your prompt history and load previous prompts.
- Change the **AI Model** (e.g., switch to a "Pro" model for complex reasoning, or a "Flash" model for speed).
- Tweak technical settings like chunk size, concurrency, and temperature.

<!-- 
TECHNICAL DETAILS FOR DEVELOPERS:
- State & CSS: The AI Coding panel (`#ai-simple-panel`) is rendered statically at the top of the **Create links** tab (`#create-link-content`). There is no mode toggle and no `<body>` class; AI as a whole is gated by the Account switch `#account-ai-enabled-toggle`.
- Layout: Left pane, Sources bar (`#sourcesHeader`), the `#link-tabs` (Create / Filter / Assess) and the RHS tabs all stay visible; the panel does not hide or relocate them.
- UI Components: Uses `.ai-simple-section` accordion sections with clickable headers (`setupAiSimpleHeaderCollapse` in `app.js`). Help buttons on each header call `window.helpManager.openToSection(...)`. **One-click coding** open/refresh: `confirmEasyAiCodingRunAll` + `wireEasyAiSetupModalLive` in `app.js` (`#confirmation-modal` is `modal-lg modal-dialog-scrollable`; custom tooltips need `z-index` above the confirm modal’s raised stacking — see `.custom-styled-tooltip.modal-context` in `styles.css`).
- Filter integration: Filtering uses the normal **Filter links** tab (`#filter-link-content`); it is no longer relocated into the AI panel.
- Data Fetching: The coded % bar is updated by `updateAiSimpleCodedPct()` in `app.js`, which calls `DataService.getSourceCodedCounts(projectName)`. It listens to `projectSelected` and `linksUpdated` events via the EventBus.
- Prompts: the textareas in the advanced panels are fully wired into `PromptHistoryService`, sharing the same history/expand-to-editor logic as the main AI panels. Allowed `public.prompts.type` values are enforced in Postgres; field→type mapping lives in `DataService._promptHistoryFieldToDbTypeMap()`. Auto-code with **Holistic first pass** stores history under `ai_holistic` (`aiHolisticPrompts`); standard Auto-code stays on `ai` (`aiPrompts`).
- Prompt history UI (single pattern): shared markup/tooltips in `js/prompt-history-chrome.js` (`promptHistoryChromeHtml`, `fillPromptHistoryChromeHosts` on boot in `app.js`). Filter-bound widgets register **only** via `FilterPipelineManager.syncFilterPipelinePromptHistoryWidgets()` at the end of `renderFilterPipeline` (not from tabs or ad-hoc hooks). See `webapp/architecture-rules.md`.
- Definitive prompt-history spec:
  - On load, bind to the newest saved version.
  - While editing, if text differs from the newest saved text, show an unsaved state.
  - On Save or Run, if text differs from newest, save a newer version.
  - If the source version has an unchanged admin custom series name, name the new version `name-vN`; otherwise use the fallback timestamp name.
- Extra constraints:
  - Prompt history is DB-backed, not URL-backed.
  - If text equals newest, do not create another version.
  - Admin name metadata must save reliably or fail loudly.
- AI subscription gating: `AIManager.applySubscriptionGating()` only clears `disabled` on controls marked `data-ai-subscription-gated` when the user gains AI access, then calls `updateAiSimpleSectionsState()` so Auto-code / Revise / Recode rules stay correct (targets `#ai-simple-panel` primary actions, not help buttons).
- If a real edge case appears (e.g. must wire a filter before the first pipeline render), we can **add a targeted hook back** — but document it next to this bullet and prefer extending `syncFilterPipelinePromptHistoryWidgets` first.
- Safeguards: If a user tries to Auto-code >100K tokens but has coded <10% of their sources, `ai-manager.js` intercepts the action and injects a warning into the `showAIConfirmModal` to prevent accidental massive spends on untested prompts.
- Recode: Uses `scoreFactorsBatchForRelabel` with `codebookLines`. When codebook is provided, the AI returns `{"mappings":[[row,codebook],[row,codebook],...]}` (1-based indices; 0 = no match) instead of full label text. Fewer tokens, easier for models. ai-answers factor-by-factor (no codebook) still uses the full label/new_label format.
- Target clusters: `RAGManager.getAiSimpleFactorClusterSliderState()`, `computeDefaultTargetClusterCount`, `_clampAiSimpleClusterCountToFactors` in `rag-manager.js` (`#ai-simple-factor-cluster-count-slider`). Not persisted in URL/bookmark state.
-->