# Roles, Resources, Cost Plan, and RACI Matrix

**Course:** CIS 4374  
**Project:** Smart Parking Platform  
**Student:** Sarrthi Jasrotia

## 1. Project Scope and Planning Assumptions

The Smart Parking Platform helps drivers view parking availability, reserve a space, and manage their reservations. Parking administrators can update spaces and review parking activity. This plan covers requirements, design, development, testing, and deployment of a working prototype.

The planning period is three months (12 weeks). Each full-time resource has 480 available hours, based on 40 hours per week. Allocation percentages represent each person's average commitment across the entire project; work can be concentrated in particular phases. All staff names, skill levels, hourly rates, and costs are fictional planning assumptions. Labor is valued even if students perform the work without receiving payment.

Availability data will be simulated or entered by administrators. Physical parking sensors, gate equipment, production payment processing, and ongoing support after the prototype are outside this budget.

## 2. Roles and Resource Plan

| Role | Fictional Name | Assumed Skill Level and Responsibilities | Allocation | Estimated Hours | Hourly Rate | Cost |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| Project Manager / Business Analyst (PM) | Alex Morgan | Intermediate; manages scope, schedule, requirements, risks, and stakeholder communication | 20% | 96 | $40 | $3,840 |
| UX/UI Designer (UX) | Jamie Lee | Intermediate; designs user flows, wireframes, accessible screens, and prototypes | 15% | 72 | $35 | $2,520 |
| Frontend Developer (FE) | Taylor Brooks | Intermediate; builds parking search, availability views, reservation screens, and administrator interface | 50% | 240 | $40 | $9,600 |
| Backend Developer (BE) | Jordan Patel | Intermediate; builds database, APIs, authentication, reservation rules, and access controls | 50% | 240 | $45 | $10,800 |
| Quality Assurance Tester (QA) | Casey Rivera | Intermediate; prepares test cases, tests features and integration, and verifies fixes | 25% | 120 | $30 | $3,600 |
| DevOps Engineer (DO) | Riley Chen | Intermediate; configures environments, deployment, backups, and monitoring | 10% | 48 | $45 | $2,160 |
| Project Sponsor (SP) | Morgan Davis | Senior; approves scope, funding, changes, and final acceptance | 2.5% | 12 | $50 | $600 |
| **Total** | | | **172.5% (1.725 FTE)** | **828** | | **$33,120** |

**Calculations:** Estimated hours = 480 × allocation percentage. Labor cost = estimated hours × hourly rate. FTE means full-time equivalent. Each person has a separate role, so no person's allocation exceeds 100%.

## 3. Bottom-Up Resource and Cost Plan

This plan uses bottom-up estimating. Each role's hours are multiplied by its hourly rate, then infrastructure and tool costs are added. A 10% contingency reserve covers estimated uncertainty, such as additional debugging or testing.

| Item | Category | Quantity | Unit Cost | Duration | Total | Notes |
| --- | --- | --- | ---: | --- | ---: | --- |
| PM / Business Analyst | Labor | 96 hours | $40/hour | 3 months | $3,840 | Planning, requirements, and coordination |
| UX/UI Designer | Labor | 72 hours | $35/hour | 3 months | $2,520 | Flows, wireframes, and usability review |
| Frontend Developer | Labor | 240 hours | $40/hour | 3 months | $9,600 | Driver and administrator screens |
| Backend Developer | Labor | 240 hours | $45/hour | 3 months | $10,800 | APIs, database, and reservation logic |
| QA Tester | Labor | 120 hours | $30/hour | 3 months | $3,600 | Functional, integration, and regression tests |
| DevOps Engineer | Labor | 48 hours | $45/hour | 3 months | $2,160 | Environments and deployment |
| Project Sponsor | Labor | 12 hours | $50/hour | 3 months | $600 | Reviews and approvals |
| Cloud hosting and database | Infrastructure | 3 monthly subscriptions | $100/month | 3 months | $300 | Shared prototype hosting and database allowance |
| Domain registration | Infrastructure | 1 registration | $20 | One time | $20 | One-year registration allowance |
| Design and testing tools | Tools | 1 project allowance | $150 | One time | $150 | Optional paid tools; otherwise use free tiers |
| **Base Cost** | | | | | **$33,590** | Labor + infrastructure + tools |
| Contingency reserve | Reserve | 10% of base cost | 10% × $33,590 | Project period | $3,359 | Released only for approved needs |
| **Total Funding Requirement** | | | | | **$36,949** | Base cost + contingency |

