# User Stories and Acceptance Criteria
## Project Opportunities & Talent Readiness Enhancement

| Document Detail | Information |
|---|---|
| Organization | ThinkPalm (Case-Study Scenario) |
| Prepared By | Mary Juliya |
| Role | Business Analyst |
| Version | 1.0 |
| Status | Proposed for Stakeholder Review |
| Date | 13 November 2026 |
| Related Documents | Business Case v1.0, BRD v2.1, FRD v2.0 |

---

## 1. Purpose

This document translates the business and functional requirements for the Project Opportunities & Talent Readiness Enhancement into user stories and testable acceptance criteria.

The stories describe the needs of Project Managers, Employees, Resource Managers, Learning and Development (L&D), and Management. They provide a common understanding for solution development, functional testing, requirements traceability and User Acceptance Testing (UAT).

The stories are aligned with the Capstone BRD and FRD. They cover the complete proposed workflow, including opportunity management, employee interest, staffing review, learning support, notifications and management reporting.

## 2. Scope

The user stories cover:

- Project opportunity creation, publication, update and closure.
- Employee opportunity discovery and skill comparison.
- Employee eligibility checks, expression of interest and withdrawal.
- Resource Manager review, suitability assessment and staffing decisions.
- Skill-gap identification and L&D learning support.
- Course completion, assessments, retries, certification and skill-profile updates.
- Notifications and management dashboards.
- Access control, data privacy, validation and auditability.

**Important business boundary:** Expressing interest or being shortlisted does not mean an employee has been allocated to a project. The final staffing decision remains with the authorized Resource Manager.

## 3. User Stories and Acceptance Criteria

### 3.1 Project Opportunity Management

#### US-01: Create a Project Opportunity

**As a** Project Manager,  
**I want** to create a project opportunity with project details and resource requirements,  
**So that** upcoming resource demand can be recorded and made available for review.

**Acceptance Criteria**

1. **Given** an authorized Project Manager is logged in, **when** they open the opportunity creation option, **then** the system allows them to enter the required opportunity details.
2. **Given** the Project Manager enters the mandatory project information, **when** they save the opportunity, **then** the system validates the information and saves the opportunity in Draft status.
3. **Given** one or more mandatory fields are missing or invalid, **when** the Project Manager attempts to save, **then** the system identifies the relevant fields and prevents an invalid record from being saved.
4. **Given** an unauthorized user attempts to create an opportunity, **when** they access the restricted action, **then** the system denies access.

**Related FRs:** FR-01, FR-02

#### US-02: Define Required Skills

**As a** Project Manager,  
**I want** to specify mandatory and preferred skills for an opportunity,  
**So that** employees and Resource Managers can assess suitability against the project requirements.

**Acceptance Criteria**

1. **Given** the Project Manager is creating or editing an opportunity, **when** they add required skills, **then** the system allows them to identify each skill as mandatory or preferred.
2. **Given** the opportunity requires at least one mandatory skill, **when** the Project Manager attempts to publish without defining the required skill information, **then** the system prevents publication.
3. **Given** skills have been defined, **when** the opportunity is saved, **then** the system retains the skill requirements against the opportunity.
4. **Given** the Project Manager enters invalid or duplicate skill information, **when** they save the details, **then** the system applies the configured validation rules.

**Related FRs:** FR-01, FR-02

#### US-03: Publish a Project Opportunity

**As a** Project Manager,  
**I want** to publish a completed project opportunity,  
**So that** eligible employees can discover and review it.

**Acceptance Criteria**

1. **Given** all mandatory opportunity details and required skills are available, **when** an authorized Project Manager publishes the opportunity, **then** the system changes its status to Published or Active according to the defined workflow.
2. **Given** an opportunity is published, **when** an eligible employee views available opportunities, **then** the published opportunity is displayed with its relevant details.
3. **Given** mandatory information is incomplete, **when** the Project Manager attempts to publish, **then** the system prevents publication and identifies the missing information.
4. **Given** an unauthorized user attempts to publish an opportunity, **when** they submit the action, **then** the system denies the action.

**Related FRs:** FR-03

#### US-04: Update or Close a Project Opportunity

**As a** Project Manager,  
**I want** to update, close or cancel an opportunity,  
**So that** employees and Resource Managers work with current project information.

**Acceptance Criteria**

