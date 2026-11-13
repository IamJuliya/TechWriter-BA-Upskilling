# Functional Requirements Document (FRD)
## Project Opportunities & Talent Readiness Enhancement

**Organization:** ThinkPalm (Case Study)  
**Prepared by:** Mary Juliya  
**Role:** Business Analyst  
**Version:** 2.0  
**Status:** Proposed for Stakeholder Review  
**Date:** 12 November 2026  
**Reference Document:** Business Requirements Document (BRD), Version 2.1

---

## 1. Purpose

This Functional Requirements Document defines the system behaviour required to enhance the existing ThinkPalm Employee Management Portal for project opportunity management and talent readiness.

It translates the business requirements into functional requirements, validations, workflows, acceptance criteria, and non-functional requirements.

The solution will help employees discover relevant internal project opportunities, allow Resource Managers to assess employee suitability and availability, and support Learning and Development activities to address identified skill gaps.

The portal will support staffing decisions but will not independently allocate employees to projects.

## 2. Project Overview

The proposed enhancement introduces a structured workflow for managing internal project opportunities and employee readiness.

The system will allow:

- Project Managers to create, update and publish project opportunities.
- Employees to view eligible opportunities, compare their skills against project requirements, identify skill gaps and express or withdraw interest.
- Resource Managers to review employee interest, assess suitability and availability, and manage shortlists and waitlists.
- Learning and Development to manage relevant learning activities, assessments, retries and certification.
- Management to review project staffing outcomes, resource availability and learning-related information.
- Authorized users to access information and perform actions according to their assigned roles.

## 3. Scope

### 3.1 In Scope

- Create, update, publish, close and cancel project opportunities.
- Define mandatory and preferred project skills.
- Display relevant opportunities to eligible employees.
- Compare employee skills with project requirements.
- Identify and display skill gaps.
- Validate employee eligibility before accepting interest.
- Prevent employees serving a notice period from expressing interest.
- Allow eligible employees to express and withdraw interest.
- Review employee suitability, readiness and availability.
- Manage shortlisted and waitlisted employees.
- Support learning, assessment, retry and certification workflows.
- Update employee skill profiles through authorized actions.
- Confirm staffing decisions through authorized Resource Managers.
- Notify affected users about relevant workflow changes.
- Provide management dashboards and reports.
- Support role-based access, privacy and auditability.
- Support the assessment of existing employee and skill data for migration, integration or reuse.

### 3.2 Out of Scope

- Automatic employee allocation without Resource Manager authorization.
- Complete recruitment and onboarding management.
- Salary, promotion and performance appraisal processes.
- Automatic assignment of training without the required business approval.
- Full workforce capacity planning.
- Replacement of the existing HR or employee management system.
- Guaranteed recruitment cost savings or financial benefits.

## 4. User Roles

| Role | Responsibilities within the system |
|---|---|
| Management | Review business outcomes, staffing information and management reports. |
| Project Manager (PM) | Create and manage project opportunities and define required skills. |
| Resource Manager (RM) | Review employee interest, assess suitability and availability, manage shortlists and confirm staffing decisions. |
| Employee | View eligible opportunities, compare skills, express or withdraw interest and participate in learning activities. |
| Learning & Development (L&D) | Manage learning activities, assessments, retries and certification. |
| Portal Administrator | Manage authorized portal configuration, roles and access-related administration. |

## 5. Functional Requirements

### 5.1 Project Opportunity Management

**FR-01: Create Project Opportunity**

The system shall allow authorized Project Managers to create project opportunities by entering the required project information.

The opportunity details shall include, at a minimum:

- Project name or title.
- Project description.
- Required role or position.
- Proposed start date.
- Expected duration, where applicable.
- Required skills.
- Opportunity closing date.
- Relevant project eligibility information.

**FR-02: Define Required Skills**

The system shall allow Project Managers to define mandatory and preferred skills for each project opportunity.

The system shall maintain a clear distinction between mandatory and preferred skills.

