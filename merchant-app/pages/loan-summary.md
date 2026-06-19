# Loan Summary — สรุปรายละเอียดการขอสินเชื่อ
> Figma node: 339:71569 (KBao — Product Confirmation)
> หน้าสรุปรายละเอียดก่อนยืนยันสมัครสินเชื่อ — ใช้ร่วมกันทุก loan product

---

## [OVERVIEW]

### Purpose
แสดงข้อมูลสรุปทั้งหมดของการขอสินเชื่อให้ผู้กู้ตรวจสอบก่อนยืนยัน
มี warning ให้ตรวจสอบ → รายละเอียด → สรุปงวด → ปุ่มแก้ไข / ยืนยัน

### Background
| Property | Value |
|----------|-------|
| Fill | `#FFFFFF` (white) |
| Font | LINE Seed Sans TH App / Noto Sans Thai (web fallback) |

---

## [STRUCTURE]

```
Status Bar (44px)
App Header ("สมัครสินเชื่อ", drop-shadow)
─────────────────
Content (scroll, pt-16 px-16 pb-64, gap-48 between blocks)
  ├── Detail Block (gap-24)
  │   ├── Remark Tab (warning)
  │   ├── Section Title + Detail List (flat rows)
  │   └── Summary Box (green bg)
  └── Button Row (แก้ไข + ยืนยันสมัครสินเชื่อ)
```

---

## [COMPONENTS]

### 1 — App Header
| Property | Value |
|----------|-------|
| Height | 56px |
| Background | `#FFFFFF` |
| Shadow | `drop-shadow 0 4px 4px rgba(0,0,0,0.05)` |
| Title | "สมัครสินเชื่อ" — Heading/Header 3 (16px Bold) centered |
| Left | Back arrow icon |
| Right | More (⋮) icon |
| **ไม่มี** | Doc No. banner |

---

### 2 — Remark Tab (Warning)
| Property | Value |
|----------|-------|
| Background | `Secondary/Yellow BG` — `#FFF9EA` |
| Border radius | 8px |
| Padding | 8px 12px |
| Icon | Warning circle 36px — bg `#FFE28A`, icon `#C28000` |
| Text | "ผู้กู้ โปรดตรวจสอบความถูกต้องของข้อมูลก่อนการยืนยัน หากไม่ถูกต้องโปรดแจ้งพนักงานเพื่อแก้ไข" |
| Text style | Body/Body 3 (12px Regular), color `Secondary/Yellow Text` `#C28000` |

---

### 3 — Section Title
| Property | Value |
|----------|-------|
| Text | "รายละเอียดการขอสินเชื่อ" |
| Style | Heading/Header 1 (20px Bold), color `#000000` |
| Margin bottom | 16px |

---

### 4 — Detail List (Flat Rows)
> ไม่มี card wrapper / border — flat list เท่านั้น

| Property | Value |
|----------|-------|
| Layout | flex row, gap 8px |
| Gap between rows | 12px |
| Label | flex 1, Body/Body 1 (16px Regular), color `Text/Text Dark Grey` `#6D6D6D` |
| Value | flex 1, Body/Body 1 (16px Regular), color `Text/Text Black` `#000000`, text-align right |
| Multi-line value | ใช้ line-height 26px, wrap ตามปกติ |

---

### 5 — Summary Box
| Property | Value |
|----------|-------|
| Background | `BG/Green5` — `#F3F9F6` |
| Border radius | 8px |
| Padding | 16px 12px |
| Gap between rows | 12px |
| Label | Body/Body 1 (16px Regular), color `#000000` |
| Value | Heading/Header 2 (18px Bold), color `Text/Primary Green` `#0B8041`, text-align right |

---

### 6 — Button Row
| Property | Value |
|----------|-------|
| Layout | flex row, gap 12px |
| **แก้ไข** | flex 1, bg white, border white, radius 8px, py 12px, 18px Bold black, shadow `rgba(166,166,166,0.35)` |
| **ยืนยันสมัครสินเชื่อ** | width 210px, bg `#0B8041`, radius 8px, py 12px, 18px Bold white, shadow `rgba(11,128,65,0.35)` |

