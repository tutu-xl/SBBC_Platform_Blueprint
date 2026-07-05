# Delivery Plan and Development Budget

## 1. Delivery approach

The SBBC platform should be delivered as a staged product program, not as one giant build.

Recommended approach:

- Plan clearly in V0
- Launch public value in V1
- Build internal operations in V2
- Expand BI, finance, approvals, and management dashboards in V3
- Expand into online learning in V4

## 2. Suggested development workflow

### Phase 0: discovery and specification

Deliverables:

- Product scope definition
- PRD (Product Requirements Document)
- Sitemap and module map
- Role and permission model
- Data model draft
- Technical architecture draft
- Cost estimate
- Delivery roadmap

### Phase 1: UX (User Experience) and design

Deliverables:

- Brand direction
- Page-level wireframes
- Core dashboard wireframes
- Design system tokens
- Responsive layout rules

### Phase 2: engineering setup

Deliverables:

- Repository and CI/CD (Continuous Integration / Continuous Delivery)
- Environments
- Database schema
- Auth and RBAC (Role-Based Access Control) foundation
- Shared UI primitives

### Phase 3: implementation by version

Deliverables:

- V1 website and conversion
- V2 admin and CRM (Customer Relationship Management)
- V3 BI dashboards, finance basics, approvals, and management reporting
- V4 online learning

### Phase 4: QA (Quality Assurance) and go-live

Deliverables:

- Test plans
- UAT (User Acceptance Testing)
- Production launch
- Monitoring and post-launch fixes

## 3. Effort estimate by version

These are planning-level estimates, not fixed quotes.

Compared with the earlier rough estimate, the timelines below are intentionally extended to around 2x to 3x the original range. This is more realistic for a real product with revisions, Quality Assurance (QA), stakeholder feedback, permissions, and production hardening.

### V0

- Product planning and architecture
- Estimated effort: `2 to 4 weeks`

### V1

- Current website refinement, payment, basic admin backend, student portal, teacher portal, basic teaching assistant / operations support workspace
- Estimated effort: `6 to 15 weeks`

### V2

- CRM, customer service workflow, student records, course packages, lesson credits, scheduling support
- Estimated effort: `8 to 20 weeks`

### V3

- Department dashboards, finance basics, approvals, reporting, certificates
- Estimated effort: `8 to 20 weeks`

### V4

- Recorded courses, progress tracking, online learning expansion
- Estimated effort: `12 to 30 weeks`

## 4. Development team shapes

### Lean team

- 1 product/technical lead
- 1 full-stack engineer
- 1 designer part-time

Best for:

- Slower but controlled staged build

### Balanced team

- 1 product lead
- 1 designer
- 2 engineers
- Quality Assurance (QA) support part-time

Best for:

- Faster multi-module delivery

## 5. Development budget model

Below is a rough planning model in AUD.

These figures are framed in two layers:

- Market reference price: a reasonable current-market custom software delivery range
- Suggested discounted price: roughly 70% of the market reference range

This is intended as a practical commercial positioning model rather than a fixed quote.

### Market reference price

#### Lean staged build

- V0 planning: `AUD 4,000 to 8,000`
- V1 build: `AUD 18,000 to 35,000`
- V2 build: `AUD 25,000 to 50,000`
- V3 build: `AUD 25,000 to 50,000`
- V4 build: `AUD 40,000 to 80,000`

Program total if all phases are completed:

- Roughly `AUD 112,000 to 223,000`

#### Stronger production-grade delivery

- V0 planning and architecture: `AUD 6,000 to 12,000`
- V1: `AUD 28,000 to 55,000`
- V2: `AUD 40,000 to 75,000`
- V3: `AUD 40,000 to 75,000`
- V4: `AUD 60,000 to 120,000`

Program total:

- Roughly `AUD 174,000 to 337,000`

### Suggested discounted price at about 70%

#### Lean staged build

- V0 planning: `AUD 2,800 to 5,600`
- V1 build: `AUD 12,600 to 24,500`
- V2 build: `AUD 17,500 to 35,000`
- V3 build: `AUD 17,500 to 35,000`
- V4 build: `AUD 28,000 to 56,000`

Program total if all phases are completed:

- Roughly `AUD 78,400 to 156,100`

#### Stronger production-grade delivery

- V0 planning and architecture: `AUD 4,200 to 8,400`
- V1: `AUD 19,600 to 38,500`
- V2: `AUD 28,000 to 52,500`
- V3: `AUD 28,000 to 52,500`
- V4: `AUD 42,000 to 84,000`

Program total:

- Roughly `AUD 121,800 to 235,900`

## 5.1 Pricing rationale

The ranges above are informed by current public Australia market references and then translated into project pricing.

Reference signals used:

- SEEK reports Software Engineer salaries in Australia at about `AUD 105,000 to 125,000` on average
- SEEK reports Web Developer salaries in Australia at about `AUD 80,000 to 100,000`
- PayScale reports an average Software Developer salary in Australia around `AUD 79,830`

How this translates into project pricing:

- A project is not priced at salary only
- Real delivery cost includes design, meetings, revisions, Quality Assurance (QA), deployment, project coordination, and business risk
- Agencies and consultants usually price significantly above raw salary-equivalent time

So the project budget above is positioned as a realistic custom-build market range, and the discounted range represents a founder-friendly or relationship-based offer at about 70% of that level

## 6. Recommended budgeting logic

- Treat V0 as a planning investment
- Do not prepay for V3/V4 complexity before V1 proves conversion value
- Keep contracts and milestones version-based
- Re-estimate after each shipped version

## 7. Risks that affect cost

- Frequent product direction changes
- Late finance requirements
- Custom payment workflows
- Advanced Learning Management System (LMS) requirements
- Multi-language editorial complexity
- Migration from current site if code quality is inconsistent
- Building native live-class features too early

## 8. Suggested next deliverables after this repo

- Formal sitemap
- Role-permission matrix
- Database Entity Relationship Diagram (ERD)
- User journeys
- V1 wireframes
- Content inventory from the current website

## Sources

- [SEEK Software Engineer salary](https://au.seek.com/career-advice/role/software-engineer/salary)
- [PayScale Software Developer salary in Australia](https://www.payscale.com/research/AU/Job=Software_Developer/Salary)
