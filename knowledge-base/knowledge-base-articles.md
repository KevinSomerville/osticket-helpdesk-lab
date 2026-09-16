# Knowledge Base Articles

---

# Account Lockout / Password Reset

**Category:** Account Access
**Priority:** Low / P4
**Audience:** End User / Tier 1 Agent
**Last Updated:** 2026-09-16

## Summary
A team member is locked out of their account and unable to log in. This is a routine, low-impact issue that a single user, with no wider system impact.

## Symptoms
- User reports being unable to log into their account
- Repeated failed login attempts may have triggered an automatic lockout
- No error suggesting a security compromise (see Security Incident article if that is suspected instead)

## Resolution Steps
1. Verify the user's identity (employee ID, manager confirmation, or verified email).
2. Navigate to Admin Panel > Staff Members > [Select User].
3. Unlock the account if it was locked due to failed attempts.
4. Issue a temporary password reset and send it to the user's verified email.
5. Confirm the user can log in successfully and prompt them to set a new password.
6. Close the ticket once access is confirmed restored.

## Escalation Criteria
Escalate to Tier 2 only if the lockout appears linked to suspicious activity (unrecognized login location, repeated lockouts in a short window) rather than a simple forgotten password.

## Related Tickets
Ticket #1 (Low/P4) - Account lockout, access restored.

---

# Permission Removal Request

**Category:** Permission Request
**Priority:** Medium / P3
**Audience:** Tier 1 Agent
**Last Updated:** 2026-09-16

## Summary
A team member has requested that another team member's permissions be removed, typically due to a role change, offboarding, or department transfer.

## Symptoms
- Requesting user asks for another named team member's access to be revoked or reduced
- No immediate outage or system-wide impact, but delay in fulfilling the request could create a compliance or access-control risk

## Resolution Steps
1. Confirm the requester has the authority to make this change (manager, HR, or the affected user's direct supervisor).
2. Identify exactly which permissions or systems are in scope for removal.
3. Navigate to Admin Panel > Staff Members > [Select Affected User].
4. Remove or downgrade the specified permissions.
5. Document what was removed and why in the ticket's internal notes.
6. Notify the requester once the change is complete.

## Escalation Criteria
Escalate to Tier 2 or a system administrator if the permissions in question span multiple systems outside the help desk's direct control, or if the request involves a security-sensitive role (admin, finance, HR systems).

## Related Tickets
Ticket #2 (Medium/P3) - Permission removal request for a team member.

---

# Dashboard Not Updating in Real-Time

**Category:** Minor Software Bug
**Priority:** Medium / P3
**Audience:** Tier 1 Agent
**Last Updated:** 2026-09-16

## Summary
A user reports that a dashboard element is not refreshing or updating with current data in real-time, though the rest of the application functions normally.

## Symptoms
- Dashboard values appear static or outdated
- Manually refreshing the page may or may not resolve the issue temporarily
- No other functionality appears to be affected

## Resolution Steps
1. Confirm the specific dashboard element affected and gather a screenshot from the user if possible.
2. Ask the user to hard refresh the page (Ctrl+F5) and clear browser cache, then confirm if the issue persists.
3. Check if the issue is isolated to one user or affecting multiple users (may indicate a backend/server-side issue rather than a client-side one).
4. If isolated to one user, walk them through clearing cache/cookies or trying a different browser.
5. Document findings and outcome in the ticket.

## Escalation Criteria
Escalate to Tier 2 or development if the issue affects multiple users, persists after basic troubleshooting, or appears to stem from a backend data refresh failure rather than a browser-side issue.

## Related Tickets
Ticket #3 (Medium/P3) - Dashboard real-time update bug.

---

# High-Volume Printer Failure

**Category:** Hardware Issue
**Priority:** High / P2
**Audience:** Tier 1 Agent
**Last Updated:** 2026-09-16

## Summary
A high-volume printer in a busy office area has completely stopped working, affecting multiple employees who rely on it for daily printing needs.

## Symptoms
- Printer is unresponsive, powered off unexpectedly, or displaying a hardware error
- Multiple employees are unable to print, creating a workflow bottleneck
- Physical inspection may reveal a paper jam, hardware fault, or power issue

## Resolution Steps
1. Confirm the printer's exact location and the scope of impact (how many users/departments affected).
2. Perform basic troubleshooting on-site: power cycle the printer, check for paper jams, check network/cable connections.
3. Check the printer's display panel or error log for a specific fault code.
4. If basic troubleshooting does not resolve the issue, notify affected staff of an estimated downtime and direct them to the nearest alternate printer.
5. Document the fault code and steps attempted before escalating.

## Escalation Criteria
Escalate to Tier 2 or a hardware vendor if the issue is not resolved by basic troubleshooting, given the number of employees affected and the urgency of restoring a shared business resource.

## Related Tickets
Ticket #4 (High/P2) - High-volume printer failure in a busy office area.

---

# Suspicious Account Activity / Possible Compromise

**Category:** Security Incident
**Priority:** Critical / P1
**Audience:** Tier 1 Agent
**Last Updated:** 2026-09-16

## Summary
A team member discovered they were logged out of their account and found evidence of a login from an unfamiliar location, along with an email sent from their account that they did not send. This indicates a likely account compromise and requires immediate action.

## Symptoms
- User was unexpectedly logged out of their account
- Login history shows access from an unrecognized location
- An email was sent from the user's account without their knowledge

## Resolution Steps
1. Immediately disable or lock the affected account to prevent further unauthorized activity.
2. Force a password reset and revoke any active sessions or tokens tied to the account.
3. Review the account's recent login history and sent items to assess the scope of the compromise.
4. Document the timeline of events (last known legitimate login, time of suspicious login, time of unauthorized email) in the ticket.
5. Escalate immediately per the criteria below, this should not be fully resolved at Tier 1 alone.

## Escalation Criteria
Escalate immediately to Tier 2/Security team. This is a Critical/P1 incident by default: any indication of account compromise, unauthorized access, or unrecognized account activity requires immediate escalation regardless of the user's role or the apparent scope of impact.

## Related Tickets
Ticket #5 (Critical/P1) - Suspicious login and unauthorized email sent from user's account.
