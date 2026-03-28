# CHANGELOG — maisoncordier.art

---

## v1.1.0 — 2026-03-28

### Files changed
- `index.html`
- `collection.html`

### What changed
Added direct **Buy Now** payment buttons to all 5 paintings on both pages, linking to Kirsteen's payment pages on kirsteenart.com. Buy Now button text is fully translated into EN / NL / FR / DE via the existing language switcher. "Express interest" button retained as secondary option beneath each Buy Now button.

### Why
Commission agreement signed 28 March 2026. Direct purchase path now permitted and active. Reduces friction from browse → payment. Every visitor can now buy in one click in their own language.

### Payment links
| Painting | URL |
|---|---|
| Coastal Grasses | kirsteenart.com/product-page/coastal-grasses |
| Malta Street | kirsteenart.com/product-page/malta-street |
| Blue Flowers on Copper | kirsteenart.com/product-page/blue-flowers-on-copper |
| Seagrasses & Island | kirsteenart.com/product-page/seagrasses-and-island |
| Magnolia & Bamboo | kirsteenart.com/product-page/magnolia-and-bamboo |

### Translations added
| Language | Button text |
|---|---|
| EN | Buy Now — €1,095 |
| NL | Nu kopen — €1,095 |
| FR | Acheter — €1,095 |
| DE | Jetzt kaufen — €1,095 |

---

## DEPLOY INSTRUCTIONS — v1.1.0

1. Go to github.com → your maisoncordier.art repo
2. Upload and replace index.html
3. Upload and replace collection.html
4. Upload CHANGELOG.md (new file — place in root)
5. Commit message: v1.1.0 — Add Buy Now payment links to all 5 paintings
6. Cloudflare will propagate within ~60 seconds — no cache flush needed

### Verify after deploy
- Visit maisoncordier.art — gold Buy Now button visible on each painting
- Switch language to NL/FR/DE — button text changes correctly
- Click any Buy Now — opens kirsteenart.com payment page in new tab

---

## v1.0.0 — prior to 2026-03-28
Initial build. All 5 paintings live. Multilingual EN/NL/FR/DE. Enquiry-only CTAs.
