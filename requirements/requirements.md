# Restaurant Table Booking & Pre-Ordering App

## 1. Project Overview

The Restaurant Table Booking & Pre-Ordering App is a restaurant hospitality system that allows diners to view available tables on a live floor plan, select and reserve a specific table, and optionally pre-order food before arriving at the restaurant. The system also allows restaurant managers and kitchen staff to manage reservations and food pre-orders efficiently.

## 2. Stakeholders / Actors

### Diner

The diner uses the application to view available tables, select a table, make a reservation, and optionally pre-order food.

### Restaurant Manager

The restaurant manager manages reservations, table availability, and pre-orders through the system.

### Kitchen Staff

Kitchen staff receive and manage food pre-order information so that food can be prepared before the diner arrives.

---

# 3. Functional Requirements

## FR-001 - View Live Floor Plan and Available Tables

**Type:** Functional Requirement

**Description:**  
The system shall allow diners to view an interactive restaurant floor plan displaying tables and their current availability status. Diners shall be able to select an available table.

**Priority:** High

**Acceptance Criteria:**
- Available tables shall be clearly displayed on the floor plan.
- Reserved or unavailable tables shall not be selectable.
- Selecting an available table shall display its table number and seating capacity.
- The system shall prevent two diners from successfully reserving the same table for the same time period.

**Rationale:**  
This is a core feature of the application because diners need to identify and select a specific available table while preventing table overbooking.

---

## FR-002 - Reserve a Table

**Type:** Functional Requirement

**Description:**  
The system shall allow a diner to reserve a selected available table for a specified date and time by providing the required booking information.

**Priority:** High

**Acceptance Criteria:**
- The diner shall provide all required reservation information.
- The system shall verify table availability before confirming the reservation.
- A successfully reserved table shall become unavailable for the selected time period.
- The diner shall receive a reservation confirmation after successful booking.

**Rationale:**  
Table reservation is the primary purpose of the application and enables diners to secure a specific table before arriving at the restaurant.

---

## FR-003 - Pre-Order Food

**Type:** Functional Requirement

**Description:**  
The system shall allow diners to select food items and quantities and associate the pre-order with their table reservation.

**Priority:** High

**Acceptance Criteria:**
- The diner shall be able to view available menu items.
- The diner shall be able to select multiple food items and quantities.
- The system shall calculate the total amount of the pre-order.
- The pre-order shall be linked to the correct table reservation.
- The diner shall be able to modify the pre-order before final confirmation.

**Rationale:**  
Pre-ordering allows the restaurant to prepare food before the diner arrives and helps provide faster service.

---

## FR-004 - Calculate Kitchen Preparation Timeline

**Type:** Functional Requirement

**Description:**  
The system shall calculate and display the estimated kitchen preparation timeline for a diner's pre-order based on the selected food items and reservation time.

**Priority:** Medium

**Acceptance Criteria:**
- The system shall calculate an estimated preparation time for the pre-order.
- The estimated completion time shall be associated with the reservation.
- The kitchen shall receive the relevant preparation information.
- The preparation timeline shall be updated when the diner modifies the pre-order.

**Rationale:**  
Preparation-time information allows kitchen staff to plan food preparation and ensure that the order is ready close to the diner's arrival.

---

## FR-005 - Manage Reservations and Pre-Orders

**Type:** Functional Requirement

**Description:**  
The system shall allow the restaurant manager to view, confirm, modify, and cancel table reservations and associated food pre-orders.

**Priority:** High

**Acceptance Criteria:**
- The restaurant manager shall be able to view upcoming reservations.
- The restaurant manager shall be able to view pre-orders associated with reservations.
- The restaurant manager shall be able to modify or cancel a reservation.
- Changes to reservations shall update the corresponding table availability.
- Updated reservation information shall be stored in the system.

**Rationale:**  
Restaurant managers need administrative control over reservations and pre-orders to manage restaurant operations effectively.

---

# 4. Non-Functional Requirements

## NFR-001 - Performance and Security

**Type:** Non-Functional Requirement - Performance & Security

**Description:**  
The system shall synchronize table availability and reservation status across all authorized restaurant manager terminals within 500 milliseconds under normal operating conditions. The system shall also ensure that reservation and customer information is accessible only to authorized users.

**Priority:** High

**Acceptance Criteria:**
- Table-status updates shall be synchronized within 500 milliseconds under normal operating conditions.
- Unauthorized users shall not be able to access restaurant manager functions.
- Customer and reservation information shall be transmitted securely.
- Performance and security testing shall confirm compliance with the required standards.

**Rationale:**  
Fast synchronization helps prevent conflicting reservations and table overbooking, while security protects customer and restaurant information.

---

## NFR-002 - Availability and Reliability

**Type:** Non-Functional Requirement - Availability & Reliability

**Description:**  
The system shall maintain accurate reservation and table-availability information and recover from temporary service failures without losing confirmed reservation data.

**Priority:** High

**Acceptance Criteria:**
- Confirmed reservations shall not be lost during temporary service failures.
- The system shall not display a table as available when it has already been confirmed for the requested time.
- Failed transactions shall not create duplicate reservations.
- Recovery testing shall confirm that reservation information remains consistent after a temporary failure.

**Rationale:**  
Reliable reservation information is essential because incorrect table availability can cause double bookings and negatively affect the customer experience.

---

# 5. Requirement Summary

| ID | Type | Requirement | Priority |
|---|---|---|---|
| FR-001 | Functional | View Live Floor Plan and Available Tables | High |
| FR-002 | Functional | Reserve a Table | High |
| FR-003 | Functional | Pre-Order Food | High |
| FR-004 | Functional | Calculate Kitchen Preparation Timeline | Medium |
| FR-005 | Functional | Manage Reservations and Pre-Orders | High |
| NFR-001 | Performance & Security | Fast synchronization and secure access | High |
| NFR-002 | Availability & Reliability | Reliable and consistent reservation data | High |
