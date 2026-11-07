# Framework Mapping

Illustrative cross-references only; they do not certify compliance or imply a procedure satisfies every control. Validate current organizational requirements and framework versions.

## NIST SP 800-61 Rev. 3 and CSF 2.0

NIST finalized SP 800-61 Rev. 3 in April 2025, superseding Rev. 2. Rev. 3 integrates incident response throughout the six CSF 2.0 Functions. This practical crosswalk does not claim that this project's six operational stages are NIST's lifecycle model.

| Playbook activity | CSF 2.0 Function(s) supported | Example evidence |
|---|---|---|
| Preparation: contacts, authority, tools, templates, exercise | Govern, Identify, Protect | Contact roster, approved procedures, exercise findings |
| Intake, validation, severity, scope | Detect, Respond | Incident record, indicators, affected entities, timeline |
| Purge, session revocation, account restriction, isolation | Respond | Decision/action records and impact notes |
| Remove rules, grants, payloads, access paths | Respond | Before/after state and validation searches |
| Restore workflows and monitor | Recover, Detect | Recovery approval, observation log, owner acceptance |
| Review and corrective actions | Govern, Identify, Protect, Detect, Respond, Recover | Lessons, action register, updated playbook |

Source: NIST [SP 800-61 Rev. 3](https://csrc.nist.gov/pubs/sp/800/61/r3/final). The stages above remain useful operational steps for this exercise; the mapping uses the current publication's CSF 2.0 framing.

## MITRE ATT&CK Enterprise

| Fictional behavior | Technique | Boundary |
|---|---|---|
| Social engineering email with link | [T1566.002 Spearphishing Link](https://attack.mitre.org/techniques/T1566/002/) | Pattern only, no attribution |
| Credential entry on lookalike portal | [T1056.003 Web Portal Capture](https://attack.mitre.org/techniques/T1056/003/) | Described credential-entry behavior only |
| Use of valid account | [T1078 Valid Accounts](https://attack.mitre.org/techniques/T1078/) | Synthetic session; access scope uncertain |
| Unauthorized mail forwarding rule | [T1114.003 Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003/) | Represented by synthetic audit fixture |

## Sources and limits

ATT&CK mapping describes observed fictional behaviors, not actor attribution or exhaustive coverage. Record confidence separately from framework labels.