1. **Given** an authorized Project Manager owns or is permitted to manage an opportunity, **when** they update its permitted details, **then** the system saves the changes and records the update.
2. **Given** an opportunity has been closed or cancelled, **when** an employee attempts to express interest, **then** the system prevents the action.
3. **Given** an opportunity has employees who have already expressed interest, **when** its material details or status change, **then** the system follows the configured notification rules.
4. **Given** a user does not have permission to manage the opportunity, **when** they attempt to update or close it, **then** the system denies the action.

**Related FRs:** FR-04, FR-05, FR-24

### 3.2 Employee Opportunity Access and Interest

#### US-05: View Available Project Opportunities

**As an** Employee,  
**I want** to view published project opportunities relevant to me,  
**So that** I can understand upcoming internal project requirements.

**Acceptance Criteria**

1. **Given** an employee is logged in, **when** they open the opportunities section, **then** the system displays published opportunities that the employee is authorized and eligible to view.
2. **Given** an opportunity is displayed, **when** the employee opens its details, **then** the system shows relevant information such as project description, required skills, dates and expected duration.
3. **Given** an opportunity is Draft, Closed or Cancelled, **when** the employee views available opportunities, **then** the system does not present it as open for interest.
4. **Given** an employee is not authorized to view restricted employee or project information, **when** they access the relevant information, **then** the system restricts access.

**Related FRs:** FR-06

#### US-06: Compare Required Skills with Recorded Skills

**As an** Employee,  
**I want** to compare my recorded skills with the skills required for an opportunity,  
**So that** I can understand my suitability and identify possible skill gaps.

**Acceptance Criteria**

1. **Given** an employee opens an opportunity, **when** they select the skill comparison option, **then** the system compares the opportunity requirements with the employee's recorded skills.
2. **Given** the employee has matching skills, **when** the comparison is displayed, **then** the system identifies the matching skills.
3. **Given** one or more required skills are not present in the employee profile, **when** the comparison is displayed, **then** the system identifies the missing skills.
4. **Given** the employee profile contains incomplete or outdated skill information, **when** the comparison is performed, **then** the system indicates the data limitation rather than presenting unverified information as confirmed.

**Related FRs:** FR-07, FR-08

#### US-07: Express Interest in a Project Opportunity

**As an** eligible Employee,  
**I want** to express interest in an available project opportunity,  
**So that** the Resource Manager can consider me during the staffing review.

**Acceptance Criteria**

1. **Given** an employee is eligible, is not serving a notice period, and the opportunity is open for interest, **when** they submit an expression of interest, **then** the system records the interest and displays a confirmation.
2. **Given** an employee is serving a notice period, **when** they attempt to express interest, **then** the system blocks the action and displays an appropriate explanation.
3. **Given** an employee has already expressed interest in the same opportunity, **when** they attempt to submit another expression of interest, **then** the system prevents duplicate active submissions.
4. **Given** an opportunity is closed or cancelled, **when** an employee attempts to express interest, **then** the system prevents the submission.
5. **Given** the authoritative notice-period or eligibility information is unavailable or cannot be verified, **when** an employee attempts to express interest, **then** the system follows the approved exception-handling rule and does not treat unverified eligibility as confirmed.

**Related FRs:** FR-09

**Applicable Business Rule:** BRL-01 — An employee serving a notice period is not eligible to express interest in any internal project opportunity.

#### US-08: Withdraw an Expression of Interest

**As an** Employee,  
**I want** to withdraw my expression of interest,  
**So that** I can indicate that I am no longer available or interested in the opportunity.

**Acceptance Criteria**

1. **Given** an employee has an active expression of interest, **when** they select the withdrawal option and confirm the action, **then** the system changes the interest status to Withdrawn.
2. **Given** an employee withdraws interest, **when** the action is completed, **then** the system records the withdrawal and applies the configured notification rules.
3. **Given** an employee has no active expression of interest, **when** they attempt to withdraw interest, **then** the system prevents an invalid withdrawal.
4. **Given** the staffing process has reached a status where withdrawal is restricted, **when** the employee attempts to withdraw, **then** the system applies the approved withdrawal policy and displays the outcome.

**Related FRs:** FR-10, FR-24

#### US-09: Update Employee Readiness Information

**As an** Employee,  
**I want** to view and update permitted readiness and skill information,  
**So that** Resource Managers can consider current information during staffing reviews.

**Acceptance Criteria**

