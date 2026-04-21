# Requirements Gathering Notes

## 1. Overview

Requirements were gathered by looking at how the delivery process actually works today, not just by asking for a wish list.

The main sources were stakeholder discussions, process observation, reviewing the Excel order tracker, checking delivery update email threads, and a few working sessions with people who handle orders every day.

The goal was to understand where orders start, who touches them, how delivery status changes, what information gets missed, and what each team needs from a new system.

These notes were used as the input for the BRD, FRD, SRS, user stories, process flows, and data model.

## 2. Stakeholders Identified

| Stakeholder | Role | What they care about |
|---|---|---|
| Operations Manager | Owns daily delivery performance and team coordination | Clear visibility of active orders, delays, driver workload, and service issues |
| Delivery Coordinator | Creates orders, assigns drivers, and follows up on delivery progress | Faster order handling, fewer calls, and one reliable place to update status |
| Finance Team | Checks completed deliveries against billing and customer records | Accurate completed delivery records and fewer mismatches |
| Customer Support | Answers customer calls and delivery status questions | Quick search, simple status messages, and confidence that the update is current |
| IT/System Owner | Supports internal systems and user access | Simple system design, clear roles, manageable support needs, and basic security |

## 3. Information Sources

- Excel order tracker  
  Showed the fields currently captured, such as customer, location, driver, date, and status. It also showed inconsistent status wording and some missing driver names.

- Email threads for delivery updates  
  Showed how many updates are buried in inboxes. Several delivery changes were confirmed by email but not reflected in the tracker straight away.

- Manual logs  
  Showed that some failed deliveries and late deliveries are written down separately, which means the main tracker is not always the full story.

- Calls between teams  
  Showed that operations, drivers, and support rely on quick calls when information is unclear. This works in the moment but leaves no useful audit trail.

- Customer queries  
  Showed that many customer calls are simple status questions. Support could answer faster if they had the latest delivery status in one place.

## 4. Sample Discussion / Meeting Notes

- Operations mentioned that delays usually become visible only when a driver calls in or a customer contacts support.

- The delivery coordinator said the Excel tracker is useful, but it is easy for two people to update different versions or forget to update it after a phone call.

- Customer support said they often need to ask operations for an update before replying to a customer, especially when the order is out for delivery.

- Finance highlighted that there can be a mismatch between delivered orders and orders ready for invoicing when completion details are not updated clearly.

## 5. Current Process Observations

- Orders are tracked manually in Excel after being received by phone or email.

- Delivery assignments are often confirmed through calls, emails, or quick messages rather than one central system.

- Status updates depend on someone remembering to update the spreadsheet after speaking to a driver.

- There is no real-time view of pending, active, delayed, or completed deliveries.

- Duplicate or slightly different entries can appear when the same customer order is discussed in more than one email thread.

- Delays are not always recorded with a clear reason, so it is hard to explain later what happened.

## 6. Key Questions Asked

- How are orders currently created and who enters them into the tracker?

- What information must be captured before a delivery can be assigned?

- Who decides which driver gets each delivery?

- How does a driver receive a delivery assignment today?

- Who updates the status when a delivery moves from pending to out for delivery?

- How are delays identified and recorded?

- What happens if a delivery fails or the customer is unavailable?

- How does customer support get delivery updates when customers call?

- What information does finance need before an order can be treated as delivered?

- Which reports or counts does management look at during the day?

## 7. Pain Points Identified

- Delays are not visible early enough, so the team often reacts after the issue has already affected the customer.

- Ownership is unclear when an order moves between operations, drivers, and support.

- Tracking is split across Excel, email, calls, and manual notes.

- Staff repeat follow-ups because they do not fully trust that the tracker is current.

- Data is inconsistent, especially around status names, delivery times, delay reasons, and failed delivery notes.

## 8. Derived Business Requirements (Input For BRD)

- The business needs one central place to track orders and delivery status.

- Operations needs better visibility of pending, assigned, active, delayed, and completed deliveries.

- Delivery coordination needs to be faster and less dependent on phone calls.

- Customer support needs access to current status information without chasing operations.

- Managers need simple daily reporting on delays, completed deliveries, and driver workload.

- The business needs a basic audit trail showing who updated a delivery and when.

## 9. Derived Functional Requirements (Input For FRD/SRS)

- The system should allow authorised users to create a new customer order.

- The system should generate a unique order ID for each order.

- The system should allow delivery coordinators to assign a driver to an order.

- The system should allow drivers or operations users to update delivery status.

- The system should track progress from pending through delivered, delayed, failed, or cancelled.

- The system should store status history with date, time, user, and notes where needed.

- The system should allow customer support to search orders by order ID, customer, or location.

- The system should show dashboard counts for pending orders, delayed deliveries, completed deliveries, and driver workload.

## 10. Derived Non-Functional Requirements

- The system must be secure and require users to log in.

- Access should be role-based so users only see the functions they need.

- The user interface should be simple because users are busy and not highly technical.

- Search and order lookup should respond quickly during normal business hours.

- The system should be reliable enough to support daily operations without falling back to spreadsheets.

## 11. User Roles Identified

- Operations Manager
- Delivery Coordinator
- Driver
- Finance User
- Customer Support

## 12. Assumptions Made

- Most users are comfortable with basic office systems but are not technical users.

- The company prefers a simple first release over a large system with route optimisation and live tracking.

- Budget and IT support capacity are limited, so the first version should avoid unnecessary complexity.

- Order volume is moderate, so the system needs to be reliable and searchable, but not designed like a large enterprise logistics platform.

## 13. Dependencies & Constraints

- The current process relies on Excel and email, so some existing data may need to be cleaned before migration.

- IT resources are limited, so user management, support, and setup should stay simple.

- Some staff may resist changing from Excel because it is familiar and quick for small updates.

- Training will be needed for operations, support, and drivers so everyone uses the same statuses.

- Driver updates may depend on mobile browser access, so the update flow should be short and easy to use.
