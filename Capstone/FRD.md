# Functional Requirements Document (FRD)

## Project Opportunities & Talent Readiness Enhancement

**Organization:** ThinkPalm (case-study scenario)  
**Version:** 1.0  
**Status:** Final Case-Study Submission  
**Prepared by:** Your Name  
**Date:** 13 October 2026

## 1. Purpose

This document defines the functional behavior required to support project opportunities, employee interest, resource review, learning, assessment, certification, staffing outcomes, notifications, and management reporting.

## 2. Scope

The system supports:

- Opportunity creation, validation, publication, updates, and closure.
- Mandatory and preferred skill definitions.
- Employee opportunity viewing, skill comparison, interest, and withdrawal.
- Availability and readiness updates.
- Resource Manager review, shortlisting, and waitlisting.
- L&D-led learning, assessment, retries, and certification.
- Authorized skill-profile updates.
- Staffing confirmation and outcome notifications.
- Management dashboards and role-based access.

Automatic staffing allocation and automatic recruitment initiation are excluded.

## 3. Actors

| Actor | System Activities |
|---|---|
| Project Manager | Creates and updates opportunities, defines skills, and publishes valid opportunities. |
| Employee | Views opportunities, compares skills, expresses or withdraws interest, and updates readiness. |
| Resource Manager | Reviews employees, records suitability/readiness, manages shortlist/waitlist, and confirms staffing. |
| L&D | Reviews skill gaps, records course enrollment and assessment results, and manages certification. |
| Management | Reviews authorized staffing, talent, and training reports. |
| Portal Administrator | Manages authorized system settings and access. |

## 4. Functional Requirements

### Opportunity Management

**FR-01 — Create Project Opportunity**  
The system shall allow an authorized Project Manager to create an opportunity with required project, role, and date information.

**FR-02 — Define Required Skills**  
The system shall allow the Project Manager to define mandatory and preferred skills.

**FR-03 — Publish Project Opportunity**  
The system shall validate mandatory information and allow authorized Project Managers to publish valid opportunities with a closing date. Publication must be blocked when mandatory information is missing.

**FR-04 — Update Project Requirements or Dates**  
The system shall allow authorized Project Managers to update active opportunity requirements and dates. Affected employees shall be notified when a change impacts their interest or readiness, and re-confirmation shall be indicated where required.

**FR-05 — Close Project Opportunity**  
The system shall allow an authorized Resource Manager to close an opportunity after the staffing outcome has been confirmed or the opportunity has otherwise been formally concluded.

### Employee Opportunity Experience

**FR-06 — View Eligible Projects**  
The system shall allow employees to view upcoming active opportunities according to the agreed eligibility and visibility rules.

**FR-07 — Compare Skills**  
The system shall display recorded employee skills alongside the mandatory and preferred skills required for an opportunity.

**FR-08 — Identify Skill Gaps**  
The system shall identify and display skills missing from the employee's recorded profile. Missing profile information must not automatically be treated as proof that an employee lacks a skill.

**FR-09 — Express Interest with Available Date**  
The system shall allow an employee to express interest in an active opportunity before its closing date and provide an available date.

**FR-10 — Withdraw Interest**  
The system shall allow an employee to withdraw submitted interest while the opportunity remains active, subject to the defined process.

**FR-11 — Update Readiness**  
The system shall allow employees to update required readiness information and make it available to authorized reviewers.

### Resource Manager Review and Staffing

**FR-12 — View Interested Employees**  
The system shall allow authorized Resource Managers to view employees who have expressed interest.

**FR-13 — Review Candidate Information**  
The system shall display relevant skills, experience, availability, readiness, and skill-gap information to authorized Resource Managers.

**FR-14 — Record Suitability and Readiness Decisions**  
The system shall allow authorized Resource Managers to record suitability and readiness decisions, including a reason or note where required.

**FR-15 — Manage Shortlist and Waitlist**  
The system shall allow authorized Resource Managers to shortlist suitable and ready employees and waitlist suitable employees who are not yet ready by the required date.

**FR-16 — Support Unfilled Opportunity Handling**  
The system shall allow an authorized Resource Manager to record that the internal review did not identify a suitable and sufficiently ready resource and that external recruitment may be considered under the approved policy. The system shall not initiate recruitment automatically.

**FR-17 — Confirm Selection and Allocate Resource**  
The system shall allow an authorized Resource Manager to confirm the selected employee and record the staffing outcome. The system must not allocate an employee without the required authorized confirmation.

### Learning and Development

**FR-18 — Use Skill-Gap Information**  
The system shall make relevant skill-gap information available to authorized L&D users.

**FR-19 — Enroll Employee in Tailored Course**  
The system shall allow authorized L&D users to record enrollment in a suitable course based on the identified skill gap.

**FR-20 — Record Course Completion and Assessment**  
The system shall allow authorized L&D users to record course completion and assessment results.

**FR-21 — Manage Assessment Retry**  
The system shall support assessment retries up to a configurable maximum. When the maximum is reached without a pass, the system shall record the result and support the approved next step.

**FR-22 — Certify and Update Skill Profile**  
The system shall allow authorized L&D users to record certification after the defined criteria are met and update the employee's skill profile through an authorized action.

**FR-23 — Plan Training from Skill-Gap Data**  
The system shall provide aggregated skill-gap information to authorized L&D users to support future training plans, subject to access rules.

### Notifications and Reporting

**FR-24 — Notify Affected Users**  
The system shall notify relevant users about defined events, including material opportunity changes, selection outcomes, and other approved process events.

