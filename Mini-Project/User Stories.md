# User Stories and Acceptance Criteria

## Project Opportunities & Talent Readiness Enhancement
**Purpose:** Mini-project deliverable — 8 focused, non-duplicative user stories.  
**Note:** Acceptance criteria are proposed for stakeholder validation.

---

## US-01 — Create a Project Opportunity
**Priority:** Must Have  
**As a** Project Manager, **I want** to create a project opportunity with required skills and key dates, **so that** employees can understand the project needs.

**Acceptance Criteria**
1. **Given** I am an authorized Project Manager, **when** I create an opportunity with all mandatory fields, **then** the system saves it as a draft.
2. **Given** a mandatory field is missing, **when** I try to save the opportunity, **then** the system identifies the missing field and does not save an incomplete record.
3. **Given** I am not authorized to create opportunities, **when** I attempt to access the create action, **then** the system denies the action.

## US-02 — Publish an Opportunity
**Priority:** Must Have  
**As a** Project Manager, **I want** to publish a complete opportunity, **so that** eligible employees can view it.

**Acceptance Criteria**
1. **Given** an opportunity contains all required information, **when** I publish it, **then** its status changes to Published and it becomes visible to eligible employees.
2. **Given** an opportunity is missing mandatory information, **when** I attempt to publish it, **then** publication is blocked and the missing information is identified.
3. **Given** an opportunity's start date has already passed, **when** I attempt to publish it, **then** the system blocks publication or requests correction according to the agreed business rule.

## US-03 — View Published Opportunities
**Priority:** Must Have  
**As an** eligible employee, **I want** to view published project opportunities, **so that** I can discover relevant internal opportunities.

**Acceptance Criteria**
1. **Given** published opportunities are available to me, **when** I open the opportunity list, **then** I see opportunities I am eligible to view.
2. **Given** an opportunity is a draft or has been closed, **when** I view the employee opportunity list, **then** it is not presented as an open opportunity.
3. **Given** no eligible published opportunities are available, **when** I open the list, **then** the system displays a clear empty-state message.

## US-04 — Compare Skills with Opportunity Requirements
**Priority:** Must Have  
**As an** employee, **I want** to compare my recorded skills with an opportunity's required skills, **so that** I can identify my suitability and skill gaps.

**Acceptance Criteria**
1. **Given** I open an opportunity, **when** I view its skill requirements, **then** the system displays the required skills and my corresponding recorded skills where available.
2. **Given** one or more required skills are not present in my recorded profile, **when** I review the comparison, **then** the missing or unconfirmed skills are clearly identified.
3. **Given** my skill profile is incomplete, **when** I review the comparison, **then** the system indicates that the comparison may be incomplete rather than treating missing data as proof of no skill.

## US-05 — Express Interest in an Opportunity
**Priority:** Must Have  
**As an** eligible employee, **I want** to express interest in a published opportunity, **so that** the Resource Manager can consider me for the project.

**Acceptance Criteria**
1. **Given** an opportunity is open and I have not already expressed interest, **when** I submit my interest, **then** the system records my interest and confirms the submission.
2. **Given** I have already expressed interest in the same opportunity, **when** I try to submit interest again, **then** the system prevents a duplicate active expression of interest.
3. **Given** an opportunity is closed or no longer accepting interest, **when** I attempt to express interest, **then** the system prevents submission and explains why.

## US-06 — Withdraw Interest
**Priority:** Must Have  
**As an** employee, **I want** to withdraw my interest while withdrawal is permitted, **so that** my interest status remains accurate if my availability or plans change.

**Acceptance Criteria**
1. **Given** I have an active expression of interest and withdrawal is permitted, **when** I confirm withdrawal, **then** the system updates my interest status to Withdrawn.
2. **Given** I have already withdrawn my interest, **when** I attempt to withdraw again, **then** the system does not create duplicate withdrawal records and displays the current status.
3. **Given** the agreed withdrawal cutoff has passed or a staffing decision prevents withdrawal, **when** I attempt to withdraw, **then** the system blocks the action and explains the applicable rule.

## US-07 — Review Interested Employees
**Priority:** Must Have  
**As a** Resource Manager, **I want** to review interested employees' skills, readiness, and availability, **so that** I can assess their suitability for a project.

**Acceptance Criteria**
1. **Given** I am an authorized Resource Manager, **when** I open an opportunity's interested-employee list, **then** I can view relevant skill, readiness, availability, and interest-status information permitted by my role.
2. **Given** an employee's profile information is missing or outdated, **when** I review the employee, **then** the system identifies the missing or unconfirmed information.
3. **Given** I do not have the required role, **when** I attempt to view restricted candidate information, **then** the system denies access.

## US-08 — Record a Staffing Outcome
**Priority:** Must Have  
**As a** Resource Manager, **I want** to record a shortlist or staffing outcome, **so that** the project staffing process has a clear and traceable result.

**Acceptance Criteria**
1. **Given** I am an authorized Resource Manager reviewing an opportunity, **when** I record a permitted shortlist or staffing outcome, **then** the system saves the decision, status, and authorized user's identity.
2. **Given** required decision information is missing, **when** I try to record the outcome, **then** the system identifies the missing information and does not save an incomplete decision.
3. **Given** an employee is shortlisted, **when** no authorized final allocation has been recorded, **then** the system does not represent the employee as finally allocated.
4. **Given** a staffing outcome is recorded, **when** the relevant users view the opportunity, **then** they see the status they are authorized to access.

---

## Coverage Summary
| Business Requirement | Related User Stories |
|---|---|
| BR-01 — Centralized opportunities | US-02, US-03 |
| BR-02 — Complete opportunity and skill information | US-01, US-02 |
| BR-03 — View opportunities and compare skills | US-03, US-04 |
| BR-04 — Express and withdraw interest | US-05, US-06 |
| BR-05 — Resource Manager review | US-07 |
| BR-06 — Shortlist and staffing outcome | US-08 |
| BR-08 — Role-based access | US-01, US-07, US-08 |

**Scope note:** Notifications and broader management reporting are not detailed as separate stories in this mini-project scope. They can be addressed in the main project deliverables.
