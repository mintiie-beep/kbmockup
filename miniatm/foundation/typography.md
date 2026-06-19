# Typography Tokens — miniATM (ตู้เงินดี)
> Figma node: 1798:134347 (ATM--CF- — Styles)
> ดึงจาก Figma variable definitions โดยตรง

---

## [FONTS]

| Font | ใช้สำหรับ | Source |
|------|----------|--------|
| **Sarabun** | Thai text ทั้งหมด (Heading, Body, Button, Input) | Google Fonts |
| **LINE Seed Sans TH App** | ตัวเลข, UI label เล็ก | LINE |

> **หมายเหตุ**: miniatm ใช้ **Sarabun** เป็น primary font (ไม่ใช่ LINE Seed)
> เพราะ Sarabun อ่านง่ายกว่าที่ขนาดใหญ่บน kiosk และมีน้ำหนัก SemiBold ที่ชัดเจน
> `letter-spacing: -2.2` ใช้กับ Sarabun เกือบทุก style เพื่อ tighten ตัวอักษร

---

## [THAI TYPOGRAPHY — Sarabun]

> line-height `100` = 100% ของ font-size (= font-size นั้นเอง)

### Heading

| Figma Style | Size | LH | Weight | LS | Use case |
|-------------|------|----|--------|----|----------|
| `thai/Heading/Header 1` | 48px | 48px | SemiBold 600 | -2.2 | Hero title, หน้าหลัก |
| `thai/Heading/Header 2` | 38px | 38px | SemiBold 600 | -2.2 | Section heading ใหญ่ |
| `thai/Heading/Header 3` | 28px | 42px | SemiBold 600 | -2.2 | Card heading |
| `thai/Heading/Header 4` | 24px | 36px | Bold 700 | -2.2 | Sub-heading |

### Subtitle

| Figma Style | Size | LH | Weight | LS |
|-------------|------|----|--------|----|
| `thai/Subtitle/Subtitle 1` | 32px | 32px | Medium 500 | -2.2 |

### Body

| Figma Style | Size | LH | Weight | LS | Use case |
|-------------|------|----|--------|----|----------|
| `thai/Body/Body 1` | 28px | 42px | Medium 500 | 0 | เนื้อหาหลัก, list item |
| `thai/Body/Body 2` | 24px | 36px | Regular 400 | -2.2 | เนื้อหาทั่วไป |
| `thai/Body/Body 3` | 20px | 20px | Regular 400 | -2.2 | ข้อความย่อย, note |
| `thai/Body/Caption` | 18px | 27px | Regular 400 | -2.2 | Caption, helper text |

### Button

| Figma Style | Size | LH | Weight | LS | Use case |
|-------------|------|----|--------|----|----------|
| `thai/Button/Button 1` | 38px | 38px | SemiBold 600 | -2.2 | ปุ่มหลัก (Primary) |
| `thai/Button/Button 2` | 36px | 50px | SemiBold 600 | -2.2 | ปุ่มรอง |
| `thai/Button/Button 3` | 28px | 28px | SemiBold 600 | -2.2 | ปุ่มเล็ก |
| `Button` (alias) | 48px | 48px | SemiBold 600 | -2.2 | ปุ่ม hero ขนาดใหญ่มาก |

### Input Text (Kiosk keypad)

| Figma Style | Size | LH | Weight | LS | Use case |
|-------------|------|----|--------|----|----------|
| `thai/InputText/InputText 1` | 64px | 64px | SemiBold 600 | 0 | ตัวเลขที่ผู้ใช้พิมพ์ (input display) |
| `thai/InputText/InputText 2` | 56px | 56px | SemiBold 600 | 0 | Input ขนาดรอง |

---

## [LINE SEED SANS TH APP — Numbers & UI]

| Figma Style | Size | LH | Weight | Use case |
|-------------|------|----|--------|----------|
| `Number/Number 1` | 24px | 32px | Bold 700 | ตัวเลขขนาดกลาง |
| `Number/Number 2` | 18px | 28px | ExtraBold 800 | ตัวเลขเด่น |
| `Number/Number 3` | 10px | 16px | Regular 400 | ตัวเลขเล็ก, label |
| `Input Text/Input Text 3` | 12px | 18px | Regular 400 | Input helper text |
| `Input Text/Input Text 4` | 10px | 16px | Regular 400 | Caption micro |
| `Button/Text Link` | 16px | 26px | Bold 700 | Link text |
| `Subtitle/Subtitle 2` | 16px | 26px | Bold 700 | Subtitle เล็ก |

---

## [CSS FONT IMPORT]

```css
/* Google Fonts — Sarabun */
@import url('https://fonts.googleapis.com/css2?family=Sarabun:wght@400;500;600;700&display=swap');

/* Fallback สำหรับ LINE Seed Sans TH App */
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Thai:wght@400;600;700;800&display=swap');
```

---

## [CSS CUSTOM PROPERTIES]

```css
:root {
  --font-thai:   'Sarabun', 'Noto Sans Thai', sans-serif;
  --font-number: 'LINE Seed Sans TH App', 'Noto Sans Thai', sans-serif;

  /* Heading */
  --text-h1:  48px; --lh-h1: 1;
  --text-h2:  38px; --lh-h2: 1;
  --text-h3:  28px; --lh-h3: 42px;
  --text-h4:  24px; --lh-h4: 36px;

  /* Body */
  --text-b1:  28px; --lh-b1: 42px;
  --text-b2:  24px; --lh-b2: 36px;
  --text-b3:  20px; --lh-b3: 1;
  --text-cap: 18px; --lh-cap: 1.5;

  /* Button */
  --text-btn1: 38px;
  --text-btn2: 36px;
  --text-btn3: 28px;

  /* Input display */
  --text-input1: 64px;
  --text-input2: 56px;

  /* Common */
  --ls-thai: -2.2px;
}
```

---

## [KIOSK SIZE RATIONALE]

> ขนาด font บน kiosk ใหญ่กว่า mobile มาก เพราะผู้ใช้ยืนห่างจากจอ 50–80cm

| Level | Mobile (Merchant App) | Kiosk (miniATM) |
|-------|----------------------|-----------------|
| Heading ใหญ่สุด | 20px | **48px** |
| Body หลัก | 16px | **28px** |
| Button | 18px | **38px** |
| Input display | — | **64px** |
| Touch target min | 52px | **80px** |

---

## Figma Reference

| Item | File | Node |
|------|------|------|
| Styles / Variables | ATM--CF- | 1798:134347 |
