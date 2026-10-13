# Business Requirements Document (BRD)

**Project Title:** Project Opportunities & Talent Readiness Enhancement  
**Organization:** ThinkPalm (case-study scenario)  
**Document Version:** 1.0  
**Status:** Draft for Review  
**Prepared by:** Business Analyst  
**Date:** 13 October 2026

---

## 1. Executive Overview

ThinkPalm may have employees available between project assignments while upcoming projects require specific skills. If project opportunities and employee skill information are not readily accessible through a common process, identifying suitable internal employees can take additional time and effort.

This proposal enhances the existing employee management portal to help Project Managers publish upcoming opportunities, allow employees to express interest, identify potential skill gaps, and enable Resource Managers to review employee suitability and availability before making staffing decisions.

The proposed enhancement aims to improve internal talent utilization, support employee upskilling, and help management make informed staffing decisions while potentially reducing unnecessary external recruitment costs.

## 2. Business Problem Statement

The current case-study scenario assumes that identifying suitable employees for upcoming projects may involve manual skill comparisons, availability checks, and communication between employees, Project Managers, and Resource Managers.

This approach can result in:

- Employees being unaware of upcoming project opportunities.
- Additional effort in identifying employees with relevant skills.
- Delays in staffing decisions.
- Limited visibility into employee skill gaps and upskilling needs.
- Potential external recruitment when suitable internal employees may be available.

A structured portal-based process could address these challenges by making opportunities and skill requirements visible and supporting a consistent employee review workflow.

## 3. Business Objectives

The objectives of the proposed enhancement are to:

1. Provide a centralized view of upcoming project opportunities.
2. Allow Project Managers to publish project requirements and required skills.
3. Enable employees to express or withdraw interest within the permitted period.
4. Help identify potential skill gaps by comparing project requirements with available employee skill information.
5. Enable Resource Managers to assess employee skills, readiness, and availability before making staffing decisions.
6. Improve utilization of existing employees and support workforce planning.
7. Provide measurable information about opportunity engagement, staffing outcomes, and internal talent utilization.

## 4. Project Scope

### 4.1 In Scope

- Creating, editing, publishing, closing, and cancelling project opportunities.
- Recording mandatory project details, required skills, project start dates, and interest deadlines.
- Displaying published opportunities to eligible employees.
- Allowing employees to express interest and withdraw interest before the deadline.
- Displaying skill comparisons using available employee profile data.
- Highlighting missing skill information without treating it as proof that an employee lacks a skill.
- Enabling Resource Managers to review employee skills, readiness, and availability.
- Recording staffing review statuses and outcomes.
- Providing relevant notifications to employees, Project Managers, and Resource Managers.
- Supporting role-based access to employee and candidate-review information.
- Providing basic reports on opportunities, employee interest, and staffing outcomes.

### 4.2 Out of Scope

- Replacing the existing employee management portal.
- Modifying unrelated modules such as attendance, leave, insurance, or tax management.
- Building a complete Learning Management System.
- Automating recruitment or final staffing decisions.
- Managing payroll, employee compensation, or client billing.
- Integrating with external systems unless separately approved.

## 5. Stakeholders and Their Interests

| Stakeholder | Interest / Responsibility |
|---|---|
| Employees | Discover opportunities, understand skill requirements, and express interest. |
| Project Managers | Publish accurate opportunities and define required skills. |
| Resource Managers | Review employee suitability, readiness, and availability and make staffing decisions. |
| Learning & Development | Identify recurring skill gaps and potential upskilling needs. |
| HR / Portal Owner | Ensure alignment with employee policies, data governance, and portal processes. |
| IT / Security Team | Implement functionality, access controls, notifications, and auditability. |
| Business Leadership | Improve delivery readiness, internal talent utilization, and staffing-cost management. |

## 6. Proposed Business Process

The proposed process follows these steps:

1. A Project Manager identifies an upcoming project opportunity.
2. The Project Manager enters project details, required skills, start date, and interest deadline.
3. The portal validates the mandatory information.
4. The Project Manager publishes the opportunity.
5. Eligible employees view the opportunity and its skill requirements.
6. Interested employees submit their interest before the deadline.
7. The portal displays available skill comparisons and potential gaps.
8. The Resource Manager reviews interested employees, including their skills, readiness, and availability.
9. The Resource Manager records the staffing outcome.
10. Relevant users receive notifications, and the outcome is available for reporting.

Final staffing decisions remain with authorized personnel; the portal supports the decision rather than making it automatically.

## 7. Business Requirements

