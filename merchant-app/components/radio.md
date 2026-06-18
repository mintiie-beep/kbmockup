# Radio Button — Merchant App DS
> 5 component types | Page 37

---

## [API]

### Radio Button Types (5 components)

| Type | Node | Description |
|------|------|-------------|
| `Radio button` | 9203:15938 | Basic — circle + label |
| `Radio button with Description` | 9203:15951 | Circle + label + description subtext |
| `Radio button with Description + Amount` | 9203:16075 | Payment option — circle + title + amount + desc |
| `Icon Radio button` | 9203:16012 | Card — icon + title + subtext |
| `Text Radio button` | 9203:16040 | Compact card — text only |

### Shared Props (Basic & With Description)
| Prop | Values | Default |
|------|--------|---------|
| `property1` | `Default` \| `Selected` \| `Disable` \| `Error` | `Default` |

---

## [COLOR]

### Basic & With Description — Row Tokens

| State | Fill | Stroke |
|-------|------|--------|
| Default | `BG/white BG` | `Stroke, Line/Green20` |
| Selected | `BG/Green5` | `Stroke, Line/Green20` |
| Disable | `Disable/Disable BG` | `Disable/Disable Stroke` |
| Error | `BG/white BG` | `State/Negative` |

### Text Radio button — Card Tokens (different selected stroke!)

| State | Fill | Stroke |
|-------|------|--------|
| Default | `BG/white BG` | `Stroke, Line/Green20` |
| **Selected** | `BG/Green5` | **`Stroke, Line/Primary Green`** |
| Disable | `Disable/Disable BG` | `Disable/Disable Stroke` |

### Token → Primitive mapping
| Token | Hex | Notes |
|-------|-----|-------|
| `BG/white BG` | #FFFFFF | White |
| `BG/Green5` | #F3F9F6 | Selected bg |
| `Stroke, Line/Green20` | #CEE6D9 | Default border |
| `Stroke, Line/Primary Green` | #0B8041 | Selected border (Text Radio) |
| `Disable/Disable BG` | #F2F2F2 | Disabled bg |
| `Disable/Disable Stroke` | #CECECE | Disabled border |
| `State/Negative` | #EA1E30 | Error border |

### Radio Circle Icon Colors
| State | Outer ring | Inner dot |
|-------|-----------|-----------|
| Default | green/200 border, white fill | — |
| Selected | green/600 border + fill | white dot (center) |
| Disable | grey/300 border, grey fill | — |
| Error | red/600 border, white fill | — |

---

## [STRUCTURE]

### Basic Radio button row
| Property | Value |
|----------|-------|
| Height | 56px (Hug) |
| Width | 343px (Fill) |
| Padding (all sides) | 16px |
| Gap (circle ↔ label) | 12px |
| Border radius | 8px |
| Border width | 1px Inside |

### Inner Structure — Basic
```
Radio row (horizontal, gap: 12px, padding: 16px)
├── Radio circle (20px × 20px)
│   └── [inner dot — Selected only]
└── Label text (Fill width)
```

### Usage — Alignment rule
| Content | Circle alignment |
|---------|----------------|
| One line text | Center |
| Many line text | **Top** |

---

## [TYPOGRAPHY]

### Basic & With Description
| Element | Size/LH | Weight |
|---------|---------|--------|
| Label — Default/Disable/Error | 14px / 22px | regular |
| Label — Selected | 14px / 22px | **bold** |
| Description subtext | 12px / 18px | regular |

---

## [STATES]

### Basic Radio button
| State | Row bg | Border | Circle | Label |
|-------|--------|--------|--------|-------|
| Default | white | #CEE6D9 | white + #CEE6D9 | regular |
| Selected | #F3F9F6 | #CEE6D9 | #0B8041 + white dot | **bold** |
| Disable | #F2F2F2 | #CECECE | grey (no dot) | muted |
| Error | white | #EA1E30 | white + #EA1E30 | regular |

### Key Difference: Stroke Token
- Basic/WithDesc Selected → `Stroke, Line/Green20` (green/200 — subtle)
- Text Radio Selected → `Stroke, Line/Primary Green` (green/600 — prominent)

---

## [ACCESSIBILITY]

- ใช้ `<input type="radio">` ในกลุ่ม `name` เดียวกันเสมอ
- ใช้ `<fieldset>` + `<legend>` สำหรับกลุ่ม radio
- Disable: `disabled` attribute บน `<input>`
- Error: `aria-invalid="true"` + `aria-describedby`
