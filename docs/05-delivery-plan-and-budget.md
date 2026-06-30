# Delivery Plan and Development Budget

## 1. Delivery approach

The SBBC platform should be delivered as a staged product program, not as one giant build.

Recommended approach:

- Plan clearly in V0
- Launch public value in V1
- Build internal operations in V2
- Open teacher and student product surfaces in V3
- Expand into online learning in V4

## 2. Suggested development workflow

### Phase 0: discovery and specification

Deliverables:

- Product scope definition
- PRD
- Sitemap and module map
- Role and permission model
- Data model draft
- Technical architecture draft
- Cost estimate
- Delivery roadmap

### Phase 1: UX and design

Deliverables:

- Brand direction
- Page-level wireframes
- Core dashboard wireframes
- Design system tokens
- Responsive layout rules

### Phase 2: engineering setup

Deliverables:

- Repository and CI/CD
- Environments
- Database schema
- Auth and RBAC foundation
- Shared UI primitives

### Phase 3: implementation by version

Deliverables:

- V1 website and conversion
- V2 admin and CRM
- V3 teacher and student portal
- V4 online learning

### Phase 4: QA and go-live

Deliverables:

- Test plans
- UAT
- Production launch
- Monitoring and post-launch fixes

## 3. Effort estimate by version

These are planning-level estimates, not fixed quotes.

### V0

- Product planning and architecture
- Estimated effort: `1 to 2 weeks`

### V1

- Premium website, programs, content, forms, lead intake
- Estimated effort: `3 to 6 weeks`

### V2

- Admin dashboard, CRM, student records, lesson credits
- Estimated effort: `4 to 8 weeks`

### V3

- Teacher dashboard, student portal, finance basics, certificates
- Estimated effort: `4 to 8 weeks`

### V4

- Recorded courses, live classes, booking automation
- Estimated effort: `6 to 12 weeks`

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
- QA support part-time

Best for:

- Faster multi-module delivery

## 5. Development budget model

Below is a rough planning model in AUD.

### Option A: lean staged build

- V0 planning: `AUD 2,000 to 5,000`
- V1 build: `AUD 8,000 to 18,000`
- V2 build: `AUD 12,000 to 25,000`
- V3 build: `AUD 12,000 to 25,000`
- V4 build: `AUD 18,000 to 40,000`

Program total if all phases are completed:

- Roughly `AUD 52,000 to 113,000`

### Option B: stronger production-grade delivery

- V0 planning and architecture: `AUD 4,000 to 8,000`
- V1: `AUD 15,000 to 30,000`
- V2: `AUD 20,000 to 40,000`
- V3: `AUD 20,000 to 40,000`
- V4: `AUD 30,000 to 60,000`

Program total:

- Roughly `AUD 89,000 to 178,000`

## 6. Recommended budgeting logic

- Treat V0 as a planning investment
- Do not prepay for V3/V4 complexity before V1 proves conversion value
- Keep contracts and milestones version-based
- Re-estimate after each shipped version

## 7. Risks that affect cost

- Frequent product direction changes
- Late finance requirements
- Custom payment workflows
- Advanced LMS requirements
- Multi-language editorial complexity
- Migration from current site if code quality is inconsistent
- Building native live-class features too early

## 8. Suggested next deliverables after this repo

- Formal sitemap
- Role-permission matrix
- Database ERD
- User journeys
- V1 wireframes
- Content inventory from the current website
