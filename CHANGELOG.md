# CHANGELOG — maisoncordier.art

## v1.5.2 — 17 April 2026 (evening)

### Focus: easy to click and pay — desktop and mobile

This release consolidates three fixes that together make the collection page easy to click and easy to buy from, on every device and in every language.

### Fixed
- **Language buttons work again.** The previous live collection.html had a truncated JavaScript block (ended mid-sentence at `document.body.style.overflow=me` with no closing tags). This killed `setLang()` before it was defined — clicking FR/NL/DE did nothing. Script is now properly closed with `</script></body></html>`. This bug was likely responsible for killing conversions from non-English ad traffic.
- **Dutch title:** `Kust-<br>gras` → `Kustgras` (single closed compound, natural Dutch).
- **German title:** `Küsten-<br>gras` → `Küstengras` (single closed compound, natural German).

### Changed — painting order
- Seagrasses & Island moved to position 01. Ad boost clickers now land on the featured painting above the fold on both desktop and mobile.
- New order: 01 Seagrasses → 02 Malta Street → 03 Coastal Grasses → 04 Blue Flowers on Copper → 05 Magnolia & Bamboo.
- `id="seagrasses"` anchor moved with it to position 01.
- CSS accent colours reordered to match.
- Translation dictionary keys `title1–title5`, `tag1–tag5`, `med1–med5` reordered in all four languages.

### Changed — Buy Now button is now dominant and readable
- Font size lifted from 0.6rem (~9.6px) to 0.92rem (~14.7px).
- Padding expanded to 1.3rem × 2.4rem.
- Box-shadow added for tactile depth: `0 4px 18px rgba(184,132,42,0.28)`.
- Right-arrow hint animates on hover.
- **Mobile:** Buy Now becomes full-width (1.25rem × 1.5rem padding). Exceeds Apple/Google 44×44px tap target guideline. Thumb can't miss it.
- Hero variant on position 01 (Seagrasses): slightly larger (1.4rem × 2.6rem) with subtle gold ring `0 0 0 1px rgba(212,168,85,0.35)` — distinguishes the ad landing CTA without shouting.

### Changed — Express Interest demoted
- Was: outline-box button competing with Buy Now (decision paralysis).
- Now: quiet underlined text link below Buy Now. Copy softened to "Or ask a question first" across EN/NL/FR/DE.
- Result: one dominant primary, one quiet secondary. Conversion-proven hierarchy.

### Removed
- "Featured Work" badge (was in v1.5.0/v1.5.1). Simpler is better.
- Associated `featured-label` translation keys and `work-featured` HTML span.
- CSS for `.work-featured` remains in the stylesheet but is now unreferenced (zero bytes of render impact, cleaned up in v1.6 if/when typography pass happens).

### Not in this release
- index.html unchanged — will receive the same Seagrasses-to-position-01 treatment in v1.5.3 once index.html content is available to me.
- Other pages (artist, collect, journal, privacy) — unchanged.
- Sitemap — separate issue, to be fixed in a dedicated release.
- Site-wide typography and CTA pass — deferred to a planned v1.6.0 which will propagate this collection.html CTA treatment to every page.

### Deploy steps
1. GitHub → maisoncordier.art repo → Upload Files → drop `collection.html` (overwrite) + `CHANGELOG.md`.
2. Wait ~1 minute for GitHub Pages rebuild.
3. Hard refresh `https://maisoncordier.art/collection.html` (Ctrl+Shift+R or Cmd+Shift+R).
4. Test language buttons by clicking FR, NL, DE.
5. Test mobile: open the page on phone, confirm Buy Now is full-width and easy to tap.

---

## v1.5.1 — 17 April 2026
- Fixed Dutch/German title typography (Kustgras, Küstengras).

## v1.5.0 — 17 April 2026
- CTA redesign (Buy Now dominant + quiet Express Interest link).
- Seagrasses hero treatment with Featured Work badge (reverted in v1.5.2).

## v1.4.0 — 17 April 2026 (earlier)
- Reordered collection.html: Seagrasses & Island promoted to position 01.

## v1.3.0 — 16 April 2026
- Seagrasses & Island painting page launched at `painting-seagrasses-and-island.html`.
- Full funnel live across all 5 paintings: Buy Now + Express Interest + WhatsApp.

## v1.2.0 — earlier April 2026
- Added 4th painting (Seagrasses & Island) to collection at position 04.

## v1.1.0 — March 2026
- Initial collection of 3 paintings launched.
- Cloudflare email obfuscation applied.
- Language switcher (EN/NL/FR/DE) operational.

## v1.0.0 — 28 March 2026
- Maison Cordier site live on GitHub Pages.
- Commission agreement with Kirsteen signed.

