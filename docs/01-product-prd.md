# SBBC Product PRD

## 1. Product definition

SBBC should be planned as a platform, not only as a website.

The platform will cover:

- Public-facing brand website
- Content and SEO system
- Consultation and trial-lesson conversion flow
- CRM for lead management
- Student enrollment and payment
- Admin dashboard and academic operations
- Teacher dashboard
- Student portal
- Financial records and reporting
- Online learning delivery for pre-recorded and live courses

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
- Preserve room for later finance, LMS, and automation features

## 3. Core user roles

- Visitor: reads content, browses programs, submits consultation or trial request
- Lead: has submitted a form and entered CRM
- Student: enrolled learner with portal access
- Parent: associated contact for minors
- Teacher: sees only assigned students, classes, and feedback tasks
- Teaching assistant: operational support with limited access
- Admin: manages students, lessons, CRM, and content
- Super admin: manages platform settings, permissions, finance rules, and audit logs

## 4. Core domains

### 4.1 Public website

- Home
- Programs
- Program detail pages
- Learning hub / articles
- About SBBC
- Faculty / teaching team
- Consultation booking
- Trial lesson booking
- Contact / WeChat / social links

### 4.2 CRM and conversion

- Leads inbox
- Source tracking
- Consultation records
- Trial booking workflow
- Follow-up status pipeline
- Enrollment conversion tracking

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
- Trial status or enrollment status
- Recorded courses
- Live course access

### 4.7 Content and CMS

- Article editor
- SEO fields
- Slug management
- Cover images
- Program highlights
- Reading analytics

### 4.8 Finance

- Payment records
- Enrollment orders
- Invoices / receipts
- Refunds / adjustments
- Revenue dashboard
- Outstanding balances

### 4.9 Online learning

- Pre-recorded lessons
- Video progress tracking
- Live class join links
- Session replay or recording access
- Learning completion milestones

## 5. Functional requirements

### 5.1 Public site requirements

- Strong premium positioning and trust-building
- Mobile-friendly Chinese and English presentation
- Clear CTA for consultation and trial booking
- Program tagging and filtering
- Search-engine-friendly article and program pages

### 5.2 CRM requirements

- Lead sources: website, WeChat, Xiaohongshu,公众号, manual import
- Lead statuses: new, contacted, trial booked, trial completed, enrolled, lost
- Notes and follow-up history
- Owner assignment
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
- Assigned teacher and TA
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
- Homework and class notes
- Download certificates
- Watch recorded lessons
- Join live classes
- View payment history

### 5.7 Admin dashboard requirements

- Monthly new students
- Active students
- Monthly revenue
- Monthly lessons
- Latest leads
- Content statistics

### 5.8 Course management requirements

- Course title
- Tags: HSK, Business Chinese, VIP, Executive, Children
- Cover image
- Pricing
- Credit count
- Featured course toggle
- Program description
- Delivery mode: in-person, online live, recorded, hybrid

### 5.9 Content requirements

- Meta title
- Meta description
- Slug
- Author
- Category
- Views

### 5.10 Certificate requirements

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
- Scalable architecture for future LMS and finance modules

## 7. Out of scope for the very first release

- Full accounting system
- Deep BI or custom data warehouse
- Enterprise multi-tenant support
- Complex affiliate / commission system
- Native mobile apps

## 8. Product decision: separate teacher and student portals or not?

Recommendation:

- Separate teacher and student experiences
- Shared platform backend
- Shared authentication service
- Shared database
- Different route groups or sub-apps

Recommended URL structure in the early stages:

- `www.sbbc.com.au` for public site
- `app.sbbc.com.au` for authenticated product
- `app.sbbc.com.au/student/*` for student portal
- `app.sbbc.com.au/teacher/*` for teacher workspace
- `app.sbbc.com.au/admin/*` for admin workspace

Reason:

- Better permission isolation than one mixed dashboard
- Cleaner UX for each role
- Easier to scale later
- Lower operational complexity than maintaining multiple independent systems

Not recommended for V0/V1:

- Completely separate products with separate backends
- Separate databases for student, teacher, and admin from day one

## 9. Open decisions to confirm later

- Payment gateway choice for Australia and Chinese users
- Whether parent accounts are first-class users
- Whether live classes are hosted inside the platform or linked from third-party tools
- Whether recorded courses require progress tracking and quizzes in V2 or later
