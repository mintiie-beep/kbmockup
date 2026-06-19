# Action Button — miniATM (ตู้เงินดี)
> Figma node: 25806:98142 (Button — ปุ่มอื่นๆ)
> ปุ่ม action ทั่วไปบน kiosk — มี 4 types: OTP, CTA (ย้อนกลับ), Next (ถัดไป), Mid (กลับหน้าหลัก)

---

## [OVERVIEW]

| Type | Size | ข้อความ | Icon |
|------|------|---------|------|
| **OTP** | auto × 68px | "ขอรหัส OTP ใหม่" | ไม่มี |
| **CTA** (ย้อนกลับ) | 200×88px | "ย้อนกลับ" | ← back icon (ซ้าย) |
| **Next** (ถัดไป) | 200×88px | "ถัดไป" | → next icon (ขวา) |
| **Mid** (กลับหน้าหลัก) | 300×88px | "กลับหน้าหลัก" | ไม่มี |

---

## [SHARED STYLES — ทุก type]

| Property | Value |
|----------|-------|
| Background | `#FFFFFF` (`var(--button/white)` / `var(--bg/white)`) |
| Border | 1px solid `#C0C0C0` (`var(--color/grey)` / `var(--stoke/grey)`) |
| Border radius | 20px |
| Shadow (Enabled) | `btn shadow 2` |
| Padding vertical | 16px |
| Align items | center |
| Justify content | center |

### Effects — btn shadow 2 (Enabled only)
```css
box-shadow:
  0px 1px 3px rgba(0, 94, 35, 0.30),
  0px 1px 4px rgba(0, 94, 35, 0.15);
```

---

## [STATES]

| State | Background | Shadow | Border | Opacity |
|-------|-----------|--------|--------|---------|
| **Enabled** | `#FFFFFF` | btn shadow 2 | `#C0C0C0` | 100% |
| **Focused** | `#F1F1F1` overlay | ไม่มี | `#C0C0C0` | 100% |
| **Disabled** | `#FFFFFF` | ไม่มี | `#C0C0C0` | **40%** |

### Focused State Details
- Background overlay: `#F1F1F1` (absolute, rounded, pointer-events-none)
- Inner shadow: `inset 1px 2px 2px 0px rgba(0,0,0,0.15)` (CTA, Mid) หรือ `inset 1px 2px 2px 1px rgba(0,0,0,0.15)` (OTP)

### Disabled State
```css
opacity: 0.4;
background: #ffffff;
/* ไม่มี shadow */
```

---

## [TYPE: OTP]

> Figma node: 25806:98164 (Enabled), 25806:98166 (Focused), 25806:98168 (Disabled)

| Property | Value |
|----------|-------|
| Width | auto (min-width: 100px) |
| Height | 68px |
| Padding | 16px 28px |

### Typography
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 (thai/Button/Button 3) |
| Size | 28px |
| Line height | normal |
| Letter spacing | -0.616px |
| Color | `#090909` |
| Align | center |

```
┌──────────────────────────────────┐
│      ขอรหัส OTP ใหม่             │  68px
└──────────────────────────────────┘
  px-28px auto-width
```

---

## [TYPE: CTA — ย้อนกลับ]

> Figma node: 25806:98170 (Enabled), 25806:98192 (Focused), 25806:98203 (Disabled)

| Property | Value |
|----------|-------|
| Width | 200px |
| Height | 88px |
| Padding right | 4px |
| Gap (icon + text) | 16px |

### Icon
| Property | Value |
|----------|-------|
| Size | 32×32px |
| Type | Back arrow (←) |
| Position | ซ้ายของ text |

### Typography
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 (thai/Button/Button 2) |
| Size | 36px |
| Line height | 50.4px |
| Letter spacing | -0.792px |
| Color | `#090909` |

```
┌──────────────────────┐
│   ←   ย้อนกลับ      │  88px
└──────────────────────┘
  200px  pr-4px  gap-16px
```

---

## [TYPE: Next — ถัดไป]