**FR-03: Publish Opportunity**

The system shall allow authorized Project Managers to publish an opportunity after all mandatory information and validation checks are completed.

Only published and active opportunities shall be displayed to eligible employees.

**FR-04: Update Opportunity Details**

The system shall allow authorized Project Managers to update published opportunity details, including skills, dates and role requirements.

When a material change affects employees who have already expressed interest, the system shall notify the affected employees and relevant Resource Manager.

The system shall retain the updated opportunity information and its relevant change history.

**FR-05: Close or Cancel Opportunity**

The system shall allow authorized Project Managers to close or cancel an opportunity.

Once closed or cancelled, the system shall prevent new expressions of interest.

The system shall retain the opportunity status and notify affected users where applicable.

### 5.2 Employee Opportunity Discovery and Interest

**FR-06: View Eligible Opportunities**

The system shall display active project opportunities to employees who meet the approved eligibility conditions.

Employees shall be able to view the relevant opportunity details, including required skills, project dates and role information.

**FR-07: Compare Employee Skills**

The system shall compare an employee's recorded skills with the mandatory and preferred skills defined for an opportunity.

The comparison shall clearly identify:

- Skills that match the project requirements.
- Skills that are not currently recorded in the employee profile.
- Preferred skills that are available or missing.

The system shall use the available employee skill-profile information for comparison.

**FR-08: Identify Skill Gaps**

The system shall identify and display the difference between the employee's recorded skills and the opportunity's required skills.

Missing or unverified skill information shall not automatically be treated as proof that the employee lacks the skill.

**FR-09: Express Interest in Opportunity**

The system shall allow an eligible employee to express interest in an active project opportunity.

Before accepting the submission, the system shall validate the employee's eligibility, including the notice-period restriction defined in BRL-01.

The system shall:

- Verify that the opportunity is active and within its submission period.
- Verify that the employee is not serving a notice period.
- Prevent duplicate active expressions of interest for the same opportunity.
- Record the employee's interest and submission date.
- Capture the proposed availability date, where required.
- Display a confirmation after successful submission.

If the employee is serving a notice period, the system shall reject the submission and display an appropriate explanation.

**FR-10: Withdraw Interest**

The system shall allow employees to withdraw previously submitted interest, subject to the approved withdrawal policy and applicable workflow status.

The system shall record the withdrawal and notify the Resource Manager.

**FR-11: Update Employee Readiness Information**

The system shall display the employee's current readiness information based on available skill, learning and assessment records.

The system shall reflect authorized updates to employee skill and certification information.

The system shall not independently classify an employee as project-ready solely because a course has been completed.

### 5.3 Resource Manager Review and Staffing

**FR-12: View Interested Employees**

The system shall allow authorized Resource Managers to view employees who have expressed interest in their assigned project opportunities.

The displayed information shall include relevant employee skills, availability, readiness and interest status, subject to role-based access restrictions.

**FR-13: Review Candidate Information**

The system shall allow Resource Managers to review relevant employee information for staffing assessment.

The information shall include:

- Employee skill profile.
- Mandatory and preferred skill comparison.
- Identified skill gaps.
- Relevant experience, where recorded and authorized for use.
- Proposed availability date.
- Readiness and learning status.
- Interest submission status.

Personal information not required for staffing decisions shall not be displayed unnecessarily.

**FR-14: Record Suitability and Readiness**

The system shall allow authorized Resource Managers to record their assessment of employee suitability and readiness for a project opportunity.

The assessment shall support the review of skills, availability, experience and identified skill gaps.

The system shall retain the assessment outcome and relevant status history.

**FR-15: Manage Shortlist and Waitlist**

The system shall allow authorized Resource Managers to shortlist or waitlist employees based on their assessment.

The system shall distinguish between:

- Shortlisted employees.
- Waitlisted employees.
- Employees under review.
- Employees not selected.

Shortlisting or waitlisting shall not be treated as final project allocation.

The system shall allow authorized users to update the status based on subsequent readiness and availability reviews.

