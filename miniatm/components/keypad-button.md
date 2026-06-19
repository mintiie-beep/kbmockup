# Keypad Button — miniATM (ตู้เงินดี)
> Figma node: 1802:135773 (Keypad — State=Default, State=Error)
> Component ใช้สำหรับรับ input ตัวเลขบน kiosk touchscreen

---

## [OVERVIEW]

Keypad ประกอบด้วย 2 ส่วน:
1. **Text Input Display** — แสดงตัวเลขที่ผู้ใช้กด (ซ้ายบน)
2. **Numpad** — กริด 3×4 ปุ่มตัวเลข 0–9 + ปุ่ม "ลบ" (ขวา)

ใช้คู่กัน layout แนวนอน: Text Input (584px) | gap 96px | Numpad (454px)

---

## [KEY BUTTON — Individual Key]

> Figma component: `Rectangle` — node `1865:12617`

| Property | Value |
|----------|-------|
| Width | 138px |
| Height | 100px |
| Background | `#FFFFFF` |
| Border | 1.147px solid `#C0C0C0` |
| Border radius | 20px (`--radiant`) |
| Shadow | `drop-shadow(0px 4.589px 4.589px 0px rgba(0,0,0,0.08))` |

### Typography — Number (1–9, 0)
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 |
| Size | 48px |
| Line height | normal |
| Letter spacing | -1.056px |
| Color | `#090909` (`Text/Black`) |
| Align | center |

### Typography — "ลบ" (Delete)
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 |
| Size | 38px |
| Letter spacing | -0.836px |
| Color | `#090909` |
| Align | center |

---

## [NUMPAD GRID]

> Container: 454×460px

| Property | Value |
|----------|-------|
| Layout | flex-wrap, content-center |
| Gap | 20px |
| Columns | 3 |
| Rows | 4 |

### Key Layout
```
┌───────────┬───────────┬───────────┐
│     1     │     2     │     3     │
├───────────┼───────────┼───────────┤
│     4     │     5     │     6     │
├───────────┼───────────┼───────────┤
│     7     │     8     │     9     │
├───────────┼───────────┼───────────┤
│  [empty]  │     0     │    ลบ     │
└───────────┴───────────┴───────────┘
  138px       138px       138px
  gap 20px
```

> หมายเหตุ: แถวสุดท้ายมี 2 ปุ่ม (0 + ลบ) วางชิดขวา — ไม่มีปุ่มแรก

---

## [TEXT INPUT DISPLAY]

> Container: 584×111px, rounded-[20px]

| Property | Value |
|----------|-------|
| Width | 584px |
| Height | 111px |
| Background | `rgba(255,255,255,0.8)` |
| Border radius | 20px |
| Inner shadow | `inset 0px 4px 4px 0px rgba(0,0,0,0.08)` |

### Input Digits
| Property | Value |
|----------|-------|
| Font | Sarabun SemiBold 600 (thai/InputText/InputText 2) |
| Size | 56px |
| Line height | 100% (56px) |
| Letter spacing | 0 |
| Color | `#090909` |
| Digit width | 36px each |

### Input Groups (13 digits)
```
[0]  [0][0][0][0]  [0][0][0][0][0]  [0][0]  [0]
 1     2  3  4  5    6  7  8  9 10   11 12   13
```
แบ่งเป็น 4 กลุ่มด้วย gap 16px

### Guide Underline (empty state)
- เส้นใต้แต่ละ digit: border-bottom: 3px solid #CCDECD
- ความสูง 83px ต่อ slot

---

## [STATES]

| State | Visual |
|-------|--------|
| **Default** | Text input bg ขาว 80%, border ปกติ |
| **Error** | Text input border สีแดง `#A90000` (1px) + error message |

### Error State
- Border: 1px solid #A90000
- แสดง error message ใต้ input: icon + ข้อความ "รหัส OTP ไม่ถูกต้อง กรุณากรอกใหม่อีกครั้ง"
- Font: Sarabun SemiBold 28px, สีแดง #A90000

---

## [HELPER / CONTEXT ELEMENTS]

### Helper Text (ใต้ input)
```
บริษัทเก็บรวบรวมข้อมูลเพื่อการยืนยันตัวตนเท่านั้น
```
| Property | Value |
|----------|-------|
| Font | Sarabun Medium 500 (Body 1) |
| Size | 28px |
| Line height | 42px |
| Color | `#FFFFFF` (สีขาว — บน bg เขียว) |

### OTP Row (แสดงเมื่อหน้าต้องการ OTP)
Layout แนวนอน: ข้อความซ้าย + ปุ่ม "ขอ OTP อีกครั้ง" ขวา

**ข้อความ OTP:**
- "รหัส OTP จะหมดอายุใน 59 วินาที" — 24px Regular, lh 36px
- "(หมายเลขอ้างอิง OKA4571)" — 20px Regular

**ปุ่ม "ขอ OTP อีกครั้ง":**
- เหมือน OTP button ใน action-button.md — 68px h, radius 20px, btn shadow 2

---

## [CSS SNIPPET]

```css
/* Individual keypad key */
.keypad-key {
  width: 138px;
  height: 100px;
  background: #ffffff;
  border: 1.147px solid #c0c0c0;
  border-radius: 20px;
  box-shadow: 0px 4.589px 4.589px 0px rgba(0, 0, 0, 0.08);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.keypad-key-text {
  font-family: 'Sarabun', sans-serif;
  font-weight: 600;
  font-size: 48px;
  color: #090909;
  letter-spacing: -1.056px;
}

.keypad-key-delete {
  font-size: 38px;
  letter-spacing: -0.836px;
}

/* Numpad grid */
.numpad {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  width: 454px;
  height: 460px;
  align-content: center;
  align-items: center;
}

/* Text input display */
.keypad-input-display {
  width: 584px;
  height: 111px;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 20px;
  box-shadow: inset 0px 4px 4px 0px rgba(0, 0, 0, 0.08);
}

/* Error state */
.keypad-input-display.error {
  border: 1px solid #a90000;
}
```

---

## Figma Reference

| Item | File | Node |
|------|------|------|
| Keypad — Default | ATM--CF- | 1802:135821 |
| Keypad — Error | ATM--CF- | 1802:135903 |
| Individual key (Rectangle) | ATM--CF- | 1865:12617 |
| Keypad container | ATM--CF- | 1802:135773 |
