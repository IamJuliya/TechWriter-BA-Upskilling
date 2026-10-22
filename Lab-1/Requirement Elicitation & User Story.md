# Lab 01 – Requirements Elicitation & User Story Writing

## 1. Project Overview

### Project Title

**Project Opportunities & Talent Readiness Enhancement**
### Business Problem

The existing Employee Management System provides employees with access to various HR and organizational services. However, temporarily unallocated employees may have limited visibility into upcoming project opportunities and the skills required for those projects.

Resource and Staffing Managers also need a structured way to identify employees who have the relevant skills, experience, interest, and readiness for upcoming project opportunities.

### Business Objective

Enhance the existing Employee Management System to provide:

- Visibility into upcoming project opportunities
- Project-specific skill requirements
- Skill-gap identification
- Employee interest management
- Employee readiness tracking
- Structured visibility for Resource and Staffing Managers

The enhancement will support staffing decisions but will **not automatically allocate employees to projects**.

---
## 2. Stakeholder Interview

### 2.1 Employee

**BA:** What information would you need before deciding whether a project is relevant to you?

**Employee:** I would need the project description, expected start date, duration, required skills, and experience requirements.

**BA:** Would it be useful to compare your existing skills with the project requirements?

**Employee:** Yes. It would help me understand which skills I already have and which skills I need to improve.

**BA:** What should happen if you express interest but later change your mind?

**Employee:** I should be able to withdraw my interest.

**BA:** What project changes should trigger a notification?

**Employee:** Important changes such as changes to required skills or the project start date should be communicated.

### 2.2 Resource/Staffing Manager

**BA:** How would you identify employees for an upcoming project?

**Resource Manager:** I would review their skills, experience, availability, and readiness against the project requirements.

**BA:** What information would help you evaluate employees who have expressed interest?

**Resource Manager:** Relevant skills, experience, availability, and preparation or readiness status would be useful.

**BA:** What should happen if an employee expresses interest more than once?

**Resource Manager:** There should be only one active interest record for an employee for a particular project.

**BA:** Who should be able to view employee skill and readiness information?

**Resource Manager:** Only authorized users involved in resource or staffing activities should have access.

**BA:** Does expressing interest mean the employee is automatically assigned to the project?

**Resource Manager:** No. Final allocation should require management evaluation and approval.

### 2.3 Project Manager

**BA:** What information is required before publishing a project opportunity?

**Project Manager:** The project name, description, expected start date, and required skills should be provided.

**BA:** What should happen when project requirements change after publication?

**Project Manager:** Authorized users should be able to update the requirements, and affected employees should be informed.

**BA:** What should happen when the project start date has already passed?

**Project Manager:** The project should no longer appear as an upcoming opportunity.

### 2.4 Learning & Development Representative

**BA:** How can skill-gap information help the Learning & Development team?

**L&D Representative:** It can help identify common learning needs and areas where training resources may be useful.

**BA:** How can employee readiness be represented?

**L&D Representative:** Readiness can be represented using defined statuses such as Not Started, In Progress, and Ready for Consideration.

**BA:** Should the system automatically assign training based on identified skill gaps?

**L&D Representative:** No. Skill gaps can support training planning, but training assignment should remain a separate process.

---
## 3. Business Requirements Document (BRD) Skeleton

### 3.1 Business Problem

Temporarily unallocated employees have limited visibility into upcoming project opportunities and the skills required for those opportunities. Resource and Staffing Managers need structured information to identify employees whose skills, experience, interest, and readiness align with upcoming project requirements.

### 3.2 Business Objective

The objective is to enhance the existing Employee Management System with a **Project Opportunities & Talent Readiness** feature that enables employees to discover opportunities, understand skill requirements, identify skill gaps, express or withdraw interest, and maintain readiness information.

The feature will also allow authorized Resource and Staffing Managers to review interested employees and support staffing decisions.

### 3.3 Proposed Solution

The proposed enhancement will allow authorized users to:

- Create and publish upcoming project opportunities
- Define mandatory and preferred skills
- Maintain project requirements
- Allow employees to view upcoming opportunities
- Allow employees to compare their skills with project requirements
- Allow employees to identify skill gaps
- Allow employees to express interest in projects
- Allow employees to withdraw interest
- Allow employees to update their readiness status
- Allow Resource Managers to review interested employees
- Notify interested employees about important project updates

The system will support staffing decisions but will **not automatically allocate employees to projects**.

---

## 4. Stakeholders and Their Interests

| Stakeholder | Interest |
|---|---|
| Employee | Find suitable opportunities, understand skill gaps, express interest, and manage readiness |
| Project Manager | Create project opportunities and maintain project requirements |
| Resource/Staffing Manager | Review interested employees and support staffing decisions |
| Learning & Development | Use skill-gap information for training and learning planning |
| System Administrator | Manage access, configuration, and system support |

