# Business Requirements Document (BRD)

## Project Opportunities & Talent Readiness Enhancement
**Organization:** ThinkPalm (case-study scenario)  
**Prepared by:** Mary Juliya  
**Role:** Business Analyst  
**Version:** 1.0  
**Status:** Proposed for stakeholder review

## 1. Business Problem
Employees who are available or unallocated may not have clear visibility into upcoming project opportunities or the skills required for those projects. Resource Managers may need to identify suitable internal employees by gathering and comparing project requirements, employee skills, and availability. This can make internal staffing less efficient and delay the identification of skill gaps.

## 2. Business Objective
Provide a centralized way to publish upcoming project opportunities and required skills, enable eligible employees to review opportunities and express interest, and help Resource Managers assess interested employees before making staffing decisions.

## 3. Feature Ask
Enhance the existing Employee Management Portal so Project Managers can publish upcoming project opportunities with required skills and key dates, employees can review opportunities and express or withdraw interest, and Resource Managers can review interested employees and record a staffing outcome.

## 4. Stakeholders
| Stakeholder | Interest / Responsibility |
|---|---|
| Project Manager (PM) | Defines project opportunity details, required skills, and dates. |
| Employee | Reviews opportunities, compares skills, and expresses or withdraws interest. |
| Resource Manager (RM) | Reviews suitability, readiness, and availability; records staffing outcome. |
| Learning & Development (L&D) | Supports employees who need learning to close skill gaps. |
| Management | Reviews staffing and talent-readiness outcomes. |
| Portal / IT team | Implements access, workflow, notifications, and data handling. |

## 5. Scope

### In Scope
- Create and publish project opportunities with mandatory details and required skills.
- Display published opportunities to eligible employees.
- Allow employees to view required skills and compare them with recorded skills.
- Allow employees to express interest and withdraw interest before a defined cutoff or staffing decision.
- Enable Resource Managers to review interested employees and record a shortlist or staffing outcome.
- Provide relevant status notifications.
- Maintain appropriate role-based access to actions and employee information.

### Out of Scope
- Automatic employee allocation without Resource Manager confirmation.
- Automated recruitment or job-offer workflows.
- Full learning-management-system implementation.
- Payroll, attendance, leave, or other unrelated portal changes.
- AI-based ranking or automated hiring decisions.

## 6. Business Requirements
| BR ID | Requirement | Priority |
|---|---|---|
| BR-01 | The system shall provide a centralized list of published project opportunities to eligible employees. | Must Have |
| BR-02 | Project Managers shall be able to create and publish opportunities with required skills, project dates, and other mandatory details. | Must Have |
| BR-03 | Employees shall be able to review opportunity details and compare required skills with their recorded skills. | Must Have |
| BR-04 | Employees shall be able to express interest in an opportunity and withdraw it while withdrawal is permitted. | Must Have |
| BR-05 | Resource Managers shall be able to review interested employees' skills, readiness information, and availability. | Must Have |
| BR-06 | Resource Managers shall be able to record a shortlist and/or staffing outcome, with final allocation remaining under authorized human control. | Must Have |
| BR-07 | The system shall notify relevant users when key opportunity or interest statuses change. | Should Have |
| BR-08 | Access to publishing, employee-interest, and staffing actions shall be restricted according to assigned roles. | Must Have |

## 7. Proposed Success Measures
The following are proposed targets for stakeholder validation, not verified ThinkPalm performance data:
- At least 80% of eligible published opportunities receive one or more expressions of interest within 14 days.
- At least 90% of initial Resource Manager reviews are completed within five business days of the agreed review point.
- At least 95% of published opportunities pass mandatory data-completeness checks.
- Establish a baseline for internal staffing utilization, time-to-staff, and recruitment/training costs before assessing financial impact.

## 8. Assumptions and Constraints
### Assumptions
- The existing portal can be enhanced to support opportunity publishing and employee interest.
- Employee skill and availability information is available from an approved source and can be reviewed for accuracy.
- Stakeholders will define eligibility rules, mandatory fields, and withdrawal cutoffs before implementation.
- Resource Managers remain accountable for staffing decisions.

### Constraints
- The feature depends on accurate, current employee skill and availability data.
- Role permissions and employee data privacy must be respected.
- Financial savings cannot be assumed without a baseline and measured results.

## 9. Risks and Dependencies
| Risk / Dependency | Potential Impact | Proposed Response |
|---|---|---|
| Outdated employee skill profiles | Poor candidate matching | Define ownership and a process for employees to review/update skills. |
| Incomplete opportunity details | Employees cannot assess suitability | Require mandatory fields before publication. |
| Delayed RM review | Staffing decisions may be delayed | Agree review service targets and monitor overdue reviews. |
| Unclear withdrawal rules | Confusion after staffing progresses | Define the withdrawal cutoff and show it to employees. |
| Incorrect access permissions | Exposure or unauthorized changes | Validate role permissions and test restricted actions. |

## 10. Acceptance / Approval
This BRD is a case-study proposal. Business rules, targets, data sources, and scope must be validated with the relevant stakeholders before implementation. Approval should be recorded by the designated business owner and relevant representatives.
