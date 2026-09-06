The [yellow button in the navbar](../navbar-bookmark/) is the fastest way to save useful views of your current project: maps or tables. 
From that one entry point you can quickly save views, update existing bookmarks, and copy links, images, legends, or a combined HTML block (link + image + legend) for reporting.

### Report views (admin) {#report-views}

<span class="badge bg-secondary" style="margin-left:6px;">Admin only, in testing</span>

The **Report views** button in the Reports toolbar builds a standard set of maps for the current project in one press: an **Overview** (top 12 factors, top 30 links by citations), **What most people say** (counted by how many people mentioned each factor and link, so one talkative respondent cannot carry them), and a **Headline** map of the few factors and links that dominate. Each is saved as a bookmark with a screenshot, and the slideshow opens on the three of them.

No AI is involved. The views come from a fixed list, so the same project gives the same three maps every time, and each one can be explained by the filters that produced it. Pressing the button again replaces the previous set rather than adding to it.

<!--- Maintainer notes. The catalogue is `js/report-recipes.js`: each recipe is a literal `filterPipeline.filters` array, so recipes are added there and nowhere else. The runner is `ReportBuilder.runReportRecipes()` in `js/report-builder.js`; it reuses `renderLinksAndWait` (a forced `_doUpdateGraph`, needed because the map skips repaints behind the signature gate and while its tab is hidden) and restores the user's prior view by replaying the whole original search string through `urlState`. Generated bookmarks are marked with `slide_content.generated` (there is no metadata column on bookmarks). Each run now files its slides in its own dated deck (`deck-rules.reportDeckName`) and leaves earlier decks alone, so the old rerun sweep by generated marker no longer deletes the previous set. Button visibility is `ReportBuilder.applyRecipesButtonVisibility()`. --->


The bookmarks table itself is not shown for users below Pro level, i.e. to users only on Free or Private plans. 

### AI report deck (MapCat) {#mapcat-report}

<span class="badge bg-warning text-dark" style="margin-left:6px;">Requires AI plan, Edit my data with AI on</span>

Ask [MapCat](../map-cat/) to build a report, slides or a deck and it reviews your project data, asks a few preference questions in chat (tables, groups, sentiment, disagreement, quotes, and so on), then builds a slide deck of the strongest views, each with short written commentary. It can open the deck in a slideshow over the chat.

- The first deck defaults to about five slides so it lands fast. Read it, then ask MapCat to extend it or build a fuller version.
- MapCat keeps the stronger of any two views that would read the same (for example a top-factors map and a top-links map over the same filter), so you do not see near-duplicate slides.
- Each view is saved as a bookmark, so you can reorder, edit or export the deck from the [Bookmarks table](../bookmarks-panel/). MapCat can also retitle or delete a slide and export the deck as a PDF on request.
- Every run makes its own [deck](../decks/), named for the date and time it ran, and leaves the previous run's deck standing so you can compare two reports. Delete the old one from the deck menu when you are done with it, since the slides and their screenshots stay until you do.

<!--- run_one_click_report / list_report_slides / edit_report_slide / delete_report_slide / export_deck / show_canvas verbs in docs-bot-manager.js; deck built by report-builder.js. Variety doctrine (48498073), short-first maxSlides default (48eedb15), live-review quality gates (4efea48f: focused disagreement, group-size floor 3+ sources/10+ links, story dedupe, citation-ranked factor table). See docs/plans/one-click-reporting-next-steps. --->

### Decks {#decks}

A deck is a named, ordered list of slides. A slide is a bookmark, so any view you have saved can go in one, and the same slide can sit in several decks at once: a map can be in both **Client A** and **Full report** without being copied.

The deck menu sits at the left of the Reports toolbar. **All slides** is the first entry and is not a deck at all: it means every slide in the project, and it cannot be deleted or renamed. Below it is one entry per deck with its slide count. Tick more than one and the list shows the slides in any of them.

Pick a single deck and four more buttons appear, because they only mean something for one deck at a time.

- **Show deck** opens it as a slideshow, in the deck's own order.
- **Remove from deck** takes the ticked slides out of it. The slides themselves are kept and still show under All slides.
- The pen renames the deck, and the bin deletes it.

To build one, tick the slides you want and press **Add to deck**. Type an existing name to add to that deck, or a new name to make one. Slides go on the end, and a slide already in the deck stays where it is rather than jumping to the bottom.

**Order.** Drag a slide by its handle to move it. Inside a deck the drag sets that deck's own order and nothing else changes; under All slides it sets the project-wide order you see when no deck is picked. The two are independent, so reordering a deck for a client does not disturb anything else.

**Saving into a deck.** While a single deck is selected, any bookmark you save from the navbar button is added to it. Switch back to All slides to save without filing anything.

**Deleting a deck** asks which of two things you mean:

- **Delete the deck, keep the slides.** The deck goes, every slide stays in the project under All slides. This is the safe one.
- **Delete the deck and its slides.** The slides are deleted for good. Version snapshots restore links and sources, never slides, so there is no undo. If the deck holds slides somebody else saved, those cannot be deleted and the message says how many were left behind.

