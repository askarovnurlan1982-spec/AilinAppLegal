# ailinlabs.com — Ailin public site

Static, dependency-free site that satisfies the Apple App Store submission
requirements for public URLs, served from this repository root via GitHub Pages
at **https://ailinlabs.com** (see `CNAME`).

No build step, no JavaScript, no external requests (no CDN fonts, no analytics,
no trackers) — consistent with the "Data Not Collected" App Privacy answer.

## Layout

| Path | Purpose |
|---|---|
| `index.html` | Marketing / landing page (EN) — includes the auto-renewable subscription disclosure |
| `support.html` | Support page (EN) — operator, contacts, subscriptions, refunds, privacy requests, FAQ |
| `privacy.html` | Privacy Policy v1.0 (EN) |
| `terms.html` | Terms of Use v1.0 (EN) |
| `ru/index.html` | Landing page (RU) |
| `ru/support.html` | Support page (RU) |
| `ru/privacy.html` | Политика конфиденциальности v1.0 (RU) |
| `ru/terms.html` | Условия использования v1.0 (RU) |
| `404.html` | Not-found page |
| `assets/styles.css` | Single stylesheet; palette mirrors the in-app Mist/Night themes, light + dark |
| `assets/favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`, `icon-512.png` | Icons, derived from the app icon |
| `robots.txt`, `sitemap.xml` | Crawling |
| `CNAME` | `ailinlabs.com` |
| `.nojekyll` | Disables Jekyll processing |
| `docs/` | **Source of record.** Approved legal and compliance markdown (EN + RU) |

## Relationship to `docs/`

The four legal pages reproduce `docs/AILIN_{PRIVACY_POLICY,TERMS_OF_USE}_{EN,RU}_v1.0.md`
**verbatim**. Only structure was restored (lists, tables, headings, anchors) and
the document placeholders filled in:

| Marker in `docs/` | Value on the site |
|---|---|
| `[LEGAL OPERATOR NAME]` | Ailin Labs LLC |
| `[PRIVACY EMAIL]` / `[TERMS CONTACT EMAIL]` | support@ailinlabs.com |
| `[EFFECTIVE DATE]` | July 31, 2026 / 31 июля 2026 года |
| `[PRIVACY POLICY URL]` | `https://ailinlabs.com/privacy.html` (RU: `/ru/privacy.html`) |
| `[TERMS OF USE URL]` | `https://ailinlabs.com/terms.html` (RU: `/ru/terms.html`) |

**If a document in `docs/` changes, update the matching HTML page** — these pages
are the public copy of record that Apple and users read.

## App Store Connect URL map

| App Store Connect field | Value |
|---|---|
| Privacy Policy URL (English / primary) | `https://ailinlabs.com/privacy.html` |
| Privacy Policy URL (Russian localization) | `https://ailinlabs.com/ru/privacy.html` |
| Terms of Use (EULA) URL — English | `https://ailinlabs.com/terms.html` |
| Terms of Use (EULA) URL — Russian | `https://ailinlabs.com/ru/terms.html` |
| Support URL — English | `https://ailinlabs.com/support.html` |
| Support URL — Russian | `https://ailinlabs.com/ru/support.html` |
| Marketing URL — English | `https://ailinlabs.com/` |
| Marketing URL — Russian | `https://ailinlabs.com/ru/` |
| License Agreement | Apple Standard EULA — do **not** paste these Terms into the Custom EULA field |
| Privacy Choices URL | Leave blank (no account, no server-side data to delete) |

## Blockers before submission

These values are unknown and render on the pages as highlighted markers. Per
`docs/06_AILIN_APP_STORE_PRIVACY_AND_REVIEW_ANSWERS_v1.0.md.md`, any unreplaced
marker on a public legal page blocks submission.

- `[BUSINESS MAILING ADDRESS]` — 12 occurrences, all 8 pages. Required for the
  EU DSA trader disclosure and referenced by the Privacy Policy and Terms.
- `[TRADER PHONE]` — 4 occurrences on the landing and support pages. Required
  for the EU trader disclosure.

Find them all with:

```bash
grep -rn 'class="todo"' --include='*.html' .
```

Also confirm before publishing:

- **Effective date** is **July 31, 2026** on all four legal pages. Change it if
  the intended effective date differs.
- **Operator name** `Ailin Labs LLC` must match the legal entity on the App
  Store Connect account and the EU trader record.
- **support@ailinlabs.com** must exist and be monitored — App Review checks that
  the Support URL has working contacts. Set up SPF/DKIM so replies do not land
  in spam.
- **Prices** on the landing and support pages ($9.99 / $59 PRO, $14.99 / $89
  PRO+) are the planned U.S. prices. If App Store Connect differs, update the
  pages and the in-app paywall.
- **In-app `Settings → Legal`** must point at these same URLs, matched to the
  active app language, with no placeholder URLs.

## Publishing

GitHub Pages, **Settings → Pages → Deploy from a branch → `main` / `(root)`**,
with **Enforce HTTPS** enabled — Apple requires the URLs to resolve over HTTPS.

Verify after deploy: every page loads, the EN↔RU language switch works both
ways, and the `grep` above returns nothing.

## Local preview

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```
