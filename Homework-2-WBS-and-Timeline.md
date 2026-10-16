# Smart Parking Platform

## Homework 2: Work Breakdown Structure and Project Timeline

**Course:** CIS 4374  
**Student:** Sarrthi Jasrotia  
**Company:** WE ARE Software Corp.  
**Date:** September 17, 2026  
**Last reviewed:** October 15, 2026

## 1. Work Breakdown Structure

The Work Breakdown Structure organizes the Smart Parking Platform into major deliverables, modules, and features. It focuses on what the project will produce. The hierarchy contains four levels, exceeding the requirement of at least three levels.

### 1.0 Smart Parking Platform

- **1.1 User Access and Account Management**
  - **1.1.1 Authentication System**
    - 1.1.1.1 User registration
    - 1.1.1.2 Secure login
    - 1.1.1.3 Password recovery
    - 1.1.1.4 Session management
  - **1.1.2 Driver Account**
    - 1.1.2.1 Driver profile
    - 1.1.2.2 Vehicle information
    - 1.1.2.3 Payment methods
    - 1.1.2.4 Notification preferences
  - **1.1.3 Operator Account**
    - 1.1.3.1 Operator profile
    - 1.1.3.2 Facility permissions
    - 1.1.3.3 Staff access roles

- **1.2 Parking Search and Availability**
  - **1.2.1 Parking Search**
    - 1.2.1.1 Destination search
    - 1.2.1.2 Current-location search
    - 1.2.1.3 Search filters
  - **1.2.2 Parking Map**
    - 1.2.2.1 Interactive map
    - 1.2.2.2 Parking-location markers
    - 1.2.2.3 Navigation-service integration
  - **1.2.3 Availability Information**
    - 1.2.3.1 Real-time space availability
    - 1.2.3.2 Parking rates
    - 1.2.3.3 Operating hours and restrictions

- **1.3 Reservation Management**
  - **1.3.1 Reservation System**
    - 1.3.1.1 Date and time selection
    - 1.3.1.2 Space reservation
    - 1.3.1.3 Reservation confirmation
  - **1.3.2 Reservation Changes**
    - 1.3.2.1 Reservation modification
    - 1.3.2.2 Reservation cancellation
    - 1.3.2.3 Availability update
  - **1.3.3 Driver Records**
    - 1.3.3.1 Reservation history
    - 1.3.3.2 Digital parking pass
    - 1.3.3.3 Reminders and alerts

- **1.4 Parking Facility Management**
  - **1.4.1 Facility Setup**
    - 1.4.1.1 Facility information
    - 1.4.1.2 Operating hours
    - 1.4.1.3 Parking rules and amenities
  - **1.4.2 Space Management**
    - 1.4.2.1 Parking-space inventory
    - 1.4.2.2 Space status
    - 1.4.2.3 Accessible parking designation
  - **1.4.3 Pricing Management**
    - 1.4.3.1 Hourly rates
    - 1.4.3.2 Event and special rates
    - 1.4.3.3 Pricing updates
  - **1.4.4 Garage Monitoring**
    - 1.4.4.1 Occupancy dashboard
    - 1.4.4.2 Reservation monitoring
    - 1.4.4.3 Availability synchronization

- **1.5 Payment and Billing**
  - **1.5.1 Payment Processing**
    - 1.5.1.1 Payment-provider integration
    - 1.5.1.2 Payment authorization
    - 1.5.1.3 Payment confirmation
  - **1.5.2 Billing Records**
    - 1.5.2.1 Digital receipts
    - 1.5.2.2 Transaction history
    - 1.5.2.3 Financial records
  - **1.5.3 Refund Management**
    - 1.5.3.1 Refund eligibility
    - 1.5.3.2 Refund processing
    - 1.5.3.3 Refund confirmation

