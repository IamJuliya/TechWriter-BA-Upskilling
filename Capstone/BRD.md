# Business Requirements Document (BRD)

## Project Opportunities & Talent Readiness Enhancement

**Organization:** ThinkPalm (case-study scenario)  
**Document Version:** 1.0  
**Status:** Draft for Review  
**Prepared by:** Mary Juliya  
**Role:** Business Analyst  
**Date:** 13 October 2026

---

## 1. Executive Overview

This project proposes an enhancement to ThinkPalm's existing employee management portal to improve the utilization of unallocated employees.

When employees are not assigned to projects, Resource Managers need visibility into upcoming project opportunities, required skills, and employee availability to identify suitable internal resources. Without a centralized process, employees may not know about upcoming opportunities, and suitable resources may remain unallocated while the organization considers external recruitment.

The proposed enhancement will allow Project Managers to publish upcoming project opportunities and their skill requirements. Employees can view opportunities and express interest, while Resource Managers can review employee skills, readiness, and availability before making staffing decisions.

The expected business benefits include improved resource utilization, better workforce planning, reduced dependency on unnecessary external recruitment, and optimized staffing costs.

## 2. Business Problem Statement

ThinkPalm may have employees who are temporarily unallocated or awaiting assignment to a new project. At the same time, upcoming projects may require skills that these employees already possess or could develop with appropriate training.

Without a structured way to communicate project opportunities and compare required skills with employee profiles, identifying suitable internal resources can be time-consuming. Employees may miss relevant opportunities, and Resource Managers may have difficulty assessing the available talent pool.

The organization needs a centralized process to make project opportunities visible, help identify suitable internal employees, and support informed staffing decisions.

## 3. Business Objectives

The primary objective is to **maximize the effective utilization of unallocated employees** by connecting them with suitable upcoming project opportunities.

The specific objectives are to:

1. Improve visibility into upcoming project opportunities and their required skills.
2. Help Resource Managers identify suitable internal employees based on skills, readiness, and availability.
3. Encourage unallocated employees to express interest in relevant opportunities.
4. Identify skill gaps and potential upskilling needs.
5. Reduce avoidable external recruitment by considering suitable internal resources first.
6. Improve resource allocation and support staffing-budget optimization.
7. Provide management with information to monitor resource utilization and opportunity engagement.

## 4. Project Scope

### 4.1 In Scope

- Enable Project Managers to create, edit, publish, and close or cancel project opportunities.
- Capture project details, required skills, expected start date, and interest deadline.
- Allow employees to view published opportunities and their skill requirements.
- Allow employees to express interest in and withdraw interest from opportunities within the permitted period.
- Display available employee skill information alongside project requirements.
- Highlight potential skill gaps or missing skill information.
- Allow Resource Managers to review employee skills, readiness, and availability.
- Record staffing review outcomes.
- Send notifications for relevant opportunity updates and review outcomes.
- Provide basic reports on opportunities, employee interest, and staffing outcomes.
- Apply role-based access to protect employee and project information.

### 4.2 Out of Scope

- Replacing or redesigning the entire employee management portal.
- Developing a complete Learning Management System (LMS).
- Automatically assigning employees to projects without human review.
- Replacing existing attendance, leave, payroll, insurance, or other unrelated portal modules.
- Integrating with external recruitment platforms or third-party systems unless approved separately.
- Guaranteeing recruitment-cost savings or automatic optimization of staffing budgets.

## 5. Stakeholders and Their Interests

| Stakeholder | Interest / Responsibility |
|---|---|
| Management | Improve resource utilization, workforce planning, and staffing-cost control. |
| Resource Manager | Identify suitable unallocated employees and coordinate staffing decisions. |
| Project Manager | Publish upcoming project opportunities and specify required skills. |
| Employees | Discover suitable opportunities, express interest, and identify skill gaps. |
| Learning and Development (L&D) | Understand recurring skill gaps and potential upskilling needs. |
| HR / Recruitment | Understand internal resource availability before initiating external recruitment. |
| Portal Administrator / IT | Maintain access control, data integrity, and system availability. |

## 6. Proposed Business Process

1. The Project Manager identifies an upcoming project and its resource requirements.
2. The Project Manager creates an opportunity in the employee management portal.
3. The opportunity is published with the required skills, expected start date, and interest deadline.
4. Employees view relevant opportunities and express interest if suitable.
5. The system displays available skill information and highlights potential gaps or missing data.
6. The Resource Manager reviews interested employees' skills, readiness, and availability.
7. The Resource Manager coordinates with the relevant stakeholders and records the staffing outcome.
8. If no suitable internal employee is available, the organization may consider upskilling, other internal options, or external recruitment according to its staffing process.

The final staffing decision remains with the authorized stakeholders.

## 7. Business Requirements

