# Framework Mapping

Illustrative cross-references only; they do not certify compliance or imply a procedure satisfies every control. Validate current organizational requirements and framework versions.

## NIST SP 800-61 Rev. 2

| Playbook activity | Phase | Evidence |
|---|---|---|
| Contacts, authority, tools, templates, exercise | Preparation | Contact roster, approved procedures, exercise findings |
| Intake, validation, severity, scope | Detection & Analysis | Incident record, indicators, affected entities, timeline |
| Purge, session revocation, account restriction, isolation | Containment | Decision/action records and impact notes |
| Remove rules, grants, payloads, access paths | Eradication | Before/after state and validation searches |
| Restore workflows and monitor | Recovery | Recovery approval, observation log, owner acceptance |
| Review and corrective actions | Post-Incident Activity | Lessons, action register, updated playbook |

## MITRE ATT&CK Enterprise

| Fictional behavior | Technique | Boundary |
|---|---|---|
| Social engineering email with link | [T1566.002 Spearphishing Link](https://attack.mitre.org/techniques/T1566/002/) | Pattern only, no attribution |
| Credential entry on lookalike portal | [T1056.003 Web Portal Capture](https://attack.mitre.org/techniques/T1056/003/) | Described credential-entry behavior only |
| Use of valid account | [T1078 Valid Accounts](https://attack.mitre.org/techniques/T1078/) | Synthetic session; access scope uncertain |
| Unauthorized mail forwarding rule | [T1114.003 Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003/) | Represented by synthetic audit fixture |

## Sources and limits

NIST: [SP 800-61 Rev. 2](https://csrc.nist.gov/pubs/sp/800/61/r2/final). ATT&CK mapping describes observed fictional behaviors, not actor attribution or exhaustive coverage. Record confidence separately from framework labels.
