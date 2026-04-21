# Business Requirements Document

## Project Name

Order Fulfillment & Delivery Tracking System

## Problem Statement

The company currently tracks orders and deliveries using Excel, emails, and phone calls. This causes delays, repeated manual work, and poor visibility across the business.

Operations staff do not have one reliable view of order status. Drivers receive assignments manually. Customer support often needs to call operations or drivers before answering customer questions. Managers cannot easily see how many orders are pending, delayed, or completed.

The business needs a simple internal system that manages orders from intake to delivery completion and gives staff accurate delivery status in one place.

## Business Objectives

- Reduce manual tracking through spreadsheets and email.
- Give operations staff a single view of all active orders and deliveries.
- Allow deliveries to be assigned to drivers more quickly.
- Improve visibility of delayed deliveries.
- Reduce customer calls about basic delivery status.
- Support basic reporting for daily operations.
- Create a foundation for future customer self-service tracking.

## Stakeholders

| Stakeholder | Business Need |
|---|---|
| Operations Manager | Needs visibility of order progress and driver workload |
| Operations Coordinators | Need to create, update, and assign orders quickly |
| Customer Support Team | Need reliable status information when customers call |
| Drivers | Need clear delivery assignments and simple status updates |
| Sales Team | Need confidence that customer deliveries are being handled |
| Finance Team | Need completed delivery records for billing checks |
| Senior Management | Need reports on service levels and delays |
| Customers | Need clearer delivery updates and fewer manual follow-ups |

## Scope

### In Scope

- Create and maintain customer orders.
- Assign deliveries to drivers.
- Track delivery status from pending to completed.
- Flag delayed deliveries.
- Provide internal order search and filtering.
- Provide basic customer update information.
- Provide simple dashboard KPIs for operations.
- Maintain delivery history for review and reporting.

### Out Of Scope

- Full route optimisation.
- Live GPS tracking.
- Driver payroll.
- Finance invoicing automation.
- Warehouse stock management.
- Mobile app store release.
- Customer-facing tracking portal in the first release.
- Integration with third-party carrier systems.

## High-Level Business Requirements

| ID | Requirement |
|---|---|
| BR-01 | The business must be able to record new customer delivery orders in one system. |
| BR-02 | Operations must be able to assign orders to available drivers. |
| BR-03 | Staff must be able to see the latest delivery status without checking email threads. |
| BR-04 | The system must highlight delayed or at-risk deliveries. |
| BR-05 | Customer support must be able to search for an order and give customers a clear update. |
| BR-06 | Managers must be able to view daily operational KPIs. |
| BR-07 | The system must keep a history of status changes for audit and follow-up. |
| BR-08 | The first release must be simple enough for operations staff to adopt without heavy training. |

## Business Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Staff continue using spreadsheets after launch | Data becomes split across tools | Provide training and remove duplicate spreadsheet templates after go-live |
| Driver updates are not entered on time | Operations still lacks accurate status | Keep driver update process simple and mobile-friendly |
| Scope grows into route optimisation too early | Delivery is delayed | Keep first release focused on order and status visibility |
| Poor data quality during order creation | Incorrect deliveries or customer updates | Add required fields and validation |
| Customer support does not trust the system | They continue calling operations | Include support team in testing and acceptance |

## Success Criteria

- At least 90% of new orders are recorded in the system within the first month.
- Operations can see active, pending, delayed, and completed deliveries from one dashboard.
- Customer support can answer basic order status questions without contacting operations.
- Manual spreadsheet tracking is retired for daily delivery management.
- Delayed deliveries are visible before customer complaints are received.
- Operations staff can assign a delivery in less than two minutes.