**FR-16: Handle Unfilled Opportunities**

The system shall provide Resource Managers with visibility into opportunities that do not have suitable or available internal candidates.

The system shall support recording the outcome of the internal resource review and the decision to proceed with external recruitment consideration.

The system shall not initiate or manage the complete external recruitment process.

**FR-17: Confirm Staffing Decision**

The system shall allow authorized Resource Managers to record the final staffing decision.

The system shall update the employee's project staffing status and the opportunity's staffing information after the decision is confirmed.

The system shall retain the decision history and notify the affected users.

Final staffing confirmation shall require authorized human approval.

### 5.4 Learning and Development

**FR-18: Use Skill-Gap Information**

The system shall make relevant skill-gap information available to authorized L&D users for learning support and planning.

L&D users shall be able to review identified skill gaps and relevant employee readiness information.

**FR-19: Manage Learning Activities**

The system shall allow authorized L&D users to associate relevant learning activities or courses with identified skill gaps.

The system shall maintain the relationship between the employee, learning activity and relevant skill requirement.

**FR-20: Record Course Completion and Assessment**

The system shall allow authorized L&D users to record course completion and assessment outcomes.

The system shall maintain relevant learning statuses and assessment results.

**FR-21: Manage Assessment Retry**

The system shall support recording assessment attempts and retry outcomes according to the approved L&D assessment policy.

The system shall apply the configured retry limit and prevent further attempts when the permitted limit has been reached.

**FR-22: Record Certification and Update Skill Profile**

The system shall allow authorized L&D users or other designated authorized users to record certification outcomes and update employee skill profiles based on approved evidence.

The system shall retain the certification and skill-update history.

Course completion alone shall not automatically establish certification unless the applicable assessment and certification requirements have been met.

**FR-23: Support Learning Planning**

The system shall provide authorized L&D users with aggregated skill-gap information to support learning planning and identify recurring training needs.

### 5.5 Notifications and Management Reporting

**FR-24: Notify Affected Users**

The system shall generate notifications when relevant workflow events occur.

Notifications shall be generated for applicable events, including:

- Opportunity publication.
- Material changes to an opportunity.
- Opportunity closure or cancellation.
- Successful expression of interest.
- Withdrawal of interest.
- Shortlisting or waitlisting.
- Changes to employee readiness or assessment outcomes, where relevant.
- Final staffing decisions.
- Relevant learning and certification updates.

Notifications shall be directed to the appropriate users based on the event and their role.

The notification channel and delivery configuration shall be confirmed during solution design.

**FR-25: Management Dashboards**

The system shall provide authorized Management users with dashboards and reports covering relevant information, including:

- Published, active, closed and cancelled opportunities.
- Employee interest and participation.
- Shortlisted, waitlisted and selected employees.
- Internal staffing outcomes.
- Available employee skills and readiness.
- Identified skill gaps.
- Learning participation and assessment outcomes.
- Opportunities requiring further staffing action.

The system shall restrict dashboard information according to authorized access levels.

### 5.6 Employee and Skill Data Integration

**FR-26: Employee and Skill Data Integration or Migration**

The solution shall support the reuse, integration or migration of relevant employee and skill information from approved existing data sources.

Before data is used in the enhanced portal, the solution shall support validation of:

- Employee identity and active employment status.
- Notice-period status.
- Employee role and organizational information required for the workflow.
- Recorded skills and relevant proficiency information, where available.
- Certification and learning records, where applicable.
- Duplicate, incomplete, outdated or inconsistent records.

The selected approach—reuse, integration or migration—shall depend on the availability, quality, ownership and accessibility of the existing data.

The solution shall maintain data integrity and prevent unauthorized or incomplete updates from being treated as verified employee information.

## 6. Business Rule Enforcement

The system shall enforce the business rules defined in the BRD.

