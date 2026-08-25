# Use-Case Specification: Reserve Table

## 1. Use Case Information

**Use Case ID:** UC-01

**Use Case Name:** Reserve Table

**Primary Actor:** Diner

**Supporting Actors:**
- Restaurant Manager
- Kitchen Staff

**Priority:** High

---

## 2. Description

This use case describes how a diner selects an available restaurant table and makes a reservation for a specified date and time. The system verifies table availability, creates the reservation, updates table status, and provides confirmation to the diner.

The diner may optionally extend the reservation process by pre-ordering food.

---

## 3. Preconditions

1. The diner has opened the Restaurant Table Booking & Pre-Ordering App.
2. The restaurant floor plan is available.
3. The selected date and time are valid.
4. The system is connected to the reservation database.
5. The restaurant has tables available for the requested time period.

---

## 4. Postconditions

### Success Postconditions

1. The selected table is successfully reserved.
2. The reservation is stored in the system.
3. The table availability status is updated.
4. The diner receives a reservation confirmation.
5. The reservation becomes visible to the restaurant manager.

### Failure Postconditions

1. No reservation is created if the selected table is unavailable.
2. The table remains available if the reservation attempt fails.
3. The diner is informed about the failure and can select another table.

---

# 5. Main Success Scenario

1. The diner opens the application.
2. The system displays the restaurant floor plan.
3. The diner selects the required date and time.
4. The system displays tables available for the selected date and time.
5. The diner selects an available table.
6. The system displays the selected table number and seating capacity.
7. The diner enters the required reservation information.
8. The system checks whether the selected table is still available.
9. The system creates the reservation.
10. The system updates the table status to reserved.
11. The system displays a reservation confirmation to the diner.
12. The system makes the reservation information available to the restaurant manager.

---

# 6. Alternate Flow

## A1 - Selected Table Becomes Unavailable

1. The diner selects an available table.
2. Before confirmation, another diner reserves the same table for the same time.
3. The system detects that the selected table is no longer available.
4. The system informs the diner that the selected table is unavailable.
5. The system displays other available tables.
6. The diner selects another available table.
7. The system continues the reservation process from Step 5 of the Main Success Scenario.

---

# 7. Alternate Flow - Optional Food Pre-Order

## A2 - Diner Adds a Food Pre-Order

1. After selecting a table, the system provides the option to pre-order food.
2. The diner chooses to pre-order food.
3. The system displays the available menu items.
4. The diner selects food items and quantities.
5. The system calculates the total pre-order amount.
6. The system calculates the estimated kitchen preparation timeline.
7. The diner confirms the pre-order.
8. The system associates the pre-order with the table reservation.
9. The kitchen receives the pre-order information.

---

# 8. Related Use Cases

- View Floor Plan
- Select Table
- Check Table Availability
- Confirm Reservation
- Pre-Order Food
- Calculate Kitchen Preparation Timeline
- Manage Reservations
- Manage Pre-Orders
- View Pre-Order Ticket

---

# 9. UML Relationships

**Reserve Table <<include>> Check Table Availability**

The availability check is mandatory whenever a diner attempts to reserve a table.

**Reserve Table <<include>> Confirm Reservation**

Reservation confirmation is a required part of successfully completing the reservation.

**Pre-Order Food <<extend>> Reserve Table**

Food pre-ordering is optional and therefore extends the table reservation process.

**Pre-Order Food <<include>> Calculate Preparation Timeline**

The preparation timeline is calculated when a diner chooses to pre-order food.
