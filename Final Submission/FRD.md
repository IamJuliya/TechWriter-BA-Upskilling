# Functional Requirements Document (FRD)

## Contents


## 1. Introduction

**Document Note**

This FRD is prepared in aligning with the corresponding Business Requirements Document.

The functional requirements describe the expected system behaviour. Items requiring confirmation, including data sources, technical feasibility, performance targets, privacy permissions and pending business policies, are identified as dependencies or open questions rather than assumed implementation decisions.

### 1.1 Purpose

This Functional Requirements Document defines the expected system behaviour for enhancing the existing ThinkPalm Employee Management Portal to support project opportunity publishing, employee interest management, resource evaluation, skill-gap identification, learning support and staffing visibility.

It translates the business requirements and business rules defined in the BRD into functional specifications that can guide solution development, functional testing and user acceptance testing.

### 1.2 Project Overview

The proposed enhancement will enable Project Managers to publish upcoming project opportunities with required skills and timelines. Eligible employees can view opportunities, compare their recorded skills with project requirements, identify skill gaps and express interest.

Resource Managers will evaluate employee suitability, availability and readiness before making staffing decisions. Learning and Development will support employees in addressing identified skill gaps through learning and assessment activities.

The portal will provide management with visibility into resource availability, opportunity status, staffing outcomes and learning progress.

The solution will support effective utilization of existing resources before external recruitment is considered. It will not automatically allocate employees to projects.

### 1.3 Scope of the FRD

This document covers:

- Project opportunity creation, publication, modification and closure.
- Employee eligibility verification and opportunity visibility.
- Skill comparison and skill-gap identification.
- Expression and withdrawal of interest.
- Resource Manager review and staffing decisions.
- Shortlisting and waitlisting.
- Learning, assessment, retries and certification.
- Notifications and status tracking.
- Management dashboards and reporting.
- Role-based access, privacy, auditability and data integrity.
- Non-functional requirements and data migration/integration considerations.

---

## 2. User Roles

| Role | Functional Responsibility |
|---|---|
| Management | View business-level dashboards, resource utilization and staffing outcomes. |
| Project Manager (PM) | Create, update and publish project opportunities and define skill requirements. |
| Resource Manager (RM) | Review interested employees, assess suitability and availability, manage shortlists and waitlists, and confirm staffing decisions. |
| Employee | View eligible opportunities, compare skills, identify gaps, express interest and withdraw interest where permitted. |
| Learning and Development (L&D) | Manage learning activities, assessments, retries and certification records. |
| Portal Administrator | Maintain authorized portal configurations, role access and supporting administration functions. |

---

## 3. Functional Requirements

### 3.1 Project Opportunity Management

**FR-01: Create Project Opportunity**

The system shall allow authorized Project Managers to create project opportunities by entering the project name, role, description, project duration, expected start date, required experience and other approved project details.

**FR-02: Define Required Skills**

The system shall allow Project Managers to specify mandatory and preferred skills for each opportunity.

Mandatory skills shall be distinguishable from preferred skills during employee skill comparison and Resource Manager evaluation.

**FR-03: Publish Opportunity**

The system shall allow authorized Project Managers to publish an opportunity only after all mandatory information has been provided and validated.

The system shall make published opportunities available to eligible employees according to the configured visibility rules.

**FR-04: Update Opportunity Details**

The system shall allow authorized Project Managers to modify published opportunity details, including skills, dates and other relevant information.

When a material change affects employees who have already expressed interest, the system shall notify the affected employees and the Resource Manager.

The system shall retain the previous and updated values in the audit history.

**FR-05: Close or Cancel Opportunity**

The system shall allow authorized users to close or cancel an opportunity based on their assigned permissions.

Once an opportunity is closed or cancelled, the system shall prevent new expressions of interest.

The system shall update the opportunity status and notify affected users where applicable.

### 3.2 Employee Opportunity Access and Eligibility

**FR-06: View Eligible Opportunities**

The system shall display active and published opportunities to employees who meet the approved eligibility conditions.

The system shall not display opportunities that are closed, cancelled or otherwise unavailable to the employee.

**FR-07: Compare Employee Skills**