| Rule ID | Business rule | Related system behaviour |
|---|---|---|
| BRL-01 | Employees serving a notice period are not eligible to express interest in internal project opportunities. | Validate notice-period status before accepting an expression of interest and block ineligible submissions. |
| BRL-02 | Only employees meeting approved eligibility conditions may participate. | Validate applicable eligibility conditions before accepting interest. |
| BRL-03 | Employees must meet approved availability requirements for the proposed project start date. | Display availability information and support RM review. |
| BRL-04 | Internal resources must be considered before external recruitment. | Provide internal staffing review information and record the outcome before external recruitment consideration. |
| BRL-05 | Final staffing decisions must be made by an authorized RM or delegate. | Restrict staffing confirmation to authorized users. |
| BRL-06 | Suitability must be assessed against mandatory requirements, experience, verified skills and availability. | Present relevant information to support RM assessment. |
| BRL-07 | Waitlisting is subject to RM approval and applicable timelines. | Allow authorized RM users to manage waitlist status. |
| BRL-08 | Mandatory and preferred skills must be treated differently. | Display and compare the two skill categories separately. |
| BRL-09 | Skill verification must use approved evidence or authorized validation. | Restrict skill-profile updates to authorized users and retain update history. |
| BRL-10 | Assessment attempts, pass criteria and certification must follow L&D policy. | Apply configured assessment and retry rules. |
| BRL-11 | Course completion or assessment participation does not guarantee staffing. | Keep learning outcomes separate from staffing decisions. |
| BRL-12 | Changes to employee eligibility after interest submission must be assessed according to approved HR/RM policy. | Support review of updated employee status; the automatic or manual handling of existing interest remains subject to policy confirmation. |
| BRL-13 | Employee personal information must only be used and accessed for authorized business purposes. | Apply role-based access and restrict unnecessary personal information visibility. |
| BRL-14 | Financial benefits must use agreed definitions and validated baselines. | Provide reportable information required for financial assessment without presenting unvalidated savings as actual benefits. |

## 7. Field and Workflow Validation Requirements

The system shall perform validation at relevant data-entry and workflow stages.

| Validation ID | Area | Validation requirement |
|---|---|---|
| VAL-01 | Opportunity creation | Mandatory opportunity fields must be completed before publication. |
| VAL-02 | Project dates | Start date and closing date must satisfy approved date rules. |
| VAL-03 | Skills | At least the required mandatory skill information must be provided before publication. |
| VAL-04 | Opportunity status | Employees must not express interest in closed, cancelled or expired opportunities. |
| VAL-05 | Employee eligibility | Eligibility must be checked before accepting an expression of interest. |
| VAL-06 | Notice period | Employees serving a notice period must be prevented from expressing interest. |
| VAL-07 | Duplicate interest | Duplicate active interest submissions for the same opportunity must be prevented. |
| VAL-08 | Withdrawal | Withdrawal must follow the approved workflow and applicable status restrictions. |
| VAL-09 | Availability | Required availability information must be captured or presented for review. |
| VAL-10 | RM actions | Shortlisting, waitlisting and staffing confirmation must be restricted to authorized users. |
| VAL-11 | Assessment | Assessment attempts must follow the configured retry limit. |
| VAL-12 | Certification | Skill-profile updates based on certification must require authorized confirmation and relevant evidence. |
| VAL-13 | Access control | Unauthorized users must not access restricted employee or project information. |
| VAL-14 | Data quality | Missing, invalid or inconsistent employee data must be identified and handled without treating unknown information as verified. |

## 8. Notifications and Workflow Statuses

### 8.1 Notification Requirements

Notifications shall be triggered by relevant changes in opportunity, employee interest, staffing and learning workflows.

The system shall maintain sufficient notification information to identify the triggering event, intended recipient and notification status.

The exact notification channel, message templates, retry handling and delivery expectations remain subject to stakeholder confirmation and solution design.

### 8.2 Opportunity Statuses

