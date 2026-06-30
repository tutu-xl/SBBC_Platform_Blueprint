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

Teacher portal should be logically independent in UX, but not a completely separate technical system in V1-V3.

Recommendation:

- Separate navigation
- Separate page routes
- Separate permission scope
- Separate API guards
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

### Frontend

- Next.js
- TypeScript
- Tailwind CSS
- Component library built from a custom design system

### Backend

- Next.js server actions / route handlers for light workflows
- Supabase for Postgres, auth, storage, and realtime
- Background jobs via Inngest or Trigger.dev if workflow complexity grows

### Content

- Use the application database for courses and structured CMS data
- Optionally use MDX or a headless CMS later if editorial workflow becomes more complex

### Payments

- Stripe for card payments and subscriptions
- Optional second payment path later if Chinese payment channels become necessary

### Email

- Resend for transactional email

### Video and live classes

Two recommended paths:

- Lean path: use third-party live class links first, protected inside portal
- Platform path: introduce managed video/live infra in V4

### Hosting

- Vercel for app hosting
- Cloudflare for DNS, CDN, and WAF layer

## 7. Domain model to stabilize early

The following entities should be designed carefully in V0/V1 because they affect every later phase:

- User
- Role
- Student
- Parent / guardian
- Teacher
- Lead
- Program / course
- Enrollment / order
- Lesson package
- Lesson session
- Attendance
- Feedback
- Payment
- Invoice / receipt
- Video asset
- Certificate

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
- `packages/config` for shared config
- `packages/types` for shared types

This is optional in V1. A single well-structured app repository is also acceptable if the team is small.
