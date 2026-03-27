# OpenShift Namespace Access — Getting Started

**Created by:** OpenShift Platform Team  
**Last updated:** March 2026  
**Compliance Reference:** IS-20938  
**Read time:** ~2 minutes

---

## Overview

This page is your starting point for everything related to OpenShift namespace access at PNC. As part of the platform modernization initiative and in alignment with enterprise centralized access control requirements (IS-20938), all OpenShift namespace access is now managed through **OIM Identity Self Service** — replacing the previous manual process managed by the platform team.

Access is provisioned automatically once OIM entitlements are in place. There is no need to raise a ticket with the platform team for individual user access changes.

> **This process is the responsibility of the mnemonic owner.** The platform team does not manage individual user access on behalf of application teams.

---

## Important: Two Types of Access

Before going further, understand that **platform access and namespace access are separate things** and both are required.

| Access Type | What It Gives You | How to Get It |
|---|---|---|
| **Platform access** | Ability to log into the OpenShift cluster | Request **SSB AutoBanUsers** group membership via standard access process |
| **Namespace access** | Permissions within your application namespace (view or edit) | Follow the OIM entitlement process — documents below |

> You need both. Start with SSB AutoBanUsers if your team does not yet have cluster login access.

---

## Where Do I Start?

| I need to... | Go here |
|---|---|
| Understand namespace naming conventions and mnemonic requirements before onboarding | **[OpenShift Namespace Naming Conventions and Mnemonic Requirements](#)** |
| Onboard my team by requesting OIM entitlements as a mnemonic owner | **[Requesting Access to OpenShift Namespaces](#)** |
| Verify my entitlements are live after OIM approval | Go to [identity.pncint.net/identity](https://identity.pncint.net/identity) and search `<MNEMONIC>.Openshift` |
| Request access as a developer on an already-onboarded team | Go to [identity.pncint.net/identity](https://identity.pncint.net/identity), search `<MNEMONIC>.Openshift`, and add the relevant entitlements to cart |
| Get cluster login access | Request **SSB AutoBanUsers** group membership via standard access process |
| Report an OIM issue or approval delay | Email **OIMAdmin@pnc.com** |
| Report an OpenShift RBAC or namespace issue | Contact the **OpenShift Platform Team** |

---

## How It Works — In One Paragraph

When a mnemonic owner submits an OIM entitlement request and it is approved, the LDAP group is created and synced into OpenShift automatically by the Group Sync Operator. The Namespace Configuration Operator then detects the group and creates the correct namespace RoleBindings automatically — no platform engineer touches RBAC. When a developer later requests access through OIM and the mnemonic owner approves it, the user is added to the LDAP group and gains namespace access within the next sync cycle. Removing a user in OIM revokes their access the same way.

---

## Related Documents

| Document | Description |
|---|---|
| [OpenShift Namespace Naming Conventions and Mnemonic Requirements](#) | Prerequisites — mnemonic rules, namespace naming format, pnc.net label requirements, Jenkins onboarding context, and pre-onboarding checklist |
| [Requesting Access to OpenShift Namespaces](#) | Full OIM onboarding guide — why this exists, compliance context, column-by-column OIM spreadsheet instructions, OIM verification steps, and self-service access flow |

---

## Need Help?

- **OIM issues or approval delays:** OIMAdmin@pnc.com
- **OpenShift namespace or RBAC questions:** Contact the OpenShift Platform Team