| ID | Business Requirement | Priority |
|---|---|---|
| BR-01 | The portal shall provide a centralized view of active, published project opportunities for eligible employees. | Must |
| BR-02 | The portal shall require essential project details and at least one required skill before publication. | Must |
| BR-03 | Employees shall be able to express interest in an open opportunity and withdraw their interest before the deadline. | Must |
| BR-04 | The portal shall display required project skills alongside available employee skill information. | Must |
| BR-05 | The portal shall support Resource Manager review of employee skills, readiness, and availability before a staffing outcome is recorded. | Must |
| BR-06 | The portal shall notify relevant users about important opportunity and interest-status changes. | Should |
| BR-07 | The portal shall provide basic reporting on published opportunities, employee interest, and staffing outcomes. | Should |
| BR-08 | Access to employee profile and candidate-review information shall be controlled by user roles. | Must |
| BR-09 | The process shall support better utilization of existing employees and evidence-based workforce planning. | Should |

**Priority definitions**

- **Must:** Essential for the initial solution to meet its primary business objectives.
- **Should:** Valuable for improving the solution but may be prioritized after essential functionality.

## 8. Success Criteria and Business Benefits

The following are proposed targets for the pilot. They must be validated against actual business conditions before implementation.

| Success Measure | Proposed Target |
|---|---|
| Opportunity engagement | At least 80% of published opportunities receive one or more expressions of interest within 14 calendar days, where the response window allows it. |
| Resource Manager review | At least 90% of opportunities with interested employees receive an initial review within five business days of the agreed review point. |
| Opportunity data completeness | At least 95% of published opportunities contain all mandatory fields and structured required skills. |
| Internal talent utilization | Establish a baseline for the proportion of staffing outcomes filled by existing employees considered through the portal, then set an improvement target. |
| User experience | Collect feedback from employees and Resource Managers during the pilot and identify improvements. |

### Expected Business Benefits

- Better visibility of existing employee capabilities.
- Reduced manual effort in identifying potential candidates.
- More timely and informed staffing decisions.
- Earlier identification of potential employee upskilling needs.
- Improved workforce planning and internal mobility.
- Better information for evaluating whether internal staffing can reduce avoidable recruitment costs.

Any recruitment-cost savings must be calculated using an agreed baseline and a Finance-approved method. Savings are an expected possibility, not a guaranteed result.

## 9. Assumptions and Dependencies

### Assumptions

1. The existing employee portal can be enhanced without replacing its core functionality.
2. Employees, Project Managers, and Resource Managers can be assigned appropriate access roles.
3. Employee skill profiles can be accessed or maintained through an agreed process.
4. Resource Managers can obtain employee availability information.
5. Staffing decisions will continue to be made by authorized personnel.

### Dependencies

- Availability and accuracy of employee skill information.
- Agreement on how employee readiness and skill proficiency are defined.
- Agreement on opportunity visibility and eligibility rules.
- Availability of an approved notification channel.
- Confirmation of privacy, access-control, and audit requirements by HR and IT.
- Stakeholder agreement on pilot success measures and reporting definitions.

## 10. Constraints

- The proposed solution is an enhancement to the existing portal, not a replacement.
- Skill comparisons depend on the quality and freshness of employee profile information.
- The project scope excludes unrelated portal modules.
- Current-state workflow details and technical capabilities must be validated with actual stakeholders.
- Final staffing decisions must remain subject to the organization's approved management process.

## 11. Risks and Mitigation

| Risk | Potential Impact | Proposed Mitigation |
|---|---|---|
| Outdated employee skill profiles | Suitable employees may be overlooked, or unsuitable matches may be suggested. | Assign profile ownership and display the last-updated date. |
| Incomplete project requirements | Employees may express interest based on unclear expectations. | Validate mandatory fields and require structured skill information. |
| Low employee engagement | Opportunities may receive insufficient interest. | Provide clear notifications and monitor engagement measures. |
| Employee privacy concerns | Sensitive employee information may be exposed. | Enforce role-based access and audit key actions. |
| Unfair or unclear staffing decisions | Reduced employee trust in the process. | Use transparent review criteria and retain human decision-making. |
| Unverified cost-saving assumptions | Business benefits may be overstated. | Establish a baseline and validate financial calculations with Finance. |

## 12. Acceptance and Approval

This BRD is ready for stakeholder review when the business problem, objectives, scope, requirements, assumptions, risks, and proposed success measures are understood and agreed upon.

The names and approval statuses below are placeholders; approval must not be assumed until the relevant stakeholders have reviewed the document.

| Role | Name | Status |
|---|---|---|
| Business Sponsor | To be confirmed | Pending review |
| Resource Manager Representative | To be confirmed | Pending review |
| Project Manager Representative | To be confirmed | Pending review |
| HR / Portal Owner | To be confirmed | Pending review |
| IT Representative | To be confirmed | Pending review |

---

**Document End**