The system shall compare the employee's recorded skills with the mandatory and preferred skills defined for the selected opportunity.

The comparison shall clearly distinguish:

- Matching skills.
- Missing mandatory skills.
- Missing preferred skills.
- Skills requiring verification, where applicable.

**FR-08: Identify Skill Gaps**

The system shall identify skill gaps based on the difference between the employee's recorded skills and the opportunity's required skills.

The system shall distinguish between a confirmed skill gap and missing or incomplete employee skill information.

Missing skill data shall not automatically be treated as proof that an employee lacks the skill.

**FR-09: Express Interest in an Opportunity**

The system shall allow an eligible employee to express interest in an active opportunity before its closing date.

Before accepting the submission, the system shall:

1. Verify the employee's eligibility.
2. Check the employee's employment and notice-period status using the approved data source.
3. Verify that the opportunity is active and open for interest.
4. Check that the employee has not already submitted an active expression of interest for the same opportunity.
5. Validate the required submission details.

The system shall prevent submission if the employee is serving a notice period.

An appropriate validation message shall be displayed when an employee is not eligible to express interest.

The system shall record the submission date and time and update the employee's interest status.

**FR-10: Withdraw Expression of Interest**

The system shall allow an employee to withdraw an existing expression of interest where withdrawal is permitted by the approved business process.

The system shall update the interest status and record the withdrawal date and time.

The Resource Manager shall be notified when an employee withdraws interest.

**FR-11: Update Employee Readiness Information**

The system shall maintain the employee's readiness information based on approved availability details, skill information and learning or assessment outcomes.

Only authorized users or approved system processes shall be permitted to update relevant employee readiness information.

Changes shall be recorded in the audit history.

### 3.3 Resource Manager Review and Staffing

**FR-12: View Interested Employees**

The system shall allow authorized Resource Managers to view employees who have expressed interest in their assigned opportunities.

The system shall display relevant information, including employee availability, recorded skills, skill comparison results, interest status and readiness information.

**FR-13: Review Employee Information**

The system shall allow Resource Managers to review employee information relevant to the staffing decision.

Access to personal and employment information shall be restricted according to the assigned role permissions and approved data-visibility rules.

**FR-14: Record Suitability and Readiness Assessment**

The system shall allow Resource Managers to record the suitability and readiness assessment for an employee.

The assessment shall support consideration of:

- Mandatory skill requirements.
- Preferred skills.
- Relevant experience.
- Employee availability.
- Skill verification status.
- Project start-date requirements.
- Learning or assessment progress, where relevant.

The system shall retain the assessment details and the identity of the authorized user making the update.

**FR-15: Manage Shortlist and Waitlist**

The system shall allow authorized Resource Managers to move employees into appropriate review statuses, including Shortlisted, Waitlisted and Not Selected.

The system shall retain the reason for a decision where required by the approved process.

A shortlisted or waitlisted status shall not automatically constitute project allocation.

**FR-16: Support Unfilled Opportunity Handling**

The system shall provide Resource Managers with visibility into opportunities that remain unfilled after internal resource review.

The system shall support recording the outcome of the internal resource review and the decision to consider external recruitment, subject to the applicable recruitment policy.

The system shall not initiate or manage the complete external recruitment process.

**FR-17: Confirm Staffing Decision**

The system shall allow only authorized Resource Managers or their approved delegates to record the final staffing decision.

The system shall update the employee's staffing status and the opportunity status as appropriate.

The system shall maintain the decision history and notify affected users.

Expression of interest, shortlisting and waitlisting shall not be treated as final allocation.

### 3.4 Learning and Development

**FR-18: Use Skill-Gap Information**

The system shall make relevant skill-gap information available to authorized L&D users to support learning and development activities.

**FR-19: Manage Learning Enrolment**

The system shall allow authorized L&D users to record or manage employee enrolment in relevant learning activities based on identified skill gaps.

Course details and enrolment status shall be maintained in the system.

**FR-20: Record Course Completion and Assessment**

The system shall allow authorized L&D users or approved integrated processes to record course completion and assessment results.

The system shall support assessment statuses such as Not Started, In Progress, Passed and Failed.

