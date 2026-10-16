# Smart Parking Platform

**Course:** CIS 4374  
**Student:** Sarrthi Jasrotia  
**Company:** WE ARE Software Corp.  
**Date:** September 10, 2026  
**Last reviewed:** October 15, 2026  

## 1. Competitive Analysis

Before developing the Smart Parking Platform, WE ARE Software Corp. researched existing parking applications to understand what is already available. The main competitors reviewed were SpotHero, ParkMobile, and ParkWhiz.

### SpotHero

SpotHero allows drivers to search for parking near a destination, compare prices, reserve a space, and pay in advance. It is available through both a mobile application and a website.

**Strengths:**

- Simple search and reservation process
- Allows users to compare parking prices
- Provides digital parking passes
- Available in many major cities
- Supports airport, event, hourly, and monthly parking

**Weaknesses and opportunities:**

- Available parking depends on participating facilities
- The system mainly focuses on finding and reserving parking
- Our platform could provide more detailed real-time occupancy information and stronger management tools for parking operators

Source: [SpotHero](https://spothero.com/)

### ParkMobile

ParkMobile allows users to pay for street parking, reserve parking in advance, manage multiple vehicles, and extend certain parking sessions from their phones. It is commonly used for street parking, universities, airports, garages, and event venues.

**Strengths:**

- Supports both on-demand payments and advance reservations
- Available in hundreds of cities
- Allows users to manage multiple vehicles
- Provides business and fleet-management options
- Includes a feature that helps users locate their parked vehicle

**Weaknesses and opportunities:**

- Features can differ depending on the city or parking location
- Users must carefully enter the correct parking zone and vehicle information
- Our platform could provide clearer verification before payment and combine driver and operator features in one consistent experience

Source: [ParkMobile](https://parkmobile.io/)

### ParkWhiz

ParkWhiz helps drivers search for and reserve parking before arriving at their destinations. Users can compare parking locations and prices and receive a digital parking pass after completing a reservation.

**Strengths:**

- Allows advance parking reservations
- Shows different parking locations and prices
- Supports parking near airports, events, and major destinations
- Provides digital confirmation and parking passes

**Weaknesses and opportunities:**

- Primarily focused on advance reservations
- Availability depends on participating parking facilities
- Our platform could offer more live occupancy information, navigation assistance, and operational analytics

Source: [ParkWhiz](https://www.parkwhiz.com/)

### Opportunity for the Smart Parking Platform

The Smart Parking Platform will combine useful features from existing applications while providing a more complete system for drivers and parking operators. Drivers will be able to view real-time availability, compare options, reserve spaces, navigate to parking locations, make digital payments, and receive notifications.

Parking operators will have access to an administrative dashboard for monitoring occupancy, managing prices and reservations, and reviewing reports and analytics. The goal is to create one platform that improves both the driver experience and the management of parking facilities.

## 2. Vision and Scope

### Company Introduction

WE ARE Software Corp. is a fictional software development company that designs technology solutions for businesses and the public. The company has been selected to plan and manage the development of a Smart Parking Platform. The initial scenario allowed unlimited theoretical resources. The current planning baseline instead uses the explicit 828-hour resource estimate and $36,949 funding requirement in the cost plan, within the semester timeline. These are fictional estimates, not actual spending or staffing commitments.

### Project Background

The Smart Parking Platform project was acquired because drivers often waste time searching for available parking. This can cause traffic congestion, frustration, wasted fuel, and delays. Parking facility operators also need better tools to monitor occupancy, manage reservations and pricing, and understand how their facilities are being used.

### Project Vision

The vision is to create a convenient web and mobile platform that connects drivers with available parking spaces in real time. Drivers will be able to locate, reserve, navigate to, and pay for parking through one system. Parking operators will be able to manage their facilities and make better decisions using occupancy data, reports, and analytics.

### Project Objectives

The project’s main objectives are to:

- Reduce the time drivers spend searching for parking
- Display parking availability in real time
- Allow users to reserve and pay for parking digitally
- Provide directions to selected parking facilities
- Help operators manage spaces, prices, and reservations
- Provide useful occupancy reports and analytics
- Protect users’ personal and payment information

### Stakeholders

The primary stakeholders include:

- Drivers and vehicle owners
- Parking facility operators
- City transportation departments
- System administrators
- Finance and billing personnel
- Mobile and web application users
- Third-party payment and navigation providers
- The project’s software development teams

### In Scope

The semester deliverable is a responsive web prototype, usable on desktop and mobile browsers. References to real-time availability mean refreshed simulated or operator-entered records, with a visible update timestamp. Payment, refund, receipt, and spending features use synthetic transactions in a sandbox or mock service; they never charge real money. Maps may use sample coordinates and navigation links. Notifications may be demonstrated in the application without paid email/SMS services. The broader product vision above is retained as context.


The initial system will include:

- User registration and authentication
- Vehicle and payment-method management
- Real-time parking availability
- Map-based parking searches
- Parking reservations
- Digital payments
- Reservation history and receipts
- Notifications and alerts
- Navigation-service integration
- An operator dashboard
- Occupancy reports and analytics
- Administrative account management

### Out of Scope

The initial project will not include:

- Native iOS/Android application releases and production service-level guarantees
- Live sensor or gate integration, real card storage, live charges, and ongoing production support
- Construction or physical maintenance of parking facilities
- Manufacturing parking sensors or gate equipment
- Issuing government parking citations
- Managing valet employees
- Providing vehicle repair or roadside-assistance services

These features may be considered in future versions but are not included in the initial project scope.

## 3. Software Requirements Specification Draft

### 3.1 Purpose

The purpose of this Software Requirements Specification is to define the initial functional and nonfunctional requirements for the Smart Parking Platform. These requirements will guide the design and development teams throughout the project.

### 3.2 Intended Users

The system will support the following types of users:

- Drivers
- Parking facility operators
- System administrators
- Finance and billing personnel
- City transportation personnel

### 3.3 Functional Requirements

The prototype shall meet the following requirements. Acceptance criteria and task links appear in [User Stories and Backlog](User-Stories-and-Backlog.md).

| ID | Requirement |
|---|---|
| FR-01 | Register accounts and maintain profiles and vehicles; reject invalid fields and duplicate emails. |
| FR-02 | Authenticate users, support logout and a simulated reset flow, and enforce role and record ownership checks on the server. |
| FR-03 | Show seeded parking locations on a map or equivalent map view with destination search and price/distance filters. |
| FR-04 | Calculate availability for the requested interval from space status and active reservations; label simulated data and show its last refresh time. |
| FR-05 | Show facility rates, operating hours, restrictions, capacity, and accessibility details. |
| FR-06 | Create, view, modify, and cancel reservations; reject invalid intervals and overlapping bookings atomically. |
| FR-07 | Demonstrate successful and failed sandbox/mock payments and eligible refunds without storing real card data. |
| FR-08 | Show reservation histories, synthetic receipts, and downloadable history for the signed-in driver only. |
| FR-09 | Display in-app confirmation, reminders, and cancellation/change notices linked to the correct reservation. |
| FR-10 | Open directions to a selected facility through an external navigation link using seeded coordinates. |
| FR-11 | Allow authorized operators to maintain their facilities, capacity, space status, rates, and reservation activity. |
| FR-12 | Provide date-filtered occupancy, reservation, cancellation, simulated revenue, and duration reports and CSV export. |
| FR-13 | Allow authorized administrators to manage accounts/roles and inspect an activity log. |
| FR-14 | Isolate external services behind mock/sandbox interfaces and show a recoverable error when an integration fails. |

### 3.4 Nonfunctional Requirements

These are planned acceptance targets; no performance, security, or accessibility results are claimed yet.

| ID | Area | Measurable acceptance target |
|---|---|---|
| NFR-01 | Security | Unauthenticated, wrong-role, and other-driver requests are rejected; passwords are hashed; secrets are excluded from Git; only synthetic data is used. |
| NFR-02 | Performance | On a documented local test environment with 100 seeded spaces and 20 concurrent simulated users, at least 95% of search/availability requests finish within 2 seconds. Record timing evidence. |
| NFR-03 | Data integrity | Two simultaneous requests for the same space and overlapping interval produce exactly one confirmed reservation; cancellation restores availability once. |
| NFR-04 | Usability and accessibility | Core registration, search, reservation, and cancellation flows work by keyboard, have visible focus and labeled fields, and show readable errors; verify contrast and a 375px viewport. |
| NFR-05 | Compatibility | Core flows pass on current Chrome and Safari at desktop and mobile viewport sizes; record tested versions. |
| NFR-06 | Reliability and recovery | Failed API/service requests display an error and retry path without duplicate reservations; a seeded database backup can be restored in a documented rehearsal. |
| NFR-07 | Privacy | Screens, exports, and logs do not expose another driver’s data or real payment details; driver exports are restricted by ownership. |
| NFR-08 | Maintainability | README documents setup, environment variable names, seed/reset steps, and test commands; API request/response examples are versioned. |

### 3.5 Initial Use Cases

| ID | Use Case | Primary Actor | Description |
|---|---|---|---|
| UC-01 | Register an Account | Driver | A driver creates an account using personal and contact information. |
| UC-02 | Log In | User | A registered user securely signs into the platform. |
| UC-03 | Manage Profile | Driver | A driver updates personal information, preferences, and account settings. |
| UC-04 | Manage Vehicles | Driver | A driver adds, edits, or removes vehicle and license-plate information. |
| UC-05 | Search for Parking | Driver | A driver searches for parking near a destination, address, or current location. |
| UC-06 | Filter Parking Results | Driver | A driver filters results by price, distance, availability, accessibility, or other preferences. |
| UC-07 | View Real-Time Availability | Driver | A driver views current parking availability at participating locations. |
| UC-08 | View Parking Details | Driver | A driver views prices, operating hours, restrictions, amenities, and location information. |
| UC-09 | Reserve a Parking Space | Driver | A driver selects an available parking option and creates a reservation. |
| UC-10 | Pay for Parking | Driver | A driver demonstrates a successful or failed mock/sandbox payment; no real charge is made. |
| UC-11 | Receive Confirmation | Driver | The system sends the driver a reservation confirmation and digital parking pass. |
| UC-12 | Navigate to Parking | Driver | A driver opens directions to the selected parking facility through a navigation service. |
| UC-13 | Modify or Cancel Reservation | Driver | A driver changes or cancels an eligible reservation. |
| UC-14 | View History and Receipts | Driver | A driver reviews previous reservations, payments, and receipts. |
| UC-15 | Receive Notifications | Driver | The system sends reminders, expiration warnings, changes, and other parking alerts. |
| UC-16 | Manage Parking Facility | Parking Operator | An operator updates facility information, hours, spaces, rules, and availability. |
| UC-17 | Manage Pricing | Parking Operator | An operator creates or changes parking rates for a facility. |
| UC-18 | View Reports and Analytics | Parking Operator | An operator views occupancy, reservation, payment, and usage reports. |
| UC-19 | Manage Users | System Administrator | An administrator reviews accounts, permissions, and reported account problems. |
| UC-20 | Process Refund | Finance Personnel | An authorized operator acting in the finance role reviews an eligible synthetic transaction and demonstrates a mock refund. |

### 3.6 Example Detailed Use Case

**Use Case ID:** UC-09  
**Use Case Name:** Reserve a Parking Space  
**Primary Actor:** Driver  

**Preconditions:**

- The driver is authenticated and has selected a vehicle.
- The selected parking facility has an available parking option.

**Main Flow:**

1. The driver searches for parking near a destination.
2. The system displays available parking options.
3. The driver selects a parking location.
4. The driver enters the desired date and time.
5. The system confirms availability and displays the total price.
6. The driver confirms the reservation and submits payment.
7. The system records a mock/sandbox payment result and confirms the booking only once; failure releases any temporary hold.
8. The system commits the reservation using an atomic conflict check, updates availability, and displays an in-app confirmation and synthetic receipt.

**Alternative Flows:**

- If the space is no longer available, the system asks the driver to select another option.
- If a mock payment fails, no confirmed booking or paid receipt is created.
- If two drivers confirm the same space at once, only one succeeds; the other receives an availability error.
- If the interval is invalid or outside facility hours, the request is rejected with a useful message.
- Modification rechecks availability atomically before replacing the previous interval; cancellation is allowed before the arrival time and is idempotent.

**Postconditions:**

- The reservation is stored in the driver’s account.
- The parking inventory is updated.
- The driver receives a confirmation and digital parking pass.

### 3.7 Assumptions and Dependencies

- Availability uses seeded/simulated or operator-entered records, not a live sensor feed.
- Users will have access to a supported mobile device or web browser.
- Internet access will be required for real-time services.
- Mock/sandbox payment and refund interfaces provide repeatable success and failure cases without real charges.
- Navigation uses an external directions link; the prototype remains usable if the map service is unavailable.
- The platform must comply with applicable security, privacy, city, and parking regulations.

### 3.8 Review and change control

This October 15 revision aligns the SRS with the existing prototype budget and risk plan. Sarrthi Jasrotia maintains the coursework; the staffing names in the resource plan are fictional scenario roles. Requirements and design approval milestones are planned gates, not evidence of instructor approval. Every scope change must identify affected requirement/story, WBS item, PARK task, risk, schedule, and cost before implementation. See the backlog for implementation status and acceptance evidence requirements.
