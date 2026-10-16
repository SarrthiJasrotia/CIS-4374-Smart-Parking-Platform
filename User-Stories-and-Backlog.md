# User Stories, Product Backlog, and Sprints

**Course:** CIS 4374  
**Student:** Sarrthi Jasrotia  
**Reviewed:** October 15, 2026

## 1. Baseline and actual status

The [Trello board](https://trello.com/b/F7a0wRUi/smart-parking-platform) now contains all **68 planned tasks**: **20 in Sprint 1, 31 in Sprint 2, 15 in Sprint 3, and 2 in Sprint 4**.

PARK-01–PARK-58 were retained, and PARK-59–PARK-68 were added. Every card includes story references, estimates, dependencies, and acceptance criteria. The board matches the revised sprint plan. Implementation remains **unverified**, and no tasks have been marked complete.

Actual coursework ownership is Sarrthi Jasrotia. FE/BE/QA/DO/PM denote the fictional responsibility roles defined in the resource/RACI plan, not additional students. Every task has one lead role; support roles follow the RACI.

## 2. User stories and acceptance criteria

All stories are planned; acceptance is pending implementation and recorded tests. Story IDs retain the original use-case numbering for US-01–US-20; US-21–US-22 add cross-cutting release criteria.

| Story | User story | Requirement | WBS | Acceptance criteria |
|---|---|---|---|---|
| US-01 | As a driver, I want to create an account so that I can sign in with my own details. | FR-01 | 1.1.1 | Valid registration creates one account; missing/invalid fields and duplicate email are rejected; stored password is hashed, never plain text. |
| US-02 | As a user, I want to sign in, sign out, and recover access so that I can use protected features safely. | FR-02 | 1.1.1 | Valid credentials establish a session; invalid credentials fail; logout invalidates it; a seeded reset token expires/is single use; wrong-role requests fail on server. |
| US-03 | As a driver, I want to edit my profile so that I can keep my contact details current. | FR-01 | 1.1.2 | Owner can view/edit valid contact fields; invalid changes fail and a second driver cannot read or edit this profile. |
| US-04 | As a driver, I want to manage my vehicles so that I can attach the correct vehicle to a booking. | FR-01 | 1.1.2.2 | Owner can add/edit/remove a vehicle; required fields are validated; another driver cannot use or modify it. |
| US-05 | As a driver, I want to search and filter parking so that I can find a suitable location. | FR-03 | 1.2.1–1.2.2 | Destination/seeded coordinates return matching locations; price and distance filters narrow results; no matches shows an empty state; map/directions use the chosen location. |
| US-06 | As a driver, I want to filter by accessibility so that I can find designated parking. | FR-03, FR-05 | 1.2.1.3 | An accessibility filter returns only designated spaces/facilities and respects their time-range availability; tested against seeded mixed data. |
| US-07 | As a driver, I want to see availability for my requested time so that I can avoid reserving a taken space. | FR-04 | 1.2.3 | Available count excludes occupied/out-of-service and overlapping active reservations; back-to-back intervals are allowed; simulated label and timestamp appear; refresh follows changes. |
| US-08 | As a driver, I want to review facility details so that I can understand parking restrictions. | FR-05 | 1.2.3 | Rate, hours, location, restrictions and accessibility display from the same facility record; an unknown facility returns a useful not-found response. |
| US-09 | As a driver, I want to reserve a space for a valid interval so that I can have parking arranged before arrival. | FR-06 | 1.3.1 | Authenticated owner selects vehicle and valid time; server calculates total and confirms once; two simultaneous overlapping requests produce one booking; outside-hours/invalid intervals fail. |
| US-10 | As a driver, I want to try a simulated payment so that I can understand the payment flow. | FR-07, FR-14 | 1.5.1 | Mock success creates one synthetic paid record and receipt; mock failure creates no confirmed paid booking; retries do not duplicate records; no real card data is requested/stored. |
| US-11 | As a driver, I want to receive confirmation and reminders so that I can know my reservation details. | FR-09 | 1.3.1.3–1.3.3 | Successful booking shows ID, vehicle, facility, time, amount and digital demo pass; in-app reminders refer to the correct active booking; cancelled bookings receive no arrival reminder. |
| US-12 | As a driver, I want to open directions so that I can reach the selected facility. | FR-10 | 1.2.2.3 | Directions link encodes the selected seeded facility coordinates; navigation failure leaves facility address and reservation visible. |
| US-13 | As a driver, I want to modify or cancel my reservation so that I can change my parking plans. | FR-06 | 1.3.2 | Owner can change/cancel before arrival; modification rechecks conflicts atomically and preserves original booking on failure; repeated cancellation restores capacity only once; other users are rejected. |
| US-14 | As a driver, I want to review history and receipts so that I can track my demo parking activity. | FR-08 | 1.3.3, 1.5.2 | History, spending, receipt and downloadable history contain only the current driver’s records; cancelled/refunded entries display correct status and synthetic totals. |
| US-15 | As a driver, I want to see change and expiration notices so that I can stay informed. | FR-09 | 1.3.3.3 | In-app changed/cancelled/expiring states reference the affected booking and do not leak another driver’s data; no paid delivery service is required. |
| US-16 | As a operator, I want to manage my facilities and capacity so that I can keep parking records accurate. | FR-11 | 1.4.1–1.4.2, 1.4.4 | Authorized operator adds/edits assigned facilities, sees reservations and updates capacity/status; negative capacity or capacity below active commitments is rejected; driver requests fail. |
| US-17 | As a operator, I want to update rates and space status so that I can control booking availability and price. | FR-11 | 1.4.2–1.4.3 | Nonnegative rates apply to new quotes; existing bookings preserve their quoted rate; marking a space out of service blocks new overlapping bookings without erasing existing reservations. |
| US-18 | As a operator, I want to review and export activity reports so that I can understand facility use. | FR-12 | 1.6.1–1.6.2 | Date-filtered occupancy, counts, cancellations, mock revenue/refunds and average duration reconcile to seeded source records; CSV matches filters and operator facility permissions; empty periods show zero safely. |
| US-19 | As a administrator, I want to manage user roles and review activity so that I can control platform access. | FR-13 | 1.6.3 | Only admin can assign permitted roles or inspect audit events; driver/operator attempts fail; changes record actor, target, action and time without passwords or tokens. |
| US-20 | As a finance-authorized operator, I want to refund an eligible mock transaction so that I can correct a cancelled booking. | FR-07 | 1.5.3 | Eligible cancelled paid booking permits one mock refund up to paid amount; duplicate/excess/unauthorized refund fails; receipt and revenue totals reflect the change. |
| US-21 | As a user, I want to use a secure accessible interface so that I can complete core tasks across devices. | NFR-01–NFR-08 | 1.7.1–1.7.2 | Core flows pass recorded keyboard, viewport, browser, unauthorized-access, concurrency, error/retry, performance and backup/restore checks against the SRS targets. |
| US-22 | As a project owner, I want to receive a reproducible release package so that I can demonstrate and hand over the prototype. | NFR-08 | 1.7.3 | README setup/seed/test steps work on a clean environment; secrets excluded; deployment and restore steps plus user guide and test results are included. |

US-06 is also an acceptance checklist on PARK-13/15/39; US-12 on PARK-63; US-15 on PARK-61. These shared cases must pass even when the task’s primary story below differs. Reservations use half-open intervals [arrival, departure); cancellation/modification is eligible before arrival. Reports use the facility’s configured timezone and explicit selected dates. Occupancy means occupied spaces / usable capacity, not the number of future reservations. Revenue is synthetic paid amounts less successful mock refunds. Average duration uses checked-out visits only. These definitions prevent inconsistent UI/API/report calculations.

## 3. Definition of Ready and Done

**Ready:** requirement/story, acceptance checks, lead, estimate and dependencies are recorded; prerequisite contracts or components are available; scope fits the remaining capacity. A dependency may be a design contract for parallel development, but final acceptance requires integrated behavior.

**Done:** work is implemented, reviewed, and passes the story’s positive, negative, role/ownership and integration checks; evidence is linked to the commit/card, documents are updated, and no critical security/data-integrity defect remains. A document, elapsed date, or card move alone cannot mark a feature Done. In Progress and Blocked require an owner and next action. QA verifies fixes before closure.

## 4. Task register and revised sprint allocation

Points are new relative planning estimates (1 small, 2 ordinary, 3 multi-component, 5 complex); no historical velocity is assumed. They do not claim measured effort. H = required foundation/core/security; M = supporting prototype feature. Every task below is planned with completion unverified. Dependency IDs refer to PARK tasks.

| Task | Existing card title / new planned task | Story | Lead | Priority | Points | Revised sprint | Dependencies |  |
|---|---|---|---|---|---:|---|---|---|
| PARK-01 | Create user registration form | US-01 | FE | H | 2 | 1 | PARK-31 | Sprint 1 |
| PARK-02 | Validate required registration fields | US-01 | FE | H | 1 | 1 | PARK-01 | Sprint 1 |
| PARK-03 | Reject duplicate email addresses | US-01 | FE | H | 1 | 1 | PARK-31, PARK-34 | Product Backlog |
| PARK-04 | Store password securely | US-01 | FE | H | 2 | 1 | PARK-31 | Sprint 1 |
| PARK-05 | Create user sign-in form | US-02 | FE | H | 2 | 1 | PARK-35 | Sprint 1 |
| PARK-06 | Verify credentials and show sign-in errors | US-02 | FE | H | 2 | 1 | PARK-35 | Product Backlog |
| PARK-07 | Keep user signed in across page reloads | US-02 | FE | M | 2 | 2 | PARK-35 | Product Backlog |
| PARK-08 | Add sign-out action | US-02 | FE | H | 1 | 1 | PARK-35 | Product Backlog |
| PARK-09 | Restrict operator pages to operator accounts | US-02 | FE | H | 2 | 1 | PARK-36 | Product Backlog |
| PARK-10 | Add password reset request | US-02 | FE | M | 2 | 2 | PARK-31 | Product Backlog |
| PARK-11 | Show available parking locations to drivers | US-05 | FE | H | 2 | 1 | PARK-37 | Sprint 1 |
| PARK-12 | Display current available space count | US-07 | FE | H | 2 | 1 | PARK-32, PARK-37 | Sprint 1 |
| PARK-13 | Filter locations by distance | US-05 | FE | M | 2 | 2 | PARK-37 | Product Backlog |
| PARK-14 | Filter locations by price | US-05 | FE | M | 1 | 2 | PARK-37 | Product Backlog |
| PARK-15 | Show location details and operating hours | US-08 | FE | M | 2 | 2 | PARK-38 | Product Backlog |
| PARK-16 | Select arrival and departure times | US-09 | FE | H | 2 | 2 | PARK-15 | Product Backlog |
| PARK-17 | Show estimated parking cost | US-09 | FE | M | 2 | 2 | PARK-16, PARK-66 | Product Backlog |
| PARK-18 | Confirm a reservation | US-09 | FE | H | 2 | 2 | PARK-16, PARK-17, PARK-41, PARK-59 | Product Backlog |
| PARK-19 | Display active reservation details | US-14 | FE | M | 1 | 2 | PARK-41 | Product Backlog |
| PARK-20 | Show reservation history | US-14 | FE | M | 2 | 3 | PARK-41 | Product Backlog |
| PARK-21 | Cancel an eligible reservation | US-13 | FE | H | 2 | 2 | PARK-42 | Product Backlog |
| PARK-22 | Show driver profile | US-03 | FE | M | 1 | 2 | PARK-36 | Product Backlog |
| PARK-23 | Edit driver contact information | US-03 | FE | M | 2 | 2 | PARK-22, PARK-45 | Product Backlog |
| PARK-24 | Create operator dashboard | US-16 | FE | H | 2 | 1 | PARK-36 | Sprint 1 |
| PARK-25 | Show occupancy by parking location | US-16 | FE | H | 2 | 1 | PARK-32, PARK-37 | Sprint 1 |
| PARK-26 | Let operator add a parking location | US-16 | FE | M | 2 | 2 | PARK-43 | Product Backlog |
| PARK-27 | Let operator edit location details | US-16 | FE | M | 2 | 2 | PARK-43 | Product Backlog |
| PARK-28 | Let operator update capacity | US-16 | FE | M | 2 | 2 | PARK-43 | Product Backlog |
| PARK-29 | Let operator view reservations | US-16 | FE | M | 2 | 2 | PARK-41 | Product Backlog |
| PARK-30 | Make core screens usable on mobile | US-21 | FE | M | 2 | 2 | PARK-11, PARK-18, PARK-24 | Product Backlog |
| PARK-31 | Design users and roles data model | US-01 | BE | H | 3 | 1 | T2 design gate | Sprint 1 |
| PARK-32 | Design parking locations and spaces data model | US-07 | BE | H | 3 | 1 | T2 design gate | Sprint 1 |
| PARK-33 | Design reservations data model | US-09 | BE | H | 3 | 1 | PARK-31, PARK-32 | Sprint 1 |
| PARK-34 | Implement registration endpoint | US-01 | BE | H | 2 | 1 | PARK-31, PARK-04, PARK-02 | Sprint 1 |
| PARK-35 | Implement sign-in endpoint | US-02 | BE | H | 2 | 1 | PARK-31, PARK-04 | Sprint 1 |
| PARK-36 | Protect authenticated endpoints | US-02 | BE | H | 3 | 1 | PARK-35 | Sprint 1 |
| PARK-37 | Implement location list endpoint | US-05 | BE | H | 2 | 1 | PARK-32 | Sprint 1 |
| PARK-38 | Implement location detail endpoint | US-08 | BE | M | 2 | 2 | PARK-37 | Product Backlog |
| PARK-39 | Calculate availability for a time range | US-07 | BE | H | 3 | 2 | PARK-32, PARK-33 | Product Backlog |
| PARK-40 | Prevent overlapping reservations for a space | US-09 | BE | H | 5 | 2 | PARK-33, PARK-39 | Product Backlog |
| PARK-41 | Create reservation endpoint | US-09 | BE | H | 5 | 2 | PARK-36, PARK-40, PARK-45 | Product Backlog |
| PARK-42 | Cancel reservation endpoint | US-13 | BE | H | 2 | 2 | PARK-36, PARK-41 | Product Backlog |
| PARK-43 | Update location and capacity endpoints | US-16 | BE | M | 3 | 2 | PARK-32, PARK-36, PARK-45 | Product Backlog |
| PARK-44 | Record check-in and check-out times | US-16 | BE | M | 2 | 3 | PARK-41 | Product Backlog |
| PARK-45 | Write API validation and error responses | US-02 | BE | H | 2 | 1 | PARK-31, PARK-32, PARK-33 | Product Backlog |
| PARK-46 | Add backend tests for reservation conflicts | US-09 | QA | H | 3 | 2 | PARK-40, PARK-41, PARK-42 | Product Backlog |
| PARK-47 | Show operator daily occupancy report | US-18 | FE | M | 2 | 3 | PARK-39, PARK-44 | Product Backlog |
| PARK-48 | Show operator weekly occupancy trend | US-18 | FE | M | 2 | 3 | PARK-47 | Product Backlog |
| PARK-49 | Show operator reservation count by location | US-18 | FE | M | 2 | 3 | PARK-41 | Product Backlog |
| PARK-50 | Show operator cancellation count | US-18 | FE | M | 1 | 3 | PARK-42 | Product Backlog |
| PARK-51 | Show operator revenue summary | US-18 | FE | M | 2 | 3 | PARK-59, PARK-60 | Product Backlog |
| PARK-52 | Allow operator report date filtering | US-18 | FE | M | 2 | 3 | PARK-47, PARK-49 | Product Backlog |
| PARK-53 | Export operator reservations to CSV | US-18 | FE | M | 2 | 3 | PARK-49, PARK-52 | Product Backlog |
| PARK-54 | Show driver parking history summary | US-14 | FE | M | 2 | 3 | PARK-20 | Product Backlog |
| PARK-55 | Show driver total spending summary | US-14 | FE | M | 1 | 3 | PARK-59 | Product Backlog |
| PARK-56 | Show driver receipts per reservation | US-14 | FE | M | 2 | 3 | PARK-59 | Product Backlog |
| PARK-57 | Allow driver to download reservation history | US-14 | FE | M | 2 | 3 | PARK-54 | Product Backlog |
| PARK-58 | Show operator average parking duration | US-18 | FE | M | 2 | 3 | PARK-44 | Product Backlog |
| PARK-59 | Demonstrate mock payment success and failure | US-10 | BE | H | 5 | 2 | PARK-41 | Not yet on Trello |
| PARK-60 | Demonstrate eligible mock refunds | US-20 | BE | M | 3 | 2 | PARK-42, PARK-59 | Not yet on Trello |
| PARK-61 | Display in-app confirmations and reminders | US-11 | FE | M | 2 | 2 | PARK-41, PARK-42 | Not yet on Trello |
| PARK-62 | Manage driver vehicles | US-04 | BE | M | 2 | 2 | PARK-31, PARK-36 | Not yet on Trello |
| PARK-63 | Open map and navigation links | US-05 | FE | M | 2 | 2 | PARK-37 | Not yet on Trello |
| PARK-64 | Manage administrator roles and activity log | US-19 | BE | M | 3 | 3 | PARK-36 | Not yet on Trello |
| PARK-65 | Modify reservations atomically | US-13 | BE | H | 5 | 2 | PARK-40, PARK-41, PARK-42 | Not yet on Trello |
| PARK-66 | Update operator rates and space status | US-17 | BE | M | 2 | 2 | PARK-43 | Not yet on Trello |
| PARK-67 | Run integrated security, accessibility and recovery checks | US-21 | QA | H | 5 | 4 | PARK-30, PARK-46, PARK-59, PARK-60, PARK-61, PARK-62, PARK-63, PARK-64, PARK-65, PARK-66, PARK-53, PARK-58 | Not yet on Trello |
| PARK-68 | Prepare deployment and handoff package | US-22 | DO | H | 3 | 4 | PARK-67 | Not yet on Trello |

PARK-13 now includes the accessibility filter checklist; PARK-63 includes map markers and a directions link. PARK-10 reset and PARK-61 notifications use local/demo delivery. PARK-59/60/51/55/56 use only mock money. PARK-64 supplies the existing WBS’s account administration/activity review; PARK-65 covers modification already present in UC-13. PARK-66 covers rate and space-status updates already present in the WBS. These ten additional tasks clarify existing scope rather than adding production features.

## 5. Sprint plan and dependency decisions

| Sprint | Dates | Goal | Planned tasks | Points | Exit condition |
|---|---|---|---:|---:|---|
| 1 | Oct. 19–30 | Accounts, server validation/access controls, seeded locations and initial operator views | 20 | 41 | US-01/02 foundations and location views demonstrated; invalid and wrong-role cases pass |
| 2 | Nov. 2–13 | Facility management, reservations, conflict prevention and mock transaction flows | 31 | 75 | Core create/change/cancel and synthetic payment/refund paths pass; T5/T6/T7 evidence recorded |
| 3 | Nov. 16–27 | Reporting, audit/admin and integration | 15 | 29 | Reports/admin complete by Nov. 20; T9 integration starts Nov. 23; aggregates reconcile |
| 4 | Nov. 30–Dec. 11 | Complete integration, quality checks, deployment and handoff | 2 | 8 | T9 complete Dec. 1; acceptance evidence by Dec. 8; release package by Dec. 11 |

Sprint 1 retains the original 15 selected cards and promotes PARK-03, 06, 08, 09 and 45 from the backlog because duplicate-account handling, credential errors, logout, authorization and API validation are prerequisites for a credible account demonstration. The revised selection is 20 tasks. Reassess capacity before starting; these are planning targets, not a commitment derived from velocity. T2 design contracts are a gate for all sprints. PARK-31–33 may be designed in T2, but implementation acceptance remains open.

Within Sprint 2, finish operator updates first (T5 target Nov. 6); build reservation conflict protection before confirmation, and mock payment/refund against the agreed reservation contract. PARK-17 can use the documented rate contract while PARK-66 is implemented, but acceptance waits for integration. PARK-59 can be developed from the T6 contract in parallel; PARK-18 acceptance waits for both services. Sprint 3 reporting work begins in T8 from Nov. 9 against agreed schemas, with final acceptance by Nov. 20. Sprint labels indicate the acceptance window and do not prohibit earlier design work.

No work is marked complete by this update. At each review record actual hours, accepted points, blockers, remaining forecast and changed risk IDs. If the plan exceeds available role hours, split stories and reforecast with the documented change process before accepting extra scope.

## 6. Trello evidence and synchronization checklist

All 68 tasks are synchronized with Trello. Sprint 1 contains 20 cards, Sprint 2 contains 31, Sprint 3 contains 15, and Sprint 4 contains 2.

Every card includes story references, estimates, dependencies, and acceptance criteria. No implementation tasks have been marked complete.
