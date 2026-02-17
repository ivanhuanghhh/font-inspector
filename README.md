# Font Inspector

Standalone HTML tool that parses uploaded font files and displays comprehensive metadata, type specimens, character maps, and glyph outlines — all client-side.

## Usage

Open `font-inspector.html` in any modern browser. Drag-and-drop (or click to browse) a `.ttf`, `.otf`, or `.woff` file.

## What it shows

- **Identification** — PostScript name, full name, family, style, version, copyright, designer, license, URLs
- **Quick Stats** — glyph count, weight class, units per em, fixed pitch
- **Technical Details** — metrics (ascender/descender/cap height/x-height), OS/2 classification, file info, available OpenType tables
- **Type Specimen** — editable waterfall preview (10–80px) and paragraph preview using the uploaded font
- **Character Map** — grid of supported glyphs with Unicode code points and glyph names on hover
- **Glyph Outlines** — canvas-rendered Bezier paths for sample characters (A–Z, digits, symbols)

## Dependencies

Loaded via CDN (no install needed):

- [Tailwind CSS](https://tailwindcss.com) — styling
- [opentype.js](https://opentype.js.org) — font parsing
- Google Fonts (Instrument Serif, IBM Plex Mono, DM Sans) — UI typography

## Notes

- All processing happens locally in the browser — no data is uploaded to any server.
- WOFF2 is not supported by opentype.js v1.x.