1. **Given** an employee is authorized to update permitted profile information, **when** they submit valid updates, **then** the system saves the information according to the applicable data ownership and validation rules.
2. **Given** an employee attempts to modify a restricted or verified skill record, **when** they submit the change, **then** the system prevents unauthorized modification.
3. **Given** readiness or availability information changes, **when** the update is accepted, **then** the system records the change and makes the updated information available to authorized reviewers.
4. **Given** required information is missing or invalid, **when** the employee submits the update, **then** the system identifies the validation issue.

**Related FRs:** FR-11

### 3.3 Resource Manager Review and Staffing

#### US-10: View Employees Interested in an Opportunity

**As a** Resource Manager,  
**I want** to view employees who have expressed interest in an opportunity,  
**So that** I can review potential internal candidates.

**Acceptance Criteria**

1. **Given** an opportunity has received expressions of interest, **when** an authorized Resource Manager opens its staffing view, **then** the system displays the associated employee records.
2. **Given** an employee has withdrawn interest, **when** the Resource Manager views the active candidate list, **then** the withdrawn record is clearly identified and is not treated as an active expression of interest.
3. **Given** the Resource Manager does not have access to a particular employee record, **when** they attempt to view restricted information, **then** the system denies access.
4. **Given** the opportunity has no expressions of interest, **when** the Resource Manager opens its staffing view, **then** the system displays an appropriate empty-state message.

**Related FRs:** FR-12

#### US-11: Review Employee Information

**As a** Resource Manager,  
**I want** to review relevant employee skills, experience, readiness and availability,  
**So that** I can assess the employee against the opportunity requirements.

**Acceptance Criteria**

1. **Given** an employee has expressed interest, **when** the Resource Manager opens the employee's review record, **then** the system displays authorized information relevant to the opportunity.
2. **Given** the employee's recorded skills are available, **when** the Resource Manager reviews the profile, **then** the system displays the recorded skill information and its available verification status.
3. **Given** information is missing, outdated or awaiting verification, **when** the Resource Manager reviews the record, **then** the system indicates the relevant data limitation.
4. **Given** the Resource Manager is not authorized to view personal or restricted employee information, **when** they access the record, **then** the system restricts that information.

**Related FRs:** FR-13

#### US-12: Record Suitability and Readiness Assessment

**As a** Resource Manager,  
**I want** to record an employee's suitability and readiness assessment,  
**So that** staffing decisions are based on documented and relevant information.

**Acceptance Criteria**

1. **Given** an employee has expressed interest, **when** the Resource Manager completes the review, **then** the system allows the authorized Resource Manager to record the assessment outcome.
2. **Given** the assessment is submitted, **when** the record is saved, **then** the system retains the assessment outcome and relevant comments or rationale.
3. **Given** mandatory assessment information is missing, **when** the Resource Manager attempts to submit the assessment, **then** the system identifies the missing information and prevents incomplete submission.
4. **Given** an unauthorized user attempts to record or modify the assessment, **when** they submit the action, **then** the system denies it.

**Related FRs:** FR-14

#### US-13: Manage Shortlist and Waitlist

**As a** Resource Manager,  
**I want** to shortlist or waitlist employees based on suitability, readiness and availability,  
**So that** potential candidates can be managed transparently while outstanding conditions are addressed.

**Acceptance Criteria**

1. **Given** an employee meets the approved suitability criteria, **when** the Resource Manager shortlists the employee, **then** the system records the Shortlisted status.
2. **Given** an employee is suitable but is not ready or available by the required date, **when** the Resource Manager selects the waitlist option, **then** the system records the Waitlisted status and the applicable reason.
3. **Given** an employee's readiness or availability changes, **when** the Resource Manager reassesses the employee, **then** the system allows the authorized status to be updated.
4. **Given** a status change affects an employee or another workflow participant, **when** the change is saved, **then** the system applies the configured notification rules.

**Related FRs:** FR-15, FR-24

#### US-14: Handle an Opportunity Without a Suitable Internal Candidate

**As a** Resource Manager,  
**I want** to record the outcome when no suitable internal candidate is available,  
**So that** the opportunity can proceed through the approved staffing or external recruitment process.

**Acceptance Criteria**

1. **Given** the Resource Manager has reviewed the available internal candidates, **when** no suitable candidate is identified, **then** the system allows the Resource Manager to record the unfilled opportunity outcome.
2. **Given** an opportunity remains unfilled, **when** the Resource Manager records the outcome, **then** the system retains the reason and relevant review information.
3. **Given** internal staffing has been reviewed, **when** an external recruitment request is considered, **then** the system follows the approved recruitment policy and does not initiate recruitment automatically.
4. **Given** the opportunity's staffing status changes, **when** the outcome is saved, **then** the system updates the status and applies the configured notifications.