**Viewing one slide.** The expand icon on any row opens that slide full screen, with the rest of the list either side, so you can page on from there.

**Comments at the side.** A slide can put its commentary in a column beside the picture instead of in a floating panel over it. Ask MapCat for a slide "with the comments at the side" and it sets the layout for you.

**What MapCat can do with decks.** Ask it to list your decks, make one, add or remove slides, show a slide, or delete a deck with or without its slides. Taking a slide out of a deck and deleting the slide are different requests and MapCat treats them differently, so say which you mean.

<!--- Maintainer notes. Decks are `public.decks` + `public.deck_slides` (migration 20260831120000), replacing the single `bookmarks.deck_name` column, which is dropped in a follow-up migration once the backfill is checked. Membership and per-deck order live in `deck_slides`; `bookmarks.slide_order` remains the project-wide All-slides order. Pure decisions (name tidying, renumbering, both reference resolvers, the delete plan, the report deck name, layout normalising) are in `js/deck-rules.js`, tested in `tests/decks.test.mjs`. The UI is owned by `report-builder.js` alone; `bookmark-manager.js` follows the selection through the `deckSelectionChanged` EventBus event so a bookmark saved while a deck is filtered joins it. RLS mirrors bookmarks through `can_view_project_bookmarks` / `can_edit_project_bookmarks`, with one difference: any project editor may edit any deck, since a deck is project furniture rather than a personal row. Verbs `list_decks` / `add_slides_to_deck` / `remove_slides_from_deck` / `delete_deck` / `show_slide` in mapcat-directives.json. --->

### Bookmarks Panel {#bookmarks-panel}

In this section you can learn about bookmarking and how to manage bookmarks.

<span class="badge bg-warning text-dark" style="margin-left:6px;">Requires Pro subscription</span>

<div class="user-guide-callout">
<strong>🔖 What you can do here:</strong> Save and organize your favorite views of your data. Bookmark specific filter combinations, map layouts, or analysis states so you can quickly return to important insights later, share clean links, and build reports from saved views.
</div>

To create a bookmark from anywhere, use the [Navbar bookmark button](../navbar-bookmark/). This adds a bookmark to the [Bookmarks table](../bookmarks-table/).

After saving, the navbar bookmark button briefly shows a green tick to confirm the save.

When you save a bookmark in the session, 
- a small popover opens near the button with a Description textarea and a **Save** button (description is optional, but useful).
- inside **Existing bookmarks**, you can pick a bookmark and **Overwrite** it with the current screen state (keeping the same bookmark number/link).
- each bookmark can then be used to copy:
    - a short plain link (`?bookmark=ID`)
    - a formatted link (HTML)
    - the bookmark image
    - combined HTML that includes the bookmark link, image, and legend



#### The Bookmarks Table {#bookmarks-table}

Use the full table / report workflow when:
- you want to work across different projects
- you need more detailed tools for managing many bookmarks
- you want to build a full report from some or all bookmarks

- Each row is one bookmark.
- Click the checkbox  to select rows.
- Click Load  to recall that bookmark, restoring tabs and outputs.
- Quick load: at the very top of the Bookmarks / Reporting tab, you can type a bookmark number and press **Load** (or Enter) to load it directly.
- Click Copy Formatted Link  to copy the bookmark's URL to the clipboard.
- Double-click on the Description field to edit it.
- Click Delete  to remove the bookmark.
- Click **Show slideshow** to present the loaded bookmarks in their table order. The slideshow opens in a large modal with previous/next controls, left/right keyboard navigation, a title slide, bookmark actions, and a **Load bookmark** button.
- Use **Share** next to **Show slideshow** to copy a link that opens the current project directly in slideshow mode. If the link includes `bookmark=ID`, that bookmark is opened first.
- Turn on **Hide from slideshow** for any bookmark that should remain in reports but not appear in the slideshow. This is saved with the bookmark.
- Click the badge at top right  when viewing a map or table to add a new bookmark to it.
- When a new current project is loaded from a URL or by changing the project dropdown, the "Project" filter in the table is pre-filled with the name of the current project.

**Main Features:**
- **Bookmark badge** <i class="fas fa-star"></i> - Save/remove current URL state from navbar
- **Bookmarks table** - Manage saved views with sorting and filtering
- **Bulk operations** - Select multiple bookmarks for deletion
- **Editable descriptions** - Double-click to edit bookmark names
- **Auto-normalization** - URLs cleaned and standardized for consistency

**Bookmarks Table:**
- **Actions** - Load URL, Copy link (plain), Copy formatted link (HTML), Edit URL, Delete individual bookmarks
- **Copy buttons** - Both create short `?bookmark=ID` URLs instead of full parameter strings
- **Columns** - Project, Description (editable), User, URL, Created, ID
- **Bulk delete** - Select multiple with checkboxes, delete with "Bulk:" trash button
- **Badge integration** - Shows bookmark ID when current view is bookmarked

**URL Editor:** 

