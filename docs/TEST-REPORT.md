# Test report (Abdullah Al Mohsin card), 2026-11-12

Tested in headless Chromium with the iPhone 13 (390 × 844) and Galaxy S9+ (320 × 658) profiles against a local copy.

| Check | Result |
|---|---|
| Page loads, no console errors, no failed requests (both profiles) | Pass |
| No horizontal scroll at phone width (both profiles) | Pass |
| `tel:` links: +8801335134476 and +8801766330755 | Pass |
| `mailto:` link: abdullah.mohsin@bgols.com | Pass |
| WhatsApp link `wa.me/8801335134476` (Mobile 1, as marked on his printed card) | Pass |
| WeChat sheet shows +8801766330755 (Mobile 2, as marked on his printed card) with Copy | Pass |
| QR codes (SVG/PNG, navy/black, portrait card back, landscape card back) decode to `https://alshams8.github.io/Business-Card-Abdullah-Al-Mohsin/` | Pass (zxing-cpp) |
| `contact.vcf`: vCard 3.0, CRLF, lines ≤ 75 octets, two mobile numbers, one email, three labelled office addresses, embedded 256 px photo | Pass |
| card.html, nfc-setup.html, email-signature.html, manifest, sw.js load | Pass |

## Still to test on his real phone (Nothing CMF Phone 2 Pro, Chrome)

Installability checked in Chromium (Pixel 7 profile) under the real /Business-Card-Abdullah-Al-Mohsin/ path: no installability errors, service worker active, manifest parsed.

- [ ] Save Contact shows the contact with photo, both numbers, email, three office addresses, website and card link.
- [ ] Add to Home Screen icon and name ("A. Al Mohsin").
- [ ] QR side opens with `#qr`.
- [ ] NFC tag opens the card on iPhone and Android.
- [ ] iPhone: NameDrop and AirDrop after setting My Card. Android: Quick Share of the link.
- [ ] WeChat: +8801766330755 can be found in WeChat search (depends on his WeChat privacy settings).