**FR-21: Manage Assessment Retries**

The system shall support assessment retry tracking based on the retry limit and rules configured by L&D.

The system shall record the number of attempts, assessment outcomes and retry eligibility.

The system shall prevent further attempts when the configured retry limit has been reached.

**FR-22: Record Certification and Update Skill Profile**

The system shall allow authorized L&D users or approved processes to record certification outcomes and update the employee's skill profile following successful completion of the applicable assessment and certification requirements.

The system shall maintain the certification details and skill profile update history.

Course completion alone shall not automatically result in certification or a verified skill update.

**FR-23: Support Training Planning**

The system shall provide authorized L&D users with visibility into aggregated skill-gap information to support training planning.

The system shall allow skill-gap information to be reviewed by relevant skill, project requirement or other approved reporting criteria.

### 3.5 Notifications and Management Reporting

**FR-24: Notify Affected Users**

The system shall generate notifications for relevant workflow events, including:

- New opportunities published.
- Material changes to published opportunities.
- Opportunity closure or cancellation.
- Successful expression of interest.
- Withdrawal of interest.
- Resource Manager review and staffing status changes.
- Waitlisting, shortlisting and selection decisions.
- Learning enrolment and assessment updates.
- Certification and skill profile updates.
- Other approved workflow events.

Notifications shall be sent to the appropriate users based on their role and involvement in the workflow.

The notification channel and delivery mechanism shall be based on the available portal capabilities and approved notification configuration.

**FR-25: Provide Management Dashboards**

The system shall provide authorized Management users with dashboards and reports covering:

- Published, active, closed and unfilled opportunities.
- Employee interest and participation.
- Employee availability and readiness.
- Shortlisted, waitlisted and selected employees.
- Internal staffing outcomes.
- Identified skill gaps.
- Learning enrolment, assessment and certification outcomes.
- Relevant resource utilization indicators.

The dashboard shall display information according to the user's access permissions.

---

## 4. Business Rules and System Enforcement

The business policies are defined in the BRD. This section specifies how the portal shall enforce the relevant rules.

| Business Rule Reference | Business Rule | System Enforcement |
|---|---|---|
| BRL-01 | Employees serving a notice period cannot express interest in internal project opportunities. | Verify notice-period status before accepting an expression of interest and block ineligible submissions. |
| BRL-02 | Only employees meeting approved eligibility conditions may participate. | Validate employee eligibility before displaying or accepting interest in an opportunity. |
| BRL-03 | Employee availability must meet approved requirements. | Capture and present availability information for Resource Manager review. |
| BRL-04 | Internal resources must be considered before external recruitment. | Provide internal resource review information and record the outcome before external recruitment consideration. |
| BRL-05 | Final staffing decisions must be made by authorized Resource Managers or delegates. | Restrict staffing decision actions to authorized roles. |
| BRL-06 | Employee suitability must be evaluated against relevant project requirements. | Present skill, experience and availability information for Resource Manager assessment. |
| BRL-07 | Suitable employees who are not immediately ready or available may be waitlisted, subject to approval. | Allow authorized Resource Managers to assign and track Waitlisted status. |
| BRL-08 | Mandatory and preferred skills must be treated differently. | Display separate comparison results for mandatory and preferred skills. |
| BRL-09 | Skill verification must follow approved validation procedures. | Maintain verification status and restrict skill updates to authorized users or processes. |
| BRL-10 | Assessment attempts and certification must follow L&D policy. | Enforce configured assessment and retry rules and maintain certification records. |
| BRL-11 | Course completion or assessment participation does not guarantee staffing. | Maintain learning and staffing statuses separately. |
| BRL-12 | Changes in employee eligibility after interest submission must be handled according to approved policy. | Provide updated employee status visibility and support authorized review. The automatic handling of existing interest remains subject to policy confirmation. |
| BRL-13 | Employee personal information must only be accessed for authorized business purposes. | Apply role-based access and restrict personal data visibility. |
| BRL-14 | Financial benefits must be based on agreed definitions and validated baselines. | Provide reportable operational data; financial benefit calculations must use approved definitions and validated data. |

