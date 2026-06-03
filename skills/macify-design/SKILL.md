---
name: macify-design
description: Mac-like design rules for operational web tool and workspace products. Use when designing or implementing web apps whose primary workflow is creating, editing, managing, publishing, configuring, analyzing, monitoring, reviewing, automating, debugging, generating, previewing, or controlling objects, including admin systems, dashboards, editors, AI tools, CMS/CRM, tutorial/documentation publishing managers, content operations tools, developer tools, internal tools, and single-file HTML prototypes. Use when the user explicitly asks for Mac-like, Mac style, macOS-inspired, windowed workbench, Mac风格, 类Mac, 工具类Web产品, 管理后台, 工作台, 发布系统, 教程管理, or AI工具.
---

# Macify Design

## Overview

Treat Mac-like as a portable web product design system for tool and workspace products: a single-window desktop workbench, light/dark skin tokens, material layering, compact controls, responsive mobile app shell, and real product states. Do not simulate macOS.

Use this skill to turn vague tool-product requests into practical web UI. Prioritize product workflow, usability, accessibility, and implementation fit over visual imitation.

## Core Workflow

1. Detect whether the request is a tool/workspace product by workflow verbs, not by industry nouns.
2. Identify the core user, core object, primary workflow, secondary actions, and expected product states.
3. Classify the product pattern: management, editor, analytics, AI workbench, media/file manager, automation builder, configuration console, monitoring/log viewer, or publishing manager.
4. Choose the minimum useful complexity: simple, medium, complex, or expert.
5. Default the desktop design to one windowed workbench unless the product genuinely needs separate workspaces or the user requests another structure.
6. Define light and dark skin tokens before styling components.
7. Map the workflow into layout regions: app window, sidebar, toolbar, main workspace, optional inspector, sheet/popover, and status feedback.
8. Design tablet and mobile as responsive app shells, not scaled-down desktop windows.
9. Implement real interactions, mock data, state changes, and failure/empty/loading states when building code or HTML.
10. Validate the result against the quality gate before finishing.

## Trigger Rules

Trigger by operational workflow:

- Use the skill for create, edit, manage, publish, configure, analyze, monitor, review, automate, batch process, debug, generate, preview, and control workflows.
- Do not use it by default for read, browse, market, showcase, advertise, and passive content consumption workflows.
- For ambiguous nouns such as tutorial system, documentation system, knowledge base, course platform, blog system, media system, data system, user system, or order system, inspect the verbs and intent. A tutorial publishing manager triggers; a tutorial reading site does not.
- If the user explicitly asks for Mac-like, Mac style, macOS-inspired, Apple-computer-software style, or a windowed tool interface, use the skill unless the request would require copying Apple assets or simulating the operating system.

Read `references/trigger-rules.md` when the request is ambiguous.

## Product Model

Default tool/workspace web products to one windowed workbench. Treat the product as a working surface, not a collection of unrelated pages.

Allow separate views for authentication, onboarding, public preview, payment, errors, mobile drill-in flows, and genuinely separate workspaces. Keep settings, detail editing, publishing, filtering, and object properties inside the workbench through sidebars, inspectors, sheets, popovers, drawers, or drill-in views whenever that preserves workflow continuity.

## Mac-Like Definition

Use Mac-like as skin, layout, density, and material inspiration for web products. Do not create a macOS clone.

Do:

- Use windowed app structure, sidebar, toolbar, split views, inspector, popovers, sheets, status bars, compact controls, semantic colors, and light/dark appearance.
- Use system font stacks and project-approved icon libraries.
- Make the skin feel precise through tokens, material layers, separators, shadows, highlights, and interaction states.

Do not:

- Add a Dock, system menu bar, desktop wallpaper, fake OS window manager, Finder/Settings/Mail copies, Apple logo, Apple screenshots, or Apple-owned visual assets.
- Treat traffic-light dots as core product controls.
- Use SF Symbols unless the user's project already has a legal, explicit basis to use them.
- Use glassmorphism as a substitute for product structure.

Read `references/apple-boundaries.md` when the design risks looking like an operating-system clone.

## Skin System

Define skin tokens before styling components. Provide light and dark values together.

Minimum token groups:

