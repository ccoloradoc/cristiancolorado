# CLAUDE.md — cristiancolorado.com

Personal portfolio and professional site for Cristian Colorado, Senior Software Engineer.

## Project structure

```
/
├── index.html          # English version (main)
├── es/
│   └── index.html      # Spanish version (mirrors English content)
├── cv.html             # Full-length CV (printable)
├── cv-short.html       # Condensed CV variant
├── cristian.colorado.cv.pdf  # Downloadable PDF CV
└── images/
    ├── cc.png          # Favicon / apple-touch-icon
    └── og.png          # Open Graph share image
```

## Key design decisions

- **Two-pane layout** — fixed sidebar (320px) + scrollable main content on desktop; stacks vertically on mobile (≤1024px).
- **Color scheme** — dark navy (`#0a192f` bg, `#020c1b` card bg), teal accent (`#4fd1c5`), slate text.
- **No external CSS frameworks** — all styles are inline `<style>` blocks per file.
- **No JS framework** — vanilla JS only; one `IntersectionObserver` drives the active nav link highlight.
- **Nav animation** — left teal accent bar (`scaleY` from bottom) on hover/active; text shifts 6px right. Mobile reverts to horizontal pill tabs.
- **Floating CTA buttons** — LinkedIn + Download CV float `position: fixed` at top-right on desktop, hidden on mobile. On mobile they appear inside the sidebar footer.

## Content sync rule

`index.html` and `es/index.html` must always stay in sync for structure and content — one is the English version, the other is a full Spanish translation. When adding a new section or card to one, always apply it to the other.

`cv.html` and `cv-short.html` are the source of truth for work history details. Pull bullet points and dates from there when updating the site.

## Sections (in order)

| Section | id (EN) | id (ES) |
|---|---|---|
| About | `#about` | `#sobre-mi` |
| Expertise | `#expertise` | `#experiencia-tecnica` |
| Skills | `#skills` | `#habilidades` |
| Experience | `#experience` | `#trayectoria` |
| Education | `#education` | `#educacion` |
| Certifications | `#recognition` | `#reconocimientos` |

## Experience cards (timeline order)

1. Tech Mahindra — Fortune 500 US grocery retailer (payments) · 2021–Present
2. Unosquare — Harvard University (platform modernization) · 2017–2021
3. Accenture — Disney (media metadata) · 2012–2014
4. Softtek — GE (energy sector, on-site Albany NY / Houston TX) · 2008–2012

## Years of experience

Currently **17+ years** (started May 2008, ~13-month MBA gap in Madrid 2014–2015). Update across all four files when this changes: `index.html`, `es/index.html`, `cv.html`, `cv-short.html`.

## Mobile breakpoints

- `≤ 1024px` — sidebar stacks to top bar, nav becomes horizontal pill scroll, floating buttons hide, sidebar-footer buttons appear.
- `≤ 600px` — reduced padding, sidebar-footer buttons stack full-width.
