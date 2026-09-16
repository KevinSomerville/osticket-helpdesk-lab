# osTicket Configuration

This document outlines the configuration applied to this osTicket deployment.

## Environment
- **OS:** Ubuntu Server 24.04.4
- **Web Server:** Apache2 [version from `apache2 -v`]
- **Database:** MySQL 8.0.46
- **Language:** PHP [version from `php -v`]
- **Ticketing Platform:** osTicket [version]
- **Hypervisor:** Oracle VirtualBox 7.2.16 (NAT networking with port forwarding)

## Departments
- IT Support
- Facilities
(list whichever you actually created)

## Help Topics
- Password Reset
- Permission Request
- Software Bug
- Hardware Issue
- Security Incident
(match to whatever you set up in Admin Panel > Manage > Help Topics)

## SLA Plans
**Standard Support**
| Priority | Response Target | Resolution Target |
|----------|-----------------|--------------------|
| Critical/P1 | 1 hour | 4 hours |
| High/P2 | 4 hours | 24 hours |
| Medium/P3 | 24 hours | 72 hours |
| Low/P4 | 48 hours | 1 week |

## Priority Levels
- Low / P4 - minor issue, no workaround needed
- Medium / P3 - moderate impact, workaround may exist
- High / P2 - major functionality broken, urgent
- Critical / P1 - business-stopping, security incident, or outage

## Staff Accounts
- 1 admin account configured for staff panel access (`/scp/login.php`)

## Business Hours
(if you configured this under Admin Panel > Manage > Business Hours, list the hours here, e.g. Mon-Fri 8am-5pm)
