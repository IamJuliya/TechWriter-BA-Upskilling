# Requirements Traceability Matrix (RTM)

## Project Opportunities & Talent Readiness Enhancement

**Organization:** ThinkPalm (case-study scenario)  
**Version:** 1.0  
**Status:** Planned for UAT

## 1. Purpose

The RTM maps each business requirement to the relevant functional requirements and UAT test cases. It supports requirement coverage, change tracking, and verification that the proposed solution meets business needs.

## 2. Traceability Matrix

| BR ID | Business Requirement Summary | FR ID(s) | UAT Test ID(s) | Priority | Test Status |
|---|---|---|---|---|---|
| BR-01 | Centralized project opportunities | FR-01, FR-03, FR-05, FR-06 | UAT-01, UAT-02, UAT-05, UAT-06 | Must Have | Not Run |
| BR-02 | Complete project and skill information | FR-01, FR-02, FR-03, FR-04 | UAT-01, UAT-02, UAT-03, UAT-04 | Must Have | Not Run |
| BR-03 | Employee opportunity view and skill comparison | FR-06, FR-07, FR-08 | UAT-06, UAT-07 | Must Have | Not Run |
| BR-04 | Express and withdraw interest | FR-09, FR-10 | UAT-08, UAT-09, UAT-10, UAT-11, UAT-27, UAT-28 | Must Have | Not Run |
| BR-05 | RM review of candidate information | FR-11, FR-12, FR-13, FR-14 | UAT-12, UAT-13, UAT-14 | Must Have | Not Run |
| BR-06 | Shortlists and waitlists | FR-14, FR-15 | UAT-14, UAT-15 | Must Have | Not Run |
| BR-07 | L&D support for skill gaps | FR-08, FR-18, FR-19 | UAT-07, UAT-18 | Must Have | Not Run |
| BR-08 | Course, assessment, retry, and certification records | FR-20, FR-21, FR-22 | UAT-19, UAT-20, UAT-21, UAT-22 | Must Have | Not Run |
| BR-09 | Authorized skill-profile updates | FR-22 | UAT-22, UAT-26 | Must Have | Not Run |
| BR-10 | Human-confirmed staffing outcomes | FR-05, FR-14, FR-17 | UAT-05, UAT-14, UAT-17 | Must Have | Not Run |
| BR-11 | Notifications to affected users | FR-04, FR-10, FR-17, FR-24 | UAT-04, UAT-11, UAT-17, UAT-24 | Must Have | Not Run |
| BR-12 | Management talent, staffing, and training reports | FR-23, FR-25 | UAT-23, UAT-25 | Should Have | Not Run |
| BR-13 | Internal review before external hiring consideration | FR-16, FR-17 | UAT-16, UAT-17 | Must Have | Not Run |
| BR-14 | Role-based access and privacy | FR-01 to FR-25, particularly restricted actions | UAT-26 | Must Have | Not Run |
| BR-15 | Traceable opportunity, review, learning, and staffing changes | FR-04, FR-05, FR-10, FR-14, FR-17, FR-20, FR-22 | UAT-04, UAT-05, UAT-11, UAT-14, UAT-17, UAT-19, UAT-22 | Must Have | Not Run |

## 3. Priority Definitions

- **Must Have:** Required for the core process, essential business control, or safe operation.
- **Should Have:** Important to business value but potentially deferrable with stakeholder approval.

## 4. Status Definitions

- **Not Run:** The test has not been executed.
- **Pass:** The test has been executed and the expected result was achieved.
- **Fail:** The actual result did not meet the expected result.
- **Blocked:** Testing cannot proceed because of a dependency or issue.

## 5. RTM Maintenance Rules

1. Keep BR IDs aligned with the BRD.
2. Keep FR IDs aligned with the FRD.
3. Keep UAT IDs aligned with the UAT Test Plan.
4. Update traceability if an approved requirement changes.
5. Do not mark tests as passed before execution.
6. Review the RTM to identify business requirements that lack functional coverage or UAT tests.
7. Treat role-based access and auditability as cross-cutting controls across applicable functions.

**Submission note:** The table can be copied into Excel with each column retained separately. Test statuses remain **Not Run** until actual UAT execution.