---

## 5. Scope

### 5.1 In Scope

- Create and publish upcoming project opportunities
- Define mandatory and preferred skills
- View project opportunities
- View project skill requirements
- Identify skill gaps
- Express interest in a project
- Withdraw interest
- Update readiness status
- View interested employees
- Update project requirements
- Notify interested employees about important updates

### 5.2 Out of Scope

- Automatic project allocation
- Salary or compensation decisions
- Performance appraisal
- Promotion decisions
- Recruitment decisions
- Automatic training assignment
- Actual training delivery
- Automated hiring or staffing decisions

---

## 6. Assumptions

- Employee skill information is available through the existing Employee Management System.
- Employees are responsible for keeping their recorded skills reasonably up to date.
- Authorized Project and Resource Managers will maintain project information.
- Employees have access to the existing Employee Management System.
- An existing or approved notification mechanism is available.

---

## 7. Constraints

- The enhancement must operate within the existing Employee Management System.
- Employee skill, experience, availability, and readiness information must be protected through role-based access.
- Automatic employee allocation is not included in the first version.
- The solution must comply with applicable organizational privacy and access policies.

---

## 8. Dependencies

- Existing employee profile and skill data
- Existing authentication and authorization mechanisms
- Project and resource management information
- Notification mechanism
- Existing Employee Management System infrastructure

---

## 9. Non-Functional Requirements

| Category | Requirement |
|---|---|
| Security | Only authorized users can view staffing-related employee information. |
| Performance | Project information should load within the existing portal's response-time standards. |
| Usability | Employees should be able to find and understand project requirements without additional training. |
| Availability | The feature should follow the existing portal availability standards. |
| Privacy | Employee skill, experience, availability, and readiness information must not be visible to unauthorized users. |

---

## 10. Success Criteria

> **Note:** The following are educational target measures for this case study and are not actual organizational targets.

- At least 80% of published projects receive one or more employee interests within two weeks, where applicable.
- At least 90% of published projects contain all mandatory project and skill information.
- At least 90% of employees who express interest have relevant skill and readiness information available to authorized Resource Managers.
- At least 95% of important project updates are reflected in the portal and associated notifications within the agreed notification timeframe.
- 100% of projects whose start date has passed are excluded from the upcoming project list.

---

# 11. User Stories and Acceptance Criteria

## US-01 – View Upcoming Projects

**Priority:** Must Have

### User Story

> As an employee, I want to view upcoming project opportunities so that I can identify projects that match my skills and interests.

### Acceptance Criteria

#### Scenario 1 – Display Upcoming Projects

- **Given** the employee is logged in
- **When** the employee opens Project Opportunities
- **Then** the system displays published projects whose start date has not passed

#### Scenario 2 – View Project Information

- **Given** an upcoming project is displayed
- **When** the employee opens the project
- **Then** the system displays the project name, description, start date, and duration where available

#### Scenario 3 – Project Start Date Has Passed

- **Given** a project's start date has passed
- **When** the employee opens Project Opportunities
- **Then** the project is not displayed as an upcoming project

---

## US-02 – View Skills and Identify Skill Gaps

**Priority:** Must Have

### User Story

> As an employee, I want to compare my recorded skills with project requirements so that I can identify skill gaps and prepare for suitable opportunities.

### Acceptance Criteria

#### Scenario 1 – View Project Skills

- **Given** the employee opens a published project
- **When** project skill requirements are available
- **Then** the system displays the required skills and identifies mandatory and preferred skills

#### Scenario 2 – Compare Skills

- **Given** the employee has recorded skills
- **When** the employee views the project requirements
- **Then** the system identifies matching and missing or below-required skills

#### Scenario 3 – Skill Information Unavailable

- **Given** the employee has no recorded skill information
- **When** the employee views the skill comparison
- **Then** the system indicates that skill information is unavailable instead of showing a false match

---

## US-03 – Express Interest

**Priority:** Must Have

### User Story

> As an employee, I want to express interest in an upcoming project so that the Resource Manager can consider me for the opportunity.

### Acceptance Criteria

#### Scenario 1 – Express Interest

- **Given** the project is published and upcoming
- **When** the employee selects Express Interest
- **Then** the system records the employee's interest and displays a confirmation

#### Scenario 2 – Duplicate Interest

- **Given** the employee has already expressed interest in the project
- **When** the employee selects Express Interest again
- **Then** the system prevents a duplicate active interest record and informs the employee that interest is already recorded

#### Scenario 3 – No Automatic Allocation

- **Given** the employee has expressed interest
- **When** the interest is recorded
- **Then** the system does not automatically assign the employee to the project

---

## US-04 – Withdraw Interest

