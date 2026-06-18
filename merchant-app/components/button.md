# Button — Merchant App DS
> Figma node: 83:1019 | Version: 1.1.0

An event or action is started by a button. Buttons let users do actions including submitting forms, showing or hiding UI elements, and navigating to new pages. The primary style should only be used once for the main call-to-action in each section.

---

## [API]

### Button Types
| Type | Description |
|------|-------------|
| `Basic Button` | Standard text + optional icon button |
| `Icon Button` | Square icon-only button |
| `Link Button` | Text link style |
| `Close Button` | Dismiss/close action |
| `Social Button` | OAuth: Google / Apple / Facebook |

### Props (Basic Button)
| Prop | Values | Default |
|------|--------|---------|
| `type` | `Primary` \| `Secondary` \| `Tertiary` \| `Ghost` | `Primary` |
| `size` | `Large` \| `Medium` \| `Small` | `Medium` |
| `state` | `Normal` \| `Hover` \| `Focus` \| `Press` \| `Disable` | `Normal` |
| `danger` | `Yes` \| `No` | `No` |
| `iconOnly` | `Yes` \| `No` | `No` |

---

## [COLOR]

### Primary (Danger=No)
> KBao implementation ใช้ `Primary/Primary Green` (green/600)

| State | Background | Text/Icon |
|-------|-----------|-----------|
| Normal | `#0B8041` | white |
| Hover | `#086634` | white |
| Press | `#064D27` | white |
| Disable | `#F2F2F2` | `#A6A6A6` |

### Secondary (Danger=No) — Outlined
| State | Background | Text/Icon | Border |
|-------|-----------|-----------|--------|
| Normal | transparent | `#262626` | `#262626` |
| Disable | transparent | `#BDBDBD` | `#CECECE` |

### Primary Danger=Yes
| State | Background | Text/Icon |
|-------|-----------|-----------|
| Normal | `#EA1E30` | white |
| Disable | `#FFE3E3` | `#FF8787` |

---

## [STRUCTURE]

### Height — KBao confirmed (node 14:1447)
| Size | Height |
|------|--------|
| Large | **52px** |
| Medium | ~40px |
| Small | ~36px |

### Padding — KBao Large button (confirmed)
| Direction | Value |
|-----------|-------|
| Left / Right | 16px |
| Top / Bottom | 12px |
| Gap icon↔text | 4px |

### Border Radius — KBao confirmed
| Variant | Radius |
|---------|--------|
| All buttons | **8px** |

---

## [TYPOGRAPHY]

| Size | Token | Size/LH | Weight |
|------|-------|---------|--------|
| Large | `Button/Button 1` | 18px / 28px | Bold |
| Medium | `Button/Button 2` | 14px / 22px | Bold |
| Small | `Button/Button 3` | 14px / 22px | Regular |

---

## [STATES]

| State | Trigger | Visual change |
|-------|---------|---------------|
| `Normal` | Default | Base style |
| `Hover` | Mouse over | Slightly darker bg |
| `Focus` | Keyboard tab | Border ring เพิ่ม |
| `Press` | Active click | Darker bg |
| `Disable` | disabled attr | Muted colors, pointer-events: none |

---

## [ACCESSIBILITY]

- Disable state: ใช้ `aria-disabled` แทน `disabled` ถ้าต้องการ tooltip
- Icon Button: ต้องมี `aria-label` เสมอ
- Focus state: มี visible focus ring

---

## Figma Node Reference
| Section | Node ID |
|---------|---------|
| Basic Button component | `83:1019` |
| Basic Button — Primary Large | `14:1447` |
| Basic Button — Primary | `83:1225` |
| Basic Button — Secondary | `1111:35940` |
