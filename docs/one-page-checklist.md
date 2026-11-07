# Phishing Incident Response | One-page Checklist

**Use with the full playbook.** Record times in UTC and use the incident ID on every record. Confirm authority and local procedures before action.

## First 15 minutes
- [ ] Open an incident record; capture reporter, received time, original message, and reporting channel.
- [ ] Preserve the original message and headers in the approved evidence location. Do not click links or attachments.
- [ ] Validate sender, authentication, URLs, attachment metadata, message ID, recipients, and delivery status using approved tools.
- [ ] Ask whether the reporter clicked, opened, entered credentials, approved MFA, downloaded a file, replied, or changed payment details. Record answers without blame.
- [ ] Search mailboxes for exact message and variants, including quarantine and deleted items where supported.
- [ ] Assign severity and an incident lead; engage identity, messaging, endpoint, legal/privacy, and business owners as indicated.

## Decide and contain
- [ ] Email only: remove/quarantine matching messages; block validated indicators after checking business impact.
- [ ] Link clicked or file opened: assess execution; isolate endpoint through approved EDR if warranted; preserve evidence where feasible.
- [ ] Credentials entered or MFA approved: revoke sessions/tokens, reset credentials through verified channels, review MFA methods and sign-in logs.
- [ ] Mailbox compromise suspected: restrict account if justified; remove unauthorized rules/forwarding/delegates; review sent/deleted mail, OAuth grants, and audit events.
- [ ] Payment or sensitive data exposure possible: stop affected transactions through established channels; involve finance, counsel, privacy, and leadership.
- [ ] Record each action, actor, time, source, rationale, and result.

## Scope and recover
- [ ] Determine affected users, devices, mailboxes, sessions, applications, data, and business processes.
- [ ] Hunt related sender infrastructure, URLs, hashes, sign-ins, mailbox changes, and endpoint alerts.
- [ ] Validate containment with repeat searches and documented observation window.
- [ ] Restore access only after identity and endpoint checks; monitor for recurrence.
- [ ] Verify changed payment instructions via a known-good contact method.
- [ ] Document impact, decisions, evidence locations/hashes, uncertainty, and owned corrective actions.

## Escalate immediately when
Executive or privileged account; successful credential/MFA compromise; active mailbox manipulation; multiple victims; malicious execution; sensitive or regulated data; payment fraud; persistence; safety/availability impact; or media/regulator inquiry.

**Authority reminder:** account disablement, endpoint isolation, external statements, legal holds, notifications, and law-enforcement contact must follow approved authority and escalation paths.