**Related FRs:** FR-16, FR-24

#### US-15: Confirm the Staffing Decision

**As an** authorized Resource Manager,  
**I want** to record the final staffing decision,  
**So that** the outcome of the internal resource review is formally documented.

**Acceptance Criteria**

1. **Given** the employee review is complete, **when** the authorized Resource Manager records a staffing decision, **then** the system saves the decision against the opportunity and employee record.
2. **Given** a staffing decision is recorded, **when** the record is saved, **then** the system updates the relevant staffing status and retains the decision details.
3. **Given** an unauthorized user attempts to confirm or modify a staffing decision, **when** they submit the action, **then** the system denies it.
4. **Given** a decision is recorded, **when** affected users view their authorized records, **then** they see the applicable status and notification.

**Related FRs:** FR-17, FR-24

### 3.4 Learning and Development

#### US-16: Identify Learning Support for Skill Gaps

**As an** L&D Representative,  
**I want** to review identified employee skill gaps,  
**So that** relevant learning support can be considered.

**Acceptance Criteria**

1. **Given** a skill gap has been identified during an employee's opportunity review, **when** an authorized L&D Representative views the learning support information, **then** the system displays the relevant employee and skill-gap details.
2. **Given** a skill gap is identified, **when** suitable learning options are available, **then** the system allows the L&D Representative to associate relevant learning support.
3. **Given** no suitable learning option is available, **when** the L&D Representative reviews the gap, **then** the system allows the gap to be recorded for follow-up.
4. **Given** the L&D Representative does not have permission to access the employee's learning information, **when** they attempt to view it, **then** the system denies access.

**Related FRs:** FR-18, FR-23

#### US-17: Manage Learning Enrolment

**As an** L&D Representative,  
**I want** to record an employee's enrolment in an approved learning course,  
**So that** learning progress can be tracked against identified skill gaps.

**Acceptance Criteria**

1. **Given** a learning option is approved and relevant to an identified skill gap, **when** the L&D Representative enrols an employee, **then** the system records the enrolment.
2. **Given** an employee is enrolled, **when** the learning record is viewed, **then** the system displays the course and enrolment status.
3. **Given** an invalid or unavailable course is selected, **when** the L&D Representative submits the enrolment, **then** the system prevents the invalid record from being saved.
4. **Given** enrolment is recorded, **when** the configured notification event occurs, **then** the relevant employee and authorized participants are notified.

**Related FRs:** FR-19, FR-24

#### US-18: Record Course Completion and Assessment Results

**As an** L&D Representative,  
**I want** to record course completion and assessment results,  
**So that** employee learning progress and assessment outcomes are available for review.

**Acceptance Criteria**

1. **Given** an employee has enrolled in a course, **when** the L&D Representative records course completion, **then** the system updates the learning record.
2. **Given** an assessment has been completed, **when** the authorized L&D Representative records the result, **then** the system stores the outcome, score where applicable, date and attempt information.
3. **Given** an assessment has not been passed, **when** the result is recorded, **then** the system retains the unsuccessful outcome and displays the applicable next step.
4. **Given** an assessment result is recorded, **when** the result is relevant to a staffing review, **then** the system makes it available to authorized reviewers according to access rules.

**Related FRs:** FR-20, FR-24

#### US-19: Manage Assessment Retries

**As an** L&D Representative,  
**I want** the system to enforce the approved assessment retry limit,  
**So that** assessment attempts are controlled and consistently recorded.

**Acceptance Criteria**

1. **Given** an employee has not reached the permitted attempt limit, **when** another assessment attempt is authorized, **then** the system allows the attempt and records it.
2. **Given** an employee has reached the configured attempt limit, **when** they attempt another assessment, **then** the system prevents further attempts.
3. **Given** the attempt limit has been reached without a passing result, **when** the learning record is reviewed, **then** the system identifies that L&D follow-up is required.
4. **Given** the approved retry policy changes, **when** the configured limit is updated by an authorized role, **then** the system applies the approved limit to the applicable assessment process.

**Related FRs:** FR-21

#### US-20: Record Certification and Update Skill Profile

**As an** authorized L&D Representative,  
**I want** to record certification evidence and update verified skill information,  
**So that** employee skill profiles reflect validated learning outcomes.

