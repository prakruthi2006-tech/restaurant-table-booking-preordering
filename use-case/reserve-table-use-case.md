# Use-Case Flow Specification

## Reserve Table

### 1. Use Case Information

**Use Case ID:** UC3
**Use Case Name:** Reserve Table
**Primary Actor:** Diner
**Supporting Actors:** Restaurant Manager
**Goal:** Allow a diner to select and reserve an available restaurant table for a desired dining time.

### 2. Preconditions

1. The restaurant booking system is available.
2. The restaurant floor plan and table information are available.
3. The diner has accessed the booking system.
4. The diner has selected the required dining date/time and party details.

### 3. Postconditions

**Success:**

* The selected table is reserved for the diner.
* The reservation details are stored in the system.
* The table status is updated to reserved.
* The diner receives a reservation confirmation.

**Failure:**

* No reservation is created if the selected table is unavailable.
* The diner is informed that the table cannot be reserved.

### 4. Main Success Scenario

1. The diner opens the restaurant booking system.
2. The system displays the restaurant floor plan.
3. The diner selects the required dining date and time.
4. The diner selects an available table from the floor plan.
5. The system checks the availability of the selected table.
6. The system displays the selected table and reservation details.
7. The diner confirms the reservation.
8. The system creates the reservation.
9. The system updates the table status to reserved.
10. The system displays a reservation confirmation to the diner.

### 5. Alternative Flow

**A1: Selected Table Is Unavailable**

1. At Step 5, the system determines that the selected table is no longer available.
2. The system informs the diner that the selected table cannot be reserved.
3. The system refreshes the floor plan and displays currently available tables.
4. The diner selects another available table.
5. The system checks the availability of the newly selected table.
6. If the table is available, the system continues from Step 6 of the Main Success Scenario.
7. If no suitable table is available, the reservation process is terminated without creating a reservation.

### 6. Related Use Cases

* **View Floor Plan (UC1):** Allows the diner to view the restaurant layout.
* **Select Table (UC2):** Allows the diner to choose a specific table.
* **Check Table Availability (UC4):** Included during the reservation process to prevent double-booking.
* **Confirm Reservation (UC5):** Included to finalize the reservation.

### 7. Relationships

* **Reserve Table (UC3) `<<include>>` Check Table Availability (UC4)**
* **Reserve Table (UC3) `<<include>>` Select Table (UC2)**
* **Reserve Table (UC3) `<<include>>` Confirm Reservation (UC5)**

The **Pre-Order Food (UC6)** use case may **`<<extend>>` Reserve Table (UC3)** when the diner chooses to pre-order food along with the reservation.
