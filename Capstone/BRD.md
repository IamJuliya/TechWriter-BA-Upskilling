# Business Requirements Document (BRD)

## Project Opportunities & Talent Readiness Enhancement

**Organization:** ThinkPalm (case-study scenario)  
**Version:** 1.0  
**Status:** Final Case-Study Submission  
**Prepared by:** Mary Juliya 
**Role:** Business Analyst  
**Date:** 13 October 2026

## 1. Executive Summary

This project proposes an enhancement to ThinkPalm's existing Employee Management Portal to improve visibility into upcoming project opportunities and employee readiness.

Project Managers will publish project opportunities and required skills. Employees can review opportunities, compare their recorded skills, identify gaps, and express interest. Resource Managers can assess employee suitability, availability, and readiness before confirming staffing decisions.

The Learning and Development (L&D) team can support skill-gap closure through tailored learning, assessments, and certification. Management can review talent availability, staffing progress, and training outcomes.

The enhancement aims to improve internal resource utilization and support consideration of suitable internal employees before external recruitment. Any financial benefits will be measured using agreed baseline data rather than assumed savings.

## 2. Business Problem

Employees who are available or unallocated may not always have visibility into upcoming project opportunities or the skills required for those projects. Resource Managers may need to collect and compare employee skills, availability, and readiness information from different sources.

This can delay the identification of suitable internal resources. Employees may also lack clarity about the skills they need to develop to become suitable for upcoming opportunities.

## 3. Business Objectives

1. Provide a centralized view of upcoming project opportunities.
2. Enable Project Managers to publish project requirements and required skills.
3. Help employees compare their skills with project requirements and identify gaps.
4. Enable Resource Managers to review and shortlist suitable internal employees.
5. Support targeted learning and assessment through L&D.
6. Improve visibility into internal talent availability before considering external recruitment.
7. Provide management with information about staffing progress, talent readiness, and training outcomes.

## 4. Scope

### 4.1 In Scope

- Creating, updating, publishing, and closing project opportunities.
- Defining mandatory and preferred skills.
- Viewing relevant opportunities.
- Comparing employee skills with project requirements.
- Identifying skill gaps.
- Expressing and withdrawing interest.
- Recording availability and readiness information.
- Reviewing candidates and recording suitability decisions.
- Managing shortlists and waitlists.
- Sharing relevant skill-gap information with L&D.
- Course enrollment, completion, assessments, retries, and certification.
- Authorized skill-profile updates.
- Confirming staffing outcomes and notifying affected users.
- Recording when external recruitment may be considered.
- Management dashboards and reporting.
- Role-based access and relevant audit records.

### 4.2 Out of Scope

- Automatic staffing allocation without authorized Resource Manager confirmation.
- End-to-end recruitment and hiring.
- Salary, compensation, or promotion decisions.
- Performance appraisal.
- Automatic training assignment without L&D involvement.
- Full workforce capacity planning.
- Guaranteeing financial savings.

## 5. Stakeholders

| Stakeholder | Responsibility / Interest |
|---|---|
| Management | Reviews talent utilization, staffing progress, training outcomes, and financial impact. |
| Project Manager | Creates opportunities and defines skills, dates, and project requirements. |
| Resource Manager | Reviews candidates, assesses suitability and readiness, manages shortlists/waitlists, and confirms staffing. |
| Employee | Views opportunities, expresses interest, updates readiness, and participates in learning activities. |
| L&D | Supports skill development, course enrollment, assessment, and certification. |
| Portal Administrator / IT | Supports access control, system configuration, and technical implementation. |

## 6. Current-State Understanding

The current-state process is a preliminary case-study assumption, not a verified description of ThinkPalm's internal procedures.

Potential challenges include:

- Project opportunities and employee information may be communicated or maintained through different channels.
- Resource Managers may need to compare project requirements with employee skills and availability manually.
- Employees may have limited visibility into upcoming opportunities.
- Skill gaps and learning needs may require separate coordination.
- Management may need to consolidate information to understand internal talent availability.

These assumptions would require stakeholder validation in a real implementation.

## 7. Proposed Future-State Process

1. The Project Manager creates an opportunity and defines its requirements.
2. The system validates mandatory details before publication.
3. Employees view relevant opportunities and compare their recorded skills.
4. Interested employees submit their interest and available date.
5. Resource Managers review skills, experience, availability, and readiness.
6. Suitable and ready employees may be shortlisted. Suitable employees who need more preparation may be waitlisted.
7. Relevant skill gaps are shared with L&D.
8. L&D supports tailored learning, assessment, and certification.
9. Authorized skill-profile updates support readiness reassessment.
10. The Resource Manager confirms the staffing outcome.
11. The system updates status and notifies affected users.
12. Management reviews staffing and training information.

Staffing decisions remain under authorized human control.

## 8. Business Requirements