**Acceptance Criteria**

1. **Given** an employee meets the approved certification criteria, **when** the authorized L&D Representative records the certification, **then** the system stores the certification details and supporting evidence as applicable.
2. **Given** a skill has been successfully validated, **when** an authorized user updates the employee skill profile, **then** the system records the updated skill information and verification status.
3. **Given** an assessment is passed but certification or skill validation is still pending, **when** the employee profile is viewed, **then** the system does not present the skill as verified.
4. **Given** an unauthorized user attempts to update a verified skill record, **when** they submit the change, **then** the system prevents the update.

**Related FRs:** FR-22

### 3.5 Notifications and Management Reporting

#### US-21: Receive Workflow Notifications

**As a** workflow participant,  
**I want** to receive notifications when an event requires my attention,  
**So that** I can take the necessary action without depending only on manual follow-up.

**Acceptance Criteria**

1. **Given** a configured workflow event occurs, **when** the event is successfully recorded, **then** the system generates a notification for the applicable recipient or recipients.
2. **Given** an employee expresses or withdraws interest, **when** the action is completed, **then** the system notifies the relevant Resource Manager according to the configured notification rules.
3. **Given** a learning result or certification is recorded, **when** the result requires staffing review, **then** the system notifies the authorized Resource Manager.
4. **Given** an opportunity is updated, closed or cancelled, **when** the change affects interested employees, **then** the system notifies the affected users according to the configured rules.
5. **Given** a notification cannot be delivered, **when** the delivery failure is detected, **then** the system handles the failure according to the approved notification reliability and retry policy.

**Related FRs:** FR-24

#### US-22: View Management Dashboard

**As a** Management Representative,  
**I want** to view consolidated information about opportunities, available talent, staffing outcomes and learning progress,  
**So that** I can monitor internal resource utilization and support informed workforce decisions.

**Acceptance Criteria**

1. **Given** an authorized Management Representative opens the dashboard, **when** the dashboard loads, **then** the system displays the approved management-level metrics and summaries.
2. **Given** opportunity and staffing records are available, **when** the dashboard is viewed, **then** it displays relevant information such as published opportunities, employee interest, staffing outcomes and unfilled opportunities.
3. **Given** learning records are available, **when** the dashboard is viewed, **then** it displays approved learning and assessment summaries.
4. **Given** a user does not have permission to view employee-level personal information, **when** they access the dashboard, **then** the system displays only the information permitted for their role.
5. **Given** dashboard data is incomplete or has not been refreshed, **when** the dashboard is displayed, **then** the system indicates the applicable data status or reporting period.

**Related FRs:** FR-25

## 4. Cross-Functional Acceptance Conditions

The following conditions apply across the relevant user stories and must be considered during functional testing and UAT.

| ID | Acceptance Condition | Applicable Areas |
|---|---|---|
| CAC-01 | Users can perform actions only when their assigned role and permissions allow them to do so. | All roles |
| CAC-02 | Employees serving a notice period cannot express interest in internal project opportunities. | Employee interest |
| CAC-03 | The system must not treat unavailable or unverified eligibility data as confirmed eligibility. | Employee interest |
| CAC-04 | Employee personal information must be visible only to authorized roles and for approved business purposes. | Employee and RM review |
| CAC-05 | Mandatory fields and configured business validations must be enforced before a transaction is saved or submitted. | Opportunity, interest, assessment and staffing |
| CAC-06 | Material status changes must be recorded with sufficient audit information to support traceability. | Opportunity, interest, staffing and learning |
| CAC-07 | An employee's expression of interest, shortlist or learning completion must not automatically result in project allocation. | Staffing |
| CAC-08 | Staffing decisions must be recorded by an authorized Resource Manager or approved delegate. | Staffing |
| CAC-09 | Notifications must follow configured event, recipient and delivery rules. | All workflow participants |
| CAC-10 | The system must retain the distinction between mandatory and preferred skills when displaying or assessing skill matches. | Opportunity and skill comparison |
| CAC-11 | Verified skill information must be updated only by authorized users using approved validation evidence. | Learning and employee profile |
| CAC-12 | Dashboard information must respect role-based access and approved data visibility rules. | Management reporting |

## 5. Business Rules Referenced by the User Stories

The following business rules govern the stories and are not separate system features.