| ID | Business Requirement | Priority |
|---|---|---|
| BR-01 | The portal shall provide a centralized view of active, published project opportunities. | Must |
| BR-02 | The portal shall capture mandatory project information, including required skills, before publication. | Must |
| BR-03 | Employees shall be able to express interest in and withdraw interest from eligible opportunities before the deadline. | Must |
| BR-04 | The portal shall display required project skills alongside available employee skill information to support resource matching. | Must |
| BR-05 | Resource Managers shall be able to review employee skills, readiness, and availability before recording a staffing outcome. | Must |
| BR-06 | The portal should notify relevant users about important opportunity changes and review outcomes. | Should |
| BR-07 | The portal should provide basic reports on published opportunities, employee interest, and staffing outcomes. | Should |
| BR-08 | The portal shall restrict access to functions and information according to user roles. | Must |
| BR-09 | The enhancement should help improve the utilization of unallocated employees by making internal project opportunities and available skills more visible. | Must |
| BR-10 | The enhancement should provide information that helps management assess internal staffing options before considering external recruitment. | Should |

## 8. Success Criteria and Expected Benefits

The following are **proposed targets for stakeholder validation**, not existing performance figures.

| Success Measure | Proposed Target | Business Value |
|---|---|---|
| Opportunity engagement | At least 80% of eligible published opportunities receive one or more expressions of interest within 14 calendar days. | Improves visibility and engagement. |
| Resource Manager review | At least 90% of eligible opportunities receive an initial resource review within five business days of the agreed review point. | Supports timely staffing decisions. |
| Opportunity data quality | At least 95% of published opportunities contain all mandatory information and structured skill requirements. | Improves matching and review quality. |
| Resource utilization | Establish a baseline for unallocated employees and measure changes after implementation. | Helps assess whether the enhancement improves utilization. |
| Internal staffing | Track how many staffing outcomes use suitable internal employees. | Helps evaluate internal talent utilization. |
| Recruitment-cost optimization | Compare avoidable external recruitment costs against a validated baseline. | Helps assess potential staffing-budget benefits. |

Targets should be finalized after reviewing existing portal data, resource allocation practices, and management expectations.

## 9. Assumptions and Dependencies

### Assumptions

- ThinkPalm's existing employee management portal can be enhanced to support this process.
- Project Managers and Resource Managers will maintain accurate opportunity and staffing information.
- Employee skill profiles and availability information will be accessible to authorized users.
- Resource Managers will remain responsible for validating employee suitability and making or coordinating staffing decisions.

### Dependencies

- Availability and accuracy of employee skill data.
- Availability of upcoming project requirements and timelines.
- Agreement on how employee readiness and availability are defined.
- Agreement on role permissions, notification rules, and reporting needs.
- Availability of baseline data for measuring utilization and staffing-cost outcomes.

## 10. Constraints

- The enhancement must work within the approved scope and capabilities of the existing portal.
- Employee information must only be accessible to authorized users.
- Skill information may be incomplete or outdated and must be validated before staffing decisions.
- The project does not guarantee that every unallocated employee will receive a suitable assignment.
- Financial benefits depend on project demand, skill availability, staffing policies, and actual recruitment decisions.

## 11. Risks and Mitigation

| Risk | Potential Impact | Proposed Mitigation |
|---|---|---|
| Outdated employee skill profiles | Unsuitable matching or missed opportunities. | Encourage employees and relevant managers to review and update skill profiles. |
| Incomplete project requirements | Delays or poor matching. | Make essential opportunity fields mandatory. |
| Low employee engagement | Opportunities may not receive suitable interest. | Provide clear opportunity details and timely notifications. |
| Unclear readiness criteria | Inconsistent staffing decisions. | Define readiness criteria with Resource Managers and Project Managers. |
| Employee interest mistaken for confirmed availability | Delays or incorrect expectations. | Require Resource Manager validation before staffing confirmation. |
| Overestimating cost savings | Inaccurate business-benefit reporting. | Compare actual outcomes with an agreed baseline and approved cost assumptions. |
| Missing skill information interpreted as a skill gap | Suitable employees may be overlooked. | Display missing information separately from confirmed skill gaps. |

## 12. Business Rules

- Only authorized Project Managers or designated users may create and publish opportunities.
- An opportunity must contain all mandatory fields and at least one required skill before publication.
- The interest deadline must be valid and earlier than the project start date.
- Employees may express interest only in opportunities that are open for interest.
- An employee may have only one active interest record for the same opportunity.
- Employees may withdraw interest before the deadline, subject to the agreed business rules.
- Missing skill information must not automatically be treated as evidence that an employee lacks the skill.
- Expressing interest does not guarantee selection or assignment.
- Resource Managers must validate skills, readiness, and availability before confirming a staffing outcome.
- Cancelled or closed opportunities must not accept new expressions of interest.

## 13. Approval and Sign-Off

| Stakeholder / Role | Name | Status / Date |
|---|---|---|
| Business / Management Representative | To be confirmed | Pending |
| Resource Manager | To be confirmed | Pending |
| Project Manager Representative | To be confirmed | Pending |
| IT / Portal Representative | To be confirmed | Pending |

**Document Status:** Draft for Review. Requirements, success targets, assumptions, and business rules must be validated with the relevant stakeholders before approval.
