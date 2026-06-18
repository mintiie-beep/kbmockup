# Form Flow — Merchant App (PRIMO)
> หน้า form ทั้งหมดใน loan application flow | KBao Figma file

---

## [OVERVIEW]

### Flow Structure
- เรียงลำดับ: Product Selection → ข้อมูลลูกค้า → OTP → สัญญา → เซ็น → ผล

### Doc No. Banner Rule
**แสดง** เมื่อ: มี doc number แล้ว (หลัง product selection)
**ไม่แสดง** เมื่อ: Product Selection step เท่านั้น

Banner spec:
| Property | Value |
|----------|-------|
| Fill | `Secondary/Yellow BG` |
| Height | 34px |
| Text | "เลขที่เอกสารการสมัคร {doc_number}" |
| Position | Below app bar, above page content |

---

## [PAGES]

### 1 — Product Selection
**Node**: 9203:20561 | **Doc No. Banner**: ❌

### 2 — Personal Information
**Node**: KBao 315:24136 | **Doc No. Banner**: ✅

Components: App bar, Doc No. banner, Input Field, Checkbox, Button Primary

### 3 — Questionnaire
**Node**: KBao 984:73262 | **Doc No. Banner**: ✅

Components: App bar, Doc No. banner, Radio Button / Checkbox groups, Input Field, Button Primary

### 4 — OTP Verification
**Node**: KBao 1015:28778 | **Doc No. Banner**: ✅

#### Variants
| Variant | Purpose |
|---------|---------|
| Default | ยืนยันตัวตนผู้กู้ |
| Variant2 | ยินยอมเปิดเผยข้อมูล |

#### OTP Input Spec
| Property | Value |
|----------|-------|
| Boxes | 6 boxes |
| Active box | Green border (#0B8041) |
| Timer color | Primary Green |

### 5 — Contract & Consent
**Node**: KBao 1220:47796 | **Doc No. Banner**: ✅ สัญญา / ❌ ข้อมูลผลิตภัณฑ์

| Variant | Buttons |
|---------|---------|
| สัญญาสินเชื่อ | ปฏิเสธ (red) + ตอบรับสินเชื่อ (green) |
| ข้อมูลผลิตภัณฑ์ | ยืนกราน (green, full width) |

### 6 — Sign Contract
**Node**: KBao 1220:47975 | **Doc No. Banner**: ✅

Buttons: เซ็นใหม่อีกครั้ง (secondary) | ยืนยัน (primary green)

### 7 — Guarantor Review
**Node**: KBao 1355:92020 | **Doc No. Banner**: ❌ (แสดง warning banner แทน)

Warning banner: amber bg + text แจ้งผู้ค้ำให้ตรวจสอบข้อมูล

### 8 — Success
**Node**: KBao 1220:68522 | **Doc No. Banner**: ✅

---

## [COLOR]

| Element | Token | Hex |
|---------|-------|-----|
| Doc No. banner bg | `Secondary/Yellow BG` | #FFF9EA |
| ปฏิเสธ button | `State/Negative` | #EA1E30 |
| Primary green buttons | `Primary/Primary Green` | #0B8041 |

---

## [TYPOGRAPHY]

| Element | Style | Weight |
|---------|-------|--------|
| App bar title | `Heading/Header 3` 16px | Bold |
| Page H1 | `Heading/Header 1` 20px | Bold |
| Doc No. banner text | `Body/Body 3` 12px | Regular |
| Data table label | `Body/Body 2` 14px | Regular (muted) |
| Summary amount | `Number/Number 2` 18px | ExtraBold (green) |

---

## [ACCESSIBILITY]

- OTP boxes: `role="group"` + each box `inputmode="numeric"`
- Timer: `aria-live="polite"`
- Signature canvas: `aria-label="พื้นที่เซ็นลายมือชื่อ"`
- Data table: semantic `<table>` หรือ `<dl><dt><dd>`
