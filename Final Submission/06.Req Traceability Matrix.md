# Requirements Traceability Matrix (RTM)   -   Project Opportunities & Talent Readiness Enhancement
## Contents

- [1. Introduction](#1-introduction)
  - [1.1 Purpose](#11-purpose)
  - [1.2 Scope](#12-scope)
  - [1.3 Traceability Objectives](#13-traceability-objectives)
- [2. Traceability Approach](#2-traceability-approach)
- [3. Requirement Traceability Matrix](#3-requirement-traceability-matrix)
  - [3.1 Business Requirements to Functional Requirements](#31-business-requirements-to-functional-requirements)
  - [3.2 Business Rules to Functional Requirements](#32-business-rules-to-functional-requirements)
  - [3.3 Functional Requirements to User Stories](#33-functional-requirements-to-user-stories)
  - [3.4 User Stories to Functional Test Cases](#34-user-stories-to-functional-test-cases)
  - [3.5 Functional Requirements to Test Cases](#35-functional-requirements-to-test-cases)
- [4. Reverse Traceability](#4-reverse-traceability)
- [5. Traceability Coverage and Gap Analysis](#5-traceability-coverage-and-gap-analysis)
- [6. Change Impact Analysis](#6-change-impact-analysis)
- [7. Priority Definitions](#7-priority-definitions)
- [8. Traceability Status Definitions](#8-traceability-status-definitions)
- [9. Assumptions and Open Questions](#9-assumptions-and-open-questions)
- [10. Approval](#10-approval)

## 1. Introduction
**Document Note:** This RTM is prepared for the ThinkPalm Capstone case-study initiative. It establishes traceability across the proposed business and functional requirements, user stories, and functional test cases. Final traceability coverage depends on stakeholder validation, approved business rules, and confirmation of the supporting user story identifiers.

### 1.1 Purpose

The Requirements Traceability Matrix (RTM) establishes a structured relationship between business requirements, business rules, functional requirements, user stories, acceptance criteria, and functional test cases for the Project Opportunities & Talent Readiness Enhancement initiative.

It ensures that each identified business need is translated into functional requirements and verified through appropriate testing.

The RTM also supports change impact analysis, regression testing, requirement coverage assessment, and stakeholder review.

### 1.2 Scope

This RTM covers the Capstone project requirements, including:

- Project opportunity management.
- Employee opportunity access and eligibility.
- Skill comparison and identification of skill gaps.
- Expression and withdrawal of interest.
- Resource Manager review and staffing decisions.
- Learning, assessment, retries, and certification.
- Notifications and management reporting.
- Role-based access and employee data privacy.
- Data migration and integration considerations.

The Mini-project remains a focused foundation of the Capstone and is not treated as a separate set of Capstone requirements.

### 1.3 Traceability Objectives

1. Ensure all approved business requirements are represented in functional requirements.
2. Link functional requirements to relevant user stories and acceptance criteria.
3. Ensure user stories are supported by functional test cases.
4. Identify requirements without corresponding test coverage.
5. Identify test cases that do not have a valid requirement reference.
6. Support impact analysis when requirements or business rules change.
7. Identify regression test cases affected by a change.

## 2. Traceability Approach

The RTM follows a bidirectional traceability approach.

**Forward traceability:**

Business Requirement → Business Rule → Functional Requirement → User Story → Acceptance Criteria → Functional Test Case

**Backward traceability:**

Functional Test Case → User Story → Functional Requirement → Business Requirement / Business Rule

Forward traceability verifies that business needs are addressed by the solution and tested.

Backward traceability verifies that every implemented and tested function has a valid business justification.

The following identifiers are used:

| Requirement Type | Identifier | Example |
|---|---|---|
| Business Requirement | BR | BR-01 |
| Business Rule | BRL | BRL-01 |
| Functional Requirement | FR | FR-01 |
| User Story | US | US-01 |
| Functional Test Case | TC | TC-001 |
| Additional Test Coverage | TC | TC-041 |

## 3. Requirement Traceability Matrix

### 3.1 Business Requirements to Functional Requirements

The following matrix connects the business requirements in BRD v2.1 to the corresponding functional requirements in FRD v2.0.

| Business Requirement ID | Business Requirement | Related Functional Requirements | Coverage |
|---|---|---|---|
| BR-01 | Provide a centralized view of project opportunities. | FR-01, FR-03, FR-06 | Covered |
| BR-02 | Enable PMs to publish opportunities with required project details and skills. | FR-01, FR-02, FR-03, FR-04, FR-05 | Covered |
| BR-03 | Allow employees to view opportunities and compare their recorded skills with project requirements. | FR-06, FR-07, FR-08 | Covered |
| BR-04 | Allow eligible employees to express and withdraw interest. | FR-09, FR-10 | Covered |
| BR-05 | Enable RMs to review skills, experience, availability, and readiness. | FR-11, FR-12, FR-13, FR-14 | Covered |
| BR-06 | Enable RMs to record suitability decisions and manage shortlists and waitlists. | FR-14, FR-15 | Covered |
| BR-07 | Support skill-gap closure through L&D-led learning and assessment. | FR-18, FR-19, FR-20, FR-21 | Covered |
| BR-08 | Allow authorized L&D users to record course completion, assessment results, retries, and certifications. | FR-19, FR-20, FR-21, FR-22 | Covered |
| BR-09 | Ensure skill-profile updates following certification are authorized. | FR-22 | Covered |
| BR-10 | Require authorized RM confirmation for staffing outcomes. | FR-16, FR-17 | Covered |
| BR-11 | Notify affected users about relevant changes and process outcomes. | FR-24 | Covered |
| BR-12 | Provide management visibility into talent availability, staffing, and training. | FR-23, FR-25 | Covered |
| BR-13 | Support internal resource review before external recruitment is considered, according to approved policy. | FR-16, FR-17 | Covered |
| BR-14 | Control access to employee, project, assessment, and staffing information by role. | FR-06, FR-13, FR-18, FR-25 | Covered |
| BR-15 | Maintain traceability of relevant opportunity, review, learning, and staffing changes. | FR-14, FR-17, FR-20, FR-22, FR-24 | Covered |

### 3.2 Business Rules to Functional Requirements

This section ensures that business policies and restrictions are represented by enforceable system requirements.

| Business Rule ID | Business Rule | Related Functional Requirements | Validation / Test Reference |
|---|---|---|---|
| BRL-01 | An employee serving a notice period is not eligible to express interest in any internal project opportunity. | FR-09 | TC-009, TC-012 |
| BRL-02 | Only employees meeting approved eligibility conditions may participate in the opportunity process. | FR-06, FR-09 | TC-007, TC-010 |
| BRL-03 | Employees must meet the approved availability requirements for the proposed project start date. | FR-09, FR-11, FR-14 | TC-010, TC-019 |
| BRL-04 | Internal resource availability must be reviewed before external recruitment is considered. | FR-16, FR-17 | Additional coverage required |
| BRL-05 | Final staffing decisions must be made by an authorized RM or approved delegate. | FR-17 | TC-022, TC-023 |
| BRL-06 | Suitability must be assessed against mandatory requirements, verified skills, experience, and availability. | FR-07, FR-13, FR-14 | TC-013, TC-018, TC-019 |
| BRL-07 | Suitable employees who are not ready by the required date may be waitlisted, subject to the approved process. | FR-14, FR-15 | TC-020, TC-021 |
| BRL-08 | Mandatory and preferred skills must be treated as distinct categories. | FR-02, FR-07, FR-08 | TC-002, TC-013, TC-014 |
| BRL-09 | Skill verification must follow approved evidence and authorization rules. | FR-07, FR-11, FR-22 | TC-013, TC-029 |
| BRL-10 | Assessment attempts, pass criteria, and certification must follow approved L&D policies. | FR-20, FR-21, FR-22 | TC-026, TC-027, TC-028 |
| BRL-11 | Course completion or assessment success does not guarantee project staffing. | FR-17, FR-20, FR-22 | TC-026, TC-029 |
| BRL-12 | If employee eligibility changes after interest submission, continued participation must follow approved HR/RM policy. | FR-09, FR-10, FR-14 | Additional coverage required |
| BRL-13 | Employee personal information must be accessed and used only for authorized business purposes. | FR-13, FR-18, FR-25 | TC-018, TC-035 |
| BRL-14 | Financial benefits must be calculated using agreed definitions and validated baseline data. | FR-25 | Additional reporting validation required |

### 3.3 Functional Requirements to User Stories

The eight core user stories from the Mini-project are retained as the foundation of the Capstone. Additional Capstone stories represent the extended L&D, reporting, notification, and supporting workflows.

| User Story ID | User Story / Capability | Actor | Related Functional Requirements |
|---|---|---|---|
| US-01 | Create a project opportunity. | PM | FR-01 |
| US-02 | Publish an opportunity. | PM | FR-02, FR-03, FR-04, FR-05 |
| US-03 | View published opportunities. | Employee | FR-06 |
| US-04 | Compare recorded skills with opportunity requirements. | Employee | FR-07, FR-08 |
| US-05 | Express interest in an opportunity. | Employee | FR-09 |
| US-06 | Withdraw an expression of interest. | Employee | FR-10 |
| US-07 | Review interested employees. | RM | FR-11, FR-12, FR-13, FR-14, FR-15 |
| US-08 | Record a staffing outcome. | RM | FR-16, FR-17 |
| US-09 | Support learning based on identified skill gaps. | L&D | FR-18, FR-19 |
| US-10 | Record course completion and assessment results. | L&D | FR-20, FR-21 |
| US-11 | Record certification and update employee skill profiles. | L&D | FR-22 |
| US-12 | Review skill-gap information for training planning. | L&D | FR-23 |
| US-13 | Receive notifications about relevant workflow events. | System / Affected Users | FR-24 |
| US-14 | View talent, staffing, and training information. | Management | FR-25 |

US-09 to US-14 are Capstone extension identifiers for the additional capabilities. They distinguish the extended Capstone scope from the eight core Mini-project stories.

### 3.4 User Stories to Functional Test Cases

| User Story ID | User Story | Related Test Cases |
|---|---|---|
| US-01 | Create a project opportunity. | TC-001 |
| US-02 | Publish an opportunity. | TC-002, TC-003, TC-004, TC-005, TC-006 |
| US-03 | View published opportunities. | TC-007, TC-008 |
| US-04 | Compare recorded skills with opportunity requirements. | TC-013, TC-014 |
| US-05 | Express interest in an opportunity. | TC-009, TC-010, TC-011, TC-012, TC-015 |
| US-06 | Withdraw an expression of interest. | TC-016 |
| US-07 | Review interested employees. | TC-017, TC-018, TC-019, TC-020, TC-021 |
| US-08 | Record a staffing outcome. | TC-022, TC-023 |
| US-09 | Support learning based on identified skill gaps. | TC-024, TC-025 |
| US-10 | Record course completion and assessment results. | TC-026, TC-027, TC-028 |
| US-11 | Record certification and update employee skill profiles. | TC-029 |
| US-12 | Review skill-gap information for training planning. | Additional coverage required |
| US-13 | Receive notifications about relevant workflow events. | TC-030, TC-031 |
| US-14 | View talent, staffing, and training information. | TC-032, TC-033 |

Access control, privacy, and data integration are supporting system capabilities and are mapped directly to the functional requirements and test cases in Section 3.5.

### 3.5 Functional Requirements to Test Cases

This matrix establishes direct traceability from the FRD to the Functional Test Cases document.

| Functional Requirement ID | Functional Requirement | Related Test Cases | Coverage |
|---|---|---|---|
| FR-01 | Create Project Opportunity | TC-001 | Covered |
| FR-02 | Define Required Skills | TC-002 | Covered |
| FR-03 | Publish Opportunity | TC-003, TC-004 | Covered |
| FR-04 | Update Opportunity Details | TC-005 | Covered |
| FR-05 | Close or Cancel Opportunity | TC-006 | Covered |
| FR-06 | View Eligible Opportunities | TC-007, TC-008 | Covered |
| FR-07 | Compare Employee Skills | TC-013 | Covered |
| FR-08 | Identify Skill Gaps | TC-014 | Covered |
| FR-09 | Express Interest in an Opportunity | TC-009, TC-010, TC-011, TC-012, TC-015 | Covered |
| FR-10 | Withdraw Expression of Interest | TC-016 | Covered |
| FR-11 | Update Employee Readiness Information | Additional coverage required | Gap identified |
| FR-12 | View Interested Employees | TC-017 | Covered |
| FR-13 | Review Employee Information | TC-018, TC-035 | Covered |
| FR-14 | Record Suitability and Readiness Assessment | TC-019 | Covered |
| FR-15 | Manage Shortlist and Waitlist | TC-020, TC-021 | Covered |
| FR-16 | Support Unfilled Opportunity Handling | Additional coverage required | Gap identified |
| FR-17 | Confirm Staffing Decision | TC-022, TC-023 | Covered |
| FR-18 | Use Skill-Gap Information | TC-024 | Covered |
| FR-19 | Manage Learning Enrolment | TC-025 | Covered |
| FR-20 | Record Course Completion and Assessment | TC-026 | Covered |
| FR-21 | Manage Assessment Retries | TC-027, TC-028 | Covered |
| FR-22 | Record Certification and Update Skill Profile | TC-029 | Covered |
| FR-23 | Support Training Planning | Additional coverage required | Gap identified |
| FR-24 | Notify Affected Users | TC-030, TC-031 | Covered |
| FR-25 | Provide Management Dashboards | TC-032, TC-033 | Covered |

## 4. Reverse Traceability

Reverse traceability verifies that each test case is linked to a documented functional requirement and an approved business need.

| Test Case Range / ID | Test Coverage | Functional Requirement Reference | Business Requirement / Rule Reference |
|---|---|---|---|
| TC-001 | Opportunity creation | FR-01 | BR-02 |
| TC-002 to TC-006 | Opportunity publication and management | FR-02 to FR-05 | BR-02, BRL-01, BRL-02 |
| TC-007 to TC-012 | Employee access and eligibility | FR-06, FR-09 | BR-03, BR-04, BRL-01, BRL-02, BRL-03 |
| TC-013 to TC-016 | Skill comparison and employee interest | FR-07 to FR-10 | BR-03, BR-04, BRL-04, BRL-05, BRL-06, BRL-08 |
| TC-017 to TC-023 | RM review and staffing | FR-12 to FR-17 | BR-05, BR-06, BR-10, BR-13, BRL-05, BRL-06, BRL-07 |
| TC-024 to TC-029 | Learning and certification | FR-18 to FR-22 | BR-07, BR-08, BR-09, BRL-09, BRL-10, BRL-11 |
| TC-030 to TC-031 | Notifications | FR-24 | BR-11, BRL-12 |
| TC-032 to TC-033 | Management reporting | FR-25 | BR-12, BR-14, BRL-14 |
| TC-034 to TC-036 | Access control, privacy, and audit | FR-13, FR-17, FR-25 | BR-14, BR-15, BRL-05, BRL-13 |
| TC-037 to TC-040 | Data migration and integration | FR-07, FR-09, FR-11 | BR-03, BR-05, BR-14 |

A test case without a valid requirement reference must be reviewed before execution. It should either be linked to an existing requirement or supported by a formally approved new requirement.

## 5. Traceability Coverage and Gap Analysis

The current traceability review identifies the following coverage gaps between FRD v2.0 and Functional Test Cases v1.0.

| Gap ID | Requirement | Identified Gap | Additional Test Coverage Required |
|---|---|---|---|
| GAP-01 | FR-11 – Update Employee Readiness Information | No dedicated test case validates employee readiness updates. | Verify authorized readiness updates, invalid values, and status changes. |
| GAP-02 | FR-16 – Support Unfilled Opportunity Handling | No dedicated test case validates the internal review outcome when no suitable and ready resource is identified. | Verify unfilled opportunity handling and authorized external recruitment consideration. |
| GAP-03 | FR-23 – Support Training Planning | No dedicated test case validates aggregated skill-gap information for L&D planning. | Verify L&D access to aggregated skill-gap information and reporting accuracy. |
| GAP-04 | BRL-12 – Eligibility Changes After Interest Submission | Existing tests do not cover an employee entering a notice period after expressing interest. | Verify the approved withdrawal or RM review behaviour. |
| GAP-05 | BRL-04 – Internal Review Before External Recruitment | No direct test case validates that the internal review outcome is recorded before external recruitment is considered. | Verify the internal review and authorization sequence. |
| GAP-06 | BRL-14 – Validated Financial Reporting | Dashboard tests do not independently validate financial benefit calculations or approved baseline definitions. | Verify only approved and validated financial data is reported. |

### Additional Test Cases Required

The following test cases extend Functional Test Cases v1.0 to close the identified coverage gaps.

| Test Case ID | Scenario | Expected Result | Priority | Requirement Reference |
|---|---|---|---|---|
| TC-041 | Update employee readiness information | Authorized readiness and availability updates are saved and reflected in the relevant employee record. | High | FR-11 |
| TC-042 | Handle an unfilled project opportunity | RM records that no suitable and sufficiently ready internal resource was identified. External recruitment consideration is recorded only through the approved process. | High | FR-16, BRL-04 |
| TC-043 | Review aggregated skill-gap information for training planning | Authorized L&D users can view aggregated skill-gap information for training planning, subject to access restrictions. | Medium | FR-23 |
| TC-044 | Employee enters notice period after expressing interest | The system applies the stakeholder-approved action, such as automatic withdrawal or referral for RM review, and records the resulting status. | Critical | FR-09, FR-10, BRL-12 |
| TC-045 | Verify internal review before external recruitment consideration | System requires the internal review outcome to be recorded before an authorized user can proceed with the external recruitment consideration workflow. | High | FR-16, BRL-04 |
| TC-046 | Verify approved financial reporting information | Dashboard reports use approved definitions and validated baseline data; unvalidated financial benefits are not presented as confirmed savings. | Medium | FR-25, BRL-14 |

**Coverage note:** TC-041 to TC-046 are additional test cases proposed to close identified gaps. They are not included in the original 40 test cases and should be incorporated into the Functional Test Cases document before the final testing baseline is established.

## 6. Change Impact Analysis

The RTM supports impact analysis whenever a business requirement, business rule, or functional requirement changes.

The following example illustrates how a change can be traced across the solution.

**Example: Change to employee notice-period eligibility**

| Impact Area | Related Reference | Potential Impact |
|---|---|---|
| Business Rule | BRL-01 | Eligibility policy or restriction changes. |
| Functional Requirement | FR-09 | Interest-submission validation may require modification. |
| User Story | US-05 | Acceptance criteria for expressing interest may change. |
| Functional Test Cases | TC-009, TC-010, TC-012, TC-044 | Positive, negative, and exception scenarios must be reviewed and retested. |
| Regression Testing | Employee eligibility and interest workflow | Previously working submission and withdrawal behaviour must be revalidated. |
| Related Documents | BRD, FRD, User Stories, Functional Test Cases, RTM, UAT Plan | All impacted documents must be updated consistently. |

**Change impact process:**

1. Identify the changed requirement or business rule.
2. Locate all linked functional requirements in the RTM.
3. Identify affected user stories and acceptance criteria.
4. Identify impacted functional and UAT test cases.
5. Determine the regression test scope.
6. Update the relevant documents and maintain consistent version references.
7. Obtain the required stakeholder review and approval.

## 7. Priority Definitions

| Priority | Definition |
|---|---|
| Critical | Essential business restriction or process control. Failure may result in an invalid staffing decision, unauthorized action, or significant business risk. |
| High | Important functionality required for the core opportunity and staffing workflow. |
| Medium | Supporting functionality that improves process visibility, reporting, or operational efficiency. |
| Low | Enhancement with limited impact on the primary business workflow. |

## 8. Traceability Status Definitions

| Status | Definition |
|---|---|
| Covered | A requirement has a corresponding functional requirement, user story, or test case as applicable. |
| Partially Covered | Some aspects of the requirement are mapped, but additional traceability or testing is required. |
| Gap Identified | No adequate downstream requirement or test coverage has been established. |
| Not Applicable | The requirement does not require a separate mapping at that level, with the reason documented. |
| Pending Validation | The requirement, mapping, or expected behaviour requires stakeholder confirmation. |

## 9. Assumptions and Open Questions

### 9.1 Assumptions

1. BRD v2.1 and FRD v2.0 are the authoritative Capstone requirement documents.
2. The eight core user stories are retained from the Mini-project as the foundation of the Capstone.
3. Additional Capstone user story identifiers represent extended L&D, notification, and management reporting capabilities.
4. Functional Test Cases v1.0 contains the initial 40 test cases, with TC-041 to TC-046 proposed as additional coverage.
5. Requirement identifiers will remain consistent across the BRD, FRD, user stories, functional test cases, RTM, and UAT Plan.
6. All proposed rules and test expectations remain subject to stakeholder validation where approval is pending.

### 9.2 Open Questions

| ID | Open Question | Impact on Traceability |
|---|---|---|
| OQ-01 | What is the approved handling when an employee enters a notice period after expressing interest? | Finalizes BRL-12 and TC-044. |
| OQ-02 | Which source provides authoritative employment and notice-period information? | Confirms FR-09 and related test dependencies. |
| OQ-03 | What are the approved rules for internal review before external recruitment? | Finalizes BRL-04 and TC-042, TC-045. |
| OQ-04 | What information can each role view in the portal? | Confirms access-control and privacy coverage. |
| OQ-05 | What financial baseline and benefit definitions will management approve? | Finalizes BRL-14 and TC-046. |
| OQ-06 | Are the proposed Capstone user story identifiers aligned with the approved User Stories and Acceptance Criteria document? | Ensures consistent story-level traceability. |

## 10. Approval

| Role | Responsibility | Approval Status |
|---|---|---|
| Business Analyst | Prepared and maintained the RTM | Prepared |
| Management / Project Sponsor | Review business requirement coverage | Pending |
| Resource Manager | Validate staffing and eligibility traceability | Pending |
| Project Manager | Validate opportunity management traceability | Pending |
| L&D Representative | Validate learning and certification traceability | Pending |
