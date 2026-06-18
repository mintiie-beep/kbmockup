# Spacing & Sizing — Merchant App DS

> ไม่มี spacing variables ใน KBao Figma file — ใช้ scale นี้เป็น standard

---

## Spacing Scale

| Token | Value | Use case |
|-------|-------|----------|
| `spacing/2xs` | 4px | Gap เล็กสุด (icon ↔ text ใน button small) |
| `spacing/sm` | 8px | Gap ภายใน element, padding เล็ก |
| `spacing/md` | 12px | Gap ระหว่าง elements (circle ↔ label ใน radio/checkbox) |
| `spacing/lg` | 16px | Padding ภายใน card/row (padding หลัก) |
| `spacing/xl` | 24px | Padding ระหว่าง section, margin ใหญ่ |

## CSS Variables

```css
--merchant-spacing-2xs: 4px;
--merchant-spacing-sm:  8px;
--merchant-spacing-md:  12px;
--merchant-spacing-lg:  16px;
--merchant-spacing-xl:  24px;
```

## Component Reference

| Component | Padding | Gap |
|-----------|---------|-----|
| Button Large | 16px (X) | 4px |
| Button Medium | 12px (X) | 4px |
| Button Small | 8px (X) | 2px |
| Input Field | 16px (top/bottom), 8px (left/right) | — |
| Checkbox / Radio row | 16px (all) | 12px |
| Text Radio card | 16px (sides), 32px (top) | 20px |
