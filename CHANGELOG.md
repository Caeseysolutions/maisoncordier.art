# CHANGELOG — maisoncordier.art / index.html

## v[next] — 10 Apr 2026

### Fixed
- **4 broken email links** — all `mailto:bonjour@maisoncordier.art` links were broken:
  - Line 328 (nav Enquire): `/mailto:` rogue slash removed → `mailto:`
  - Line 363 (hero "Private enquiry" button): Cloudflare cdn-cgi obfuscated href → plain `mailto:`
  - Line 526 (closer "Write to us" button): Cloudflare cdn-cgi obfuscated href → plain `mailto:`
  - Line 535 (footer email display): Cloudflare `[email protected]` span → plain `bonjour@maisoncordier.art` text with `mailto:` href

### Why
Cloudflare email obfuscation (`cdn-cgi/l/email-protection`) broke when site moved to GitHub Pages (no Cloudflare Worker decoding available). The nav link had an additional `/mailto:` typo. All replaced with plain `mailto:` hrefs.
