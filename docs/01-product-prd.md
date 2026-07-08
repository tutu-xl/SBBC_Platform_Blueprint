# SBBC Product Requirements Document (PRD)

This document defines WHAT the platform does. For WHEN each capability ships, see [02-roadmap-v0-v4.md](./02-roadmap-v0-v4.md). For HOW it is built, see [03-architecture-and-portal-strategy.md](./03-architecture-and-portal-strategy.md).

## 1. Product definition

SBBC should be planned as a platform, not only as a website.

The platform scope can be grouped into the following areas:

**Public brand, content, and acquisition**

- Public-facing brand website
- Content Management System (CMS) with native Search Engine Optimization (SEO) support
- Consultation and trial-lesson conversion flow
- Merchandise showcase on the main site, with purchase handled by a separate `SBBC Store`

**Enrollment and conversion**

- Customer Relationship Management (CRM) for consultation lead / prospect record management
- Trial booking and follow-up workflow
- Student enrollment and payment

**Teaching and daily operations**

- Admin backend
- Academic operations
- Teacher workspace
- Student portal
- Parent / guardian portal

**Data, finance, and management reporting**

- Financial records and reporting
- Business Intelligence (BI) dashboards and management analytics

**Future learning capability expansion**

- Pre-recorded learning capability
- Live online learning capability

## 2. Product goals

### Business goals

- Build a premium bilingual brand presence
- Improve consultation-to-enrollment conversion
- Standardize student and lesson management
- Reduce manual work in scheduling, follow-up, and progress tracking
- Create a scalable foundation for online programs and hybrid delivery

### Product goals

- Make the public website excellent for brand, trust, and conversion
- Make the internal system practical for daily operations
- Let students manage learning and payments in one place
- Let teachers complete teaching tasks with minimal friction
- Preserve room for later finance, Learning Management System (LMS), and automation features

## 3. Core user roles

- Visitor: reads content, browses programs, submits consultation or trial request
- Student: enrolled learner who can log into the student portal to view courses, lesson credits, timetable, feedback, payment status, learning materials, and points; the student portal should distinguish adult and underage students. Adult students can enroll, pay, and manage orders and invoices themselves. Underage students can start enrollment / select courses, but cannot complete payment; payment, confirmation, and terms acceptance must be completed by a parent or guardian
- Parent: parent or guardian of an underage student, responsible for paying for the student's enrolled courses, accepting terms and privacy policies, handling billing and notifications, and supervising learning progress
- Teacher: sees only assigned students, classes, and feedback tasks
- Teaching assistant (TA): operational support with limited access, including assigned consultation lead follow-up
- Admin: manages students, lessons, CRM, and content
- Super admin: manages platform settings, permissions, finance rules, and audit logs

Note: a "Lead" means a consultation lead / prospect record in CRM, not a login role.

## 4. Core domains

### 4.1 Public website and brand

- Home
- Programs and program detail pages
- Learning hub / articles / news
- About SBBC and faculty team
- Consultation and trial booking
- Contact / WeChat / social links
- Merchandise showcase and `SBBC Store` referral entry
- The main SBBC site only showcases and refers; product checkout, inventory, and fulfillment stay outside the main platform

### 4.2 CRM and conversion

- Consultation lead / prospect record inbox
- Source tracking
- Consultation records
- Trial booking workflow
- Follow-up status pipeline
- Enrollment conversion tracking
- Teaching assistant / operations assignment for follow-up

### 4.3 Student management

- Student profile
- Contact and guardian info
- Course and package info
- Lesson consumption
- Attendance
- Homework and feedback
- Exam readiness and scores
- Certificates

### 4.4 Lesson and scheduling

- Teacher schedule
- Student bookings
- Trial lesson slots
- Completed / booked / cancelled / leave / makeup statuses
- Lesson credit deduction and restoration

### 4.5 Teacher workspace

- My students
- Today's lessons
- Submit lesson feedback
- Attendance
- Homework and next lesson plan

### 4.6 Student portal

- My courses
- Remaining credits
- My timetable
- Lesson history
- Teacher feedback
- Homework
- Billing and invoices
- Recorded courses
- Live course access
- Points balance and earning history
- Adult students can enroll, pay, and manage orders and invoices themselves
- Underage students can start enrollment / select courses, but cannot complete payment
- Payment, confirmation, and terms acceptance for underage students must be completed by a parent or guardian

### 4.7 Parent / guardian portal

- Complete payment for underage students' course enrollment
- Accept the terms of service, privacy policy, and minor-related confirmations
- View the student's timetable, lesson credits, feedback, and learning progress
- Receive payment, renewal, absence, and makeup-lesson notifications
- Handle refunds, invoices, and billing
- Supervise the student's learning progress

### 4.8 Public content CMS (SEO-native)

- Article and program editor
- Search Engine Optimization (SEO) fields per page
- URL slug management
- Cover images and media management
- Program highlights
- Reading analytics

### 4.9 Finance

- Payment records
- Enrollment orders
- Invoices / receipts
- Refunds / adjustments
- Revenue dashboard
- Outstanding balances

