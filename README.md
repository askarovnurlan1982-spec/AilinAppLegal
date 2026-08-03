# Ailin public site (`public/`)

Static, dependency-free site that satisfies the Apple App Store submission
requirements for public URLs. No build step, no JavaScript, no external
requests (no CDN fonts, no analytics, no trackers) — consistent with the
"Data Not Collected" App Privacy answer.

Deploy the contents of this directory to the web root of `ailinlabs.com`.

## Files

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
| `CNAME` | `ailinlabs.com` (GitHub Pages custom domain) |
| `.nojekyll` | Disables Jekyll processing on GitHub Pages |

Legal text is reproduced verbatim from
`AilinAppLegal/docs/AILIN_{PRIVACY_POLICY,TERMS_OF_USE}_{EN,RU}_v1.0.md`.
Only structure was restored (lists, tables, headings) and the document
placeholders were filled. **If the source documents change, update these
pages — they are the public copy of record.**

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

## Checks before submission

No highlighted placeholder markers should be published. Confirm with:

```bash
grep -rn 'class="todo"' public/
```

Also confirm before publishing:

- **Effective date** is set to **July 31, 2026** on all four legal pages
  (`Effective date` / `Дата вступления в силу`). Change it if the intended
  effective date differs.
- **Operator name** is `Ailin Labs LLC` throughout. It must match the legal
  entity on the App Store Connect account and the EU trader record.
- **Contact email** is `support@ailinlabs.com` throughout, used as the support,
  privacy and terms contact. The mailbox must exist and be monitored before
  submission — App Review checks that the Support URL has working contacts.
- **Prices** on the landing and support pages ($9.99 / $59 PRO, $14.99 / $89
  PRO+) are the planned U.S. prices from the compliance doc. If App Store
  Connect differs, update the pages and the in-app paywall.
- **Support email deliverability** — set up SPF/DKIM for `ailinlabs.com` so
  replies do not land in spam.

## In-app links

`Settings → Legal` in the app must point at the same URLs, matched to the
active app language, and must contain no placeholder URLs. See section 13.3 of
the compliance document.

## Publishing with GitHub Pages

1. Push the repository to GitHub.
2. **Settings → Pages → Build and deployment → Deploy from a branch.**
3. Select the branch and the `/public` folder (or copy `public/` to the root of
   a dedicated Pages repo — the existing `AilinAppLegal` repo already holds the
   `ailinlabs.com` CNAME, so only one of the two should serve the domain).
4. Enable **Enforce HTTPS**. Apple requires the URLs to resolve over HTTPS.

Verify after deploy: every page loads, the language switch works both ways, and
`grep` for `class="todo"` returns nothing.
