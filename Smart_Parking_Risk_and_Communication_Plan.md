# Smart Parking App: Risk and Communication Plan

**Course:** CIS 4374  
**Prepared by:** Sarrthi Jasrotia  
**Date:** October 1, 2026

## 1. Purpose and planning assumptions

This document identifies risks that could affect the Smart Parking App and defines how they will be monitored, addressed, and reported. It builds on the product backlog containing login, driver and operator interfaces, backend, and reporting tasks.

This plan covers a course prototype. Live parking sensors, production payments, and paid services are not assumed to be available or required. Risks concerning external data or paid services apply if those features are adopted. Development roles describe responsibilities; they do not imply separate people. Sarrthi Jasrotia owns the risks until responsibilities are formally reassigned.

## 2. Risks by category

Each risk is a possible future event, rather than a claim that a problem has already occurred.

### Technical risks

1. **T01 — Inaccurate availability:** Delayed updates or inconsistent test data could show a space as available when it is occupied or reserved.
2. **T02 — Conflicting reservations:** Two requests processed at the same time could reserve the same space.
3. **T03 — Unauthorized access:** Incorrect authentication or role checks could allow a driver to access operator functions or another user's records.
4. **T04 — Integration failures:** Mismatched frontend, API, and database formats could prevent login, availability views, or reservation requests from working.

### Schedule risks

1. **S01 — Underestimated work:** Tasks could take longer than estimated, delaying Sprint 1 or later milestones.
2. **S02 — Dependency delays:** An unfinished data model or API could block interface development and testing.
3. **S03 — Scope growth:** Adding features beyond the agreed backlog could consume time needed for required functionality.
4. **S04 — Late defect discovery:** Problems discovered near submission could leave insufficient time for fixes and verification.

### Financial risks

1. **F01 — Hosting limits or charges:** Hosting or database usage could exceed a free allowance, creating costs or interrupting access.
2. **F02 — External service costs:** Map, notification, or payment services could require paid plans if adopted.
3. **F03 — Hardware costs:** A request for physical parking sensors or other equipment could exceed available funds.
4. **F04 — Equipment replacement costs:** Laptop failure or data loss could require repairs, replacement, or paid recovery and delay work.

### People risks

1. **P01 — Skill gaps:** Limited familiarity with a selected framework, database, or security practice could lead to rework.
2. **P02 — Limited availability:** Illness or competing academic and work commitments could reduce available development time.
3. **P03 — Unclear responsibilities:** An unclear task owner or handoff could cause work to be duplicated or missed, especially if collaborators join.
4. **P04 — Delayed or misunderstood feedback:** Late instructor or tester responses, or misunderstood comments, could cause incorrect requirements to persist.

## 3. Risk rating method

Probability and impact are qualitative planning estimates and will be revised as evidence becomes available.

| Rating | Probability | Impact |
| --- | --- | --- |
| Low (1) | Unlikely during the course project | Minor rework within a planned work session; no required milestone affected |
| Medium (2) | Plausible during the course project | Several work sessions lost, reduced functionality, or a manageable added expense |
| High (3) | Likely without preventive action | A required milestone, core function, data security, or project affordability could be seriously affected |

**Risk score = probability × impact.** Scores 6–9 are high priority, 3–4 are medium priority, and 1–2 are low priority. Review high-priority risks first. A security or data-loss incident requires immediate attention regardless of score.

## 4. Risk register

All entries are initially **Open**: the risk has been identified, and the listed response is planned. Open does not mean that the event has occurred. The owner is **Sarrthi Jasrotia** for every entry.

### Technical register

| ID | Description | Probability | Impact | Score / priority | Owner | Response strategy | Status / notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| T01 | Delayed or inconsistent availability could show occupied or reserved spaces as free. | Medium (2) | High (3) | 6 / High | Sarrthi Jasrotia | Mitigate: use one database source of truth, refresh after changes, and display the last update time. Test occupied, reserved, and available states. | Open; review if displayed counts disagree with database records. Use clearly labeled simulated data if a live feed is unavailable. |
| T02 | Simultaneous requests could reserve the same space. | Medium (2) | High (3) | 6 / High | Sarrthi Jasrotia | Mitigate: check availability on the server and enforce reservation conflicts within a database transaction or equivalent atomic operation. | Open; trigger is an overlapping reservation in testing. Disable new bookings for the affected space until corrected. |
| T03 | Missing authentication or role checks could expose operator functions or another user's data. | Medium (2) | High (3) | 6 / High | Sarrthi Jasrotia | Mitigate: enforce server-side authentication, role checks, and record ownership checks; securely hash passwords. Test unauthenticated and wrong-role requests. | Open; use synthetic test accounts. Any unauthorized successful request blocks release of the affected function. |
| T04 | Frontend, API, and database mismatches could break core requests. | Medium (2) | High (3) | 6 / High | Sarrthi Jasrotia | Mitigate: document request and response fields, build one complete request path early, and verify success and failure responses. | Open; review when a core request fails. Fix the interface contract before adding dependent features. |

