# Incident Recovery Runbook

## 1. Purpose
This runbook covers the basic recovery steps for on-call incidents in this repository.

## 2. Scope
- Locating the runbook and first-response checklist
- Killing a stuck CI job that is burning runner minutes

## 3. First Response
1. Acknowledge the page and join the incident bridge.
2. Open the first-response checklist: `checklist.md`.
3. Identify the affected system and blast radius.
4. Escalate if the incident is not contained within 15 minutes.

## 4. CI Run Recovery
1. Identify the stuck workflow run (repo → Actions tab, or `gh run list`).
2. Confirm the run is genuinely stuck (no progress, no output, exceeding expected duration).
3. Cancel the run: `gh run cancel <run-id>` (or Actions UI → Cancel workflow).
4. Verify the run shows status `cancelled`.

## 5. Escalation Contacts
- Primary on-call: _TBD_
- Secondary on-call: _TBD_
- Manager escalation: _TBD_

## 6. Post-Incident
1. Capture a timeline of events.
2. File follow-up actions from the outage review.
3. Rehearse this runbook quarterly.