The labor subtotal is $33,120. Nonlabor costs total $470. Therefore, the base cost is $33,590, and the total funding requirement is $36,949. This is a modeled project budget, not a claim about actual expenses already incurred.

## 4. Monthly Budgeted Cash Flow

Month 1 emphasizes planning and design. Month 2 emphasizes development and integration. Month 3 emphasizes testing, fixes, deployment, and handoff. Labor is assumed to be paid in the month worked; the domain and tool allowances are paid in Month 1.

| Cost Item | Month 1 | Month 2 | Month 3 | Total |
| --- | ---: | ---: | ---: | ---: |
| PM: 32 / 32 / 32 hours | $1,280 | $1,280 | $1,280 | $3,840 |
| UX: 48 / 16 / 8 hours | $1,680 | $560 | $280 | $2,520 |
| FE: 60 / 120 / 60 hours | $2,400 | $4,800 | $2,400 | $9,600 |
| BE: 60 / 120 / 60 hours | $2,700 | $5,400 | $2,700 | $10,800 |
| QA: 16 / 40 / 64 hours | $480 | $1,200 | $1,920 | $3,600 |
| DO: 16 / 8 / 24 hours | $720 | $360 | $1,080 | $2,160 |
| SP: 4 / 4 / 4 hours | $200 | $200 | $200 | $600 |
| Cloud hosting and database | $100 | $100 | $100 | $300 |
| Domain registration | $20 | $0 | $0 | $20 |
| Design and testing tools | $150 | $0 | $0 | $150 |
| **Planned Cash Outflow** | **$9,730** | **$13,900** | **$9,960** | **$33,590** |
| Contingency funding allowance | $973 | $1,390 | $996 | $3,359 |
| **Monthly Funding Allowance** | **$10,703** | **$15,290** | **$10,956** | **$36,949** |
| **Cumulative Funding Allowance** | **$10,703** | **$25,993** | **$36,949** | |

Contingency funding is available if needed and is not automatically spent. Month 2 requires the largest funding allowance because both developers devote the most hours to implementation. The monthly labor hours reconcile to the resource plan, and all monthly cost totals reconcile to the cost plan.

## 5. RACI Matrix

**R — Responsible:** Performs the work.  
**A — Accountable:** Owns the outcome and approves completion.  
**C — Consulted:** Provides input before a decision or completion.  
**I — Informed:** Receives progress or outcome updates.

Role abbreviations match the resource plan. Every activity has exactly one accountable role and at least one responsible role. A/R means the same role both performs and owns the activity.

| Activity / Deliverable | PM | UX | FE | BE | QA | DO | SP |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Approve project scope and budget | R | C | C | C | I | C | A |
| Gather requirements and define acceptance criteria | A/R | C | C | C | C | I | C |
| Maintain schedule, resources, and risk log | A/R | I | C | C | C | C | I |
| Design user flows and interface prototype | C | A/R | C | C | C | I | I |
| Design database and API contracts | C | C | C | A/R | C | C | I |
| Build driver parking search and availability views | I | C | A/R | R | C | I | I |
| Build reservation creation and cancellation | C | C | R | A/R | C | I | I |
| Implement authentication and role-based access | I | I | R | A/R | C | C | I |
| Build administrator parking management screens | C | C | A/R | R | C | I | I |
| Execute functional, integration, and regression tests | I | C | R | R | A/R | C | I |
| Conduct user acceptance testing and approve release | R | C | C | C | R | C | A |
| Configure hosting, backups, and deployment | I | I | C | R | C | A/R | I |
| Prepare user documentation and project handoff | A/R | C | R | R | C | R | I |
| Approve scope changes and contingency use | R | C | C | C | C | C | A |

The sponsor approves funding, major scope changes, and final acceptance. The project manager coordinates delivery and maintains the plan. Technical roles own their respective deliverables, while QA owns test execution and reports defects. Developers implement fixes and QA verifies them before release.