---

## 5. Field and Workflow Validations

### 5.1 Project Opportunity Validations

| Validation ID | Validation Description | Expected System Behaviour |
|---|---|---|
| VAL-01 | Project name is mandatory. | Prevent saving or publishing without a project name. |
| VAL-02 | Role or resource requirement is mandatory. | Prevent publication if the role information is missing. |
| VAL-03 | Project start and end dates must be valid. | Prevent invalid date ranges. |
| VAL-04 | At least one required skill must be specified. | Prevent publication if the approved skill requirement is missing. |
| VAL-05 | Mandatory and preferred skills must be distinguishable. | Display the two skill categories separately. |
| VAL-06 | Only authorized Project Managers can publish opportunities. | Deny publication attempts from unauthorized users. |
| VAL-07 | Closed or cancelled opportunities cannot accept new interest. | Disable or reject new submissions. |

### 5.2 Employee Interest Validations

| Validation ID | Validation Description | Expected System Behaviour |
|---|---|---|
| VAL-08 | Employee must meet approved eligibility conditions. | Prevent interest submission when eligibility criteria are not met. |
| VAL-09 | Employee must not be serving a notice period. | Block submission and display an appropriate message. |
| VAL-10 | Opportunity must be active and open. | Reject submissions for closed, cancelled or expired opportunities. |
| VAL-11 | Duplicate active interest is not permitted. | Prevent duplicate submissions for the same opportunity. |
| VAL-12 | Required submission details must be provided. | Highlight missing mandatory information. |
| VAL-13 | Employee withdrawal must follow the permitted workflow. | Update the interest status only when withdrawal is allowed. |
| VAL-14 | Employment eligibility may change after submission. | Make the updated status available for authorized review; subsequent action follows the approved policy. |

### 5.3 Resource Manager and L&D Validations

| Validation ID | Validation Description | Expected System Behaviour |
|---|---|---|
| VAL-15 | Only authorized Resource Managers can update staffing decisions. | Restrict decision actions to authorized users. |
| VAL-16 | Shortlisting and waitlisting are not final allocation. | Maintain separate workflow statuses. |
| VAL-17 | Assessment attempts must follow configured retry limits. | Prevent attempts beyond the permitted limit. |
| VAL-18 | Certification requires approved completion criteria. | Prevent certification from being recorded without the required outcome. |
| VAL-19 | Skill profile updates must be authorized. | Restrict updates to authorized L&D users or approved processes. |
| VAL-20 | Personal data access must follow role permissions. | Restrict unauthorized viewing and modification. |

---

## 6. Workflow Status Definitions

### 6.1 Opportunity Status

| Status | Description |
|---|---|
| Draft | Opportunity created but not published. |
| Published | Opportunity made available to eligible employees. |
| Active | Opportunity is open for employee interest and review. |
| Closed | Opportunity is no longer accepting interest. |
| Cancelled | Opportunity withdrawn from the process. |

### 6.2 Employee Interest and Staffing Status

| Status | Description |
|---|---|
| Interested | Employee has successfully expressed interest. |
| Withdrawn | Employee has withdrawn their interest. |
| Under Review | Resource Manager is evaluating the employee. |
| Shortlisted | Employee has been shortlisted for further consideration. |
| Waitlisted | Employee is retained for possible future consideration. |
| Selected | Employee has been selected through the authorized staffing process. |
| Not Selected | Employee has not been selected for the opportunity. |

### 6.3 Learning Status

| Status | Description |
|---|---|
| Not Started | Learning activity has not started. |
| Enrolled | Employee has been enrolled in the learning activity. |
| In Progress | Learning activity is underway. |
| Assessment Failed | Employee did not meet the assessment criteria. |
| Passed | Employee has met the assessment criteria. |
| Certified | Required certification has been completed and recorded. |
| Retry Limit Reached | The configured maximum number of assessment attempts has been reached. |

---

## 7. Notification Requirements