| Business Rule ID | Business Rule |
|---|---|
| BRL-01 | An employee serving a notice period is not eligible to express interest in any internal project opportunity. |
| BRL-02 | Only employees meeting the approved eligibility conditions may participate in the opportunity process. |
| BRL-03 | Employee availability must satisfy the approved requirements for the proposed project start date. |
| BRL-04 | Internal resource availability must be reviewed before external recruitment is considered, subject to the approved recruitment policy. |
| BRL-05 | Final staffing decisions remain with the authorized Resource Manager or approved delegate. |
| BRL-06 | Suitability must be assessed against mandatory project requirements, relevant experience, verified skills and availability. |
| BRL-07 | A suitable employee who is not currently ready or available may be waitlisted, subject to the approved review process. |
| BRL-08 | Mandatory and preferred skills must be treated distinctly during skill comparison and suitability assessment. |
| BRL-09 | Skill verification must follow approved evidence and authorization procedures. |
| BRL-10 | Assessment pass criteria, permitted attempts and certification requirements must follow the approved L&D policy. |
| BRL-11 | Course completion or assessment success does not guarantee project staffing or allocation. |
| BRL-12 | If an employee's eligibility changes after expressing interest, continued participation must be assessed according to the approved policy. |
| BRL-13 | Employee personal information must be used and accessed only for authorized business purposes. |
| BRL-14 | Financial benefits and success measures must use agreed definitions and validated baseline information. |

## 6. Story-to-Functional Requirement Mapping

This mapping connects each user story to the corresponding FRD requirement IDs. It supports development planning and bidirectional requirements traceability.

| User Story | Related Functional Requirements |
|---|---|
| US-01 | FR-01, FR-02 |
| US-02 | FR-01, FR-02 |
| US-03 | FR-03 |
| US-04 | FR-04, FR-05, FR-24 |
| US-05 | FR-06 |
| US-06 | FR-07, FR-08 |
| US-07 | FR-09 |
| US-08 | FR-10, FR-24 |
| US-09 | FR-11 |
| US-10 | FR-12 |
| US-11 | FR-13 |
| US-12 | FR-14 |
| US-13 | FR-15, FR-24 |
| US-14 | FR-16, FR-24 |
| US-15 | FR-17, FR-24 |
| US-16 | FR-18, FR-23 |
| US-17 | FR-19, FR-24 |
| US-18 | FR-20, FR-24 |
| US-19 | FR-21 |
| US-20 | FR-22 |
| US-21 | FR-24 |
| US-22 | FR-25 |

## 7. Dependencies and Assumptions

1. Employee employment status, including notice-period status, must be available from an approved authoritative data source.
2. The source, ownership and update frequency of employee skill and availability information must be confirmed.
3. Employee eligibility conditions beyond the confirmed notice-period restriction require stakeholder approval.
4. Project Managers, Resource Managers, Employees, L&D and Management must have approved role-based access.
5. Assessment criteria, retry limits and certification requirements must be defined by the authorized L&D function.
6. Notification recipients, triggers, delivery channels and failure-handling rules must be confirmed.
7. The proposed stories assume that the existing Employee Management Portal can be enhanced to support the required workflow, subject to technical feasibility.
8. Data migration, integration and data-quality requirements must be confirmed before implementation.

## 8. Out of Scope

The following capabilities are not included in these user stories:

- Automatic employee allocation to projects.
- Automatic approval of staffing decisions.
- Automated external recruitment or candidate selection.
- Salary, promotion or performance appraisal management.
- Automatic assignment of training without the approved L&D process.
- Replacement of the organization's existing Learning Management System.
- Full workforce capacity planning beyond the defined opportunity and staffing workflow.

## 9. Traceability and Testing Notes

- Each user story is linked to one or more functional requirements in the FRD.
- Acceptance criteria are written in Given/When/Then format to support functional test-case preparation.
- Positive, negative, boundary, authorization and exception scenarios must be considered when deriving functional test cases.
- The notice-period restriction must have a dedicated negative test case, along with a positive test confirming that an otherwise eligible employee who is not serving notice can express interest.
- Changes to business rules or functional requirements must be assessed for their impact on related stories, acceptance criteria and regression test cases.
- The RTM must maintain both forward and backward traceability between business requirements, functional requirements, user stories and test cases.

## 10. Document Status

This document represents the proposed Capstone user stories and acceptance criteria for the ThinkPalm case-study solution. Business rules, data dependencies, eligibility conditions, workflow policies and acceptance criteria remain subject to stakeholder validation.

**End of Document**