Click the Edit button <i class="fas fa-pencil-alt"></i> next to any bookmark to open the URL Editor. You can edit the bookmark description (Markdown supported). The editor also provides a user-friendly interface to understand complex bookmark parameters. Instead of viewing raw query strings, you see a structured breakdown with proper labels and grouping - showing your selected project, sources, active filters (displayed as individual cards), table settings, and map configurations. The editor categorizes parameters into logical groups (Navigation, Data Selection, Filters & Processing, etc.) and displays filter pipeline details with sequential numbering and status indicators. This makes it easy to understand exactly what state each bookmark preserves without needing technical knowledge of URL parameters.

<!---

**Complete state preservation** - Your entire analysis view is saved in the URL for easy bookmarking and sharing.

**What gets saved:**
- Active tabs and panel selections
- Window layout (pane width)
- Selected project and sources
- All filter pipeline settings
- Custom column configurations
- Table states (sorting, pagination, filters)

**Smart filtering** - Only saves filters that differ from defaults to keep URLs clean and readable.

**Bookmark URL format** - Copy link functions create short URLs with `?bookmark=ID` parameter instead of long parameter strings. When visited, the system automatically loads the bookmark's full state.

**State restoration** - Page reload restores your complete analysis exactly as you left it.

When copying a formatted or unformatted URL using the File menu, the app copies the short form using the bookmark ID (e.g., `?bookmark=abc123`), and the URL state handler loads the full state from that ID.


**Bookmarking Support:**
Application state is preserved in URL parameters for:
- Active left and right tabs
- Left pane width
- Selected project and sources
- Filter pipeline configuration
- Custom column settings

**State Persistence:**
- URL serves as primary state storage
- LocalStorage provides secondary backup
- All sliders and interface controls included
- Table filter states, column sorting and pagination preserved
- Page reload restores complete application state

Filters are saved to the URL only when:
- They are enabled, and
- They differ from their default settings.
Disabled/inactive/default filters are omitted, keeping the URL clean.

**Bookmark Parameter Handling:**
- URLs with `?bookmark=ID` automatically redirect to the bookmark's full URL before app initialization
- File menu copy functions create short bookmark URLs instead of full parameter strings
- Bookmark IDs are used as display text in formatted links (e.g., `#abc123`)
- Page reload ensures proper widget initialization with complete state
- Provides clean, shareable URLs while preserving complete application state
- Backward compatible - existing full URLs continue to work normally
-->


#### Building reports from the Bookmarks table {#report-builder}

The Bookmarks table lets you create professional reports by combining multiple bookmarked views with custom descriptions and variant filtering.

<span class="badge bg-warning text-dark" style="margin-left:6px;">Requires Pro subscription</span>

<div class="user-guide-callout">
<strong>📊 What you can do here:</strong> Build multi-slide reports from your bookmarks. Add markdown descriptions, choose variant fields/values from your current filtered data, reorder slides, and export as formatted HTML or PDF. This is useful for producing stakeholder-ready outputs from saved app views.
</div>

**Key Features:**
- **Drag-and-drop reordering** - Arrange slides in any order
- **Markdown descriptions** - Add rich text titles and explanations with heading styles, lists, and formatting
- **Variant generation** - Create multiple versions of the same bookmark view filtered by selected field values
- **Include/Exclude toggles** - Selectively include slides in your export
- **HTML/PDF export** - Copy formatted HTML or export PDF with clickable bookmark links and legends
- **Persistent settings** - Your slide order, descriptions, and include/exclude states are saved automatically

Legends:
- For maps we use the full legend
- For tables we use the relevant parts of the legend, omitting material about link and factor colours, sizes and annotation. 

Variants:
- Variants simply add an extra filter on top of the bookmark’s existing filters (sources + filter pipeline). We do not change any other filters. For example, if the bookmark has 4 selected sources and you choose village=X and Y, then the X variant uses only those of the 4 sources with village=X, and the Y variant uses only those with village=Y. If a value has no data after the existing filters, no variant is produced.  


Where to find the variants: when the accordion section is open, the variants appear as thumbnails above the main bookmark image, each preceded by which variable/value it represents (e.g., village: Y). On PDF export and copy to clipboard, first the original bookmark image and its legend are shown, and then each variant with its fullsize image and legend.



**How to use:**
1. Create bookmarks of your maps and tables
2. Switch to the Report tab (yellow bookmark icon)
3. Click on slide descriptions to edit them (supports markdown: `# Heading`, `## Subheading`, `- List items`)
4. Drag slides to reorder them
5. Use the variant controls to generate multiple versions filtered by selected field values
6. Toggle "Include/Exclude" to control which slides appear in your export. **Hidden from slideshow** bookmarks are also skipped by Copy HTML and Export PDF.
7. Click "Copy HTML" (or "Export PDF") to export all included slides
8. Paste into Word/Google Docs - headings and links will be preserved

<!-- Technical: Report Builder is implemented in bookmark-manager.js as the ReportBuilder class. It loads bookmarks with their screenshots, allows inline markdown editing with live preview, stores settings in slide_content.report_settings JSONB column, and generates Word-compatible HTML with proper semantic heading tags. Variant metadata is collected from sources.metadata.custom_columns. -->