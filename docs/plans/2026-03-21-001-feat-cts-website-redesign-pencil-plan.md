---
title: "feat: CTS Thailand Full Website Redesign in Pencil"
type: feat
status: active
date: 2026-03-21
origin: docs/brainstorms/2026-03-21-cts-website-redesign-requirements.md
---

# CTS Thailand Full Website Redesign in Pencil

## Overview

Redesign the full ctsthailand.org website (Chiang Mai Theological Seminary) in Pencil MCP. The current WordPress site is visually dated with clutter, broken embeds, and inconsistent hierarchy. The goal is a bold & professional visual modernization — keeping all existing content but transforming the visual presentation to feel like a respected university website.

## Problem Statement / Motivation

CTS is a legitimate theological seminary in Chiang Mai offering programs from church leadership training through doctoral degrees. The current website undermines this credibility with an outdated WordPress theme, visible broken shortcodes, ad-like promotional banners, and a cluttered multi-language footer. A modernized design will better represent the institution's professionalism. (see origin: docs/brainstorms/2026-03-21-cts-website-redesign-requirements.md)

## Design System Foundation

### Color Palette

Refined gold + navy — a classic university aesthetic:

| Token | Hex | Usage |
|-------|-----|-------|
| `primary-dark` | #1B2A4A | Navigation, headers, footer background |
| `primary` | #2C4A7C | Section backgrounds, hover states |
| `accent-gold` | #C8A951 | CTAs, highlights, active states, accents |
| `accent-gold-light` | #E8D9A0 | Subtle highlights, borders |
| `bg-white` | #FFFFFF | Page backgrounds |
| `bg-warm` | #F8F6F0 | Alternate section backgrounds |
| `bg-light` | #F0EDE5 | Card backgrounds, subtle containers |
| `text-primary` | #1A1A2E | Body text |
| `text-secondary` | #5A5A6E | Secondary text, captions |
| `text-on-dark` | #FFFFFF | Text on dark backgrounds |
| `text-on-dark-muted` | #B8C4D8 | Secondary text on dark backgrounds |
| `border` | #E0DCD4 | Borders, dividers |
| `success` | #2D7D46 | Confirmation states |
| `error` | #C44536 | Error states |

### Typography

For Thai + English bilingual design:

| Role | Font | Weight | Size |
|------|------|--------|------|
| Display heading | Sarabun Bold / Inter Bold | 700 | 48-64px |
| Section heading | Sarabun SemiBold / Inter SemiBold | 600 | 32-40px |
| Subsection heading | Sarabun SemiBold / Inter SemiBold | 600 | 24-28px |
| Body | Sarabun Regular / Inter Regular | 400 | 16-18px |
| Caption / Small | Sarabun Regular / Inter Regular | 400 | 14px |
| Nav items | Sarabun Medium / Inter Medium | 500 | 15px |
| CTA buttons | Sarabun SemiBold / Inter SemiBold | 600 | 16px |

*Sarabun is a professional Thai font with excellent Latin character support — available in Google Fonts. Inter is its best English complement for a clean, authoritative feel.*

### Spacing System

- Base unit: 8px
- Section padding: 80px vertical, 120px horizontal max-width container
- Card padding: 24px
- Component gap: 16-24px
- Grid: 12-column, 1280px max-width, 24px gutters

### Artboard Convention

- Width: 1440px (standard desktop)
- Height: Variable per page content
- Background: #FFFFFF

## Navigation Architecture

**Solution: Grouped dropdown mega-menu**

Consolidate 9+ top-level items into 6 clear groups:

| Menu Item | Type | Children |
|-----------|------|----------|
| หน้าหลัก (Home) | Direct link | — |
| เกี่ยวกับเรา (About) | Dropdown | History, Mission/Vision, Statement of Faith, Director's Message, Faculty (Residential + Visiting) |
| หลักสูตร (Programs) | Mega menu | Overview, 7 programs, Enrollment, Course Descriptions, Schedule, Calendar |
| สื่อการเรียนรู้ (Learning Media) | Dropdown | Online Courses, Bible Series (5 series), Video Clips (subcategories) |
| ข่าวสารและกิจกรรม (News) | Dropdown | Newsletter, Construction, Alumni, Gallery, Reviews |
| สนับสนุนพันธกิจ (Support) | CTA button | Direct link to donate page |

- "Languages" becomes a small icon/toggle in the top utility bar, not a main nav item
- Contact info (phone, email, location) stays in a slim utility bar above the main nav
- CTS logo anchored left, nav items center-right

## Deliverables: ~20 Pencil Artboards

### Phase 1: Design System + Homepage (5 artboards)

Priority: This phase establishes the visual language everything else builds from.

1. **Design System / Style Guide** — Colors, typography scale, button styles, form elements, card patterns, icon style, spacing grid
2. **Component Library** — Reusable blocks: hero slider, video embed card, program card, faculty card, news card, CTA banner, quote block, donation info block, footer
3. **Navigation** — Header with utility bar + main nav + mega menu expanded state
4. **Homepage (above fold)** — Hero slider with overlay text, sticky nav
5. **Homepage (full page)** — Complete homepage: hero, YouTube embed section, featured news, enrollment CTA, online course section, Dr. Henry quote, library/LINE links, full footer

