# UI Context

## Theme

Mobile-first dashboard using shadcn/ui.  
Light mode first. Clean and structured layout.

## Colors

All colors are defined as CSS custom properties in `globals.css` and mapped to Tailwind tokens via `@theme inline`. Components must use these tokens — no hardcoded hex values or raw Tailwind color classes like `zinc-*`.

```css
:root {
  --color-background: oklch(0.98 0.01 250);
  --color-background-100: oklch(0.96 0.01 250);
  --color-background-200: oklch(0.93 0.012 250);
  --color-background-300: oklch(0.89 0.014 250);
  --color-background-400: oklch(0.82 0.016 250);
  --color-background-500: oklch(0.72 0.018 250);
  --color-background-600: oklch(0.58 0.02 250);
  --color-background-700: oklch(0.44 0.022 250);

  --color-foreground: oklch(0.2 0.02 250);
  --color-muted: oklch(0.93 0.012 250);

  --color-primary: oklch(0.62 0.15 250);
  --color-secondary: oklch(0.78 0.08 250);
  --color-accent: oklch(0.65 0.16 150);

  --color-black: oklch(0.12 0.01 250);
  --color-white: oklch(1 0 0);

  --color-border: oklch(0.96 0.01 250);
}
```

Tailwind utility names map to these variables

## Typography

| Role    | Font       |
| ------- | ---------- |
| UI text | Geist Sans |
| Mono    | Geist Mono |

## Component Library

- shadcn/ui
- Tailwind CSS

## Layout Patterns

- Mobile-first stacked layout
- Top navbar
- Card-based UI
- Modal forms for CRUD

## Icons

- Lucide React
- Sizes:
  - h-4 w-4 (small)
  - h-5 w-5 (buttons)

```

```
