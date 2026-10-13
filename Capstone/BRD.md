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

This project proposes an enhancement to ThinkPalm's existing employee management portal to improve the effective utilization of unallocated employees.

When employees are unallocated or awaiting assignment to a project, the organization needs a reliable way to identify upcoming project opportunities and match available employees with suitable resource requirements. Without a structured process, relevant opportunities may not be visible to employees, and Resource Managers may need to spend additional time identifying suitable internal candidates.

The proposed enhancement will allow Project Managers to publish upcoming project opportunities and specify the required skills, expected start dates, and interest deadlines. Employees can view opportunities and express interest, while Resource Managers can review employee skills, readiness, and availability before coordinating staffing decisions.

The enhancement is expected to improve internal resource utilization, support workforce planning, identify upskilling needs, and reduce avoidable external recruitment where suitable internal employees are available.

## 2. Business Problem Statement

The case-study scenario assumes that ThinkPalm may have employees who are temporarily unallocated while upcoming projects require resources with specific skills.

The current process for identifying suitable internal employees, communicating upcoming opportunities, and reviewing resource availability needs to be validated with stakeholders. If these activities depend heavily on manual coordination or information that is not centrally visible, suitable employees may be overlooked and staffing decisions may take longer than necessary.

This can result in employees remaining unallocated while project resource requirements are being addressed, potentially increasing staffing costs or creating unnecessary dependency on external recruitment.

The organization needs a structured process to make upcoming opportunities visible, compare project skill requirements with available employee information, and help Resource Managers make informed staffing decisions.

### 2.1 Current-State Understanding

The following is a preliminary understanding for the case study and must be validated with stakeholders.

1. An upcoming project creates a need for specific skills and resources.
2. The Resource Manager identifies employees who may be available for assignment.
3. Employee skills and project requirements are compared.
4. Suitable employees are identified for further review.
5. The Resource Manager coordinates the staffing decision.
6. If suitable internal resources cannot be identified, other staffing options, including external recruitment, may be considered.

**Information gap:** The actual tools, communication channels, average allocation time, number of unallocated employees, and recruitment costs are not yet confirmed.

## 3. Business Objectives

The primary objective is to **improve the effective utilization of unallocated employees by connecting them with suitable upcoming project opportunities**.

The supporting objectives are to:

1. Improve visibility into upcoming projects and their required skills.
2. Help Resource Managers identify suitable internal employees based on skills, readiness, and availability.
3. Encourage unallocated employees to explore relevant opportunities and express interest.
4. Identify skill gaps and potential upskilling opportunities.
5. Reduce avoidable external recruitment by considering suitable internal resources before recruiting externally.
6. Improve the speed and consistency of resource identification and staffing coordination.
7. Support management decisions using resource-utilization and staffing-outcome reports.
8. Provide measurable evidence of the enhancement's contribution to workforce planning and staffing-cost optimization.

## 4. Project Scope

### 4.1 In Scope

- Enhancing the existing employee management portal to support project opportunity management.
- Allowing authorized Project Managers to create, edit, publish, close, and cancel project opportunities.
- Capturing project details, required skills, expected start date, and interest deadline.
- Allowing employees to view published opportunities and express interest.
- Allowing employees to withdraw interest within the permitted period.
- Displaying available employee skill information alongside project requirements.
- Highlighting potential skill gaps and distinguishing them from missing skill information.
- Enabling Resource Managers to review skills, readiness, and availability.
- Recording staffing review outcomes.
- Sending notifications for important opportunity changes and review outcomes.
- Providing basic reports on opportunities, employee interest, and staffing outcomes.
- Applying role-based access and maintaining an appropriate history of important changes.
- Supporting internal resource utilization and identifying potential upskilling needs.

### 4.2 Out of Scope

- Replacing or redesigning the entire employee management portal.
- Replacing existing attendance, leave, payroll, insurance, or other unrelated portal modules.
- Developing a full Learning Management System (LMS).
- Automatically assigning employees to projects without human review.
- Automatically approving training or recruitment expenditure.
- Integrating with external recruitment platforms or other third-party systems unless approved separately.
- Guaranteeing a reduction in recruitment costs or a specific improvement in utilization without measured evidence.

