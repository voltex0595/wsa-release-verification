# WSA v1.4.6 — Independent Release Verification Notice

Date: 2026-11-27  
Product: Web Security Assistant (WSA)  
Release scope: **Windows Local Test**

This reference is hosted on GitHub independently from the Cloudflare release service. It records the identity of the signed Windows v1.4.6 release candidate approved for publication. **The existence of this notice does not prove that the Cloudflare download is already live.** Confirm actual availability using the release API below.

## Release identity

- Release version: **1.4.6**
- Windows Local Test release ZIP size: **1,783,878 bytes** (as reported for the signed RC)
- Release ZIP SHA-256: `66e7704699a696385dd8a2cc5923d3e95a09d132860448cf55f7de92cea35e6e`
- Official Ed25519 signing-key fingerprint (**SHA-256 of the SPKI DER public key**): `9f23e3adf9f7f2c96ff45814baa318eedf95eccfe794537cba914d3b1846f10c`
- Same official signing-key fingerprint as WSA v1.4.5.
- Signed manifest verification: PASS, with 220 listed files verified and no unregistered files reported.

The values above come from the signed release candidate's final validation record. Compare them against the actual bytes downloaded from the official distribution service.

## Official distribution and independent checking

- Release API: https://wsa-release-api.youtube-marketingdx-trainingworkers.workers.dev/api/releases/latest
- Download landing page: https://wsa-v145-download.pages.dev/

Obtain the v1.4.6 ZIP from the official release endpoint/landing page **only once it is listed as available**. Verify the complete 64-character SHA-256 of the downloaded ZIP, compare the full signing-key fingerprint with this independently hosted notice, and verify the signed manifest and file hashes. Do not run the package if any identity, signature, or digest differs.

Windows PowerShell: `(Get-FileHash -Algorithm SHA256 -LiteralPath "PATH_TO_DOWNLOADED_ZIP").Hash.ToLowerInvariant()`

## Windows validation summary (2026-11-27)

- Signed release candidate and official Ed25519 key: PASS.
- Norton 360 enabled during signed release candidate startup: PASS.
- AV status: `AV_UNVERIFIED`; launch in that condition requires an explicit one-time acknowledgement. **It is not a verified antivirus scan.**
- Dedicated-drive tests: 66 items on a single selected drive and 132 across two selected drives, with progress display and pause/resume/cancel.
- Interrupted-job recovery: four forced-termination cases; 144 items matched the expected set after recovery.
- JSON/HTML/CSV export and normal shutdown: PASS.
- Regression results: **337 PASS, 0 FAIL, 3 SKIP**.

## Known limits and disclosure

The following were **NOT TESTED** on physical hardware/real workloads: system sleep/resume, physical USB unplug/replug, default scanning of all physical drives, and macOS hardware operation. The public release scope is Windows Local Test; tests in dedicated drives or simulated conditions do not guarantee safe operation on every host.

This is **not** a certification that the software or its dependencies are free of vulnerabilities or malware. Existing security findings remain subject to separate review; a valid signature proves provenance and integrity, not safety.

This independent record contains no private signing key or Cloudflare credentials. The earlier WSA releases remain separately verifiable.
