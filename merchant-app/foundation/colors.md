# Colors — Merchant App (KBao)
> Figma node: 4:721 (Style Guide - Colors)
> Source of truth for all color tokens used in KBao Merchant App UI

---

## Brand Primary

| Token name | Hex | Usage |
|-----------|-----|-------|
| Primary Green | `#0B8041` | Main action, CTA buttons, icons, active states |
| Primary Red | `#EA1E30` | Destructive actions, error states |

---

## Secondary

| Token name | Hex | Usage |
|-----------|-----|-------|
| Yellow | `#FBC02D` | Warning, highlight accent |
| Yellow Text | `#C28000` | Text on yellow BG |
| Yellow BG | `#FFF9EA` | Warning background, banner BG |

---

## Text

| Token name | Hex | Usage |
|-----------|-----|-------|
| Text Black | `#000000` | Header, main text, icon |
| Text Dark Grey | `#6D6D6D` | Description, secondary text |
| Text Middle Grey | `#A6A6A6` | Placeholder, helper text, disabled text |
| Text Grey | `#D9D9D9` | Input field placeholder (light) |
| Text White | `#FFFFFF` | Text on dark background |
| Primary Green (link) | `#0B8041` | Link text, active label |

---

## Background

| Token name | Hex | Usage |
|-----------|-----|-------|
| White BG | `#FFFFFF` | Card, content area, input field |
| Frame BG | `#F3F5F8` | App frame, status bar, page background |
| Content BG | `#F8F8F8` | Secondary content background |
| Green5 | `#F3F9F6` | Light green tint background |

---

## Line / Stroke

| Token name | Hex | Usage |
|-----------|-----|-------|
| Stroke Dark Grey | `#6D6D6D` | Strong border |
| Stroke Grey | `#E6E6E6` | Default card/input border |
| Stroke White | `#FFFFFF` | Border on dark background |
| Primary Green | `#0B8041` | Active/selected border (e.g. KM card) |
| Green20 | `#CEE6D9` | App bar border-bottom, input border |

---

## Disable

| Token name | Hex | Usage |
|-----------|-----|-------|
| Disable Text Grey | `#A5A5A5` | Disabled label text |
| Disable Stroke | `#E6E6E6` | Disabled border |
| Disable BG | `#F4F4F4` | Disabled button background |
| Disable Text White | `#FFFFFF` | Disabled text on dark bg |

> Note: Disabled primary button = bg `#F2F2F2`, text `#A6A6A6` (per button.md)

---

## State

| Token name | Hex | Usage |
|-----------|-----|-------|
| Success | `#0B8041` | Success state icon/text |
| Warning | `#FBC02D` | Warning state icon/text |
| Negative | `#EA1E30` | Error/failure state icon/text |

---

## Icon

| Token name | Hex | Usage |
|-----------|-----|-------|
| Icon Black | `#000000` | Default icon color |
| Icon Green | `#0B8041` | Function/service icon color |

---

## Overlay

| Token name | Value | Usage |
|-----------|-------|-------|
| Overlay BG | `rgba(0, 0, 0, 0.35)` | Modal/bottom sheet backdrop |

---

## Gradient

| Token name | From | To | Usage |
|-----------|------|----|-------|
| Gradian BG | `#FFFFFF` | `#E5F6ED` | Subtle white-to-green card background |
| Gradian Green | `#1DD779` | `#01AA1D` | Special green gradient |

> User card gradient on Home page: `#0B8041` → `#289F5A` (linear, left to right)

---

## CSS Variables (Quick Reference)

```css
:root {
  /* Brand */
  --color-primary-green: #0B8041;
  --color-primary-red: #EA1E30;

  /* Secondary */
  --color-yellow: #FBC02D;
  --color-yellow-text: #C28000;
  --color-yellow-bg: #FFF9EA;

  /* Text */
  --color-text-black: #000000;
  --color-text-dark-grey: #6D6D6D;
  --color-text-mid-grey: #A6A6A6;
  --color-text-grey: #D9D9D9;
  --color-text-white: #FFFFFF;

  /* Background */
  --color-white-bg: #FFFFFF;
  --color-frame-bg: #F3F5F8;
  --color-content-bg: #F8F8F8;
  --color-green5: #F3F9F6;

  /* Stroke */
  --color-stroke-grey: #E6E6E6;
  --color-stroke-dark: #6D6D6D;
  --color-stroke-green: #0B8041;
  --color-green20: #CEE6D9;

  /* Disable */
  --color-disable-text: #A5A5A5;
  --color-disable-bg: #F4F4F4;
  --color-disable-stroke: #E6E6E6;

  /* State */
  --color-success: #0B8041;
  --color-warning: #FBC02D;
  --color-negative: #EA1E30;

  /* Icon */
  --color-icon-black: #000000;
  --color-icon-green: #0B8041;

  /* Overlay */
  --color-overlay: rgba(0, 0, 0, 0.35);
}
```
