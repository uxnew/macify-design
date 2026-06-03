# Decision Cases

Use these cases to validate whether Macify Design should apply. The skill triggers by workflow behavior, not industry nouns.

## Should Trigger

| Prompt | Expected reason |
| --- | --- |
| Build a tutorial system HTML to manage and publish tutorials. | Publishing manager: manage, edit, preview, publish. |
| Build an AI prompt manager with folders, model settings, and run history. | AI workbench: manage, generate, preview, configure. |
| Build an order management admin for refunds and fulfillment. | Operational admin: manage and process objects. |
| Build a monitoring dashboard for logs, alerts, and incident review. | Monitoring workflow: analyze, monitor, review. |
| Build a document template editor with variables and preview. | Editor workflow: create, edit, preview. |
| Build a knowledge base admin for tagging, reviewing, and publishing articles. | Content operations: edit, review, publish. |

## Should Not Trigger By Default

| Prompt | Expected reason |
| --- | --- |
| Build a landing page for an AI startup. | Marketing workflow. |
| Build a tutorial website where users read HTML/CSS lessons. | Passive reading workflow. |
| Build a static documentation site. | Passive browsing/reading workflow. |
| Build an ecommerce storefront homepage. | Storefront, not admin tool. |
| Build a portfolio for a designer. | Showcase workflow. |
| Build a game homepage. | Game/marketing surface, not tool workbench. |

## Explicit Override

If the user explicitly asks for Mac-like, Mac style, macOS-inspired, or a windowed tool interface, apply Macify Design only as far as it helps the product. Still enforce:

- No macOS simulation.
- No Apple assets.
- No Dock, system menu bar, fake desktop, Finder clone, or Settings clone.
- Product workflow and usability stay above visual imitation.

## Ambiguous Cases

| Prompt | Expected action |
| --- | --- |
| Build a tutorial system. | Inspect verbs/context. If missing, ask whether it is for reading or managing/publishing. |
| Build a documentation platform. | Inspect whether it is a docs reader or docs CMS. |
| Build a knowledge base. | Inspect whether it is an article browser or KB management tool. |
| Build a data dashboard. | Trigger if users filter/analyze/monitor; do not trigger for a passive data storytelling page unless requested. |
