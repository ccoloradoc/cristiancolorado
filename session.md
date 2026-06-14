# Session changelog — 2026-06-12 / 2026-06-14

## Changes made

### Content

- **Added Softtek experience card** to `index.html` and `es/index.html` (after Accenture in the timeline). Client: GE, energy sector, 2008–2012. Includes on-site deployment detail (Albany NY / Houston TX).
- **Updated years of experience** from 15+ → **17+** across all four files: `index.html`, `es/index.html`, `cv.html`, `cv-short.html`. Calculated from May 2008 start minus ~13-month MBA gap.
- **Added Education section** to `index.html` and `es/index.html` with two entries:
  - Universidad Carlos III de Madrid — MBA, Entrepreneurship & Business Creation (2014–2015)
  - Universidad Autónoma de San Luis Potosí — B.Eng., Computer Science (2002–2007)
- Added **Education nav link** to sidebar in both language versions.

### Design / UX

- **Nav animation redesign** — replaced the horizontal extending line (`::before` width trick) with a **left accent bar** that scales vertically (`scaleY 0→1` from bottom) on hover/active. Text also shifts 6px right. Mobile nav unchanged (horizontal pill tabs).
- **Floating CTA buttons (Option C)** — LinkedIn and Download CV buttons moved to `position: fixed; top: 24px; right: 28px` on desktop, always visible regardless of sidebar scroll. On mobile they appear in the sidebar footer as before.

### Housekeeping

- `index-b.html` and `index-c.html` created for A/B/C comparison, then deleted after Option C was chosen.
- `CLAUDE.md` created with project documentation.
- `session.md` created (this file).

## Commits

| Hash | Message |
|---|---|
| `8913c54` | Add Softtek experience card and update years of experience to 17+ |
| `f1f1b1d` | Add Education section and left accent bar nav animation |

## Pending

- Apply floating button + nav changes to production (git push / deploy).
- Decide whether to propagate Option C floating buttons to `es/index.html` commit (already applied in files, not yet committed).
