# Changelog

All changes to `pihole-ad-servers.txt`, newest first.

Pi-hole URL for this list:
`https://raw.githubusercontent.com/RTO2222/pihole-ad-servers/main/pihole-ad-servers.txt`

## 2026-11-21
- Moved the list from Google Drive to this GitHub repository so the download link never changes and needs no sign-in.
- Updated the header comments to describe the current layout (consolidated rules plus sections 1–3). No rules changed.

## 2026-11-20
- Added `||adjoe-programmatic.com^` and `||fyber.com^`: adjoe and Fyber in-app ad networks seen from the iPhone.

## 2026-11-19
- Added `||blueduckredapple.com^`: rotating in-app ad server used by a game on the iPhone after other ad networks were blocked.
- Removed the three Sentry error-reporting rules (`ingest.sentry.io`, `ingest.us.sentry.io`, `ingest.de.sentry.io`), which were overridden by an allowlist entry and had no effect.
- Consolidated the list: 94 `||domain^` rules replaced about 395 individual entries, each blocking a domain and all its subdomains. Whole-domain rules are only used for ad and tracking companies; shared domains (Apple, Amazon, Unity, Google) use narrower rules.
  - Dropped the proposed `||bblmw.com^` rule because it would have blocked Bambu Lab's MakerWorld and printer content. Only `event.bblmw.com` and `perf.bblmw.com` are blocked.
- Added Mintegral in-app ad rules (`||mtgglobals.com^`, `||mintegral.net^`) and seven in-app ad servers seen from the iPhone (Voodoo ad network, ContextSDK, everestop, InMobi, Rayjump).
- Created the list from the home Pi-hole query log (14–19 Nov 2026): 351 ad and tracking domains that were getting through, plus 303 already blocked, matched against the StevenBlack and HaGeZi Pro lists. App Store, iCloud, iOS update, YouTube image, CDN, consent and bank fraud-check domains were left out on purpose.
