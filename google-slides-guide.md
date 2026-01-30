# Google Slides Recreation Guide

Complete guide to recreating the Rift presentation style in Google Slides.

## Slide Setup

### Slide Size
- **Widescreen 16:9** (default)
- Or custom: 1280 x 720 pixels

### Background Color
- **Hex:** `0F0F1A`
- Apply to all slides: Slide → Change background → Custom

---

## Typography

### Primary Font: Roboto (or Open Sans)
Available in Google Slides. Closest match to Inter.

### Monospace Font: Roboto Mono
For code snippets. Add via: Format → Text → Font

### Font Sizes & Styles

| Element | Font | Weight | Size | Color |
|---------|------|--------|------|-------|
| Slide Title | Roboto | Bold | 60pt | `FFFFFF` |
| Title Accent (e.g., "Rift:") | Roboto | Bold | 60pt | `E07A5F` |
| Section Header | Roboto | Semi-Bold | 36pt | `FFFFFF` |
| Card Title | Roboto | Semi-Bold | 24pt | `FFFFFF` |
| Body Text | Roboto | Regular | 18pt | `9CA3AF` |
| Small/Caption | Roboto | Regular | 14pt | `6B7280` |
| Labels (UPPERCASE) | Roboto | Medium | 12pt | `6B7280` |
| Statistics | Roboto | Bold | 72pt | varies |
| Code | Roboto Mono | Regular | 14pt | `E07A5F` |

---

## Color Palette

Enter these in Google Slides: Format → Text color → Custom

### Accent Colors
| Name | Hex (no #) | Usage |
|------|------------|-------|
| Coral | `E07A5F` | Brand accent, "Rift", highlights |
| Green | `81B29A` | Success, checkmarks, positive |
| Blue | `6366F1` | Info, links |
| Purple | `8B5CF6` | Features, special |
| Yellow | `F59E0B` | Warnings |
| Red | `EF4444` | Errors, negative |

### Background Colors
| Name | Hex (no #) | Usage |
|------|------------|-------|
| Primary BG | `0F0F1A` | Slide background |
| Card BG | `1E2235` | Shape fills |
| Elevated | `252836` | Hover states |

### Text Colors
| Name | Hex (no #) | Usage |
|------|------------|-------|
| Primary | `FFFFFF` | Headings |
| Secondary | `9CA3AF` | Body text |
| Muted | `6B7280` | Captions |

### Border Color
| Name | Hex (no #) |
|------|------------|
| Border | `2D3348` |

---

## Creating Cards/Panels

### Basic Card
1. Insert → Shape → Rectangle (rounded corners)
2. Fill color: `1E2235`
3. Border color: `2D3348`
4. Border weight: 1px
5. Corner radius: 12px (if available) or use rounded rectangle

### Success Card
- Fill: `81B29A` at 10% opacity, or `1E2235`
- Border: `81B29A` at 40% opacity

### Warning Card
- Fill: `F59E0B` at 10% opacity
- Border: `F59E0B` at 40% opacity

---

## Creating Badges

### Standard Badge
1. Insert → Shape → Rounded Rectangle
2. Make it pill-shaped (very rounded)
3. Fill: Use accent color at 15% opacity
4. Border: Same accent color at 30% opacity
5. Text: Same accent color, 12pt, UPPERCASE

### Badge Color Combos
| Badge Type | Fill Opacity | Border Opacity | Text Color |
|------------|--------------|----------------|------------|
| Coral | 15% of `E07A5F` | 30% | `E07A5F` |
| Green | 15% of `81B29A` | 30% | `81B29A` |
| Blue | 15% of `6366F1` | 30% | `6366F1` |

---

## Creating Buttons

### Primary Button
1. Rounded rectangle
2. Fill: `E07A5F` (or accent color)
3. No border
4. Text: White, 14pt, Medium weight
5. Padding: ~10px vertical, ~20px horizontal

### Outline Button
1. Rounded rectangle
2. Fill: Transparent
3. Border: 1px, `E07A5F`
4. Text: `E07A5F`, 14pt

---

## Icons

Upload the SVG icons from the `icons/` folder:
1. Insert → Image → Upload from computer
2. Select SVG file
3. Resize as needed (typically 24-32px for inline, 40-48px for card icons)

### Icon Backgrounds
Place icons on colored circles:
1. Insert → Shape → Circle
2. Fill with accent color at 15-20% opacity
3. No border
4. Place icon on top

---

## Code Blocks

### Creating Code Look
1. Insert → Shape → Rectangle (slightly rounded)
2. Fill: `1A1B2E`
3. Border: `2D3348`, 1px
4. Insert text box inside
5. Font: Roboto Mono, 14pt
6. Text color: `9CA3AF`

### Code Header Bar
1. Create narrow rectangle at top
2. Fill: `252836`
3. Add filename text: Roboto Mono, 12pt, `6B7280`

### Terminal Dots
1. Three small circles: 12px diameter
2. Colors: `FF5F56` (red), `FFBD2E` (yellow), `27C93F` (green)
3. Spacing: 6px apart

---

## Tables

### Table Styling
1. Header row background: `1E2235`
2. Header text: White, Bold
3. Body rows: `1E2235` at 50% opacity
4. All text: `9CA3AF`
5. Border: `2D3348`

---

## Comparison Layout

### Side-by-Side Panels
1. Create two equal-width cards
2. Left (negative): Default card style
3. Right (positive): Border color `81B29A`, subtle green tint

### Comparison Items
- Use ✓ or ✗ symbols
- Green (`81B29A`) for positive
- Red (`EF4444`) for negative

---

## Stats/Metrics Display

### Large Stat
1. Number: 72pt, Bold, Accent color
2. Label below: 12pt, UPPERCASE, `6B7280`

### Stat Card
1. Card with icon at top
2. Large number in middle
3. Label at bottom

---

## Grid Background (Advanced)

Google Slides doesn't support CSS grid backgrounds. Alternatives:
1. Create a master slide with faint grid lines
2. Use a PNG grid pattern as background image
3. Skip it - the dark solid background still looks professional

---

## Quick Reference Card

Copy these values frequently:

```
SLIDE BACKGROUND: 0F0F1A
CARD BACKGROUND:  1E2235
BORDER COLOR:     2D3348

CORAL ACCENT:     E07A5F
GREEN ACCENT:     81B29A
BLUE ACCENT:      6366F1
PURPLE ACCENT:    8B5CF6

WHITE TEXT:       FFFFFF
GRAY TEXT:        9CA3AF
MUTED TEXT:       6B7280
```

---

## Tips

1. **Consistency**: Use the same padding (20px) for all cards
2. **Alignment**: Use Google Slides guides for consistent spacing
3. **Icons**: Keep icons the same size within a section
4. **Contrast**: Always use white text on dark backgrounds
5. **Badges**: Keep badge text short (1-3 words)
