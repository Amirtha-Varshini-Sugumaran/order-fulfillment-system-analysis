# Functional Requirements Document

## Purpose

This document defines the main functions required for the order fulfillment and delivery tracking system.

The focus is on what users need to do, how the system should behave, and what information should move through the process.

## User Groups

| User Group | Main Actions |
|---|---|
| Operations Coordinator | Create orders, assign drivers, update delivery details |
| Operations Manager | Monitor workload, review delays, manage exceptions |
| Customer Support Agent | Search orders and view latest status |
| Driver | View assigned deliveries and update delivery status |
| Senior Manager | View high-level operational KPIs |

## Functional Requirements

### FR-01: Create Order

The system shall allow an operations coordinator to create a new order.

Required inputs:

- Customer name
- Customer contact number or email
- Delivery address
- Requested delivery date
- Order reference
- Delivery notes, if available

Expected outputs:

- Unique order ID
- Initial order status of `Pending`
- Created date and created by user

### FR-02: View Order List

The system shall display a list of orders with key information.

Users must be able to view:

- Order ID
- Customer name
- Delivery location
- Assigned driver
- Current status
- Requested delivery date
- Delay flag

Users must be able to filter by:

- Status
- Driver
- Delivery date
- Delayed orders

### FR-03: Search Order

The system shall allow users to search for an order.

Search fields:

- Order ID
- Customer name
- Customer phone number
- Location

The search result shall show the latest known order and delivery status.

### FR-04: Assign Delivery

The system shall allow operations staff to assign a pending order to a driver.

Required inputs:

- Order ID
- Driver
- Planned delivery date and time

System behaviour:

- Order status changes from `Pending` to `Assigned`.
- Driver name is linked to the delivery.
- Assignment timestamp is recorded.

### FR-05: Update Delivery Status

The system shall allow delivery status updates.

Supported statuses:

- Pending
- Assigned
- Out for Delivery
- Delayed
- Delivered
- Failed Delivery
- Cancelled

Each status update must record:

- Status
- Date and time
- Updated by
- Optional note

### FR-06: Delay Flagging

The system shall flag a delivery as delayed when:

- The planned delivery time has passed and the order is not delivered.
- A driver or operations user manually marks the delivery as delayed.

Delayed orders must be visible on the dashboard and order list.

### FR-07: Customer Status View

Customer support users shall be able to open an order and view a simple customer-friendly status message.

Example:

`Your order is out for delivery and is expected today between 14:00 and 16:00.`

The system should avoid exposing internal notes to customers.

### FR-08: Dashboard KPIs

The system shall provide a simple operations dashboard showing:

- Orders pending
- Orders assigned
- Deliveries out for delivery
- Deliveries delayed
- Deliveries completed today
- Average delivery time
- Orders per driver

### FR-09: Delivery History

The system shall keep a status history for each order.

History shall include:

- Previous status
- New status
- Date and time
- User who made the change
- Notes

### FR-10: Driver Workload View

The system shall show the number of active deliveries assigned to each driver.

This helps operations avoid overloading one driver while another has capacity.

## Use Cases

### Use Case 1: Create A New Delivery Order

Actor: Operations Coordinator

Steps:

1. Coordinator receives a new customer delivery request.
2. Coordinator opens the system and selects `Create Order`.
3. Coordinator enters customer and delivery details.
4. System validates required fields.
5. System creates the order with status `Pending`.
6. Order appears in the pending order list.

### Use Case 2: Assign Order To Driver

Actor: Operations Coordinator

Steps:

1. Coordinator opens the pending order list.
2. Coordinator reviews delivery location and requested time.
3. Coordinator selects an available driver.
4. Coordinator confirms planned delivery time.
5. System updates status to `Assigned`.
6. Driver can see the assigned delivery.

### Use Case 3: Update Delivery Status

Actor: Driver

Steps:

1. Driver opens assigned deliveries.
2. Driver selects an order.
3. Driver updates status to `Out for Delivery`, `Delivered`, or `Delayed`.
4. Driver adds a note if needed.
5. System records the update and timestamp.
6. Operations and customer support see the latest status.

### Use Case 4: Answer Customer Status Query

Actor: Customer Support Agent

Steps:

1. Customer calls for a delivery update.
2. Support agent searches by order ID or customer name.
3. System shows latest delivery status.
4. Agent gives customer the current update.
5. If delayed, agent can see the reason note where available.