### Schedule register

| ID | Description | Probability | Impact | Score / priority | Owner | Response strategy | Status / notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| S01 | Underestimated tasks could delay planned milestones. | High (3) | Medium (2) | 6 / High | Sarrthi Jasrotia | Mitigate: split large cards into smaller tasks, compare estimates with actual progress, and reserve time before each deadline for verification. | Open; review any task taking more than twice its estimate. Replan optional work before moving required deadlines. |
| S02 | Unfinished database or API work could block interface development. | Medium (2) | High (3) | 6 / High | Sarrthi Jasrotia | Mitigate: record dependencies on Trello and complete foundational tasks first. Use agreed sample responses for parallel interface work. | Open; flag a blocked task at the next check-in. Finish the dependency or revise the task order. |
| S03 | Unplanned features could divert effort from required work. | Medium (2) | Medium (2) | 4 / Medium | Sarrthi Jasrotia | Avoid: keep a minimum required scope; place new ideas in the product backlog and assess effort before accepting them into a sprint. | Open; review whenever a new feature is requested. Defer optional additions if they threaten a milestone. |
| S04 | Late testing could reveal defects too close to submission. | High (3) | High (3) | 9 / High | Sarrthi Jasrotia | Mitigate: verify each completed feature and schedule a full core-flow check at least two days before a known submission deadline. | Open; prioritize login, availability, and required reservation flows over cosmetic fixes. |

### Financial register

| ID | Description | Probability | Impact | Score / priority | Owner | Response strategy | Status / notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| F01 | Hosting or database limits could create costs or interrupt access. | Medium (2) | Medium (2) | 4 / Medium | Sarrthi Jasrotia | Mitigate: check service limits before selection, monitor usage weekly, and avoid enabling paid upgrades without a cost review. | Open; conditional on hosted deployment. Maintain a local demo option if a service becomes unavailable. |
| F02 | External map, notification, or payment services could add unplanned fees. | Medium (2) | Medium (2) | 4 / Medium | Sarrthi Jasrotia | Avoid: use mock or sandbox integrations for the prototype where permitted; review pricing and required features before adopting a service. | Open; conditional on external services being added. Omit optional paid integrations if costs are unacceptable. |
| F03 | Physical parking hardware could exceed available funds. | Low (1) | High (3) | 3 / Medium | Sarrthi Jasrotia | Avoid: use simulated occupancy data for the course prototype unless hardware is explicitly required and funded. | Open; conditional on a hardware requirement. Seek clarification before purchasing equipment. |
| F04 | Equipment failure or lost files could require unexpected spending. | Low (1) | High (3) | 3 / Medium | Sarrthi Jasrotia | Mitigate: commit code regularly, back up documents, and confirm access to an alternative computer before a deadline. | Open; review backup availability weekly. Restore from backups and use an alternative device if needed. |

### People register

| ID | Description | Probability | Impact | Score / priority | Owner | Response strategy | Status / notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| P01 | Unfamiliar tools or practices could cause defects and rework. | Medium (2) | Medium (2) | 4 / Medium | Sarrthi Jasrotia | Mitigate: select familiar tools where practical, prototype unfamiliar features early, and verify implementation against official documentation. | Open; review if a technical blocker remains unresolved after a planned work session. Seek targeted guidance and simplify the design where appropriate. |
| P02 | Illness or competing commitments could reduce development time. | Medium (2) | High (3) | 6 / High | Sarrthi Jasrotia | Mitigate: schedule work blocks in advance, keep tasks small, and protect time for required features and submission preparation. | Open; review missed work blocks weekly. Reprioritize optional tasks and report material delays promptly. |
| P03 | Unclear ownership or handoffs could cause missed or duplicate work. | Low (1) | Medium (2) | 2 / Low | Sarrthi Jasrotia | Mitigate: record one accountable owner, a completion criterion, and relevant dependencies for each active task. Document handoffs if collaborators are assigned. | Open; currently one accountable owner. Review ownership whenever responsibilities change. |
| P04 | Delayed or misunderstood feedback could lead to incorrect requirements. | Medium (2) | Medium (2) | 4 / Medium | Sarrthi Jasrotia | Mitigate: ask focused questions early, summarize decisions in writing, and record assumptions while awaiting replies. | Open; escalate requirement uncertainty that blocks required work. Avoid building optional features based on an unresolved assumption. |

