# Agile Delivery Plan

## Delivery Approach

The project will be delivered using short Agile sprints. The first release focuses on replacing the manual order and delivery tracker with a simple internal system.

The priority is to deliver the core workflow first:

1. Create order
2. Assign driver
3. Update delivery status
4. Search and view latest status
5. Report on daily operations

## Sprint Plan

## Sprint 1: Order Intake And Core Tracking

Goal: Build the base order management workflow.

Backlog items:

- Create order form
- Required field validation
- Order list view
- Search by order ID and customer name
- Basic status values
- Status history storage

BA activities:

- Confirm required order fields with operations.
- Review sample Excel tracker.
- Define field rules and status values.
- Support backlog refinement.
- Review test scenarios with QA.

## Sprint 2: Delivery Assignment And Driver Updates

Goal: Allow operations to assign orders and capture delivery progress.

Backlog items:

- Assign driver to order
- Planned delivery date and time
- Driver delivery list
- Status update function
- Delay reason capture
- Driver workload view

BA activities:

- Run walkthrough with operations coordinators.
- Confirm driver update steps.
- Define acceptance criteria for assignment and delay handling.
- Support UAT preparation.

## Sprint 3: Dashboard And Operational Readiness

Goal: Give managers and support teams visibility before launch.

Backlog items:

- Dashboard KPI summary
- Delayed delivery view
- Customer support status view
- Role-based access
- UAT fixes
- Training notes and go-live checklist

BA activities:

- Facilitate UAT sessions.
- Capture business feedback and defects.
- Confirm reporting definitions.
- Support go-live readiness review.
- Help prepare simple user guidance.

## Backlog Overview

| Priority | Item | Reason |
|---|---|---|
| Must Have | Create order | Required to replace spreadsheet intake |
| Must Have | Assign delivery | Core operations workflow |
| Must Have | Update status | Needed for visibility |
| Must Have | Search order | Needed by customer support |
| Must Have | Delayed delivery flag | Needed for exception handling |
| Should Have | Dashboard KPIs | Useful for managers and daily stand-ups |
| Should Have | Driver workload view | Helps assignment decisions |
| Could Have | Customer notification templates | Valuable but can come later |
| Could Have | Customer tracking portal | Future phase |
| Won't Have In Release 1 | Route optimisation | Too large for first release |

## Prioritisation Logic

Items were prioritised based on business value and dependency.

The first release must solve the biggest pain point: lack of one reliable delivery status. Features that support that goal are treated as must-have. Items that improve reporting or customer experience are planned after the core workflow is stable.

## BA Role In Agile Lifecycle

The BA supports the Agile lifecycle by:

- Gathering requirements through interviews and process walkthroughs.
- Turning business needs into user stories.
- Writing acceptance criteria that can be tested.
- Clarifying scope during backlog refinement.
- Helping developers understand business rules.
- Supporting QA with test scenarios.
- Running UAT sessions with operations and support.
- Capturing feedback and helping the Product Owner decide priority.

