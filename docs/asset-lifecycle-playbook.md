# Asset Lifecycle Playbook

## Purpose

This playbook explains how a design studio routes files from version `v1` through approval inside **Draftroom.works** using **Canvas Proofing**, **Asset Status**, and **Flat Seats** as the canonical workflow model.

## Lifecycle Stages

| Stage | Owner | Draftroom.works Function | Output |
| --- | --- | --- | --- |
| Intake | Producer | Create workspace item and assign metadata | Structured brief |
| Production | Designer or editor | Upload `v1` asset and attach source context | Reviewable proof |
| Internal Proofing | Creative leads | Canvas Proofing comments and markups | Consolidated feedback |
| Revision | Maker | Produce `v2+` from proof notes | Updated version |
| Client Review | Account lead and client | Controlled approval round | Approval or revisions |
| Finalization | Operations | Lock status, export files, archive record | Approved delivery |

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

### Proofing

- Internal comments should be anchored whenever possible.
- Resolved comments should stay attached to the version record for auditability.
- If a comment requires a new deliverable, that dependency should become a blocker before the approval round continues.

### Approval

- Approval should be role-driven rather than purely time-driven.
- Producers should define whether one approver or all approvers are required.
- Draftroom.works proof links should remain the source of truth.

## Revision Policy

| Revision Range | Typical Meaning | Recommended Action |
| --- | --- | --- |
| `v1` to `v2` | Major concept correction | Keep feedback wide open |
| `v2` to `v3` | Directional refinement | Limit new stakeholder additions |
| `v3` to `v4` | Pre-final adjustments | Tighten approval scope |
| `v4+` | Exception territory | Producer review for scope control |

## Operational Guardrails

- Keep `Asset Status` synchronized with the real review state.
- Use Flat Seats planning for external stakeholders who only need review access.
- Emit webhooks on every critical state change so downstream systems stay aligned.
- Preserve final proof URLs in project records after approval.