| ID | Business Requirement |
|---|---|
| BR-01 | Provide a centralized view of upcoming project opportunities. |
| BR-02 | Ensure mandatory project, role, date, and skill information is available before publication. |
| BR-03 | Enable employees to view relevant opportunities and compare their recorded skills with requirements. |
| BR-04 | Enable employees to express and withdraw interest according to the defined process. |
| BR-05 | Enable Resource Managers to review skills, experience, availability, and readiness. |
| BR-06 | Enable Resource Managers to record suitability decisions and manage shortlists and waitlists. |
| BR-07 | Support skill-gap closure through L&D-led learning and assessment. |
| BR-08 | Allow authorized L&D users to record course completion, assessment results, retries, and certifications. |
| BR-09 | Ensure skill-profile updates following certification are authorized. |
| BR-10 | Require authorized Resource Manager confirmation for staffing outcomes. |
| BR-11 | Notify affected users about relevant changes and process outcomes. |
| BR-12 | Provide management visibility into talent availability, staffing, and training. |
| BR-13 | Support internal resource review before external recruitment is considered, according to approved policy. |
| BR-14 | Control access to employee, project, assessment, and staffing information by role. |
| BR-15 | Maintain traceability of relevant opportunity, review, learning, and staffing changes. |

## 9. Proposed Success Measures

These are proposed targets for stakeholder validation, not actual ThinkPalm performance results.

| Measure | Proposed Target | Measurement |
|---|---|---|
| Opportunity engagement | At least 80% of eligible published opportunities receive interest within 14 days. | Opportunity and interest records. |
| Initial RM review | At least 90% of reviews are completed within five business days of the agreed review point. | Review timestamps. |
| Opportunity data quality | At least 95% of published opportunities meet mandatory data checks. | Validation records. |
| Internal resource utilization | Establish a baseline and track internal staffing outcomes. | Staffing and availability records. |
| Learning effectiveness | Track course completion, assessment pass rates, certification, and readiness reassessment. | L&D records. |
| Financial impact | Compare relevant recruitment and staffing costs against an agreed baseline. | Approved finance data and cost definitions. |

## 10. Business Rules

- **BRL-01:** Only authorized Project Managers may create and publish opportunities.
- **BRL-02:** Mandatory project details and required skills must be completed before publication.
- **BRL-03:** Interest can be submitted only while an opportunity is active and before its closing date.
- **BRL-04:** Duplicate active interest for the same employee and opportunity is not permitted.
- **BRL-05:** Withdrawal is permitted according to the agreed process and opportunity status.
- **BRL-06:** Skill comparison uses recorded employee skills and published project requirements.
- **BRL-07:** Suitability and staffing decisions remain with authorized Resource Managers.
- **BRL-08:** Suitable employees who are not ready by the required date may be waitlisted where the process permits.
- **BRL-09:** External recruitment may be considered when the internal review does not identify a suitable and sufficiently ready resource, according to management policy.
- **BRL-10:** Assessment retries follow a configurable, approved limit.
- **BRL-11:** Skill-profile updates following certification require authorized action.
- **BRL-12:** Material changes affecting employee interest or readiness must be communicated to affected users.

## 11. Assumptions and Dependencies

### Assumptions

- The existing portal can be enhanced to support the proposed workflow.
- Employee skill and availability data can be accessed by authorized users.
- PM, RM, employee, and L&D responsibilities will be defined.
- Management will define the internal staffing and external recruitment policy.
- L&D will define learning, assessment, certification, and retry rules.
- Proposed targets will be validated before implementation.

### Dependencies

- Reliable employee and skill-profile data.
- Agreed role permissions and visibility rules.
- Defined opportunity statuses and transitions.
- Agreed notification events and channels.
- Approved courses, assessments, and certification criteria.
- Availability of staffing, training, and financial data for reporting.

## 12. Constraints

- Employee information must be protected through appropriate access controls.
- Staffing decisions remain human-controlled.
- The enhancement does not replace the recruitment process.
- Financial benefits cannot be confirmed without a measured baseline.
- Integration with other systems depends on technical feasibility and authorization.

## 13. Risks and Mitigations

| Risk | Mitigation |
|---|---|
| Incomplete or outdated skill profiles | Define profile ownership and an authorized update process. |
| Employees miss opportunities | Provide a centralized opportunity view and agreed notifications. |
| Project requirements change after interest is submitted | Notify affected employees and request re-confirmation where required. |
| Training does not make an employee ready in time | Track learning progress and reassess readiness. |
| Delayed Resource Manager review | Define review milestones and monitor them. |
| Sensitive information is exposed | Apply role-based access and trace relevant changes. |
| Financial benefits are overstated | Use agreed financial definitions and baseline data. |
| Waitlist or assessment rules are unclear | Obtain stakeholder approval before implementation. |

## 14. Open Questions for Stakeholder Validation

- **OQ-01:** Which opportunity fields and skills are mandatory?
- **OQ-02:** How is employee eligibility for an opportunity determined?
- **OQ-03:** Which employee information is visible to each role?
- **OQ-04:** What are the expected Resource Manager review timelines?
- **OQ-05:** What rules govern waitlisting and readiness reassessment?
- **OQ-06:** Which notifications are required and through which channels?
- **OQ-07:** What is the maximum number of assessment attempts?
- **OQ-08:** Who can update skill profiles following certification?
- **OQ-09:** What policy determines when external recruitment can be considered?
- **OQ-10:** Which data sources and cost definitions will be used to measure utilization and financial impact?

## 15. Approval

| Role | Name | Status |
|---|---|---|
| Business Sponsor | To be confirmed | Pending stakeholder validation |
| Resource Manager Representative | To be confirmed | Pending stakeholder validation |
| L&D Representative | To be confirmed | Pending stakeholder validation |
| Business Analyst | Your Name | Prepared for case-study submission |

**Case-study note:** The current-state description, targets, and assumptions require validation before use in a real implementation. The approval table is a template and does not imply actual stakeholder approval.