- **1.6 Reporting and Administration**
  - **1.6.1 Operational Reporting**
    - 1.6.1.1 Occupancy reports
    - 1.6.1.2 Reservation reports
    - 1.6.1.3 Usage trends
  - **1.6.2 Financial Reporting**
    - 1.6.2.1 Revenue reports
    - 1.6.2.2 Refund reports
    - 1.6.2.3 Report export
  - **1.6.3 System Administration**
    - 1.6.3.1 User management
    - 1.6.3.2 Role and permission management
    - 1.6.3.3 System activity review

- **1.7 Quality Assurance and Release**
  - **1.7.1 System Testing**
    - 1.7.1.1 Functional testing
    - 1.7.1.2 Integration testing
    - 1.7.1.3 Performance testing
  - **1.7.2 Security and Accessibility**
    - 1.7.2.1 Security testing
    - 1.7.2.2 Privacy review
    - 1.7.2.3 Accessibility review
  - **1.7.3 Final Release**
    - 1.7.3.1 Deployment package
    - 1.7.3.2 User documentation
    - 1.7.3.3 Final project delivery

### WBS interpretation and completion criteria — October 15 review

The hierarchy above remains the deliverable baseline. Availability (1.2.3 and 1.4.4) uses simulated/operator-entered data; payment methods, payments, financial records, and refunds (1.1.2.3, 1.5, and 1.6.2) use synthetic data and mock/sandbox processing. Map/navigation (1.2.2) uses seeded coordinates and a directions link. Mobile delivery means a responsive web interface. Hardware and live payments are excluded.

| WBS branch | Deliverable acceptance evidence | Planned gate |
|---|---|---|
| 1.1 | Registration, login, logout, profile/vehicle and permission tests | T3; vehicle/reset completion T6 |
| 1.2 | Search/filter/detail and time-range availability demonstrations | T4; map link T6 |
| 1.3 | Create/modify/cancel, ownership and atomic conflict tests | T6 |
| 1.4 | Authorized facility, capacity, rate and occupancy updates | T5 |
| 1.5 | Synthetic payment success/failure and eligible refund scenarios | T7 |
| 1.6 | Reconciled reports, exports and restricted admin functions | T8 |
| 1.7 | Integrated tests, security/accessibility checks, restore rehearsal and handoff | T9–T11 |

For every branch, “complete” requires implementation plus recorded acceptance results. Document updates alone do not establish feature completion. PARK task and user-story mappings are in [User Stories and Backlog](User-Stories-and-Backlog.md).

## 2. Project Timeline

The timeline uses estimation by analogy with a semester software project. The September 21–December 11 dates remain the 12-week planning baseline. They are target dates; elapsed dates do not establish actual completion or approval. No executable application or test results were present in the repository at this review. Work may proceed in parallel when dependencies allow.

| ID | Project activity | Start | Finish | Duration | Dependency |
|---|---|---|---|---:|---|
| T1 | Requirements validation | Sep. 21, 2026 | Oct. 2, 2026 | 10 workdays | None |
| T2 | Interface and system design | Oct. 5, 2026 | Oct. 16, 2026 | 10 workdays | T1 |
| T3 | Authentication and user profiles | Oct. 19, 2026 | Oct. 30, 2026 | 10 workdays | T2 |
| T4 | Parking search and availability | Oct. 19, 2026 | Oct. 30, 2026 | 10 workdays | T2 |
| T5 | Operator and garage management | Oct. 19, 2026 | Nov. 6, 2026 | 15 workdays | T2 |
| T6 | Reservation, vehicles, notifications and navigation | Nov. 2, 2026 | Nov. 13, 2026 | 10 workdays | T3, T4; T5 API contract |
| T7 | Payment and refund integration | Nov. 2, 2026 | Nov. 13, 2026 | 10 workdays | T3; T6 booking contract (SS) |
| T8 | Reporting and administration | Nov. 9, 2026 | Nov. 20, 2026 | 10 workdays | T5 |
| T9 | System integration | Nov. 23, 2026 | Dec. 1, 2026 | 7 workdays | T3–T8 complete |
| T10 | Testing and quality review | Dec. 2, 2026 | Dec. 8, 2026 | 5 workdays | T9 |
| T11 | Documentation and final release | Dec. 9, 2026 | Dec. 11, 2026 | 3 workdays | T10 |

