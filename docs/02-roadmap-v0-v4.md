# SBBC Roadmap: V0 to V4

## Planning principle

SBBC should be delivered in phases. The current public website is already close to a usable first-generation brand site, so the next versions should build on that base rather than restart from zero.

Core principles:

- Clarify direction and architecture first
- Prioritize the parts that create the most business value
- Let each version prepare the foundation for the next version

## V0: Foundation and planning

Goal:

- Clarify platform boundaries, version roadmap, technical approach, and budget model

Includes:

- Product requirements clarification
- Information architecture
- Core business flows
- Core data model draft
- Tech stack decision
- Service and budget estimate
- Delivery plan

Output:

- Project planning documentation library
- Product requirements document
- Initial architecture document
- Phased implementation plan

## V1: Current website refinement + payment + basic portals

Goal:

- Build on the current website and make the first operational version truly usable

Includes:

- Keep and refine the existing public website
- Improve consultation and trial booking flow where needed
- Add online payment for enrollment
- Support the current core teaching model: one-to-one and small-group live classes
- Use third-party live class links such as Zoom or Tencent Meeting in the early stage
- Basic student portal
- Basic teacher portal
- Basic teaching assistant / operations support workspace
- Basic admin backend
- Student profile and enrollment records
- Lesson package / remaining credit tracking
- Basic teacher-student assignment
- Basic teaching assistant assignment to students or consultation records
- Basic order and payment records

Must-have outcomes:

- The public website stays usable and credible
- Students can enroll and pay
- Admins can manage core records
- Teachers, students, and teaching assistants can start using their own workspaces
- Teaching assistants can support basic consultation follow-up, student information review, and operations tasks

## V1 explicit exclusions

The following capabilities are intentionally not included in V1:

- Recorded course library
- Platform-owned live video infrastructure
- `SBBC Store` checkout, inventory, fulfillment, and after-sales operations inside the SBBC main platform
- Main-site merchandise showcase and `SBBC Store` referral flow
- Student points account and earning history
- Points redemption or merchandise exchange flow
- Parent portal
- Advanced finance reporting
- Advanced automation and workflow approvals
- Native mobile app
- Multi-campus or multi-brand support
- Complex referral or commission system

## V2: Customer Relationship Management (CRM) + academic operations + scheduling

Goal:

- Move daily academic operations and customer follow-up into a structured system

Includes:

- Customer Relationship Management (CRM) pipeline for consultation customers
- Customer service / consultant workflow
- Student profiles
- Teacher profiles
- Teaching Assistant (TA) support workflow
- Course and package management
- Lesson records
- Credit deduction / restoration
- Scheduling support
- Leave / makeup / cancellation handling
- Notes and follow-up history
- Basic notifications
- Student points account
- Points earning rules and earning history
- Points can be earned from course enrollment, classroom performance, competition results, and other sources; different sources may use different point rules
- Points are visible in the student portal, but redemption is not included yet

Must-have outcomes:

- Centralized management of students, teachers, TAs, and consultation customers
- Better scheduling and academic coordination
- Reduced admin and teaching support friction
- Students can see points earned from courses and learning-related activities

## V3: Comprehensive BI Dashboards + finance + workflow approvals

Goal:

- Transform operational data into strategic insights with deep BI dashboards

Includes:

- Core Team BI Dashboard: Comprehensive student, teacher, marketing, and learning analytics
- Marketing attribution tracking (Google, Meta, Xiaohongshu, etc.)
- Website performance and conversion funnel analytics
- Role-specific dashboards (Academic ops, Finance, Founder)
- Cultural events performance and ROI tracking
- Expense reimbursement and OA-style approval flows
- Invoice / receipt management
- Automated certificate generation
- Main-site merchandise showcase and `SBBC Store` referral design
- Clear merchandise entry points, link placement, and referral rules
- Evaluate whether future voucher or redemption-code handoff to the independent `SBBC Store` is needed
- Advanced reporting widgets using modern visualization libraries (e.g., Tremor)

Must-have outcomes:

- Data-driven decision making for leadership (LTV, CAC, Churn)
- Clear ROI on marketing and cultural events
- Streamlined approvals and finance visibility
- SBBC can show merchandise on the main site while keeping purchasing on the independent store website

## V4: Online learning expansion

Goal:

- Extend SBBC from live teaching operations into online learning products when the business is ready

Includes:

- Recorded course library
- Video hosting and access control
- Progress tracking
- Learning completion markers
- Optional quizzes or checkpoints later
- Continued use of third-party live class links such as Zoom or Tencent Meeting

Must-have outcomes:

- SBBC can launch structured recorded programs when ready
- Online learning becomes a real second growth path

## V5 and later

Potential future scope:

- Advanced finance reporting
- Commission or referral system
- Advanced analytics
- AI-assisted study support
- Multi-campus or multi-brand support
- Native mobile app
- Deeper `SBBC Store` integration if needed, such as points redemption rules or voucher handoff

## Recommended sequencing notes

- V1 should focus on making the current business flow work end-to-end
- V1 does not need recorded courses
- V1 should support the current teaching model: one-to-one and small-group live classes
- V2 should establish the operational model for customer service, TAs, scheduling, and teaching support
- V2 can add the student points account and earning history, but should not include redemption yet
- V3 can define the main-site merchandise showcase and referral flow to the independent `SBBC Store`
- The SBBC main platform should not handle store checkout, inventory, fulfillment, or after-sales operations
- V3 should not be built before Role-Based Access Control (RBAC), student, course, lesson, and payment models are stable
- V4 should start only when SBBC is truly ready to invest in recorded-course operations
