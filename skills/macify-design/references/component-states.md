# Component And State Rules

Mac-like web products must feel like usable tools, not static screenshots.

## Core Components

Use the components that match the workflow:

- App window.
- Toolbar/titlebar.
- Sidebar/navigation/source list.
- Split view.
- Main workspace.
- Inspector/properties panel.
- Segmented control.
- Search field.
- Icon button and icon+text button.
- List row and table row.
- Table/grid.
- Popover.
- Sheet/modal.
- Context menu or menu button.
- Status bar.
- Toast or inline status feedback.
- Theme toggle when appropriate.

## Required States

Every interactive control needs relevant states:

- Default.
- Hover where pointer exists.
- Pressed/active.
- Selected/current.
- Focus-visible.
- Disabled.
- Loading/busy where actions take time.
- Error and success where actions can fail or complete.

Mobile controls need pressed and selected states even where hover is irrelevant.

## Product States

Include the states that make the tool believable:

- Empty state.
- Loading state.
- Error state.
- No permission or locked state.
- No results state.
- Dirty/unsaved state.
- Saving/syncing state.
- Published/draft/scheduled/reviewing states for publishing tools.
- Running/queued/succeeded/failed states for automation or AI tools.
- Selected, editing, previewing, and bulk-selection states where relevant.

## Interaction Baseline

Implement or specify realistic interactions:

- Search, filter, and sort for collections.
- Select rows/items and show details.
- Create/edit/delete or the product-specific equivalent.
- Preview and publish for content operations.
- Run, stop, retry, export, or import for operational tools.
- Open sheets/popovers for secondary tasks.
- Show status changes after actions.

For single-file HTML prototypes, use in-memory state or `localStorage` when persistence makes the prototype more useful.

## Accessibility

- Keep visible focus rings.
- Keep contrast readable in both light and dark appearances.
- Use semantic buttons/inputs where implementing HTML.
- Maintain keyboard navigation for toolbar controls, lists, dialogs, and forms.
- Make mobile touch targets close to 40-44px where possible.
- Respect reduced motion and provide reduced transparency fallback.
- Do not hide essential labels behind unexplained icons; use accessible names and tooltips where appropriate.
