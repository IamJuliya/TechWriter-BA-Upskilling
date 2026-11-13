# User Acceptance Testing (UAT) Plan - Project Opportunities & Talent Readiness Enhancement

## Contents
[1. Introduction](#1-introduction)
  - [1.1 Purpose](#11-purpose)
  - [1.2 Project Overview](#12-project-overview)
  - [1.3 UAT Objectives](#13-uat-objectives)
  - [1.4 Scope](#14-scope)

[2. UAT Approach](#2-uat-approach)

[3. UAT Participants and Responsibilities](#3-uat-participants-and-responsibilities)

[4. UAT Environment and Test Data](#4-uat-environment-and-test-data)

[5. Entry Criteria](#5-entry-criteria)

[6. UAT Scenarios and Acceptance Criteria](#6-uat-scenarios-and-acceptance-criteria)
  - [6.1 Project Opportunity Management](#61-project-opportunity-management)
  - [6.2 Employee Opportunity Access and Eligibility](#62-employee-opportunity-access-and-eligibility)
  - [6.3 Skill Comparison and Expression of Interest](#63-skill-comparison-and-expression-of-interest)
  - [6.4 Resource Manager Review and Staffing](#64-resource-manager-review-and-staffing)
  - [6.5 Learning and Development](#65-learning-and-development)
  - [6.6 Notifications and Management Reporting](#66-notifications-and-management-reporting)
  - [6.7 Access Control and Data Privacy](#67-access-control-and-data-privacy)
  - [6.8 Data Migration and Integration](#68-data-migration-and-integration)

[7. Exit Criteria](#7-exit-criteria)

[8. Defect Management](#8-defect-management)

[9. UAT Execution and Sign-off](#9-uat-execution-and-sign-off)

[10. Risks and Mitigation](#10-risks-and-mitigation)

[11. Assumptions and Open Questions](#11-assumptions-and-open-questions)

[12. Approval](#12-approval)

## 1. Introduction

### 1.1 Purpose

This document defines the User Acceptance Testing (UAT) approach for the Project Opportunities & Talent Readiness Enhancement initiative.

The purpose of UAT is to confirm that the proposed portal enhancement meets the identified business needs and supports the intended business workflows.

Business representatives will validate the solution using realistic business scenarios and confirm whether the implemented functionality is suitable for acceptance.

### 1.2 Project Overview

The initiative proposes enhancing the existing ThinkPalm Employee Management Portal to improve visibility into upcoming project opportunities and make more effective use of available employee skills.

The proposed solution enables:

- Project Managers to publish opportunities with required skills and project timelines.
- Employees to discover opportunities, compare their skills, identify gaps, and express or withdraw interest.
- Resource Managers to review employee suitability, readiness, and availability and make staffing decisions.
- L&D teams to support skill-gap closure through learning, assessments, retries, and certification.
- Management to review talent availability, staffing outcomes, and learning information.

The solution supports internal resource consideration before external recruitment, according to approved management policy. Staffing decisions remain with authorized personnel; the system does not automatically allocate employees.

### 1.3 UAT Objectives

The objectives are to:

1. Validate that the solution supports the agreed business requirements.
2. Confirm that each stakeholder can complete their intended activities.
3. Verify that business rules and eligibility restrictions are enforced.
4. Validate end-to-end workflow transitions and status updates.
5. Confirm that employees and stakeholders receive relevant notifications.
6. Verify that employee information is accessible only to authorized users.
7. Confirm that management reporting provides meaningful and accurate information.
8. Obtain business stakeholder acceptance before release.

### 1.4 Scope

**In Scope**

- Project opportunity creation, publication, modification, and closure.
- Employee opportunity discovery and eligibility.
- Skill comparison and skill-gap identification.
- Expression and withdrawal of interest.
- Resource Manager review, shortlisting, waitlisting, and staffing decisions.
- L&D learning, assessment, retry, and certification workflows.
- Notifications and management dashboards.
- Role-based access and employee information privacy.
- Employee and skill data migration or integration validation.

**Out of Scope**

- Automatic employee allocation.
- End-to-end external recruitment processing.
- Salary, promotion, or performance appraisal workflows.
- Automatic training assignment.
- Full organizational capacity planning.
- Verification of financial savings without an approved baseline and validated financial data.

## 2. UAT Approach

UAT will follow a business-scenario-based approach.

Business users will execute the agreed UAT scenarios using the test environment and representative test data. Results will be compared with the expected business outcomes.

| UAT Stage | Description |
|---|---|
| UAT Preparation | Confirm scope, participants, environment, test data, and acceptance criteria. |
| Scenario Review | Review UAT scenarios against approved business requirements and business rules. |
| Test Execution | Business users execute the scenarios and record actual results. |
| Defect Reporting | Deviations from expected results are recorded and assigned for resolution. |
| Retesting | Corrected functionality is retested to confirm defect resolution. |
| Regression Validation | Related business workflows are revalidated after significant changes. |
| Business Sign-off | Authorized stakeholders review the results and record acceptance or outstanding conditions. |

UAT is intended to validate business suitability and is not a replacement for developer testing, system testing, or functional testing.

## 3. UAT Participants and Responsibilities

| Stakeholder | UAT Responsibility |
|---|---|
| Management / Project Sponsor | Review business outcomes, management reporting, and overall business suitability. |
| Project Manager | Validate opportunity creation, required skills, publication, updates, and closure. |
| Resource Manager | Validate employee review, suitability, readiness, waitlisting, and staffing decisions. |
| Employee Representatives | Validate opportunity visibility, skill comparison, eligibility, expression of interest, and withdrawal. |
| L&D Representative | Validate learning enrolment, assessment results, retries, certification, and skill updates. |
| Business Analyst | Coordinate UAT preparation, clarify requirements, support execution, track defects, and maintain traceability. |
| Development / Testing Team | Support the UAT environment, investigate defects, implement fixes, and provide technical assistance. |

The Development and Testing Team provides implementation support; business acceptance remains the responsibility of the authorized business stakeholders.

## 4. UAT Environment and Test Data

### 4.1 UAT Environment

The UAT environment should provide the following:

- A stable version of the enhanced Employee Management Portal.
- Configured user accounts for all participating business roles.
- Required role-based access permissions.
- Connectivity to approved employee and skill data sources.
- Configured notification channels.
- Sample learning courses, assessments, and certification records.
- Access to relevant opportunity, interest, staffing, and reporting information.
- Defect tracking and test evidence recording facilities.

### 4.2 Test Data

The following representative data will be used during UAT.

| Data Category | Sample Test Data |
|---|---|
| Project Opportunity | Marine Project – System Engineer |
| Mandatory Skills | Python, SQL |
| Preferred Skills | AWS, Docker |
| Employee A | Eligible employee with all mandatory skills |
| Employee B | Eligible employee with a skill gap |
| Employee C | Employee serving notice period |
| Employee D | Employee with incomplete skill information |
| Availability | Available, Partially Available, Unavailable |
| Learning Course | Python Advanced Training |
| Assessment Results | Passed, Failed |
| Staffing Outcomes | Shortlisted, Waitlisted, Selected, Not Selected |

All test data must be approved for UAT and must not expose actual employee personal information.

## 5. Entry Criteria

UAT may begin when the following conditions are satisfied:

1. Approved BRD, FRD, and relevant user stories are available.
2. Functional testing has been completed for the agreed UAT scope.
3. Critical and high-severity functional defects affecting UAT scenarios have been resolved or formally accepted for controlled evaluation.
4. The UAT environment is stable and accessible.
5. Required user roles and permissions are configured.
6. Representative employee, skill, opportunity, and learning data is available.
7. Notice-period and employment-status data sources are available for eligibility validation.
8. UAT scenarios and expected results have been reviewed by relevant business representatives.
9. Participants understand their roles and the UAT execution process.

## 6. UAT Scenarios and Acceptance Criteria

The following scenarios represent the key business workflows to be validated.

### 6.1 Project Opportunity Management

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-001 | Project Manager creates a project opportunity with required project information. | Opportunity is created successfully and saved in Draft status. | High | BR-02, FR-01 |
| UAT-002 | Project Manager defines mandatory and preferred skills. | Required skills are correctly classified and visible in the opportunity details. | High | BR-02, FR-02 |
| UAT-003 | Project Manager publishes a complete opportunity. | Opportunity becomes available to eligible employees. | High | BR-01, FR-03 |
| UAT-004 | Project Manager attempts to publish an opportunity with missing mandatory information. | Publication is prevented and the missing information is clearly identified. | High | BR-02, FR-03 |
| UAT-005 | Project Manager updates or closes an opportunity. | Changes are saved, the opportunity status is updated, and affected users are informed where applicable. | Medium | BR-11, FR-04, FR-05 |

### 6.2 Employee Opportunity Access and Eligibility

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-006 | Eligible employee views published opportunities. | Employee can discover relevant opportunities and review project details. | High | BR-03, FR-06 |
| UAT-007 | Employee attempts to access a draft or closed opportunity as an available opportunity. | Draft and closed opportunities are not presented as open opportunities for interest. | High | BR-03, FR-06 |
| UAT-008 | Employee serving a notice period attempts to express interest. | System blocks the action. No interest record is created, and the employee receives an appropriate explanation. | Critical | BRL-01, FR-09 |
| UAT-009 | Employee attempts to express interest when employment-status information is unavailable or stale. | System does not assume eligibility. The approved exception process is followed. | Critical | BRL-01, FR-09 |
| UAT-010 | Employee becomes subject to a notice period after expressing interest. | The system follows the approved policy for automatic withdrawal or RM review, and the resulting action is recorded. | Critical | BRL-12, FR-09, FR-10 |

### 6.3 Skill Comparison and Expression of Interest

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-011 | Employee compares recorded skills with project requirements. | Mandatory and preferred skills are displayed clearly against the employee's recorded skills. | High | BR-03, FR-07 |
| UAT-012 | Employee identifies missing or insufficient skills. | Skill gaps are clearly highlighted without treating incomplete profile data as proof that an employee lacks a skill. | High | BR-03, FR-08 |
| UAT-013 | Eligible employee expresses interest in an active opportunity. | Interest is recorded successfully and confirmation is displayed. | Critical | BR-04, FR-09 |
| UAT-014 | Employee attempts to submit duplicate interest. | Duplicate active interest is prevented. | High | BR-04, FR-09 |
| UAT-015 | Employee withdraws interest before the staffing outcome is finalized. | Interest status is updated and relevant stakeholders are informed where applicable. | Medium | BR-04, FR-10 |

### 6.4 Resource Manager Review and Staffing

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-016 | RM reviews employees interested in an opportunity. | RM can view the relevant employee list and review available information. | High | BR-05, FR-12, FR-13 |
| UAT-017 | RM evaluates employee skills, experience, availability, and readiness. | RM can record a suitability and readiness assessment based on project requirements. | High | BR-05, BR-06, FR-14 |
| UAT-018 | RM shortlists a suitable employee. | Employee status changes to Shortlisted and the decision is recorded. | High | BR-06, FR-15 |
| UAT-019 | RM waitlists an employee who may become ready by the required date. | Employee status changes to Waitlisted and the readiness consideration is recorded. | Medium | BR-06, FR-15 |
| UAT-020 | No suitable and sufficiently ready internal employee is identified. | RM records the unfilled opportunity outcome. External recruitment may be considered only through the approved internal review and authorization process. | High | BR-13, FR-16 |
| UAT-021 | Authorized RM confirms the final staffing outcome. | Staffing decision is recorded and relevant users receive the appropriate status update. | Critical | BR-10, FR-17 |
| UAT-022 | Unauthorized user attempts to confirm staffing. | System prevents the action and does not change the staffing decision. | Critical | BR-10, FR-17 |

### 6.5 Learning and Development

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-023 | L&D reviews skill-gap information for an employee. | Authorized L&D users can access the information needed to plan learning support. | Medium | BR-07, FR-18 |
| UAT-024 | L&D enrols an employee in a relevant learning course. | Enrolment is recorded and the learning status is updated. | Medium | BR-07, FR-19 |
| UAT-025 | L&D records course completion and assessment results. | Course completion and assessment results are recorded accurately. | High | BR-08, FR-20 |
| UAT-026 | Employee requires another assessment attempt within the permitted limit. | The system permits the retry according to the approved L&D policy. | Medium | BR-08, FR-21 |
| UAT-027 | Employee reaches the maximum permitted assessment attempts. | Further attempts are prevented and the correct learning status is displayed. | High | BR-08, FR-21 |
| UAT-028 | Authorized L&D user records certification and updates the skill profile. | Certification is recorded and the employee skill profile is updated by an authorized user. | High | BR-09, FR-22 |
| UAT-029 | Employee completes learning and certification but is not yet selected for a project. | Learning completion does not automatically result in project allocation or staffing confirmation. | High | BRL-11, FR-17, FR-22 |
| UAT-030 | L&D reviews aggregated skill-gap information for training planning. | Authorized L&D users can review relevant skill-gap trends for training planning. | Medium | BR-07, FR-23 |

### 6.6 Notifications and Management Reporting

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-031 | Opportunity is published. | Eligible employees receive the configured opportunity notification. | Medium | BR-11, FR-24 |
| UAT-032 | Opportunity details or staffing status change. | Relevant affected users receive appropriate notifications. | High | BR-11, FR-24 |
| UAT-033 | Management reviews the dashboard. | Management can view authorized information about opportunities, availability, staffing, and learning. | Medium | BR-12, FR-25 |
| UAT-034 | Management reviews reported staffing and financial information. | Staffing information is consistent with underlying records. Financial benefits are presented only using approved definitions and validated baseline data. | High | BR-12, BRL-14, FR-25 |

### 6.7 Access Control and Data Privacy

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-035 | Different user roles access the portal. | Each role can access only the functions and information permitted by its assigned permissions. | Critical | BR-14, FR-13, FR-17, FR-25 |
| UAT-036 | User attempts to view restricted employee personal information. | Restricted information is not exposed to unauthorized users. | Critical | BR-14, BRL-13, FR-13 |
| UAT-037 | Important opportunity, assessment, or staffing actions are performed. | Relevant actions are recorded for traceability and audit purposes. | High | BR-15, FR-14, FR-17, FR-22 |

### 6.8 Data Migration and Integration

| UAT ID | Business Scenario | Expected Business Outcome | Priority | Related Requirements |
|---|---|---|---|---|
| UAT-038 | Business representatives validate migrated or integrated employee and skill information. | Employee records and skill information are accurate and consistent with the approved source. | High | BR-03, BR-05, FR-07, FR-11 |
| UAT-039 | Duplicate or incomplete employee records are identified. | Data quality issues are identified and handled according to the approved migration or integration process. | High | BR-15, FR-11 |
| UAT-040 | Employment and notice-period information is updated in the approved source. | Updated information is reflected in the portal within the agreed synchronization interval. | Critical | BRL-01, FR-09, FR-11 |
| UAT-041 | Employee or skill data synchronization fails. | Failure is handled without using unreliable information for eligibility or staffing decisions. | High | BR-14, FR-09, FR-11 |

## 7. Exit Criteria

UAT can be considered complete when the following conditions are met:

1. All planned UAT scenarios have been executed or formally deferred with documented justification.
2. All Critical-priority UAT scenarios have passed.
3. No unresolved Critical-severity defects remain.
4. High-severity defects have been resolved or formally accepted with documented business approval and mitigation.
5. Failed scenarios have been retested after defect resolution.
6. Relevant regression scenarios have been completed.
7. Business stakeholders have reviewed the UAT results.
8. Outstanding issues and known limitations are documented.
9. Authorized stakeholders have recorded the final acceptance decision.

A failed or blocked scenario must not be treated as passed. Any conditional acceptance must clearly document the outstanding issue, business impact, mitigation, owner, and approval.

## 8. Defect Management

Defects identified during UAT must be recorded and tracked until resolution or an approved disposition is reached.

### 8.1 Defect Severity

| Severity | Description | Example |
|---|---|---|
| Critical | A major business process is blocked or a serious business rule or security control is violated. | Employee serving notice can express interest; unauthorized user can confirm staffing. |
| High | Important business functionality does not work as expected. | RM cannot record a staffing outcome. |
| Medium | Supporting functionality is affected, but the main business workflow can continue. | A non-critical notification is delayed. |
| Low | Minor issue with limited business impact. | Minor display or wording issue. |

### 8.2 Defect Lifecycle

| Defect Status | Description |
|---|---|
| New | Defect has been reported. |
| Assigned | Defect has been assigned for investigation. |
| In Progress | Investigation or correction is underway. |
| Fixed | Correction has been implemented and is ready for retesting. |
| Retest | Business user or tester is verifying the correction. |
| Closed | Correction has been verified successfully. |
| Reopened | Defect persists or reappears after retesting. |
| Deferred | Resolution is postponed with documented approval and justification. |

### 8.3 Defect Information

Each defect record should include:

- Defect ID.
- Related UAT ID and requirement reference.
- Defect summary and description.
- Steps to reproduce.
- Expected and actual results.
- Severity and priority.
- Reported date and reported by.
- Assigned owner.
- Current status.
- Resolution details and retest result.

## 9. UAT Execution and Sign-off

### 9.1 UAT Execution Record

The following information must be recorded for each UAT scenario.

| Field | Description |
|---|---|
| UAT ID | Unique scenario identifier. |
| Scenario | Business scenario being validated. |
| Executed By | Business user who performed the scenario. |
| Execution Date | Date of execution. |
| Expected Result | Expected business outcome. |
| Actual Result | Actual outcome observed. |
| Status | Not Run, Pass, Fail, or Blocked. |
| Evidence Reference | Screenshot, record ID, or other supporting evidence. |
| Defect ID | Reference to a defect, if applicable. |
| Comments | Observations or clarification. |

### 9.2 UAT Status Definitions

| Status | Definition |
|---|---|
| Not Run | Scenario has not yet been executed. |
| Pass | Actual outcome meets the expected business result. |
| Fail | Actual outcome does not meet the expected business result. |
| Blocked | Scenario cannot be executed because of an unresolved dependency or issue. |
| Retest Required | A defect has been corrected and the scenario needs to be executed again. |

All UAT scenarios are initially assigned the status **Not Run**. No test result or business acceptance is assumed before actual execution.

### 9.3 UAT Sign-off

At the end of UAT, the results will be reviewed by the relevant business stakeholders.

The sign-off decision may be:

| Decision | Meaning |
|---|---|
| Accepted | UAT criteria are met and the business accepts the solution. |
| Conditionally Accepted | The business accepts the solution subject to documented outstanding issues and agreed actions. |
| Rejected | Significant issues remain and the solution is not accepted for release. |

### 9.4 Sign-off Record

| Stakeholder Role | Sign-off Responsibility | Name | Decision | Date |
|---|---|---|---|---|
| Management / Project Sponsor | Overall business acceptance | Pending | Pending | Pending |
| Project Manager | Opportunity management acceptance | Pending | Pending | Pending |
| Resource Manager | Review and staffing workflow acceptance | Pending | Pending | Pending |
| Employee Representative | Employee opportunity and interest workflow acceptance | Pending | Pending | Pending |
| L&D Representative | Learning and certification workflow acceptance | Pending | Pending | Pending |

## 10. Risks and Mitigation

| Risk ID | Risk | Potential Impact | Mitigation |
|---|---|---|---|
| R-01 | Incomplete or outdated employee skill information. | Incorrect skill comparison and suitability assessment. | Validate employee and skill data before UAT. |
| R-02 | Notice-period information is unavailable or inaccurate. | Ineligible employees may be allowed to express interest. | Confirm the authoritative source and validate exception handling. |
| R-03 | UAT participants are unavailable. | Delayed validation and sign-off. | Agree participant availability and responsibilities in advance. |
| R-04 | UAT environment is unstable. | Test execution may be interrupted. | Validate environment readiness before UAT. |
| R-05 | Business rules are not finalized. | Expected outcomes may be disputed during testing. | Obtain stakeholder confirmation for pending policy decisions. |
| R-06 | Personal employee information is exposed during UAT. | Privacy and confidentiality risk. | Use approved test data and role-based access controls. |
| R-07 | Integration or notification dependencies fail. | Incomplete end-to-end workflow validation. | Validate dependencies and document any blocked scenarios. |
| R-08 | Critical defects remain unresolved. | Business process may not be suitable for acceptance. | Resolve critical defects and complete retesting before sign-off. |

## 11. Assumptions and Open Questions

### 11.1 Assumptions

1. UAT will be conducted after the agreed functional testing activities are completed.
2. Business representatives will participate in validating their respective workflows.
3. The UAT environment will be separate from production and contain approved test data.
4. Employee employment status and notice-period information will be available through an approved source.
5. Business rules for eligibility, availability, assessment retries, and staffing decisions will be confirmed before execution.
6. Notification channels and recipient rules will be configured according to approved requirements.
7. UAT results and evidence will be recorded in an agreed tracking location.
8. Final business acceptance will be provided by authorized stakeholders.

### 11.2 Open Questions

| ID | Open Question | Impact on UAT |
|---|---|---|
| OQ-01 | Who will represent each business role during UAT? | Confirms UAT participants and execution ownership. |
| OQ-02 | What is the approved behaviour when an employee enters a notice period after expressing interest? | Finalizes UAT-010. |
| OQ-03 | Which system provides authoritative employment and notice-period information? | Confirms UAT-008, UAT-009, and UAT-040. |
| OQ-04 | What is the approved internal review process before external recruitment is considered? | Finalizes UAT-020. |
| OQ-05 | What employee information can each role access? | Finalizes privacy and access-control acceptance criteria. |
| OQ-06 | What are the approved assessment retry and certification rules? | Finalizes learning workflow scenarios. |
| OQ-07 | What are the agreed notification channels and recipients? | Finalizes notification acceptance criteria. |
| OQ-08 | What are the approved performance and availability expectations? | Determines whether additional non-functional acceptance testing is required. |
| OQ-09 | What financial baseline and benefit definitions will management approve? | Finalizes financial reporting validation. |

## 12. Approval

| Role | Responsibility | Approval Status |
|---|---|---|
| Business Analyst | Prepared the UAT Plan | Prepared |
| Management / Project Sponsor | Review and approve UAT approach | Pending |
| Resource Manager | Validate staffing-related UAT scenarios | Pending |
| Project Manager | Validate opportunity-related UAT scenarios | Pending |
| Employee Representative | Validate employee-related UAT scenarios | Pending |
| L&D Representative | Validate learning-related UAT scenarios | Pending |

**Document Note:** This UAT Plan is prepared for the ThinkPalm Capstone case-study initiative. It defines the proposed business acceptance approach and scenarios. Actual execution results, defect resolution, and final acceptance remain subject to implementation readiness and stakeholder validation.
