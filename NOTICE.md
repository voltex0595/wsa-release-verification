# WSA v1.4.4 — Independent Release Verification Notice

This page is the independent public reference for verifying the WSA v1.4.4 release identity.
It is intentionally hosted separately from the Cloudflare Worker and R2 distribution service.

## Release identity

- Product: Web Security Assessment Platform (WSA)
- Version: **1.4.4**
- Ed25519 signing key fingerprint (SHA-256 of SPKI DER):

  `9f23e3adf9f7f2c96ff45814baa318eedf95eccfe794537cba914d3b1846f10c`

- Key ID: `9f23e3adf9f7f2c9`
- Release ZIP SHA-256:

  `feb4d9d6528c7ea02f3c9c96cc4389e21e7ea25837f8bb020cdf9756bbc40d6f`

- Verification bootstrap (`WSA_BOOTSTRAP.mjs`) SHA-256:

  `f6b69d96795c2dfcf5db94d84a3a9cf65c6111a99413534cf814e8a8cf4512d9`

## Official distribution endpoint

- Latest release API: https://wsa-release-api.youtube-marketingdx-trainingworkers.workers.dev/api/releases/latest

The API is authoritative for availability and supplies the current release metadata/download location. If `/api/releases/latest` does not report `1.4.4`, the v1.4.4 release has not yet become the current public release. This notice alone does not imply that the release is live.

## Verification instructions

1. Obtain the ZIP only from the official release API/download endpoint.
2. Calculate SHA-256 locally and compare the full 64-character digest above.
3. Verify the Ed25519 manifest signature and compare the full signing-key fingerprint above.
4. Verify the bootstrap SHA-256 before using it.
5. If any digest or fingerprint differs, do not execute the package.

This notice is published under the `voltex0595/wsa-release-verification` GitHub repository as an independent trust reference. It does not contain the WSA source tree, private signing key, Cloudflare credentials, or R2 credentials.
