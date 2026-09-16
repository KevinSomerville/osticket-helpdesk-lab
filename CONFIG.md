# osTicket Configuration

This document outlines the configuration applied to this osTicket deployment.

## Environment
- **OS:** Ubuntu Server 24.04.4
- **Web Server:** Apache2 [2.4.58]
- **Database:** MySQL 8.0.46
- **Language:** PHP [8.3.6 cli]
- **Ticketing Platform:** osTicket [v1.18.4]
- **Hypervisor:** Oracle VirtualBox 7.2.16 (NAT networking with port forwarding)

## Departments
- IT Support
- Facilities

## Help Topics
- Password Reset
- Change Request
- Software Bug
- Software Issue
- Security Incident
- Service Request
- Software Install
- VPN/Network Issue


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
- Mon-Fri 8 am-5 pm
