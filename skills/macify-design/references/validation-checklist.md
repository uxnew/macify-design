# Validation Checklist

Use this checklist before finishing substantial Macify Design work.

## Trigger Fit

- The product is a tool/workspace workflow, or the user explicitly requested Mac-like design.
- Ambiguous nouns were resolved by verbs and intent.
- Passive reading, marketing, ecommerce storefront, blog, portfolio, game, or brand homepage requests were not forced into this style.

## Product Structure

- The core user, object, workflow, and primary actions are clear.
- The design defaults to one coherent workbench where appropriate.
- Exceptions such as auth, public preview, errors, mobile drill-ins, or genuinely separate workspaces are justified.
- Each pane exists for workflow value, not decoration.

## Mac-Like Skin

- The result is not a macOS clone.
- No Apple logo, Dock, system menu bar, Apple screenshots, copied app UI, or default SF Symbols.
- Light and dark appearances are both defined.
- Skin uses semantic tokens instead of scattered literal colors.
- Window, chrome, content, inspector, sheet/popover, and status areas have distinct material roles.
- `backdrop-filter` is optional enhancement only.

## Real Tool Behavior

- Mock data exists where needed.
- Search/filter/sort, selection, edit/create/delete, publish/save/run/export/import, or product-specific equivalents are implemented or specified.
- Empty, loading, error, success, disabled, selected, editing, saving/syncing, permission, and no-data states are covered where relevant.
- Status feedback is visible and understandable.

## Responsive Behavior

- Desktop uses a windowed workbench.
- Tablet collapses or overlays secondary panes.
- Mobile uses an app shell, not a scaled desktop window.
- Sidebar, inspector, toolbar, tables, and dense workspaces have mobile alternatives.
- Horizontal overflow is not the default mobile strategy.
- Touch targets and typography remain usable.

## Accessibility And Polish

- Text does not overflow, overlap, or become unreadable.
- Controls have focus-visible states.
- Keyboard navigation remains possible.
- Contrast works in both appearances.
- Motion and transparency have sensible fallbacks.
- The product does not look like a static mockup.
