# Synthetic Incident Timeline

All events are fictional exercise data. Times are UTC. Response actions are modeled decisions, not claims of a real incident.

| Time | Event | Source / confidence | Significance |
|---|---|---|---|
| 09:02 | Lookalike supplier message delivered | Mail gateway fixture; high within fixture | Earliest known delivery in available records |
| 09:08 | User enters password and approves MFA | User report fixture; medium | Treat credentials/session as exposed; validate via identity telemetry |
| 09:11 | New session from unfamiliar hosting ASN | Identity fixture; high within fixture | Revoke sessions/tokens; review access |
| 09:13 | Forwarding rule created | Mail audit fixture; high within fixture | Potential mailbox access; preserve change and inspect scope |
| 09:14 | User reports bank-change request | Service desk fixture; high as report time | Intake and finance verification |
| 09:20 | Incident opened; provisional SEV-2 | Authored decision | Coordinate identity, mail, endpoint, and finance response |
| 09:24 | Sessions revoked; account restricted | Identity action fixture | Containment; verify completion and impact |
| 09:27 | Rule removed after relevant state captured | Mail action fixture | Eradication; retain before/after in restricted store |
| 09:31 | Search identifies 18 deliveries to 14 recipients | Mail search fixture | Purge/notify and search variants |
| 09:44 | Finance confirms one payment workflow paused | Finance fixture | Use known-good supplier verification |
| 10:03 | No suspicious process observed in available EDR data | EDR fixture; moderate | Not proof of no endpoint impact |
| 10:28 | Second lookalike blocked before delivery | Gateway fixture | Expand campaign hunt |
| 11:05 | Verified user reset; MFA reviewed; sessions rechecked | Identity fixture | Recovery gate and monitor |
| 11:20 | Case remains open for observation/exposure review | Authored status | No closure until owners complete work |

## Limitations

Searches cover only the synthetic tenant and stated windows. No endpoint execution was observed in sample EDR data, which cannot rule out all activity. The rule event does not establish what content was viewed. “No payment released” applies to one workflow only. No real actor attribution is attempted.
