# Triage, Containment, and Recovery Decision Flows

```mermaid
flowchart TD
 A[Report received] --> B[Open record; preserve original message]
 B --> C{Suspicious?}
 C -- No or unclear --> D[Safe analysis; retain uncertainty; monitor]
 C -- Yes --> E[Search recipients, variants, URLs, files, replies]
 E --> F{User interacted?}
 F -- No --> G[Purge; validated blocks; scoped search]
 G --> H{Compromise indicators or sensitive exposure?}
 H -- No --> I[Monitor; document limits; close with owner]
 H -- Yes --> J[Escalate]
 F -- Click or open --> K[Assess credential entry and execution]
 F -- Credentials or MFA --> L[Revoke sessions; verified reset; review identity]
 F -- Mailbox control --> M[Restrict account; preserve state; inspect rules and grants]
 F -- Payment or data --> N[Engage finance, legal/privacy, leadership]
 K --> O[Scope endpoint; isolate if warranted and authorized]
 L --> P[Search sign-ins, tokens, roles, apps, mailbox changes]
 M --> Q[Remove unauthorized access; review sent/deleted/forwarded activity]
 N --> R[Assess impact and notification with authorized owners]
 O --> S[Eradicate; validate; recover with monitoring]
 P --> S
 Q --> S
 R --> S
 S --> T{Containment verified and recovery gates met?}
 T -- No --> J
 T -- Yes --> U[Observe; document uncertainty; approve closure]
 U --> V[After-action review; track improvements]
```

| Gate | Proceed when | Stop/escalate when |
|---|---|---|
| Validate | Indicators/account preserved; approved tools used | Authority unclear, analysis unsafe, or evidence may be destroyed |
| Contain identity | User verified; scope and impact understood | Privileged identity, critical dependency, or uncertain blast radius |
| Isolate endpoint | Correct device and evidence needs considered | Safety, availability, or forensic conflict requires decision |
| Stop payment | Finance uses known-good workflow and authorized approver | Suspected loss: engage finance leadership/bank per policy |
| Recover | Access path removed, checks pass, owner accepts | Recurrence or material unknown remains |
| Close | Approvals, evidence, monitoring handoff, owners documented | High-impact unknown or unowned risk remains |
