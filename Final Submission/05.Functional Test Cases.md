# Functional Test Cases
## Contents

- [1. Introduction](#1-introduction)
  - [1.1 Purpose](#11-purpose)
  - [1.2 Scope](#12-scope)
  - [1.3 Testing Objectives](#13-testing-objectives)
- [2. Testing Approach](#2-testing-approach)
- [3. Test Environment and Preconditions](#3-test-environment-and-preconditions)
- [4. Test Data Requirements](#4-test-data-requirements)
- [5. Functional Test Cases](#5-functional-test-cases)
  - [5.1 Project Opportunity Management](#51-project-opportunity-management)
  - [5.2 Employee Opportunity Access and Eligibility](#52-employee-opportunity-access-and-eligibility)
  - [5.3 Employee Skill Comparison and Interest](#53-employee-skill-comparison-and-interest)
  - [5.4 Resource Manager Review and Staffing](#54-resource-manager-review-and-staffing)
  - [5.5 Learning and Development](#55-learning-and-development)
  - [5.6 Notifications and Management Reporting](#56-notifications-and-management-reporting)
  - [5.7 Access Control and Data Privacy](#57-access-control-and-data-privacy)
  - [5.8 Data Migration and Integration](#58-data-migration-and-integration)
- [6. Negative and Exception Test Cases](#6-negative-and-exception-test-cases)
- [7. Regression Testing](#7-regression-testing)
- [8. Test Execution Summary](#8-test-execution-summary)
- [9. Defect Management](#9-defect-management)
- [10. Requirements Traceability](#10-requirements-traceability)
- [11. Assumptions and Open Questions](#11-assumptions-and-open-questions)

## 1. Introduction
**Document Note:** 
This document defines proposed functional test scenarios for the ThinkPalm case-study initiative. Test execution results, defect status, and final acceptance depend on implementation, environment readiness, and stakeholder-approved business policies.

### 1.1 Purpose

This document defines the functional test cases for the Project Opportunities & Talent Readiness Enhancement initiative.

It provides a structured approach to verifying that the proposed portal enhancements meet the functional requirements documented in the Functional Requirements Document (FRD).

The test cases validate the complete opportunity-to-staffing workflow, including opportunity publication, employee eligibility, skill comparison, expression of interest, Resource Manager review, learning support, notifications, and management reporting.

### 1.2 Scope

Testing covers the following functional areas:

- Project opportunity creation, publication, modification, and closure.
- Employee access to eligible opportunities.
- Skill comparison and identification of skill gaps.
- Employee eligibility and expression of interest.
- Resource Manager review, shortlisting, waitlisting, and staffing decisions.
- Learning enrolment, assessments, retries, and certification.
- Notifications and management dashboards.
- Role-based access and personal data protection.
- Existing employee and skill data migration or integration.

Automatic employee allocation and end-to-end recruitment processing are outside the scope of this testing.

### 1.3 Testing Objectives

The objectives are to:

1. Verify that each implemented function meets its documented requirement.
2. Confirm that business rules and eligibility restrictions are enforced.
3. Validate positive, negative, boundary, and exception scenarios.
4. Verify role-based access and protection of employee information.
5. Ensure that workflow statuses and notifications are updated correctly.
6. Identify defects before business acceptance and release.
7. Establish regression coverage for future changes.

## 2. Testing Approach

The test cases follow a requirement-based functional testing approach.

| Testing Type | Purpose |
|---|---|
| Positive Testing | Verify that valid user actions produce the expected results. |
| Negative Testing | Verify that invalid actions and restricted operations are prevented. |
| Boundary Testing | Validate behaviour at date, attempt-limit, and other defined boundaries. |
| Exception Testing | Verify system behaviour when required data or dependent services are unavailable. |
| Role-Based Testing | Confirm that users can access only the functions and information permitted for their roles. |
| Regression Testing | Confirm that changes do not adversely affect previously working functionality. |

Each test case includes a unique ID, scenario, preconditions, execution steps, expected result, priority, test type, and requirement references.

## 3. Test Environment and Preconditions

The following conditions are assumed for test execution:

- A test environment containing the enhanced Employee Management Portal is available.
- Test accounts are configured for Project Manager, Employee, Resource Manager, L&D, and Management roles.
- Employee profiles contain sample employment status, availability, and skill information.
- Project opportunities can be created with mandatory and preferred skills.
- Required notification channels are configured in the test environment.
- Learning courses, assessments, retry limits, and certification rules are configured for testing.
- Test data is approved and does not expose actual employee personal information.
- The authoritative source for notice-period and employment-status information is available for integration testing.

## 4. Test Data Requirements

The following sample data is required to execute the test cases.

| Test Data | Sample Values |
|---|---|
| Project Opportunity | Marine Project – System Engineer |
| Mandatory Skills | Python, SQL |
| Preferred Skills | AWS, Docker |
| Opportunity Status | Draft, Published, Closed |
| Employee A | Eligible employee with all mandatory skills |
| Employee B | Eligible employee with one mandatory skill gap |
| Employee C | Employee serving notice period |
| Employee D | Employee with incomplete skill information |
| Employee Availability | Available, Partially Available, Unavailable |
| Learning Course | Python Advanced Training |
| Assessment Result | Passed, Failed |
| Assessment Attempts | Within configured limit, Limit reached |
| User Roles | PM, Employee, RM, L&D, Management |

These are illustrative test values for the case study. Actual test data and policy configurations are subject to stakeholder approval.

## 5. Functional Test Cases

### 5.1 Project Opportunity Management

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-001 | Create a project opportunity | PM logs in, enters valid project details, role, dates, and description, and saves the opportunity. | Opportunity is created successfully with Draft status. | High | Positive | FR-01 |
| TC-002 | Add mandatory and preferred skills | PM adds mandatory and preferred skills to an opportunity and saves the details. | Skills are saved under the correct categories. | High | Positive | FR-02 |
| TC-003 | Publish an opportunity with complete details | PM completes all required fields and publishes the opportunity. | Opportunity is published and becomes available to eligible employees. | High | Positive | FR-03 |
| TC-004 | Publish an opportunity with missing mandatory information | PM attempts to publish an opportunity without required fields or mandatory skills. | Publication is blocked and appropriate validation messages are displayed. | High | Negative | FR-03, BRL-02 |
| TC-005 | Update a published opportunity | PM modifies permitted details of an active opportunity and saves the changes. | Updated information is saved and affected users are notified where applicable. | Medium | Positive | FR-04, FR-24 |
| TC-006 | Close or cancel an opportunity | Authorized PM closes or cancels an active opportunity. | Opportunity status is updated, further expressions of interest are prevented, and affected users are notified. | High | Positive | FR-05, FR-24 |

### 5.2 Employee Opportunity Access and Eligibility

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-007 | View published opportunities | Eligible employee logs in and opens the opportunity listing. | Employee can view relevant published opportunities and their details. | High | Positive | FR-06 |
| TC-008 | Prevent access to draft opportunities | Employee attempts to access an opportunity that is still in Draft status. | Draft opportunity is not visible or accessible to the employee. | High | Negative | FR-06, BRL-01 |
| TC-009 | Prevent an employee serving notice from expressing interest | Employee C has an active notice-period status in the approved employment-status data source. Employee opens a published opportunity and attempts to express interest. | System blocks the action and displays an appropriate message explaining that employees serving notice are not eligible to express interest. No interest record is created. | Critical | Negative | FR-09, BRL-01 |
| TC-010 | Allow an eligible employee to express interest | Employee A is eligible, is not serving notice, and meets the configured participation conditions. Employee expresses interest in an active opportunity. | Expression of interest is recorded successfully and the status is updated. | Critical | Positive | FR-09, BRL-02 |
| TC-011 | Prevent interest after the opportunity closing date | Employee attempts to express interest after the opportunity has closed or its application period has ended. | System prevents the action and displays an appropriate message. | High | Negative | FR-09, BRL-03 |
| TC-012 | Handle unavailable notice-period information | Employee attempts to express interest, but the approved employment-status source is unavailable or returns stale information. | System does not assume eligibility. The action is handled according to the approved exception policy, and the issue is recorded or communicated appropriately. | Critical | Exception | FR-09, BRL-01 |

### 5.3 Employee Skill Comparison and Interest

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-013 | Compare employee skills with project requirements | Employee opens an opportunity and selects the skill comparison view. | System displays the employee's recorded skills against the opportunity's required skills. | High | Positive | FR-07 |
| TC-014 | Identify missing mandatory skills | Employee profile does not contain one or more mandatory project skills. Employee views the comparison. | Missing mandatory skills are clearly identified as skill gaps. | High | Positive | FR-08 |
| TC-015 | Prevent duplicate active expressions of interest | Employee has already expressed interest in an opportunity and attempts to submit another expression for the same opportunity. | System prevents duplicate active interest records. | High | Negative | FR-09, BRL-04 |
| TC-016 | Withdraw an expression of interest | Employee has an active expression of interest and selects Withdraw. | Interest status is updated to Withdrawn, and the relevant users are notified where applicable. | Medium | Positive | FR-10, BRL-05 |

### 5.4 Resource Manager Review and Staffing

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-017 | View employees interested in an opportunity | RM opens a published opportunity with employee expressions of interest. | RM can view the relevant interested employee list. | High | Positive | FR-12 |
| TC-018 | Review employee information | RM selects an employee from the interested list. | RM can view authorized employment, availability, experience, and skill information needed for assessment. Restricted personal information remains protected. | High | Positive | FR-13 |
| TC-019 | Record suitability and readiness assessment | RM evaluates an employee against the project requirements and records the assessment. | Assessment details are saved and associated with the correct employee and opportunity. | High | Positive | FR-14 |
| TC-020 | Shortlist a suitable employee | RM identifies an employee as suitable and selects the Shortlist action. | Employee status is updated to Shortlisted and the decision is recorded. | High | Positive | FR-15 |
| TC-021 | Waitlist a suitable but not-ready employee | RM determines that an employee may become ready by the required date and selects Waitlist. | Employee status is updated to Waitlisted, with the relevant readiness information recorded. | Medium | Positive | FR-15 |
| TC-022 | Confirm a staffing decision | Authorized RM records the final staffing decision for an opportunity. | Decision is saved, the relevant status is updated, and affected users are notified. | Critical | Positive | FR-17, FR-24 |
| TC-023 | Prevent unauthorized staffing confirmation | An employee or PM without the required authorization attempts to confirm a staffing decision. | System denies the action and does not change the staffing status. | Critical | Negative | FR-17, BRL-06 |

### 5.5 Learning and Development

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-024 | View skill-gap information for learning support | RM identifies an employee with a skill gap and makes the relevant information available to L&D. | Authorized L&D users can view the skill-gap information required for learning support. | Medium | Positive | FR-18 |
| TC-025 | Enrol an employee in a learning course | Authorized L&D user enrols an employee in a relevant course. | Enrolment is recorded and learning status is updated. | Medium | Positive | FR-19 |
| TC-026 | Record course completion and assessment result | L&D records course completion and the employee's assessment result. | Completion and assessment details are saved with the correct learning status. | High | Positive | FR-20 |
| TC-027 | Allow assessment retry within the permitted limit | Employee fails an assessment but has remaining attempts. | System allows another attempt according to the configured retry policy and updates the attempt count. | Medium | Boundary | FR-21 |
| TC-028 | Prevent assessment retry after the permitted limit | Employee has reached the configured maximum number of assessment attempts and attempts another retry. | Further attempts are blocked and the status is updated to Retry Limit Reached. | High | Negative | FR-21 |
| TC-029 | Update skill profile after authorized certification | Employee passes the required assessment and receives certification. Authorized L&D user records the certification and updates the skill profile. | Certification is recorded and the skill profile is updated by an authorized user. | High | Positive | FR-22, BRL-11 |

### 5.6 Notifications and Management Reporting

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-030 | Notify employees when an opportunity is published | PM publishes an opportunity. | Eligible employees receive the configured notification. | Medium | Positive | FR-24 |
| TC-031 | Notify affected users about a staffing decision | RM confirms a staffing decision. | Relevant employees and authorized stakeholders receive the appropriate status notification. | High | Positive | FR-24 |
| TC-032 | Display management dashboard information | Management user opens the dashboard. | Dashboard displays authorized information about opportunities, employee availability, staffing outcomes, and learning status. | Medium | Positive | FR-25 |
| TC-033 | Verify dashboard data consistency | Management dashboard is compared with the corresponding underlying opportunity, staffing, and learning records. | Dashboard figures and statuses match the underlying records for the selected reporting period. | High | Positive | FR-25 |

### 5.7 Access Control and Data Privacy

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-034 | Verify role-based access | Users with PM, Employee, RM, L&D, and Management roles access the portal. | Each role can access only the functions and information permitted by its assigned permissions. | Critical | Positive | FR-13, FR-17, FR-25 |
| TC-035 | Prevent unauthorized access to employee personal information | User attempts to view restricted employee personal information without permission. | Access is denied or restricted fields are masked according to the approved privacy policy. | Critical | Negative | FR-13 |
| TC-036 | Verify audit trail for important actions | Authorized users create, modify, publish, withdraw, assess, or confirm records. | Relevant actions are recorded with user, action, and timestamp details in the audit trail. | High | Positive | FR-15, FR-17 |

### 5.8 Data Migration and Integration

| Test Case ID | Scenario | Preconditions and Test Steps | Expected Result | Priority | Test Type | Requirement Reference |
|---|---|---|---|---|---|---|
| TC-037 | Verify migrated employee and skill data | Approved employee and skill data is migrated or made available through the agreed integration. Compare selected records against the source. | Employee and skill information is transferred or retrieved accurately, with required data relationships maintained. | High | Positive | FR-07, FR-11 |
| TC-038 | Identify incomplete or duplicate employee records | Test data contains duplicate or incomplete employee and skill records. Execute the agreed data validation process. | Records are identified and handled according to the approved data quality and migration rules. | High | Exception | FR-11 |
| TC-039 | Verify employment-status data synchronization | Change an employee's notice-period or employment status in the approved source and perform the configured synchronization. | The portal reflects the updated status within the approved synchronization interval. | Critical | Integration | FR-09 |
| TC-040 | Handle data synchronization failure | Simulate failure while retrieving or synchronizing required employee information. | Failure is logged or reported, and the system avoids using incomplete or unreliable data for eligibility decisions. | High | Exception | FR-09, FR-11 |

## 6. Negative and Exception Test Cases

The following scenarios require particular attention because they involve business restrictions, incomplete information, or invalid workflow actions.

| Test Case ID | Scenario | Expected Result | Priority | Related Test Case |
|---|---|---|---|---|
| NTC-001 | Employee serving notice attempts to express interest. | System blocks the action and does not create an interest record. | Critical | TC-009 |
| NTC-002 | Employee attempts to express interest in a closed opportunity. | System prevents submission. | High | TC-011 |
| NTC-003 | Employee attempts to submit duplicate active interest. | Duplicate record is prevented. | High | TC-015 |
| NTC-004 | PM attempts to publish an opportunity without mandatory details. | Validation errors are displayed and publication is blocked. | High | TC-004 |
| NTC-005 | Unauthorized user attempts to confirm staffing. | Action is denied and no staffing status is changed. | Critical | TC-023 |
| NTC-006 | Employee information is unavailable during eligibility verification. | System does not assume eligibility; approved exception handling is applied. | Critical | TC-012 |
| NTC-007 | Employee attempts assessment retry after reaching the maximum limit. | Further attempt is blocked. | High | TC-028 |
| NTC-008 | User attempts to access restricted personal information. | Access is denied or restricted according to permissions. | Critical | TC-035 |
| NTC-009 | Data synchronization fails during an update. | Failure is handled without using unreliable data for eligibility decisions. | High | TC-040 |

## 7. Regression Testing

Regression testing should be performed whenever changes are introduced to business rules, employee eligibility, opportunity workflows, data integrations, or access permissions.

The following areas require regression coverage:

| Regression Area | Scenarios to Revalidate | Reason |
|---|---|---|
| Employee Eligibility | Notice-period restriction, active employment status, opportunity closing date | Changes to eligibility logic may affect employee participation. |
| Expression of Interest | Submit, duplicate prevention, withdraw | Changes may affect interest records and workflow status. |
| Skill Comparison | Mandatory and preferred skill comparison, gap identification | Changes to skill data or matching logic may affect suitability information. |
| RM Review | Assessment, shortlist, waitlist, staffing confirmation | Changes may affect staffing decisions and status transitions. |
| Learning Workflow | Enrolment, assessment, retries, certification, skill update | Changes may affect learning progress and readiness information. |
| Notifications | Opportunity publication, changes, withdrawal, staffing decisions | Changes may affect notification triggers and recipients. |
| Access and Privacy | Role permissions and employee information visibility | Changes may expose restricted information or allow unauthorized actions. |
| Reporting | Opportunity, staffing, availability, and learning dashboard figures | Changes may affect reporting accuracy. |
| Data Integration | Employee status, skill records, synchronization failures | Changes may affect data consistency and eligibility decisions. |

## 8. Test Execution Summary

Test execution results should be recorded for each test case during the testing cycle.

| Test Execution Metric | Description |
|---|---|
| Total Test Cases | Number of test cases planned for execution. |
| Executed | Test cases for which execution has been completed. |
| Passed | Test cases that produced the expected results. |
| Failed | Test cases that did not produce the expected results. |
| Blocked | Test cases that could not be executed due to dependencies or environment issues. |
| Not Run | Test cases that are yet to be executed. |

**Test Case Status Definitions**

| Status | Definition |
|---|---|
| Not Run | Testing has not started for the test case. |
| Pass | Actual result matches the expected result. |
| Fail | Actual result differs from the expected result. |
| Blocked | Execution cannot proceed because of an unresolved dependency or issue. |
| Retest Required | A defect has been fixed and the test case needs to be executed again. |

All test cases are initially considered Not Run. Actual execution results must be recorded during the testing cycle.

## 9. Defect Management

Any deviation between the expected and actual result must be recorded as a defect.

Each defect should contain:

- Defect ID.
- Related Test Case ID.
- Defect Summary.
- Steps to Reproduce.
- Expected Result.
- Actual Result.
- Severity and Priority.
- Reported By and Reported Date.
- Assigned Owner.
- Defect Status.
- Resolution Details.
- Retest Result.

Defects should be tracked through the agreed defect management process until they are resolved, retested, and closed.

## 10. Requirements Traceability

The test cases are mapped to the functional requirements documented in FRD v2.0.

| Functional Requirement | Requirement Description | Related Test Cases |
|---|---|---|
| FR-01 to FR-05 | Project opportunity management | TC-001 to TC-006 |
| FR-06 to FR-08 | Employee opportunity access and skill comparison | TC-007, TC-008, TC-013, TC-014 |
| FR-09 to FR-10 | Employee eligibility and expression of interest | TC-009 to TC-012, TC-015, TC-016 |
| FR-12 to FR-17 | Resource Manager review and staffing | TC-017 to TC-023 |
| FR-18 to FR-23 | Learning and Development | TC-024 to TC-029 |
| FR-24 | Notifications | TC-030, TC-031 |
| FR-25 | Management dashboards | TC-032, TC-033 |
| Access and Privacy Requirements | Role-based access, restricted information, and auditability | TC-018, TC-034 to TC-036 |
| Data Requirements | Employee and skill data migration, integration, and synchronization | TC-037 to TC-040 |

The Requirements Traceability Matrix (RTM) will provide detailed bidirectional mapping between business requirements, functional requirements, user stories, and test cases.

## 11. Assumptions and Open Questions

### 11.1 Assumptions

1. The enhanced Employee Management Portal will provide the required functions in the agreed test environment.
2. User roles and access permissions will be configured before test execution.
3. Employee availability, skill, and employment-status information will be available through approved data sources.
4. Notice-period information will be obtained from an authoritative source approved by the relevant stakeholders.
5. Assessment retry limits and certification rules will be configured based on L&D policy.
6. Notification channels and recipient rules will be agreed before notification testing.
7. Test data will be representative of the intended business scenarios and will not expose actual employee personal information.

### 11.2 Open Questions

| ID | Open Question | Impact on Testing |
|---|---|---|
| OQ-01 | Which system is the authoritative source for employee employment and notice-period status? | Determines the source for eligibility verification. |
| OQ-02 | How frequently must employment and notice-period information synchronize with the portal? | Determines synchronization and boundary test expectations. |
| OQ-03 | What should happen if an employee enters the notice period after expressing interest? | Determines whether the existing interest is withdrawn automatically or referred for RM review. |
| OQ-04 | What is the approved behaviour when employment-status information is unavailable or stale? | Determines exception handling and whether the action must be blocked. |
| OQ-05 | What are the approved assessment retry limits and certification criteria? | Determines learning workflow test data and expected results. |
| OQ-06 | Which notification channels and recipients are approved for each workflow event? | Determines notification test coverage. |
| OQ-07 | What employee information can each role view? | Determines access-control and privacy test expectations. |
| OQ-08 | What is the approved migration or integration approach for existing employee and skill data? | Determines data validation and integration test coverage. |
| OQ-09 | What are the expected user volume, concurrent usage, and performance targets? | Determines the required non-functional testing scope. |


