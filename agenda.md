# Milestone 1.3 Internal Team Meeting — Agenda

**Date:** <!-- Insert date -->
**Time:** <!-- Insert time -->
**Location / Call Link:** <!-- Insert link -->
**Facilitator:** <!-- Insert name -->

---

## Purpose

The purpose of this meeting is to present the completed OpenShift RBAC Automation implementation to the internal platform engineering team. This includes a walkthrough of the reference architecture, a review of the documentation produced, and a hands-on discussion to ensure the team understands how to operate and support the automation going forward.

---

## Attendees

| Name | Role |
|------|------|
| <!-- Name --> | Platform/OCP Engineer |
| <!-- Name --> | Platform/OCP Engineer |
| <!-- Name --> | Platform Lead |

---

## Agenda

**1. Introduction and Context (5 min)**
- Overview of what was delivered in Milestones 1.1 and 1.2
- Why this automation was built and what problem it solves
- Scope of today's session

**2. Reference Architecture Walkthrough (20 min)**
- Review of the end-to-end RBAC architecture diagram
- How OIM, LDAP Group Sync, and the Namespace Configuration Operator work together
- Namespace-level automation: NamespaceConfig, mnemonic-based labeling, and RoleBinding generation
- Cluster-level automation: GroupConfig and ClusterRoleBinding generation
- Production vs. non-production access model (no admin binding in PROD)

**3. Documentation Review (15 min)**
- Walkthrough of the naming conventions for LDAP groups and RoleBindings
- Operator-stamped provenance annotations and what they indicate
- Onboarding guide: how a new mnemonic/namespace gets set up end-to-end
- Self-service access request flow for application teams

**4. Team Q&A and Discussion (15 min)**
- Open floor for the team to ask questions on the architecture or implementation
- Clarify any operational responsibilities
- Identify gaps or concerns the team wants documented

**5. Operational Handoff (10 min)**
- Who owns what going forward
- How to handle new mnemonic onboarding requests
- Escalation path for issues or edge cases
- Where the documentation and manifests live: `ephico2real2/openshift-rbac-automation`

**6. Action Items and Next Steps (5 min)**

| Action Item | Owner | Due Date |
|-------------|-------|----------|
| | | |
| | | |

---

**Next Meeting:** <!-- Date and purpose -->
