# Assets

This folder holds visual assets for W.A.Y? — logo, banner, and any supporting
imagery used by the README and docs. **Design contributions are welcome.** If you'd
like to give W.A.Y? a face, this is the place.

The actual image files are produced as separate work; the entries below are
placeholders describing what fits where, so a contributor can drop in a file without
guessing.

---

## What lives here

| File (suggested) | Purpose | Status |
|------------------|---------|--------|
| `hero.png` | Wide header image shown at the top of the README. | **in use** |
| `logo.svg` | Primary mark. Square, scalable, works on light and dark backgrounds. | placeholder |
| `logo.png` | Raster fallback of the logo for places SVG isn't supported. | placeholder |
| `banner.png` | Alternate wide header / social preview. | placeholder |
| `icon.png` | Small square icon (favicon-style, app-tile use). | placeholder |

---

## Recommended specs

These are guidance, not hard requirements — clarity at small sizes matters more than
hitting exact numbers.

- **Logo (SVG)** — vector, transparent background, square viewBox (for example
  `512 x 512`). Avoid baked-in padding so it can be placed flexibly.
- **Logo (PNG)** — transparent background, at least `512 x 512`, plus a `256 x 256`
  variant if convenient.
- **Banner** — roughly `1280 x 640` (the common social-preview ratio). Keep important
  content away from the edges so cropping is safe.
- **Icon** — square, `256 x 256` or larger, readable when shrunk to `32 x 32`.
- **Format** — SVG for line/flat marks; PNG (transparent) for raster. Avoid JPG for
  anything with text or sharp edges.
- **Color** — should read clearly on both light and dark themes; supply a light-on-dark
  variant if the mark is dark.

---

## Spirit of the mark

W.A.Y? is **"Who Are You?"** — a harness that learns *you* rather than asking you to
learn it. It is built for people who are **not developers**, and it leads with
**reliability** (anti-hallucination, honest reporting) and **structure**. A fitting
mark leans calm, trustworthy, and personal rather than busy or hype-driven. There's no
fixed palette yet, so a proposal that sets one is genuinely useful.

---

## How to contribute an asset

1. Open an issue (use the **Feature request** template) describing the asset you'd like
   to add, or comment on an existing design issue.
2. Place your file here with one of the suggested names above (or propose a better
   name in your pull request).
3. In the pull request, note the source — original work, or the license of anything you
   built on. **Only contribute assets you have the right to share under this repo's MIT
   license.**
4. Keep the file lightweight (optimize SVGs, compress PNGs) so the repo stays small.

> Reminder, per the repo's contribution rules: no personal information or operational
> data in any asset or its metadata.
