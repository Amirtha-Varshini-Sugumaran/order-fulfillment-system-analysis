# Interview Notes

## 90-Second Explanation

This project was based on a logistics company that was managing orders and deliveries through Excel, email, and phone calls. The main issue was that nobody had one reliable view of delivery status. Operations had to chase drivers, customer support had to ask around before giving updates, and delays were often noticed too late.

I approached it as a Business Systems Analyst project. First, I documented the current process and the pain points. Then I identified the main stakeholders: operations, drivers, customer support, management, finance, and customers. From there, I created a BRD to capture the business need, an FRD for the system functions, and an SRS to describe the system behaviour and constraints.

The proposed solution was an internal order fulfillment and delivery tracking system. It lets operations create orders, assign drivers, track delivery status, flag delays, and give customer support a clear status view. I also created user stories, acceptance criteria, process flows, a data model, an API overview, and an Agile sprint plan.

The main value of the project is that it shows the full SDLC thinking: understand the current business process, gather requirements, define scope, support system design, prepare Agile delivery items, and help the team test and launch something practical.

## How I Worked In The SDLC

I started with discovery and requirements gathering. I looked at the current manual process and documented how orders moved from customer request to delivery completion.

Then I moved into analysis and design. I separated business requirements from functional and system requirements, because managers care about outcomes while developers need clearer detail on system behaviour.

After that, I supported Agile delivery by creating user stories, acceptance criteria, and a sprint plan. I also thought through UAT, reporting, and go-live readiness because the work does not stop when requirements are written.

## How I Gathered Requirements

I would gather requirements through:

- Interviews with operations managers and coordinators
- A walkthrough of the existing Excel tracker
- A review of common customer support queries
- A driver workflow discussion
- Observation of how delays are currently handled
- Follow-up sessions to confirm business rules

I would ask practical questions like:

- What information is needed before a delivery can be assigned?
- What statuses do teams actually use?
- When is a delivery considered delayed?
- What does customer support need to say to customers?
- What reports are used in daily operations meetings?

## How I Collaborated With Developers

I would work with developers by giving them clear user stories, acceptance criteria, process flows, and data rules. If a developer had a question about status logic or role access, I would take that back to the business and confirm it quickly.

I would also join backlog refinement, sprint planning, and demo sessions. During development, I would help explain edge cases, review test scenarios, and check whether the delivered feature matched the business need.

## How Agile Was Followed

The project was broken into three short sprints.

Sprint 1 focused on order intake and basic tracking. Sprint 2 focused on driver assignment and delivery updates. Sprint 3 focused on dashboard reporting, customer support view, and UAT fixes.

The Agile work included user stories, acceptance criteria, prioritised backlog items, sprint goals, demos, feedback, and UAT involvement. The BA role was to keep the business need clear and help the team avoid building features that were outside the first release.

## Interview Q&A

### 1. What was the main business problem?

The main problem was lack of visibility. Orders and deliveries were tracked in Excel and email, so operations, drivers, and customer support were not always working from the same information.

### 2. Who were the key stakeholders?

The key stakeholders were operations managers, operations coordinators, drivers, customer support agents, senior management, finance, sales, IT support, and customers.

### 3. How did you define the project scope?

I kept the first release focused on order intake, delivery assignment, status tracking, search, delay visibility, and basic reporting. I left route optimisation, GPS tracking, customer portal, and finance automation out of scope.

### 4. What documents did you create?

I created a BRD, FRD, SRS, AS-IS and TO-BE process analysis, user stories, acceptance criteria, process flows, stakeholder analysis, data model, API overview, Agile delivery plan, and interview notes.

### 5. How did you handle requirements?

I separated business needs from functional details. The BRD explained why the project mattered. The FRD explained what users needed to do. The SRS explained system behaviour, constraints, and non-functional requirements.

### 6. What was an important business rule?

One important rule was that a delivery should be flagged as delayed if the planned delivery time has passed and it has not been marked as delivered. A user can also manually mark it delayed, but they must enter a reason.

### 7. How did you support Agile delivery?

I created user stories and acceptance criteria, helped prioritise the backlog, supported sprint planning, clarified questions during development, and prepared UAT scenarios with the business users.

### 8. How would you test this system?

I would test the full workflow: create an order, assign it to a driver, update status, mark a delay, search the order as customer support, and check that dashboard counts update correctly.

### 9. What would you do if operations wanted route optimisation in Sprint 1?

I would explain that route optimisation is valuable but larger than the first release. I would capture it as a future backlog item and keep Sprint 1 focused on replacing the manual tracking process first.

### 10. What did this project teach you?

It showed how important it is to understand the real working process before writing requirements. The issue was not just a missing system. It was also unclear ownership, manual updates, and teams not having the same information at the same time.

