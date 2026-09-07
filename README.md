<div align="center">

# Osmium Themes

![Themes](https://img.shields.io/badge/themes-11-6b21a8?style=for-the-badge)
![Format](https://img.shields.io/badge/format-.osmtheme-0F5C58?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-c084fc?style=for-the-badge)

A collection of custom themes for **Osmium**, 11 palettes with native `.osmtheme` files.

</div>

---

## Themes

### Dark

- **Aubergine** — deep purple, the house style
- **Emerald** — teal-forward, sibling to Aubergine
- **Mocha** — warm, low-contrast dark
- **Ruby Star** — gemstone red over wine-black gradients

Aubergine and Emerald share the same structure and contrast ratios, only the accent hue changes (`#6b21a8` vs `#0F5C58`).

Ruby Star is gradient-based rather than flat. The tinting lives in the `--neutral-700/800/900` ramp, so surfaces fade continuously instead of tiling per element. It ships with `forceAccent: true` — set your custom accent to `#e0244a` to drive the primary color.

### Pride

- **Lesbian Pride** — flag gradient accents on dark
- **Trans Pride** — flag gradient accents on dark

### Novelty

- **Frutiger Aero** — glossy, glass, aggressively 2007
- **Terminal 95** — yellow over black translucent accents
- **Skype Modern Blue**
- **Skype Modern Purple**
- **Windows 10**
---

## Installation

### `.osmtheme` — recommended

1. Download the theme you want from the [latest release](../../releases/latest), or grab the file directly from its folder in `themes/`
2. Open Osmium and go to **Settings → Appearance → Themes**
3. Import the `.osmtheme` file
4. Select it from the theme list

---

## Making your own

The quickest route is usually to start from an existing theme. Duplicate `themes/aubergine.osmtheme`, swap the accent colors, and adjust from there.

For a gradient theme, start from `themes/ruby-star.osmtheme` instead — gradients belong on the foundation ramp and the large surface tokens, not on `--bg-soft-200` or `--bg-surface-800`, which repeat across every bubble and hover state.

Two things worth knowing before you edit:

- Osmium only accepts its own token names. Inventing a new ramp (`--ruby-500`, `--gold-500`) reports every one of them as a broken value, even though the JSON is
