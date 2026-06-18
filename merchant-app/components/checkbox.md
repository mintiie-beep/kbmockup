# Checkbox — Merchant App DS
> Figma node: 9203:15972 | 4 Variants

---

## [API]

### Props
| Prop | Values | Default |
|------|--------|---------|
| `property1` | `Default` \| `Selected` \| `Disable` \| `Error` | `Default` |

### Layout Variants
| Type | Description |
|------|-------------|
| `One line` | Single-line label ข้างขวา |
| `Many line` | Multi-line label — checkbox align top |

---

## [COLOR]

### Row Container — Fill & Stroke by State

| State | Fill | Stroke |
|-------|------|--------|
| Default | `#FFFFFF` | `#CEE6D9` |
| Selected | `#F3F9F6` | `#CEE6D9` |
| Disable | `#F2F2F2` | `#CECECE` |
| Error | `#FFFFFF` | `#EA1E30` |

### Checkbox Icon Colors
| State | Box Fill | Box Border | Checkmark |
|-------|----------|-----------|-----------|
| Default | white | `#CEE6D9` | — |
| Selected | `#0B8041` | `#0B8041` | white |
| Disable | `#F2F2F2` | `#CECECE` | — |
| Error | white | `#EA1E30` | — |

---

## [STRUCTURE]

### Row Container
| Property | Value |
|----------|-------|
| Height | 56px (Hug) |
| Width | 343px (Fill) |
| Padding (all) | 16px |
| Gap (checkbox ↔ label) | 12px |
| Border radius | 8px |
| Border width | 1px |

### Checkbox Icon Box
| Property | Value |
|----------|-------|
| Size | 20 × 20px |
| Border radius | 4px |

### Usage: Text Alignment
| Layout | Checkbox vertical align |
|--------|------------------------|
| One line | Center |
| Many line | **Top** |

---

## [TYPOGRAPHY]

| Element | Token | Size/LH | Weight |
|---------|-------|---------|--------|
| Label — Default/Error | `Body/Body 2` | 14px / 22px | regular |
| Label — Selected | `Body/Body 2` | 14px / 22px | **bold** |
| Label — Disable | `Body/Body 2` | 14px / 22px | regular (muted) |

---

## [STATES]

| State | Row bg | Row border | Checkbox | Label |
|-------|--------|-----------|----------|-------|
| Default | white | `#CEE6D9` | white + `#CEE6D9` border | regular |
| Selected | `#F3F9F6` | `#CEE6D9` | `#0B8041` filled + ✓ | **bold** |
| Disable | `#F2F2F2` | `#CECECE` | grey (no check) | muted |
| Error | white | `#EA1E30` | white + `#EA1E30` border | regular |

---

## [ACCESSIBILITY]

- ใช้ `<input type="checkbox">` พร้อม `<label>` ที่ผูก `for` / `id` เสมอ
- Disable: ใช้ `disabled` attribute
- Error: ใช้ `aria-invalid="true"` + `aria-describedby` ชี้ไป error message
- Many-line layout: label wrap ตามธรรมชาติ ไม่ตัด