## 5. Stakeholders and Responsibilities

| Stakeholder | Primary Interest / Responsibility |
|---|---|
| Management | Define business priorities, review resource-utilization outcomes, and assess staffing-cost benefits. |
| Resource Manager | Review available employees, validate readiness and availability, coordinate staffing decisions, and record outcomes. |
| Project Manager | Define project requirements, required skills, expected start dates, and interest deadlines; maintain accurate opportunity details. |
| Employees | Maintain accurate skill information where permitted, review opportunities, and express or withdraw interest. |
| Learning and Development (L&D) | Review recurring skill gaps and advise on relevant upskilling opportunities. |
| HR / Recruitment | Support internal staffing decisions and provide recruitment-cost information where available and authorized. |
| Portal Administrator / IT | Manage role-based access, system configuration, availability, and technical support. |
| Business Analyst | Elicit and document requirements, clarify business rules, manage requirement traceability, and coordinate stakeholder validation. |

Final ownership and approval responsibilities must be confirmed during stakeholder discussions.

## 6. Proposed Future-State Process

1. The Project Manager identifies an upcoming project and its resource requirements.
2. The Project Manager creates an opportunity and specifies required skills, expected start date, and interest deadline.
3. The system validates the mandatory information.
4. The Project Manager publishes the opportunity.
5. Employees view the opportunity and assess whether their skills and availability may be suitable.
6. Interested employees express interest through the portal.
7. The system displays available employee skill information and highlights potential gaps or missing data.
8. The Resource Manager reviews interested employees' skills, readiness, and availability.
9. The Resource Manager coordinates with the Project Manager and other relevant stakeholders.
10. The staffing outcome is recorded.
11. If a suitable internal employee is not available, other options, including upskilling or external recruitment, may be considered through the organization's approved process.
12. Management reviews available reports to assess resource utilization and staffing outcomes.

**Important:** Employee interest does not guarantee selection. Final staffing decisions remain with authorized stakeholders.

## 7. Business Requirements

| ID | Business Requirement | Priority |
|---|---|---|
| BR-01 | The portal shall provide a centralized view of active, published project opportunities. | Must |
| BR-02 | The portal shall capture mandatory project information, including at least one required skill, before publication. | Must |
| BR-03 | Employees shall be able to express interest in eligible opportunities and withdraw interest before the permitted deadline. | Must |
| BR-04 | The portal shall display required project skills alongside available employee skill information to support resource matching. | Must |
| BR-05 | Resource Managers shall be able to review employee skills, readiness, and availability before recording a staffing outcome. | Must |
| BR-06 | The portal should notify relevant users about important opportunity changes and review outcomes. | Should |
| BR-07 | The portal should provide basic reports on opportunities, employee interest, and staffing outcomes. | Should |
| BR-08 | The portal shall restrict access to functions and information according to assigned user roles. | Must |
| BR-09 | The enhancement shall support better utilization of unallocated employees by improving the visibility of project opportunities and internal skills. | Must |
| BR-10 | The enhancement should help management evaluate internal staffing options before considering external recruitment. | Should |
| BR-11 | The system should distinguish missing skill information from a confirmed skill gap. | Must |
| BR-12 | The system should maintain a traceable history of important opportunity changes and staffing outcomes, subject to approved access and retention rules. | Should |

**Priority definitions**

- **Must:** Essential for the initial solution to meet its core business objectives.
- **Should:** Important but potentially deferrable if agreed with stakeholders.

## 8. Success Criteria and Business Benefits

The targets below are proposed measures for stakeholder validation. They are not existing ThinkPalm performance figures.