**FR-25 — Management Dashboards**  
The system shall provide authorized management users with dashboards or reports covering talent availability, opportunity status, staffing outcomes, and training information.

## 5. Business Rules

1. Only authorized Project Managers can create and publish opportunities.
2. Mandatory opportunity information and required skills must be complete before publication.
3. New interest is accepted only while an opportunity is active and before the closing date.
4. Duplicate active interest for the same employee and opportunity is not permitted.
5. Withdrawal follows the defined opportunity status and process rules.
6. Skill comparison uses recorded employee skills and published project requirements.
7. Missing skill data must be distinguished from a confirmed skill gap.
8. Suitability and staffing decisions remain with authorized Resource Managers.
9. Shortlisting does not itself constitute final allocation.
10. External recruitment consideration follows the approved internal review and management policy.
11. Assessment retries follow a configurable maximum.
12. Certification and skill-profile updates require authorized L&D action.
13. Material changes affecting interest or readiness must be communicated to affected users.

## 6. Proposed Status Definitions

These statuses are proposed for the capstone and should be validated before implementation.

**Opportunity:** Draft, Published/Active, Closed, Cancelled.

**Employee interest/review:** Interested, Withdrawn, Under Review, Shortlisted, Waitlisted, Selected, Not Selected.

**Learning:** Not Started, Enrolled, In Progress, Assessment Failed, Assessment Passed, Certified, Retry Limit Reached.

Status changes must follow defined rules and retain relevant history.

## 7. Non-Functional Requirements

- **NFR-01 — Access Control:** Restrict functions and data according to assigned user roles.
- **NFR-02 — Privacy:** Protect employee, assessment, and staffing information from unauthorized access.
- **NFR-03 — Data Integrity:** Validate mandatory fields and prevent invalid state changes.
- **NFR-04 — Auditability:** Maintain traceability for relevant opportunity, interest, decision, learning, certification, and staffing changes.
- **NFR-05 — Usability:** Present requirements, skill comparisons, statuses, and next actions clearly.
- **NFR-06 — Performance:** Agree on response-time targets based on expected user volumes and technical constraints.
- **NFR-07 — Availability and Recovery:** Follow approved organizational availability, backup, and recovery standards.
- **NFR-08 — Maintainability:** Make configurable business rules maintainable by authorized administrators where technically feasible.

## 8. Acceptance Criteria

**AC-01 — Valid publication**  
Given all mandatory opportunity details and required skills are provided, when an authorized Project Manager publishes the opportunity, then it is published and made visible to eligible employees.

**AC-02 — Invalid publication**  
Given mandatory information is missing, when publication is attempted, then the system blocks publication and identifies the missing information.

**AC-03 — Skill comparison**  
Given an employee views an opportunity, when the skill comparison is displayed, then recorded employee skills are compared with mandatory and preferred skills, and missing profile data is distinguished from confirmed gaps.

**AC-04 — Interest submission**  
Given an opportunity is active and before its closing date, when an employee submits interest with the required available date, then the system records the interest.

**AC-05 — Duplicate interest**  
Given active interest already exists for an employee and opportunity, when the employee attempts to submit it again, then the system prevents a duplicate record.

**AC-06 — Withdrawal**  
Given an employee has expressed interest in an active opportunity, when the employee withdraws interest according to the process, then the withdrawal is recorded and relevant views are updated.

**AC-07 — Changed opportunity**  
Given a saved opportunity change affects an interested employee, when the change is processed, then the affected employee is notified and re-confirmation is indicated where required.

**AC-08 — RM decision**  
Given an authorized Resource Manager reviews an employee, when the RM records a suitability and readiness decision, then the decision is stored and available to authorized users.

**AC-09 — Waitlist**  
Given an employee is suitable but not ready by the required date, when the RM records the decision, then the employee can be waitlisted with a reason where required.

**AC-10 — Learning and retries**  
Given an employee is enrolled in a tailored course, when completion and assessment results are recorded, then the system updates learning status and enforces the configured retry limit.

**AC-11 — Certification**  
Given an employee meets the defined certification criteria, when an authorized L&D user records certification, then the system records it and updates the skill profile through the authorized process.

**AC-12 — Staffing confirmation**  
Given a staffing decision has been made, when an authorized Resource Manager confirms the selected employee, then the system records the outcome and notifies relevant users without performing an unauthorized allocation.

**AC-13 — External recruitment consideration**  
Given the internal review does not identify a suitable and sufficiently ready resource, when the authorized RM records the outcome, then the system records the reason and consideration of external recruitment without initiating recruitment automatically.

**AC-14 — Access control**  
Given a user lacks permission for a function, when the user attempts a restricted action, then the system denies the action and makes no unauthorized change.

**AC-15 — Management reporting**  
Given an authorized management user accesses a dashboard, when a reporting view is selected, then the system displays available opportunity, staffing, talent, and training information based on recorded data.

## 9. Key Exceptions

- Missing mandatory information prevents publication.
- Interest submitted after the closing date is rejected.
- Duplicate interest is prevented.
- Withdrawal before RM review is reflected in the candidate list.
- Changes to dates or requirements trigger appropriate notifications.
- Suitable but not-ready employees may be waitlisted.
- Reaching the assessment retry limit triggers the approved next step.
- No suitable internal resource results in a recorded unfilled outcome.
- Unauthorized changes are denied.
- Missing skill-profile information is distinguished from a confirmed skill gap.
- Closure or cancellation prevents invalid new interest.
- Course completion alone does not imply certification unless the defined criteria are met.

**Case-study note:** The functional requirements and proposed status definitions should be validated with stakeholders before a real implementation.
