# Glyph It ✦

> 宛若星河流入长夜，散落在笔画周围，这是汉字的宇宙星辰向空中发出信号。

Glyph It is a Chinese character art generator. Type any hanzi — it deconstructs into ink particles, stroke by stroke, rendered as a unique sumi-e poster. Every character, a universe.

---

## What it does

Enter a Chinese character. Glyph It fetches its stroke paths via hanzi-writer, scatters ink dots along each brushstroke with physics-based repulsion, and composes them into a poster with a hero stroke, flowing star-trail background, and a caption bar showing pinyin, meaning, and stroke count.

Every render is seeded — same character, different universe each time.

---

## Visual system

- **Sumi-e ink dots** — each stroke is sampled pixel-by-pixel, scattered as 0.3–0.9px ink drops with depth focus
- **Hero stroke** — one random stroke is enlarged 3–4× to fill the canvas dramatically
- **Force-repulsion layout** — 80 iterations push strokes apart, minimum distance enforced
- **Particle stream background** — 2–3 Bézier flow lines drift behind the strokes like the Milky Way
- **Bottom caption bar** — character (42px) · pinyin (15px) · meaning (12px) · stroke count (13px) · solar term + weather

---

## Color palettes

8 built-in themes:

`parchment` · `ink` · `night` · `minimal` · `crimson` · `forest` · `dusk` · `paper`

Plus fully custom colors: background · ink · caption text — all independently adjustable.

---

## Modes

- **Animate** — strokes draw in simultaneously with random delay (0–600ms), circular scatter origin, 800–1300ms duration; blends into ink bleed flow field after completion
- **Static** — instant full render

---

## Export

| Format | Resolution |
|--------|-----------|
| PNG 1× | Screen |
| PNG 2× | High-res |
| PNG 4× | True 4× re-render (not upscale) |
| SVG | Vector, re-rendered at full quality |

---

## Tech

- Stroke data: [hanzi-writer](https://hanziwriter.org/) via CDN
- Rendering: Canvas 2D, 720×1020px, DPR-scaled
- Weather: [wttr.in](https://wttr.in/) API (non-blocking, 4s timeout)
- No backend. No framework. One HTML file.

---

## Try it

→ **[glyphitapp.com](https://glyphitapp.com)**

---

## Made by

Design by [Mog](mailto:daftlamb@gmail.com)

Part of the *\*It* series of single-purpose creative tools.