| Notification ID | Trigger Event | Intended Recipient |
|---|---|---|
| NOT-01 | New opportunity published | Eligible employees |
| NOT-02 | Material opportunity details changed | Employees who expressed interest and relevant RM |
| NOT-03 | Employee expresses interest | Relevant RM and employee |
| NOT-04 | Employee withdraws interest | Relevant RM |
| NOT-05 | Employee shortlisted or waitlisted | Employee and relevant RM |
| NOT-06 | Employee selected or not selected | Employee and relevant RM |
| NOT-07 | Opportunity closed or cancelled | Affected employees and relevant RM |
| NOT-08 | Learning enrolment created or updated | Employee and relevant L&D user |
| NOT-09 | Assessment result recorded | Employee and relevant L&D user |
| NOT-10 | Certification or skill profile updated | Employee and relevant authorized users |

Notification delivery failures should be logged where supported by the portal's notification mechanism.

The specific notification channels, templates and delivery timelines are subject to stakeholder confirmation.

---

## 8. Data Requirements and Migration Considerations

### 8.1 Key Data Entities

| Data Entity | Relevant Information |
|---|---|
| Employee | Employee identifier, employment status, role, department and approved availability information. |
| Employee Skills | Skill name, proficiency or experience level, verification status and last updated date. |
| Employment Eligibility | Employment status, notice-period status and relevant effective dates. |
| Project Opportunity | Project name, role, description, dates, status and project requirements. |
| Opportunity Skills | Mandatory skills, preferred skills and experience requirements. |
| Employee Interest | Employee identifier, opportunity identifier, submission date, withdrawal date and status. |
| Resource Assessment | Suitability, readiness, availability and decision details. |
| Learning Records | Course details, enrolment, completion and assessment outcomes. |
| Certification | Certification status, issue date and supporting details. |
| Notifications | Event type, recipient, delivery status and timestamp. |
| Audit Records | User, action, date/time and relevant record changes. |

### 8.2 Existing Data Assessment

The enhancement shall assess the availability, quality and reliability of existing employee and skill information before it is reused.

The assessment shall consider:

- Existing employee records and their authoritative source.
- Accuracy and completeness of employee skill profiles.
- Availability and reliability of employment and notice-period status.
- Duplicate employee or skill records.
- Outdated or inconsistent information.
- Existing portal modules or external systems that maintain relevant data.

### 8.3 Data Migration and Integration Requirements

The solution shall support reuse, migration or integration of existing employee and skill information based on the approved technical approach.

The data migration or integration process shall address:

1. Identification of authoritative source systems.
2. Mapping of existing data fields to the enhanced portal.
3. Data-quality checks before migration or synchronization.
4. Identification and handling of duplicate or incomplete records.
5. Validation of migrated or synchronized records.
6. Handling of failed or incomplete data transfers.
7. Access controls and protection of personal information.
8. Reconciliation of source and target records.

The decision to migrate data, reuse existing portal records or integrate with another source system remains subject to technical assessment and stakeholder approval.

### 8.4 Notice-Period Data Dependency

The system requires reliable and sufficiently current employment and notice-period information to enforce the restriction defined in BRL-01.

The authoritative source, synchronization frequency and handling of unavailable or outdated status information must be confirmed before implementation.

The system must not assume that an employee is eligible merely because notice-period information is unavailable.

The final exception-handling behaviour for unavailable or stale employment data is subject to business and technical approval.

---

## 9. Non-Functional Requirements

| NFR ID | Category | Requirement |
|---|---|---|
| NFR-01 | Access Control | The system shall enforce role-based access so users can access only the functions and information permitted for their roles. |
| NFR-02 | Privacy and Security | Employee personal information shall be protected against unauthorized access, disclosure or modification. |
| NFR-03 | Data Integrity | The system shall maintain accurate and consistent employee, skill, opportunity and staffing records. |
| NFR-04 | Auditability | The system shall record relevant user actions, status changes and updates with user identity and timestamps. |
| NFR-05 | Usability | The portal shall provide clear navigation, understandable status labels and meaningful validation messages. |
| NFR-06 | Performance | Common user operations and reports shall meet response-time targets agreed during solution design and stakeholder review. |
| NFR-07 | Scalability | The solution shall support the expected growth in employees, opportunities, skill records and concurrent users. |
| NFR-08 | Availability and Recovery | The solution shall meet agreed availability, backup and recovery expectations. |
| NFR-09 | Compatibility | The portal shall support the approved browsers, devices and operating environments. |
| NFR-10 | Maintainability | The solution shall support future updates to business rules, skill categories, workflows and configurations without unnecessary disruption. |
| NFR-11 | Data Protection | Data transfer, storage, retention and access shall follow approved organizational security and privacy requirements. |
| NFR-12 | Notification Reliability | The system shall record notification outcomes where supported and provide visibility into delivery failures. |

