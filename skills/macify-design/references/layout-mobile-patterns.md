# Layout And Mobile Patterns

Use Mac-like layout as an information architecture pattern, not decoration.

## Desktop Workbench

Default desktop structure:

```text
app window
├── toolbar / titlebar
├── sidebar
├── main workspace
├── optional inspector
└── status feedback
```

Use this structure when it helps users keep context while acting on objects.

## Complexity Levels

- Simple: toolbar + main workspace + result/status area.
- Medium: sidebar + toolbar + main workspace.
- Complex: sidebar + toolbar + main workspace + inspector + status bar.
- Expert: multi-pane workspace, saved views, command/search affordances, keyboard shortcuts, batch actions, and deep status feedback.

Do not use a complex structure for a simple tool.

## Product Pattern Mapping

- Management tool: sidebar filters/collections, table or list, inspector or detail drawer.
- Editor: toolbar, canvas/editor, inspector/properties, asset browser when needed.
- Analytics/dashboard: sidebar filters or saved views, main charts/tables, detail panel or drill-in.
- AI tool: history/sidebar, conversation or workbench, input composer, settings/model inspector, run/status feedback.
- File/media manager: source/sidebar, grid/list, preview inspector, metadata/actions.
- Automation builder: node/canvas, run toolbar, properties inspector, logs/status.
- Configuration console: category sidebar, form sections, validation/status area.
- Monitoring/log viewer: navigation, dense stream/table, filters, detail drawer, live status.
- Publishing manager: collection/sidebar, list/editor, preview, publishing settings, version/status feedback.

## Tablet

- Collapse sidebar into a drawer, compact rail, or view switcher.
- Move inspector into overlay, drawer, or tabbed detail.
- Keep primary action and search/filter reachable.
- Avoid three fixed columns.

## Mobile

Mobile is a Mac-like app shell, not a scaled desktop window.

Use:

- Top app bar with title, back/menu, one primary action, and overflow.
- Drawer, bottom sheet, or drill-in navigation instead of a permanent sidebar.
- Bottom sheet, full-screen sheet, detail view, or drill-in instead of a permanent inspector.
- List rows or summary cards instead of dense tables.
- Sticky primary action or bottom action area only when it improves task completion.

Preserve:

- Object navigation.
- Viewing and search.
- Primary create/edit/publish/run action.
- Status feedback.
- Lightweight editing.

Allow:

- Advanced canvas, code, workflow, spreadsheet, or bulk operations to be best on desktop, while mobile remains useful for review, status, small edits, approvals, and simple actions.

Do not:

- Keep a 240px desktop sidebar on mobile.
- Use three columns on mobile.
- Depend on horizontal overflow as the default adaptation.
- Show a full desktop window frame with traffic lights on small screens.
- Shrink font and controls until touch targets fail.
