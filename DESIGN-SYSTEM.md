# Castleland Management — Design System

## Theme: Antique Shop Showroom
A warm, genuine, vintage aesthetic executed with modern professionalism. The design evokes a well-organized antique shop with hardwood interiors, warm lighting, and tasteful signage.

---

## Color Palette

### Primary Blues (Headers, Buttons, Links)
| Token | Hex | Usage |
|-------|-----|-------|
| `--navy-900` | `#1a2a3a` | Deepest navy, footer |
| `--navy-800` | `#243447` | Deep navy, header |
| `--navy-700` | `#2d4156` | **Primary buttons, nav** |
| `--slate-600` | `#3d5a73` | Slate blue accents |
| `--slate-500` | `#4a6d8a` | Medium slate |
| `--dusty-400` | `#6b8fa8` | Dusty blue, hover states |
| `--dusty-300` | `#8fb3cc` | Light dusty blue |

### Wood Tones (Surfaces, Shelves, Accents)
| Token | Hex | Usage |
|-------|-----|-------|
| `--walnut-900` | `#3d2b1f` | Deep walnut |
| `--walnut-700` | `#5c4633` | Walnut |
| `--oak-600` | `#6f5941` | Dark oak |
| `--oak-500` | `#8b7355` | **Shelf backgrounds** |
| `--oak-400` | `#a68b6a` | Oak accents |
| `--oak-300` | `#c4a882` | Light oak, borders |
| `--birch-200` | `#dcc9a9` | Birch |

### Neutrals (Backgrounds, Text)
| Token | Hex | Usage |
|-------|-----|-------|
| `--charcoal` | `#2c2c2c` | Primary text |
| `--charcoal-light` | `#4a4a4a` | Secondary text |
| `--parchment-100` | `#faf8f5` | **Page background** |
| `--parchment-200` | `#f5f1ea` | Light parchment sections |
| `--parchment-300` | `#ebe5da` | Borders, dividers |
| `--parchment-400` | `#ddd5c7` | Warm gray |

### Brass Accents (Sparingly)
| Token | Hex | Usage |
|-------|-----|-------|
| `--brass-500` | `#b8860b` | Dark brass |
| `--brass-400` | `#d4a84b` | **Accent highlights, dividers** |
| `--brass-300` | `#e8c777` | Light brass, hover |

---

## Typography

### Font Families
- **Headings:** `'Playfair Display'` — Classic serif for heritage feel
- **Body:** `'EB Garamond'` — Elegant readable serif
- **UI/Sans:** `'Inter'` — Clean modern sans-serif for buttons, labels

### Type Scale
| Token | Size | Usage |
|-------|------|-------|
| `--text-xs` | 0.75rem (12px) | Labels, badges |
| `--text-sm` | 0.875rem (14px) | Buttons, captions |
| `--text-base` | 1rem (16px) | Body text |
| `--text-lg` | 1.125rem (18px) | Card titles |
| `--text-xl` | 1.25rem (20px) | Section subtitles |
| `--text-2xl` | 1.5rem (24px) | Small headings |
| `--text-3xl` | 1.875rem (30px) | Section headings |
| `--text-4xl` | 2.25rem (36px) | Page headings |
| `--text-5xl` | 3rem (48px) | Hero headings |

### Letter Spacing
- `--tracking-wide`: `0.05em` — Headings
- `--tracking-wider`: `0.1em` — Nav items, logos

---

## Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | 0.25rem (4px) | Tight gaps |
| `--space-2` | 0.5rem (8px) | Icon gaps |
| `--space-3` | 0.75rem (12px) | Button padding |
| `--space-4` | 1rem (16px) | Card padding |
| `--space-5` | 1.25rem (20px) | Standard spacing |
| `--space-6` | 1.5rem (24px) | Section gaps |
| `--space-8` | 2rem (32px) | Large spacing |
| `--space-10` | 2.5rem (40px) | Section margins |
| `--space-16` | 4rem (64px) | Section padding |

---

## Shadows

| Token | Usage |
|-------|-------|
| `--shadow-sm` | Subtle elevation |
| `--shadow-md` | Cards, buttons |
| `--shadow-lg` | Hover states |
| `--shadow-card` | Auction cards |
| `--shadow-card-hover` | Card hover lift |
| `--shadow-shelf` | Shelf drop shadow |
| `--glow-blue` | Blue glow on hover (cards) |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | 0.25rem | Buttons, inputs |
| `--radius-md` | 0.5rem | Cards, shelves |
| `--radius-lg` | 0.75rem | Large containers |
| `--radius-xl` | 1rem | Status pills |

---

## Components

### Header (Antique Shop Signage)
- Navy gradient background (`--navy-700` → `--navy-800`)
- Wood trim accent line at bottom (oak + brass gradient)
- Logo left, nav links right
- Primary CTA button in brass (`nav-cta` class)

### Auction Shelf
- Wood plank background (`--oak-400` → `--oak-600`)
- Subtle wood grain texture overlay
- Drop shadow to simulate depth
- Shelf label badge (navy with brass accents)

```html
<div class="auction-shelf">
    <span class="shelf-label">Now Accepting Bids</span>
    <div class="auction-grid">
        <!-- auction cards here -->
    </div>
</div>
```

### Auction Card (Framed Item)
- White background with subtle border
- Thin brass accent line on top
- Image with frame border effect
- Status pill (Open/Ending/Ended)
- **Hover:** Lift + blue glow outline

```html
<div class="auction-card">
    <div class="auction-image">
        <img src="..." class="auction-photo">
        <span class="auction-status status-open">Open</span>
    </div>
    <div class="auction-details">
        <h3>Auction Title</h3>
        <p class="auction-date"><i class="fas fa-clock"></i> Bidding Open</p>
        <a href="..." class="btn">Bid Now</a>
    </div>
</div>
```

### Status Pills
| Class | Color | Usage |
|-------|-------|-------|
| `.status-open` | Green (`--success`) | Active auctions |
| `.status-ending` | Gold (`--warning`) | Ending soon |
| `.status-ended` | Gray (`--charcoal-light`) | Past auctions |

### Buttons
| Class | Style |
|-------|-------|
| `.btn` | Solid navy, white text |
| `.btn-secondary` | Outlined navy |
| `.btn-accent` | Solid brass |
| `.btn-past` | Solid oak (past auctions) |

---

## Page Layout

### Homepage Flow
1. **Header** — Sticky nav with wood trim
2. **Newsletter Banner** — Wood background, email signup
3. **Current Auctions** — Shelf display with cards
4. **Hero/Welcome** — Navy section, about text
5. **Contact** — Parchment background, contact cards
6. **Footer** — Navy with wood trim
7. **Past Auctions** — Parchment archive grid

### Section Backgrounds
- **Primary sections:** `--parchment-100`
- **Alternate sections:** `--parchment-200`
- **Hero/Footer:** Navy gradient
- **Shelves:** Oak gradient

---

## Accessibility

- AA contrast ratios maintained
- Focus states on interactive elements
- Keyboard navigation support
- Semantic HTML structure
- Alt text on all images

---

## Responsive Breakpoints

| Breakpoint | Layout Changes |
|------------|----------------|
| `992px` | 2-column auction grid |
| `768px` | Stack header, mobile nav, compact cards |
| `480px` | Single column auctions (current), 2-col (past) |

---

## File Structure

```
/
├── index.html          # Homepage
├── policies.html       # Policies page
├── styles.css          # Main stylesheet with design tokens
├── DESIGN-SYSTEM.md    # This file
└── [images]            # Auction photos
```
