# Evidence Handling Guide

- Follow approved authority, privacy, retention, and legal-hold rules.
- Preserve original sources in a restricted evidence store; work from controlled copies where practical.
- Record collector, UTC time, source/query, transfer, and transformations.
- Hash evidence with an approved tool; a matching hash supports byte-integrity checks but does not prove authenticity or completeness.
- Capture query details, time range, timezone, retention gaps, export settings, and limits.
- Keep secrets, personal data, and sensitive payloads out of broad updates and source control.

All files under `evidence/` are generated synthetic fixtures. Reserved `.example` names and documentation-only IP ranges are used. No active attachment or executable is included. `manifest.json` records SHA-256 digests for the fixture files. Recalculation checks current bytes against that manifest only.

Use `templates/chain-of-custody.csv`. Keep raw exports separate from analysis. Document redactions; retain unredacted originals only where authorized and necessary.