### Phase 2: About & Institutional Pages (4 artboards)

6. **About Us Landing** — Hub page with cards linking to History, Mission, Faculty, etc.
7. **Content Page Template** — Used for History, Mission/Vision, Statement of Faith, Director's Message (text-heavy with images)
8. **Faculty Page** — Grid of faculty cards with photo, name, credentials, bio — covers both Residential and Visiting faculty
9. **Director's Message** — If distinct from content template (features director photo prominently + message)

### Phase 3: Curriculum & Enrollment (4 artboards)

10. **Curriculum Overview** — Hub page with program cards showing degree level, duration, description
11. **Individual Program Page Template** — For all 7 degree programs: hero banner, program details, curriculum outline, requirements, CTA to enroll
12. **Enrollment Page** — Application information, requirements, process steps, contact/form CTA
13. **Schedule / Calendar Template** — For Class Schedule and Academic Calendar pages (table-based layout)

### Phase 4: Media & Content Pages (4 artboards)

14. **Online Courses Landing** — Course cards with thumbnail, title, instructor, price (499 baht), CTA
15. **Bible Series / Video Landing Template** — Grid of video thumbnails with series info — used for Bible Series landing, Video Clips subcategories
16. **Individual Video/Article Page** — Video player + description + related content sidebar
17. **News & Activities Landing** — News cards with categories, featured article, grid of recent posts

### Phase 5: Support & Utility Pages (3 artboards)

18. **Support/Donate Page** — Mission statement, bank account details, QR code, impact messaging
19. **Search Results Page** — Search bar + filtered results list
20. **Footer (detailed)** — Three-language contact info, course links, bank details, social links, copyright (2012-2026)

## Content & Image Strategy

### Images to Source from Current Site
- 5 hero slider photos (IMG_8588, PIC_0144, PIC_0092, IMG_8499, IMG_8569)
- Dr. Henry Bridenthal photos (multiple across site)
- Faculty headshots
- Library entrance photo
- LINE QR code image
- CTS logo (cross with flame)
- Online course promotional images (instructor photos)
- Construction/campus photos
- Student activity photos

### Image Treatment
Since existing photos vary in quality and style, apply consistent treatment:
- Hero images: Dark gradient overlay (navy to transparent) for text readability
- Faculty photos: Uniform circular or rounded-square crop, consistent size
- Course/article thumbnails: 16:9 aspect ratio crop, subtle overlay on hover
- Campus photos: Full-bleed with dark overlay for section backgrounds

### Content Handling
- **Footer**: Simplified — Thai contact info + English contact info + Chinese contact info in clean columns. Remove "Recent Posts" widget (currently showing spam). Keep bank account details only on Donate page, not footer. Keep Facebook + YouTube social links.
- **Copyright**: Update to "2012-2026"
- **Broken YouTube**: Design as a clean embedded video player section with playlist navigation
- **Promotional banners**: Replace ad-like images with integrated section designs using the design system's card and CTA patterns

## Acceptance Criteria

- [ ] All 20 artboards completed in Pencil
- [ ] Design system artboard establishes all colors, typography, spacing, and components
- [ ] Every page uses consistent components from the design system
- [ ] Homepage shows all current content sections in modernized layout
- [ ] Navigation mega-menu handles all existing pages without clutter
- [ ] Thai text is primary, readable, and well-typeset at all sizes
- [ ] Existing CTS photography is integrated with consistent treatment
- [ ] Bold & professional aesthetic — comparable to a respected university site
- [ ] Footer handles Thai, English, and Chinese contact info cleanly
- [ ] No broken shortcodes, ad-like banners, or visual clutter

## Success Metrics

- Visual cohesion: Any two random pages placed side by side look like they belong to the same site
- Professionalism: A prospective student visiting the site would take the institution seriously
- Content parity: Every piece of content on the current site has a home in the new design

## Dependencies & Risks

- **Image quality**: Some existing photos may be low-resolution. Mitigation: overlay treatments and careful cropping
- **Thai font availability in Pencil**: Sarabun may need to be confirmed as available. Fallback: Noto Sans Thai
- **Scope creep**: 20 artboards is already substantial. Mitigation: strict template reuse across similar pages
- **Content in Thai**: Cannot verify Thai text readability without actual Thai content placed in designs

## Implementation Phases & Order of Work

| Phase | Artboards | Dependency |
|-------|-----------|------------|
| 1. Design System + Homepage | 1-5 | None — start here |
| 2. About & Institutional | 6-9 | Phase 1 (needs design system) |
| 3. Curriculum & Enrollment | 10-13 | Phase 1 |
| 4. Media & Content | 14-17 | Phase 1 |
| 5. Support & Utility | 18-20 | Phase 1 |

Phases 2-5 can run in parallel once Phase 1 is complete.

## Sources & References

### Origin
- **Origin document:** [docs/brainstorms/2026-03-21-cts-website-redesign-requirements.md](docs/brainstorms/2026-03-21-cts-website-redesign-requirements.md) — Key decisions carried forward: bold & professional style direction, content preservation, reuse existing images, Pencil MCP tool, refined gold + navy color palette

### External References
- Current live site: https://www.ctsthailand.org/
- Sarabun font: Google Fonts (Thai + Latin)
- Inter font: Google Fonts (Latin)
