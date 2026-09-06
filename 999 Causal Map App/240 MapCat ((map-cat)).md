MapCat is the small chat helper at the bottom-right. **MapCat is available to all users**, even if you do not have an AI subscription or if AI is disabled in your account settings. It is the only AI feature that does not require a subscription or for AI to be enabled, because it does not see your project data.

### What MapCat is for

MapCat answers questions about the app and about causal mapping while you work. With **Edit my data with AI** on and a project open (AI plan), it also works alongside you: you can ask it to do things and it carries them out, showing a confirm step before any change.

Without that switch on (the default), you can:

- Ask how a control, panel or workflow works.
- Ask it to open help, highlight a control, or switch tab.
- Read its nudge when the cat wiggles: it has a suggested next step.

With **Edit my data with AI** on and a project loaded, you can also:

- Ask questions about your own data: your factors, sources and links, or what a filtered view holds.
- Set what you want to find out and let MapCat hold that aim across the chat.
- Run AI coding by chat. MapCat asks a couple of plain questions about how you want the sources coded, then starts the run for you, so you do not need the settings screen. It shows the conventions it chose in a coding-decisions summary before the run.
- Build a report. MapCat asks what it should cover, builds a slide deck, and can open it in a slideshow over the chat (see [AI report deck](../mapcat-report/)).
- Ask about your findings, and MapCat answers by running a report view and telling you what it shows.
- Change map, filter and pivot settings, and edit links and sources, by asking.
- Have MapCat build a view and save it as a bookmark for you, so you can ask for a set of maps in one go and come back to each one later.
- Ask it to reopen a saved bookmark, change something about it and save it back, so a set of views can be corrected without rebuilding each one by hand.

Every change shows a confirm step first, so nothing happens to your project until you approve it.

<!--- Capability-level summary of the guided front end. Mechanics (verbs, tool-loop, model routing, admin Haiku/Sonnet/Opus/Flash toggle) are in the TECH NOTES (MapCat) block below and in docs/plans/mapcat-*. The guided coding/report flow is driven by set_project_aim / run_one_click_coding / set_ai_coding_fields / run_one_click_report. Keep this list capability-level, not verb-level. --->


### Header controls (top of MapCat panel)

- **Window controls** (group of 3 icons):
    - **Maximize icon**: open MapCat in large centered mode.
    - **Restore icon**: dock MapCat in the normal bottom-right position.
    - **Minus icon**: minimize back to the cat chat-head button.

### Footer controls (bottom of MapCat panel)

- **Contact support**: sends the latest question/answer context to support.
- **Edit my data with AI** (AI plan only). The switch was called **Superpowers** until August 2026; the name changed because ticking it is your consent to send this project's data to the AI, and the old name said nothing about that.
    - Default is **OFF** (safe mode).
    - When OFF, MapCat can still answer documentation questions and use non-data UI helpers (for example help/hints/tab switching).
    - When ON, MapCat can run data-aware actions (for example sources selection, filter pipeline edits, pivot config), which means project state data is sent to the AI. It can also change your project, and every change asks you to confirm first.
- **Clear**: clears MapCat chat history.
- **Send**: sends the current prompt.

### Privacy and data-sharing behavior

- With **Edit my data with AI** OFF (default), MapCat runs in safe mode intended for users who do not want project data sent for AI actions.
- With **Edit my data with AI** ON, MapCat may send project-derived context needed to execute data-aware requests (such as source IDs, filtered link/factor context, and related view state) to the AI service.

### Safety rules

- UI actions are whitelist-only.
- Project deletion actions are explicitly blocked (`delete/remove/destroy/drop project`) even if requested by a tool directive.

<!--
TECH NOTES (MapCat)
- UI: `#docs-bot-toggle-btn` + `#docs-bot-panel` in `webapp/index.html`; styles in `webapp/css/styles.css`.
- Runtime: `webapp/js/docs-bot-manager.js` (chat, nudges, persistence, support handoff).
- Nudge copy source: `webapp/mapcat-nudges.md` (`### <nudge_id>` sections).
- Nudge cooldowns: global 10 minutes (`_nudgeCooldownMs`), same nudge 48 hours (`_sameNudgeCooldownMs`).
- Chat model: admin toggle (`#docs-bot-model-select`) picks Haiku / Sonnet / Opus (Claude, EU via Vertex rawPredict) or Flash (gemini-3.5-flash, EU via the `vertex-ai` edge function's chat-translation branch). Default Sonnet; Haiku is forced for accounts without an AI subscription. Resolved in `_getSelectedModel()`. Distinct from the coding/recode models, which always run Gemini Flash.
- Tools (Edit my data with AI ON + a project loaded): the agentic loop in `submit()` offers three read tools plus the write verbs. `query_project` (pure module `webapp/js/mapcat-query-tool.js`) queries links/factors/sources client-side over cached golden links. `read_app_state` returns the full untruncated value of a topic registry (`_stateTopics()`: coding_prompt, project_aim, coding_settings, filter_pipeline, selected_sources, last_run_prompt, view_extract). `consult_coder` forwards a coding-judgement question plus the passage to the production coding model (gemini-3.5-flash) under the project's live coding prompt, so coding-convention verdicts come from the coder, not the chat model — the system prompt tells the chat model to delegate rather than adjudicate. Write verbs (`_buildMapCatVerbTools`) are Claude-only native tools; on Flash they fall back to the `[[MAPCAT_TOOL:...]]` text protocol.
-->