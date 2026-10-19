# Release review — 20 October 2026

## Server files

Upload only these two files to the same directory:

- `dist/index.html`
- `dist/hero.jpg`

No build, package installation, external fonts or remote JavaScript is required on the server. The HTML references `./hero.jpg`. Language variants use `?lang=en` and `?lang=kk`; Russian is the default.

## Completed changes

- Proofread Russian, English and Kazakh copy, including accessibility labels and all 30 Telegram draft messages.
- Simplified the roadmap: consistent horizontal milestones above 900px and a vertical timeline on smaller screens; location badges moved out of the third milestone.
- Kept service content visible without accordion controls, prices after value and scope, and prominent Telegram/email actions.
- Removed retired component styles and unused runtime code; corrected heading levels and added a keyboard skip link.
- Preserved keyboard focus on the language selector after a language change. Fixed menu closing on Escape/outside click, reduced-motion behaviour, counter lifecycle, language metadata and local-file fallbacks.
- Extracted the photo from the HTML. The HTML is about 259 KB instead of 2.7 MB.

## Checks passed

- JavaScript parses; stylesheet parses without errors in jsdom.
- DOM interaction tests for RU, EN and KK: menu, Escape, outside click, nav closing, FAQ toggling, language switching, full Telegram messages, metadata, back-to-top.
- Count-up reaches the final values once; reduced-motion and no-IntersectionObserver fallbacks retain the final numbers.
- Local file opening and no-JavaScript content availability.
- Unique IDs, valid anchor destinations, preserved prices/contact details, four roadmap points and five service offers.
- HTTP 200 for the HTML, language query variants and JPEG, with correct MIME types.
- Known text/background colour pairs meet WCAG AA contrast.
- Distribution ZIP contains exactly two files, with no nested directory.

## Verification limits

The connected browser was unavailable. These were DOM/logic, source and HTTP checks, not rendered desktop/mobile screenshots. Visual acceptance on Chrome/Safari/Firefox/Edge and real mobile devices remains unverified. Do not treat this report as a cross-browser visual sign-off.

The public domain was intentionally left unspecified. Canonical, alternate-language and Open Graph URLs are generated from the actual HTTP location. Optional `robots.txt` and `sitemap.xml` were moved to `deployment-extras/` and are not in the two-file upload; update them if a domain and a larger upload set are agreed later.
