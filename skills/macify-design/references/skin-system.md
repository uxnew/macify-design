# Skin System

Build the Mac-like effect through semantic tokens and material layers. Do not rely on generic adjectives such as premium, elegant, frosted, or glassy unless they are implemented through explicit colors, borders, shadows, transparency, and states.

## Required Token Groups

Define light and dark values together:

The palette below is an example, not a fixed theme. Do not copy it unchanged when product context, brand, or domain suggests a better accent, density, or material contrast. Keep the semantic token structure stable while adapting the values.

```css
:root {
  color-scheme: light;
  --mac-page-bg: #eef0f3;
  --mac-window-bg: rgba(248, 249, 251, 0.92);
  --mac-window-border: rgba(20, 24, 32, 0.14);
  --mac-window-shadow: 0 24px 70px rgba(18, 24, 38, 0.22);
  --mac-sidebar-bg: rgba(238, 240, 244, 0.78);
  --mac-toolbar-bg: rgba(250, 251, 253, 0.82);
  --mac-content-bg: rgba(255, 255, 255, 0.88);
  --mac-inspector-bg: rgba(246, 247, 250, 0.84);
  --mac-material-thin: rgba(255, 255, 255, 0.54);
  --mac-material-regular: rgba(248, 249, 251, 0.78);
  --mac-material-thick: rgba(255, 255, 255, 0.92);
  --mac-separator: rgba(20, 24, 32, 0.12);
  --mac-text-primary: #111827;
  --mac-text-secondary: #4b5563;
  --mac-text-tertiary: #7b8493;
  --mac-accent: #0a84ff;
  --mac-control-bg: rgba(255, 255, 255, 0.72);
  --mac-control-hover: rgba(255, 255, 255, 0.95);
  --mac-control-active: rgba(232, 239, 255, 0.96);
  --mac-selection-bg: rgba(10, 132, 255, 0.15);
  --mac-focus-ring: rgba(10, 132, 255, 0.45);
}

@media (prefers-color-scheme: dark) {
  :root {
    color-scheme: dark;
    --mac-page-bg: #111318;
    --mac-window-bg: rgba(29, 31, 36, 0.94);
    --mac-window-border: rgba(255, 255, 255, 0.12);
    --mac-window-shadow: 0 24px 80px rgba(0, 0, 0, 0.55);
    --mac-sidebar-bg: rgba(38, 40, 46, 0.72);
    --mac-toolbar-bg: rgba(32, 34, 39, 0.84);
    --mac-content-bg: rgba(24, 26, 31, 0.88);
    --mac-inspector-bg: rgba(34, 36, 42, 0.82);
    --mac-material-thin: rgba(255, 255, 255, 0.06);
    --mac-material-regular: rgba(255, 255, 255, 0.09);
    --mac-material-thick: rgba(255, 255, 255, 0.13);
    --mac-separator: rgba(255, 255, 255, 0.11);
    --mac-text-primary: #f4f6fb;
    --mac-text-secondary: #b7bfcc;
    --mac-text-tertiary: #7f8794;
    --mac-accent: #0a84ff;
    --mac-control-bg: rgba(255, 255, 255, 0.08);
    --mac-control-hover: rgba(255, 255, 255, 0.13);
    --mac-control-active: rgba(10, 132, 255, 0.24);
    --mac-selection-bg: rgba(10, 132, 255, 0.26);
    --mac-focus-ring: rgba(10, 132, 255, 0.58);
  }
}
```

Adapt values to the product's brand and existing design system. Keep semantic names stable.

## Domain Variants

Use product domain to tune the skin so every output does not become the same gray-blue shell:

- Publishing/tutorial tools: favor calm content surfaces, slightly warmer content material, clear draft/published/scheduled status colors, and a restrained blue/green accent.
- AI workbenches: favor cooler chrome, stronger run/status contrast, model/settings inspector clarity, and blue/cyan or violet accents only when they do not dominate the UI.
- Analytics/admin consoles: favor neutral dense tables, clear separators, low-noise chart surfaces, and blue/teal accents for selected views and filters.
- Developer/monitoring tools: favor graphite or neutral dark surfaces, precise monospace regions, green/amber/red status tokens, and high-contrast log/table states.

Never change the product's brand just to make it look more Mac-like. Use Mac-like material and layout as a skin layer over the product's actual identity.

## Material Layers

Use four conceptual layers:

- Page backdrop: environment only, never the product surface.
- Window material: rounded application container with border and shadow.
- Chrome material: sidebar, toolbar, titlebar, inspector, status bar. More translucent and layered than content.
- Content material: tables, editors, forms, canvases, lists, dashboards. More solid for readability.

`backdrop-filter` may enhance chrome material only. Always provide readable background colors without blur.

## Light And Dark Appearance

- Implement both light and dark appearances by default.
- Use `prefers-color-scheme` and allow a manual toggle when useful.
- Do not invert light colors mechanically for dark mode.
- In dark mode, reduce heavy external shadows and rely on separators, subtle highlights, and local contrast.
- In light mode, use clear but restrained window shadows.
- Ensure images, charts, embedded previews, and white-background content do not glare in dark mode.

## Texture Without Noise

Mac-like texture comes from a calibrated combination:

- Slightly different material backgrounds for window/chrome/content.
- 1px separators with low opacity.
- Compact control shadows or inset highlights.
- Clear selected states.
- Small radius, generally 6-10px for controls and 10-16px for the outer window unless the existing product says otherwise.

Avoid one-note gray shells. Use a restrained accent color derived from product domain or brand, not a random rainbow.
