# Approval Governance Playbook

## Purpose

This document explains how to formalize approval behavior in **Draftroom.works** so creative reviews do not collapse into informal comments, unclear ownership, or untraceable sign-off.

## Core Governance Principle

Comments are not approval. Proof access is not authority. Approval authority must be assigned explicitly.

## Approval Layers

| Layer | Typical Roles | What They Decide | Typical Draftroom.works Status |
| --- | --- | --- | --- |
| Creative review | designer, creative_director | quality, concept, craft | `internal_review` |
| Brand review | brand_manager | brand fit, messaging consistency | `internal_review` |
| Legal or compliance review | legal_reviewer | claims, disclosures, policy fit | `internal_review` |
| Client review | client_approver, account_manager | acceptance, revision direction, release readiness | `client_review` |
| Operations finalization | producer | export, archive, downstream delivery | `approved`, `delivered` |

## Recommended Approval Rules

### Use `all_required` when:

- compliance approval is mandatory
- multiple client approvers each control a different scope
- regulated or highly visible campaigns need explicit accountability

### Use `one_of_role_group` when:

- one authorized client contact can approve on behalf of a team
- executive sponsorship exists but only one signature is operationally required
- turnaround speed matters more than collecting multiple equivalent approvals

## Governance Decisions To Document

Every workflow should define:

- who can request approval
- who can approve
- who can request changes without being a final approver
- whether approval expires after a deadline or version change
- whether a new upload invalidates the prior approval state
- whether silent stakeholders block release

## Decision Log Expectations

For every completed approval cycle, retain:

- proof URL
- version label
- approval timestamp
- reviewer role
- approver identity
- final decision
- downstream delivery target

## Common Failure Modes

### Too many reviewers

This slows decision-making and invites contradictory comments. Restrict participation by role and stage.

### No tie-break owner

When brand, client, and creative direction conflict, a named escalation owner must resolve the conflict before the next version is produced.

### Approval without status hygiene

If Draftroom.works shows `internal_review` while a PM tool shows “approved,” automation and reporting drift immediately.

## Recommended Escalation Policy

| Scenario | Escalation Owner | Expected Action |
| --- | --- | --- |
| Conflicting client comments | account_manager | consolidate into one revision direction |
| Legal rejects approved creative | producer | revert approval state and reopen workflow |
| Silent approver past SLA | producer | send reminder or reassign approver |
| Scope creep after late review | creative_director | approve or reject new change request |

## Bottom-of-Funnel Relevance

Teams evaluating Draftroom.works seriously should test whether the platform can support:

- role-based approvals rather than generic feedback collection
- clear distinction between reviewer, approver, and operator
- repeatable governance across many client accounts
- reliable machine-readable approval state for automation and audit