## 5. Risk monitoring and escalation

- Review the register every Thursday during the weekly progress review and whenever a major requirement changes.
- Update probability, impact, owner, response, and notes when new evidence changes an assessment.
- Use **Open**, **Monitoring** (response underway), **Occurred** (the event is now an issue), and **Closed** (no longer applicable or resolved) as status values. Record the reason for each status change.
- If a risk occurs, create a Trello issue card referencing its risk ID, describe the effect, assign the next action, and document the resolution.
- Address security, data loss, and failures of core functions immediately. Record other blockers within one working day. Contact the instructor through the course's approved channel if a blocker threatens required scope or a submission deadline.
- Track changes through GitHub commits so earlier risk assessments and decisions remain available.

## 6. Communication plan

The cadence below is proposed for the project. For an individual project, development check-ins are self-reviews documented on Trello. If collaborators are assigned, use the same cadence as short meetings and record participants and task owners. Instructor updates follow the course's required submission channel and deadlines.

| Activity / responsibility area | Participants or audience | Cadence / duration | Reporting method | Required information | Accountable owner |
| --- | --- | --- | --- | --- | --- |
| Project planning | Project owner; assigned collaborators if applicable | Monday, 15 minutes | Trello sprint cards and a short GitHub planning note | Current priorities, dependencies, owners, and work planned before the next review | Sarrthi Jasrotia |
| Development check-in | Person responsible for frontend, backend, or database work | Each planned workday, 5 minutes | Trello card status and comments | Work completed, next action, blockers, and any changed estimate | Sarrthi Jasrotia |
| Integration review | Frontend, backend, and database responsibilities | Wednesday, 15 minutes | GitHub issue or pull-request notes with test evidence | API/data-format changes, integration results, and unresolved defects | Sarrthi Jasrotia |
| Risk and cost review | Project owner; relevant role owners if assigned | Thursday, 15 minutes | Updated risk register in GitHub and linked Trello issue cards | Changed risk ratings, responses, service usage or costs, and decisions needed | Sarrthi Jasrotia |
| Testing and progress review | Project owner; available testers if applicable | Friday, 20 minutes, and before each milestone | Trello completion status and GitHub verification notes | Features demonstrated, test outcomes, incomplete work, and next priorities | Sarrthi Jasrotia |
| Instructor progress report | Instructor | Weekly, by the course deadline | Required update video and updated project documents through the course submission method | Accomplishments, risks or blockers, response actions, and next steps | Sarrthi Jasrotia |
| Blocker or urgent issue report | Project owner; affected collaborators; instructor when course scope or deadlines are threatened | Immediately for security/data-loss/core-function incidents; within one working day for other blockers | Trello issue linked to a GitHub issue; course-approved message for instructor escalation | Risk ID, impact, evidence, action needed, responsible person, and next update time | Sarrthi Jasrotia |
| Requirement or scope decision | Project owner; instructor when clarification is required | As needed, before committing to a change | Written decision in GitHub and updated Trello cards | Requested change, reason, schedule/cost effect, and accepted or deferred decision | Sarrthi Jasrotia |

### Reporting conventions

- **Trello** tracks task status, next actions, and blockers. Board: https://trello.com/b/F7a0wRUi/smart-parking-platform
- **GitHub** stores project documents, code when developed, verification evidence, and written decisions. Link related risk IDs in issue and commit descriptions.
- **Weekly updates** state what was completed, what remains, the most significant risks, and the next planned steps. Report actual results rather than marking planned responses as completed.
- **Check-in notes** use four fields: completed work, next work, blocker or risk ID, and action owner.
- **Meeting notes**, if meetings occur, include the date, attendees, decisions, action owners, and target dates. Add notes within one working day.
