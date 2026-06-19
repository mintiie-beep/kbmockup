# Color Tokens — miniATM (ตู้เงินดี)
> Figma node: 1798:134347 (ATM--CF- — Styles)
> ดึงจาก Figma variable definitions โดยตรง

---

## [PRIMARY GREEN]

| Token | Hex | Use |
|-------|-----|-----|
| `Primary/Primary Green` | `#0B8041` | ปุ่มหลัก, icon primary — shared กับ KBao Merchant |
| `Bg/Green` / `Color/Green` / `Text/Green` | `#005E23` | พื้นหลังสีเขียวเข้ม, text on light bg, header zone |
| `Text/Dark green` | `#0F4B4D` | Text เขียวเข้มมาก, title บนหน้ามืด |
| `Color/Light Green` / `Bg/Light Green` | `#C5D8C7` | พื้นหลังสีเขียวอ่อน, highlight zone |
| `Bg/Lightest Green` | `#F1F8EE` | พื้นหลัง section สีเขียวจางมาก |
| `BG/Green5` | `#F3F9F6` | Shared กับ KBao — summary box bg |

---

## [NEUTRAL]

| Token | Hex | Use |
|-------|-----|-----|
| `Text/Black` / `Color/Black` | `#090909` | Text หลักบนพื้นขาว |
| `Text/Text Black` | `#000000` | Text pure black |
| `Text/Dark Grey` / `Color/Dark Grey` | `#3D3D3D` | Text secondary |
| `Text/Text Dark Grey` | `#6D6D6D` | Text muted, label |
| `Color/Grey` / `Stoke/Grey` | `#C0C0C0` | Border, divider |
| `Color/Light Grey` | `#F1F1F1` | Background card, input bg |
| `Bg/White` / `Text/White` / `Color/White` | `#FFFFFF` | White — text on dark, bg |
| `Color/Black 7` / `Bg/Black 7` | `#00000012` | Black 7% opacity — overlay |
| `Bg/White 10` | `#FFFFFF1A` | White 10% opacity — overlay on dark bg |

---

## [STATUS / ACTION]

| Token | Hex | Use |
|-------|-----|-----|
| `Color/Red` / `Text/Red` / `error` / `Stoke/Red` | `#A90000` | Error, destructive action |
| `Button/White` | `#FFFFFF` | Button text/bg สีขาว |
| `Button/White 60` / `Color/White 60` | `#FFFFFF99` | Button/text ขาว 60% opacity — disabled / ghost |

---

## [BRAND]

| Token | Hex | Use |
|-------|-----|-----|
| `Brand color` | `#EE2128` | เจ็นดี brand red |
| `lightblue` | `#C6D0EB` | — |
| `darkgreen` | `#205284` | — |

---

## [EFFECTS]

| Token | Value | Use |
|-------|-------|-----|
| `btn shadow 2` | `drop-shadow(0 1px 8px #005E2326), drop-shadow(0 1px 6px #005E234D)` | Button shadow (green tint) |
| `btn-focused` | `inner-shadow(1 2px 2px #00000026)` | Button focus state |
| `radiant` | `20px` | Border radius หลัก |

---

## [CSS CUSTOM PROPERTIES]

```css
:root {
  /* Primary Green */
  --color-primary:        #0B8041;
  --color-green-deep:     #005E23;
  --color-green-dark:     #0F4B4D;
  --color-green-light:    #C5D8C7;
  --color-green-lightest: #F1F8EE;
  --color-green-5:        #F3F9F6;

  /* Neutral */
  --color-black:          #090909;
  --color-dark-grey:      #3D3D3D;
  --color-grey:           #6D6D6D;
  --color-light-grey:     #C0C0C0;
  --color-bg-light:       #F1F1F1;
  --color-white:          #FFFFFF;
  --color-overlay-black:  rgba(0,0,0,0.07);
  --color-overlay-white:  rgba(255,255,255,0.10);

  /* Status */
  --color-error:          #A90000;

  /* Brand */
  --color-jend:           #EE2128;

  /* Radius */
  --radius-base:          20px;
}
```
