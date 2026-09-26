# mrchypark's R-universe

Package registry for <https://mrchypark.r-universe.dev>.

`packages.json` lists each package once and points to its upstream Git repository.
R-universe follows each repository's default branch. Keep `churon` pointed at
`https://github.com/mrchypark/churon`; do not add a separate CRAN mirror entry.

The **Sync R-universe** workflow requests synchronization when the registry
changes, once daily at 03:17 UTC, or manually through GitHub Actions. It uses
R-universe's public synchronization endpoint and needs no credentials. This
provides a fallback when upstream changes are not picked up automatically.
A successful request queues the R-universe sync; package builds and publication
finish separately in <https://github.com/r-universe/mrchypark/actions>.

After a first CRAN release, ownership metadata may temporarily show both the
CRAN mirror and the development package. The CRAN-to-Git mapping and subsequent
R-universe builds determine the canonical listing; changing the registry to the
CRAN mirror is not necessary.

See the [R-universe setup documentation](https://docs.r-universe.dev/publish/set-up.html).