**Priority:** Should Have

### User Story

> As an employee, I want to withdraw my interest in a project so that the Resource Manager has accurate information about my current interest.

### Acceptance Criteria

#### Scenario 1 – Withdraw Active Interest

- **Given** the employee has an active interest in a project
- **When** the employee selects Withdraw Interest
- **Then** the system marks the interest as withdrawn and displays a confirmation

#### Scenario 2 – No Active Interest

- **Given** the employee does not have an active interest in the project
- **When** the employee attempts to withdraw interest
- **Then** the system does not create or modify an interest record

---

## US-05 – Update Readiness Status

**Priority:** Should Have

### User Story

> As an employee, I want to update my readiness status for a project so that the Resource Manager can understand my preparation level.

### Acceptance Criteria

#### Scenario 1 – Update Readiness

- **Given** the employee has expressed interest in an upcoming project
- **When** the employee selects a readiness status
- **Then** the system saves the selected readiness status

#### Scenario 2 – Display Defined Readiness Statuses

- **Given** the employee opens the readiness options
- **When** the available statuses are displayed
- **Then** the system provides defined statuses such as Not Started, In Progress, and Ready for Consideration

#### Scenario 3 – Resource Manager Views Readiness

- **Given** the employee has updated the readiness status
- **When** an authorized Resource Manager reviews the employee
- **Then** the latest readiness status is displayed

---

## US-06 – Create and Publish Project Opportunity

**Priority:** Must Have

### User Story

> As a Project Manager, I want to create and publish an upcoming project with its required skills so that employees can view the opportunity and prepare in advance.

### Acceptance Criteria

#### Scenario 1 – Create Project

- **Given** the Project Manager is authorized to create project opportunities
- **When** the Project Manager enters the required project information
- **Then** the system allows the project to be saved

#### Scenario 2 – Missing Mandatory Information

- **Given** one or more mandatory fields are missing
- **When** the Project Manager selects Publish
- **Then** the system prevents publication and identifies the missing information

#### Scenario 3 – Publish Project

- **Given** all mandatory project information is complete
- **When** the Project Manager selects Publish
- **Then** the project becomes visible to eligible employees

---

## US-07 – View Interested Employees

**Priority:** Must Have

### User Story

> As a Resource Manager, I want to view employees who have active interest in a project so that I can evaluate potential candidates for further consideration.

### Acceptance Criteria

#### Scenario 1 – View Interested Employees

- **Given** employees have expressed interest in a project
- **When** an authorized Resource Manager opens the project
- **Then** the system displays employees with active interest

#### Scenario 2 – View Employee Details

- **Given** an interested employee is displayed
- **When** the Resource Manager opens the employee details
- **Then** the system displays authorized skill, experience, and readiness information

#### Scenario 3 – Withdrawn Interest

- **Given** an employee has withdrawn interest
- **When** the Resource Manager views the active-interest list
- **Then** the employee is not displayed in the active-interest list

#### Scenario 4 – Unauthorized Access

- **Given** a user is not authorized to view staffing information
- **When** the user attempts to access interested employee details
- **Then** the system denies access

---

## US-08 – Update Project Requirements

**Priority:** Should Have

### User Story

> As an authorized Project or Resource Manager, I want to update project requirements when project needs change so that employees and Resource Managers have current project information.

### Acceptance Criteria

#### Scenario 1 – Update Requirements

- **Given** an authorized user opens a published project
- **When** the user changes an allowed project requirement
- **Then** the system saves and displays the latest requirement

#### Scenario 2 – Update Start Date

- **Given** an authorized user changes the project start date
- **When** the change is saved
- **Then** the updated date is displayed wherever the project information is shown

#### Scenario 3 – Notify Affected Employees

- **Given** an important requirement or start-date change is made
- **When** the change is published
- **Then** employees with active interest receive a notification

#### Scenario 4 – Unauthorized Modification

- **Given** the user is not authorized to edit the project
- **When** the user attempts to modify project requirements
- **Then** the system prevents the modification

---

## US-09 – Receive Project Notifications

**Priority:** Should Have

### User Story

> As an employee who has active interest in a project, I want to receive notifications about important project updates so that I can stay informed about changes that may affect my preparation or interest.

### Acceptance Criteria

#### Scenario 1 – Requirement Change Notification

- **Given** the employee has active interest in a project
- **When** an important project requirement changes
- **Then** the employee receives a notification describing the change

#### Scenario 2 – Start-Date Change Notification

- **Given** the employee has active interest in a project
- **When** the project start date changes
- **Then** the employee receives a notification containing the updated date

#### Scenario 3 – Employee Without Active Interest

- **Given** the employee does not have active interest in the project
- **When** the project is updated
- **Then** the employee does not receive an interest-specific notification

---
