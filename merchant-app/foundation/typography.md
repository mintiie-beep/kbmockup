# Typography Tokens — Merchant App DS
> Figma node: 9203:10944 (Style Guide - Typography)
> Font reference: https://seed.line.me/index_th.html

---

## Font

| Property | Value |
|----------|-------|
| Font family | LINE Seed Sans TH App |
| Figma token | `typography/font-family/sans` |
| CSS | `--merchant-font-family: "LINE Seed Sans TH App", sans-serif` |

---

## Typography Scale (Figma Text Styles)

> ใช้ชื่อ style ตามนี้ทุก component

| Figma Style Name | Size | Line Height | Weight | Use case |
|-----------------|------|------------|--------|----------|
| `Heading/Header 1` | 20px | 32px | Bold | Page title, header หลัก |
| `Heading/Header 2` | 18px | 30px | Bold | Section header |
| `Heading/Header 3` | 16px | 24px | Bold | Card header, sub-section |
| `Heading/Subtitle 1` | 18px | 28px | Regular | Subtitle ขนาดใหญ่ |
| `Heading/Subtitle 2` | 16px | 26px | Bold | Subtitle ขนาดกลาง |
| `Body/Body 1` | 16px | 26px | Regular | เนื้อหาหลัก |
| `Body/Body 2` | 14px | 22px | Regular | เนื้อหาทั่วไป |
| `Body/Body 3` | 12px | 18px | Regular | Helper text, ข้อความย่อย |
| `Number/Number 1` | 24px | 32px | Bold | ตัวเลขขนาดใหญ่, จำนวนเงิน |
| `Number/Number 2` | 18px | 28px | ExtraBold | ตัวเลขเด่น |
| `Number/Number 3` | 10px | 12px | Regular | ตัวเลขเล็ก, label ตัวเลข |
| `Input/Input Text 1` | 16px | 24px | Regular | Input value (default) |
| `Input/Input Text 2` | 16px | 24px | Bold | Input value (filled/bold) |
| `Input/Input Text 3` | 12px | 18px | Regular | Input helper text, floating label |
| `Input/Input Text 4` | 10px | 16px | Regular | Input caption / micro label |
| `Button/Button 1` | 18px | 28px | Bold | Button Large |
| `Button/Button 2` | 14px | 22px | Bold | Button Medium |
| `Button/Button 3` | 14px | 22px | Regular | Button Small ⚠️ ตรวจสอบ |
| `Body/Text Link` | 16px | 24px | Bold | Link text ⚠️ ตรวจสอบ |

---

## Alias → Figma Style Mapping

| Alias Token | → Figma Style | Size/LH |
|-------------|--------------|---------|
| `alias/typography/display-lg` | `Number/Number 1` | 24/32 Bold |
| `alias/typography/heading-lg` | `Heading/Header 1` | 20/32 Bold |
| `alias/typography/heading-md` | `Button/Button 1` | 18/28 Bold |
| `alias/typography/heading-sm` | `Heading/Header 3` | 16/24 Bold |
| `alias/typography/body-lg` | `Body/Body 1` | 16/26 Regular |
| `alias/typography/body-md` | `Body/Body 2` | 14/22 Regular |
| `alias/typography/body-sm` | `Body/Body 3` | 12/18 Regular |
| `alias/typography/caption` | `Input/Input Text 4` | 10/16 Regular |

---

## Primitive Tokens

| Token | Value |
|-------|-------|
| `typography/font-family/sans` | "LINE Seed Sans TH App" |
| `typography/fontweight/regular` | 400 |
| `typography/fontweight/medium` | 500 |
| `typography/fontweight/semibold` | 600 |
| `typography/fontweight/bold` | 700 |
| `typography/fontweight/extrabold` | 800 |

Font sizes: 10, 12, 14, 16, 18, 20, 24, 32, 40, 48px
Line heights: 12, 15, 16, 18, 21, 22, 24, 26, 27, 28, 30, 32, 36px
