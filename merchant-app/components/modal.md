# Modal / Bottom Sheet — Merchant App DS
> 3 patterns: Center Modal · Alert Bottom Sheet · Search Bottom Sheet

---

## [API]

### Pattern Types

| Type | Trigger | Position | Page |
|------|---------|----------|------|
| `Center Modal` | Action required / notification | Screen center | Home page เท่านั้น |
| `Alert Bottom Sheet` | Alert / confirm / info | Bottom center | หน้าอื่นๆ ทุกหน้า |
| `Search Bottom Sheet` | Dropdown open | Bottom, slides up | ทุกหน้าที่มี Dropdown |

### Center Modal Props
| Prop | Values |
|------|--------|
| icon | `warning` \| `success` \| `info` \| `image` |
| button | single CTA only |

### Alert Bottom Sheet Props
| Prop | Values |
|------|--------|
| `property1` | `Default` (1 button) \| `Variant5` (2 buttons) |

---

## [COLOR]

### Overlay
| Token | Value |
|-------|-------|
| `Overlay/Overlay BG` | rgba(0,0,0,~0.5) |

### Alert Icon Colors
| State | Color |
|-------|-------|
| Warning / Error | red/600 #EA1E30 |
| Success | green/600 #0B8041 |
| Info / General | grey |

---

## [STRUCTURE]

### 1 — Center Modal (Home page)

| Property | Value |
|----------|-------|
| Card width | 312px |
| Padding LR | 24px |
| Padding TB | 32px |
| Gap (vertical) | 20px |
| Border radius | 16px |

### 2 — Alert Bottom Sheet (other pages)

| Property | Value |
|----------|-------|
| Width | 360px (Fill) |
| Padding Top | 24px |
| Padding LR | 24px |
| Padding Bottom | 64px |
| Gap (vertical) | 20px |
| Border radius | top-left=16, top-right=16, bottom=0 |

### 3 — Search Bottom Sheet (Dropdown)

| Property | Value |
|----------|-------|
| Width | 360px (Fill) |
| Height | Hug (max ~75% screen) |
| Option item height | 56px |
| Selected indicator | ✓ green right-aligned |

### Search States

| State | List |
|-------|------|
| Default | Full list |
| Typing | Filtered results |
| Selected | Selected item shows ✓ |
| No result | Empty state message |

---

## [TYPOGRAPHY]

| Element | Style | Weight |
|---------|-------|--------|
| Modal title | `Heading/Header 2` 18px/30px | Bold |
| Modal body | `Body/Body 2` 14px/22px | Regular |
| Option item label | `Body/Body 1` 16px/26px | Regular |

---

## [ACCESSIBILITY]

- Modal: `role="dialog"` + `aria-modal="true"` + `aria-labelledby`
- Overlay: click outside → close (ยกเว้น force-action modal)
- Close button: `aria-label="ปิด"`
- Option item: `role="option"` + `aria-selected`

---

## Figma Node Reference

| Component | Node |
|-----------|------|
| Center Modal | 23924:399226 |
| Alert Bottom Sheet | 9203:16476 |
| Search Bottom Sheet | 271:22510 |