> Figma node: 25806:98181 (Enabled only)

| Property | Value |
|----------|-------|
| Width | 200px |
| Height | 88px |
| Padding right | 4px |
| Gap (text + icon) | 16px |

### Icon
| Property | Value |
|----------|-------|
| Size | 32×32px |
| Type | Next arrow (→) |
| Position | ขวาของ text |

### Typography (เหมือน CTA)
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 |
| Size | 36px |
| Line height | 50.4px |
| Letter spacing | -0.792px |
| Color | `#090909` |

```
┌──────────────────────┐
│    ถัดไป   →         │  88px
└──────────────────────┘
  200px
```

---

## [TYPE: Mid — กลับหน้าหลัก]

> Figma node: 25806:98214 (Enabled), 25806:98220 (Focused), 25806:98226 (Disabled)

| Property | Value |
|----------|-------|
| Width | 300px |
| Height | 88px |
| Padding | 16px 28px |
| Gap | 16px |
| Icon | ไม่มี |

### Typography (เหมือน CTA)
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 (thai/Button/Button 2) |
| Size | 36px |
| Line height | 50.4px |
| Letter spacing | -0.792px |
| Color | `#090909` |
| Align | center |

```
┌────────────────────────────────────┐
│          กลับหน้าหลัก              │  88px
└────────────────────────────────────┘
  300px  px-28px
```

---

## [CSS SNIPPET]

```css
/* Base — shared */
.action-btn {
  background: #ffffff;
  border: 1px solid #c0c0c0;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 16px;
  cursor: pointer;
}

/* Enabled shadow */
.action-btn--enabled {
  box-shadow:
    0px 1px 3px rgba(0, 94, 35, 0.30),
    0px 1px 4px rgba(0, 94, 35, 0.15);
}

/* Focused */
.action-btn--focused {
  background: #f1f1f1;
  box-shadow: inset 1px 2px 2px 0px rgba(0, 0, 0, 0.15);
}

/* Disabled */
.action-btn--disabled {
  opacity: 0.4;
}

/* OTP */
.action-btn--otp {
  height: 68px;
  padding: 16px 28px;
}

/* CTA / Next */
.action-btn--cta,
.action-btn--next {
  width: 200px;
  height: 88px;
  gap: 16px;
  padding-right: 4px;
}

/* Mid */
.action-btn--mid {
  width: 300px;
  height: 88px;
  padding: 16px 28px;
  gap: 16px;
}

/* Label — Button 2 (CTA, Mid, Next) */
.action-btn--cta .btn-label,
.action-btn--mid .btn-label,
.action-btn--next .btn-label {
  font-family: 'Sarabun', sans-serif;
  font-weight: 600;
  font-size: 36px;
  line-height: 50.4px;
  letter-spacing: -0.792px;
  color: #090909;
}

/* Label — Button 3 (OTP) */
.action-btn--otp .btn-label {
  font-family: 'Sarabun', sans-serif;
  font-weight: 600;
  font-size: 28px;
  line-height: normal;
  letter-spacing: -0.616px;
  color: #090909;
}

/* Icon */
.action-btn-icon {
  width: 32px;
  height: 32px;
  flex-shrink: 0;
}
```

---

## Figma Reference

| Item | File | Node |
|------|------|------|
| Button group | ATM--CF- | 25806:98142 |
| OTP — Enabled | ATM--CF- | 25806:98164 |
| OTP — Focused | ATM--CF- | 25806:98166 |
| OTP — Disabled | ATM--CF- | 25806:98168 |
| CTA — Enabled | ATM--CF- | 25806:98170 |
| CTA — Focused | ATM--CF- | 25806:98192 |
| CTA — Disabled | ATM--CF- | 25806:98203 |
| Next — Enabled | ATM--CF- | 25806:98181 |
| Mid — Enabled | ATM--CF- | 25806:98214 |
| Mid — Focused | ATM--CF- | 25806:98220 |
| Mid — Disabled | ATM--CF- | 25806:98226 |
