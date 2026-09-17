# nwalker-cc-published (GitHub, public)

Canonical published markdown corpus for nwalker.cc. Written only by promotion PRs.

## Layout

```text
nwalker-cc/
  essays/
    <slug>.md   # one file per published essay; none are seeds or test fixtures
```

Entries the site will render must carry `status: published` (or no `status`) and
must not carry `canonical: false`. The site build (nwalker.cc, `src/lib/content.ts`)
skips anything else, so a promotion-path test seed never reaches production again.

## Editorial CI

See `.github/workflows/editorial-gates.yml` — runs on PRs to `main`.
