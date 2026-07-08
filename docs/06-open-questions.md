# Open Questions

This document collects decisions that still need confirmation.

It is intentionally separate from the PRD, roadmap, and architecture docs so we do not repeat scope, sequence, or system-design decisions in multiple places.

## 1. Payments and minors

- The payment method mix needs confirmation, including Australian local payment methods, card payments, and payment methods familiar to Chinese users.
- The student portal needs to distinguish adult and underage students: adult students can enroll, pay, and manage orders and invoices themselves; underage students can start enrollment / select courses, but payment, terms acceptance, privacy policy acceptance, and minor-related confirmations should be completed by a parent or guardian.

## 2. Parent accounts

- Parent / guardian accounts need to be included in the permission design and aligned with the student portal, payment flow, and notification permissions.
- The launch phase and boundaries of a full parent portal still need confirmation; early versions should at least support payment, confirmation, notifications, and learning supervision for underage students.
- Student and parent access boundaries need further page-level detail: the student side focuses on courses, timetable, lesson credits, feedback, learning materials, and points; the parent side focuses on payment, terms acceptance, notifications, refunds, invoices, billing, and learning supervision.

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