| Status | Description |
|---|---|
| Draft | Opportunity created but not published. |
| Published | Opportunity made available to eligible employees. |
| Active | Opportunity is open for employee interest and review. |
| Closed | Opportunity is no longer accepting new interest. |
| Cancelled | Opportunity discontinued by an authorized user. |

### 8.3 Employee Interest and Staffing Statuses

| Status | Description |
|---|---|
| Interested | Employee has successfully expressed interest. |
| Withdrawn | Employee has withdrawn interest. |
| Under Review | Resource Manager is assessing the employee. |
| Shortlisted | Employee has been shortlisted for further consideration. |
| Waitlisted | Employee is retained for possible consideration subject to readiness or availability. |
| Selected | Employee has been selected through an authorized staffing decision. |
| Not Selected | Employee has not been selected for the opportunity. |

### 8.4 Learning Statuses

| Status | Description |
|---|---|
| Not Started | Learning activity has not started. |
| Enrolled | Employee has been enrolled in the learning activity. |
| In Progress | Learning activity is ongoing. |
| Assessment Failed | Employee did not meet the assessment pass criteria. |
| Passed | Employee met the applicable assessment criteria. |
| Certified | Certification has been recorded by an authorized user. |
| Retry Limit Reached | The permitted assessment attempts have been exhausted. |

## 9. Non-Functional Requirements

### 9.1 Access Control and Security

**NFR-01: Role-Based Access Control**

The system shall restrict access to functionality and information based on assigned user roles and permissions.

Users shall only perform actions authorized for their role.

**NFR-02: Employee Data Privacy**

The system shall protect employee personal information and restrict its visibility to authorized users with a legitimate business need.

Personal contact information, including mobile numbers, shall not be displayed to users unless access is explicitly authorized and required for an approved business purpose.

**NFR-03: Data Integrity**

The system shall maintain accurate and consistent employee, skill, opportunity, interest, learning and staffing information.

The system shall prevent unauthorized or invalid updates from compromising existing records.

**NFR-04: Auditability**

The system shall maintain an audit trail for relevant activities, including:

- Opportunity creation and updates.
- Publication, closure and cancellation.
- Expression and withdrawal of interest.
- RM assessment and staffing decisions.
- Learning and assessment updates.
- Certification and skill-profile changes.
- Changes to roles and access permissions.

Audit records shall identify the relevant action, user and timestamp, subject to the approved retention policy.

### 9.2 Usability and Compatibility

**NFR-05: Usability**

The portal shall provide clear navigation and understandable information for employees, Project Managers, Resource Managers, L&D users and Management.

Validation messages and workflow statuses shall be clear enough for users to understand the next required action.

**NFR-06: Browser and Platform Compatibility**

The solution shall support the browsers and platforms approved by ThinkPalm.

Supported browser versions, desktop and mobile access expectations shall be confirmed as part of solution design.

### 9.3 Performance and Scalability

**NFR-07: Performance**

The system shall provide acceptable response times for common activities, including opportunity listing, skill comparison, interest submission and dashboard access.

Specific response-time targets shall be established based on expected usage and agreed performance expectations.

**NFR-08: Scalability**

The solution shall support anticipated growth in employee records, project opportunities, skills, learning records and concurrent users without unacceptable performance degradation.

Expected user volumes, peak concurrent usage and future growth assumptions shall be established before performance targets are finalized.

### 9.4 Availability and Recovery

**NFR-09: Availability and Recovery**

The solution shall meet agreed availability, backup and recovery expectations.

Recovery objectives, maintenance windows and acceptable downtime shall be confirmed based on business requirements.

### 9.5 Maintainability and Configuration

**NFR-10: Maintainability**

The solution shall support maintainable enhancements to opportunity workflows, eligibility checks, notification rules, assessment settings and reporting.

**NFR-11: Configurability**

Business-controlled settings, such as assessment retry limits and applicable workflow timelines, shall be configurable by authorized users where supported by the approved solution design.

**NFR-12: Technical and Integration Constraints**

The enhancement shall consider the existing portal environment, approved technology standards, integration constraints and any customer or organizational technical requirements.