### Project Milestones

| Milestone | Target date | Completion condition |
|---|---|---|
| Requirements approved | Oct. 2, 2026 | Initial requirements and scope receive approval |
| Design approved | Oct. 16, 2026 | Interface design and system architecture are complete |
| Core platform complete | Nov. 20, 2026 | Major driver and operator functions are integrated |
| Test build complete | Dec. 8, 2026 | Integration, security, and accessibility testing are complete |
| Final project delivery | Dec. 11, 2026 | Final platform package and documentation are delivered |

## 3. Gantt Chart

```mermaid
gantt
    title Smart Parking Platform Baseline (Targets, Not Actuals)
    dateFormat YYYY-MM-DD
    axisFormat %b %d
    excludes weekends

    section Planning and Design
    Requirements validation            :crit, req, 2026-09-21, 10d
    Requirements approved              :milestone, m1, after req, 0d
    Interface and system design         :crit, design, after req, 10d
    Design approved                     :milestone, m2, after design, 0d

    section Core Platform
    Authentication and user profiles    :auth, after design, 10d
    Parking search and availability     :search, after design, 10d
    Operator and garage management      :garage, after design, 15d
    Reservation and supporting flows    :reserve, after auth search, 10d
    Payment and refund integration      :pay, after auth, 10d

    section Reporting and Integration
    Reporting and administration        :report, after garage, 10d
    Core platform complete              :milestone, m3, after report, 0d
    System integration                  :crit, integration, after report, 7d

    section Testing and Release
    Testing and quality review           :crit, testing, after integration, 5d
    Test build complete                  :milestone, m4, after testing, 0d
    Documentation and final release      :crit, release, after testing, 3d
    Final project delivery               :milestone, m5, after release, 0d
```

## 4. Timeline Assumptions

- The project team can work on independent components at the same time.
- Requirements must be approved before design begins.
- System design must be approved before development begins.
- T1 and T2 are approval gates; their actual acceptance must be recorded before dependent development is marked ready.
- Reservation development depends on authentication, search/availability, and the agreed operator data contract.
- Mock payment/refund development shares the booking contract with T6 (start-to-start); it cannot be accepted until reservation integration passes.
- System integration requires T3–T8, including reservations, payments, operator functions, and reports. The longest baseline chain is T1 → T2 → T5 → T8 → T9 → T10 → T11.
- Durations use weekdays only, without holiday exclusions. November 26–27 availability is an explicit schedule risk, not assumed time off. Reforecast if coursework or availability changes.
- The team will update the timeline if the project scope or requirements change.


## 5. Sprint alignment and review status

| Period | Dates | Scope and exit evidence |
|---|---|---|
| Planning/design | Sep. 21–Oct. 16 | Reviewed SRS, stories, wireframes, API/database contracts; approval evidence required |
| Sprint 1 | Oct. 19–Oct. 30 | Accounts, security foundations, parking list and initial operator views (T3/T4 and start of T5) |
| Sprint 2 | Nov. 2–Nov. 13 | Finish T5; reservations, mock payments/refunds, vehicles and in-app notices (T6/T7); start reporting |
| Sprint 3 | Nov. 16–Nov. 27 | Finish T8 by Nov. 20; begin T9 Nov. 23; reporting reconciliation and integration checks |
| Sprint 4 | Nov. 30–Dec. 11 | Finish T9 Dec. 1, T10 Dec. 2–8, and T11 Dec. 9–11 |

As of October 15, the planning documents have been revised. Implementation, milestone approvals, and test completion remain unverified. The live Trello board matches the revised sprint selection and task dependencies documented in the backlog. No schedule slip or completed development is invented from the calendar alone.
