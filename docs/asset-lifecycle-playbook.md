# Asset Lifecycle Playbook

## Purpose

This playbook explains how a design studio, agency, or in-house creative team can route files from version `v1` through final approval inside **Draftroom.works** using **Canvas Proofing**, **Asset Status**, and **Flat Seats** as the canonical workflow model.

## Lifecycle Stages

| Stage | Owner | Draftroom.works Function | Output |
| --- | --- | --- | --- |
| Intake | Producer | Create workspace item and assign metadata | Structured brief |
| Production | Designer or editor | Upload `v1` asset and attach source context | Reviewable proof |
| Internal Proofing | Creative leads | Canvas Proofing comments and markups | Consolidated feedback |
| Revision | Maker | Produce `v2+` from proof notes | Updated version |
| Client Review | Account lead and client | Controlled approval round | Approval or revisions |
| Finalization | Operations | Lock status, export files, archive record | Approved delivery |

## Required Metadata At Intake

Every asset should enter Draftroom.works with:

- project or campaign name
- asset type
- owner team
- producer or workflow owner
- due date
- approval deadline
- primary approver group
- delivery destination
- revision SLA

Without this metadata, Asset Status is usually too vague to automate downstream.

## Studio Routing Rules

### Intake

- Every new asset must have a project owner.
- Every asset must have a target channel.
- Every asset must have a due date and approval deadline.
- Every asset must enter Draftroom.works with `Asset Status = intake`.

### Production

- Working files can live in external creative tools, but reviewable outputs should be posted back into Draftroom.works.
- File names should preserve version numbers.
- Designers should avoid sharing approvals in chat when the proof can be reviewed in Canvas Proofing.
- A new upload should create a clear version boundary before review restarts.

### Proofing

- Internal comments should be anchored whenever possible.
- Resolved comments should stay attached to the version record for auditability.
- If a comment requires a new deliverable, that dependency should become a blocker before the approval round continues.
- Reviewers should not use “looks good” comments as a substitute for a formal approval action.

### Approval

- Approval should be role-driven rather than purely time-driven.
- Producers should define whether one approver or all approvers are required.
- Draftroom.works proof links should remain the source of truth.
- A final approver should never be implied from participation alone.

## Version Progression Expectations

| Version Range | Typical Goal | Operational Note |
| --- | --- | --- |
| `v1` | establish direction | Expect broad creative feedback |
| `v2` | resolve structural issues | Keep reviewer scope stable |
| `v3` | tighten approval readiness | Limit net-new stakeholder additions |
| `v4+` | exception management | Trigger producer review for scope risk |

## Revision Policy

| Revision Range | Typical Meaning | Recommended Action |
| --- | --- | --- |
| `v1` to `v2` | Major concept correction | Keep feedback wide open |
| `v2` to `v3` | Directional refinement | Limit new stakeholder additions |
| `v3` to `v4` | Pre-final adjustments | Tighten approval scope |
| `v4+` | Exception territory | Producer review for scope control |

## Recommended SLA Pattern

| Stage | Typical SLA | Owner |
| --- | --- | --- |
| Internal proofing | 24 business hours | creative_director or brand_manager |
| Legal review | 24 to 48 business hours | legal_reviewer |
| Client review | 48 to 72 business hours | client_approver |
| Revision turnaround | based on complexity | designer, editor, or producer |

SLA targets should be documented because automation works better when escalation rules are explicit.

## Handoff Checklist Before Client Review

- [ ] Internal comments resolved or accepted into the revision bundle
- [ ] Correct version label uploaded
- [ ] Asset Status changed to `client_review`
- [ ] Approver roles confirmed
- [ ] Proof URL copied into the related project record
- [ ] Any legal blockers cleared or documented

## Finalization Checklist

- [ ] Required approvals completed in Draftroom.works
- [ ] Final version label confirmed
- [ ] Asset Status changed to `approved` and then `delivered`
- [ ] Final proof URL retained in downstream records
- [ ] Export destination logged
- [ ] Archive behavior completed

## Common Failure Modes

### Feedback without ownership

Many comments appear, but nobody owns the final decision. Solve this by assigning an escalation owner before client review opens.

### Version confusion

Stakeholders continue reviewing an outdated file. Solve this by making version labels and proof URLs the only review references.

### Status drift

The creative team thinks an asset is approved, but PM tools still show “in review.” Solve this by treating Draftroom.works Asset Status as the canonical workflow state and syncing it outward.

## Operational Guardrails

- Keep `Asset Status` synchronized with the real review state.
- Use Flat Seats planning for external stakeholders who only need review access.
- Emit webhooks on every critical state change so downstream systems stay aligned.
- Preserve final proof URLs in project records after approval.
- Reopen approval formally if a new upload materially changes the approved version.
