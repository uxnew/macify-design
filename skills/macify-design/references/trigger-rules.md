# Trigger Rules

Use workflow behavior, not industry nouns, to decide whether Macify Design applies.

## Trigger

Use the skill when the user's requested web product is primarily operational:

- Create, edit, manage, publish, configure, analyze, monitor, review, automate, batch process, debug, generate, preview, or control objects.
- Build a tool, workbench, admin console, dashboard, editor, AI tool, CMS/CRM, developer tool, internal system, monitoring console, automation builder, content operations tool, or publishing manager.
- Create a single-file HTML prototype for a tool/workspace product.
- Explicitly request Mac-like, Mac style, macOS-inspired, Apple-computer-software style, or a windowed tool interface.

## Do Not Trigger By Default

Do not use the skill by default when the primary workflow is passive:

- Read, browse, consume, market, present, showcase, advertise, or explain content.
- Marketing site, brand homepage, blog, passive documentation site, article/video library, ecommerce storefront, portfolio, game, or immersive landing page.
- A project with a stronger explicit design direction such as Material Design, iOS native, Windows Fluent, Notion-like, Linear-like, shadcn default, or an existing enterprise design system.

If the user explicitly asks for Mac-like design in one of these cases, apply only the skin and layout ideas that do not harm the product's actual purpose.

## Ambiguous Product Nouns

Inspect verbs and intent for ambiguous nouns:

- Tutorial system: trigger for authoring, managing, publishing, reviewing, progress tracking, interactive labs; do not trigger for a tutorial reading site.
- Documentation system: trigger for documentation CMS, publishing workflow, review dashboard; do not trigger for a static docs reader.
- Knowledge base: trigger for KB management, tagging, review, analytics; do not trigger for a passive article browser.
- Course platform: trigger for course builder, teacher admin, assignments, analytics; do not trigger for a course marketing page.
- Media system: trigger for asset manager, editor, transcoding queue, review tool; do not trigger for a media showcase.
- Ecommerce: trigger for order/inventory/admin tools; do not trigger for storefronts by default.

## Strong Override

If the user says "make it Mac-like" or similar, use the skill, but still enforce:

- No macOS simulation.
- No Apple assets.
- No Dock, menu bar, Finder clone, Settings clone, Mail clone, or fake OS.
- Product workflow stays more important than visual imitation.
