# Order Fulfillment & Delivery Tracking System Analysis

## Overview

This project documents the analysis and proposed design for an internal order fulfillment and delivery tracking system for a mid-sized Irish logistics and delivery company.

The company currently manages customer orders, delivery assignments, and delivery updates through Excel spreadsheets, emails, phone calls, and manual follow-ups. This works while volumes are low, but it creates delays, missed updates, duplicate work, and poor visibility for customers and operations staff.

The proposed system gives the operations team one place to manage orders from intake through delivery completion. It supports order creation, delivery assignment, driver status updates, customer visibility, and basic reporting.

## Business Problem

The current process depends heavily on manual tracking. Orders are entered into spreadsheets, delivery updates are sent by email or phone, and customers often call the support team because they do not have a clear delivery status.

This creates several problems:

- Operations staff spend time chasing updates instead of managing exceptions.
- Drivers receive assignments manually and sometimes receive changed information late.
- Customer support cannot always answer status questions quickly.
- Delays are only noticed after customers complain or drivers call in.
- Managers do not have a reliable view of pending, active, delayed, or completed deliveries.

## Approach

The analysis follows a practical business systems workflow:

1. Map the current manual process and identify operational pain points.
2. Define the future process and first-release scope.
3. Translate business needs into BRD, FRD, SRS, user stories, and acceptance criteria.
4. Outline the supporting data model, API concepts, dashboard view, and delivery plan.

The first release is intentionally focused on visibility and coordination. Larger features such as route optimisation, GPS tracking, and a customer portal are treated as future enhancements so the core workflow can be delivered quickly.

## Key Outputs

- `BRD.md` - Business Requirements Document
- `FRD.md` - Functional Requirements Document
- `SRS.md` - System Requirements Specification
- `AS_IS_TO_BE.md` - Current and future process comparison
- `USER_STORIES.md` - Agile user stories
- `ACCEPTANCE_CRITERIA.md` - Acceptance criteria for key stories
- `PROCESS_FLOWS.md` - Current and future process diagrams
- `DATA_MODEL.md` - Logical data model
- `API_OVERVIEW.md` - High-level API overview
- `STAKEHOLDER_ANALYSIS.md` - Stakeholder table
- `AGILE_DELIVERY_PLAN.md` - Sprint plan and delivery approach
- `artifacts/sample_dataset.csv` - Sample order and delivery records
- `artifacts/dashboard_mockup.md` - Simple dashboard mockup

## Business Value

The proposed system helps the business move from reactive manual tracking to a more controlled delivery workflow.

- Operations gets a single view of active, delayed, and completed deliveries.
- Customer support can answer basic order status questions without chasing updates.
- Drivers receive clearer assignments and have a simple way to update status.
- Managers get practical daily KPIs for workload, delays, and completion.
- The business gains a foundation for future customer self-service tracking.

## Scope Decisions

The design keeps the first release simple because adoption is the main success factor. The system focuses on order intake, delivery assignment, status updates, search, delay visibility, and dashboard reporting.

Out-of-scope items such as live GPS, route optimisation, finance automation, and a customer-facing portal are documented separately to protect delivery timelines and avoid overbuilding the first version.

## Skills Demonstrated

- Business process analysis
- Requirements gathering
- BRD, FRD, and SRS documentation
- User stories and acceptance criteria
- Stakeholder analysis
- Agile sprint planning
- Basic system and data modelling
- API and workflow understanding
- SDLC communication between business and technical teams
