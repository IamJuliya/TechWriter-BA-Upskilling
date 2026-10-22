# Lab 1 – Requirements Elicitation & User Story Writing

## 1. Project Title

Enhancement of Employee Management Portal – Project Opportunities & Talent Readiness

## 2. Business Problem Statement

The organization has an existing Employee Management System that provides various employee and HR-related services. However, employees who are temporarily unallocated may have limited visibility into upcoming project opportunities and the skills required for those projects.
Project and Resource Managers also need a structured way to communicate upcoming project requirements and identify employees whose skills and interests may align with those requirements.
The proposed enhancement will introduce a Project Opportunities & Talent Readiness feature within the existing Employee Management System. It will allow authorized users to publish upcoming project requirements, while employees can view opportunities, identify skill gaps, express interest, and update their preparation status.

## 3. Mock Stakeholder Interview

Stakeholder: Resource/Staffing Manager
BA: How are upcoming project requirements currently communicated to employees?
Stakeholder: They are generally communicated through internal channels and discussions. Employees may not always get early visibility.
BA: What information should employees see about an upcoming project?
Stakeholder: Project name, description, expected start date, duration, required skills, and experience requirements.
BA: How do you currently identify suitable employees?
Stakeholder: We review employee skills and experience against project requirements and coordinate with managers.
BA: What if an employee has some but not all required skills?
Stakeholder: If there is sufficient time, the employee can work on the missing skills before the project starts.
BA: Should employees be able to express interest in a project?
Stakeholder: Yes.
BA: Should expressing interest automatically assign the employee to the project?
Stakeholder: No. Final allocation requires management evaluation.
BA: Should employees be able to update their preparation status?
Stakeholder: Yes. This would help us understand their readiness.
BA: Who should create and publish project requirements?
Stakeholder: Authorized Project or Resource Management users.
BA: What information would Resource Managers need when reviewing interested employees?
Stakeholder: Relevant skills, experience, availability, and preparation/readiness status.

## 4. BRD Skeleton 
## Project Title

**Project Opportunities & Talent Readiness Enhancement**

## Business Problem

Employees who are temporarily unallocated have limited visibility into upcoming project opportunities and required skills. Resource Managers also need a structured way to identify potentially suitable employees.

## Business Objective

Enhance the existing Employee Management System to provide visibility into upcoming projects, required skills, employee skill gaps, and employee interest/readiness.

## Proposed Solution

Introduce a **Project Opportunities & Talent Readiness** feature that allows authorized users to publish project requirements and employees to review opportunities, identify skill gaps, express interest, and update readiness.

## Key Stakeholders

- Employees
- Project Managers
- Resource/Staffing Managers
- Learning & Development
- System Administrator

## In Scope

- Create and publish upcoming projects
- Define required skills
- View project opportunities
- View skill requirements
- Identify employee skill gaps
- Express interest in projects
- Update readiness/preparation status
- View interested employees

## Out of Scope

- Automatic project allocation
- Salary or promotion decisions
- Performance appraisal
- Recruitment decisions
- Actual training delivery

## Success Criteria

- Employees can view upcoming opportunities and required skills.
- Employees can identify their skill gaps.
- Employees can express interest and update readiness.
- Resource Managers can view interested employees and relevant information.
- Authorized users can maintain project requirements.

# User Stories & Acceptance Criteria

## US-01 – View Upcoming Projects

**User Story:**

As an **employee**, I want to **view upcoming project opportunities** so that **I can identify projects that match my skills and interests.**

**Acceptance Criteria:**

- Published projects are visible to employees.
- Project name and description are displayed.
- Expected start date is displayed.

## US-02 – View Required Skills

**User Story:**

As an **employee**, I want to **view the skills required for a project** so that **I can understand the capabilities needed.**

**Acceptance Criteria:**

- Required skills are displayed.
- Mandatory and preferred skills are identified.
- Experience requirements are displayed where applicable.

## US-03 – Identify Skill Gaps

**User Story:**

As an **employee**, I want to **compare my skills with project requirements** so that **I can identify my skill gaps.**

**Acceptance Criteria:**

- Existing employee skills are compared with project requirements.
- Matching skills are displayed.
- Missing or insufficient skills are highlighted.

## US-04 – Express Interest

**User Story:**

As an **employee**, I want to **express interest in an upcoming project** so that **the Resource Manager can consider me for the opportunity.**

**Acceptance Criteria:**

- An **Express Interest** option is available.
- Interest is recorded.
- A confirmation is displayed.
- Interest does not automatically assign the employee to the project.

## US-05 – Update Readiness

**User Story:**

As an **employee**, I want to **update my preparation status** so that **the Resource Manager can understand my readiness.**

**Acceptance Criteria:**

- Employee can update preparation status.
- Current status is visible to authorized Resource Managers.
- Employee can update the status as preparation progresses.

## US-06 – Define Project Requirements

**User Story:**

As a **Project Manager**, I want to **define the skills required for an upcoming project** so that **the required talent capabilities are clearly communicated.**

**Acceptance Criteria:**

- Authorized users can create project information.
- Required skills can be added.
- Skills can be identified as mandatory or preferred.
- Expected start date can be specified.

## US-07 – Publish Project

**User Story:**

As a **Project Manager**, I want to **publish upcoming project requirements** so that **employees can view the opportunity and prepare in advance.**

**Acceptance Criteria:**

- Authorized users can publish projects.
- Required information must be completed before publishing.
- Published projects are visible to employees.

## US-08 – View Interested Employees

**User Story:**

As a **Resource Manager**, I want to **view employees who expressed interest in a project** so that **I can identify potential candidates for further evaluation.**

**Acceptance Criteria:**

- Interested employees are displayed.
- Relevant skills and experience are displayed.
- Readiness status is displayed.
- Access is restricted to authorized users.

## US-09 – Review Employee Skills

**User Story:**

As a **Resource Manager**, I want to **view employee skills and preparation status** so that **I can evaluate potential candidates against project requirements.**

**Acceptance Criteria:**

- Relevant employee skills are displayed.
- Relevant experience is displayed.
- Preparation status is displayed.
- Project requirements can be viewed during evaluation.

## US-10 – Update Project Requirements

**User Story:**

As an **authorized user**, I want to **update project requirements when project needs change** so that **employees and Resource Managers have current information.**

**Acceptance Criteria:**

- Authorized users can edit requirements.
- Changes are saved.
- Updated requirements are displayed to employees.
- Unauthorized users cannot modify requirements.
