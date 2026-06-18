# Input Field — Merchant App DS
> Figma node: 9203:16133 | 18 Variants

---

## [API]

### Types
| Type | Description |
|------|-------------|
| `Input Field` | Text input พื้นฐาน + clear button |
| `Dropdown` | Select พร้อม chevron icon (▼/▲) |
| `Date` | Date picker พร้อม calendar icon |

### Props
| Prop | Values | Default |
|------|--------|---------|
| `type` | `Input Field` \| `Dropdown` \| `Date` | `Input Field` |
| `state` | `Default` \| `Focus` \| `Focus + Typing` \| `Filled` \| `Disable` \| `Disable + Filled` \| `Error` \| `Error + Filled` \| `Error + Focus + Typing` | `Default` |

---

## [COLOR]

### Input Box — Fill & Stroke by State

| State | Fill Token | Stroke Token |
|-------|-----------|--------------|
| Default | `BG/white BG` | `Stroke, Line/Green20` |
| Focus | `BG/white BG` | `Stroke, Line/Green20` |
| Filled | `BG/white BG` | `Stroke, Line/Green20` |
| Disable | `Disable/Disable BG` | `Stroke, Line/Stroke Grey` |
| Error | `BG/white BG` | `State/Negative` |

### Token → Primitive mapping
| Token | → Primitive | Hex |
|-------|------------|-----|
| `BG/white BG` | — | #FFFFFF |
| `Stroke, Line/Green20` | color/green/200 | #CEE6D9 |
| `Stroke, Line/Stroke Grey` | color/grey/300 | #CECECE |
| `Disable/Disable BG` | color/grey/100 | #F2F2F2 |
| `State/Negative` | color/red/600 | #EA1E30 |

### Text Colors
| Element | State | Color |
|---------|-------|-------|
| Placeholder | Default/Focus | `alias/color/text/muted` (grey/600) |
| Input text | Filled/Typing | `alias/color/text/default` (grey/900) |
| Floating label | Focus/Filled | `alias/color/text/muted` (grey/600) |
| Floating label | Error | `State/Negative` (red/600) |
| Description | Default | `alias/color/text/muted` (grey/600) |
| Description | Error | `State/Negative` (red/600) |

---

## [STRUCTURE]

### Dimensions
| Property | Value |
|----------|-------|
| Input box height | 56px |
| Padding left | 16px |
| Padding right | 8px |
| Border radius | 8px |
| Border width | 1px (Inside) |
| Gap (input ↔ description) | 8px |

### Inner Structure
```
InputField (vertical auto layout, gap: 8px)
├── Input (Frame: 56px height, horizontal layout)
│   ├── [floating label — when focus/filled]
│   ├── text (placeholder / input value)
│   └── [trailing icon: × clear / ▼ chevron / 📅 calendar]
└── Description (helper/error text)
```

### Label Behavior (Floating Label Pattern)
| State | Label visibility |
|-------|-----------------|
| Default | Hidden (placeholder shown) |
| Focus | Shown small above cursor |
| Filled | Shown small above input text |

---

## [TYPOGRAPHY]

| Element | Token | Size/LH | Weight |
|---------|-------|---------|--------|
| Placeholder text | `Input/Input Text 1` | 16px / 24px | regular |
| Input text (value) | `Input/Input Text 1` | 16px / 24px | regular |
| Floating label (active) | `Input/Input Text 4` | 10px / 16px | regular |
| Description/helper | `alias/typography/body-sm` | 12px / 18px | regular |

---

## [STATES]

| State | Visual |
|-------|--------|
| Default | White bg, green/200 border, placeholder |
| Focus | White bg, green/200 border, floating label + cursor |
| Filled | White bg, green/200 border, floating label + value |
| Disable | Grey bg, grey border, placeholder muted |
| Error | White bg, red border, red description |

### Trailing Icons
| Type | State | Icon |
|------|-------|------|
| Input Field | Focus / Typing | × (clear) |
| Dropdown | Default/Filled | ▼ |
| Dropdown | Focus | ▲ |
| Date | All | 📅 |

---

## [ACCESSIBILITY]

- Floating label: ผูก `<label for>` กับ `<input id>` เสมอ
- Error state: `aria-invalid="true"` + `aria-describedby`
- Disable state: `disabled` attribute
- Clear button (×): `aria-label="Clear input"`
