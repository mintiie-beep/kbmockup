# Home Page — Merchant App (KBao)
> Figma node: 2582:79612 (KBao — Home)
> หน้าแรกของระบบ PRIMO สำหรับพนักงานขาย (SA)

---

## [OVERVIEW]

### Purpose
หน้าแรกที่แสดงหลังจาก login สำเร็จ ประกอบด้วย:
- ข้อมูลพนักงาน (user card)
- คู่มือการขาย
- บริการอื่นๆ (shortcut)
- รายการสินเชื่อที่สมัครได้

### Background
| Property | Value |
|----------|-------|
| Fill | `#F3F5F8` |
| Font | LINE Seed Sans TH App / Noto Sans Thai (web fallback) |

---

## [STRUCTURE]

```
Status Bar (44px)
App Header
User Card (green gradient)
คู่มือการขาย Card
บริการอื่นๆ Section
  └── Preorder Banner (with badge)
  └── 3 Service Icons
สมัครสินเชื่อ Section
  └── 3 Loan Product Cards
```

---

## [COMPONENTS]

### 1 — Status Bar
| Property | Value |
|----------|-------|
| Height | 44px |
| Background | `#F3F5F8` |
| Left | Time "9:41" — SF Pro Text Semibold 15px |
| Right | Signal bars + WiFi + Battery SVG icons |
| Figma node | 247:21025 |

---

### 2 — App Header
| Property | Value |
|----------|-------|
| Height | Hug content (~58px) |
| Background | `#F3F5F8` (same as page bg, no border) |
| Logo | `asset/icon/main logo.svg` — ดึงจาก local เท่านั้น |
| Subtitle | "ระบบการขอสินเชื่อ" — Subtitle 2 (14px Medium), สีดำ `#000000`, gap 8px ใต้ logo, ชิดซ้าย |
| Right | Profile avatar (40×40px circle) + gear icon overlay |

---

### 3 — User Card (Green Gradient)
| Property | Value |
|----------|-------|
| Background | Linear gradient `#0B8041` → `#289F5A` (135deg) |
| Border radius | 8px |
| Padding | 12px |
| Avatar | `asset/image/image area.png` (40×46px) — แสดงตรงๆ ไม่ต้องซ้อนรูป user |
| Info background | สีจาก gradient card เท่านั้น ไม่ต้องใช้รูป |
| Name | ชื่อ-นามสกุล user — white, Heading/Header 3 16px Bold |
| Branch | รหัสสาขา + ชื่อสาขา เช่น "001 สาขาสีลม" — white, Body/Body 2 13px Regular |
| Arrow | "›" — rgba(255,255,255,0.7) — ขวาสุด |

---

### 4 — คู่มือการขาย Card (KM)
| Property | Value |
|----------|-------|
| Background | `#FFFFFF` |
| Border | 2px solid `#0B8041` |
| Border radius | 8px |
| Padding | 8px 12px |
| Icon | `asset/icon/Manual.svg` (32×32px) — line style green |
| Title | "คู่มือการขาย และวิธีแก้ปัญหา" — Body/Body 1 15px Bold, green |
| CTA Button | "คลิกที่นี่" — Primary Green, Button/Button 2 14px Bold |
| Purpose | ช่องทางเข้าถึงคู่มือขาย (KM) |

---

### 5 — บริการอื่นๆ Section

#### Preorder Banner
| Property | Value |
|----------|-------|
| Background | `#1A73E9` |
| Border radius | 8px |
| Icon | `asset/icon/Add [Vectorized].svg` (32×32px, white 3D box) |
| Label | "สินค้าพรีออเดอร์" — white, 16px Bold |
| CTA Button | "รับสินค้า" — white bg, black text, 14px Bold |
| Badge | Red circle "12" — overlap บน button ด้านขวาบน |
| Badge style | position: absolute, top: -8px, right: -8px |

#### Service Icons (3 items)
| Icon (asset) | Label |
|-------------|-------|
| `asset/icon/Bill.svg` | "ดูใบแจ้งหนี้ ชำระบิล" |
| `asset/icon/Phone call.svg` | "เปลี่ยนเบอร์ โทรศัพท์" |
| `asset/icon/Shopping basket.svg` | "ใช้วงเงิน สินเชื่อ" |

