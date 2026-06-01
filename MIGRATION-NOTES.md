# Royco Dawn — GitBook → Mintlify migration

Source: https://royco.gitbook.io/royco-dawn
All 11 published pages were migrated from their **live** GitBook content.

## What's here

```
docs.json                      # Mintlify site config + sidebar navigation
favicon.svg                    # placeholder favicon (swap for the real Royco mark)
overview.mdx                   # 1. Overview
how-dawn-works.mdx             # 2. How Dawn Works
vault-products.mdx             # 3. Vault Products
governance-and-fees.mdx        # 4. Governance and Fees
yield-share-fees-explained.mdx # (child of Governance and Fees in GitBook)
deposits-and-withdrawals.mdx   # 5. Deposits and Withdrawals
risk-framework.mdx             # 6. Risk Framework
security-and-audits.mdx        # 7. Security and Audits
roycoentrypoint.mdx            # 8. RoycoEntryPoint
faq.mdx                        # 9. Frequently Asked Questions
key-addresses.mdx              # 10. Key Addresses
images/                        # drop the 8 exported figures here (see README-IMAGES.md)
```

## Conversion choices (kept formatting as close to GitBook as possible)

- Each page's title is set in MDX frontmatter (e.g. `title: "2. How Dawn Works"`),
  which Mintlify renders as the page H1 — matching GitBook's numbered headings.
- GitBook `<figure>` blocks → Mintlify `<Frame>` wrappers.
- GitBook collapsible toggles (`<details>`) on the FAQ → Mintlify
  `<AccordionGroup>` / `<Accordion>`, the closest visual equivalent.
- HTML `<table>` blocks were converted to clean Markdown tables (same columns/rows).
- Internal cross-links were rewritten to Mintlify routes
  (e.g. `/royco-dawn/...7.-security-and-audits.md` → `/security-and-audits`).
- The italic legal disclaimer at the foot of each page is preserved verbatim.

## Things for you to confirm / finish

1. **Figures (8):** export from GitBook into `/images` — see `images/README-IMAGES.md`.
2. **Brand color & logo:** `docs.json` uses a placeholder primary color (#E8623D) and a
   placeholder `favicon.svg`. Replace with the real Royco palette and logo (add a
   `logo/light.svg` + `logo/dark.svg` and a `logo` block in docs.json if wanted).
3. **The `archive/` GitBook section was NOT migrated.** GitBook lists ~16 older/draft
   pages under an "archive" space (old Overview, Mechanism, LPs, Applications, etc.).
   These don't appear in the live published sidebar, so I treated them as deprecated.
   Tell me if you want any of them brought over.
4. **Stale `.md` export caveat:** GitBook's machine-readable `.md` endpoints were serving
   out-of-date copies of some pages. This migration was taken from the **live rendered**
   pages, which are current.
5. **`[link]` placeholder:** the Vault Products disclaimer ends with "Terms of Service
   \[link]" — that placeholder exists in the live GitBook too. Add the real URL when ready.

## No logins were required

Everything was readable from the public GitBook. The only blocked step was downloading
the image binaries (privacy redaction on tokenized CDN URLs), which is why the 8 figures
are a manual export.