### Fixed — Dutch and German title typography
- **`title3` NL:** `Kust-<br>gras` → `Kustgras` (single closed compound, natural Dutch)
- **`title3` DE:** `Küsten-<br>gras` → `Küstengras` (single closed compound, natural German)
  - **Why:** Both Dutch and German use closed compounds for this kind of word. The forced hyphen-break inherited from the original file read as "Kust-gras" / "Küsten-gras" which is not how a native speaker would write either word. Removing the `<br>` lets the word sit as one lexical unit; the title's clamp sizing will wrap naturally on narrow viewports if needed.

### No other changes
- Everything else from v1.5.0 is preserved exactly.

---

## v1.5.0 — 17 April 2026

### Changed — CTA system redesign across all 5 paintings
- **Buy Now button enlarged and promoted to dominant CTA.** Font size lifted from 0.6rem (~9.6px) to 0.92rem (~14.7px). Padding expanded (1.3rem × 2.4rem). Added right-arrow affordance that animates on hover. Gold box-shadow added for depth without breaking the flat dark aesthetic.
  - **Why:** Malta Street boost data showed 391 clicks but zero sales. Prior CTAs were below conversion-threshold size. 55–64 and 65+ users (our best-performing age brackets per the same boost data) cannot reliably read 9.6px tracked caps. Mobile tap targets were below the 44×44px Apple/Google guideline.
- **Express Interest demoted** from outline-box button to underlined secondary text link. Copy changed from "Express interest" to "Or ask a question first" — makes the secondary action feel like a softer fallback rather than a competing primary action.
  - **Why:** Two visually equivalent CTAs create decision paralysis. Single dominant primary + quiet secondary is the conversion-proven pattern used by Saatchi Art, Artsy, Singulart (all in our boost targeting interests).
- **Mobile Buy Now** now full-width, 100% container width, 1.25rem × 1.5rem padding. Thumb can't miss it.

### Added — Seagrasses hero treatment (position 01 only)
- **"Featured Work" badge** above the painting title on Seagrasses. Solid gold pill with indicator dot and gold glow. Translated across EN/NL/FR/DE.
  - **Why:** Ad clickers need a match signal when they land from a Meta boost. Without it there is no confirmation they reached the right painting. The badge says "you're in the right place."
- **Larger title treatment on hero:** clamp(2.6rem, 4vw, 4.2rem) vs standard clamp(2.2rem, 3.5vw, 3.5rem).
- **Buy Now hero variant:** slightly larger padding (1.4rem × 2.6rem) and a subtle 1px gold ring (`0 0 0 1px rgba(212,168,85,0.35)`) to distinguish the hero CTA from the others without shouting.

### Added — polish details
- Availability dot now pulses with a green glow ring (`box-shadow: 0 0 8px rgba(76,175,80,0.5)`) — a living signal rather than a static label.
- Work-tag font size lifted 0.52rem → 0.56rem for legibility.
- Work-medium font size lifted 0.56rem → 0.6rem for EU-friendly type scale on compliance lines.
- Work-availability and cta-note font sizes lifted for 55+ audience legibility.

### Changed — translation dictionary
- Added `featured-label` key across EN / NL / FR / DE (Featured Work / Uitgelicht Werk / Œuvre en Vedette / Hervorgehoben).
- Changed `cta1–cta5` copy from "Express interest" style CTAs to softer "Or ask a question first" style link-copy in all four languages.

### Unchanged (preserved)
- Painting order: Seagrasses → Malta → Coastal → Blue Flowers → Magnolia (v1.4.0).
- `id="seagrasses"` anchor on position 01.
- All image URLs, Buy Now destinations (kirsteenart.com product pages), Express Interest query strings.
- Accent colour mapping per position.
- Standalone painting detail pages.
- All copy/descriptions of each painting.

### Deployment note
- `collection.html` is the only file changing in this release. `index.html` home page CTA alignment will follow in v1.6.0 once you've seen this live and confirmed the design direction.

---

## v1.4.0 — 17 April 2026 (earlier)
- Reordered collection.html: Seagrasses & Island promoted to position 01
- Malta Street → 02, Coastal Grasses → 03, Blue Flowers on Copper → 04, Magnolia & Bamboo → 05
- `id="seagrasses"` now on position 01
- Translation dictionary and CSS accents reordered to match

## v1.3.0 — 16 April 2026
- Seagrasses & Island painting page launched at `painting-seagrasses-and-island.html`
- Full funnel live across all 5 paintings: Buy Now + Express Interest + WhatsApp
- Instagram + Facebook posts published; boost submitted for approval

## v1.2.0 — earlier April 2026
- Added 4th painting (Seagrasses & Island) to collection at position 04
- Malta Street boost completed: 391 clicks, €0.07/click, 7 days, €35 total

## v1.1.0 — March 2026
- Initial collection of 3 paintings launched
- Cloudflare email obfuscation applied
- Language switcher (EN/NL/FR/DE) operational

## v1.0.0 — 28 March 2026
- Maison Cordier site live on GitHub Pages
- Commission agreement with Kirsteen signed
