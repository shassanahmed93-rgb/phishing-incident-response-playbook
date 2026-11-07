# PhishOps | Phishing Incident Response Playbook

A practical, evidence-led phishing response package for a small security team. Built around a fictional business email compromise scenario, with clear decision gates, owners, records, and recovery checks.

**Portfolio simulation. All organizations, people, domains, events, and telemetry are fictional and synthetic.** This is educational material, not legal advice or a substitute for an organization-specific plan.

- [Interactive walkthrough](site/index.html)
- [One-page checklist](docs/one-page-checklist.md)
- [Full response playbook](docs/playbook.md)
- [Scenario](docs/scenario.md)
- [Timeline](docs/timeline.md)
- [Decision flows](docs/decision-flows.md)
- [Roles and RACI](docs/roles-raci.md)
- [Framework mapping](docs/framework-mapping.md)
- [Evidence guide](docs/evidence-guide.md)

## Contents

`docs/` provides operational guidance, scenario, timeline, decision flows, framework mapping, and evidence notes. `evidence/` contains sanitized synthetic CSV/JSON fixtures and a SHA-256 manifest. `templates/` contains incident, decision, custody, and communications records. `site/` contains a dependency-free interactive walkthrough.

## What this demonstrates

- Intake, validation, severity, scoping, containment, eradication, recovery, and lessons learned.
- Decision paths for email-only delivery, credential theft, mailbox compromise, endpoint interaction, and payment risk.
- Fictional UTC timeline with uncertainty and evidence limitations preserved.
- RACI, communications, chain-of-custody, and decision-log templates.
- Mapping to current NIST SP 800-61 Rev. 3 and selected MITRE ATT&CK Enterprise techniques.
- Synthetic email, identity, mailbox, endpoint, and finance fixtures with a SHA-256 manifest.

## Framework sources

- NIST, [SP 800-61 Rev. 3: Incident Response Recommendations and Considerations for Cybersecurity Risk Management](https://csrc.nist.gov/pubs/sp/800/61/r3/final). Finalized April 2025 and supersedes Rev. 2. The crosswalk maps operational actions to CSF 2.0 Functions; it does not claim this playbook's stages are the NIST lifecycle.
- MITRE, [ATT&CK Enterprise](https://attack.mitre.org/). Behavior mapping is illustrative and not attribution.

## Safe use and limits

Never open a suspicious attachment or follow a suspicious link to verify it. Use approved analysis tooling. Preserve evidence when safe and practical; containment takes priority when harm is active. Confirm every action is authorized and scoped. Legal, privacy, regulatory, law-enforcement, and customer-notification decisions belong to authorized organizational owners.

All sample records use fictional reserved `.example` domains and documentation IP ranges. No sample telemetry represents a real organization or incident. “Not observed” does not mean “did not occur.”

## License

Documentation and original visuals are provided under the MIT License. Adapt the playbook and validate authorities, contacts, tools, retention rules, and notification requirements before operational use.
