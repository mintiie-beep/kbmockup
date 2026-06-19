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
  └── สินเชื่อค่าเล่าเรียน (featured — NEW)
  └── 3 Loan Product Cards
Footer (version)
Bottom Navigation Bar (fixed)
```

---

## [COMPONENTS]

### 1 — Status Bar
| Property | Value |
|----------|-------|
| Height | 44px |
| Background | `#FFFFFF` |
| Left | Time "9:41" — SF Pro Text Semibold 15px |
| Right | Signal bars + WiFi + Battery SVG icons |
| Figma node | 247:21025 |

---

### 2 — App Header
| Property | Value |
|----------|-------|
| Height | ~56px |
| Background | `#FFFFFF` |
| Logo | "kbao" — Red italic bold |
| Subtitle | "ระบบการขอสินเชื่อ" — Body/Body 2 14px Regular grey |
| Right | Profile avatar 40x40px + edit icon |

---

### 3 — User Card (Green Gradient)
| Property | Value |
|----------|-------|
| Background | Linear gradient `#0B8041` → `#086634` |
| Border radius | 16px |
| Padding | 16px |
| Name | "ฐาปนา ปานประกอบ" — white Heading/Header 3 16px Bold |
| Role | "ซีเจ สาขาสีลม" — white Body/Body 3 12px |

---

### 4 — คู่มือการขาย Card
| Property | Value |
|----------|-------|
| Background | `#FFFFFF` |
| Border | 2px solid `#0B8041` |
| Border radius | 12px |
| Icon | Book icon green `#0B8041` |
| CTA | "คลิกที่นี่" — Button/Button 2 14px Bold |

---

### 5 — บริการอื่นๆ Section

#### Preorder Banner
| Property | Value |
|----------|-------|
| Background | `#1C7ED6` (color/blue/600) |
| Border radius | 12px |
| Badge | Red circle "12" |
| Text color | `#FFFFFF` |

#### Service Icons
| Icon | Label |
|------|-------|
| Bill/receipt | "ดูใบแจ้งหนี้/ชำระบิล" |
| Phone | "เปลี่ยนเบอร์โทรศัพท์" |
| Credit/wallet | "ใช้วงเงินสินเชื่อ" |

Icon container: ~48x48px rounded | color `#0B8041` | Label Body/Body 3 12px centered

---

### 6 — สมัครสินเชื่อ Section

#### สินเชื่อค่าเล่าเรียน (Featured — NEW, full-width)
| Property | Value |
|----------|-------|
| Background | Green gradient `#0B8041` → `#289F5A` |
| Badge | "✦ ใหม่!" white pill |
| Amount | "200,000 บ." white Number/Number 1 24px Bold |
| Rate | "0.99%/เดือน" white Body/Body 2 14px |
| CTA | "สมัครเลย" white bg green text |

#### Loan Product Cards (3 items, 2-col grid)
| Product | Image |
|---------|-------|
| สินเชื่อมือถือ | Mobile illustration |
| สินเชื่อเนื้อ/เกษตร | Meat/agri illustration |
| สินเชื่อพนักงาน | Employee illustration |

Card: white bg, 12px radius, 12px padding, shadow `0 2px 8px rgba(0,0,0,0.08)`

---

### 7 — Footer
| Property | Value |
|----------|-------|
| Text | "Version 0.0.000" |
| Style | Body/Body 3 12px Regular `#A6A6A6` centered |

---

### 8 — Bottom Navigation Bar
| Property | Value |
|----------|-------|
| Position | Fixed bottom |
| Background | `#FFFFFF` |
| Border top | 1px solid `#CEE6D9` |
| Height | ~64px |

| Tab | Icon | State |
|-----|------|-------|
| หน้าแรก | Home | Active `#0B8041` |
| สั่งจอง | Order | Inactive `#A6A6A6` |
| ประวัติ | History | Inactive |
| เพิ่มเติม | More | Inactive |

---

## [COLOR]

| Element | Token | Hex |
|---------|-------|-----|
| Page bg | `alias/color/bg/default` | `#F3F5F8` |
| User card start | `color/green/600` | `#0B8041` |
| User card end | `color/green/700` | `#086634` |
| Preorder banner | `color/blue/600` | `#1C7ED6` |
| Featured gradient | green/600→green/500 | `#0B8041`→`#289F5A` |
| Nav active | `color/green/600` | `#0B8041` |
| Nav inactive | `color/grey/500` | `#A6A6A6` |
| Version text | `alias/color/text/muted` | `#A6A6A6` |

---

## [TYPOGRAPHY]

| Element | Figma Style | Size/LH | Weight |
|---------|-------------|---------|--------|
| Logo "kbao" | Custom | ~28px | Bold Italic |
| App subtitle | Body/Body 2 | 14/22px | Regular |
| User name | Heading/Header 3 | 16/24px | Bold |
| User role | Body/Body 3 | 12/18px | Regular |
| Section title | Heading/Header 2 | 18/30px | Bold |
| Product name | Body/Body 2 | 14/22px | Bold |
| Featured amount | Number/Number 1 | 24/32px | Bold |
| Rate | Body/Body 2 | 14/22px | Regular |
| Nav label | Body/Body 3 | 12/18px | Regular |

---

## [ASSETS — Recommended Folder Structure]

```
kbmockup/
└── merchant-app/
    └── assets/
        ├── icons/
        │   ├── bill.svg
        │   ├── phone-call.svg
        │   ├── credit-wallet.svg
        │   ├── home.svg
        │   ├── order.svg
        │   ├── history.svg
        │   ├── more.svg
        │   ├── book-manual.svg
        │   └── edit-pen.svg
        └── images/
            ├── loan-mobile.png
            ├── loan-meat.png
            ├── loan-employee.png
            ├── loan-education.png
            └── avatar-placeholder.png
```

---

## [ACCESSIBILITY]

- User card: `aria-label="ข้อมูลพนักงาน: {name}, {role}"`
- Preorder badge: `aria-label="สั่งจองสินค้า, 12 รายการ"`
- Bottom nav: `role="navigation"` + `aria-label="เมนูหลัก"`, active `aria-current="page"`
- Loan cards: `role="button"` + `aria-label="{product name}"`

---

## Figma Node Reference

| Section | File | Node |
|---------|------|------|
| Home Page | KBao | 2582:79612 |
| Status Bar | KBao | 247:21025 |
