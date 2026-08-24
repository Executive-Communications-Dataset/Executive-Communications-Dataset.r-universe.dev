# Executive Communications Dataset — R universe

This repository does one thing: it tells [r-universe](https://r-universe.dev) to
build the `ecdata` R package from
[`Executive-Communications-Dataset/ecdata`](https://github.com/Executive-Communications-Dataset/ecdata).

## Installing ecdata

```r
install.packages('ecdata', repos = 'https://executive-communications-dataset.r-universe.dev')
```

That is a real R repository, so `update.packages()` works and dependencies
resolve from CRAN as usual. No `remotes`, no `pak`, no compiler toolchain needed
on platforms r-universe builds binaries for.

## Why this exists

`ecdata` was archived from CRAN on 2025-01-12. Returning it there means a new
submission of a previously-archived package, which has to be made from the
maintainer's own email address and reviewed by the CRAN team. r-universe needs
neither, rebuilds on every push to `main`, and gives users a current package in
the meantime.

This is not a replacement for CRAN. It is what people can install from until the
CRAN question is settled.

## Adding another package

Append to `packages.json`:

```json
{ "package": "somepkg", "url": "https://github.com/Executive-Communications-Dataset/somepkg" }
```

r-universe picks up changes within about an hour. Build status, logs and the
package listing are at
<https://executive-communications-dataset.r-universe.dev>.
