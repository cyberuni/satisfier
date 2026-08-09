---
'satisfier': patch
---

Publish through npm trusted publishing (OIDC) with provenance, and correct the package
`version` back to the last real release. The previous `0.0.0-development` placeholder was
taken literally by changesets and published as `latest` on 2026-08-09; this release moves
the `latest` dist-tag back onto a real version.
