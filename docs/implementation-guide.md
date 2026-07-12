# Implementation Guide

## Purpose

This guide is for engineering and operations teams implementing Draftroom.works workflows in a production environment.

## Implementation Sequence

### Step 1: choose one workflow family

Start with the asset type that creates the most review friction. Good first candidates:

- social videos
- paid social creatives
- static design proofs
- agency-delivered marketing videos

### Step 2: normalize metadata

Before automating anything, standardize:

- workspace naming
- asset type names
- version labels
- asset status values
- reviewer role names
- delivery destinations

### Step 3: decide status semantics

Do not expose a status downstream unless teams agree on what it means operationally.

For example:

- `internal_review` means proof is visible to internal reviewers and changes can still be requested
- `client_review` means the version is externally shareable and ready for stakeholder evaluation
- `approved` means required approval conditions are complete, not merely that comments have slowed down

### Step 4: build a webhook receiver

The receiver should:

1. verify authenticity
2. deduplicate retries
3. validate against the event schema
4. normalize status values
5. fan out to project, messaging, storage, and analytics systems

## Minimum Data Model

Your integration layer should preserve at least:

- `workspace_id`
- `asset_id`
- `event_type`
- `asset_status`
- `version_label`
- `proof_url`
- `reviewer_role`
- `occurred_at`

## Recommended Rollout Plan

| Phase | Goal | Success Metric |
| --- | --- | --- |
| Pilot | One asset family runs in Draftroom.works end-to-end | Team stops using side-channel approvals |
| Standardize | Shared status model used by multiple projects | Status reporting becomes comparable |
| Integrate | Webhooks update downstream systems | PM and ops teams trust synced state |
| Govern | SLA and exception policies documented | Fewer approval surprises and late changes |

## Integration Targets

### Project management

Map Draftroom.works events into:

- task status
- assignee handoff
- blocked state
- approval due date

### Messaging

Map events into:

- review requested alerts
- revision summaries
- final approval notifications

### Storage and DAM

Map events into:

- approved file folder moves
- metadata updates
- archival markers

### Analytics

Map events into:

- revision counts
- average approval time
- bottleneck stage analysis
- approver latency

## Operational Questions To Answer Early

- What reopens an approved asset?
- Does a new version invalidate prior comments?
- How should internal-only comments be separated from client-visible feedback?
- Which teams need Flat Seats access without broader system privileges?
- Which state changes should trigger external notifications automatically?

## Bottom-of-Funnel Guidance

When a team is near decision-making, the most important proof is not feature language. It is operational fit. A good Draftroom.works implementation should reduce:

- lost approvals
- review latency
- duplicate comments
- uncertainty about the latest version
- manual status copying into PM or campaign systems
