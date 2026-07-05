# Architecture and Portal Strategy

## 1. Recommended product structure

Recommendation:

- One platform
- One shared backend
- One shared database
- One authentication system
- One design system
- Multiple role-based frontends inside the same product ecosystem

This is the best trade-off between isolation and maintainability for SBBC at this stage.

## 2. Why not build fully separate systems now?

If teacher, student, admin, and public website are built as independent systems too early, the team will likely face:

- Duplicated authentication logic
- Duplicated user and permission models
- Duplicated deployment pipelines
- Higher maintenance cost
- Slower iteration across connected workflows
- More integration bugs around lessons, payments, and student state

## 3. Recommended topology

### Public layer

- `www.sbbc.com.au`
- marketing pages
- programs
- articles
- contact and consultation pages

### Authenticated application layer

- `app.sbbc.com.au`
- shared login
- role-based routing after login

### Role workspaces

- `app.sbbc.com.au/student/*`
- `app.sbbc.com.au/teacher/*`
- `app.sbbc.com.au/admin/*`

This keeps the user experience separated even when the codebase is shared.

## 4. Teacher portal recommendation

Teacher portal should be logically independent in User Experience (UX), but not a completely separate technical system in V1-V3.

Recommendation:

- Separate navigation
- Separate page routes
- Separate permission scope
- Separate Application Programming Interface (API) guards
- Shared backend and infra

Reason:

- Teachers and admins have very different tasks
- Teachers should not be exposed to admin complexity
- It is easier to secure a least-privilege model

## 5. Student portal recommendation

Student portal should also be a distinct role-based product area.

Recommendation:

- Different entry experience after login
- Strong separation from admin and teacher workflows
- Shared auth and backend

Student portal should eventually include:

- Enrolled courses
- Remaining credits
- Timetable
- Learning records
- Payments
- Recorded lessons
- Live lesson access

## 6. Suggested tech stack

This section describes the recommended direction only. It does not mean every tool must be adopted in the first phase. Early versions should prioritize mature, low-maintenance choices that leave room for later expansion.

### Frontend

- Use Next.js as the main framework so the public site, admin backend, teacher workspace, and student portal can share one technical foundation
- Use TypeScript to improve long-term maintainability and reduce regression risk
- Use Tailwind CSS and gradually build shared UI patterns for buttons, forms, tables, cards, and navigation
- Add an appropriate charting library during the BI dashboard phase for revenue, enrollment, course, and event analytics

### Backend

- Use Supabase as the baseline backend for database, authentication, file storage, and realtime capability
- Keep lightweight business logic in Next.js backend capabilities first, so the early architecture does not become too heavy
- Combine role permissions and database-level controls so students, teachers, TAs, and admins can only access the right data
- Do not introduce complex workflow tooling at the start; evaluate dedicated workflow tools later if automated reminders, approvals, sync, or retry flows become complex

### Analytics & Search Engine Optimization (SEO)

- Consider basic SEO from the first phase so program pages, article pages, and brand pages have clear titles, descriptions, and page structure
- Connect Google Search Console to monitor Google indexing, search keywords, and page performance
- Choose a website analytics tool as needed, such as Google Analytics 4, Umami, or PostHog, to understand traffic, sources, page performance, and key conversion actions
- Generate Sitemap and Robots.txt automatically so search engines can crawl the site correctly
- Manage page titles, descriptions, image alt text, and structured data consistently to improve search presentation

### Content

- Store courses, articles, and structured content in the application database first, so they can connect naturally with enrollment, course, and student data
- Consider a fuller Content Management System (CMS) later if editorial approval, multilingual publishing, or content operations become more complex

### Payments

- Prioritize online payment methods that fit Australian operations and support enrollment and course payment flows
- Evaluate a second payment path later if Chinese payment channels become necessary

### Email

- Email service is mainly used for registration, enrollment, payment, and class reminder emails
- The exact email provider can be selected based on cost, deliverability, and maintenance convenience

### Video and live classes

Two recommended paths:

- Lean path: use third-party live class links first, protected inside portal
- Platform path: introduce managed video/live infra in V4

### Hosting

- Vercel for app hosting
- Cloudflare for Domain Name System (DNS), Content Delivery Network (CDN), and Web Application Firewall (WAF) layer

## 7. Domain model to define early

The data model should stay aligned with the roadmap. V0/V1 does not need to implement every entity in full, but the core relationships should be designed early so later CRM, academic operations, finance, and recorded-learning modules do not require major rewrites.

### Must be stable in V0/V1

- User
- Role
- Student
- Teacher
- Teaching assistant
- Program / course
- Enrollment / order
- Lesson package
- Payment

### Reserve and expand in V2

- Parent / guardian: contact relationship first; whether this becomes a separate login role requires confirmation
- Consultation lead / prospect record: for CRM, trial booking, and enrollment follow-up
- Lesson session
- Attendance
- Feedback

### Expand in V3/V4

- Invoice / receipt: for finance basics
- Certificate: for automated certificate generation
- Video asset: for the recorded-learning phase

## 8. Security and permission model

Core principles:

- Role-based access control
- Row-level security for student and teacher data
- Audit logs for sensitive actions
- Clear separation between content editing and academic operations
- No teacher access to unrelated student financial data

## 9. Delivery architecture recommendation

Recommended repository direction:

- One monorepo or one well-structured main repository in the first stage

Suggested app structure:

- `apps/web` for public site and app shell
- `packages/ui` for shared components
- `packages/types` for shared types
- `packages/config` for shared config

This is optional in V1. A single well-structured app repository is also acceptable if the team is small.
