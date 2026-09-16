# Executive Communications Dataset — R universe (dormant)

This registry is empty. `ecdata` is no longer published through
[r-universe](https://r-universe.dev), and
`https://executive-communications-dataset.r-universe.dev` no longer serves it.

## Installing ecdata

```r
pak::pkg_install('Executive-Communications-Dataset/ecdata')
```

That installs the current `main` of
[Executive-Communications-Dataset/ecdata](https://github.com/Executive-Communications-Dataset/ecdata),
which is where the package is maintained.

## Why it was switched off

r-universe built the package for three weeks in August and September 2026 and
then stopped syncing silently — the GitHub App stayed installed and healthy, the
registry was unchanged, and the subdomain simply kept serving an old version.
Nothing signalled it. A publishing channel that can go stale without saying so is
worse than not having one, since users cannot tell the difference between "this
is current" and "this has not updated in a month".

## Turning it back on

Put the package back in `packages.json`:

```json
[
  {
    "package": "ecdata",
    "url": "https://github.com/Executive-Communications-Dataset/ecdata"
  }
]
```

and reinstall the [r-universe GitHub App](https://github.com/apps/r-universe/installations/new)
if it has since been removed. Builds resume from `main`. If you do, pair it with
a check that compares the served version against `DESCRIPTION`, so a stall is
visible.