| Success Measure | Proposed Measurement | Expected Business Benefit |
|---|---|---|
| Opportunity engagement | Percentage of eligible published opportunities receiving at least one expression of interest within 14 calendar days. Proposed target: at least 80%. | Improved visibility and employee engagement. |
| Resource review timeliness | Percentage of eligible opportunities receiving an initial Resource Manager review within five business days of the agreed review point. Proposed target: at least 90%. | Faster resource identification. |
| Opportunity data quality | Percentage of published opportunities containing all mandatory details and structured skill requirements. Proposed target: at least 95%. | More reliable resource matching. |
| Unallocated employee utilization | Measure changes in the number of unallocated employees and the time they remain unallocated against an agreed baseline. | Better workforce utilization. |
| Internal staffing outcomes | Track the number and percentage of staffing needs filled by suitable internal employees. | Better use of existing talent. |
| Upskilling opportunities | Track skill gaps identified and relevant upskilling actions recommended or completed, where data is available. | Improved employee readiness for future projects. |
| Recruitment-cost optimization | Estimate potentially avoided external recruitment costs using validated cost assumptions and actual staffing outcomes. | Better staffing-budget decisions. |

### 8.1 Measurement Approach

Before implementation, stakeholders should agree on the baseline period, data source, calculation method, reporting frequency, and target for each metric.

For example, an internal staffing outcome should count only when an employee is actually assigned or formally confirmed for a project—not merely when the employee expresses interest.

Potential recruitment savings must be calculated using agreed cost data and actual decisions. An internal assignment does not automatically mean the organization avoided a recruitment expense.

## 9. Assumptions and Dependencies

### 9.1 Assumptions

- The existing portal can be enhanced to support the proposed process.
- Upcoming project opportunities and required skills can be provided by authorized Project Managers.
- Employee skill and availability information can be accessed by authorized users.
- Employees may express interest, but Resource Managers retain responsibility for validating suitability.
- Staffing decisions will continue to follow existing organizational approval practices unless changes are explicitly approved.

### 9.2 Dependencies

- Accurate employee skill profiles and availability information.
- Timely updates to upcoming project requirements and dates.
- Agreement on skill definitions, proficiency levels, and readiness criteria.
- Confirmation of user roles and access permissions.
- Agreement on notification triggers and recipients.
- Availability of baseline data for resource utilization and staffing-cost analysis.
- Confirmation of technical feasibility within the existing portal.

## 10. Constraints

- The solution must remain within the approved enhancement scope and existing portal architecture.
- Employee and project information must be protected according to organizational policies.
- Incomplete or outdated skill data may limit matching accuracy.
- Expressing interest does not guarantee that an employee is suitable, available, or selected.
- The solution cannot guarantee that every unallocated employee will receive an assignment.
- Business benefits depend on project demand, skills, availability, and staffing decisions.
- Integration with other systems is not assumed unless separately approved.

## 11. Business Rules

| ID | Business Rule |
|---|---|
| BRL-01 | Only authorized users may create, edit, publish, close, or cancel project opportunities. |
| BRL-02 | An opportunity must contain all mandatory information and at least one required skill before publication. |
| BRL-03 | The interest deadline must be valid and earlier than the project start date. |
| BRL-04 | Employees may express interest only while an opportunity is open for interest. |
| BRL-05 | An employee may have only one active interest record for the same opportunity. |
| BRL-06 | Employees may withdraw interest before the deadline, subject to the approved process. |
| BRL-07 | Missing skill information must not automatically be treated as evidence that an employee lacks the skill. |
| BRL-08 | Employee interest does not constitute staffing approval or a confirmed project assignment. |
| BRL-09 | Resource Managers must validate skills, readiness, and availability before recording a confirmed staffing outcome. |
| BRL-10 | Closed or cancelled opportunities must not accept new expressions of interest. |
| BRL-11 | If important project details change after employees express interest, affected users must be informed according to the approved notification rules. |
| BRL-12 | Access to employee information and staffing outcomes must follow approved role permissions and data-handling policies. |

The exact behavior when deadlines are reached, start dates change, or an opportunity is cancelled must be confirmed during requirements validation.

## 12. Non-Functional Requirements

The following are proposed requirements. Specific measurable thresholds must be agreed with stakeholders and IT.

