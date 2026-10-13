# User Acceptance Testing (UAT) Test Plan

## Project Opportunities & Talent Readiness Enhancement

**Organization:** ThinkPalm (case-study scenario)  
**Version:** 1.0  

**Prepared by:** Mary Juliya 

**Status:** Planned for UAT

## 1. Purpose

This document defines the user acceptance tests required to verify that the enhanced Employee Management Portal supports the agreed business and functional requirements.

## 2. UAT Objectives

- Verify that authorized users can complete their assigned activities.
- Confirm mandatory-field validation and business rules.
- Test employee interest, withdrawal, and skill comparison.
- Verify Resource Manager review and staffing decisions.
- Test L&D enrollment, assessment, retry, and certification activities.
- Confirm notification behavior and management reporting.
- Verify that unauthorized actions are blocked.
- Confirm that staffing allocation remains under authorized human control.

## 3. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| UAT Coordinator | Organizes testing and records results. |
| Business Representative | Confirms business behavior and acceptance. |
| Project Manager | Tests opportunity creation, publication, and updates. |
| Employee | Tests opportunity viewing, skill comparison, interest, withdrawal, and readiness updates. |
| Resource Manager | Tests candidate review, shortlist/waitlist, and staffing outcomes. |
| L&D Representative | Tests learning, assessment, retries, and certification. |
| Management Representative | Reviews management dashboards. |
| Technical Team | Investigates defects and implements fixes. |

## 4. Test Environment and Preconditions

- UAT environment is available.
- Test accounts exist for the relevant user roles.
- Test opportunities include valid, incomplete, active, closed, and changed records.
- Employee profiles include complete, incomplete, suitable, and skill-gap scenarios.
- Training courses and assessment outcomes are available for testing.
- Assessment retry limits are configured or documented for the test.
- Notifications can be verified in the test environment.
- Test data is prepared without unnecessarily exposing real employee information.

## 5. UAT Test Cases