- Page backdrop, window background, window border, window shadow.
- Sidebar, toolbar/titlebar, content, inspector, sheet/popover, status bar.
- Thin, regular, and thick material colors.
- Separators, text levels, accent, selection, focus ring.
- Control background, hover, active, selected, disabled, danger, success, warning, loading.

Use `prefers-color-scheme` by default and add a manual theme toggle when the product benefits from it. In dark mode, rely more on borders, subtle highlights, and material contrast than heavy external shadows. In light mode, use clearer shadows and translucent chrome cautiously. `backdrop-filter` may enhance chrome layers only; never rely on it for readability.

Read `references/skin-system.md` for token and material rules.

## Layout And Responsive Rules

Desktop:

- Use a windowed workbench with toolbar/titlebar, sidebar, main workspace, optional inspector, sheets/popovers, and status feedback.
- Let each region serve workflow logic. Do not add panes just to look Mac-like.
- Prefer split views for object-list/detail, editor/properties, asset-grid/preview, workflow-canvas/configuration, and dashboard/filter-detail patterns.

Tablet:

- Collapse the sidebar into a drawer or compact navigation.
- Convert the inspector into an overlay, drawer, or mode switch.
- Keep the toolbar compact and preserve primary actions.

Mobile:

- Use a Mac-like mobile app shell, not a scaled desktop window.
- Replace sidebar with drawer, bottom sheet, or navigation view.
- Replace inspector with bottom sheet, full-screen detail, or drill-in view.
- Replace dense tables with list rows, summary cards, or detail drill-ins unless the table is genuinely the product surface.
- Preserve navigation, viewing, primary actions, status, and lightweight editing. For complex canvas, code, table, or automation tools, allow advanced editing to be best on desktop while keeping essential mobile flows usable.
- Do not use horizontal overflow as the default mobile adaptation.

Read `references/layout-mobile-patterns.md` for product pattern mappings.

## Real Product Behavior

When building code or HTML prototypes, implement a usable product surface rather than a static screenshot.

Include realistic mock data and product-specific interactions where relevant:

- Search, filter, sort, selection, preview, edit, create, delete, duplicate, publish, save, run, export, import, or product-specific equivalents.
- Empty, loading, error, disabled, selected, editing, saving/syncing, success, permission, and no-data states.
- Clear toolbar actions, contextual menus/popovers, sheet flows, and status feedback.
- Keyboard focus states and mobile pressed states.

For single-file HTML requests, build a static but interactive prototype with in-memory or `localStorage` state when appropriate.

Read `references/component-states.md` for component and state requirements.

## Existing Projects

When working in an existing codebase:

- Inspect the framework, routing, component library, CSS strategy, icons, and design tokens before editing.
- Layer Mac-like skin over the existing architecture rather than replacing it wholesale.
- Reuse existing components and utilities unless they block the requested quality.
- Avoid adding heavy dependencies unless the project already uses them or the user approves.
- Keep edits scoped to the requested product surface.

## Output Contract

- If the user asks to implement, edit the project or create the requested files.
- If the user asks for HTML, create a usable interactive prototype, not a passive mockup.
- If the user asks only for a design plan, provide product structure, layout, skin tokens, responsive behavior, and key component states.
- If runtime validation tools are available, run or inspect the result. If not, perform a static self-check using the validation checklist.
- Ask at most 1-3 questions only when missing information would materially change the product model. Otherwise make reasonable assumptions and proceed.

## Quality Gate

Before finishing, validate that:

- The request is actually a tool/workspace workflow or explicitly asks for this style.
- The result is not a marketing page, passive reading site, or macOS clone.
- The design uses one coherent product workbench by default, with justified exceptions.
- Light and dark appearances exist and use semantic tokens.
- Window, chrome, content, inspector, sheet/popover, and status layers have distinct material roles.
- Desktop, tablet, and mobile layouts are intentionally adapted.
- Real product states and interactions exist.
- Controls include hover/pressed, selected, disabled, loading, and focus-visible states.
- Text, controls, tables, and panels do not overlap or overflow incoherently.
- Contrast, keyboard navigation, touch targets, reduced motion, and reduced transparency fallbacks are respected.

Read `references/validation-checklist.md` when completing a substantial UI.
