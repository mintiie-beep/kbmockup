# Color Tokens — Merchant App DS

## Primitive Colors

### Green (Brand/Success)
| Token | Value |
|-------|-------|
| `color/green/50` | #F3F9F6 |
| `color/green/100` | #E4F1E9 |
| `color/green/200` | #CEE6D9 |
| `color/green/300` | #A3D6BB |
| `color/green/400` | #68BA90 |
| `color/green/500` | #289F5A |
| `color/green/600` | #0B8041 ← Primary Brand |
| `color/green/700` | #086634 |
| `color/green/800` | #064D27 |
| `color/green/900` | #04331A |
| `color/green/950` | #021A0D |

### Grey (Neutral)
| Token | Value |
|-------|-------|
| `color/grey/50` | #F9F9F9 |
| `color/grey/100` | #F2F2F2 |
| `color/grey/200` | #E6E6E6 |
| `color/grey/300` | #CECECE |
| `color/grey/400` | #BDBDBD |
| `color/grey/500` | #A6A6A6 |
| `color/grey/600` | #8C8C8C |
| `color/grey/700` | #737373 |
| `color/grey/800` | #595959 |
| `color/grey/900` | #404040 |
| `color/grey/950` | #262626 |

### Yellow (Warning)
| Token | Value |
|-------|-------|
| `color/yellow/50` | #FFF9EA |
| `color/yellow/100` | #FFF1C5 |
| `color/yellow/200` | #FFE28A |
| `color/yellow/300` | #FFD24F |
| `color/yellow/400` | #FFC214 |
| `color/yellow/500` | #FBC02D |
| `color/yellow/600` | #E0A600 |
| `color/yellow/700` | #C28000 |
| `color/yellow/800` | #A36B00 |
| `color/yellow/900` | #855600 |
| `color/yellow/950` | #5C3A00 |

### Red (Danger/Error)
| Token | Value |
|-------|-------|
| `color/red/50` | #FFF5F5 |
| `color/red/100` | #FFE3E3 |
| `color/red/200` | #FFC9C9 |
| `color/red/300` | #FFA8A8 |
| `color/red/400` | #FF8787 |
| `color/red/500` | #FF6B6B |
| `color/red/600` | #EA1E30 |
| `color/red/700` | #C92A2A |
| `color/red/800` | #A61E1E |
| `color/red/900` | #8A1515 |
| `color/red/950` | #600E0E |

### Blue (Info)
| Token | Value |
|-------|-------|
| `color/blue/50` | #EDF2FF |
| `color/blue/100` | #DBE4FF |
| `color/blue/200` | #BAC8FF |
| `color/blue/300` | #91A7FF |
| `color/blue/400` | #748FFC |
| `color/blue/500` | #5C7CFA |
| `color/blue/600` | #1C7ED6 |
| `color/blue/700` | #1A67A5 |
| `color/blue/800` | #185A9D |
| `color/blue/900` | #144880 |
| `color/blue/950` | #0E3560 |

---

## Alias Colors (Semantic)

### Background
| Token | → Primitive | Description |
|-------|------------|-------------|
| `alias/color/bg/default` | color/grey/50 | สีพื้นหลังหลักของแอป |
| `alias/color/bg/muted` | color/grey/100 | พื้นหลังแบ่งสัดส่วนเนื้อหา |
| `alias/color/bg/brand` | color/green/600 | พื้นหลัง Primary Brand |
| `alias/color/bg/brand-subtle` | color/green/50 | พื้นหลังแบรนด์อ่อน / Active state |

### Text
| Token | → Primitive | Description |
|-------|------------|-------------|
| `alias/color/text/default` | color/grey/900 | ตัวอักษรหลัก |
| `alias/color/text/muted` | color/grey/600 | ตัวอักษรรอง / คำอธิบาย |

### Border
| Token | → Primitive | Description |
|-------|------------|-------------|
| `alias/color/border/default` | color/grey/300 | เส้นขอบทั่วไป |
| `alias/color/border/brand` | color/green/200 | เส้นขอบ Focus / Brand |

### Status
| Token | → Primitive | Description |
|-------|------------|-------------|
| `alias/color/status/warning/bg` | color/yellow/50 | พื้นหลัง Warning |
| `alias/color/status/warning/main` | color/yellow/500 | ไอคอน Warning |
| `alias/color/status/warning/text` | color/yellow/700 | ข้อความ Warning |
| `alias/color/status/error/main` | color/red/600 | สถานะ Error / Danger |