| ID | Category | Requirement |
|---|---|---|
| NFR-01 | Security | The system shall restrict access to opportunity-management functions and employee information according to approved user roles. |
| NFR-02 | Performance | Opportunity listings, details, and interest records should load within an agreed response-time target under expected usage. |
| NFR-03 | Availability | The enhancement should meet the existing portal's approved availability expectations. |
| NFR-04 | Data Quality | The system shall validate mandatory opportunity information and display missing employee skill information distinctly from confirmed gaps. |
| NFR-05 | Auditability | Important opportunity changes and staffing outcomes should be traceable to an authorized user and timestamp, subject to approved retention rules. |
| NFR-06 | Usability | Employees and managers should be able to complete their main tasks using clear labels, understandable statuses, and consistent navigation. |
| NFR-07 | Maintainability | Required skills, status values, and other configurable business rules should be maintainable through an approved process. |
| NFR-08 | Privacy | Employee information shall be displayed and retained according to approved organizational policies and access permissions. |

## 13. Risks and Mitigation

| Risk | Potential Impact | Proposed Mitigation |
|---|---|---|
| Outdated employee skill profiles | Suitable candidates may be overlooked or unsuitable matches may be suggested. | Establish a process for reviewing and updating skill profiles. |
| Incomplete project requirements | Resource matching and staffing may be delayed. | Validate mandatory fields before publication. |
| Low employee engagement | Opportunities may receive insufficient interest. | Provide clear project details and agreed notifications. |
| Unclear readiness criteria | Resource Managers may assess candidates inconsistently. | Define readiness criteria with relevant stakeholders. |
| Interest mistaken for availability | Employees may be considered available when they are committed elsewhere. | Require availability validation before staffing confirmation. |
| Unclear change-handling rules | Employees may act on outdated project information. | Define change, cancellation, and notification rules. |
| Overestimated cost savings | Business benefits may be reported inaccurately. | Use an agreed baseline, validated cost assumptions, and actual staffing outcomes. |
| Excessive access to employee information | Employee privacy may be affected. | Define and test role-based permissions. |

## 14. Open Questions and Decisions Log

These items must be clarified before final approval or documented as agreed assumptions.

| ID | Open Question | Suggested Stakeholder | Status |
|---|---|---|---|
| OQ-01 | What is the current process for identifying unallocated employees and matching them to projects? | Resource Manager | Open |
| OQ-02 | Where is employee skill information maintained, and who is responsible for keeping it accurate? | HR / Resource Manager / IT | Open |
| OQ-03 | How should skill proficiency and project readiness be defined? | Resource Manager / Project Manager | Open |
| OQ-04 | Which roles can view employee profiles, interest records, and staffing outcomes? | Management / HR / IT | Open |
| OQ-05 | What should happen when project requirements or start dates change after employees express interest? | Project Manager / Resource Manager | Open |
| OQ-06 | Which notification events and recipients are required? | Employees / Resource Manager / Project Manager | Open |
| OQ-07 | What baseline data is available for unallocated headcount, allocation time, internal staffing, and recruitment costs? | Management / HR / Finance | Open |
| OQ-08 | Which reports are essential, and how frequently should they be generated? | Management / Resource Manager | Open |
| OQ-09 | What response-time, availability, audit-retention, and privacy requirements apply? | IT / HR / Management | Open |
| OQ-10 | Who approves the final staffing outcome, and when should external recruitment be considered? | Management / Resource Manager / HR | Open |

## 15. Acceptance and Approval

The BRD may be considered ready for approval when:

- The business problem and primary objective are agreed upon.
- In-scope and out-of-scope items are confirmed.
- Business requirements and priorities are reviewed by stakeholders.
- Success measures and baseline-data collection are agreed upon.
- Critical business rules and access requirements are validated.
- Open questions affecting the initial scope are resolved or recorded as approved assumptions.
- The relevant stakeholders approve the document.

| Stakeholder / Role | Name | Approval Status / Date |
|---|---|---|
| Business / Management Representative | To be confirmed | Pending |
| Resource Manager | To be confirmed | Pending |
| Project Manager Representative | To be confirmed | Pending |
| HR / Recruitment Representative | To be confirmed | Pending |
| IT / Portal Representative | To be confirmed | Pending |

**Document Status:** Draft for Review.

**Next Step:** Validate the open questions and baseline measures with stakeholders, then finalize the BRD. The approved BRD will serve as the baseline for the Functional Requirements Document (FRD), Process Flow diagrams, UAT Test Plan, and Requirements Traceability Matrix (RTM).