The final technical architecture and technology choices shall be determined by the responsible technical team in consultation with relevant stakeholders.

## 10. Data Requirements and Migration Considerations

The solution depends on accurate and current employee, employment-status and skill information.

The following data areas are required:

| Data area | Required information | Business purpose |
|---|---|---|
| Employee information | Employee identifier and relevant profile details | Identify employees and associate workflow records. |
| Employment status | Active employment and notice-period status | Validate eligibility before accepting interest. |
| Skill profile | Recorded skills and relevant proficiency details, where available | Compare employee skills with project requirements. |
| Project information | Project title, role, dates and required skills | Manage opportunities. |
| Interest information | Employee, opportunity, submission date and status | Track employee participation. |
| Readiness information | Relevant skill gaps, availability and assessment outcomes | Support RM review. |
| Learning information | Course, enrollment, completion and assessment details | Support L&D activities. |
| Certification information | Certification outcome and relevant evidence | Support authorized skill-profile updates. |
| Staffing information | Shortlist, waitlist and final staffing outcomes | Track internal staffing decisions. |

### 10.1 Data Migration and Integration Requirements

The data strategy shall assess whether the existing portal data can be reused directly, integrated with an authoritative source or migrated into the enhanced solution.

The assessment shall consider:

- Identification of authoritative sources for employee and employment-status information.
- Availability and reliability of notice-period status.
- Accuracy and completeness of employee skill profiles.
- Duplicate and outdated employee records.
- Mapping of existing fields to the enhanced portal.
- Validation of migrated or integrated data.
- Handling of incomplete, invalid or inconsistent records.
- Data synchronization frequency and failure handling.
- Access permissions and protection of personal information.
- Data retention and audit requirements.

The final migration or integration approach shall be based on source-system assessment and approved technical feasibility.

## 11. Exception and Error Handling

The system shall handle invalid data, unauthorized actions and workflow exceptions without creating incorrect or incomplete business records.

| Exception ID | Scenario | Expected system behaviour |
|---|---|---|
| EX-01 | Mandatory opportunity information is missing. | Prevent publication and identify the missing information. |
| EX-02 | Opportunity is closed, cancelled or expired. | Prevent new expressions of interest. |
| EX-03 | Employee is serving a notice period. | Block expression of interest and display an appropriate message. |
| EX-04 | Employee submits duplicate interest. | Prevent duplicate active submissions. |
| EX-05 | Employee attempts withdrawal in a restricted status. | Prevent the action and display the applicable restriction. |
| EX-06 | Employee skill information is missing. | Identify the missing information without automatically classifying it as a skill gap. |
| EX-07 | Employee eligibility or notice-period data is unavailable or outdated. | Do not treat the employee as verified eligible; apply the approved exception and data-refresh process. |
| EX-08 | Unauthorized user attempts a restricted action. | Deny access and record the relevant security event. |
| EX-09 | Employee reaches the assessment retry limit. | Prevent further attempts under the configured policy and update the learning status. |
| EX-10 | Employee completes a course but has not met certification criteria. | Do not mark the employee as certified. |
| EX-11 | Opportunity requirements change after employees express interest. | Notify affected users and retain the relevant change history. |
| EX-12 | Employee employment status changes after interest submission. | Flag the record for handling under the approved HR/RM policy; the exact automatic or manual action requires confirmation. |
| EX-13 | Employee or skill data migration contains invalid or duplicate records. | Identify the records for validation and prevent unverified data from being treated as accurate. |
| EX-14 | Notification delivery fails. | Record the delivery failure and apply the approved notification retry or exception process. |

## 12. Acceptance Criteria

The following acceptance criteria provide the basis for functional verification and UAT.

**AC-01: Opportunity Publication**

Given an authorized Project Manager has entered all mandatory opportunity details, when the Project Manager publishes the opportunity, then the system shall validate the information and make the opportunity available to eligible employees.

**AC-02: Mandatory and Preferred Skills**

