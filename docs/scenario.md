# Scenario | Northstar Creative BEC

## Exercise brief

Northstar Creative is a fictional 240-person digital services company. At 09:14 UTC on 2026-10-20, Finance reports an apparent supplier email requesting an urgent bank-detail change. It includes a lookalike sign-in link. A finance analyst says they entered their work password and approved one MFA prompt. A second employee received the message but did not interact.

The exercise begins at 09:20 UTC. Participants act as the response team. The facilitator reveals evidence in stages. Prioritize containment and fact gathering; do not assume the initial report captures full scope.

## Injects

| UTC | Inject | Decision pressure |
|---|---|---|
| 09:20 | User confirms password entry and one MFA approval; unsure whether the page loaded. | Severity, identity containment, user support |
| 09:28 | Identity logs show a new session from an unfamiliar hosting ASN. | Revoke sessions/tokens; assess identity scope |
| 09:36 | Mail audit shows a forwarding rule created, then removed by containment. | Preserve state; inspect mailbox access |
| 09:45 | Search finds 18 deliveries to 14 users; one reply contains no sensitive attachment. | Campaign scope, purge, recipient communications |
| 10:02 | A draft invoice payment is scheduled for 15:00 but not yet approved. | Pause workflow; verify supplier out of band |
| 10:18 | Endpoint telemetry shows no suspicious process or download; coverage is current. | State confidence and limitations accurately |
| 10:42 | A second lookalike domain is blocked before delivery. | Expand hunt and indicator controls |
| 11:20 | User is verified, password reset, sessions revoked, MFA reviewed; monitoring active. | Recovery gate and observation window |

## Authored case outcome

Synthetic evidence models credential disclosure and session creation, a short-lived unauthorized forwarding rule, no confirmed payment release, no observed endpoint execution, and a second blocked campaign variant. It does **not** establish that no data was viewed or copied. Audit coverage is finite; exposure review and monitoring remain follow-up work.

## Facilitator prompts

- Which facts raise severity, and which remain unverified?
- What can be done quickly without destroying important evidence?
- Who can authorize session revocation, account restriction, endpoint isolation, or payment pause?
- What is needed to close each decision branch?
- How do participants distinguish “not observed” from “did not occur”?

Scenario times are authored inject times and are not response-time performance claims.
