# Open Questions

This document collects decisions that still need confirmation.

It is intentionally separate from the PRD, roadmap, and architecture docs so we do not repeat scope, sequence, or system-design decisions in multiple places.

## 1. Payments and minors

- The payment method mix needs confirmation, including Australian local payment methods, card payments, and payment methods familiar to Chinese users.
- Payment for underage students needs a separate flow decision: should a parent or guardian always pay or confirm, or can the student complete part of the process independently?

## 2. Parent accounts

- Whether parent accounts should be treated as a first-class role needs to be decided together with the student portal, payment flow, and notification permissions.
- Whether to build a dedicated parent portal needs separate confirmation and should not be assumed as a fixed later-phase scope.
- The split between student and parent access needs to be clear: what students can view, what parents can view, and which actions require parent confirmation.

## 3. Live and recorded learning

- V1 should support one-to-one and small-group live classes through third-party links such as Zoom or Tencent Meeting.
- Platform-owned live or video infrastructure should be evaluated later rather than assumed in V1.
- The launch phase for recorded courses needs confirmation. If recorded courses are moved to V2 / V3 or later, the platform should still consider whether to reserve progress tracking, quizzes, and learning completion records.

## 4. Data access and security

- Automation should be reserved architecturally, while the early versions should focus on core workflows first. Notifications, approvals, reminders, and rule-based automation can be added later.
- Logs can be considered in Supabase, but the system should distinguish ordinary logs from audit logs.
- Database and file backups should be considered early to reduce future data recovery risk.
- Sensitive data access must be permission-controlled, including who can view, edit, or export student and payment data.
- `Super Admin` should have access to system settings, permissions, logs, and critical operation records, but should not be treated as the same thing as a daily business admin.

## 5. Where to track other decisions

- Phase scope and V1 exclusions belong in [02-roadmap-v0-v4.md](./02-roadmap-v0-v4.md)
- Portal and backend structure belong in [03-architecture-and-portal-strategy.md](./03-architecture-and-portal-strategy.md)