Given an opportunity contains mandatory and preferred skills, when an employee views the opportunity, then the system shall display and compare these skill categories separately.

**AC-03: Skill Comparison**

Given an employee has recorded skills, when the employee views an opportunity, then the system shall identify matching, missing and preferred skills based on the available profile information.

**AC-04: Eligible Employee Interest**

Given an employee is eligible and the opportunity is active, when the employee submits interest, then the system shall record the submission and display a confirmation.

**AC-05: Notice-Period Restriction**

Given an employee is serving a notice period, when the employee attempts to express interest in an internal project opportunity, then the system shall prevent the submission and display an appropriate message.

**AC-06: Duplicate Interest**

Given an employee has already expressed active interest in an opportunity, when the employee attempts to submit interest again, then the system shall prevent the duplicate submission.

**AC-07: Withdrawal of Interest**

Given an employee has expressed interest and withdrawal is permitted under the approved policy, when the employee withdraws interest, then the system shall update the status and notify the Resource Manager.

**AC-08: Opportunity Changes**

Given an opportunity has employees who have expressed interest, when a Project Manager makes a material change, then the system shall retain the change history and notify affected users.

**AC-09: RM Assessment**

Given employees have expressed interest, when an authorized Resource Manager reviews them, then the system shall display the relevant skills, availability, readiness and interest information.

**AC-10: Shortlist and Waitlist**

Given an authorized Resource Manager has reviewed an employee, when the Resource Manager records a shortlist or waitlist decision, then the system shall update the employee's status without treating it as final allocation.

**AC-11: Learning and Assessment**

Given an employee has an identified skill gap and an applicable learning activity, when authorized L&D users record learning and assessment outcomes, then the system shall maintain the corresponding learning status and attempt history.

**AC-12: Certification and Skill Update**

Given an employee has met the applicable certification criteria, when an authorized user records the certification, then the system shall update the relevant skill information and retain the update history.

**AC-13: Staffing Confirmation**

Given an authorized Resource Manager has made a staffing decision, when the decision is confirmed, then the system shall update the staffing status and notify affected users.

**AC-14: Role-Based Access**

Given a user attempts to access information or functionality outside the user's assigned permissions, when the access request is made, then the system shall deny the unauthorized action.

**AC-15: Management Reporting**

Given authorized Management users access the dashboard, when they review project and resource information, then the system shall display the available staffing, opportunity, skill-gap and learning information according to their permissions.

## 13. Dependencies and Assumptions

### 13.1 Dependencies

- Availability of accurate employee and employment-status information.
- Availability of a reliable source for notice-period status.
- Availability of employee skill and certification records.
- Defined roles and permissions for all participating user groups.
- Approved eligibility and staffing policies.
- Defined L&D assessment and certification policies.
- Availability of relevant notification channels.
- Availability of project and staffing information for management reporting.
- Feasibility of integration with or reuse of existing portal data.

### 13.2 Assumptions

- The existing ThinkPalm Employee Management Portal can be enhanced to support the proposed workflow.
- The identified user roles will be authorized to perform their respective activities.
- Resource Managers retain responsibility for final staffing decisions.
- Employees serving a notice period are not eligible to express interest in internal project opportunities.
- Skill-profile information may require validation before it is used for staffing assessment.
- The final data integration or migration approach will depend on the assessment of existing systems and data.
- Performance, availability and scalability targets will be agreed based on expected usage.

## 14. Open Questions

