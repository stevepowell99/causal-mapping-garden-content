Hints are small popovers that help you discover features. They never appear on their own timer: you see one only when you ask (the lightbulb button in the navbar), after certain first-time actions, or when MapCat points you at a relevant control.

- Hints are **tied to specific UI elements** (buttons, inputs, panels).
- Hints are **capability gated** (you won’t see hints for features your plan doesn’t include).
- When the **Link Editor (causal overlay)** is open, you only see **overlay-specific hints**.
- Repeated lightbulb clicks walk the current panel's hints in a **deterministic sequence** (so you don’t keep seeing the same ones at random).
- **Don’t show** turns hints off permanently; the lightbulb still shows them on demand.

<!--
TECH NOTES (Hints system)
- Data: `webapp/hints/hints.json` (array of hint objects).
- Each hint:
  - `id` (string, unique)
  - `priority` (int, higher = earlier/more likely)
  - `title`, `body` (strings)
  - `target`: `{ selector?: string, elementId?: string }`
  - `helpAnchor` (string, README anchor to open on "Learn more")
  - `requiresCapabilities` (array of capability keys, checked against `window.capabilities`)
  - `context`: `overlayOnly` (shown only when `#causal-overlay` is open)
- UI: Bootstrap Popover, `customClass: 'hint-popover'` (styles in `webapp/css/styles.css`).
- Placement: Popper.js config in `webapp/js/hints-manager.js` with extra top/bottom offset; overlay footer gets larger vertical spacing.
- Rule: hints never change app state (no auto-switching tabs/collapses to reveal targets). If target isn't visible OR is covered by something else (`document.elementFromPoint` at its centre, e.g. an open modal), hint is skipped.
- No ambient timer: hints show only via the navbar lightbulb (`showNextRandomHint`), event-driven teachable moments (`showHintById`), MapCat (`showHintForQuery`), or arrow-key history. The old random 2-4 minute scheduler was removed July 2026 (it fired hints into modals and mid-task).
- Deterministic sequencing (per session):
  - When overlay is open: scope `overlay`
  - When a right-panel tab is open: scope `tab:<tabKey>` (per-panel walk order in `PANEL_HINT_ORDER`, hints-manager.js)
  - Stored in sessionStorage: `cm_hints_seen:<scope>`
- Keyboard: Left/Right arrows step back and forward through hint history, but ONLY while a hint popover is open (`hintsManager.isOpen()`), and never when focus is inside a Tabulator. Bare arrows must stay free for grid/map navigation: an app-wide binding fired a hint on every arrow press in a table, and its `force: true` bypassed "Don't show".
- Suppression: "Don't show" is permanent, stored in localStorage `cm_hints_suppress_all` (`'1'`); a legacy `cm_hints_dont_show_count` >= 1 also counts. Explicit pulls (lightbulb, arrows, teachable moments) pass `force: true` and still work.
- Admin simulation:
  - Navbar "Hint" button shows a hint using the currently selected capability simulation profile (radio group in the dropdown).
-->

<!---
Bookmark links: You can add `[foo](bookmark=173)` to load a bookmark without URL refresh (same behavior as the Bookmarks tab buttons). Above `.help-drawer-content`, Previous and Next buttons let you navigate back and forward within the help drawer history after following internal links.

The old hard-coded glow mapping has been removed. The rule now is simple: internal anchors control both help navigation and UI glow. Example: `[Projects dropdown](../project-selector-dropdown/)` opens the section and glows the dropdown.

Standalone help: 
- make it also treat multiple words as OR except when in quotes
- drop the scrolling and orange highlighting. Keep the "Showing n results for foobar" but just add ", scroll to see them"

In the in-app help, clicking an internal link moves to that section and also "glows" the corresponding UI element. 
In the standalone help, clicking an internal link only moves to that section and shows a notification: "Try the interactive help within the app which also shows you the individual components." Clicking bookmarks like this [here](bookmark=176) opens the app in a new named tab.



### <i class="fas fa-question-circle"></i> Features common to Help Drawer and Standalone Guide

- Initially shows only H1 and H2 headers
- Clickable sections expand to show full content
- Anchors: Grey anchor/link symbols appear on hover for easy link copying

### Search Features

**Search Box:**
- Located at top of help drawer for quick access
- **Enter key** or **Search button** to execute search
- **Light green styling** consistent with app design

**Search Logic:**
- **Multiple words**: Treated as OR logic - either word will match
  - Example: `filter map` finds sections containing "filter" OR "map"
- **Quoted phrases**: Exact phrase matching when enclosed in quotes
  - Example: `"filter pipeline"` finds only sections containing that exact phrase
- **Fuzzy matching**: Handles typos and partial matches

**Search Results:**
- **Automatic expansion**: Only matching sections are opened
- **Yellow highlighting**: All matching terms are highlighted in results
- **Clean state**: Previous highlights cleared between searches


### <i class="fas fa-question-circle"></i> Standalone Guide

Uses the same advanced search system as the help drawer for consistency and DRY principles.

### <i class="fas fa-question-circle"></i> Help Drawer



**Features:**
- <i class="fas fa-times"></i> Reset function closes all sections when opened via contextual help



### Contextual Help Buttons

Context-sensitive help system accessible via <i class="fas fa-question-circle"></i> button next to logout. Opens drawer sliding from right (1/3 window width) displaying README content in collapsible tree structure.

<i class="fas fa-question-circle"></i> Question mark icons distributed throughout the interface provide section-specific help:
- Opens help drawer if closed
- Navigates directly to relevant documentation section
- Resets drawer state before showing targeted content

**Panel Integration:**
When help sections or internal links reference UI elements, the system automatically:
- Activates required containers so the target is visible: Bootstrap tabs, collapses, dropdowns, and toggleable cards (card bodies hidden via `style="display:none"` with `*-toggle-btn` buttons)
- Glows the UI element (never the help element). Cards like `#map-formatting-card`, `#vignette-card`, and AI `#ai-simple-widget` auto-open before glowing.

--->