### 9.1 Performance and Capacity Considerations

The following parameters require confirmation during solution design:

- Expected number of employees using the portal.
- Expected concurrent users during opportunity publication and application periods.
- Expected number of active opportunities.
- Expected volume of employee skill records and interest submissions.
- Acceptable response time for common transactions.
- Acceptable report generation time.
- Expected data growth and retention requirements.

The BA specification records these as business and operational needs. Technical architecture, infrastructure sizing and implementation decisions remain within the technical solution design.

### 9.2 Platform and Compatibility Considerations

The solution shall be assessed for compatibility with the browsers, desktop environments and mobile access requirements approved by the organization.

The final supported platform list shall be confirmed during technical and stakeholder review.

---

## 10. Exception and Error Handling

| Exception ID | Scenario | Expected System Behaviour |
|---|---|---|
| EX-01 | Mandatory opportunity information is missing. | Prevent publication and identify missing fields. |
| EX-02 | Employee attempts to express interest in a closed opportunity. | Reject submission and display an appropriate message. |
| EX-03 | Employee serving notice attempts to express interest. | Block submission and display an eligibility message. |
| EX-04 | Employee submits duplicate interest. | Prevent duplicate active submission. |
| EX-05 | Employee skill information is incomplete. | Identify missing information separately from confirmed skill gaps. |
| EX-06 | Opportunity details change after employee interest submission. | Notify affected users and retain the change history. |
| EX-07 | Employee withdraws interest. | Update the status and notify the relevant Resource Manager. |
| EX-08 | No suitable internal employee is identified. | Allow the Resource Manager to record the internal review outcome and external recruitment consideration. |
| EX-09 | Employee is waitlisted. | Maintain Waitlisted status without treating it as final allocation. |
| EX-10 | Assessment retry limit is reached. | Prevent further attempts and update the learning status. |
| EX-11 | Assessment is passed but certification is pending. | Do not mark the employee as Certified until certification requirements are met. |
| EX-12 | Unauthorized user attempts a restricted action. | Deny access and record the event where audit logging is supported. |
| EX-13 | Employee employment or notice-period status changes after interest submission. | Make the updated status available for authorized review; subsequent action follows the approved policy. |
| EX-14 | Employee or skill data is unavailable or fails synchronization. | Record the data issue and follow the approved exception-handling process. |
| EX-15 | Notification delivery fails. | Record the failure where supported and make it available for monitoring. |

---

## 11. Functional Acceptance Criteria

The following acceptance criteria define the expected outcomes for the principal functional workflows.

