# FMG Operations Console Brand Spec

Source: `mp1joq1r-image.png`, `index.html`, and the merged `fmg-system-suite.html` system direction.

## Core Tokens

```css
:root {
  --bg:      oklch(98.3% 0.003 286.4);
  --surface: oklch(100.0% 0.000 89.9);
  --fg:      oklch(28.1% 0.002 286.3);
  --muted:   oklch(47.6% 0.001 17.2);
  --border:  oklch(92.6% 0.005 286.3);
  --accent:  oklch(69.1% 0.177 134.2);

  --font-display: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Segoe UI", system-ui, sans-serif;
  --font-body:    -apple-system, BlinkMacSystemFont, "SF Pro Text", "Segoe UI", system-ui, sans-serif;
  --font-mono:    "JetBrains Mono", "IBM Plex Mono", ui-monospace, Menlo, monospace;
}
```

## Supporting Status Colors

```css
:root {
  --success-soft: oklch(96.4% 0.015 145.5);
  --danger:       oklch(55.8% 0.193 25.6);
  --danger-soft:  oklch(95.3% 0.013 17.4);
  --warning:      oklch(80.3% 0.110 58.2);
  --info:         oklch(51.3% 0.185 259.0);
  --map-line:     oklch(79.3% 0.017 259.4);
}
```

Usage rule: FMG green is the only brand and product accent. Red, orange, and blue are status colors only. Do not introduce purple or additional category colors for future FMG console pages.

## Layout Posture

- Near-white operations background with white dense cards.
- Cards use 1px low-saturation grey borders, 12px radius, and only a very soft container shadow where hierarchy needs separation.
- Desktop console shell uses an 82px left rail, 64px top bar, compact filters, and dense page grids.
- Typography is compact system UI: 9-10px metadata, 10-11px tables/lists, 12-14px card titles, 18-22px KPI values.
- Numerics, IDs, timestamps, and metrics use a mono stack with tabular figures.
- Tables and queues are real DOM rows with tight density, subtle separators, small status chips, and no zebra striping.
- Maps are structured placeholders with terrain-like pale texture, route overlays, zones, object labels, and legends. They are not decorative hero images.
- Evidence thumbnails reference local cropped assets from `assets/`; no generic external imagery.
- Icons are one Lucide/Feather-style thin-line SVG system: 14-22px, 2px stroke, nav and status icons from the same source.
- Accent budget is restrained: FMG green for active navigation, ready/verified/success states, primary CTA, and key route/title signals. Red is critical/risk, orange is pending/warning, blue is in-progress/information.

## Locked Restoration Rules

These rules are mandatory for every new FMG console page.

- Use a near-white operating canvas, white dense cards, 1px pale grey borders, and 12px primary card radius.
- FMG green is the only primary brand accent. Do not introduce purple, cyan, decorative gradients, or secondary brand accents.
- Red, orange, and blue are semantic-only: red for critical/risk/offline, orange for pending/warning/verification, blue for in-progress/information.
- Tables and queues must be real DOM structures, not bitmap screenshots. Row height should stay within 28-38px, with 9-11px row text.
- Map areas are structured placeholders only: pale terrain texture, route overlays, zones, labels, and legends. No real map tiles are required.
- Evidence thumbnails should reuse local cropped assets first; only generate mock assets when local assets cannot cover the state.
- Icons must stay in one Lucide/Feather-style outline family, sized 14-22px with 2px stroke. Navigation, status, and table icons must not mix filled or multi-weight styles.
- Use system UI for all interface text and the mono stack for numerics, IDs, timestamps, percentages, distances, and metric values.
- Before handoff, check for horizontal overflow, broken SVG symbol references, missing image assets, and table/list density drift.
