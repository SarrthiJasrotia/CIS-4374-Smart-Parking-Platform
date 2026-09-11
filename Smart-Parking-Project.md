# Smart Parking Platform

**Course:** CIS 4374  
**Student:** Sarrthi Jasrotia  
**Company:** WE ARE Software Corp.  
**Date:** September 10, 2026  

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

WE ARE Software Corp. is a fictional software development company that designs technology solutions for businesses and the public. The company has been selected to plan and manage the development of a Smart Parking Platform. For this project, the company has unlimited theoretical resources and funding but must complete the project within the semester timeline.

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

The Smart Parking Platform shall:

1. Allow users to create and manage accounts.
2. Authenticate users securely.
3. Display available parking locations on an interactive map.
4. provide real-time parking-space availability.
5. Allow drivers to search and filter parking options.
6. Allow drivers to reserve and cancel parking reservations.
7. Process digital payments securely.
8. Store reservation histories and receipts.
9. Send reservation confirmations, reminders, and alerts.
10. Provide navigation to selected parking locations.
11. Allow operators to manage parking facilities, availability, and pricing.
12. Provide occupancy reports and analytics.
13. Allow administrators to manage users and system activity.
14. Integrate with external payment and navigation services.

### 3.4 Nonfunctional Requirements

- **Security:** Personal and payment information must be protected through appropriate security controls.
- **Availability:** The system should be available at all times except during planned maintenance.
- **Performance:** Searches and availability updates should load within a reasonable amount of time.
- **Usability:** The mobile and web interfaces should be easy to understand and navigate.
- **Scalability:** The system should support growth in users, reservations, and parking facilities.
- **Accessibility:** The platform should follow accepted accessibility guidelines.
- **Privacy:** User information must be collected, stored, and processed according to applicable privacy requirements.
- **Compatibility:** The platform should work on commonly used mobile devices and web browsers.

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
| UC-10 | Pay for Parking | Driver | A driver pays for a reservation using an approved digital payment method. |
| UC-11 | Receive Confirmation | Driver | The system sends the driver a reservation confirmation and digital parking pass. |
| UC-12 | Navigate to Parking | Driver | A driver opens directions to the selected parking facility through a navigation service. |
| UC-13 | Modify or Cancel Reservation | Driver | A driver changes or cancels an eligible reservation. |
| UC-14 | View History and Receipts | Driver | A driver reviews previous reservations, payments, and receipts. |
| UC-15 | Receive Notifications | Driver | The system sends reminders, expiration warnings, changes, and other parking alerts. |
| UC-16 | Manage Parking Facility | Parking Operator | An operator updates facility information, hours, spaces, rules, and availability. |
| UC-17 | Manage Pricing | Parking Operator | An operator creates or changes parking rates for a facility. |
| UC-18 | View Reports and Analytics | Parking Operator | An operator views occupancy, reservation, payment, and usage reports. |
| UC-19 | Manage Users | System Administrator | An administrator reviews accounts, permissions, and reported account problems. |
| UC-20 | Process Refund | Finance Personnel | Authorized personnel review an eligible transaction and issue a refund. |

### 3.6 Example Detailed Use Case

**Use Case ID:** UC-09  
**Use Case Name:** Reserve a Parking Space  
**Primary Actor:** Driver  

**Preconditions:**

- The driver has opened the platform.
- The selected parking facility has an available parking option.

**Main Flow:**

1. The driver searches for parking near a destination.
2. The system displays available parking options.
3. The driver selects a parking location.
4. The driver enters the desired date and time.
5. The system confirms availability and displays the total price.
6. The driver confirms the reservation and submits payment.
7. The system processes the payment.
8. The system creates the reservation and provides a confirmation.

**Alternative Flows:**

- If the space is no longer available, the system asks the driver to select another option.
- If payment fails, the system asks the driver to use another payment method.

**Postconditions:**

- The reservation is stored in the driver’s account.
- The parking inventory is updated.
- The driver receives a confirmation and digital parking pass.

### 3.7 Assumptions and Dependencies

- Participating parking facilities will provide accurate availability information.
- Users will have access to a supported mobile device or web browser.
- Internet access will be required for real-time services.
- Payment processing will depend on a third-party payment provider.
- Navigation will depend on an external mapping service.
- The platform must comply with applicable security, privacy, city, and parking regulations.

This SRS is an initial draft and will be expanded and refined as additional requirements are gathered throughout the semester.
