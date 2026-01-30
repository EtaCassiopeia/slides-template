# Rift Presentation Design System

Complete design assets extracted from the Rift presentation for reuse in other projects and Google Slides.

## Quick Start

**PowerPoint Template (Recommended):**
- Import `rift-template.pptx` into Google Slides (File → Import slides)
- 50 ready-to-use slide layouts

**Web Preview:**
- `color-swatch.html` - Visual color palette with copy buttons
- `ui-components.html` - Complete UI component library

---

## PowerPoint Template (50 Slides)

### Core Slides (1-10)
1. Title Slide
2. Code Block with Line Numbers
3. Code with Annotations
4. Table Layout
5. Terminal Output
6. TUI Mockup
7. Comparison Panels
8. Feature Cards Grid
9. Step Panels
10. Color Palette Reference

### UI Components (11-19)
11. Button Styles (Primary, Outline, Ghost)
12. Badges, Pills & Metrics
13. Alert Boxes (Info, Success, Warning, Error)
14. Card Variants
15. Resource Cards
16. Icon Library Page 1
17. Icon Library Page 2
18. Icon Library Page 3
19. Typography Scale

### Layouts (20-25)
20. Two-Column Layout
21. Three-Column Layout
22. Timeline / Roadmap
23. Process Flow Diagram
24. Architecture Diagram
25. Dashboard / Metrics Layout

### Business Templates (26-33)
26. Pricing Cards
27. Team / Profile Cards
28. Testimonials / Quotes
29. FAQ / Accordion Layout
30. Progress Indicators
31. Callouts & Blockquotes
32. List Styles
33. Stat Box Variants

### Diagrams (34-41)
34. SWOT Analysis
35. Funnel Diagram
36. Pyramid Diagram
37. Venn Diagram
38. Priority Matrix
39. Kanban Board
40. Org Chart
41. Mind Map

### Extras (42-50)
42. Device Mockups
43. Social / Contact
44. Partners / Logos
45. Awards & Recognition
46. Case Study
47. Before / After
48. Section Divider
49. Q&A
50. Thank You

---

## Contents

```
presentation-assets/
├── README.md                  # This file
├── rift-template.pptx         # 50-slide PowerPoint template
├── color-palette.json         # Color definitions (JSON)
├── color-palette.css          # CSS variables for colors
├── color-swatch.html          # Visual color preview
├── ui-components.html         # Complete UI component demo
├── ui-components.css          # Full component CSS library
├── typography.css             # Font specifications
├── google-slides-guide.md     # Google Slides recreation guide
└── icons/                     # 119 SVG icons
```

---

## Color Palette

### Accent Colors
| Color | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Coral | `#E07A5F` | rgb(224, 122, 95) | Primary brand, "Rift", highlights |
| Green | `#81B29A` | rgb(129, 178, 154) | Success, checkmarks, positive |
| Blue | `#6366F1` | rgb(99, 102, 241) | Links, info badges |
| Purple | `#8B5CF6` | rgb(139, 92, 246) | Features, special callouts |
| Yellow | `#F59E0B` | rgb(245, 158, 11) | Warnings, attention |
| Red | `#EF4444` | rgb(239, 68, 68) | Errors, negative states |

### Background Colors
| Color | Hex | Usage |
|-------|-----|-------|
| Primary | `#0F0F1A` | Main slide background |
| Secondary | `#1A1B2E` | Code blocks |
| Card | `#1E2235` | Card/panel backgrounds |
| Elevated | `#252836` | Hover states |

### Text Colors
| Color | Hex | Usage |
|-------|-----|-------|
| Primary | `#FFFFFF` | Headings |
| Secondary | `#9CA3AF` | Body text |
| Muted | `#6B7280` | Captions, labels |
| Border | `#2D3348` | Card borders |

---

## Typography

### Fonts
- **Primary**: Inter (Google Fonts)
- **Monospace**: JetBrains Mono (Google Fonts)

### Google Slides Alternative
- **Primary**: Roboto or Open Sans
- **Monospace**: Roboto Mono

### Type Scale

