# CHANGELOG — maisoncordier.art

## [Unreleased] — 2026-04-18

### Fixed (second deploy today — title/description alignment)
- **index.html**: Corrected JavaScript T dictionary so titles, medium tags, and descriptions align with their correct paintings on homepage.
  - **Slot 01**: now displays "Seagrasses & Island" + Seagrasses description + A3 Oil Pastel medium tag (matches Seagrasses close-up image already on card)
  - **Slot 04**: now displays "Coastal Grasses" + Coastal Grasses description + A2 Mixed Media medium tag (matches Coastal Grasses full painting image already on card)
  - Swap applied across all 4 languages (EN / NL / FR / DE) in T dictionary
  - Swapped: title1↔title4, tag1↔tag4, desc1↔desc4 × 4 languages
  - HTML hardcoded values untouched (were already correct — JS was overriding them wrongly)
  - Images untouched · Order untouched · Buy Now URLs untouched · Mailto subjects untouched
  - Verified post-edit: 744 lines, 58.3 KB, all 6 ibb.co image URLs at same line positions, Buy Now + Enquiry alignment correct for both affected slots.

### Fixed (first deploy today — Coastal Grasses image)
- **index.html**: Corrected Coastal Grasses image on homepage slot 04.
  - Was: `https://i.ibb.co/rKgLZ9G5/Painting-40-Grasses1.avif` (close-up of reed strands — wrong)
  - Now: `https://i.ibb.co/pjPhsxMk/Painting-40-Grasses7.jpg` (full Coastal Grasses painting — matches painting-coastal-grasses.html detail page)

### Known tech debt (not fixed tonight — deferred)
- Slot 01 / Slot 04 HTML hardcoded values describe opposite paintings to their JS override values. Works correctly via JS but fragile if JS ever fails. Clean-up candidate for future CSS/structure session.
- Painting card fonts (`.work-tag`, `.work-medium`, `.work-desc`, `.cta-note`) use fixed rem sizes instead of `clamp()`. Text doesn't scale symmetrically with browser zoom. Candidate for dedicated CSS responsive audit session.

## [Previous] — 2026-04-17
- Full index.html rebuild (57 KB, ibb.co CDN URLs)
- collect.html reverted to working state (4 languages)
- Cloudflare email obfuscation disabled sitewide
- sitemap.xml validated with 19 URLs (GREEN in Search Console)
