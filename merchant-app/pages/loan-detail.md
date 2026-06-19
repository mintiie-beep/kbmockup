# Loan Detail — รายละเอียดสินเชื่อ
> Figma node: 481:38608 (KBao — Loan Detail)
> หน้าแสดงรายละเอียดสินเชื่อก่อนเริ่มกรอกฟอร์ม — ผู้กู้อ่านเงื่อนไขแล้วกด "สมัครสินเชื่อ"

---

## [OVERVIEW]

### Purpose
แสดงข้อมูลสินเชื่อ ได้แก่ Hero picture, คุณสมบัติผู้กู้, เอกสารที่ต้องใช้
ก่อนนำ user เข้าสู่ form flow

### Background
| Property | Value |
|----------|-------|
| Fill | `#FFFFFF` (white) |
| Font | LINE Seed Sans TH App / Noto Sans Thai (web fallback) |

---

## [STRUCTURE]

```
Status Bar (44px)
App Header ("รายละเอียดสินเชื่อ", drop-shadow)
─────────────────
Content (scroll, pt-24 px-16 pb-64, gap-48 between blocks)
  ├── Detail Block (gap-24)
  │   ├── Hero Picture (gray placeholder)
  │   └── Inner Detail (gap-16)
  │       ├── Page Title (loan name 2 lines)
  │       └── Section Group (gap-24)
  │           ├── คุณสมบัติของผู้กู้เบื้องต้น
  │           └── เอกสารการสมัครสินเชื่อ
  └── Button: สมัครสินเชื่อ
```

---

## [COMPONENTS]

### 1 — App Header
| Property | Value |
|----------|-------|
| Height | 56px |
| Background | `#FFFFFF` |
| Shadow | `drop-shadow 0 4px 4px rgba(0,0,0,0.05)` |
| Title | "รายละเอียดสินเชื่อ" — Heading/Header 3 (16px Bold) centered |
| Left | Back arrow icon |
| Right | More (⋮) icon |

---

### 2 — Hero Picture
| Property | Value |
|----------|-------|
| Width | 100% (328px in 360px frame) |
| Height | 246px |
| Border radius | 12px |
| object-fit | cover |
| Placeholder | bg `#D0D0D0`, label "รอรูปภาพ Hero" |
| **ถ้ามีรูปจริง** | ใช้รูปจาก Figma asset ตามแต่ละ loan type |

---

### 3 — Page Title
| Property | Value |
|----------|-------|
| Line 1 | "การสมัครสินเชื่อ" — Heading/Header 1 (20px Bold), `#000000` |
| Line 2 | ชื่อสินเชื่อ เช่น "สินเชื่อ เคบาว ผ่อนได้" — Heading/Header 1 (20px Bold), `#0B8041` |
| Line height | 32px |

---

### 4 — Section Label
| Property | Value |
|----------|-------|
| Style | Heading/Header 3 (16px Bold), `#000000` |
| Line height | 24px |

---

### 5 — Criteria / Doc List Box
| Property | Value |
|----------|-------|
| Background | `BG/Content BG` — `#F8F8F8` |
| Border radius | 8px |
| Padding | 12px |
| Gap between items | 12px |
| Item layout | flex row, gap 8px, items-start |
| Icon | 24×24px (ดูหัวข้อถัดไป) |
| Text | Body/Body 1 (16px Regular), `#000000`, line-height 26px |

#### Criteria Icon (คุณสมบัติ)
| Property | Value |
|----------|-------|
| Shape | วงกลม 24px |
| Fill | `#0B8041` (green) |
| Inner | White checkmark ✓ |

#### Document Icon (เอกสาร)
| Property | Value |
|----------|-------|
| Shape | Document/ID card 24px |
| Fill | `#0B8041` (green) |
| Inner | White lines |

---

### 6 — Primary Button
| Property | Value |
|----------|-------|
| Label | "สมัครสินเชื่อ" |
| Height | 52px |
| Width | 100% |
| Background | `Primary/Primary Green` — `#0B8041` |
| Border radius | 8px |
| Font | Button/Button 1 (18px Bold), white |
| Shadow | `0 4px 8px rgba(11,128,65,0.35)` |

---

## [CONTENT PER LOAN TYPE]

> Hero image และ Page Title Line 2 เปลี่ยนตาม loan type
> Section คุณสมบัติ + เอกสาร อาจต่างกันตาม product — เพิ่ม column ถ้ามี product ใหม่

| Field | เคบาว ผ่อนได้ (มือถือ & ไฟฟ้า) | หมุนเวียน | พนักงาน | เพื่อการศึกษา |
|-------|-------------------------------|----------|--------|--------------|
| Hero image | รูปสินค้า / บัตรสมาชิก | — | — | — |
| Page title line 2 | สินเชื่อ เคบาว ผ่อนได้ | สินเชื่อหมุนเวียน | สินเชื่อพนักงาน | สินเชื่อเพื่อการศึกษา |
| คุณสมบัติ | บุคคลธรรมดา ไทย / อายุ 20-70 / สมาชิก CJ / มีเบอร์รับ OTP | TBD | TBD | TBD |
| เอกสาร | บัตรประชาชนผู้กู้+ผู้ค้ำ / รูปแผนที่ | TBD | TBD | TBD |

---

## [RULES]

- **Hero picture** → ใช้ gray placeholder `#D0D0D0` ไปก่อน ขอรูปจาก user ก่อน deploy จริง
- **Page title line 2** → สีเขียว `#0B8041` เสมอ ไม่ว่า loan type ไหน
- **Criteria/Doc items** → ซ่อน item ที่ไม่มีข้อมูล ไม่แสดง empty row
- **New loan type** → ขอ criteria + doc list จาก user ก่อน เพิ่ม column ในตารางนี้
- **ปุ่มสมัครสินเชื่อ** → นำ user ไปยัง form หน้าแรกของ loan type นั้น

---

## [COLOR]

| Element | Token | Hex |
|---------|-------|-----|
| Page bg | white | `#FFFFFF` |
| List box bg | `BG/Content BG` | `#F8F8F8` |
| Criteria/doc icon | `Icon/Icon Green` | `#0B8041` |
| Page title line 2 | `Text/Primary Green` | `#0B8041` |
| Item text | `Text/Text Black` | `#000000` |
| Section label | `Text/Text Black` | `#000000` |
| Primary button | `Primary/Primary Green` | `#0B8041` |

---

## [TYPOGRAPHY]

| Element | Figma Style | Size/LH | Weight |
|---------|-------------|---------|--------|
| App bar title | `Heading/Header 3` | 16/24px | Bold |
| Page title | `Heading/Header 1` | 20/32px | Bold |
| Section label | `Heading/Header 3` | 16/24px | Bold |
| Criteria/doc text | `Body/Body 1` | 16/26px | Regular |
| Button | `Button/Button 1` | 18/28px | Bold |

---

## Figma Node Reference

| Section | File | Node |
|---------|------|------|
| Loan Detail (Default) | KBao | 481:38608 |