### 4.10 Online learning

- Pre-recorded lessons
- Video progress tracking
- Live class join links
- Session replay or recording access
- Learning completion milestones

### 4.11 Points and merchandise showcase

- Because a school entity may not be the right operating body for merchandise sales, `SBBC Store` should be considered as a separate website or separate company for merchandise sales
- The SBBC main site only provides merchandise showcase and referral entry points, and does not directly handle merchandise checkout, inventory, shipping, or after-sales support
- When users click a merchandise entry, they are redirected to the independent `SBBC Store` to complete the purchase
- Student points account
- Point earning rules and earning history
- Points can be earned from course enrollment, classroom performance, competition results, and other sources; different sources may use different point rules
- Points are recorded in the student portal first; redemption ships in a later version
- Future versions can define how points connect with `SBBC Store`, such as vouchers, redemption codes, or other redemption flows

## 5. Functional requirements

### 5.1 Public site requirements

- Strong premium positioning and trust-building
- Mobile-friendly Chinese and English presentation
- Clear Call to Action (CTA) for consultation and trial booking
- Program tagging and filtering
- Search-engine-friendly article and program pages

### 5.2 CRM requirements

- Consultation lead sources: website, WeChat, Xiaohongshu, WeChat Official Account, manual import
- Consultation lead statuses: new, contacted, trial booked, trial completed, enrolled, lost
- Notes and follow-up history
- Owner assignment, including Teaching Assistant (TA) or operations staff where appropriate
- Latest activity tracking

### 5.3 Student profile requirements

- Chinese name
- English name
- Email
- Phone
- WeChat
- Parent contact if minor
- Current course
- Remaining credits
- Course start and end date
- Assigned teacher and Teaching Assistant (TA)
- Attendance log
- Feedback log
- Homework log
- HSK/BCT records
- Mock test records

### 5.4 Lesson management requirements

- Calendar-based lesson records
- Lesson states: booked, completed, cancelled, leave, makeup
- Credit deduction and correction
- Trial lesson booking
- Teacher availability slots
- Student booking request form
- Email notifications for admins, teachers, and students

### 5.5 Teacher workspace requirements

- Restricted visibility to assigned students only
- Daily lesson agenda
- Post-class feedback form
- Attendance marking
- Homework and next-step planning

### 5.6 Student portal requirements

- Secure login
- Enrollment status and active programs
- Remaining lesson credits
- Learning history
- Feedback history
- Payment and invoice records
- Download certificates
- Watch recorded lessons
- Join live classes
- View points balance and earning history
- Adult students can enroll, pay, and manage orders and invoices themselves
- Underage students can start enrollment / select courses, but cannot complete payment
- Payment, confirmation, and terms acceptance for underage students must be completed by a parent or guardian

### 5.7 Parent / guardian portal requirements

- Complete payment for underage students' course enrollment
- Accept the terms of service, privacy policy, and minor-related confirmations
- View the student's timetable, lesson credits, feedback, and learning progress
- Receive payment, renewal, absence, and makeup-lesson notifications
- Handle refunds, invoices, and billing
- Supervise the student's learning progress

### 5.8 Admin dashboard requirements

- View monthly new students, active students, and enrolled students
- View latest inquiries, trial bookings, and enrollment conversion status
- View course, lesson, scheduling, and teacher work summaries
- View basic revenue, order, and payment records
- View content, website traffic, and event data summaries
- Expand into deeper Business Intelligence (BI) dashboards in later versions, as defined in the roadmap

### 5.9 Course management requirements

- Course title
- Tags: HSK, Business Chinese, VIP, Executive, Children
- Cover image
- Pricing
- Credit count
- Featured course toggle
- Program description
- Delivery mode: in-person, online live, recorded, hybrid

### 5.10 Content requirements (SEO-native)

- Meta title
- Meta description
- URL slug management
- Author
- Category
- Views
- Image alt text
- Structured data (Schema.org)
- Bilingual page mapping

### 5.11 Certificate requirements

- Generate certificate from completed course status
- Student name
- Course name
- Completion date
- SBBC logo

## 6. Non-functional requirements

- Role-based access control
- Audit logs for sensitive operations
- Secure auth and password reset
- Data backup and recovery
- Good performance on mobile
- Clean admin UX for Chinese-speaking operators
- Scalable architecture for future Learning Management System (LMS) and finance modules

## 7. Scope phasing

This PRD describes the full platform scope. Which capabilities ship in which version — and what is explicitly excluded from V1 — is maintained in [02-roadmap-v0-v4.md](./02-roadmap-v0-v4.md) only, to avoid duplicated and conflicting scope lists.

## 8. Portal and architecture decisions

Whether teacher/student portals are separate systems, the URL structure, and the shared-backend rationale are architecture decisions, maintained in [03-architecture-and-portal-strategy.md](./03-architecture-and-portal-strategy.md).

## 9. Open questions

All pending product decisions (payment gateways, parent accounts, live-class hosting, etc.) are tracked in [06-open-questions.md](./06-open-questions.md).
