# SBBC Platform Blueprint

This repository is the planning workspace for the SBBC platform.

SBBC is not only a marketing website. It is a staged software platform that will eventually include:

- Brand website and content hub
- Lead generation and consultation funnel
- CRM
- Admin and academic operations system
- Teacher workspace
- Student portal
- Enrollment and payment flow
- Finance and reporting
- Pre-recorded online courses
- Live classes

The goal of this repository is to keep product planning, architecture decisions, delivery phases, and budget assumptions in one place before full-scale development.

## Suggested reading order

1. [docs/01-product-prd.md](./docs/01-product-prd.md)
2. [docs/02-roadmap-v0-v4.md](./docs/02-roadmap-v0-v4.md)
3. [docs/03-architecture-and-portal-strategy.md](./docs/03-architecture-and-portal-strategy.md)
4. [docs/04-services-cost-estimate.md](./docs/04-services-cost-estimate.md)
5. [docs/05-delivery-plan-and-budget.md](./docs/05-delivery-plan-and-budget.md)

## Chinese versions

1. [docs/zh/01-产品需求文档.md](./docs/zh/01-%E4%BA%A7%E5%93%81%E9%9C%80%E6%B1%82%E6%96%87%E6%A1%A3.md)
2. [docs/zh/02-路线图-V0-V4.md](./docs/zh/02-%E8%B7%AF%E7%BA%BF%E5%9B%BE-V0-V4.md)
3. [docs/zh/03-架构与门户策略.md](./docs/zh/03-%E6%9E%B6%E6%9E%84%E4%B8%8E%E9%97%A8%E6%88%B7%E7%AD%96%E7%95%A5.md)
4. [docs/zh/04-技术栈服务与成本估算.md](./docs/zh/04-%E6%8A%80%E6%9C%AF%E6%A0%88%E6%9C%8D%E5%8A%A1%E4%B8%8E%E6%88%90%E6%9C%AC%E4%BC%B0%E7%AE%97.md)
5. [docs/zh/05-开发流程与预算.md](./docs/zh/05-%E5%BC%80%E5%8F%91%E6%B5%81%E7%A8%8B%E4%B8%8E%E9%A2%84%E7%AE%97.md)

## Current recommendation

At the beginning, build one platform with:

- One shared backend
- One shared database
- One codebase or monorepo
- Separate role-based experiences for public users, students, teachers, and admins

This gives strong isolation in permissions and user experience without creating unnecessary operational complexity too early.