| AC ID | Related FR | Acceptance Criteria |
|---|---|---|
| AC-01 | FR-01 to FR-03 | Given an authorized Project Manager, when all mandatory opportunity details and skill requirements are entered, then the system shall allow the opportunity to be published. |
| AC-02 | FR-03 | Given an opportunity with missing mandatory information, when the Project Manager attempts to publish it, then the system shall prevent publication and identify the missing information. |
| AC-03 | FR-06 | Given an eligible employee, when the employee opens the opportunities page, then the system shall display active opportunities available to that employee. |
| AC-04 | FR-07 | Given an employee and an opportunity with defined skills, when the employee views the skill comparison, then mandatory and preferred skill matches shall be displayed separately. |
| AC-05 | FR-08 | Given incomplete employee skill information, when the employee views the skill comparison, then missing information shall not automatically be classified as a confirmed skill gap. |
| AC-06 | FR-09 | Given an eligible employee who is not serving a notice period, when the employee submits interest in an active opportunity, then the system shall accept the submission and record the interest status. |
| AC-07 | FR-09 | Given an employee who is serving a notice period, when the employee attempts to express interest, then the system shall block the submission and display an appropriate eligibility message. |
| AC-08 | FR-09 | Given an employee who has already expressed active interest in an opportunity, when the employee attempts to submit again, then the system shall prevent duplicate active interest. |
| AC-09 | FR-10 | Given an employee with an existing expression of interest, when withdrawal is permitted and the employee withdraws, then the system shall update the status and notify the relevant Resource Manager. |
| AC-10 | FR-12 to FR-14 | Given a Resource Manager with the required permissions, when the manager opens an opportunity, then the system shall display relevant interested employee information and allow the assessment to be recorded. |
| AC-11 | FR-15 | Given a suitable employee who is not immediately ready or available, when the Resource Manager approves waitlisting, then the system shall record Waitlisted status without marking the employee as allocated. |
| AC-12 | FR-16 | Given an opportunity without a suitable internal resource, when the Resource Manager completes the internal review, then the system shall allow the review outcome and external recruitment consideration to be recorded. |
| AC-13 | FR-17 | Given an authorized Resource Manager, when a final staffing decision is recorded, then the system shall update the relevant staffing status and retain the decision history. |
| AC-14 | FR-19 to FR-22 | Given an employee enrolled in a learning activity, when course and assessment outcomes are recorded, then the system shall maintain the learning status and enforce the configured retry limit. |
| AC-15 | FR-22 | Given an employee who meets the approved certification requirements, when an authorized user records certification, then the system shall update the certification and skill profile records. |
| AC-16 | FR-24 | Given a configured workflow event, when the event occurs, then the system shall generate a notification for the appropriate recipient. |
| AC-17 | FR-25 | Given an authorized Management user, when the dashboard is accessed, then the system shall display the approved staffing, opportunity and learning indicators. |
| AC-18 | FR-13, FR-25 | Given a user without permission to view restricted employee information, when the user attempts to access that information, then the system shall deny access. |
| AC-19 | FR-04, FR-05 | Given a published opportunity, when authorized changes or closure occur, then the system shall update the status and retain relevant change history. |
| AC-20 | FR-09, FR-11 | Given an employee's eligibility status changes after interest submission, when the updated status becomes available, then the system shall make it available for authorized review without assuming an unapproved automatic withdrawal policy. |

---

## 12. Functional Testing Considerations

Functional testing shall verify that the system meets the requirements and acceptance criteria defined in this document.

Testing shall include:

### 12.1 Positive Testing

- Authorized Project Manager successfully creates and publishes an opportunity.
- Eligible employee views an available opportunity.
- Employee successfully compares skills and expresses interest.
- Employee withdraws interest where permitted.
- Resource Manager records suitability and staffing decisions.
- L&D records course completion and assessment outcomes.
- Management views authorized dashboard information.

### 12.2 Negative Testing

- Unauthorized user attempts to publish an opportunity.
- Employee serving a notice period attempts to express interest.
- Employee attempts to submit duplicate interest.
- Employee attempts to express interest in a closed opportunity.
- User attempts an action outside their role permissions.
- Assessment retry exceeds the configured limit.
- Certification is attempted without meeting the approved criteria.

### 12.3 Boundary and Exception Testing

- Opportunity closing date and submission timing.
- Project start-date and employee availability combinations.
- Missing, incomplete or outdated skill records.
- Changes to project requirements after interest submission.
- Changes to employee eligibility after interest submission.
- Unavailable employment or notice-period data.
- Failed data migration or synchronization.
- Notification delivery failure.

### 12.4 Regression Testing

When an existing workflow, business rule or data structure is changed, related functional test cases shall be reviewed to identify potential regression impacts.

The bidirectional Requirements Traceability Matrix shall be used to identify affected requirements, functional modules and test cases.

---

## 13. Dependencies and Assumptions

### 13.1 Dependencies

- Availability of reliable employee and skill information.
- Availability of authoritative employment and notice-period status.
- Approved employee eligibility policies.
- Defined Project Manager and Resource Manager permissions.
- Availability of learning courses and assessment information.
- Approved certification and assessment retry rules.
- Availability of portal notification capabilities.
- Availability of existing portal data and integration interfaces.
- Agreement on management reporting definitions and metrics.

