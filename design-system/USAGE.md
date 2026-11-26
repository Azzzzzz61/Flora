# 芙洛拉 Flora Design System Usage

Design System package guide for OpenDesign agents, Claude Design, and frontend developers.

## Read Order

1. Read this file first to align on visual boundaries and non-negotiables.
2. Read `DESIGN.md` for atmosphere, color contrast rules, seasonal wash boundaries, typography, and atomic component states.
3. Paste `tokens.css` (or map `tokens.json`) as the single source of truth before styling any screen.
4. Open `preview.html` in a browser when you need an offline visual check of colors, seasonal washes, typography, or atomic component states.
5. Read `../docs/product.md` before designing any specific product screen — this design system intentionally does **not** lock page layouts.

## Design Highlights

- **Pure white gallery canvas (`#FFFFFF`) + neutral photo containers (`#F6F6F8`)**: Keeps bouquet colors completely true without pink cast or filters.
- **Seasonal top atmospheric wash + frosted glass cards**: Default Spring pastel wash (`#CFC8EA → #F3C8DC → #FFFFFF`) melts seamlessly into white; seasonal changes swap ONLY `--flora-wash-start` and `--flora-wash-mid`.
- **Obsidian-violet ink primary CTAs (`#0B051D` + white text)** in light mode paired with **Flora Pink (`#FFB3C7` + `#0B051D` text)** brand highlights, **iris violet (`#5B3FD9`)** links/progress, and **botanical lime (`#DAF79A` / `#1E3308`)** featured badges.
- **Floating frosted pill 5-tab dock** (`逛花｜花店｜挑花｜消息｜我的`, `62px` height, `32px` radius) with soft inner active capsule (`#EFEFF4`) and hairline-bordered layered cards (`#E9E5EE` / `#EFEBF2`).

## Do

- Use pure neutral `--surface-warm` (`#F6F6F8`) for bouquet image tiles and filled inputs.
- Pair `--accent` (`#FFB3C7`) strictly with deep ink `--accent-on` (`#0B051D`).
- Use `font-variant-numeric: tabular-nums` on every price, distance, and count.
- Keep default screen explorations on the Spring pastel wash (`#CFC8EA → #F3C8DC`) unless explicitly asked for another season.
- Respect `prefers-reduced-motion: reduce` and preserve at least `44 × 44` touch targets.

## Avoid

- Never put white text on `#FFB3C7` Flora Pink, and never use `#FFB3C7` as a standalone hairline border or icon on a light canvas (1.71:1 contrast).
- Never use harsh dark outlines on every card or pure `#000000` black text; keep borders delicate (`#E9E5EE` / `#EFEBF2`) and structural ink `#0B051D`.
- Never tint bouquet image backgrounds pink or overlay dark scrims on bouquet photos in dark mode.
- Never swap core brand colors, primary CTA ink, or semantic colors when changing seasons — only swap the two top wash tokens.
