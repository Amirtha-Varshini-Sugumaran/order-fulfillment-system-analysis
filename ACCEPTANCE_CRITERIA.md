# Acceptance Criteria

## US-01: Create Order

- Given I am an authorised operations user, when I enter all required order details, then the system creates a new order.
- Given required fields are missing, when I try to save the order, then the system shows validation messages.
- Given an order is created, then the system assigns a unique order ID.
- Given an order is created, then the initial status is `Pending`.

## US-02: Assign Delivery

- Given an order is in `Pending` status, when I assign it to a driver, then the status changes to `Assigned`.
- Given I assign a driver, then the driver name is shown on the order.
- Given I save the assignment, then the system records the assignment date and time.
- Given an order is cancelled or delivered, then it cannot be assigned again without manager action.

## US-04: Update Delivery Status

- Given I am a driver with assigned deliveries, when I open my delivery list, then I only see deliveries assigned to me.
- Given I update a delivery status, then the new status is visible to operations and support.
- Given I mark a delivery as delayed, then the system asks for a reason note.
- Given a status is updated, then the system records who updated it and when.

## US-05: Search Customer Order

- Given I am a customer support agent, when I search by order ID, then the matching order is shown.
- Given I search by customer name, then matching orders are listed.
- Given an order is found, then the latest status and planned delivery time are visible.
- Given no order is found, then the system shows a clear no-results message.

## US-06: Flag Delayed Delivery

- Given the planned delivery time has passed and the order is not delivered, then the system flags the order as delayed.
- Given an order is delayed, then it appears in the delayed deliveries dashboard count.
- Given a delayed order is delivered, then it no longer appears as active delayed work.
- Given a user manually marks an order delayed, then a delay reason is required.

## US-08: View Status History

- Given I open an order, when I view status history, then I can see each previous status update.
- Given a status update exists, then it shows date, time, user, status, and note where available.
- Given there are no previous updates, then the system shows the current status only.

## US-09: View Daily Dashboard

- Given I open the dashboard, then I can see pending, active, delayed, and completed delivery counts.
- Given deliveries are assigned to drivers, then I can see orders per driver.
- Given orders are completed today, then they are included in the completed today count.

