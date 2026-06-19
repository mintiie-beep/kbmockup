# Design System — miniATM (ตู้เงินดี)
> Figma file: ATM--CF- (`JMhoxPJRvtVT9yV8FAr4CY`)
> Platform: Kiosk touchscreen (landscape)
> ระบบ miniATM สำหรับให้บริการสินเชื่อผ่านตู้เงินดี — ใช้ร่วมกับ KBao Merchant ecosystem

---

## [OVERVIEW]

### System
| Property | Value |
|----------|-------|
| ชื่อระบบ | miniATM (ตู้เงินดี) |
| Platform | Kiosk — landscape touchscreen |
| ร่วมกับ | KBao Merchant App |
| Primary brand | kbao (KasikornBank Carabao) |
| Co-brand | เจ็นดี (เงินดี) |

---

## [CANVAS]

### Base Canvas (Primary)
| Property | Value |
|----------|-------|
| Width | 1280px |
| Height | 800px |
| Aspect ratio | **10:6.25** (≈ 10:6) |
| Orientation | Landscape |
| Figma frame ref | M-Home-001-s1 (5265:25804) — symbol 1728:83736 |

### Responsive Strategy
| Breakpoint | Canvas | Use case |
|-----------|--------|----------|
| **Base** | 1280×800 | ตู้ miniATM มาตรฐาน |
| Scale up | 1920×1200 | Kiosk จอใหญ่ |
| Scale down | 1024×640 | Kiosk จอเล็ก |

```css
/* Responsive container — scale to fill screen */
.kiosk-root {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}
.kiosk-canvas {
  width: 1280px;
  height: 800px;
  transform-origin: center center;
  /* JS: scale = Math.min(vw/1280, vh/800) */
}
```

> ใช้ CSS transform scale เพื่อ fit จอได้ทุกขนาด โดย maintain 1280×800 layout เดิม

---

## [BACKGROUND — Main Layout]

> Node: 1728:83736 (Property 1=Default)

### Background Layer
| Property | Value |
|----------|-------|
| Fill type | Radial gradient |
| Center color | `#3A9A5C` (lighter green) |
| Edge color | `#1A6638` (darker green) |
| Gradient center | ~50% 65% (slightly below center) |
| CSS | `radial-gradient(ellipse at 50% 65%, #3A9A5C 0%, #1A6638 100%)` |

### Logo Placement (Top Bar)
| Logo | Position | Size | Asset |
|------|----------|------|-------|
| **kbao** | top-left, 20px from edge | ~72×72px | `kbao-logo.svg` (white circle) |
| **เจ็นดี** | top-right, 20px from edge | ~72×72px | `jend-logo.svg` (red square, rounded) |

```
┌─────────────────────────────────────────────────────────┐
│ [kbao logo]                              [เจ็นดี logo]  │  ← 20px padding all sides
│                                                          │
│                  [content zone]                          │
│                                                          │
│                                                          │
│                                                          │
└─────────────────────────────────────────────────────────┘
  1280px
```

### Layout Zones
| Zone | Position | Size (approx) |
|------|----------|--------------|
| Top bar | 0, 0 | 1280 × 112px |
| Content area | 0, 112 | 1280 × 600px |
| Bottom bar | 0, 712 | 1280 × 88px |

---

## [ASSETS]

> Assets ทั้งหมดอยู่ใน Figma asset library ของไฟล์ ATM--CF-
> Export เป็น SVG / PNG ก่อน embed ใน mockup

### Logos
| Asset | Description |
|-------|-------------|
| `kbao-logo` | วงกลมขาว ตัวอักษร kbao (k แดง, b เขียว, ao ดำ) |
| `jend-logo` | สี่เหลี่ยมแดง rounded มีไอคอนปีกขาว + "เจ็นดี" |

### Icons (in asset)
> ดึงจาก Figma → export SVG ใส่ใน `miniatm/assets/icons/`
> ยังไม่ได้ list ครบ — เพิ่มเมื่อ implement แต่ละหน้า

---

## [COLORS]

> ยังไม่มี full token file — รอ foundation/colors.md
> ใช้ค่า observed จาก Figma ไปก่อน

| Token (ชั่วคราว) | Hex | Use |
|-----------------|-----|-----|
| `green/bg-dark` | `#1A6638` | Background edge |
| `green/bg-light` | `#3A9A5C` | Background center |
| `green/primary` | `#0B8041` | Shared กับ KBao DS |
| `red/jend` | `#D81C2E` | เจ็นดี brand |
| `white` | `#FFFFFF` | Text on dark bg, logo fill |

---

## [TYPOGRAPHY]

> รอ foundation/typography.md — คาดว่าใช้ font เดียวกับ KBao Merchant App

| Property | Value |
|----------|-------|
| Font family | LINE Seed Sans TH App |
| CSS fallback | `'Noto Sans Thai', sans-serif` |

---

## [INTERACTION NOTES — Kiosk]

- **Touch target minimum**: 80×80px (นิ้วมือ kiosk)
- **Font size minimum**: 20px (อ่านได้จากระยะ 50–80cm)
- **No hover states** — ใช้ `:active` / pressed state แทน
- **No keyboard input** — ใช้ numpad / on-screen keyboard เท่านั้น
- **Idle timeout**: หน้า home reset หลัง 60s ไม่มี interaction
- **Scroll**: หลีกเลี่ยง — ออกแบบให้ fit canvas ทุกหน้า

---

## [FILE STRUCTURE]

```
miniatm/
├── design.md          ← ไฟล์นี้ — system overview + canvas
├── foundation/
│   ├── colors.md      ← (TODO)
│   └── typography.md  ← (TODO)
├── pages/
│   └── home.md        ← (TODO)
└── assets/
    ├── icons/
    └── images/
```

---

## Figma Reference

| Item | File | Node |
|------|------|------|
| Home background (symbol) | ATM--CF- | 1728:83736 |
| M-Home-001-s1 (frame) | ATM--CF- | 5265:25804 |
