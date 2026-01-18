# Changelog

All notable changes to KlipCeeper will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.3.0] - 2026-01-18

### Highlights

🎹 **Smarter Keyboard Hints** — The hint dock now shows context-aware shortcuts.
Enter reorder mode and see ↑↓/Enter/Esc instead of the default shortcuts.

📋 **Richer Annotation Export** — Exports now include textQuote selectors,
notes, and entity IDs for better RAG pipeline integration.

🔗 **Quick Source Navigation** — Click any domain pill to jump directly
to the source URL.

### Features

- **Contextual keyboard hints**: Modals and reorder modes push their own
  shortcut hints, so you always see what's relevant
- **Delete empty topics**: Clean up unused topics directly from the dropdown
- **DOM-aware capture**: Smarter text extraction with automatic plaintext fallback
- **Popover system**: New fixed-position popover with auto-dismiss

### Fixes

- Command palette now shows all topics and has unified focus behavior
- Annotation toolbar closes properly on click-outside
- Storage fixes prevent orphaned items and annotation loss
- Design tokens replace hardcoded colors throughout

### Polish

- Light theme and expanded sidebar as new defaults
- Tighter editorial feel with visual refinements
- Restructured CSS architecture for maintainability
- Removed unused Active filters section from left sidebar

---

## [0.2.0] - 2024-12-23

### Added

- **Right Rail Topic Filter** — New `/` shortcut opens a right rail panel for filtering within current topic by search query, annotation type (highlights/notes/entities), and domain
- **Right Rail Keyboard Model** — Full keyboard navigation in filter rail: Up/Down to navigate filters, Space/Enter to toggle, Escape to close
- **Filter Badge** — "Filtered" badge appears in topic strip when filters are active and rail is closed
- **Value Signal Badges** — Cards now show highlight/note/entity counts in metadata
- **Enriched Cards in Cmd+K** — Topic switcher palette shows cards with their annotations
- **Lens Switcher** — Replaced dropdown layout picker with segmented Curate/Read lens switcher
- **Shared Card Header Renderer** — Unified card header primitive for consistent hierarchy
- **Topic Search Service** — Clean abstraction layer for topic-local filtering

### Changed

- **Shortcuts Cheatsheet** — Refreshed labels, descriptions, and priority ordering:
  - Switch topic (⌘K), Global search (⌘⇧K), Topic filter (/)
  - Next/Previous card (j/k) now priority 90/89
  - User-facing labels (no internal terms like "palette")
- **Filters Scoped Per Topic** — Switching topics now clears rail filters
- **Layout Grounding** — Sparse topics now have proper visual grounding (cards at top, container fills space)
- **Typography System** — Harmonized expanded snippet typography across layouts

### Removed

- **Compare (Reel) Lens** — Retired the carousel-style Compare layout; only Curate and Read remain

### Fixed

- Right rail ModalManager integration for clean keyboard scope
- Tab/Shift+Tab no longer traps focus in palette
- Atomic DOM focus initialization with shadow DOM guards
- Layout navigation and mouse click expansion
- Native DOM focus for card navigation
- Scroll-into-view reliability for cards and snippets
