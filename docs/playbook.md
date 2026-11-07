# Phishing Incident Response Playbook

## Purpose and assumptions

Guide a security team from intake through closure for suspected phishing, credential theft, mailbox compromise, malware delivery, and business email compromise (BEC). Assume an organization has designated incident authority, approved mail/identity/endpoint tools, a restricted evidence store, and named escalation contacts. Record and escalate any missing assumption.

All actions must be authorized and proportionate. Verify payment or account changes through known-good contact details. Preserve evidence when safe and practical. Avoid interacting with attacker infrastructure except through approved analysis services.

## Objectives

1. Protect people, systems, data, and operations.
2. Establish what happened, who or what was affected, and what remains uncertain.
3. Contain access and remove malicious artifacts while preserving evidence where feasible.
4. Restore trusted operations and prevent recurrence.
5. Maintain an auditable record of decisions, evidence, communications, and follow-up.

## Intake and validation

Create a unique incident ID. Capture reporter, reporting channel, UTC time, original message location, recipients, user interaction, and observed impact. Preserve the original message and full headers in an approved restricted location; record source and hash where supported. Do not ask reporters to forward it to personal accounts.

Use approved tools to validate sender/reply-to alignment, SPF/DKIM/DMARC results, message ID, delivery scope, URL redirects/reputation, attachment metadata/hash, and gateway verdicts. Authentication results are signals, not proof of benign or malicious intent.

Ask neutrally: did the user open the message, click a link, enter credentials, approve MFA, download/open a file, reply, disclose information, or change payment details? When, and on which device/network? Record exact answers without blame.

## Severity and escalation

Severity is provisional; reassess after material findings. Highest applicable condition governs.

| Level | Example criteria | Coordination |
|---|---|---|
| SEV-1 Critical | Confirmed privileged/executive compromise; active payment fraud; broad malware execution; material sensitive-data exposure; widespread service impact | Incident commander, executive, security, identity, mail, endpoint, legal/privacy, finance/business; frequent updates |
| SEV-2 High | Credential/MFA compromise; mailbox control; multiple users/endpoints; suspected data access; targeted BEC | Incident lead, identity, mail, endpoint, business owner, legal/privacy as indicated |
| SEV-3 Moderate | User interaction without confirmed compromise; limited scope | Security and service owners; legal/privacy when facts warrant |
| SEV-4 Low | Blocked/reported message with no interaction or compromise indicators after scoped checks | Security queue; trend tracking |

Escalate before attribution is complete when harm is active, regulated data may be involved, funds may move, or a critical account is affected. Legal/privacy and authorized leadership determine notifications and deadlines; security supplies facts and preserves records.

## Triage and scope

Search mail telemetry for exact message ID, sender, reply-to, subject, URL, attachment hash, and variants. Identify delivered, quarantined, forwarded, replied-to, and deleted copies. Correlate identity sign-in/MFA/token events, mailbox audit, endpoint, DNS/proxy, and application logs with a consistent UTC window. Normalize clock offsets and record source timezone.

List affected users, accounts, mailboxes, devices, applications, data classes, transactions, and processes. Separate confirmed facts, assessments, and unknowns. Record query window, sources, retention gaps, and limits. Missing telemetry is an evidence gap, not a negative finding.

### Email-only branch

Remove/quarantine confirmed malicious copies with approved tools. Block validated indicators after checking business impact. Search variants, replies, and forwarding. Close only after scoped searches support no interaction/compromise indicators; retain residual uncertainty.

### Link or attachment interaction

Determine whether credentials were submitted, code executed, or data disclosed. If execution is possible, isolate using approved EDR and preserve evidence as feasible. Scope process, persistence, network, and file indicators. If isolation creates safety/availability risk, incident command and service owner choose a compensating action and document it.

### Credentials or MFA

Use verified identity procedures. Revoke active sessions/refresh tokens where supported; reset credentials; review or reset MFA methods if compromise is plausible; inspect sign-in, token, device, privileged role, app consent/OAuth, and cross-service access. A password change alone may not invalidate stolen sessions.

### Mailbox control or BEC

Assess unauthorized inbox rules, forwarding, delegates, send-as permissions, OAuth grants, sent/deleted items, recovery methods, and audit events. Restrict the account if justified; preserve pre-change state. Notify intended recipients through a trusted channel. For payment risk, contact Finance and the bank through known-good numbers immediately; request hold/recall when available and preserve approvals and references.

## Containment, eradication, recovery

Select containment based on evidence, blast radius, and business impact. Options include message purge, validated sender/URL blocks, account restriction, session revocation, credential/MFA reset, grant/rule removal, endpoint isolation, and transaction hold. Confirm target and authority. Record operator, time, change, rationale, impact, and verification.

Remove known access paths and payloads after evidence preservation. Validate removal of unauthorized rules, grants, tokens, sessions, persistence, and endpoint artifacts. Re-scan and search campaign indicators across the environment.

Restore in a controlled order. Verify user identity out of band; validate endpoint health and account configuration; re-enable least-privilege access; monitor sign-ins, mailbox changes, outbound messages, and transactions during an organization-defined observation period. Confirm workflows and data are intact. An alert closure or password reset alone does not prove recovery.

## Communications and records

The incident lead maintains audience-specific updates. Avoid credentials, unnecessary sensitive data, unverified attribution, and broad circulation of indicators. Use `templates/communications.md`. Counsel/privacy and authorized leadership determine external notifications.

Maintain `templates/incident-record.md`, `templates/decision-log.csv`, and `templates/chain-of-custody.csv`. Store evidence in a restricted location; use stable IDs and hashes in general updates.

## Closure and improvement

Close only when scope and impact are recorded; containment/eradication verified; recovery accepted by service owner; evidence and integrity notes captured; legal/privacy/finance decisions recorded where applicable; monitoring completed or handed off; residual risks accepted by an authorized owner; and corrective actions have owners, due dates, and measurable closure evidence.

Conduct a blameless review. Track gaps and update procedures after exercises, incidents, or material tool/process changes. See `docs/scenario.md` and `docs/timeline.md` for the fictional exercise.
