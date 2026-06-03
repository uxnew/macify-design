# Example: Tutorial Publishing System

Prompt:

> Build a tutorial system HTML to manage and publish tutorials.

Macify Design should trigger.

Expected product interpretation:

- Product type: tutorial publishing manager.
- Core objects: tutorials, chapters, assets, drafts, versions, publish status.
- Primary workflow: create, edit, organize, preview, publish.
- Secondary workflows: search, filter, schedule, manage metadata, review status.

Expected desktop layout:

- Sidebar: tutorial library, categories, status filters.
- Toolbar: search, new tutorial, preview, publish.
- Main workspace: tutorial list, chapter editor, or selected tutorial workspace.
- Inspector: cover, SEO, metadata, status, schedule, version info.
- Sheet/popover: create tutorial, asset picker, publish confirmation.
- Status feedback: draft, saved, scheduled, published, failed.

Expected mobile layout:

- Top app bar with menu, title, primary publish/new action, overflow.
- Tutorial list as primary view.
- Categories/status filters in drawer or sheet.
- Editor/settings as drill-in view or bottom sheet.
- Publishing flow as full-screen sheet or confirmation sheet.

Required states:

- Empty tutorial library.
- Loading/saving.
- Draft/published/scheduled/reviewing/failed.
- Selected tutorial.
- Dirty unsaved edits.
- Publish success/error.