| Element | Weight | Size | Color |
|---------|--------|------|-------|
| Heading 1 | 700 (Bold) | 40px / 60pt | `#FFFFFF` |
| Heading 2 | 600 (Semi-Bold) | 28px / 36pt | `#FFFFFF` |
| Heading 3 | 600 (Semi-Bold) | 20px / 24pt | `#E07A5F` |
| Body | 400 (Regular) | 16px / 18pt | `#9CA3AF` |
| Small | 400 (Regular) | 14px / 14pt | `#6B7280` |
| Label | 500 (Medium) | 12px / 12pt | `#6B7280` + UPPERCASE |
| Code | 400 (Regular) | 14px | `#E07A5F` |

---

## Icons (119 Total)

### Core Icons (39)
| Category | Icons |
|----------|-------|
| Status | checkmark, checkmark-circle, x-mark, x-circle, warning, info-circle |
| Actions | rocket, lightning, zap, target, play, arrow-right |
| Development | code-brackets, terminal, file-code, git-branch, rust-gear |
| Data | chart-bar, database, filter, search, layers |
| Infrastructure | server, cpu, monitor, cloud, package |
| UI | settings, folder, clock, link, shield, star |
| Numbers | number-1, number-2, number-3, number-4 |
| Finance | dollar, speedometer, wrench |

### Tech & Platform Icons (30)
| Category | Icons |
|----------|-------|
| Version Control | github |
| Cloud Platforms | aws, gcp, azure, docker, kubernetes |
| Languages | python, typescript, nodejs, react, vue |
| Communication | mail, bell, message, slack, discord |
| Social | linkedin, twitter, youtube, instagram, facebook, dribbble |
| Design | figma |
| Navigation | home, menu, globe, external-link |
| Security | lock, unlock, key, api |

### Device & Media Icons (20)
| Category | Icons |
|----------|-------|
| Devices | smartphone, tablet, laptop, desktop, watch |
| Media | camera, video, image, music, mic, headphones |
| Actions | download, upload, refresh, edit, copy, trash |
| Status | check-square, plus, minus, trending-up, trending-down |

### Business & UI Icons (30)
| Category | Icons |
|----------|-------|
| User | user, users |
| Time | calendar, clock |
| Weather | sun, moon, cloud-rain, thermometer |
| Commerce | shopping-cart, credit-card, gift, briefcase |
| Analytics | pie-chart, bar-chart-2, activity, percent |
| Location | map-pin, compass, flag |
| Recognition | award, trophy |
| Misc | heart, bookmark, tag, battery, bluetooth, wifi |

### Icon Colors by Category
- **Green** (`#81B29A`): checkmark, target, shield, play, cpu, dollar, user, users, home, lock, download, trending-up, check-square, plus, activity, percent
- **Coral** (`#E07A5F`): rust-gear, rocket, clock, server, speedometer, wrench, git-branch, settings, github, menu, copy, dribbble, mic, trophy
- **Blue** (`#6366F1`): code-brackets, search, info-circle, file-code, link, package, docker, kubernetes, cloud, mail, globe, refresh, upload, external-link, message, linkedin, slack, bar-chart-2
- **Purple** (`#8B5CF6`): chart-bar, filter, database, layers, monitor, api, calendar, figma, pie-chart, video, headphones, compass
- **Yellow** (`#F59E0B`): lightning, zap, star, folder, warning, bell, key, edit, sun, award, gift, flag, battery
- **Red** (`#EF4444`): x-mark, x-circle, unlock, trash, minus, trending-down, heart, youtube

### Changing Icon Colors

Open the SVG in a text editor and change the `stroke` attribute:
```svg
stroke="#E07A5F"  <!-- Change this hex value -->
```

---

## UI Components

### Buttons

**Primary Buttons**
- Background: Accent color (coral, green, blue, purple)
- Text: White
- Padding: 10px 20px
- Border-radius: 12px

**Outline Buttons**
- Background: Transparent
- Border: 1px accent color
- Text: Accent color

**Ghost Buttons**
- Background: Transparent
- Border: None
- Text: Accent color

### Badges & Pills

**Badges** (pill-shaped labels):
- Background: Accent at 15% opacity
- Border: Accent at 30% opacity
- Text: Accent color, 12px, UPPERCASE

**Status Pills**:
- Background: Card color
- Border: Border color
- Text: Accent color (indicates status)

**Metric Badges**:
- Background: Accent at 15% opacity
- Text: Accent color, bold

### Cards

**Basic Card**
- Background: `#1E2235`
- Border: 1px `#2D3348`
- Border-radius: 12px
- Padding: 20px

**Tinted Cards**
- Success: Green background tint
- Warning: Yellow background tint
- Info: Blue background tint
- Error: Red background tint