### 13.2 Assumptions

- The existing Employee Management Portal can be enhanced, subject to technical feasibility.
- The portal can support the required role-based access controls.
- Existing employee and skill data can be reused, migrated or integrated after assessment.
- Resource Managers retain authority over final staffing decisions.
- L&D retains authority over learning, assessment and certification policies.
- Management defines the criteria for considering external recruitment.
- Financial benefits will be calculated using validated organizational data and agreed definitions.

---

## 14. Risks and Mitigation Considerations

| Risk ID | Risk | Mitigation Consideration |
|---|---|---|
| RISK-01 | Employee skill profiles may be incomplete or outdated. | Assess data quality and establish an authorized update and verification process. |
| RISK-02 | Notice-period information may be unavailable or outdated. | Identify the authoritative source and establish a reliable synchronization mechanism. |
| RISK-03 | Employees may not receive relevant notifications. | Define notification events, recipients and delivery monitoring. |
| RISK-04 | Unauthorized access may expose employee personal information. | Apply role-based access, privacy controls and audit logging. |
| RISK-05 | Data migration may introduce duplicate or inconsistent records. | Perform data profiling, mapping, validation and reconciliation. |
| RISK-06 | Unclear staffing and waitlist rules may lead to inconsistent decisions. | Obtain approval for decision criteria and workflow rules. |
| RISK-07 | Learning and certification timelines may not align with project requirements. | Provide readiness and learning-status visibility to Resource Managers. |
| RISK-08 | Performance may be affected as users and records increase. | Confirm expected user volumes and establish measurable performance targets. |

---

## 15. Open Questions and Pending Decisions

| OQ ID | Open Question | Related Area |
|---|---|---|
| OQ-01 | What is the authoritative source for employee employment and notice-period status? | Eligibility |
| OQ-02 | How frequently should employment and notice-period information be synchronized or refreshed? | Data integration |
| OQ-03 | What should happen when an employee enters a notice period after expressing interest: automatic withdrawal or Resource Manager review? | Eligibility workflow |
| OQ-04 | What should the portal do when employment or notice-period data is unavailable or outdated? | Validation and exception handling |
| OQ-05 | What additional employee eligibility conditions apply beyond the notice-period restriction? | Eligibility |
| OQ-06 | Which employee personal information may be viewed by each role? | Privacy and access |
| OQ-07 | Which notification channels should be supported? | Notifications |
| OQ-08 | What are the approved assessment retry limits and certification criteria? | L&D |
| OQ-09 | Which system or portal module is the authoritative source for employee skills? | Data integration |
| OQ-10 | What data migration, synchronization or integration approach is technically feasible? | Data migration |
| OQ-11 | What are the expected user volumes, concurrency levels and performance targets? | Non-functional requirements |
| OQ-12 | Which browsers, devices and mobile access options must be supported? | Compatibility |
| OQ-13 | What data retention and audit-history periods are required? | Privacy and auditability |
| OQ-14 | What are the approved management dashboard definitions and reporting periods? | Reporting |
| OQ-15 | What notification delivery and failure-handling expectations apply? | Notifications |

---

## 16. Requirements Traceability

The FRD shall be maintained in alignment with the BRD and the Requirements Traceability Matrix.

Each functional requirement shall be traceable to its originating business requirement and relevant business rule. Functional test cases shall be linked to the corresponding functional requirements and acceptance criteria.

The RTM shall support bidirectional traceability so that:

- Each business requirement can be traced to its functional implementation and verification.
- Each functional requirement can be traced to its business justification.
- Each test case can be traced to the requirement it verifies.
- Changes to requirements can be assessed for their impact on related functional requirements and regression test cases.

---

## 17. Approval

| Role | Name | Approval Status |
|---|---|---|
| Business Sponsor / Management | To be confirmed | Pending |
| Resource Management Representative | To be confirmed | Pending |
| Learning and Development Representative | To be confirmed | Pending |
| Business Analyst | Mary Juliya | Prepared |
