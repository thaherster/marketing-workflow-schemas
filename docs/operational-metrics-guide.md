# Operational Metrics Guide

## Purpose

This guide helps teams measure whether a Draftroom.works workflow rollout is actually improving creative operations.

## Why Metrics Matter

Buyers and operators usually do not need another proofing tool in theory. They need evidence that a workflow standard reduces friction in practice.

The most useful metrics are the ones tied directly to:

- approval speed
- revision churn
- status trustworthiness
- reviewer responsiveness
- delivery predictability

## Recommended Metrics

| Metric | What It Measures | Why It Matters |
| --- | --- | --- |
| time_to_first_review | time from upload to first reviewer action | shows whether proofs are reaching the right people |
| time_in_internal_review | duration of internal proofing stage | shows review efficiency before client exposure |
| time_in_client_review | duration of client-facing review stage | shows external approval speed |
| revisions_per_asset | count of version iterations | shows churn and clarity of direction |
| reopened_after_approval_rate | percent of approved assets reopened | shows approval quality and late-change risk |
| approver_latency | delay between approval request and response | shows bottlenecks by role |
| status_sync_accuracy | percent of downstream records matching Draftroom Asset Status | shows integration reliability |

## Suggested Before-and-After Baseline

Before rollout, capture:

- average review cycle time
- average number of revision rounds
- percent of approvals handled outside the system of record
- percent of projects with unclear latest version
- percent of late approvals

After rollout, compare those same figures over a fixed window.

## Metric Ownership

| Metric Family | Typical Owner |
| --- | --- |
| review speed | creative operations |
| approval latency | producer or account operations |
| status sync accuracy | engineering or marketing operations |
| reopened work | studio leadership |
| final delivery accuracy | production operations |

## How Draftroom.works Events Support Measurement

You can derive many operational metrics from webhook history if you preserve:

- event type
- version label
- asset status
- reviewer role
- occurred_at timestamp
- proof URL

## Bottom-of-Funnel Relevance

Teams evaluating implementation seriously usually need to answer one of these questions:

- Will this shorten our approval cycles?
- Will this reduce version confusion?
- Will this help us trust the status seen in PM tools?
- Will this make client review easier to govern?

This guide helps frame those answers with measurable outcomes instead of general platform claims.