Icon spec:
| Property | Value |
|----------|-------|
| Icon container | 68×68px, white bg, border-radius 8px, shadow |
| Icon size | 40×40px (line style, green `#0B8041`) |
| Layout | flex-start (ชิดซ้าย), gap 8px |
| Label | Body/Body 3 12px Bold, centered below |

---

### 6 — สมัครสินเชื่อ Section

#### Section Header
| Property | Value |
|----------|-------|
| Title | "สมัครสินเชื่อ" — Heading/Header 2 18px Bold |
| Text color | `color/grey/900` (`#404040`) |

#### Loan Product Cards (2-col grid — ทุก card เดียวกัน)
> **กฎ**: card ทุกใบขนาดเท่ากัน `calc(50% - 6px)` แม้แถวมีใบเดียว
> ถ้ามีสินเชื่อใหม่ → ขอรูปจาก user ก่อน ห้ามสร้างเอง

| Product | Image (asset) |
|---------|--------------|
| เคบาว ผ่อนได้ (มือถือ และเครื่องใช้ไฟฟ้า) | `asset/image/mobile.png` |
| เคบาว ผ่อนได้ (สินเชื่อหมุนเวียน) | `asset/image/meat.png` |
| เคบาว ผ่อนได้ (สินเชื่อพนักงาน) | `asset/image/employee.png` |

Card spec:
| Property | Value |
|----------|-------|
| Width | `calc(50% - 6px)` — ไม่ stretch |
| Background | `#FFFFFF` |
| Border radius | 8px |
| Image area | 112px height, object-fit: cover |
| Product name | Body/Body 2 14px Bold |
| CTA | "สมัคร" button — Primary Green full-width |
| Shadow | `0 4px 8px rgba(166,166,166,0.2)` |

---

## [COLOR]

| Element | Token | Hex |
|---------|-------|-----|
| Page background | `alias/color/bg/default` | `#F3F5F8` |
| App header bg | same as page bg | `#F3F5F8` |
| Content area bg | white (starts mid-user-card) | `#FFFFFF` |
| User card gradient start | `color/green/600` | `#0B8041` |
| User card gradient end | `color/green/500` | `#289F5A` |
| คู่มือ border | `color/green/600` | `#0B8041` |
| Preorder banner | — | `#1A73E9` |
| Section title | `alias/color/text/default` | `#000000` |

---

## [TYPOGRAPHY]

| Element | Figma Style | Size / LH | Weight |
|---------|-------------|-----------|--------|
| Logo | Display / custom | 24px | — |
| App subtitle | `Subtitle 2` | 14/20px | Medium |
| User name | `Heading/Header 3` | 16/24px | Bold |
| User branch | `Body/Body 2` | 13/20px | Regular |
| Section title | `Heading/Header 2` | 18/30px | Bold |
| Product name (card) | `Body/Body 2` | 14/22px | Bold |

---

## [ASSETS]

| Asset | Path | Usage |
|-------|------|-------|
| Main logo | `asset/icon/main logo.svg` | App header — local only |
| User profile | `asset/image/userprofile-cj.png` หรือ `userprofile-cjx.png` | Header avatar เท่านั้น |
| Avatar frame | `asset/image/image area.png` | User card avatar |
| Manual icon | `asset/icon/Manual.svg` | KM card |
| Bill icon | `asset/icon/Bill.svg` | Service icon |
| Phone call icon | `asset/icon/Phone call.svg` | Service icon |
| Shopping basket | `asset/icon/Shopping basket.svg` | Service icon |
| Preorder icon | `asset/icon/Add [Vectorized].svg` | Preorder banner |
| Loan mobile | `asset/image/mobile.png` | Loan card |
| Loan meat | `asset/image/meat.png` | Loan card |
| Loan employee | `asset/image/employee.png` | Loan card |

---

## [ACCESSIBILITY]

- User card: `aria-label="ข้อมูลพนักงาน: {name}, {role}"`
- Preorder badge: `aria-label="สั่งจองสินค้า, 12 รายการ"`
- Loan cards: `role="button"` หรือ `<a>` + `aria-label="{product name}"`

---

## Figma Node Reference

| Section | File | Node |
|---------|------|------|
| Home Page (full) | KBao | 2582:79612 |
| Status Bar | KBao | 247:21025 |