| Test ID | Requirement(s) | Test Scenario | Expected Result |
|---|---|---|---|
| UAT-01 | FR-01, FR-02 | Authorized PM creates an opportunity and defines mandatory and preferred skills. | Opportunity details and skill requirements are saved correctly. |
| UAT-02 | FR-03 | PM publishes an opportunity with all mandatory fields completed. | Opportunity is published and visible to eligible employees. |
| UAT-03 | FR-03 | PM attempts publication with a mandatory field or skill missing. | Publication is blocked and missing information is identified. |
| UAT-04 | FR-04, FR-24 | PM changes dates or required skills after employees have expressed interest. | The change is saved and affected employees are notified; re-confirmation is indicated where required. |
| UAT-05 | FR-05 | Authorized RM closes an opportunity after the outcome is confirmed. | Opportunity status changes to Closed and the outcome is recorded. |
| UAT-06 | FR-06 | Employee views upcoming opportunities. | Only opportunities permitted by eligibility and visibility rules are shown. |
| UAT-07 | FR-07, FR-08 | Employee compares recorded skills with opportunity requirements. | Matching skills and gaps are displayed, and missing profile data is not treated as a confirmed skill gap. |
| UAT-08 | FR-09 | Employee submits interest before the closing date. | Interest and available date are saved. |
| UAT-09 | FR-09 | Employee attempts to express interest after the closing date or on a closed opportunity. | New interest is rejected with an appropriate message. |
| UAT-10 | FR-09 | Employee attempts to submit duplicate interest. | Duplicate interest is prevented. |
| UAT-11 | FR-10, FR-24 | Employee withdraws interest while the opportunity is active. | Withdrawal is recorded and relevant views are updated. |
| UAT-12 | FR-11 | Employee updates readiness information. | Updated information is saved and visible to authorized reviewers. |
| UAT-13 | FR-12, FR-13 | RM opens the interested-employee list and reviews a candidate. | Relevant skills, experience, availability, readiness, and gaps are displayed according to access rules. |
| UAT-14 | FR-14 | RM records suitability and readiness decisions. | The decision and required supporting notes are recorded. |
| UAT-15 | FR-15 | RM waitlists a suitable employee who is not ready by the required date. | Waitlist status and applicable reason are recorded. |
| UAT-16 | FR-16 | RM records that no suitable and sufficiently ready internal resource is available. | Internal review outcome is recorded; external hiring may be considered without automatic recruitment initiation. |
| UAT-17 | FR-17, FR-24 | RM confirms a staffing outcome. | Selected employee and outcome are recorded, and relevant users are notified. |
| UAT-18 | FR-18, FR-19 | L&D reviews a skill gap and enrolls an employee in a tailored course. | Relevant gap information is available and enrollment is recorded. |
| UAT-19 | FR-20 | L&D records course completion and assessment result. | Learning status and assessment result are updated correctly. |
| UAT-20 | FR-21 | Employee fails an assessment and retries within the configured limit. | Retry is permitted according to the configuration and the result is recorded. |
| UAT-21 | FR-21 | Employee reaches the maximum number of assessment attempts without passing. | Further retries are restricted and the approved next step is recorded. |
| UAT-22 | FR-22 | Authorized L&D user records successful certification. | Certification is recorded and the skill profile is updated through the authorized process. |
| UAT-23 | FR-23 | L&D reviews aggregated skill-gap information. | Authorized L&D users can access information needed for training planning. |
| UAT-24 | FR-24 | A configured opportunity, review, or staffing event triggers a notification. | The appropriate affected users receive the notification. |
| UAT-25 | FR-25 | Management opens talent, staffing, and training dashboards. | Dashboard information matches the recorded data and access permissions. |
| UAT-26 | Relevant restricted functions | An unauthorized user attempts a restricted action. | Access is denied and no unauthorized change occurs. |
| UAT-27 | FR-10, FR-12 | Employee withdraws interest before RM review is complete. | Withdrawal is reflected in the RM's candidate view and remains traceable. |
| UAT-28 | FR-05, FR-06, FR-09 | Opportunity is closed or cancelled while an employee attempts to submit interest. | Invalid interest is prevented and the current opportunity status is shown. |

## 6. Test Execution Record

For every test, record:

| Field | Description |
|---|---|
| Test ID | Unique identifier from the test-case table. |
| Actual Result | What happened during execution. |
| Status | Not Run, Pass, Fail, or Blocked. |
| Evidence | Screenshot, log, or evidence reference. |
| Defect ID | Reference to a defect, if applicable. |
| Tester | Person who executed the test. |
| Execution Date | Date the test was performed. |
| Comments | Additional observations or retest details. |

**Status definitions**

- **Not Run:** Testing has not started for this case.
- **Pass:** Actual behavior matches the expected result.
- **Fail:** Actual behavior does not match the expected result.
- **Blocked:** Testing cannot proceed because of a dependency or issue.

## 7. Defect Management

1. Record the failed test and actual behavior.
2. Describe the defect and include supporting evidence.
3. Assign the defect to the responsible team.
4. Fix and retest the affected functionality.
5. Record the retest outcome.
6. Close the defect only when the agreed resolution criteria are met.

## 8. Entry Criteria

- Requirements and test cases have been reviewed.
- The UAT environment and test accounts are available.
- Required test data is prepared.
- The functionality is ready for business testing.

## 9. Exit Criteria

- All critical test cases have been executed.
- Critical and high-severity defects are resolved or formally accepted by authorized stakeholders.
- Failed tests are retested after fixes.
- Results and supporting evidence are recorded.
- Business acceptance and any outstanding concerns are documented.

## 10. UAT Sign-Off

| Role | Name | Decision / Date |
|---|---|---|
| Business Representative | To be confirmed | Pending UAT |
| Resource Manager Representative | To be confirmed | Pending UAT |
| L&D Representative | To be confirmed | Pending UAT |
| UAT Coordinator | To be confirmed | Pending UAT |

**Note:** This is a planned UAT document. Do not mark test cases as passed until they have actually been executed and verified.