### Alert Boxes

Horizontal boxes with icon + text:
- Info: Blue accent
- Success: Green accent
- Warning: Yellow accent
- Error: Red accent

### Code Blocks

- Background: `#1A1B2E`
- Border: `#2D3348`
- Header bar: `#252836` with filename
- Terminal dots: red/yellow/green
- Font: JetBrains Mono, 14px

---

## Diagram Templates

### SWOT Analysis (Slide 34)
Four-quadrant layout with color-coded sections:
- Strengths (Green)
- Weaknesses (Red)
- Opportunities (Blue)
- Threats (Yellow)

### Funnel Diagram (Slide 35)
Five-stage conversion funnel:
- Awareness → Interest → Consideration → Intent → Conversion
- Color gradient from blue to green

### Pyramid Diagram (Slide 36)
Four-level hierarchy pyramid with stacked colored sections.

### Venn Diagram (Slide 37)
Three overlapping circles showing relationships:
- Product, Marketing, Engineering with intersection areas

### Priority Matrix (Slide 38)
2x2 quadrant for prioritization:
- High/Low Impact × High/Low Effort axes

### Kanban Board (Slide 39)
Four-column task board:
- Backlog, To Do, In Progress, Done

### Org Chart (Slide 40)
Hierarchical organization structure with CEO and department heads.

### Mind Map (Slide 41)
Central concept with four branching topics.

---

## Layouts

### Two-Column
Side-by-side content for comparisons, before/after, or text + image layouts.

### Three-Column
Feature grids, pricing tiers, or step breakdowns.

### Timeline/Roadmap
Horizontal timeline with colored milestones and date labels.

### Process Flow
Step-by-step process with numbered circles and arrows.

### Architecture Diagram
Layered architecture with color-coded components.

### Dashboard
KPI cards at top, chart area, and activity sidebar.

---

## Business Templates

### Pricing Cards
Three-tier pricing with features list and CTA buttons.

### Team/Profile Cards
Avatar, name, role, and bio in a card layout.

### Testimonials
Quote marks, testimonial text, and author attribution.

### FAQ/Accordion
Expandable question/answer format.

### Case Study (Slide 46)
Three-section layout: Problem, Solution, Results.

### Before/After (Slide 47)
Side-by-side comparison layout.

---

## Extra Slides

### Device Mockups (Slide 42)
Desktop, tablet, and smartphone frames for UI screenshots.

### Social/Contact (Slide 43)
Contact cards with social media links.

### Partners/Logos (Slide 44)
4x2 grid for partner or client logos.

### Awards & Recognition (Slide 45)
Trophy cards for achievements and awards.

### Section Divider (Slide 48)
Large centered title for chapter breaks.

### Q&A (Slide 49)
Questions slide for presentation discussions.

### Thank You (Slide 50)
Closing slide with key stats summary.

---

## Using in Google Slides

1. Go to slides.google.com
2. File → Import slides
3. Upload `rift-template.pptx`
4. Select slides to import
5. Choose "Keep original theme"

See `google-slides-guide.md` for detailed manual recreation instructions.

---

## Using in Web Projects

### Include CSS
```html
<link rel="stylesheet" href="ui-components.css">
```

### Use Components
```html
<!-- Badge -->
<span class="badge badge-coral">Written in Rust</span>

<!-- Button -->
<button class="btn btn-coral">Get Started</button>

<!-- Card -->
<div class="card">
    <div class="card-header">
        <div class="card-icon card-icon-green">
            <img src="icons/checkmark-circle.svg" alt="">
        </div>
        <span class="card-title">Features</span>
    </div>
    <div class="card-content">
        <p>Content here...</p>
    </div>
</div>

<!-- Alert -->
<div class="alert alert-success">
    <img src="icons/checkmark-circle.svg" alt="">
    <div><strong>Success:</strong> All tests passed.</div>
</div>
```

---

## File Formats

| File | Format | Purpose |
|------|--------|---------|
| `rift-template.pptx` | PowerPoint | Google Slides import |
| `color-palette.json` | JSON | Programmatic color access |
| `color-palette.css` | CSS | Web projects |
| `typography.css` | CSS | Font definitions |
| `ui-components.css` | CSS | Full component library |
| `google-slides-guide.md` | Markdown | Slides recreation |
| `icons/*.svg` | SVG | Scalable icons |