---

## [FIELDS PER LOAN TYPE]

> เพิ่ม loan type ใหม่ → เพิ่ม column ในตาราง
> ถ้า field ไม่มีในสินเชื่อนั้น ใส่ `—`

| Field | มือถือ & ไฟฟ้า | หมุนเวียน | พนักงาน | เพื่อการศึกษา |
|-------|--------------|----------|--------|--------------|
| ประเภทสินค้า | ✅ มือถือ / เครื่องใช้ไฟฟ้า | — | — | — |
| ยี่ห้อสินค้า | ✅ | — | — | — |
| สินค้า | ✅ (ชื่อรุ่น + สี) | — | — | — |
| ประเภทสินเชื่อ | — | — | — | ✅ สินเชื่อเพื่อการศึกษา |
| สถาบันการศึกษา | — | — | — | ✅ |
| หลักสูตร / สาขา | — | — | — | ✅ |
| ระยะเวลาเรียน | — | — | — | ✅ |
| วัตถุประสงค์ | — | — | — | ✅ |
| สินเชื่อ | ✅ เคบาว ผ่อนได้ | ✅ | ✅ | ✅ |
| ผู้ค้ำประกันสินเชื่อ | ✅ มีผู้ค้ำ / ไม่มี | ✅ | ✅ | ✅ |
| เงินดาวน์ | ✅ | — | — | — |
| วงเงินกู้ | — | ✅ | ✅ | ✅ |
| รายละเอียดสินเชื่อ / โปรแกรม | ✅ | ✅ | ✅ | ✅ |

### Summary Box Fields
| Field | ทุก loan type |
|-------|-------------|
| จำนวนงวดผ่อนชำระ | ✅ (หน่วย: เดือน) |
| ผ่อนชำระต่อเดือน | ✅ (หน่วย: บาท) |

---

## [RULES]

- **ไม่มี Doc No. Banner** — ใช้ Remark Tab แทน
- **Field ที่ไม่มีข้อมูล** → ซ่อน row นั้นออก ไม่แสดง "—"
- **New loan type** → ขอ field list จาก user ก่อน เพิ่ม column ในตารางนี้
- **ปุ่มแก้ไข** → นำ user กลับไปหน้า form ก่อนหน้า
- **ยืนยันสมัครสินเชื่อ** → ไปหน้า OTP / Contract ถัดไป

---

## [COLOR]

| Element | Token | Hex |
|---------|-------|-----|
| Page bg | white | `#FFFFFF` |
| Remark tab bg | `Secondary/Yellow BG` | `#FFF9EA` |
| Remark icon bg | — | `#FFE28A` |
| Remark text | `Secondary/Yellow Text` | `#C28000` |
| Detail label | `Text/Text Dark Grey` | `#6D6D6D` |
| Detail value | `Text/Text Black` | `#000000` |
| Summary box bg | `BG/Green5` | `#F3F9F6` |
| Summary value | `Text/Primary Green` | `#0B8041` |
| Confirm button | `Primary/Primary Green` | `#0B8041` |

---

## [TYPOGRAPHY]

| Element | Figma Style | Size/LH | Weight |
|---------|-------------|---------|--------|
| App bar title | `Heading/Header 3` | 16/24px | Bold |
| Section title | `Heading/Header 1` | 20/32px | Bold |
| Detail label | `Body/Body 1` | 16/26px | Regular |
| Detail value | `Body/Body 1` | 16/26px | Regular |
| Summary label | `Body/Body 1` | 16/26px | Regular |
| Summary value | `Heading/Header 2` | 18/30px | Bold |
| Remark text | `Body/Body 3` | 12/18px | Regular |
| Button | `Button/Button 1` | 18/28px | Bold |

---

## Figma Node Reference

| Section | File | Node |
|---------|------|------|
| Product Confirmation (Default) | KBao | 339:71569 |
| Product Confirmation (PreOrder) | KBao | 339:71569 (preOrder=true) |