| ID | Open question | Area requiring confirmation |
|---|---|---|
| OQ-01 | What are the mandatory fields required for every project opportunity? | Opportunity management |
| OQ-02 | Are there additional employee eligibility restrictions beyond the notice-period rule? | Employee eligibility |
| OQ-03 | Which employee information can each role view? | Access and privacy |
| OQ-04 | What is the expected timeline for RM review of employee interest? | Staffing workflow |
| OQ-05 | How should waitlisted employees be reassessed, and within what timeline? | Readiness and waitlisting |
| OQ-06 | Which notification channels are approved for workflow alerts? | Notifications |
| OQ-07 | What is the maximum permitted number of assessment attempts? | L&D |
| OQ-08 | Which role is authorized to update employee skill profiles after certification? | Skill management |
| OQ-09 | What conditions must be met before external recruitment can be considered? | Staffing policy |
| OQ-10 | Which data source is authoritative for employee and skill information? | Data integration |
| OQ-11 | What is the approved process when an employee enters a notice period after expressing interest? Should the existing interest be withdrawn automatically or reviewed by the RM? | Eligibility and workflow |
| OQ-12 | How frequently should employee employment and notice-period status be refreshed? | Data synchronization |
| OQ-13 | What are the expected number of users, peak concurrent users and projected growth? | Performance and scalability |
| OQ-14 | Which browsers and platforms must the enhanced portal support? | Compatibility |
| OQ-15 | What are the agreed response-time, availability, backup and recovery targets? | Non-functional requirements |
| OQ-16 | What data retention and audit-log retention periods are required? | Data governance |
| OQ-17 | What is the approved approach for handling incomplete, duplicate or outdated employee and skill records? | Data quality |
| OQ-18 | What are the expected notification delivery and failure-handling requirements? | Notifications |

## 15. Requirement Traceability References

The functional requirements in this document are derived from the business requirements in BRD Version 2.1.

| BRD Business Requirement | Related Functional Requirements |
|---|---|
| BR-01: Centralized opportunity visibility | FR-01, FR-03, FR-06 |
| BR-02: Mandatory opportunity details | FR-01, FR-02, FR-03 |
| BR-03: Employee skill comparison | FR-06, FR-07, FR-08 |
| BR-04: Employee interest and withdrawal | FR-09, FR-10 |
| BR-05: RM review | FR-12, FR-13, FR-14 |
| BR-06: Suitability, shortlist and waitlist | FR-14, FR-15 |
| BR-07: L&D learning support | FR-18, FR-19 |
| BR-08: Assessment, retries and certification | FR-20, FR-21, FR-22 |
| BR-09: Authorized skill-profile updates | FR-22 |
| BR-10: Authorized staffing confirmation | FR-17 |
| BR-11: Notifications | FR-04, FR-05, FR-09, FR-10, FR-24 |
| BR-12: Management visibility | FR-23, FR-25 |
| BR-13: Internal resource consideration | FR-16, FR-17 |
| BR-14: Role-based access | FR-12, FR-13, FR-17, FR-25 and NFR-01 |
| BR-15: Auditability and traceability | FR-04, FR-14, FR-17, FR-22 and NFR-04 |
| BR-21: Employee eligibility, including notice-period restrictions | FR-09, FR-26, VAL-05, VAL-06 and AC-05 |

The detailed bidirectional mapping between business requirements, functional requirements, user stories, development modules and test cases shall be maintained in the Requirements Traceability Matrix (RTM).

## 16. Approval and Review

| Role | Name | Responsibility | Status |
|---|---|---|---|
| Business Analyst | Mary Juliya | Requirements analysis and documentation | Prepared |
| Business Sponsor / Management | To be confirmed | Business review and approval | Pending |
| Resource Manager | To be confirmed | Staffing workflow validation | Pending |
| Project Manager Representative | To be confirmed | Opportunity workflow validation | Pending |
| L&D Representative | To be confirmed | Learning and assessment workflow validation | Pending |
| Portal Administrator | To be confirmed | Existing portal and access-related review | Pending |

## 17. Document Status

This FRD represents the proposed functional and non-functional requirements for the ThinkPalm case-study enhancement.

It is aligned with the Capstone BRD Version 2.1 and incorporates the identified business rules, notice-period eligibility restriction, data privacy considerations, validation requirements, notifications, data integration considerations and testing acceptance criteria.

Items requiring organizational policy confirmation or technical feasibility assessment are explicitly identified as open questions, assumptions or dependencies rather than treated as confirmed decisions.
