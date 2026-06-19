# Service Button — miniATM (ตู้เงินดี)
> Figma node: 1711:79676 (Button — เลือกบริการ)
> ปุ่มเลือกบริการ/ธนาคาร บน kiosk — มี 2 variants: Default (text only) และ Menu-Icon (text + logo)

---

## [OVERVIEW]

| Property | Value |
|----------|-------|
| Component name | Button (Service Selection) |
| Size | 446×140px |
| Variants | Default, Menu-Icon |
| States | Enabled (เดียว — ไม่มี Disabled/Focused ใน component นี้) |

---

## [SHARED STYLES — ทุก variant]

| Property | Value |
|----------|-------|
| Background | `#FFFFFF` (`var(--button/white)`) |
| Border | 1px solid `#C0C0C0` (`var(--stoke/grey)`) |
| Border radius | 20px (`var(--radiant)`) |
| Shadow | `btn shadow 2` — ดู Effects |
| Padding vertical | 16px |
| Overflow | clip |

### Effects — btn shadow 2
```css
box-shadow:
  0px 1px 6px 4px rgba(0, 94, 35, 0.30),
  0px 1px 8px 2px rgba(0, 94, 35, 0.15);
```

---

## [VARIANT: Default — ไม่มีรูป]

> Figma node: 1711:79677

ใช้สำหรับเลือกบริการทั่วไป เช่น "ฝากเงิน", "ถอนเงิน"

| Property | Value |
|----------|-------|
| Justify content | center |
| Padding horizontal | 32px |
| Icon | ไม่มี |

### Typography
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 (thai/Button/Button 1) |
| Size | 38px |
| Line height | 100% (38px) |
| Letter spacing | -0.836px (≈ -2.2px) |
| Color | `#090909` (`var(--text/black)`) |
| Align | center |

```
┌─────────────────────────────────────────────────────┐
│                                                     │
│                    ฝากเงิน                          │
│                                                     │
└─────────────────────────────────────────────────────┘
  446px × 140px
```

---

## [VARIANT: Menu-Icon — มีรูป]

> Figma node: 1958:81714

ใช้สำหรับเลือกธนาคาร/ผู้ให้บริการ เช่น "กสิกรไทย" + logo

| Property | Value |
|----------|-------|
| Justify content | space-between |
| Padding left | 60px |
| Padding right | 48px |
| Icon size | 100×100px |
| Icon position | right side |
| Icon shape | วงกลม — circular logo |

### Typography (เหมือน Default)
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 |
| Size | 38px |
| Letter spacing | -0.836px |
| Color | `#090909` |
| Align | center (text อยู่ซ้าย, center ใน column) |

### Icon Container
| Property | Value |
|----------|-------|
| Size | 100×100px |
| Overflow | clip |
| Position | right side of button |

```
┌─────────────────────────────────────────────────────┐
│                                                     │
│    กสิกรไทย                    ⊙                   │
│                                                     │
└─────────────────────────────────────────────────────┘
  ← pl-60px text center →    ← icon 100px pr-48px →
  446px × 140px
```

---

## [CSS SNIPPET]

```css
/* Base — shared */
.service-btn {
  width: 446px;
  height: 140px;
  background: #ffffff;
  border: 1px solid #c0c0c0;
  border-radius: 20px;
  box-shadow:
    0px 1px 6px 4px rgba(0, 94, 35, 0.30),
    0px 1px 8px 2px rgba(0, 94, 35, 0.15);
  display: flex;
  align-items: center;
  padding: 16px;
  overflow: hidden;
}

/* Variant: Default */
.service-btn--default {
  justify-content: center;
  padding-left: 32px;
  padding-right: 32px;
}

/* Variant: Menu-Icon */
.service-btn--icon {
  justify-content: space-between;
  padding-left: 60px;
  padding-right: 48px;
}

/* Label */
.service-btn-label {
  font-family: 'Sarabun', sans-serif;
  font-weight: 600;
  font-size: 38px;
  line-height: 1;
  letter-spacing: -0.836px;
  color: #090909;
  text-align: center;
  white-space: nowrap;
}

/* Icon */
.service-btn-icon {
  width: 100px;
  height: 100px;
  overflow: hidden;
  flex-shrink: 0;
}
```

---

## [USAGE EXAMPLES]

ปุ่มบริการหลัก (Default):
- ฝากเงิน
- ถอนเงิน
- โอนเงิน
- ชำระบิล

ปุ่มเลือกธนาคาร (Menu-Icon):
- กสิกรไทย + KBank logo
- กรุงไทย + KTB logo
- ไทยพาณิชย์ + SCB logo

---

## Figma Reference

| Item | File | Node |
|------|------|------|
| Service Button container | ATM--CF- | 1711:79676 |
| Variant: Default | ATM--CF- | 1711:79677 |
| Variant: Menu-Icon | ATM--CF- | 1958:81714 |
