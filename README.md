## NAME-PRAKRUTHI.NK
##SRN-PES2UG24AM118
##SECTION-5B
# Restaurant Table Booking & Pre-Ordering App

## Software Engineering Lab 1

## 1. Project Overview

The Restaurant Table Booking & Pre-Ordering App is a restaurant hospitality system that allows diners to view available tables on a live floor plan, select and reserve a specific table, and optionally pre-order food before arriving at the restaurant.

The system also allows restaurant managers and kitchen staff to manage reservations and food pre-orders efficiently.

## 2. Problem Statement

A restaurant hospitality application is required to enable diners to select specific tables using a live floor plan, place advance food orders, and calculate kitchen preparation timelines for seamless arrival dining.

## 3. Stakeholders / Actors

### Diner

Views available tables, selects tables, makes reservations, and optionally pre-orders food.

### Restaurant Manager

Manages reservations, table availability, and food pre-orders.

### Kitchen Staff

Receives and manages food pre-order information for kitchen preparation.

## 4. Functional Requirements

The system contains five functional requirements:

- FR-001 - View Live Floor Plan and Available Tables
- FR-002 - Reserve a Table
- FR-003 - Pre-Order Food
- FR-004 - Calculate Kitchen Preparation Timeline
- FR-005 - Manage Reservations and Pre-Orders

Detailed requirements are available in:

`requirements/requirements.md`

## 5. Non-Functional Requirements

The system contains two non-functional requirements:

- NFR-001 - Performance and Security
- NFR-002 - Availability and Reliability

Detailed requirements are available in:

`requirements/requirements.md`

## 6. UML Use-Case Model

The UML use-case model contains:

- Diner
- Restaurant Manager
- Kitchen Staff
- View Floor Plan
- Select Table
- Reserve Table
- Check Table Availability
- Confirm Reservation
- Pre-Order Food
- Calculate Preparation Timeline
- Manage Reservations
- Manage Pre-Orders
- View Pre-Order Ticket

The UML model contains both:

- `<<include>>`
- `<<extend>>`

relationships.

The PlantUML source is available at:

`uml/use-case-diagram.puml`

## 7. Core Use Case

The selected core use case is:

**UC-01 - Reserve Table**

The detailed specification contains:

- Preconditions
- Postconditions
- Main Success Scenario
- Alternate Flow
- Optional Food Pre-Order Flow

The specification is available at:

`use-case/reserve-table-use-case.md`

## 8. Repository Structure

```text
restaurant-table-booking-preordering/
│
├── README.md
│
├── requirements/
│   └── requirements.md
│
├── uml/
│   └── use-case-diagram.puml

Course: Software Engineering

Department: Department of Computer Science and Engineering

Project: Restaurant Table Booking & Pre-Ordering App
│
└── use-case/
    └── reserve-table-use-case.md
